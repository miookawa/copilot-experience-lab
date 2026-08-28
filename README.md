# Copilot Experience Lab

GitHub 上に「再利用できる体験コンテンツ基盤」をつくるためのリポジトリです。
このリポジトリの体験コンテンツは、Microsoft の公式教材を日本語化したコンテンツと、Copilot Experience Lab オリジナルのコンテンツで構成されています。

<!--
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
ファイル名は `ハンズオンの内容_体験ID.md` の形式で、**ファイル名を見るだけで何を体験するか分かる**ようにしています。
-->
---

## 体験コンテンツ一覧

<!--
このリポジトリの体験コンテンツは、Microsoft の公式教材
「M365 Copilot + Agents SMB Guided Experience（Participant Guide v1.1 / Facilitator Delivery Guide / Partner Preparation Guide）」を
日本語で部品化したコンテンツと、Copilot Experience Lab オリジナルのコンテンツで構成されています。
-->


| 体験 ID | タイトル | 利用サービス | 入力 |
|---|---|---|---|
| [SETUP-01](content/00-setup/サインイン確認と安全なAI利用の土台づくり_SETUP-01.md) | サインイン確認と安全なAI利用の土台づくり | Copilot Chat / OneDrive / SharePoint | 職場アカウント、Lakeshore サンプルデータ一式 |
| [CHAT-01](content/01-copilot-chat/競合3社のメモを比較表と示唆に変える_CHAT-01.md) | 競合3社のメモを比較表と示唆に変える | Copilot Chat | 競合 3 社のメモ（プロンプトに含む） |
| [CHAT-02](content/01-copilot-chat/キャンペーンブリーフと役員向けプレゼン骨子を作る_CHAT-02.md) | キャンペーンブリーフと役員向けプレゼン骨子を作る | Copilot Chat | ローンチの前提情報（プロンプトに含む） |
| [CHAT-03](content/01-copilot-chat/顧客クレームを論点整理し返信案まで作る_CHAT-03.md) | 顧客クレームを論点整理し返信案まで作る | Copilot Chat | 顧客からのクレーム メール（プロンプトに含む） |
| [CHAT-04](content/01-copilot-chat/パートナー提案書を要約し確認すべき質問を洗い出す_CHAT-04.md) | パートナー提案書を要約し確認すべき質問を洗い出す | Copilot Chat | パートナー提案書の抜粋（プロンプトに含む） |
| [CHAT-IMG-01](content/01-copilot-chat/自分のワークペルソナを1枚のスケッチにする_CHAT-IMG-01.md) | 自分のワークペルソナを1枚のスケッチにする | Microsoft 365 Copilot Chat | Work IQ の業務コンテキスト ＋ LinkedIn 公開プロフィール ＋ 顔写真（任意） |
| [CHAT-05](content/02-microsoft365-copilot/自社ファイルを根拠に競合分析を自社視点へ引き上げる_CHAT-05.md) | 自社ファイルを根拠に競合分析を自社視点へ引き上げる | Microsoft 365 Copilot Chat（Work） | `lakeshore-prior-season-strategy.docx`、`lakeshore-brand-playbook.docx` |
| [CATCH-01](content/03-outlook-teams/メールとチャットから未対応のフォローアップを洗い出す_CATCH-01.md) | メールとチャットから未対応のフォローアップを洗い出す | Outlook / Teams / Microsoft 365 Copilot Chat（Work） | 自分の安全なメール スレッド、Teams チャットまたはチャネル スレッド |
| [MTG-01](content/03-outlook-teams/会議を要約しフォローアップ連絡文を作る_MTG-01.md) | 会議を要約しフォローアップ連絡文を作る | Copilot in Teams | 自分の安全な会議（リキャップ／トランスクリプト／録画／会議チャット） |
| [XLS-01](content/04-excel/売上データから地域別の弱点と価格施策を導く_XLS-01.md) | 売上データから地域別の弱点と価格施策を導く | Copilot in Excel | `lakeshore-q4-sales.xlsx` |
| [WRD-01](content/05-word/短いブリーフを10章のローンチ文書に展開する_WRD-01.md) | 短いブリーフを10章のローンチ文書に展開する | Copilot in Word | `lakeshore-launch-brief-template.docx`（＋ブランド プレイブック、Q4 売上データ） |
| [AGT-01](content/06-researcher-analyst/Researcherに市場調査ブリーフを委任する_AGT-01.md) | Researcherに市場調査ブリーフを委任する | Microsoft 365 Copilot の Researcher エージェント | 調査テーマ（アウトドア テクニカル アパレル市場） |
| [AGT-02](content/06-researcher-analyst/Analystにリスクの高いSKU特定を委任する_AGT-02.md) | Analystにリスクの高いSKU特定を委任する | Microsoft 365 Copilot の Analyst エージェント | `lakeshore-q4-sales.xlsx` |
| [AGT-03](content/07-agent-builder/顧客フォローアップ用エージェントを作る_AGT-03.md) | 顧客フォローアップ用エージェントを作る | Agent Builder | エージェント名・説明・指示・スターター プロンプト（＋許可されたナレッジ ソース） |
| [AGT-04](content/07-agent-builder/提案書作成エージェントを作る_AGT-04.md) | 提案書作成エージェントを作る | Agent Builder | エージェント名・説明・指示・スターター プロンプト（＋許可されたナレッジ ソース） |

---

## プログラム

| プログラム | 内容 | 時間 |
|---|---|---|
| [SMB Guided Experience](programs/smb-guided-experience/README.md) | 架空の小売企業を題材に、Chat から Agent Builder までを一気通貫で体験 | 約 90 分 |
| [Copilot in 30](programs/copilot-in-30/README.md) | 30 日間の伴走を通じて、Copilot を使う定番業務の定着と成果確認を支援 | 30 日 |
| MS Base | 準備中 | 準備中 |

---

## 体験コンテンツの共通フォーマット

すべての体験は、どのプログラムからも同じ形で参照できるよう、次の構成に揃えています。

- **メタ情報**：目的 / 所要 / 利用 / 入力 / 成果
- **シナリオ**：誰が、どんな業務課題を抱えているか
- **TRY**：実行手順とプロンプト
- **REFLECT**：価値の振り返り
- **NEXT**：次の体験へのリンク

---

## 出典と注意事項

<!--- 本コンテンツは、Microsoft 提供の「M365 Copilot + Agents SMB Guided Experience」3 ガイドを基に日本語化・部品化したものです。-->
- 登場する企業名、商品名、および人物名はすべて架空のものです。
- Copilot Chat、Microsoft 365 Copilot、Researcher、Analyst、Agent Builder の画面や機能は継続的に更新されます。画面キャプチャや表示名は実際と異なる場合があります。
- 一部の演習では**自分自身の業務データ**を使います。機密情報、人事・法務・財務情報、個人情報、機微な顧客情報は使用しないでください。
