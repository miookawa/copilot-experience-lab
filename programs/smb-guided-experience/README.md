# M365 Copilot + Agents SMB Guided Experience（日本語版）

> このファイルは**ポインタ + 順番 + ルール**だけを持ちます。体験の中身は `contents/` にあります。

- **対象**：SMB のお客様、および本ワークショップを実施するパートナー
- **所要**：約 90 分（元教材の推奨時間。人数・アクセス状況で調整可）
- **ゴール**：日常業務のプロンプトから、業務コンテキスト活用、エージェントへの委任、再利用可能なエージェント作成までを一気通貫で体験する
- **位置づけ**：技術導入セッションでも機能ツアーでもなく、**ビジネス起点のワークショップ**

---

## ストーリーライン

架空の中堅オムニチャネル小売企業 **レイクショア**（約 120 店舗＋EC）が、
春のスプリングアウトドア ラインのローンチを **6 週間後**に控えている、という一本の物語で全演習をつなぎます。

| 登場人物 | 役割 | 担当する体験 |
|---|---|---|
| 曽根拓海 | 商品企画部長 | CHAT-01 / CHAT-06 / XLS-01 |
| 大沢澪 | マーケティング部長 | CHAT-02 / WRD-01 |
| 遠藤淳也 | カスタマーサポート責任者 | CHAT-03 / AGB-04 |
| 松吉優香 | パートナー連携責任者 | CHAT-04 / AGB-04 / AGB-05 |
| 山本夏帆 | 店舗運営部長 | MTG-01 |
| リーダーシップ チーム | 経営陣 | AGT-01 / AGT-02 |

AI が支援する 4 つのステージ：

| ステージ | チームのニーズ | 体験するもの | ビジネス成果 |
|---|---|---|---|
| 1. 早く着手する | 調査・執筆・要約・発想 | Copilot Chat | 初稿が速くなり、出発点が良くなる |
| 2. 業務コンテキストで働く | 社内ファイル・データ・メール・会議 | Microsoft 365 Copilot | より的確で根拠のある提案 |
| 3. 大きな仕事を委任する | 調査・分析 | Researcher / Analyst | 経営層向けのアウトプット |
| 4. 繰り返しを再利用する | 定型業務 | Agent Builder | 再利用可能なアシスタント |

---

## 進行の流れ

### セクション 0 | 信頼とストーリーの土台
1. [サインイン確認と安全なAI利用の土台づくり](../../contents/00-setup/SETUP-01_サインイン確認と安全なAI利用の土台づくり.md)

**必須**：1 つ完了（全員のアカウント確認）

### セクション 1 | まず好きになる — Copilot Chat
1. [競合3社のメモを比較表と示唆に変える](../../contents/01-copilot-chat/CHAT-01_競合3社のメモを比較表と示唆に変える.md)
2. [キャンペーンブリーフと役員向けプレゼン骨子を作る](../../contents/01-copilot-chat/CHAT-02_キャンペーンブリーフと役員向けプレゼン骨子を作る.md)
3. [顧客クレームを論点整理し返信案まで作る](../../contents/01-copilot-chat/CHAT-03_顧客クレームを論点整理し返信案まで作る.md)
4. [パートナー提案書を要約し確認すべき質問を洗い出す](../../contents/01-copilot-chat/CHAT-04_パートナー提案書を要約し確認すべき質問を洗い出す.md)

**必須**：2 つ完了 ／ **選択**：興味のある体験を 1 つ追加
**到達目標**：Copilot による最初の成功体験

### セクション 2 | 自分の仕事につながる — Microsoft 365 Copilot
1. [メールとチャットから未対応のフォローアップを洗い出す](../../contents/02-outlook-teams/CATCH-01_メールとチャットから未対応のフォローアップを洗い出す.md)
2. [自社ファイルを根拠に競合分析を自社視点へ引き上げる](../../contents/01-copilot-chat/CHAT-06_自社ファイルを根拠に競合分析を自社視点へ引き上げる.md)
3. [売上データから地域別の弱点と価格施策を導く](../../contents/03-excel/XLS-01_売上データから地域別の弱点と価格施策を導く.md)
4. [短いブリーフを10章のローンチ文書に展開する](../../contents/04-word/WRD-01_短いブリーフを10章のローンチ文書に展開する.md)
5. [会議を要約しフォローアップ連絡文を作る](../../contents/02-outlook-teams/MTG-01_会議を要約しフォローアップ連絡文を作る.md)

**必須**：2 つ完了 ／ **代替進行**：ライセンスやアクセスの状況に応じて、進行役によるデモに切り替える

### セクション 3 | 任せてみる — Agents
1. [Researcherに市場調査ブリーフを委任する](../../contents/06-researcher-analyst/AGT-01_Researcherに市場調査ブリーフを委任する.md)
2. [Analystにリスクの高いSKU特定を委任する](../../contents/06-researcher-analyst/AGT-02_Analystにリスクの高いSKU特定を委任する.md)

**必須**：1 つ以上を体験またはデモ視聴

### セクション 4 | 自分のものにする — Agent Builder
1. [顧客フォローアップ用エージェントを作る](../../contents/07-agent-builder/AGB-04_顧客フォローアップ用エージェントを作る.md)
2. [提案書作成エージェントを作る](../../contents/07-agent-builder/AGB-05_提案書作成エージェントを作る.md)

