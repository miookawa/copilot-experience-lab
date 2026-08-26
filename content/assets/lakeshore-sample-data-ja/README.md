# Lakeshore サンプルデータ（日本語版）

M365 Copilot + Agents SMB Guided Experience（Copilot Experience Lab 日本語版）のハンズオンで使用するサンプルデータです。
元の Lakeshore Sample Data Bundle 7 ファイルについて、**書式・数式・テーブル構造を維持したまま**、日本企業の業務文書として自然な表現・体裁に整えています。

記載内容はすべて架空のものであり、実在の企業・顧客・売上とは一切関係ありません。

---

## ファイル一覧

| ファイル | 内容 | 使用する体験 |
|---|---|---|
| `lakeshore-prior-season-strategy.docx` | 前期施策振り返り（総括、エリア別・チャネル別、今期方針） | CHAT-05 / WRD-01 |
| `lakeshore-brand-playbook.docx` | ブランドガイドライン（表現トーン、メッセージの柱、推奨・非推奨表現） | CHAT-05 / WRD-01 |
| `lakeshore-q4-sales.xlsx` | 2025年 第4四半期 売上実績（明細20,000行＋集計＋エリア別分析） | XLS-01 / WRD-01 / AGT-02 |
| `lakeshore-launch-brief-template.docx` | 発売企画書（骨子）※Copilot in Word への入力用 | WRD-01 |
| `northwind-outfitters-proposal.docx` | 取引先からの共同販促キャンペーン提案書 | CHAT-04 / AGT-04 |
| `agent-knowledge-pack.docx` | エージェント運用ガイド | AGT-03 / AGT-04 |
| `customer-complaint-cases.xlsx` | お申し出一覧10件＋エスカレーション基準 | CHAT-03（発展） |

---

## 事前準備

1. OneDrive または SharePoint に `Lakeshore Retail Immersive Experience` フォルダーを作成する
2. 上記 7 ファイルをアップロードする
3. 各ファイルを一度開き、正常に表示されることを確認する
4. Section 2・3・4 の演習が終わるまでフォルダーを保持する

> Outlook / Teams / 会議の演習では、これらのファイルは使用しません。参加者ご自身の、機密性のない業務データをお使いください。

---

## 日本語化にあたっての方針

### 文体・体裁

日本の一般企業で流通している業務文書に近づけるため、直訳を避け、文書の種類ごとに文体を整えています。

| 文書 | 想定した文書種別 | 文体 |
|---|---|---|
| 前期施策振り返り | 社内の振り返り資料 | である調。章番号を付与し、箇条書きは体言止めを基本とする |
| ブランドガイドライン | 社内規程・指針 | である調。「〜すること」の指示形 |
| 発売企画書（骨子） | 社内の企画書 | である調。目的／骨子／対象／留意点の構成 |
| 共同販促キャンペーン提案書 | 取引先からの対外提案書 | ですます調。「貴社」「弊社」「ご提案申し上げます」等の商慣行に沿った敬語 |
| エージェント運用ガイド | 社内の運用手順書 | である調の指示形 |
| お申し出一覧 | カスタマーサービスの受付台帳 | 業務記録調。お客様に関する記述は敬語 |

### 主な表記の調整

- 部門名を日本企業の一般的な名称に：カスタマーサービス部、店舗運営部、物流部、商品部、マーケティング部、品質管理部
- チャネル表記を小売実務に合わせる：店舗／EC／モール／卸売
- 「地域」→「エリア」、「製品」→「商品」など、小売業で使われる語に統一
- 対応状況を台帳表記に：未着手／対応中／先方回答待ち
- 分析シートの判定を「要対策」「要注視」とし、所見は分析コメント調に

### 原文のまま残したもの

- 架空の企業名：Lakeshore Retail、Northwind Outfitters、Adventure Works Cycles、Alpine Ski House、Boulder Innovations
- 架空の商品名：Summit Pro Jacket、Alpine Storm Shell、TrailFlex Hiking Pant など（ブランド名として機能するため）
- SKU コード：JKT-1001、WTB-6001 など
- 人物名：Eugenia Lopez、D. Patel など
- 数値・日付・金額（USD 表記を維持）
- ファイル名

商品名とファイル名を原文のまま残しているのは、演習中に参加者が貼り付けるプロンプトと表記を一致させ、Copilot が対象ファイルを正しく特定できるようにするためです。

---

## Excel ファイルについて

**`lakeshore-q4-sales.xlsx`**

- シート構成：`売上明細`（20,000行）／`集計`（SUMIFS による集計）／`エリア別分析`
- 列見出しの日本語化にあわせ、テーブル `SalesQ4` の列定義と `集計` シートの SUMIFS 数式を更新しています
- 数式が正しく計算されることを確認済みです（店舗チャネル合計 17,854,493.97 USD、北東部 13,113,555.29 USD ほか）
- XLS-01 のプロンプトは、日本語の列見出しのままで動作します

**`customer-complaint-cases.xlsx`**

- シート構成：`お申し出一覧`（10件）／`エスカレーション基準`（6件）
- テーブル `ComplaintCases` / `EscalationRules` の列定義も日本語に更新済みです

---

## 出典

Microsoft 提供の「M365 Copilot + Agents SMB Guided Experience — Lakeshore Sample Data Bundle」を日本語化したものです。
