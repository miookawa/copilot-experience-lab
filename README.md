# Copilot Experience Lab

Microsoft Copilot を試すための日本語の体験コンテンツ集です。
**実業務のデータ**で実施する体験と、**用意されたサンプルデータ**で実施する体験があります。

## このラボの考え方

このリポジトリは、**体験**と**進行の台本**の 2 層でできています。

| 層 | フォルダー | 役割 |
| --- | --- | --- |
| 体験 | `contents/` | 体験の実体。1 体験 1 ファイルで、製品・シーン別のカテゴリに配置 |
| 進行プログラム | `programs/` | 体験の順番・必須/選択・運営ルールだけを持ち、体験は相対リンクで参照 |


> **体験の中身は `contents/` にのみ置きます。`programs/` にコンテンツを複製しないでください。**
> プログラムは「どの体験を、どの順で実施してもらうか」だけを持ちます。この分担が、このラボの設計の中心です。

## 想定する読者と使い方

この GitHub リポジトリは、主に Microsoft Copilot をお客様へ提案し、導入や活用を支援する**パートナー**を想定しています。Copilot の提案・拡販活動に合わせて Clone または Fork し、体験内容、進行プログラム、サンプルデータへの導線などを改変して利用できます。

一方、体験に参加する**エンドユーザー**には、リポジトリを直接読まなくても使える [GitHub Pages の体験ページ](https://miookawa.github.io/copilot-experience-lab/) を用意しています。パートナーは、目的に合う体験やプログラムを選び、このページのリンクを参加者へ案内してください。GitHub Pages の体験カードは、`contents/` 配下のコンテンツから自動生成されます。

## あなたは何をしたいですか

| やりたいこと | 開く場所 |
| --- | --- |
| 環境の準備をしたい | [SETUP-01 サインイン確認と安全なAI利用の土台づくり](contents/00-setup/SETUP-01_サインイン確認と安全なAI利用の土台づくり.md) |
| とりあえずまずは1つ試してみたい | [自分のワークペルソナを1枚のスケッチにする](contents/01-copilot-chat/CHAT-IMG-01_自分のワークペルソナを1枚のスケッチにする.md) |
| 体験を探したい・選びたい | [体験の一覧](contents/README.md) |
| プログラムを実施したい | [プログラムの一覧](programs/README.md) |
| 自分でプログラムを組みたい | [プログラム雛形](programs/templates/README.md) |
| 体験やプログラムを追加したい | [CONTRIBUTING.md](CONTRIBUTING.md) |

## プログラム一覧

プログラムは、体験を並べた**進行の台本**です。最新の一覧と選び方は [programs/README.md](programs/README.md) を参照してください。

| プログラム | 対象 | 期間・所要 | パートナー向け（GitHub リポジトリ） | エンドユーザー向け（GitHub Pages） |
| --- | --- | --- | --- | --- |
| Copilot in 30 | Copilot トライアルを行うお客様と、伴走支援するパートナー | 30日 | [進行ガイド](programs/copilot-in-30/README.md) | [体験ページ](https://miookawa.github.io/copilot-experience-lab/programs/copilot-in-30/) |
| M365 Copilot + Agents SMB Guided Experience | SMB のお客様と、実施するパートナー | 約 90 分 | [進行ガイド](programs/smb-guided-experience/README.md) | [体験ページ](https://miookawa.github.io/copilot-experience-lab/programs/smb-guided-experience/) |


## コンテンツを探す

体験は `contents/` 配下に、製品・シーン別のカテゴリ（フォルダー）へ分かれて置かれています。

**[体験の一覧（contents/README.md）](contents/README.md)** に、ID・所要・利用する製品・入力に使うデータをまとめた索引があります。プログラムを組むときも、単発で試す体験を選ぶときも、まずここを開いてください。

一覧では、次の観点で体験を絞り込めます。

- **入力データ** — 参加者自身の業務データを使うか、サンプル ファイルを使うか、プロンプトに題材が含まれていてファイル準備なしで試せるか
- **所要** — 与えられた時間に収まるかどうか

## サンプルデータ

実業務のデータを使えない場合や、適切な題材が見つからない場合に備えて、架空企業を題材にしたサンプルデータを用意しています。

どのデータを使うかは、**各体験の「入力」欄**と、**そのデータを使うプログラムの README** に記載しています。配布用の一式は [GitHub Releases](../../releases) から取得できます。

## 実施前に確認すること

> このセクションは、ラボ全体で共通の注意事項です。各プログラムの README からは、ここへリンクしています。

- **参加者の実データを扱います。** 多くの体験で、参加者自身のメール・会議・チャット・ファイルを使います。共有・公開する成果物に機密情報が含まれていないか、必ず確認してください。
- **利用できる機能は、ライセンスとテナント設定によって異なります。** 特に Excel を使う体験と、Agent Builder を使う体験は、実施前の確認が必要です。
- **Copilot in Excel** は、ファイルを OneDrive / SharePoint に保存し、AutoSave を有効にする必要があります。
- **エージェントの作成・共有の可否**は、管理者設定・テナント構成・ライセンスによって異なります。実施前に管理者へ確認してください。
- **Copilot の回答をうのみにせず、根拠リンクを開いて確認する**運用を前提とします。
- **時間短縮は参加者が実測します。** Copilot に見積もらせないでください。
- **ハンズオンが難しい回は、進行役のデモに切り替えて構いません。**

## リポジトリ構成

```
copilot-experience-lab/
├─ index.md                     … GitHub Pages のトップ（体験カードは自動生成）
├─ README.md                    … このファイル（ラボ全体の入口）
├─ CONTRIBUTING.md              … 追加・改訂のルール
├─ CODESPACES_PREVIEW.md        … Codespaces で Pages をプレビューする手順
├─ _config.yml                  … GitHub Pages の設定
├─ _includes/                   … Pages のテンプレート部品
├─ .github/workflows/           … GitHub Actions（アクセス統計の自動収集など）
├─ contents/                    … 体験の実体
│  ├─ README.md                 … 体験の一覧（索引）
│  ├─ 00-setup/                 … Setup
│  ├─ 01-copilot-chat/          … Copilot Chat
│  ├─ 02-outlook-teams/         … Outlook / Teams
│  ├─ 03-excel/                 … Excel
│  ├─ 04-word/                  … Word
│  ├─ 05-powerpoint/            … PowerPoint
│  ├─ 06-researcher-analyst/    … Researcher / Analyst
│  ├─ 07-agent-builder/         … Agent Builder
│  ├─ 08-personas/              … Personas
│  └─ assets/                   … 体験別の画像・動画と、サンプルデータ
└─ programs/                    … 進行プログラム（順番とルールのみ）
   ├─ README.md                 … プログラムの一覧と選び方
   ├─ copilot-in-30/            … 30 日間プログラム
   ├─ smb-guided-experience/    … 90 分ワークショップ
   ├─ ms-base/                  … 将来のプログラム用（準備中）
   └─ templates/                … 新規プログラムの雛形
```

カテゴリやプログラムは今後追加されます。最新の内容は `contents/README.md` と `programs/README.md` を参照してください。

## 独自にカスタマイズする

このリポジトリを Clone または Fork して独自にカスタマイズする場合は、体験やプログラムの追加、既存コンテンツの改訂手順を **[CONTRIBUTING.md](CONTRIBUTING.md)** で確認してください。

GitHub Pages へ公開する前に任意のブランチを確認する方法は、**[Codespaces で GitHub Pages をプレビューする](CODESPACES_PREVIEW.md)**を参照してください。
