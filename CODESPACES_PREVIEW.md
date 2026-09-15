# Codespaces で GitHub Pages をプレビューする

GitHub Pages へ公開する前に、任意のブランチの表示を GitHub Codespaces で確認する手順です。初めて使うとき、確認を終えるとき、同じ Codespace を再び使うときの順に説明します。

この手順で作成する Ruby、Jekyll、生成済みサイトは Codespace の一時領域へ置きます。リポジトリやローカル PC の環境は変更しません。

> [!NOTE]
> 実際の確認時には、Codespace に最初から入っていた Ruby のバージョンが `github-pages` gem と合わず、`rbenv`も入っていませんでした。そのため、この手順では`rbenv`を一時領域へ導入し、動作を確認できた Ruby `3.1.6`を明示的に使用します。この対応も以下の初回手順に含まれています。

## 1. 初めて Codespaces を使うとき

### Codespace を作成する

1. GitHub でこのリポジトリを開きます。
2. 画面左上のブランチ名を選び、表示を確認したいブランチへ切り替えます。
3. **Code**を選びます。
4. **Codespaces**タブを選びます。
5. **Create codespace on ＜ブランチ名＞**を選びます。
6. ブラウザー上で VS Code のような画面が開くまで待ちます。

以降のコマンドは、Codespace 画面下部の bash ターミナルへ貼り付けて実行します。

### ブランチを確認する

```bash
git branch --show-current
```

表示された名前が、確認したいブランチ名と同じであることを確認します。

### Ruby のビルド環境を準備する

次のコマンドで、Rubyを作成するために必要なパッケージをCodespaceへ追加します。

```bash
sudo apt-get update
sudo apt-get install -y \
  build-essential \
  libssl-dev \
  libreadline-dev \
  zlib1g-dev \
  libyaml-dev \
  libffi-dev \
  libgdbm-dev \
  libncurses-dev \
  libdb-dev \
  uuid-dev
```

### rbenv と Ruby 3.1.6 を準備する

次のコマンドで、`rbenv`とRubyをCodespaceの一時領域へ導入します。

```bash
git clone --depth 1 \
  https://github.com/rbenv/rbenv.git \
  /tmp/rbenv

git clone --depth 1 \
  https://github.com/rbenv/ruby-build.git \
  /tmp/rbenv/plugins/ruby-build

export RBENV_ROOT=/tmp/rbenv
export PATH="$RBENV_ROOT/bin:$PATH"
eval "$(rbenv init - bash)"

rbenv install -s 3.1.6
rbenv shell 3.1.6
ruby --version
```

Rubyの作成には数分かかる場合があります。最後に`ruby 3.1.6`と表示されれば成功です。

### Jekyll を準備する

次のコマンドで、一時的な設定ファイルと必要なgemを`/tmp/cel-preview`へ準備します。

```bash
mkdir -p /tmp/cel-preview

printf '%s\n' \
  'source "https://rubygems.org"' \
  'gem "github-pages", group: :jekyll_plugins' \
  'gem "webrick"' \
  > /tmp/cel-preview/Gemfile

gem install bundler

export BUNDLE_GEMFILE=/tmp/cel-preview/Gemfile
export BUNDLE_PATH=/tmp/cel-preview/vendor/bundle
bundle install
```

`bundle install`には数分かかる場合があります。

### プレビューを起動する

```bash
bundle exec jekyll serve \
  --source "$PWD" \
  --destination /tmp/cel-preview/_site \
  --host 0.0.0.0 \
  --port 4000 \
  --baseurl ""
```

ターミナルに`Server running`と表示されたら、Codespace画面下部の**PORTS**タブを開き、ポート`4000`の地球アイコンを選びます。ポートが表示されない場合は、**Add port**を選択して`4000`を入力します。

ブラウザーにGitHub Pagesと同様の画面が表示されます。Markdownファイルを変更した場合は、ブラウザーを再読み込みして確認します。

## 2. 確認を終えたとき

Codespaceは削除せず、停止して残しておけます。停止するとCPUの利用時間としては加算されませんが、ストレージ料金が発生する場合があります。組織の保持期間や自動削除の設定にも注意してください。

1. Jekyllを実行しているターミナルを選びます。
2. `Ctrl+C`を押してJekyllを停止します。
3. 次のコマンドを実行します。

```bash
git status --short
```

何も表示されなければ、リポジトリに意図しない変更はありません。変更が表示された場合は、内容を確認してからCodespaceを停止します。

4. <https://github.com/codespaces>を開きます。
5. 使用したCodespaceの右側にある**...**を選びます。
6. **Stop codespace**を選びます。

**Delete**は選ばないでください。削除すると、次回はCodespaceの作成と初回セットアップからやり直す必要があります。

## 3. 同じ Codespace を再び使うとき

### Codespace を再開する

1. <https://github.com/codespaces>を開きます。
2. 前回使用したCodespaceの名前を選びます。
3. Codespaceが開くまで待ちます。
4. 新しいターミナルを開きます。

### 一時環境が残っているか確認する

同じCodespaceを停止して再開した場合でも、`/tmp`の内容が残ることは保証されません。まず次のコマンドで確認します。

```bash
test -d /tmp/rbenv && test -d /tmp/cel-preview && echo "準備済み" || echo "初回セットアップが必要"
```

- `準備済み`と表示された場合は、次の「環境を有効にして起動する」へ進みます。
- `初回セットアップが必要`と表示された場合は、「1. 初めて Codespaces を使うとき」の「Ruby のビルド環境を準備する」からやり直します。

### 環境を有効にして起動する

新しいターミナルでは環境変数がリセットされるため、次のコマンドを実行します。Rubyやgemを再インストールする必要はありません。

```bash
export RBENV_ROOT=/tmp/rbenv
export PATH="$RBENV_ROOT/bin:$PATH"
eval "$(rbenv init - bash)"
rbenv shell 3.1.6

export BUNDLE_GEMFILE=/tmp/cel-preview/Gemfile
export BUNDLE_PATH=/tmp/cel-preview/vendor/bundle

bundle exec jekyll serve \
  --source "$PWD" \
  --destination /tmp/cel-preview/_site \
  --host 0.0.0.0 \
  --port 4000 \
  --baseurl ""
```

`Server running`と表示されたら、**PORTS**タブからポート`4000`を開きます。

## 別のブランチを確認する場合

同じCodespaceで別のブランチも確認できます。Jekyllを`Ctrl+C`で停止してから、次を実行します。

```bash
git status --short
git switch ＜確認するブランチ名＞
```

`git status --short`で何か表示された場合は、ブランチを切り替える前に変更内容を確認してください。切り替え後は「環境を有効にして起動する」のコマンドでJekyllを起動します。

各利用者のCodespaceは独立しています。他の利用者も、確認したいブランチから自分のCodespaceを作成し、この手順を実行してください。