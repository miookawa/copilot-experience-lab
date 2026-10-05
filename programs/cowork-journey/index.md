---
layout: default
title: Copilot Cowork Journey
description: 指示から委任へ。任せる範囲を広げながら Copilot Cowork を身につける
---

<!-- 置き場所：programs/cowork-journey/index.md
     各カードのリンク先は ../../contents/08-copilot-cowork/ 配下の .html です。
     GitHub Pages は jekyll-optional-front-matter を既定で有効にしているため、
     front matter を持たない .md も .html として出力されます。
     リポジトリ上（github.com）で直接見る場合は、同じフォルダの README.md をご利用ください。 -->

<style>
.cwj-hero{padding:2rem 1.6rem;margin:0 0 1.4rem;border-radius:14px;color:#fff;
  background:linear-gradient(135deg,#0f3d6e 0%,#1668b8 55%,#2aa3a3 100%);}
.cwj-hero h1{margin:0 0 .4rem;font-size:1.9rem;line-height:1.3;color:#fff;border:0;}
.cwj-hero p{margin:.3rem 0 0;opacity:.94;line-height:1.7;}
.cwj-hero .cwj-tag{display:inline-block;margin-top:.9rem;padding:.25rem .7rem;border-radius:999px;
  background:rgba(255,255,255,.18);font-size:.8rem;}

.cwj-note{border:1px solid #cfe3f5;border-left:5px solid #1668b8;border-radius:12px;
  padding:1rem 1.2rem;background:#f6fbff;margin:0 0 1.6rem;}
.cwj-note p{margin:.35rem 0;line-height:1.8;}
.cwj-note p:first-child{margin-top:0;}
.cwj-note p:last-child{margin-bottom:0;}

.cwj-legend{display:flex;flex-wrap:wrap;gap:.5rem;margin:0 0 1.6rem;padding:0;list-style:none;}
.cwj-legend li{display:flex;align-items:center;gap:.45rem;padding:.35rem .7rem;border-radius:999px;
  background:#f2f4f7;font-size:.82rem;color:#333;}
.cwj-legend li a{color:#333;text-decoration:none;}
.cwj-legend li a:hover{text-decoration:underline;}
.cwj-legend i{width:.7rem;height:.7rem;border-radius:50%;display:inline-block;background:var(--c);}

.cwj-sec{margin:0 0 .2rem;scroll-margin-top:1rem;}
.cwj-sec h3{display:flex;align-items:center;gap:.55rem;margin:0 0 .2rem;font-size:1.05rem;
  padding-bottom:.35rem;border-bottom:2px solid var(--c);}
.cwj-sec h3 i{width:.7rem;height:.7rem;border-radius:50%;display:inline-block;background:var(--c);}
.cwj-secnote{margin:.5rem 0 .9rem;font-size:.82rem;color:#61697a;line-height:1.75;}

.cwj-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:.8rem;margin:0 0 2rem;}
.cwj-card{display:flex;flex-direction:column;position:relative;padding:.95rem .95rem 1rem;border-radius:12px;
  text-decoration:none;border:1px solid #e3e6ea;background:#fff;color:#1b1b1b;overflow:hidden;
  transition:transform .15s ease,box-shadow .15s ease,border-color .15s ease;}
.cwj-card:before{content:"";position:absolute;top:0;bottom:0;left:0;width:5px;background:var(--c);}
.cwj-card:hover{transform:translateY(-3px);box-shadow:0 8px 18px rgba(16,32,60,.14);
  border-color:var(--c);text-decoration:none;}
.cwj-id{font-size:.74rem;font-weight:700;color:var(--c);letter-spacing:.02em;}
.cwj-title{display:block;margin:.45rem 0 .4rem;font-size:.88rem;line-height:1.5;font-weight:600;color:#1b1b1b;}
.cwj-lead{display:block;margin:0 0 .6rem;font-size:.75rem;line-height:1.55;color:#3f4757;}
.cwj-labels{display:flex;flex-wrap:wrap;gap:.3rem;margin:auto 0 .5rem;padding:0;list-style:none;}
.cwj-labels li{padding:.12rem .45rem;border:1px solid #d7dbe0;border-radius:999px;
  background:#f7f8fa;font-size:.68rem;color:#4b5563;line-height:1.5;}
.cwj-labels li.is-warn{border-color:#e7c48a;background:#fffaf0;color:#8a5a08;}
.cwj-meta{font-size:.72rem;color:#61697a;}
.cwj-card.is-key:after{content:"\2605";position:absolute;top:.6rem;right:.7rem;font-size:.8rem;color:var(--c);}

.s1{--c:#c2410c;}
.s2{--c:#1668b8;}
.s3{--c:#0f766e;}
.s4{--c:#6d28d9;}

.cwj-start{border:1px solid #e3e6ea;border-radius:12px;padding:1rem 1.2rem;background:#fafbfc;margin:0 0 1.6rem;}
.cwj-start ol{margin:.4rem 0 0;padding-left:1.2rem;}
.cwj-start li{margin:.25rem 0;line-height:1.7;}

.cwj-care{border:1px solid #f0d8a8;border-left:5px solid #b45309;border-radius:12px;
  padding:1rem 1.2rem;background:#fffaf0;margin:0 0 2rem;}
.cwj-care ul{margin:.4rem 0 0;padding-left:1.2rem;}
.cwj-care li{margin:.25rem 0;line-height:1.7;}

@media (max-width:480px){.cwj-grid{grid-template-columns:1fr;gap:.6rem;}
  .cwj-hero{padding:1.4rem 1.1rem;}.cwj-hero h1{font-size:1.55rem;}}
</style>

<div class="cwj-hero">
  <h1>Copilot Cowork Journey</h1>
  <p>指示から、委任へ。<br>
  調べる・作る・整えるまでを<strong>ひとつの依頼でまとめて任せる</strong>体験を集めました。</p>
  <p class="cwj-tag">Microsoft 365 Copilot Cowork &nbsp;·&nbsp; 1 つあたり 15〜45 分</p>
</div>

<div class="cwj-note">
  <p><strong>上から順にやる必要はありません。</strong><br>
  STEP は「どこまで任せるか」の広がりを表しています。今いちばん手間がかかっている仕事に近いものから選んでください。</p>
  <p><strong>★ は、その STEP で最初に試すのにおすすめの体験です。</strong>迷ったら ★ から始めてください。</p>
  <p><strong>カードのラベルで、今すぐ試せるかが分かります。</strong><br>
  必要なデータ、必要な環境、クレジットの目安を表示しています。環境が整っていない体験は、読んで雰囲気をつかむだけでもかまいません。</p>
  <p><strong>体験の最後に、次のおすすめがあります。</strong>ページの末尾にある <code>NEXT</code> から、関連する体験へそのまま進めます。</p>
</div>

## はじめる前に

<div class="cwj-start">
  <ol>
    <li>職場のアカウントで Microsoft 365 Copilot にサインインし、<strong>Cowork</strong> が利用できることを確認します。</li>
    <li>最初の 1 件は <strong>★ 今週の予定、整理しておきました。</strong>がおすすめです。自分のカレンダーだけで試せます。</li>
    <li>実業務のデータを使いにくい場合は、<strong>サンプルデータ</strong>のラベルが付いた体験を選んでください。</li>
  </ol>
</div>

<div class="cwj-care">
  <strong>安全に進めるために</strong>
  <ul>
    <li>予約、購入、メール送信、会議設定などの<strong>確定操作は、必ず内容を確認してから</strong>行ってください。</li>
    <li>個人情報、人事情報、評価情報を扱うときは、組織のルールに従ってください。</li>
    <li>Cowork がアクセスできない情報は結果に含まれません。重要な判断では、何を調べた結果なのかを確認してください。</li>
  </ul>
</div>

## STEP を選ぶ

<ul class="cwj-legend">
  <li class="s1"><i></i><a href="#step1">STEP 1 自分の仕事</a></li>
  <li class="s2"><i></i><a href="#step2">STEP 2 チームの仕事</a></li>
  <li class="s3"><i></i><a href="#step3">STEP 3 システムをまたぐ仕事</a></li>
  <li class="s4"><i></i><a href="#step4">STEP 4 判断を支える仕事</a></li>
</ul>

<section class="cwj-sec s1" id="step1">
  <h3><i></i>STEP 1 ｜ 自分の仕事を任せる</h3>
  <p class="cwj-secnote">まずは自分のカレンダーと受信トレイから。Cowork が勝手に実行せず、<strong>提案してから承認を求める</strong>ことを確かめてください。結果をその場で確認できるので、最初の 1 件に向いています。</p>
</section>
<div class="cwj-grid s1">
  <a class="cwj-card s1 is-key" href="../../contents/08-copilot-cowork/CWK-01_%E4%BB%8A%E9%80%B1%E3%81%AE%E4%BA%88%E5%AE%9A%E3%80%81%E6%95%B4%E7%90%86%E3%81%97%E3%81%A6%E3%81%8A%E3%81%8D%E3%81%BE%E3%81%97%E3%81%9F.html">
    <span class="cwj-id">CWK-01</span>
    <span class="cwj-title">今週の予定、整理しておきました。</span>
    <span class="cwj-lead">週の予定を読み、変更を提案。承認したものだけカレンダーに反映されます。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>標準</li><li>Light</li></ul>
    <span class="cwj-meta">約 15 分</span>
  </a>
  <a class="cwj-card s1" href="../../contents/08-copilot-cowork/CWK-03_%E8%AA%AD%E3%82%80%E3%81%AE%E3%82%92%E8%AB%A6%E3%82%81%E3%81%9F100%E9%80%9A%E3%82%92%E3%80%815%E5%88%86%E3%81%A7%E8%AA%AD%E3%82%81%E3%82%8B%E8%A8%98%E4%BA%8B%E3%81%AB%E3%81%97%E3%81%9F.html">
    <span class="cwj-id">CWK-03</span>
    <span class="cwj-title">読むのを諦めた100通を、5分で読める記事にした。</span>
    <span class="cwj-lead">1 週間分のニュースレターを、記事形式の週次ブリーフにまとめます。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>標準</li><li>Medium</li></ul>
    <span class="cwj-meta">約 20 分</span>
  </a>
  <a class="cwj-card s1" href="../../contents/08-copilot-cowork/CWK-04_%E6%9C%88%E6%9B%9C%E3%81%AE%E6%9C%9D%E3%81%AB%E3%81%AF%E3%80%81%E8%BF%94%E4%BF%A1%E4%B8%8B%E6%9B%B8%E3%81%8D%E3%81%8C%E6%8F%83%E3%81%A3%E3%81%A6%E3%81%84%E3%82%8B.html">
    <span class="cwj-id">CWK-04</span>
    <span class="cwj-title">月曜の朝には、返信下書きが揃っている。</span>
    <span class="cwj-lead">やるべきことを洗い出し、返信を下書き。毎週くり返す仕組みにします。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li class="is-warn">スケジュール実行</li><li>Medium</li></ul>
    <span class="cwj-meta">約 20 分</span>
  </a>
</div>

<section class="cwj-sec s2" id="step2">
  <h3><i></i>STEP 2 ｜ チームの仕事を任せる</h3>
  <p class="cwj-secnote">対象を、自分の予定からチームのファイルや案件へ広げます。<strong>フォルダーごと渡して</strong>、整理された成果物を受け取ってください。人が入れ替わるときの引き継ぎと受け入れも、ここで扱います。</p>
</section>
<div class="cwj-grid s2">
  <a class="cwj-card s2" href="../../contents/08-copilot-cowork/CWK-05_%E3%83%95%E3%82%A9%E3%83%AB%E3%83%80%E3%83%BC%E3%81%94%E3%81%A8%E6%B8%A1%E3%81%97%E3%81%9F%E3%82%89%E3%80%81%E6%94%B9%E5%96%84%E7%82%B9%E3%83%AA%E3%82%B9%E3%83%88%E3%81%8C%E5%87%BA%E6%9D%A5%E3%81%A6%E3%81%84%E3%81%9F.html">
    <span class="cwj-id">CWK-05</span>
    <span class="cwj-title">フォルダーごと渡したら、改善点リストが出来ていた。</span>
    <span class="cwj-lead">複数のファイルを社内基準に照らして点検し、重大度順の Excel レポートにします。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>サンプルデータ</li><li>Heavy</li></ul>
    <span class="cwj-meta">約 30 分</span>
  </a>
  <a class="cwj-card s2" href="../../contents/08-copilot-cowork/CWK-02_%E7%B5%82%E3%82%8F%E3%81%A3%E3%81%9F%E6%A1%88%E4%BB%B6%E3%82%92%E6%B8%A1%E3%81%97%E3%81%9F%E3%82%89%E3%80%81%E3%82%A2%E3%83%BC%E3%82%AB%E3%82%A4%E3%83%96%E3%82%B5%E3%82%A4%E3%83%88%E3%81%BE%E3%81%A7%E5%87%BA%E6%9D%A5%E3%81%A6%E3%81%84%E3%81%9F.html">
    <span class="cwj-id">CWK-02</span>
    <span class="cwj-title">終わった案件を渡したら、アーカイブサイトまで出来ていた。</span>
    <span class="cwj-lead">散らばったファイルを集約し、共有できる振り返りページまで作ります。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>標準</li><li>Light</li></ul>
    <span class="cwj-meta">約 20 分</span>
  </a>
  <a class="cwj-card s2" href="../../contents/08-copilot-cowork/CWK-06_%E4%BB%95%E4%BA%8B%E3%82%92%E6%AD%A2%E3%82%81%E3%81%AA%E3%81%84%E3%81%9F%E3%82%81%E3%81%AE%E5%BC%95%E3%81%8D%E7%B6%99%E3%81%8E%E3%82%92%E6%BA%96%E5%82%99%E3%81%99%E3%82%8B.html">
    <span class="cwj-id">CWK-06</span>
    <span class="cwj-title">仕事を止めないための引き継ぎを準備する</span>
    <span class="cwj-lead">送り出す側。進行中の案件と判断の背景を整理し、移管案まで用意します。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>標準</li><li>Medium</li></ul>
    <span class="cwj-meta">約 30 分</span>
  </a>
  <a class="cwj-card s2 is-key" href="../../contents/08-copilot-cowork/CWK-08_%E6%96%B0%E3%81%97%E3%81%84%E3%83%A1%E3%83%B3%E3%83%90%E3%83%BC%E3%82%9230%E6%97%A5%E5%BE%8C%E3%81%AB%E6%88%A6%E5%8A%9B%E5%8C%96%E3%81%99%E3%82%8B%E3%81%9F%E3%82%81%E3%81%AE%E6%BA%96%E5%82%99%E3%82%92%E3%80%81Cowork%E3%81%AB%E4%BB%BB%E3%81%9B%E3%82%8B.html">
    <span class="cwj-id">CWK-08</span>
    <span class="cwj-title">新しいメンバーを30日後に戦力化するための準備を、Coworkに任せる</span>
    <span class="cwj-lead">迎える側。30・60・90 日計画、進捗ダッシュボード、1on1 候補までまとめて。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>サンプルデータ</li><li>Heavy</li></ul>
    <span class="cwj-meta">約 30 分</span>
  </a>
</div>

<section class="cwj-sec s3" id="step3">
  <h3><i></i>STEP 3 ｜ システムをまたぐ仕事を任せる</h3>
  <p class="cwj-secnote">Microsoft 365 の外へ出ます。外部サイトや社内の申請画面まで含めて任せ、<strong>最後の確定操作だけを自分で行う</strong>進め方を試します。いずれもローカル ブラウザー機能が必要です。</p>
</section>
<div class="cwj-grid s3">
  <a class="cwj-card s3" href="../../contents/08-copilot-cowork/CWK-11_%E5%A4%A7%E9%98%AA%E5%87%BA%E5%BC%B5%E3%81%AE%E6%BA%96%E5%82%99%E3%80%81%E5%85%A8%E9%83%A8%E3%82%84%E3%81%A3%E3%81%A6%E3%81%8A%E3%81%84%E3%81%A6.html">
    <span class="cwj-id">CWK-11</span>
    <span class="cwj-title">大阪出張の準備、全部やっておいて。</span>
    <span class="cwj-lead">出張前。複数サイトから候補を集めて比較し、稟議メールの下書きまで。予約はしません。</span>
    <ul class="cwj-labels"><li>自分のアカウント</li><li class="is-warn">ローカル ブラウザー</li><li>Medium</li></ul>
    <span class="cwj-meta">約 20 分</span>
  </a>
  <a class="cwj-card s3 is-key" href="../../contents/08-copilot-cowork/CWK-10_%E9%A0%98%E5%8F%8E%E6%9B%B8%E9%9B%86%E3%82%81%E3%81%8B%E3%82%89%E7%94%B3%E8%AB%8B%E5%85%A5%E5%8A%9B%E3%81%BE%E3%81%A7%E3%82%92%E4%BB%BB%E3%81%9B%E3%82%8B.html">
    <span class="cwj-id">CWK-10</span>
    <span class="cwj-title">領収書集めから申請入力までを任せる</span>
    <span class="cwj-lead">出張後。メール、領収書、規程を突き合わせ、申請フォームの入力まで。送信は自分で。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li class="is-warn">ローカル ブラウザー</li><li class="is-warn">事前準備あり</li><li>Heavy</li></ul>
    <span class="cwj-meta">約 30 分</span>
  </a>
</div>

<section class="cwj-sec s4" id="step4">
  <h3><i></i>STEP 4 ｜ 判断を支える仕事を任せる</h3>
  <p class="cwj-secnote">組織の意思決定に使う成果物を任せます。読むための資料にとどまらず、<strong>その場で条件を変えて確かめられるアプリ</strong>まで作らせます。最終判断は、必ず人が行います。</p>
</section>
<div class="cwj-grid s4">
  <a class="cwj-card s4" href="../../contents/08-copilot-cowork/CWK-07_%E7%A4%BE%E5%86%85%E3%81%AE%E8%B3%9B%E6%88%90%E6%B4%BE%E3%83%BB%E5%8F%8D%E5%AF%BE%E6%B4%BE%E3%82%92%E5%85%A8%E9%83%A8%E8%AA%BF%E3%81%B9%E3%81%A6%E3%81%8D%E3%81%A6.html">
    <span class="cwj-id">CWK-07</span>
    <span class="cwj-title">社内の賛成派・反対派を全部調べてきて。</span>
    <span class="cwj-lead">会議、メール、チャット、資料に散らばった意見を横断調査し、合意形成ブリーフに。</span>
    <ul class="cwj-labels"><li>自分の業務データ</li><li>標準</li><li>Heavy</li></ul>
    <span class="cwj-meta">約 30 分</span>
  </a>
  <a class="cwj-card s4 is-key" href="../../contents/08-copilot-cowork/CWK-09_%E5%A3%B2%E4%B8%8A%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E6%B8%A1%E3%81%97%E3%81%9F%E3%82%89%E3%80%81%E5%BD%B9%E5%93%A1%E4%BC%9A%E8%B3%87%E6%96%99%E3%81%BE%E3%81%A7%E5%87%BA%E6%9D%A5%E3%81%A6%E3%81%84%E3%81%9F.html">
    <span class="cwj-id">CWK-09</span>
    <span class="cwj-title">売上データを渡したら、役員会資料まで出来ていた。</span>
    <span class="cwj-lead">分析用 Excel と役員会用 PowerPoint を、数字と結論が一致した状態で同時に。</span>
    <ul class="cwj-labels"><li>サンプルデータ</li><li>標準</li><li>Heavy</li></ul>
    <span class="cwj-meta">約 45 分</span>
  </a>
  <a class="cwj-card s4" href="../../contents/08-copilot-cowork/CWK-12_%E5%BD%B9%E5%93%A1%E4%BC%9A%E3%81%A7%E6%93%8D%E4%BD%9C%E3%81%A7%E3%81%8D%E3%82%8B%E6%8A%95%E8%B3%87%E5%88%A4%E6%96%AD%E3%82%A2%E3%83%97%E3%83%AA%E3%82%92%E4%BD%9C%E3%82%89%E3%81%9B%E3%82%8B.html">
    <span class="cwj-id">CWK-12</span>
    <span class="cwj-title">役員会で操作できる投資判断アプリを作らせる</span>
    <span class="cwj-lead">読む資料から一歩先へ。その場の質問に答えられるアプリを、会話で育てます。</span>
    <ul class="cwj-labels"><li>サンプルデータ</li><li class="is-warn">App Skill（Frontier）</li><li>Heavy</li></ul>
    <span class="cwj-meta">約 30 分</span>
  </a>
</div>

## つながっている体験

いくつかの体験は、続けて試すと 1 つの流れになります。

- **CWK-06 → CWK-08**　送り出す側の引き継ぎと、迎える側の受け入れ
- **CWK-11 → CWK-10**　出張の前の準備と、出張の後の経費申請
- **CWK-09 → CWK-12**　同じ売上データから、読む資料と、操作できるアプリへ

## 試したあとに

- どの作業が減ったかを、具体的な時間で振り返る
- 成果物の根拠を確認し、推測で補われた箇所がないかを確かめる
- 人が判断すべき箇所を決めて、チームの進め方として共有する
- 気に入った依頼は、毎週くり返す仕組みにできないか検討する

<p class="cwj-meta">進行役・ファシリテーター向けの進め方は <a href="https://github.com/miookawa/copilot-experience-lab/blob/main/programs/cowork-journey/README.md">プログラム概要</a> にまとめています。</p>
