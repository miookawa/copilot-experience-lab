# Copilot Experience Lab

Microsoft Copilot を試すための、日本語の体験コンテンツ集です。
1 コンテンツ 5〜30 分、全 37 件。**実業務のデータ**でも、**架空企業「レイクショア」のサンプルデータ**でも試せます。

| フォルダー | 役割 |
|---|---|
| [`contents/`](./contents) | **体験の実体 [扉]**。1 体験 1 ファイルで、製品・シーン別のカテゴリに配置 |
| [`programs/`](./programs) | **進行プログラム**。体験の順番・必須/選択・運営ルールだけを持ち、体験は相対リンクで参照 |
| [`contents/assets/`](./contents/assets) | 体験ごとの画像・動画と、レイクショア サンプルデータ一式 |
| [`index.md`](./index.md) | GitHub Pages 用のトップページ。扉カードは `contents/` から自動生成 |

> **体験(ユーザ向けには[扉]と記述しています)の中身は `contents/` にのみ置きます。`programs/` にコンテンツを複製しないでください。**
> 追加・改訂のルールは [CONTRIBUTING.md](./CONTRIBUTING.md) を参照してください。

---

## 目的別の入口

| やりたいこと | 開く場所 |
|---|---|
| まず 1 件だけ試したい | [SETUP-01 サインイン確認と安全なAI利用の土台づくり](./contents/00-setup/SETUP-01_%E3%82%B5%E3%82%A4%E3%83%B3%E3%82%A4%E3%83%B3%E7%A2%BA%E8%AA%8D%E3%81%A8%E5%AE%89%E5%85%A8%E3%81%AAAI%E5%88%A9%E7%94%A8%E3%81%AE%E5%9C%9F%E5%8F%B0%E3%81%A5%E3%81%8F%E3%82%8A.md) → [下のコンテンツ一覧](#コンテンツ一覧) |
| 30 日間の伴走プログラムを回したい | [Copilot in 30](./programs/copilot-in-30/README.md) |
| 90 分のワークショップを実施したい | [M365 Copilot + Agents SMB Guided Experience](./programs/smb-guided-experience/README.md) |
| サンプルデータを配布したい | [レイクショア サンプルデータ（日本語版）](./contents/assets/lakeshore-sample-data-ja/README.md) |
| 体験やプログラムを追加したい | [CONTRIBUTING.md](./CONTRIBUTING.md) ／ [プログラム雛形](./programs/templates/README.md) |

---

## コンテンツ一覧

カテゴリ（`contents/` 配下のフォルダー）ごとの一覧です。**データ**欄は、その体験で何を入力に使うかを示します。

| 表記 | 意味 |
|---|---|
| 自分の業務データ | 参加者自身のメール・会議・チャット・ファイルを使う |
| サンプル ファイル | レイクショア（架空企業）のサンプル ファイルを使う |
| サンプル（プロンプト内） | 題材がプロンプトに含まれ、ファイル準備なしで試せる |

**カテゴリ**：[Setup](#00-setup)（1） ／ [Copilot Chat](#01-copilot-chat)（20） ／ [Outlook / Teams](#02-outlook-teams)（6） ／ [Excel](#03-excel)（1） ／ [Word](#04-word)（2） ／ [PowerPoint](#05-powerpoint)（準備中） ／ [Researcher / Analyst](#06-researcher-analyst)（2） ／ [Agent Builder](#07-agent-builder)（5） ／ [Personas](#08-personas)（準備中）

<a id="00-setup"></a>

### Setup ｜ `00-setup`（1 件）

はじめる前に。環境と進め方をそろえる

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `SETUP-01` | [サインイン確認と安全なAI利用の土台づくり](./contents/00-setup/SETUP-01_サインイン確認と安全なAI利用の土台づくり.md) | 正しいアカウントで Copilot に入り、AI をどの信頼基盤の上で使っているかを理解する | 約 10 分 | Copilot Chat / OneDrive / SharePoint | サンプル ファイル |

<a id="01-copilot-chat"></a>

### Copilot Chat ｜ `01-copilot-chat`（20 件）

まず驚く。自分のデータで対話する

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `CHAT-01` | [競合3社のメモを比較表と示唆に変える](./contents/01-copilot-chat/CHAT-01_競合3社のメモを比較表と示唆に変える.md) | 断片的な競合メモを、会議で使える構造化された比較表と示唆に変える | 約 10 分 | Copilot Chat | サンプル（プロンプト内） |
| `CHAT-02` | [キャンペーンブリーフと役員向けプレゼン骨子を作る](./contents/01-copilot-chat/CHAT-02_キャンペーンブリーフと役員向けプレゼン骨子を作る.md) | 複数の業務情報を、レビュー可能なキャンペーン ブリーフと経営層向けプレゼン骨子に変える | 約 15 分 | Copilot Chat | サンプル（プロンプト内） |
| `CHAT-03` | [顧客クレームを論点整理し返信案まで作る](./contents/01-copilot-chat/CHAT-03_顧客クレームを論点整理し返信案まで作る.md) | 感情的な長文クレームから論点を切り出し、選択肢を比較し、共感的な返信案までを一気に作る | 約 10 分 | Copilot Chat | サンプル（プロンプト内） |
| `CHAT-04` | [パートナー提案書を要約し確認すべき質問を洗い出す](./contents/01-copilot-chat/CHAT-04_パートナー提案書を要約し確認すべき質問を洗い出す.md) | 長い提案書から、意思決定に必要な要点、双方の対応事項、リスク、確認事項を整理する | 約 10 分 | Copilot Chat | サンプル（プロンプト内） |
| `CHAT-05` | [Copilotはもう、あなたの仕事を知っている](./contents/01-copilot-chat/CHAT-05_Copilotはもうあなたの仕事を知っている.md) | 一般知識ではなく、自分の仕事データにグラウンディングされた回答を最初に体験する | 約 10 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-06` | [自社ファイルを根拠に競合分析を自社視点へ引き上げる](./contents/01-copilot-chat/CHAT-06_自社ファイルを根拠に競合分析を自社視点へ引き上げる.md) | 一般的な競合サマリーから、自社にとっての意味を語る提言へ引き上げる | 約 10 分 | Microsoft 365 Copilot Chat（Work） | サンプル ファイル |
| `CHAT-07` | [忙しい朝を3分で整理、スケジュール実行する](./contents/01-copilot-chat/CHAT-07_忙しい朝を3分で整理する.md) | 予定・メール・依頼の確認を 1 回の依頼にまとめ、毎朝使える「仕事開始ボタン」を作る | 約 5 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-08` | [会議前の「何を話せばよいか」を作る](./contents/01-copilot-chat/CHAT-08_会議前の_何を話せばよいか_を作る.md) | 「とりあえず参加」する状態から、論点を持って参加する状態へ変える | 約 10 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-09` | [Week 1の驚きを言語化する](./contents/01-copilot-chat/CHAT-09_Week%201の驚きを言語化する.md) | 1 週間の体験を「今後も使うもの」「指示を変えるべきもの」に仕分けし、チームへ共有する | 約 10 分＋ 共有 5 分 | Microsoft 365 Copilot Chat（Work） ／ Teams（専用チャネル） | 自分の業務データ |
| `CHAT-10` | [未処理メールをまとめて整理する](./contents/01-copilot-chat/CHAT-10_未処理メールをまとめて整理する.md) | 溜まった未処理メールを、判断理由つきで 4 段階に仕分けする | 約 10 分 | Microsoft 365 Copilot Chat（Work） ／ Outlook の Copilot | 自分の業務データ |
| `CHAT-11` | [この画面は何するところ？を、撮って聞く](./contents/01-copilot-chat/CHAT-11_この画面は何かを撮って聞く.md) | 初めて開いた管理画面を、その場でスクリーンショットから解説してもらう | 約 10 分 | Microsoft 365 Copilot Chat（スクリーンショット入力） | 自分の業務データ |
| `CHAT-12` | [朝または夕方のプロンプトを定型化する](./contents/01-copilot-chat/CHAT-12_朝または夕方のプロンプトを定型化する.md) | 効果の高かったプロンプトを、毎日繰り返し使える形に作り替える | 約 10 分 | Microsoft 365 Copilot Chat（Work）（利用可能な環境ではスケジュール実行） | 自分の業務データ |
| `CHAT-13` | [1日の終わりをCopilotで締める](./contents/01-copilot-chat/CHAT-13_1日の終わりをCopilotで締める.md) | その日の結果を残し、翌日の最優先事項 3 つを決めた状態で終業する | 約 5 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-14` | [プロジェクトの状況を横断的に把握する](./contents/01-copilot-chat/CHAT-14_プロジェクトの状況を横断的に把握する.md) | メール・会議・チャット・ファイルに散らばった情報から、プロジェクトの現在地を 1 枚にまとめる | 約 10 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-15` | [Copilot自分の使い方からユースケースを作る](./contents/01-copilot-chat/CHAT-15_Copilot自分の使い方からユースケースを作る.md) | 自分の役割で繰り返し使える業務を洗い出し、任せる範囲と判断する範囲を分ける | 約 10 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-16` | [複数資料を比較する](./contents/01-copilot-chat/CHAT-16_複数資料を比較する.md) | 複数案・複数資料を同じ軸で比較し、判断に足りない情報を明らかにする | 約 10 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-17` | [自分専用の「鉄板プロンプト」を作る](./contents/01-copilot-chat/CHAT-17_自分専用の「鉄板プロンプト」を作る.md) | 日常的に使うプロンプトを 5 本に絞り、毎日繰り返し使える形に整えて、いつでも呼び出せる状態にする | 約 20 分 | Microsoft 365 Copilot Chat（Work）（Prompt Gallery への保存／利用可能な環境ではスケジュール実行） | 自分の業務データ |
| `CHAT-18` | [既存資料を要約する](./contents/01-copilot-chat/CHAT-18_既存資料を要約する.md) | 読む必要のある資料を、説明できる状態まで一気に引き上げる | 約 10 分 | Microsoft 365 Copilot Chat（Work） ／ Word の Copilot | 自分の業務データ |
| `CHAT-IMG-01` | [自分のワークペルソナを1枚のスケッチにする](./contents/01-copilot-chat/CHAT-IMG-01_自分のワークペルソナを1枚のスケッチにする.md) | Copilot が把握している自分の仕事、関係者、役割、価値観を、ホワイトボード風の1枚絵として可視化する | 約 10 分 | Microsoft 365 Copilot Chat | 自分の業務データ |
| `CHAT-IMG-02` | [自社のホームページから企業紹介インフォグラフィックを作る](./contents/01-copilot-chat/CHAT-IMG-02_自社のホームページから企業紹介インフォグラフィックを作る.md) | 自社ホームページの公開情報をもとに、会社の特徴や事業内容を1枚で伝える企業紹介インフォグラフィックを作成する | 約 10 分 | Microsoft 365 Copilot Chat | 自社の公開情報 |

<a id="02-outlook-teams"></a>

### Outlook / Teams ｜ `02-outlook-teams`（6 件）

毎日の面倒を減らす。メールと会議

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `CATCH-01` | [メールとチャットから未対応のフォローアップを洗い出す](./contents/02-outlook-teams/CATCH-01_メールとチャットから未対応のフォローアップを洗い出す.md) | 自分の実際のメールとチャットから、抱えているフォローアップを浮かび上がらせる | 約 15 分 | Outlook / Teams / Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `CHAT-07` | [長いメールスレッドから結論だけを得る](./contents/02-outlook-teams/CHAT-07_長いメールスレッドから結論だけを得る.md) | 読む時間だけでなく、返信に着手するまでの時間を短縮する | 約 10 分 | Outlook の Copilot ／ Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `MAL-01` | [メール返信を3パターン作る](./contents/02-outlook-teams/MAL-01_メール返信を3パターン作る.md) | 1 通の返信に複数の選択肢を持ち、判断は人が行う進め方を体験する | 約 5 分 | Outlook の Copilot ／ Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `MTG-01` | [会議を要約しフォローアップ連絡文を作る](./contents/02-outlook-teams/MTG-01_会議を要約しフォローアップ連絡文を作る.md) | 複数の会議に散らばった決定事項とアクションを、明確なフォローアップに変える | 約 10 分 | Copilot in Teams | 自分の業務データ |
| `MTG-02` | [会議後のアクションを自分用に再整理する](./contents/02-outlook-teams/MTG-02_会議後のアクションを自分用に再整理する.md) | 会議の記録ではなく、「自分が次に何をするか」を取り出す | 約 10 分 | Microsoft 365 Copilot Chat（Work） ／ Teams の会議 Copilot | 自分の業務データ |
| `MTG-03` | [会議前から会議後までを一連で使う](./contents/02-outlook-teams/MTG-03_会議前から会議後までを一連で使う.md) | 単発の依頼をつなげ、会議という業務プロセス全体を Copilot と回す | 会議前 10 分 ＋ 会議後 10 分 | Microsoft 365 Copilot Chat（Work） ／ Teams の会議 Copilot | 自分の業務データ |

<a id="03-excel"></a>

### Excel ｜ `03-excel`（1 件）

数字から示唆を取り出す

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `XLS-01` | [売上データから地域別の弱点と価格施策を導く](./contents/03-excel/XLS-01_売上データから地域別の弱点と価格施策を導く.md) | 手作業では追いきれない売上ブックから、エリア別のパターンと価格施策の示唆を引き出す | 約 15 分 | Copilot in Excel | サンプル ファイル |

<a id="04-word"></a>

### Word ｜ `04-word`（2 件）

文書をゼロから書かない

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `WRD-01` | [短いブリーフを10章のローンチ文書に展開する](./contents/04-word/WRD-01_短いブリーフを10章のローンチ文書に展開する.md) | 短いブリーフを、自社のブランド ガイダンスと売上データに基づく正式なローンチ文書に展開する | 約 10 分 | Copilot in Word | サンプル ファイル |
| `WRD-02` | [長い文書をレビューしてもらう](./contents/04-word/WRD-02_長い文書をレビューしてもらう.md) | 書き直しではなく、修正候補と理由を受け取って自分で直す | 約 10 分 | Microsoft 365 Copilot Chat（Work） ／ Word の Copilot | 自分の業務データ |

<a id="05-powerpoint"></a>

### PowerPoint ｜ `05-powerpoint`

伝わる資料に仕上げる（**準備中**：コンテンツはまだありません）

<a id="06-researcher-analyst"></a>

### Researcher / Analyst ｜ `06-researcher-analyst`（2 件）

調べる・分析するを任せる

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `AGT-01` | [Researcherに市場調査ブリーフを委任する](./contents/06-researcher-analyst/AGT-01_Researcherに市場調査ブリーフを委任する.md) | まとまった調査タスクを丸ごと任せ、経営層向けのブリーフを受け取る | 約 10 分 | Microsoft 365 Copilot の Researcher エージェント | サンプル（プロンプト内） |
| `AGT-02` | [Analystにリスクの高いSKU特定を委任する](./contents/06-researcher-analyst/AGT-02_Analystにリスクの高いSKU特定を委任する.md) | 売上データの分析を委任し、リスクのある SKU と打ち手の提言を受け取る | 約 10 分 | Microsoft 365 Copilot の Analyst エージェント | サンプル ファイル |

<a id="07-agent-builder"></a>

### Agent Builder ｜ `07-agent-builder`（5 件）

自分専用のエージェントを作る

| ID | 体験 | ねらい | 所要 | 利用 | データ |
|---|---|---|---|---|---|
| `AGB-01` | [繰り返し業務を洗い出して1件に絞る](./contents/07-agent-builder/AGB-01_繰り返し業務を洗い出して1件に絞る.md) | 自分の役割で繰り返している業務を洗い出し、任せる範囲と人が判断する範囲を分けたうえで、エージェント化する 1 件を決める | 約 15 分 | Microsoft 365 Copilot Chat（Work） | 自分の業務データ |
| `AGB-02` | [軽量Agent Builder体験](./contents/07-agent-builder/AGB-02_軽量Agent%20Builder体験.md) | 繰り返し業務を、指示を書いたエージェントとして固定する | 約 25 分 | Copilot の Agent Builder（インストラクション ＋ ナレッジ ソース） | 自分の業務データ |
| `AGB-03` | [ホワイトボード写真から議事録とスライドを作る](./contents/07-agent-builder/AGB-03_ホワイトボード写真から議事録とスライドを作る.md) | ホワイトボードを iPhone で撮るだけで、議事録の下書きとスライド構成までを自動で受け取る | 約 30 分 | Copilot の Agent Builder ／ Copilot モバイル アプリ（iPhone）／ PowerPoint の Copilot | 自分の業務データ |
| `AGB-04` | [顧客フォローアップ用エージェントを作る](./contents/07-agent-builder/AGB-04_顧客フォローアップ用エージェントを作る.md) | 毎週繰り返す業務プロセスを、再利用可能なエージェントとして定型化する | 約 20 分 | Agent Builder | サンプル ファイル |
| `AGB-05` | [提案書作成エージェントを作る](./contents/07-agent-builder/AGB-05_提案書作成エージェントを作る.md) | 提案書作成という繰り返し業務を、より強い初稿を出すエージェントにまとめる | 約 15 分 | Agent Builder | サンプル ファイル |

<a id="08-personas"></a>

### Personas ｜ `08-personas`

役割別の使いどころ（**準備中**：コンテンツはまだありません）

### ID の接頭辞

| 接頭辞 | 領域 | 配置先 |
|---|---|---|
| `SETUP-` | 事前準備・信頼基盤 | `contents/00-setup/` |
| `CHAT-` | Copilot Chat | `contents/01-copilot-chat/` |
| `CHAT-IMG-` | Copilot Chat（画像生成） | `contents/01-copilot-chat/` |
| `CATCH-` | キャッチアップ シナリオ | `contents/02-outlook-teams/` |
| `MAL-` | メール | `contents/02-outlook-teams/` |
| `MTG-` | 会議シナリオ | `contents/02-outlook-teams/` |
| `XLS-` | Excel | `contents/03-excel/` |
| `WRD-` | Word | `contents/04-word/` |
| `AGT-` | Researcher / Analyst エージェント | `contents/06-researcher-analyst/` |
| `AGB-` | Agent Builder | `contents/07-agent-builder/` |

一度発行した ID は変更しません（プログラムからの参照が壊れるため）。

---

## プログラム一覧

プログラムは、体験を並べた**進行の台本**です。体験そのものは持たず、`contents/` への相対リンク・順番・必須/選択・運営ルールだけを持ちます。

| プログラム | 対象 | 期間・所要 | 入口 |
|---|---|---|---|
| **Copilot in 30** | Copilot トライアルを行うお客様、伴走支援するパートナー向け | Day 0 〜 Day 21 | [進行ガイド](./programs/copilot-in-30/README.md) ／ [参加者向けページ](https://miookawa.github.io/copilot-experience-lab/programs/copilot-in-30/) |
| **M365 Copilot + Agents SMB Guided Experience** | SMB のお客様と、実施するパートナー | 約 90 分 | [進行ガイド](./programs/smb-guided-experience/README.md) ／ [参加者向けページ](https://miookawa.github.io/copilot-experience-lab/programs/smb-guided-experience/) |
| **プログラム雛形** | 新しいプログラムを追加する人 | — | [テンプレート](./programs/templates/README.md) |

### Copilot in 30 ｜ 30 日間 AI 活用プログラム

**ゴール**：参加者が繰り返し業務を 1 つ Copilot に置き換え、その成果を導入判断の材料として残せるよう支援する。
Week 1〜3 で選択肢を広げ、**Day 15 前後で「自分の定番」を 1 つ決め**、Week 4 で仕組みにして定着させる流れです。

| 期間 | テーマ | 使う体験 |
|---|---|---|
| Week 0 ｜ Day 0 | はじめる前に | [サインイン確認と安全なAI利用の土台づくり](./contents/00-setup/SETUP-01_サインイン確認と安全なAI利用の土台づくり.md)<br>[自分のワークペルソナを1枚のスケッチにする](./contents/01-copilot-chat/CHAT-IMG-01_自分のワークペルソナを1枚のスケッチにする.md) |
| Week 1 ｜ Day 1-5 | 受信トレイを制する | [メールとチャットから未対応のフォローアップを洗い出す](./contents/02-outlook-teams/CATCH-01_メールとチャットから未対応のフォローアップを洗い出す.md)<br>**オプション**：[顧客クレームを論点整理し返信案まで作る](./contents/01-copilot-chat/CHAT-03_顧客クレームを論点整理し返信案まで作る.md)／[パートナー提案書を要約し確認すべき質問を洗い出す](./contents/01-copilot-chat/CHAT-04_パートナー提案書を要約し確認すべき質問を洗い出す.md) |
| Week 2 ｜ Day 6-10 | 会議から成果を取り出す | [会議を要約しフォローアップ連絡文を作る](./contents/02-outlook-teams/MTG-01_会議を要約しフォローアップ連絡文を作る.md) |
| Week 3 ｜ Day 11-15 | つくる時間を短くする | [自社ファイルを根拠に競合分析を自社視点へ引き上げる](./contents/01-copilot-chat/CHAT-06_自社ファイルを根拠に競合分析を自社視点へ引き上げる.md)<br>**オプション**：[短いブリーフを10章のローンチ文書に展開する](./contents/04-word/WRD-01_短いブリーフを10章のローンチ文書に展開する.md)／[売上データから地域別の弱点と価格施策を導く](./contents/03-excel/XLS-01_売上データから地域別の弱点と価格施策を導く.md)／[キャンペーンブリーフと役員向けプレゼン骨子を作る](./contents/01-copilot-chat/CHAT-02_キャンペーンブリーフと役員向けプレゼン骨子を作る.md)／[競合3社のメモを比較表と示唆に変える](./contents/01-copilot-chat/CHAT-01_競合3社のメモを比較表と示唆に変える.md) |
| Day 15 前後 | **立ち止まる：自分の定番を 1 つ決める** | 体験なし。[進行ガイドの手順](./programs/copilot-in-30/README.md)で振り返りを支援 |
| Week 4 ｜ Day 16-20 | 決めた仕事を仕組みにする | [顧客フォローアップ用エージェントを作る](./contents/07-agent-builder/AGB-04_顧客フォローアップ用エージェントを作る.md)<br>[提案書作成エージェントを作る](./contents/07-agent-builder/AGB-05_提案書作成エージェントを作る.md)<br>**オプション**：[Researcherに市場調査ブリーフを委任する](./contents/06-researcher-analyst/AGT-01_Researcherに市場調査ブリーフを委任する.md)／[Analystにリスクの高いSKU特定を委任する](./contents/06-researcher-analyst/AGT-02_Analystにリスクの高いSKU特定を委任する.md) |
| Day 21 | 成果を振り返り、次の一歩を決める | 体験なし。回数・時間の変化・証跡を確認 |

参加者向けページ [`programs/copilot-in-30/index.md`](./programs/copilot-in-30/index.md) には、上記に加えて Copilot Chat・会議・文書作成の扉が Week ごとに並んでいます（GitHub Pages 用）。

### M365 Copilot + Agents SMB Guided Experience（日本語版）

**ゴール**：日常業務のプロンプトから、業務コンテキスト活用、エージェントへの委任、再利用可能なエージェント作成までを一気通貫で体験する。
架空の中堅オムニチャネル小売企業「レイクショア」のローンチ準備という 1 本の物語で全演習をつなぎます。ハンズオン形式と、進行役によるデモ形式のどちらでも実施できます。

| セクション | テーマ | 使う体験 | 必須 / 選択 |
|---|---|---|---|
| 0 | 信頼とストーリーの土台 | [サインイン確認と安全なAI利用の土台づくり](./contents/00-setup/SETUP-01_サインイン確認と安全なAI利用の土台づくり.md) | 全員 |
| 1 | まず好きになる — Copilot Chat | [競合3社のメモを比較表と示唆に変える](./contents/01-copilot-chat/CHAT-01_競合3社のメモを比較表と示唆に変える.md)／[キャンペーンブリーフと役員向けプレゼン骨子を作る](./contents/01-copilot-chat/CHAT-02_キャンペーンブリーフと役員向けプレゼン骨子を作る.md)／[顧客クレームを論点整理し返信案まで作る](./contents/01-copilot-chat/CHAT-03_顧客クレームを論点整理し返信案まで作る.md)／[パートナー提案書を要約し確認すべき質問を洗い出す](./contents/01-copilot-chat/CHAT-04_パートナー提案書を要約し確認すべき質問を洗い出す.md) | 2 つ完了 ＋ 選択 1 つ |
| 2 | 自分の仕事につながる — Microsoft 365 Copilot | [メールとチャットから未対応のフォローアップを洗い出す](./contents/02-outlook-teams/CATCH-01_メールとチャットから未対応のフォローアップを洗い出す.md)／[自社ファイルを根拠に競合分析を自社視点へ引き上げる](./contents/01-copilot-chat/CHAT-06_自社ファイルを根拠に競合分析を自社視点へ引き上げる.md)／[売上データから地域別の弱点と価格施策を導く](./contents/03-excel/XLS-01_売上データから地域別の弱点と価格施策を導く.md)／[短いブリーフを10章のローンチ文書に展開する](./contents/04-word/WRD-01_短いブリーフを10章のローンチ文書に展開する.md)／[会議を要約しフォローアップ連絡文を作る](./contents/02-outlook-teams/MTG-01_会議を要約しフォローアップ連絡文を作る.md) | 2 つ完了 |
| 3 | 任せてみる — Agents | [Researcherに市場調査ブリーフを委任する](./contents/06-researcher-analyst/AGT-01_Researcherに市場調査ブリーフを委任する.md)／[Analystにリスクの高いSKU特定を委任する](./contents/06-researcher-analyst/AGT-02_Analystにリスクの高いSKU特定を委任する.md) | 1 つ以上（デモ可） |
| 4 | 自分のものにする — Agent Builder | [顧客フォローアップ用エージェントを作る](./contents/07-agent-builder/AGB-04_顧客フォローアップ用エージェントを作る.md)／[提案書作成エージェントを作る](./contents/07-agent-builder/AGB-05_提案書作成エージェントを作る.md) | AGB-04 必須 |

---

## サンプルデータ（レイクショア）

実業務のデータを使えない場合や、適切な題材が見つからない場合に使います。
[GitHub Releases](https://github.com/miookawa/copilot-experience-lab/releases/tag/lakeshore-sample-data-ja-v1.0.0) に個別ファイル、[`lakeshore-sample-data-ja.zip`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/lakeshore-sample-data-ja.zip) に一式があります。

| ファイル | 内容 | 主に使う体験 |
|---|---|---|
| [`lakeshore-prior-season-strategy.docx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/lakeshore-prior-season-strategy.docx) | 前シーズン戦略 | CHAT-06 |
| [`lakeshore-brand-playbook.docx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/lakeshore-brand-playbook.docx) | ブランド ガイダンス | CHAT-06 / WRD-01 |
| [`lakeshore-q4-sales.xlsx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/lakeshore-q4-sales.xlsx) | Q4 売上データ | XLS-01 / AGT-02 |
| [`lakeshore-launch-brief-template.docx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/lakeshore-launch-brief-template.docx) | ローンチ ブリーフ雛形 | WRD-01 |
| [`northwind-outfitters-proposal.docx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/northwind-outfitters-proposal.docx) | パートナー提案書 | CHAT-04 / AGB-05 |
| [`agent-knowledge-pack.docx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/agent-knowledge-pack.docx) | エージェント用ナレッジ | AGB-02 / AGB-04 / AGB-05 |
| [`customer-complaint-cases.xlsx`](https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/customer-complaint-cases.xlsx) | 顧客クレーム事例（任意・発展演習用） | CHAT-03 / AGB-04 |

> 配置先は OneDrive または SharePoint の `レイクショア Immersive Experience` フォルダーを推奨します。Copilot が引用できるよう、実施前に各ファイルを一度開いて確認してください。

---

## リポジトリ構成

```text
copilot-experience-lab/
├─ index.md                     … GitHub Pages のトップ（扉カードは自動生成）
├─ README.md                    … このファイル（コンテンツとプログラムの一覧）
├─ CONTRIBUTING.md              … 追加・改訂のルール
├─ contents/                    … 体験の実体
│  ├─ 00-setup/                 … Setup（1 件）
│  ├─ 01-copilot-chat/          … Copilot Chat（20 件）
│  ├─ 02-outlook-teams/         … Outlook / Teams（6 件）
│  ├─ 03-excel/                 … Excel（1 件）
│  ├─ 04-word/                  … Word（2 件）
│  ├─ 05-powerpoint/            … PowerPoint（準備中）
│  ├─ 06-researcher-analyst/    … Researcher / Analyst（2 件）
│  ├─ 07-agent-builder/         … Agent Builder（5 件）
│  ├─ 08-personas/              … Personas（準備中）
│  └─ assets/                   … 体験別の画像・動画、レイクショア サンプルデータ
└─ programs/                    … 進行プログラム（順番とルールのみ）
   ├─ copilot-in-30/            … 30 日間プログラム（README = 進行ガイド／index = 参加者向け）
   ├─ smb-guided-experience/    … 90 分ワークショップ
   └─ templates/                … 新規プログラムの雛形
```

---

## 体験ページの共通フォーマット

| セクション | 内容 |
|---|---|
| 冒頭の表 | 目的 / 所要 / 利用 / 入力 / 成果 |
| シナリオ | なぜこの体験を行うのか。進行役の説明例つき |
| TRY — 手順 | 番号つきの操作手順と、そのまま貼り付けられるプロンプト（`text` ブロック） |
| WATCH | 動画 / GIF の配置場所（素材がない場合はコメントアウト） |
| REFLECT — 振り返り | その場で自分に答える 3 つの問い |
| NEXT ／ CONTINUE YOUR JOURNEY | 次に開く体験へのリンク |

---

## 実施にあたっての注意

- 多くの体験で**参加者自身の実データ**を使います。共有・公開する成果物に機密情報が含まれていないか、必ず確認してください。
- 利用できる機能は、**ライセンスとテナント設定**によって異なります。特に Excel（XLS-01）と Agent Builder（AGB-02 〜 AGB-05）は事前確認が必要です。
- Copilot in Excel は、ファイルを OneDrive / SharePoint に保存し、AutoSave を有効にする必要があります。
- エージェントの作成・共有の可否は、管理者設定・テナント構成・ライセンスによって異なります。実施前に管理者へ確認してください。
- Copilot の回答をうのみにせず、**根拠リンクを開いて確認する**運用を前提とします。
- 時間短縮は**参加者が実測**します。Copilot に見積もらせないでください。
- ハンズオンが難しい回は、進行役のデモに切り替えて構いません。

---

## 参考リンク

- Copilot in 30 キット一式（週次メール、Teams チャネル ガイド、管理者設定ガイド）：https://aka.ms/Copilotin30Kit
- Copilot Success Planner（役割別の 30 日プラン）：https://adoption.microsoft.com/copilot/success-planner
- M365 Copilot + Agents Guided Experience：https://aka.ms/CopilotBusinessGuidedExperience
