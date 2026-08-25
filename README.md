# Copilot Experience Lab

GitHub 上に「再利用できる体験コンテンツ基盤」をつくるためのリポジトリです。

**コンテンツは一度つくる。プログラムごとに、順番・選択・演出を変えて使う。**

このリポジトリでは「素材（content）」と「プログラム（programs）」を分離しています。
体験の実体は `content/` にのみ置き、`programs/` は相対リンク・順番・必須/選択・演出だけを持ちます。

> **重要ルール：`programs/` 配下に content をコピーしない。**

---

## フォルダ構成

```text
copilot-experience-lab/
├─ README.md
├─ CONTRIBUTING.md
├─ content/                          # 体験の実体。1 コンテンツ 1 か所
│  ├─ 00-setup/                      # 事前準備・セキュリティ
│  ├─ 01-copilot-chat/               # Copilot Chat（プロンプト内完結）
│  ├─ 02-microsoft365-copilot/       # Microsoft 365 Copilot（Work / 自社ファイル）
│  ├─ 03-outlook-teams/              # Copilot in Outlook / Teams
│  ├─ 04-excel/                      # Copilot in Excel
│  ├─ 05-word/                       # Copilot in Word
│  ├─ 06-researcher-analyst/         # Researcher / Analyst エージェント
│  ├─ 07-agent-builder/              # Agent Builder
│  ├─ 08-powerpoint/                 # Copilot in PowerPoint（今後追加）
│  ├─ 09-personas/                   # 職種別（今後追加）
│  └─ assets/                        # 動画 / GIF / サンプル（体験 ID のフォルダーで管理）
│     └─ EXP-CHAT-001/ ...
├─ programs/                         # 参照先・順番・必須/選択・演出
│  ├─ smb-guided-experience/README.md
│  ├─ copilot-in-30/                 # 今後追加
│  ├─ ms-base/                       # 今後追加
│  └─ templates/
```

フォルダーは**扱う製品ごと**に分かれています。番号は体験の推奨順序（Chat → 業務コンテキスト → エージェント）を表します。
ファイル名は `体験ID_ハンズオンの内容.md` の形式で、**ファイル名を見るだけで何を体験するか分かる**ようにしています。

---

## 体験コンテンツ一覧

このリポジトリの初期セットは、Microsoft の公式教材
「M365 Copilot + Agents SMB Guided Experience（Participant Guide v1.1 / Facilitator Delivery Guide / Partner Preparation Guide）」を
日本語の体験コンテンツとして部品化したものです。

