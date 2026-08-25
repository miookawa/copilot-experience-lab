---
id: EXP-CHAT-005
title: 自社ファイルを根拠に競合分析を自社視点へ引き上げる
category: 02-microsoft365-copilot
product: Microsoft 365 Copilot（Copilot Chat / Work）
level: 実践
duration: 10分（目安）
data: Lakeshore サンプルファイル
source: M365 Copilot + Agents SMB Guided Experience – Participant Guide v1.1 / 2B
---

# EXP-CHAT-005｜自社ファイルを根拠に競合分析を自社視点へ引き上げる

| 項目 | 内容 |
|---|---|
| **目的** | 一般的な競合サマリーから、自社にとっての意味を語る提言へ引き上げる |
| **所要** | 約 10 分（目安） |
| **利用** | Microsoft 365 Copilot Chat（Work） |
| **入力** | `lakeshore-prior-season-strategy.docx`、`lakeshore-brand-playbook.docx` |
| **成果** | 競合比較表 ＋ Lakeshore 固有のポジショニング提言（4〜5 文） |
| **証跡** | 引用元（ソース参照）が表示されているかを確認・記録する |

> **実施条件**：Microsoft 365 Copilot と Lakeshore ファイルにアクセスできる場合のみハンズオンで実施します。
> そうでない場合は、ファシリテーターのデモを見ながら進めてください。

---

## シナリオ

**Briana** が [EXP-CHAT-001](../01-copilot-chat/EXP-CHAT-001_競合3社のメモを比較表と示唆に変える.md) の競合スキャンに戻ってきます。
今回必要なのは、競合の一般的な状況ではなく、**その状況が Lakeshore にとって何を意味するか**です。

Lakeshore の前シーズン戦略とブランド プレイブックを使うことで、Microsoft 365 Copilot は
「一般的な競合サマリー」から「自社固有のビジネス提言」へと進みます。

> ファシリテーターの語り：「これは Section 1A への呼び戻しです。さきほど Briana が受け取ったのは一般的な競合比較でした。今回は違います。」

---

## TRY — 手順

1. Copilot Chat を開く
2. **Work** が選択されていることを確認する
3. Lakeshore ファイルが OneDrive または SharePoint にあることを確認する
4. プロンプト ボックスをクリックする
5. 次のプロンプトを貼り付ける

```text
2026 年春向けに、競合のアウトドア アパレル 3 ライン
（Adventure Works Cycles、Alpine Ski House、Boulder Innovations）を比較してください。

次の列を持つ比較表を返してください:
ブランド、主力製品、価格帯（USD）、ターゲット顧客、最近のマーケティング訴求。

そのうえで、lakeshore-prior-season-strategy.docx と lakeshore-brand-playbook.docx を使い、
これらのブランドの春のポジショニングが Lakeshore のポジショニングに具体的にどう影響するかを
4〜5 文の段落で書いてください。どこで攻めるべきか、どこで差別化すべきか、
そして前シーズンの結果から「繰り返すべきでない」ことは何かを含めてください。
```

6. **送信**を選ぶ
7. 競合比較表を確認する
8. Lakeshore 固有の提言の段落を確認する
9. 戦略文書とブランド プレイブックへの参照があるかを探す
10. 引用元やソース参照を、表示されていれば開いてみる

---

## WATCH

`../assets/EXP-CHAT-005/` に動画 / GIF を配置してください（EXP-CHAT-001 の出力との並置がおすすめ）。

---

## REFLECT — 振り返り

- [EXP-CHAT-001](../01-copilot-chat/EXP-CHAT-001_競合3社のメモを比較表と示唆に変える.md) の出力と比べて、**具体性**はどこが変わったか
- 引用元が示されることは、業務での信頼性にどう効くか
- 自社で同じことをするなら、どのファイルを Copilot に見せておくべきか

---

## NEXT

- [EXP-XLS-001｜売上データから地域別の弱点と価格施策を導く](../04-excel/EXP-XLS-001_売上データから地域別の弱点と価格施策を導く.md)
