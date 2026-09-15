# Codespaces で GitHub Pages をプレビューする

GitHub Pages へ公開する前に、任意のブランチの表示を GitHub Codespaces で確認する手順です。Jekyll の実行環境は Codespace の一時領域に作成するため、リポジトリやローカル PC の環境は変更しません。

## Codespace を作成する

1. GitHub でこのリポジトリを開きます。
2. プレビューするブランチへ切り替えます。
3. **Code**、**Codespaces**、**Create codespace on ＜ブランチ名＞**の順に選択します。
4. Codespace のターミナルで、対象ブランチを確認します。

```bash
git branch --show-current
```

## 初回だけ実行する

以下のコマンドは Codespace の bash ターミナルで実行します。

### Ruby のビルド環境を準備する

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

### rbenv と Ruby 3.1 を一時領域へインストールする

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

Ruby のインストールには数分かかる場合があります。`ruby 3.1.6` と表示されれば準備完了です。

### Jekyll の依存関係を一時領域へインストールする

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

## プレビューを起動する

リポジトリのルートで次を実行します。

```bash
bundle exec jekyll serve \
  --source "$PWD" \
  --destination /tmp/cel-preview/_site \
  --host 0.0.0.0 \
  --port 4000 \
  --baseurl ""
```

`Server running` と表示されたら、Codespace 下部の **PORTS** タブからポート `4000` をブラウザーで開きます。ポートが自動表示されない場合は、**Add port**を選択して `4000` を追加してください。

Jekyll の起動中に Markdown ファイルを変更するとページが自動生成されます。ブラウザーを再読み込みして確認してください。

## Codespace を再開したとき

同じ Codespace の `/tmp/rbenv` と `/tmp/cel-preview` が残っていれば、Ruby や gem を再インストールする必要はありません。新しいターミナルでは環境変数だけを設定し直してから、Jekyll を起動します。

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

`/tmp/rbenv` または `/tmp/cel-preview` がなくなっている場合は、「初回だけ実行する」からやり直してください。

## 別のブランチを確認する

Jekyll を `Ctrl+C` で停止してから、ブランチを切り替えて再度起動します。

```bash
git status --short
git switch ＜確認するブランチ名＞
```

未コミットの変更がある場合は、ブランチを切り替える前に内容を確認してください。Ruby と Jekyll の再インストールは不要です。

## チームメンバーと共有する

転送されたポートは、初期状態では自分だけが閲覧できます。**PORTS** タブでポート `4000` を右クリックし、**Port Visibility**から組織内または公開の範囲を選択します。

- **Private to Organization**: 同じ組織のメンバーへ共有する
- **Public**: URL を知っている人へ公開する

組織のポリシーによって選択できる範囲は異なります。機密情報を含むページを **Public** にしないでください。

## 終了する

Jekyll を実行しているターミナルで `Ctrl+C` を押します。Codespace を削除すると、`/tmp` に作成した Ruby、Jekyll、生成済みサイトも削除されます。

リポジトリに意図しない変更がないことは、次のコマンドで確認できます。

```bash
git status --short
```

何も表示されなければ、作業ツリーはクリーンです。