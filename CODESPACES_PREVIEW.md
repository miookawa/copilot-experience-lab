# Codespaces で GitHub Pages をプレビューする

GitHub Pages へ公開する前に、任意のブランチの表示を GitHub Codespaces で確認する手順です。初めて使うとき、確認を終えるとき、同じ Codespace を再び使うときの順に説明します。

Codespace に最初から入っている Ruby を使用し、Jekyll と生成済みサイトは Codespace のホームディレクトリへ置きます。リポジトリやローカル PC の環境は変更しません。

> [!NOTE]
> ホームディレクトリに作成した環境は、同じ Codespace を停止して再開しても保持されます。Codespace を削除した場合やコンテナを再構築した場合は、初回セットアップからやり直してください。

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

### Ruby を確認する

Codespace に最初から入っている Ruby を確認します。

```bash
ruby --version
gem --version
```

両方のバージョンが表示されれば、次へ進みます。

### Jekyll を準備する

次のコマンドで、設定ファイルと必要な gem を Codespace のホームディレクトリへ準備します。

```bash
export GEM_HOME="$(ruby -e 'print Gem.user_dir')"
export PATH="$GEM_HOME/bin:$PATH"

gem install --user-install bundler --no-document

mkdir -p "$HOME/.local/share/cel-preview"

printf '%s\n' \
  'source "https://rubygems.org"' \
  'gem "github-pages", "232", group: :jekyll_plugins' \
  'gem "webrick"' \
  > "$HOME/.local/share/cel-preview/Gemfile"

export BUNDLE_GEMFILE="$HOME/.local/share/cel-preview/Gemfile"
export BUNDLE_PATH="$HOME/.local/share/cel-preview/vendor/bundle"
bundle install
```

`bundle install`には数分かかる場合があります。Ruby Sassなどのサポート終了に関する案内が表示されても、最後までエラーなく完了すれば問題ありません。

### プレビューを起動する

```bash
mkdir -p "$HOME/.cache/cel-preview"

bundle exec jekyll serve \
  --source "$PWD" \
  --destination "$HOME/.cache/cel-preview/_site" \
  --host 0.0.0.0 \
  --port 4000 \
  --baseurl ""
```

ターミナルに`Server running`と表示されたら、Codespace画面下部の**PORTS**タブを開き、ポート`4000`の地球アイコンを選びます。ポートが表示されない場合は、**Add port**を選択して`4000`を入力します。

ブラウザーにGitHub Pagesと同様の画面が表示されます。Markdownファイルを変更した場合は、ブラウザーを再読み込みして確認します。

## 2. 確認を終えたとき

Codespaceは削除せず、停止して残しておけます。停止するとCPUの利用時間としては加算されませんが、ストレージ料金が発生する場合があります。組織の保持期間や自動削除の設定にも注意してください。

### Jekyllを停止して変更を確認する

1. Jekyllを実行しているターミナルを選びます。
2. `Ctrl+C`を押してJekyllを停止します。
3. 次のコマンドを実行します。

```bash
git status --short
```

何も表示されなければ、リポジトリに意図しない変更はありません。変更が表示された場合は、内容を確認してからCodespaceを停止します。

### Codespaceを停止する

Codespaceのブラウザー画面を閉じるだけでは、Codespaceはすぐには停止しません。次の手順で明示的に停止します。

1. 別のブラウザータブで<https://github.com/codespaces>を開きます。
2. リポジトリ名とブランチ名を確認し、使用したCodespaceを見つけます。
3. Codespaceの右側にある**...**を選びます。
4. **Stop codespace**を選びます。
5. 状態が**Stopped**に変わったことを確認します。

**Delete**は選ばないでください。削除すると、次回はCodespaceの作成と初回セットアップからやり直す必要があります。

## 3. 同じ Codespace を再び使うとき

### Codespace を再開する

1. <https://github.com/codespaces>を開きます。
2. 前回使用したCodespaceの名前を選びます。
3. Codespaceが開くまで待ちます。
4. 新しいターミナルを開きます。

### ブランチを最新の状態にする

同じCodespaceを再開しても、リモートブランチの更新は自動では取り込まれません。まず次のコマンドを実行します。

```bash
git status --short
```

何も表示されなければ、次のコマンドで最新の状態を取り込みます。

```bash
git pull --ff-only
```

変更が表示された場合は、内容を確認してから取り込み方法を決めてください。そのまま`git pull`すると、Codespace内の変更と競合する場合があります。

### 環境を有効にして起動する

新しいターミナルでは環境変数がリセットされるため、次のコマンドを実行します。Rubyや gem を再インストールする必要はありません。

```bash
export GEM_HOME="$(ruby -e 'print Gem.user_dir')"
export PATH="$GEM_HOME/bin:$PATH"

export BUNDLE_GEMFILE="$HOME/.local/share/cel-preview/Gemfile"
export BUNDLE_PATH="$HOME/.local/share/cel-preview/vendor/bundle"

bundle exec jekyll serve \
  --source "$PWD" \
  --destination "$HOME/.cache/cel-preview/_site" \
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