**必須**：AGB-04 ／ **選択**：AGB-05（時間があれば）

### Close | 振り返りと次の一歩
- 一番使えそうだった体験を 1 つ選び、自分の業務に置き換えて言語化する
- 自社で最初に作るエージェントの候補を 1 つ決める

---

## 実施形式

元教材は 2 つの実施形態を想定しています。事前に**どちらで行うかを決めてから**当日を迎えてください。

| モデル | 適するお客様 | 進め方 |
|---|---|---|
| ハンズオン形式 | Microsoft 365 Copilot ライセンスがあり、Outlook / Teams / Excel / Word の Copilot、Researcher、Analyst、Agent Builder にアクセスできる少人数 | 参加者が自分で全演習を実施 |
| 進行役によるデモ形式 | Microsoft 365 Copilot ライセンスがない、試用開始前、本番/サンプルデータを当日使えない、時間が限られている | 進行役が実演し、参加者は自社での適用を議論 |

---

## 事前準備チェックリスト

- [ ] 実施形式（ハンズオン／デモ）を決定した
- [ ] ライセンスとアクセス（Copilot Chat / M365 Copilot / Researcher / Analyst / Agent Builder）を確認した
- [ ] レイクショア サンプルデータ一式を入手した
- [ ] OneDrive または SharePoint に `レイクショア Immersive Experience` フォルダを作成し、ファイルをアップロードした
- [ ] 各ファイルを一度開いて、正しく開くことを確認した
- [ ] 利用できない場合に備えた代替資料（事前に取得した出力例）を用意した
- [ ] 参加者に「Outlook / Teams 演習では機密でない自分のデータを使う」ことを事前案内した

### レイクショア サンプルファイル

- [`lakeshore-prior-season-strategy.docx`](../../contents/assets/lakeshore-sample-data-ja/lakeshore-prior-season-strategy.docx)（前シーズン戦略）
- [`lakeshore-brand-playbook.docx`](../../contents/assets/lakeshore-sample-data-ja/lakeshore-brand-playbook.docx)（ブランド ガイダンス）
- [`lakeshore-q4-sales.xlsx`](../../contents/assets/lakeshore-sample-data-ja/lakeshore-q4-sales.xlsx)（Q4 売上データ）
- [`lakeshore-launch-brief-template.docx`](../../contents/assets/lakeshore-sample-data-ja/lakeshore-launch-brief-template.docx)（ローンチ ブリーフ雛形）
- [`northwind-outfitters-proposal.docx`](../../contents/assets/lakeshore-sample-data-ja/northwind-outfitters-proposal.docx)（パートナー提案書）
- [`agent-knowledge-pack.docx`](../../contents/assets/lakeshore-sample-data-ja/agent-knowledge-pack.docx)（エージェント用ナレッジ）
- [`customer-complaint-cases.xlsx`](../../contents/assets/lakeshore-sample-data-ja/customer-complaint-cases.xlsx)（任意・発展演習用）

---

## ファシリテーター向けの心得

- **ビジネス ファースト**で進める。技術ラボとして位置づけない。
- 当日はライセンスの説明に時間を使いすぎない。
- レイクショアのストーリーを常につなげる。
- **出力が人によって異なるのは当たり前**であることを繰り返し伝える。
- 必要な機能を利用できない場合は迷わずデモ形式に切り替える。
- 当日のトラブル対応に時間をかけすぎない。
- Agent Builder は「エージェントのデモ」から「繰り返し業務の自動化」への実践的な橋渡しとして扱う。
- **各アクティビティの最後に、必ずビジネス価値を着地させる。**

---

## トラブルシューティング

| 症状 | 対応 |
|---|---|
| サインインできない | 正しいアカウントか確認 → ページを再読み込み → プライベート/シークレット ウィンドウで試す → ファシリテーターに相談 |
| 個人アカウントでサインインしている | サインアウトし、タブを閉じ、リンクを開き直して職場アカウントでサインインする |
| Copilot Chat が表示されない | デモを視聴する。シナリオとプロンプトの確認は可能 |
| レイクショアのファイルにアクセスできない | 正しいアカウントとリンクか確認し、ファイルの場所をファシリテーターに確認する |
| Copilot がファイルを引用しない | ファイルが OneDrive / SharePoint にアップロードされ、開けることを確認する。それでも引用されない場合はデモに切り替える |
| Outlook に「Copilot による要約」が出ない | Microsoft 365 Copilot アクセスのある職場アカウントか確認し、別のスレッドで試す |
| Teams に Copilot／スレッドの要約が出ない | Copilot が使えるチャット・グループ チャット・チャネル スレッド・会議かを確認する |
| 要約に使える安全なメール・チャット・会議がない | デモを視聴する。機密・人事・法務・財務・個人・機微な顧客情報は使わない |
| 会議のリキャップがない | トランスクリプト・リキャップ・録画・会議チャット・Copilot が利用できる会議を選ぶ |
| Excel の Copilot が分析できない | ブックが OneDrive / SharePoint に保存され、データがテーブル形式になっていることを確認する |
| PowerPoint に Copilot が出ない | PowerPoint 向けの Microsoft 365 Copilot アクセスがない、または組織で有効化されていない可能性がある |
