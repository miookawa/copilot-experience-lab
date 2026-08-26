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
│     └─ CHAT-01/ ...
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
| [SETUP-01](content/00-setup/サインイン確認と安全なAI利用の土台づくり_SETUP-01.md) | サインイン確認と安全なAI利用の土台づくり | Copilot Chat | ― | Before You Begin / Secure AI in Practice |
| [CHAT-01](content/01-copilot-chat/競合3社のメモを比較表と示唆に変える_CHAT-01.md) | 競合3社のメモを比較表と示唆に変える | Copilot Chat | プロンプト内完結 | 1A |
| [CHAT-02](content/01-copilot-chat/キャンペーンブリーフと役員向けプレゼン骨子を作る_CHAT-02.md) | キャンペーンブリーフと役員向けプレゼン骨子を作る | Copilot Chat | プロンプト内完結 | 1B |
| [CHAT-03](content/01-copilot-chat/顧客クレームを論点整理し返信案まで作る_CHAT-03.md) | 顧客クレームを論点整理し返信案まで作る | Copilot Chat | プロンプト内完結 | 1C |
| [CHAT-04](content/01-copilot-chat/パートナー提案書を要約し確認すべき質問を洗い出す_CHAT-04.md) | パートナー提案書を要約し確認すべき質問を洗い出す | Copilot Chat | プロンプト内完結 | 1D |
| [CATCH-01](content/03-outlook-teams/メールとチャットから未対応のフォローアップを洗い出す_CATCH-01.md) | メールとチャットから未対応のフォローアップを洗い出す | Microsoft 365 Copilot | 自分の業務データ | 2A |
| [CHAT-05](content/02-microsoft365-copilot/自社ファイルを根拠に競合分析を自社視点へ引き上げる_CHAT-05.md) | 自社ファイルを根拠に競合分析を自社視点へ引き上げる | Microsoft 365 Copilot | Lakeshore サンプル | 2B |
| [XLS-01](content/04-excel/売上データから地域別の弱点と価格施策を導く_XLS-01.md) | 売上データから地域別の弱点と価格施策を導く | Copilot in Excel | Lakeshore サンプル | 2C |
| [WRD-01](content/05-word/短いブリーフを10章のローンチ文書に展開する_WRD-01.md) | 短いブリーフを10章のローンチ文書に展開する | Copilot in Word | Lakeshore サンプル | 2D |
| [MTG-01](content/03-outlook-teams/会議を要約しフォローアップ連絡文を作る_MTG-01.md) | 会議を要約しフォローアップ連絡文を作る | Copilot in Teams | 自分の業務データ | 2E |
| [AGT-01](content/06-researcher-analyst/Researcherに市場調査ブリーフを委任する_AGT-01.md) | Researcherに市場調査ブリーフを委任する | Researcher | Web | 3A |
| [AGT-02](content/06-researcher-analyst/Analystにリスクの高いSKU特定を委任する_AGT-02.md) | Analystにリスクの高いSKU特定を委任する | Analyst | Lakeshore サンプル | 3B |
| [AGT-03](content/07-agent-builder/顧客フォローアップ用エージェントを作る_AGT-03.md) | 顧客フォローアップ用エージェントを作る | Agent Builder | 任意（許可された範囲） | 4A |
| [AGT-04](content/07-agent-builder/提案書作成エージェントを作る_AGT-04.md) | 提案書作成エージェントを作る | Agent Builder | 任意（許可された範囲） | 4B |

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