| 体験 ID | タイトル | 利用サービス | データ | 元教材 |
|---|---|---|---|---|
| [EXP-SETUP-001](content/00-setup/EXP-SETUP-001_サインイン確認と安全なAI利用の土台づくり.md) | サインイン確認と安全なAI利用の土台づくり | Copilot Chat | ― | Before You Begin / Secure AI in Practice |
| [EXP-CHAT-001](content/01-copilot-chat/EXP-CHAT-001_競合3社のメモを比較表と示唆に変える.md) | 競合3社のメモを比較表と示唆に変える | Copilot Chat | プロンプト内完結 | 1A |
| [EXP-CHAT-002](content/01-copilot-chat/EXP-CHAT-002_キャンペーンブリーフと役員向けプレゼン骨子を作る.md) | キャンペーンブリーフと役員向けプレゼン骨子を作る | Copilot Chat | プロンプト内完結 | 1B |
| [EXP-CHAT-003](content/01-copilot-chat/EXP-CHAT-003_顧客クレームを論点整理し返信案まで作る.md) | 顧客クレームを論点整理し返信案まで作る | Copilot Chat | プロンプト内完結 | 1C |
| [EXP-CHAT-004](content/01-copilot-chat/EXP-CHAT-004_パートナー提案書を要約し確認すべき質問を洗い出す.md) | パートナー提案書を要約し確認すべき質問を洗い出す | Copilot Chat | プロンプト内完結 | 1D |
| [EXP-CATCH-001](content/03-outlook-teams/EXP-CATCH-001_メールとチャットから未対応のフォローアップを洗い出す.md) | メールとチャットから未対応のフォローアップを洗い出す | Microsoft 365 Copilot | 自分の業務データ | 2A |
| [EXP-CHAT-005](content/02-microsoft365-copilot/EXP-CHAT-005_自社ファイルを根拠に競合分析を自社視点へ引き上げる.md) | 自社ファイルを根拠に競合分析を自社視点へ引き上げる | Microsoft 365 Copilot | Lakeshore サンプル | 2B |
| [EXP-XLS-001](content/04-excel/EXP-XLS-001_売上データから地域別の弱点と価格施策を導く.md) | 売上データから地域別の弱点と価格施策を導く | Copilot in Excel | Lakeshore サンプル | 2C |
| [EXP-WRD-001](content/05-word/EXP-WRD-001_短いブリーフを10章のローンチ文書に展開する.md) | 短いブリーフを10章のローンチ文書に展開する | Copilot in Word | Lakeshore サンプル | 2D |
| [EXP-MTG-001](content/03-outlook-teams/EXP-MTG-001_会議を要約しフォローアップ連絡文を作る.md) | 会議を要約しフォローアップ連絡文を作る | Copilot in Teams | 自分の業務データ | 2E |
| [EXP-AGT-001](content/06-researcher-analyst/EXP-AGT-001_Researcherに市場調査ブリーフを委任する.md) | Researcherに市場調査ブリーフを委任する | Researcher | Web | 3A |
| [EXP-AGT-002](content/06-researcher-analyst/EXP-AGT-002_Analystにリスクの高いSKU特定を委任する.md) | Analystにリスクの高いSKU特定を委任する | Analyst | Lakeshore サンプル | 3B |
| [EXP-AGT-003](content/07-agent-builder/EXP-AGT-003_顧客フォローアップ用エージェントを作る.md) | 顧客フォローアップ用エージェントを作る | Agent Builder | 任意（許可された範囲） | 4A |
| [EXP-AGT-004](content/07-agent-builder/EXP-AGT-004_提案書作成エージェントを作る.md) | 提案書作成エージェントを作る | Agent Builder | 任意（許可された範囲） | 4B |

---

## プログラム

| プログラム | 対象 | 時間 | ねらい |
|---|---|---|---|
| [SMB Guided Experience](programs/smb-guided-experience/README.md) | SMB のお客様・パートナー | 約 90 分 | Chat から Agent 作成までを一気通貫で体験 |
| Copilot in 30 | 社内定着 | 30 日 | 定着・価値証明（今後追加） |
| MS Base | 来場者・短時間 | 短時間 | 驚きと理解（今後追加） |

---

## 体験コンテンツの共通フォーマット

すべての体験は、どのプログラムからも同じ形で参照できるよう、次の構成に揃えています。

- **メタ情報**：目的 / 所要 / 利用 / 入力 / 成果 / 証跡
- **シナリオ**：誰が、どんな業務課題を抱えているか
- **TRY**：実行手順とプロンプト
- **WATCH**：動画 / GIF（`content/assets/<体験ID>/`）
- **REFLECT**：価値の振り返り
- **NEXT**：次の体験へのリンク

---

## 出典と注意事項

- 本コンテンツは、Microsoft 提供の「M365 Copilot + Agents SMB Guided Experience」3 ガイドを基に日本語化・部品化したものです。
- 登場する Lakeshore Retail、Adventure Works Cycles、Alpine Ski House、Boulder Innovations、Northwind Outfitters、および人物名はすべて架空のものです。
- Copilot Chat、Microsoft 365 Copilot、Researcher、Analyst、Agent Builder の画面や機能は継続的に更新されます。画面キャプチャや表示名は実際と異なる場合があります。
- Outlook / Teams / 会議の演習では**自分自身の業務データ**を使います。機密情報、人事・法務・財務情報、個人情報、機微な顧客情報は使用しないでください。
