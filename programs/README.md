<!--
=====================================================================
 配置先： copilot-experience-lab/programs/README.md
 新規作成。
 このコメントブロックは、コミット前に削除してください。

 【前提】リポジトリの現状（main）を確認したうえで作成しています。
 ・templates/ には README.md のみが存在します。
   HOW-TO-BUILD.md はまだ無いため、リンクしていません。
 ・ms-base/ は将来のプログラム用の空フォルダーとして記載しています。
=====================================================================
-->

# 進行プログラムの一覧

**プログラムとは、体験を並べた進行の台本です。**
体験そのものは持たず、[体験の一覧](../contents/README.md)への相対リンク・順番・必須/選択・運営ルールだけを持ちます。

実施する人は、ここから対象と時間に合うプログラムを選んでください。

## 一覧

| プログラム | 対象 | 期間・所要 | 形式 | 進行ガイド | エンドユーザー向けページ |
| --- | --- | --- | --- | --- | --- |
| Copilot in 30 | Copilot トライアルを行うお客様と、伴走支援するパートナー | Day 0 〜 Day 21（30日） | 伴走（週次の案内とチェックイン） | [README](copilot-in-30/README.md) | [GitHub Pages](https://miookawa.github.io/copilot-experience-lab/programs/copilot-in-30/) |
| M365 Copilot + Agents SMB Guided Experience | SMB のお客様と、実施するパートナー | 約 90 分 | ハンズオン／デモ | [README](smb-guided-experience/README.md) | [GitHub Pages](https://miookawa.github.io/copilot-experience-lab/programs/smb-guided-experience/) |

## プログラムの選び方

選ぶ軸は、**かけられる時間**と**相手との関係**の 2 つです。

| 状況 | 向いているプログラム |
| --- | --- |
| 短時間で価値を体感してもらいたい。その場で完結させたい | [SMB Guided Experience](smb-guided-experience/README.md) |
| 期間をかけて、業務への定着まで伴走したい | [Copilot in 30](copilot-in-30/README.md) |
| 参加者が実業務のデータを使いにくい | [SMB Guided Experience](smb-guided-experience/README.md)（レイクショアのサンプルデータで通しで実施できます） |
| 上記に当てはまらない。相手に合わせて独自に組みたい | [自分で組み立てる](templates/README.md) |

## プログラムの共通構造

プログラムは、次の 2 枚のファイルで構成します。

| ファイル | 読者 | 内容 |
| --- | --- | --- |
| `README.md` | 進行役・ファシリテーター | 進行ガイド。体験の並び、必ず案内する体験、つまずき対処、運用と指標 |
| `index.md` | エンドユーザー | GitHub Pages 用のページ。実施する体験が順番に並んでいる |

エンドユーザー向けページを持たないプログラムもあります。その場合は、進行役が README の体験リンクを直接案内します。
両方を持つ場合は、**体験の並びと ★ を `README.md` と `index.md` で一致させてください。**

補足資料（週次メールの雛形など）が必要な場合は、各プログラムのフォルダー配下に置いてください。

## 自分でプログラムを組みたいとき

相手や時間に合わせて、独自のプログラムを組めます。

**[templates/README.md](templates/README.md)** をコピーして、`programs/<プログラム名>/README.md` を作成してください。

素材となる体験は **[体験の一覧](../contents/README.md)** から選びます。
一覧の「入力データ」列で、参加者の状況に合う体験を絞り込めます。実業務のデータを使いにくい相手には、`サンプル（プロンプト内）` の体験が向いています。

> **体験の中身をプログラム配下に複製しないでください。** プログラムは、体験への相対リンクと順番だけを持ちます。

## フォルダー構成

```
programs/
├─ README.md                 … このファイル（プログラムの一覧と選び方）
├─ copilot-in-30/            … 伴走型プログラム
├─ smb-guided-experience/    … 短時間のワークショップ
├─ ms-base/                  … 将来のプログラム用（準備中）
└─ templates/                … 新規プログラムの雛形
```

## プログラムを追加したいとき

手順は **[CONTRIBUTING.md](../CONTRIBUTING.md)** を参照してください。
プログラムを追加したら、**この一覧にも 1 行追加**してください。
