---
layout: default
title: Copilot in 30
description: 30 日間で「自分の仕事」に Copilot を溶かし込む体験カレンダー
---

<!-- 置き場所：programs/copilot-in-30/index.md
     各扉のリンク先は ../../contents/ 配下の .html です。
     GitHub Pages は jekyll-optional-front-matter を既定で有効にしているため、
     front matter を持たない .md も .html として出力されます。
     リポジトリ上（github.com）で直接見る場合は、同じフォルダの README.md をご利用ください。 -->

<style>
.c30-hero{padding:2rem 1.6rem;margin:0 0 1.4rem;border-radius:14px;color:#fff;
  background:linear-gradient(135deg,#0f3d6e 0%,#1668b8 55%,#2aa3a3 100%);}
.c30-hero h1{margin:0 0 .4rem;font-size:1.9rem;line-height:1.3;color:#fff;border:0;}
.c30-hero p{margin:.3rem 0 0;opacity:.94;line-height:1.7;}
.c30-hero .c30-tag{display:inline-block;margin-top:.9rem;padding:.25rem .7rem;border-radius:999px;
  background:rgba(255,255,255,.18);font-size:.8rem;}

.c30-note{border:1px solid #cfe3f5;border-left:5px solid #1668b8;border-radius:12px;
  padding:1rem 1.2rem;background:#f6fbff;margin:0 0 1.6rem;}
.c30-note p{margin:.35rem 0;line-height:1.8;}
.c30-note p:first-child{margin-top:0;}
.c30-note p:last-child{margin-bottom:0;}
.c30-note code{background:#e8f1fa;padding:.1rem .35rem;border-radius:4px;font-size:.85em;}

.c30-legend{display:flex;flex-wrap:wrap;gap:.5rem;margin:0 0 1.6rem;padding:0;list-style:none;}
.c30-legend li{display:flex;align-items:center;gap:.45rem;padding:.35rem .7rem;border-radius:999px;
  background:#f2f4f7;font-size:.82rem;color:#333;}
.c30-legend li a{color:#333;text-decoration:none;}
.c30-legend li a:hover{text-decoration:underline;}
.c30-legend i{width:.7rem;height:.7rem;border-radius:50%;display:inline-block;background:var(--c);}

.c30-sec{margin:0 0 .2rem;scroll-margin-top:1rem;}
.c30-sec h3{display:flex;align-items:center;gap:.55rem;margin:0 0 .2rem;font-size:1.05rem;
  padding-bottom:.35rem;border-bottom:2px solid var(--c);}
.c30-sec h3 i{width:.7rem;height:.7rem;border-radius:50%;display:inline-block;background:var(--c);}
.c30-secnote{margin:.5rem 0 .9rem;font-size:.82rem;color:#61697a;line-height:1.75;}

.c30-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(158px,1fr));gap:.8rem;margin:0 0 2rem;}
.c30-door{display:block;position:relative;padding:.9rem .9rem 1rem;border-radius:12px;text-decoration:none;
  border:1px solid #e3e6ea;background:#fff;color:#1b1b1b;overflow:hidden;
  transition:transform .15s ease,box-shadow .15s ease,border-color .15s ease;}
.c30-door:before{content:"";position:absolute;top:0;bottom:0;left:0;width:5px;background:var(--c);}
.c30-door:hover{transform:translateY(-3px);box-shadow:0 8px 18px rgba(16,32,60,.14);
  border-color:var(--c);text-decoration:none;}
.c30-num{display:flex;align-items:baseline;gap:.35rem;font-weight:700;color:var(--c);letter-spacing:.02em;}
.c30-num b{font-size:1.6rem;line-height:1;}
.c30-num span{font-size:.72rem;opacity:.75;}
.c30-title{display:block;margin:.5rem 0 .35rem;font-size:.86rem;line-height:1.45;font-weight:600;color:#1b1b1b;}
.c30-subtitle{display:block;margin:0 0 .55rem;font-size:.73rem;line-height:1.45;color:#3f4757;}
.c30-meta{font-size:.72rem;color:#61697a;}
.c30-door.is-key:after{content:"\2605";position:absolute;top:.6rem;right:.7rem;font-size:.8rem;color:var(--c);}

.w0{--c:#475569;}
.w1{--c:#c2410c;}
.w2{--c:#1668b8;}
.w3{--c:#0f766e;}
.w4{--c:#b45309;}
.w5{--c:#6d28d9;}

.c30-start{border:1px solid #e3e6ea;border-radius:12px;padding:1rem 1.2rem;background:#fafbfc;}
.c30-start ol{margin:.4rem 0 0;padding-left:1.2rem;}
.c30-start li{margin:.25rem 0;line-height:1.7;}

.c30-stop{border:1px solid #f0d8a8;border-left:5px solid #b45309;border-radius:12px;
  padding:1rem 1.2rem;background:#fffaf0;margin:0 0 2rem;}

@media (max-width:480px){.c30-grid{grid-template-columns:repeat(auto-fill,minmax(140px,1fr));gap:.6rem;}}
</style>

<div class="c30-hero">
  <h1>Copilot in 30</h1>
  <p>1 つずつ、扉を開けるように試す 30 日間。<br>
  使うのはサンプルデータではなく、<strong>あなた自身のメール・会議・チャット・ファイル</strong>です。</p>
  <p class="c30-tag">1 つあたり 5〜20 分 &nbsp;·&nbsp; Microsoft 365 Copilot</p>
</div>

<div class="c30-note">
  <p><strong>Week はあくまで目安です。好きな扉から開けてください。</strong><br>
  上から順にやる必要はありません。今日いちばん困っていることに近い扉、面白そうな扉、どれから開けても大丈夫です。扉の番号は見分けるための番号で、順番ではありません。</p>
  <p><strong>開けた扉の最後に、次のおすすめが置いてあります。</strong><br>
  多くの扉では、ページの末尾に <code>NEXT</code> と <code>CONTINUE YOUR JOURNEY</code> があり、そこから関連する体験にそのまま進めます。気に入った扉があったら、ここに戻らず<strong>そのまま隣の扉へ</strong>進んでみてください。そうやってつながっていくのがいちばん身につきます。</p>
  <p><strong>★ が付いた扉だけは、できれば全員に開けてほしいものです。</strong>迷ったら ★ から選んでください。</p>
</div>

## 扉を選ぶ

<ul class="c30-legend">
  <li class="w0"><i></i><a href="#week0">Week 0</a></li>
  <li class="w1"><i></i><a href="#week1">Week 1</a></li>
  <li class="w2"><i></i><a href="#week2">Week 2</a></li>
  <li class="w3"><i></i><a href="#week3">Week 3</a></li>
  <li class="w4"><i></i><a href="#stop">立ち止まる</a></li>
  <li class="w5"><i></i><a href="#week4">Week 4</a></li>
</ul>

<section class="c30-sec w0" id="week0">
  <h3><i></i>Week 0 ｜ はじめる前に</h3>
  <p class="c30-secnote">正しい職場アカウントで入れることを確認します。Copilot が Microsoft 365 の信頼基盤の上にあることも、ここで押さえておきます。</p>
</section>
<div class="c30-grid w0">
  <a class="c30-door w0 is-key" href="../../contents/00-setup/SETUP-01_%E3%82%B5%E3%82%A4%E3%83%B3%E3%82%A4%E3%83%B3%E7%A2%BA%E8%AA%8D%E3%81%A8%E5%AE%89%E5%85%A8%E3%81%AAAI%E5%88%A9%E7%94%A8%E3%81%AE%E5%9C%9F%E5%8F%B0%E3%81%A5%E3%81%8F%E3%82%8A.html">
    <span class="c30-num"><b>01</b><span>DOOR</span></span>
    <span class="c30-title">サインイン確認と安全なAI利用の土台づくり</span>
    <span class="c30-subtitle">最初にここから</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w0 is-key" href="../../contents/01-copilot-chat/CHAT-IMG-01_%E8%87%AA%E5%88%86%E3%81%AE%E3%83%AF%E3%83%BC%E3%82%AF%E3%83%9A%E3%83%AB%E3%82%BD%E3%83%8A%E3%82%921%E6%9E%9A%E3%81%AE%E3%82%B9%E3%82%B1%E3%83%83%E3%83%81%E3%81%AB%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>02</b><span>DOOR</span></span>
    <span class="c30-title">自分のワークペルソナを1枚のスケッチにする</span>
    <span class="c30-subtitle">アイスブレイクにも使える</span>
    <span class="c30-meta">約 10 分</span>
  </a>
</div>

<section class="c30-sec w1" id="week1">
  <h3><i></i>Week 1 ｜ 驚いて、翌朝から使う</h3>
  <p class="c30-secnote">まず「自分の仕事を知っている」ことに驚いてください。そのうえで、毎朝の 3 分を固定します。ここで毎日の型が 1 つできると、30 日後の実感がまったく変わります。</p>
</section>
<div class="c30-grid w1">
  <a class="c30-door w1 is-key" href="../../contents/01-copilot-chat/CHAT-05_Copilot%E3%81%AF%E3%82%82%E3%81%86%E3%81%82%E3%81%AA%E3%81%9F%E3%81%AE%E4%BB%95%E4%BA%8B%E3%82%92%E7%9F%A5%E3%81%A3%E3%81%A6%E3%81%84%E3%82%8B.html">
    <span class="c30-num"><b>03</b><span>DOOR</span></span>
    <span class="c30-title">Copilotはもうあなたの仕事を知っている</span>
    <span class="c30-subtitle">一言も説明していないのに</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w1 is-key" href="../../contents/01-copilot-chat/CHAT-07_%E5%BF%99%E3%81%97%E3%81%84%E6%9C%9D%E3%82%923%E5%88%86%E3%81%A7%E6%95%B4%E7%90%86%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>04</b><span>DOOR</span></span>
    <span class="c30-title">忙しい朝を3分で整理する</span>
    <span class="c30-subtitle">毎朝の「仕事開始ボタン」を作る</span>
    <span class="c30-meta">約 5 分</span>
  </a>
  <a class="c30-door w1" href="../../contents/02-outlook-teams/CHAT-07_%E9%95%B7%E3%81%84%E3%83%A1%E3%83%BC%E3%83%AB%E3%82%B9%E3%83%AC%E3%83%83%E3%83%89%E3%81%8B%E3%82%89%E7%B5%90%E8%AB%96%E3%81%A0%E3%81%91%E3%82%92%E5%BE%97%E3%82%8B.html">
    <span class="c30-num"><b>05</b><span>DOOR</span></span>
    <span class="c30-title">長いメールスレッドから結論だけを得る</span>
    <span class="c30-subtitle">効き目が最も分かりやすい</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w1" href="../../contents/02-outlook-teams/MAL-01_%E3%83%A1%E3%83%BC%E3%83%AB%E8%BF%94%E4%BF%A1%E3%82%923%E3%83%91%E3%82%BF%E3%83%BC%E3%83%B3%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>06</b><span>DOOR</span></span>
    <span class="c30-title">メール返信を3パターン作る</span>
    <span class="c30-subtitle">選択肢は Copilot、判断は自分</span>
    <span class="c30-meta">約 5 分</span>
  </a>
  <a class="c30-door w1" href="../../contents/01-copilot-chat/CHAT-03_%E9%A1%A7%E5%AE%A2%E3%82%AF%E3%83%AC%E3%83%BC%E3%83%A0%E3%82%92%E8%AB%96%E7%82%B9%E6%95%B4%E7%90%86%E3%81%97%E8%BF%94%E4%BF%A1%E6%A1%88%E3%81%BE%E3%81%A7%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>07</b><span>DOOR</span></span>
    <span class="c30-title">顧客クレームを論点整理し返信案まで作る</span>
    <span class="c30-subtitle">自分のデータを使わずに試せる</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w1" href="../../contents/01-copilot-chat/CHAT-04_%E3%83%91%E3%83%BC%E3%83%88%E3%83%8A%E3%83%BC%E6%8F%90%E6%A1%88%E6%9B%B8%E3%82%92%E8%A6%81%E7%B4%84%E3%81%97%E7%A2%BA%E8%AA%8D%E3%81%99%E3%81%B9%E3%81%8D%E8%B3%AA%E5%95%8F%E3%82%92%E6%B4%97%E3%81%84%E5%87%BA%E3%81%99.html">
    <span class="c30-num"><b>08</b><span>DOOR</span></span>
    <span class="c30-title">パートナー提案書を要約し確認すべき質問を洗い出す</span>
    <span class="c30-subtitle">自分のデータを使わずに試せる</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w1" href="../../contents/01-copilot-chat/CHAT-09_Week%201%E3%81%AE%E9%A9%9A%E3%81%8D%E3%82%92%E8%A8%80%E8%AA%9E%E5%8C%96%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>09</b><span>DOOR</span></span>
    <span class="c30-title">Week 1の驚きを言語化する</span>
    <span class="c30-subtitle">チームに共有して締める</span>
    <span class="c30-meta">約 10 分 ＋ 共有 5 分</span>
  </a>
</div>

<section class="c30-sec w2" id="week2">
  <h3><i></i>Week 2 ｜ 会議とメールの面倒を消す</h3>
  <p class="c30-secnote">ここを抜けると「元のやり方に戻りたくない」感覚が出てきます。単発の依頼をつなげて、会議という業務プロセスごと Copilot と回してみてください。</p>
</section>
<div class="c30-grid w2">
  <a class="c30-door w2 is-key" href="../../contents/02-outlook-teams/MTG-01_%E4%BC%9A%E8%AD%B0%E3%82%92%E8%A6%81%E7%B4%84%E3%81%97%E3%83%95%E3%82%A9%E3%83%AD%E3%83%BC%E3%82%A2%E3%83%83%E3%83%97%E9%80%A3%E7%B5%A1%E6%96%87%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>10</b><span>DOOR</span></span>
    <span class="c30-title">会議を要約しフォローアップ連絡文を作る</span>
    <span class="c30-subtitle">要約から、送れる連絡文まで</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w2 is-key" href="../../contents/02-outlook-teams/MTG-03_%E4%BC%9A%E8%AD%B0%E5%89%8D%E3%81%8B%E3%82%89%E4%BC%9A%E8%AD%B0%E5%BE%8C%E3%81%BE%E3%81%A7%E3%82%92%E4%B8%80%E9%80%A3%E3%81%A7%E4%BD%BF%E3%81%86.html">
    <span class="c30-num"><b>11</b><span>DOOR</span></span>
    <span class="c30-title">会議前から会議後までを一連で使う</span>
    <span class="c30-subtitle">この週の山場</span>
    <span class="c30-meta">会議前 10 分 ＋ 会議後 10 分</span>
  </a>
  <a class="c30-door w2" href="../../contents/02-outlook-teams/MTG-02_%E4%BC%9A%E8%AD%B0%E5%BE%8C%E3%81%AE%E3%82%A2%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%82%92%E8%87%AA%E5%88%86%E7%94%A8%E3%81%AB%E5%86%8D%E6%95%B4%E7%90%86%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>12</b><span>DOOR</span></span>
    <span class="c30-title">会議後のアクションを自分用に再整理する</span>
    <span class="c30-subtitle">記録ではなく「自分の次の一手」</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w2" href="../../contents/01-copilot-chat/CHAT-08_%E4%BC%9A%E8%AD%B0%E5%89%8D%E3%81%AE_%E4%BD%95%E3%82%92%E8%A9%B1%E3%81%9B%E3%81%B0%E3%82%88%E3%81%84%E3%81%8B_%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>13</b><span>DOOR</span></span>
    <span class="c30-title">会議前の「何を話せばよいか」を作る</span>
    <span class="c30-subtitle">とりあえず参加、をやめる</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w2" href="../../contents/02-outlook-teams/CATCH-01_%E3%83%A1%E3%83%BC%E3%83%AB%E3%81%A8%E3%83%81%E3%83%A3%E3%83%83%E3%83%88%E3%81%8B%E3%82%89%E6%9C%AA%E5%AF%BE%E5%BF%9C%E3%81%AE%E3%83%95%E3%82%A9%E3%83%AD%E3%83%BC%E3%82%A2%E3%83%83%E3%83%97%E3%82%92%E6%B4%97%E3%81%84%E5%87%BA%E3%81%99.html">
    <span class="c30-num"><b>14</b><span>DOOR</span></span>
    <span class="c30-title">メールとチャットから未対応のフォローアップを洗い出す</span>
    <span class="c30-subtitle">メールと Teams を横断する</span>
    <span class="c30-meta">約 15 分</span>
  </a>
  <a class="c30-door w2" href="../../contents/01-copilot-chat/CHAT-10_%E6%9C%AA%E5%87%A6%E7%90%86%E3%83%A1%E3%83%BC%E3%83%AB%E3%82%92%E3%81%BE%E3%81%A8%E3%82%81%E3%81%A6%E6%95%B4%E7%90%86%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>15</b><span>DOOR</span></span>
    <span class="c30-title">未処理メールをまとめて整理する</span>
    <span class="c30-subtitle">判断理由つきで 4 段階に仕分け</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w2" href="../../contents/01-copilot-chat/CHAT-14_%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E3%81%AE%E7%8A%B6%E6%B3%81%E3%82%92%E6%A8%AA%E6%96%AD%E7%9A%84%E3%81%AB%E6%8A%8A%E6%8F%A1%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>16</b><span>DOOR</span></span>
    <span class="c30-title">プロジェクトの状況を横断的に把握する</span>
    <span class="c30-subtitle">散らばった情報を 1 枚に</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w2" href="../../contents/01-copilot-chat/CHAT-13_1%E6%97%A5%E3%81%AE%E7%B5%82%E3%82%8F%E3%82%8A%E3%82%92Copilot%E3%81%A7%E7%B7%A0%E3%82%81%E3%82%8B.html">
    <span class="c30-num"><b>17</b><span>DOOR</span></span>
    <span class="c30-title">1日の終わりをCopilotで締める</span>
    <span class="c30-subtitle">朝 3 分とセットで効く</span>
    <span class="c30-meta">約 5 分</span>
  </a>
</div>

<section class="c30-sec w3" id="week3">
  <h3><i></i>Week 3 ｜ 成果物を作る（自分の役割で選ぶ）</h3>
  <p class="c30-secnote">ここは全部やる必要はありません。上の 2 つを試したら、あとは<strong>自分の役割に近いものを 1〜2 つ</strong>選んでください。副題に想定する役割を書いてあります。</p>
</section>
<div class="c30-grid w3">
  <a class="c30-door w3 is-key" href="../../contents/01-copilot-chat/CHAT-18_%E6%97%A2%E5%AD%98%E8%B3%87%E6%96%99%E3%82%92%E8%A6%81%E7%B4%84%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>18</b><span>DOOR</span></span>
    <span class="c30-title">既存資料を要約する</span>
    <span class="c30-subtitle">まずこれ：説明できる状態まで一気に</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3 is-key" href="../../contents/04-word/WRD-02_%E9%95%B7%E3%81%84%E6%96%87%E6%9B%B8%E3%82%92%E3%83%AC%E3%83%93%E3%83%A5%E3%83%BC%E3%81%97%E3%81%A6%E3%82%82%E3%82%89%E3%81%86.html">
    <span class="c30-num"><b>19</b><span>DOOR</span></span>
    <span class="c30-title">長い文書をレビューしてもらう</span>
    <span class="c30-subtitle">まずこれ：書き直しではなく、指摘をもらう</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/01-copilot-chat/CHAT-11_%E3%81%93%E3%81%AE%E7%94%BB%E9%9D%A2%E3%81%AF%E4%BD%95%E3%81%8B%E3%82%92%E6%92%AE%E3%81%A3%E3%81%A6%E8%81%9E%E3%81%8F.html">
    <span class="c30-num"><b>20</b><span>DOOR</span></span>
    <span class="c30-title">この画面は何かを撮って聞く</span>
    <span class="c30-subtitle">IT・情シス</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/01-copilot-chat/CHAT-06_%E8%87%AA%E7%A4%BE%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%82%92%E6%A0%B9%E6%8B%A0%E3%81%AB%E7%AB%B6%E5%90%88%E5%88%86%E6%9E%90%E3%82%92%E8%87%AA%E7%A4%BE%E8%A6%96%E7%82%B9%E3%81%B8%E5%BC%95%E3%81%8D%E4%B8%8A%E3%81%92%E3%82%8B.html">
    <span class="c30-num"><b>21</b><span>DOOR</span></span>
    <span class="c30-title">自社ファイルを根拠に競合分析を自社視点へ引き上げる</span>
    <span class="c30-subtitle">全社視点・戦略</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/01-copilot-chat/CHAT-02_%E3%82%AD%E3%83%A3%E3%83%B3%E3%83%9A%E3%83%BC%E3%83%B3%E3%83%96%E3%83%AA%E3%83%BC%E3%83%95%E3%81%A8%E5%BD%B9%E5%93%A1%E5%90%91%E3%81%91%E3%83%97%E3%83%AC%E3%82%BC%E3%83%B3%E9%AA%A8%E5%AD%90%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>22</b><span>DOOR</span></span>
    <span class="c30-title">キャンペーンブリーフと役員向けプレゼン骨子を作る</span>
    <span class="c30-subtitle">企画・マーケティング</span>
    <span class="c30-meta">約 15 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/01-copilot-chat/CHAT-01_%E7%AB%B6%E5%90%883%E7%A4%BE%E3%81%AE%E3%83%A1%E3%83%A2%E3%82%92%E6%AF%94%E8%BC%83%E8%A1%A8%E3%81%A8%E7%A4%BA%E5%94%86%E3%81%AB%E5%A4%89%E3%81%88%E3%82%8B.html">
    <span class="c30-num"><b>23</b><span>DOOR</span></span>
    <span class="c30-title">競合3社のメモを比較表と示唆に変える</span>
    <span class="c30-subtitle">企画・マーケティング</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/04-word/WRD-01_%E7%9F%AD%E3%81%84%E3%83%96%E3%83%AA%E3%83%BC%E3%83%95%E3%82%9210%E7%AB%A0%E3%81%AE%E3%83%AD%E3%83%BC%E3%83%B3%E3%83%81%E6%96%87%E6%9B%B8%E3%81%AB%E5%B1%95%E9%96%8B%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>24</b><span>DOOR</span></span>
    <span class="c30-title">短いブリーフを10章のローンチ文書に展開する</span>
    <span class="c30-subtitle">営業・提案</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/01-copilot-chat/CHAT-16_%E8%A4%87%E6%95%B0%E8%B3%87%E6%96%99%E3%82%92%E6%AF%94%E8%BC%83%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>25</b><span>DOOR</span></span>
    <span class="c30-title">複数資料を比較する</span>
    <span class="c30-subtitle">営業・提案・調達</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/03-excel/XLS-01_%E5%A3%B2%E4%B8%8A%E3%83%87%E3%83%BC%E3%82%BF%E3%81%8B%E3%82%89%E5%9C%B0%E5%9F%9F%E5%88%A5%E3%81%AE%E5%BC%B1%E7%82%B9%E3%81%A8%E4%BE%A1%E6%A0%BC%E6%96%BD%E7%AD%96%E3%82%92%E5%B0%8E%E3%81%8F.html">
    <span class="c30-num"><b>26</b><span>DOOR</span></span>
    <span class="c30-title">売上データから地域別の弱点と価格施策を導く</span>
    <span class="c30-subtitle">データ・経営管理</span>
    <span class="c30-meta">約 15 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/05-researcher-analyst/AGT-02_Analyst%E3%81%AB%E3%83%AA%E3%82%B9%E3%82%AF%E3%81%AE%E9%AB%98%E3%81%84SKU%E7%89%B9%E5%AE%9A%E3%82%92%E5%A7%94%E4%BB%BB%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>27</b><span>DOOR</span></span>
    <span class="c30-title">Analystにリスクの高いSKU特定を委任する</span>
    <span class="c30-subtitle">データ・経営管理</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/05-researcher-analyst/AGT-01_Researcher%E3%81%AB%E5%B8%82%E5%A0%B4%E8%AA%BF%E6%9F%BB%E3%83%96%E3%83%AA%E3%83%BC%E3%83%95%E3%82%92%E5%A7%94%E4%BB%BB%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>28</b><span>DOOR</span></span>
    <span class="c30-title">Researcherに市場調査ブリーフを委任する</span>
    <span class="c30-subtitle">調査・戦略</span>
    <span class="c30-meta">約 10 分</span>
  </a>
  <a class="c30-door w3" href="../../contents/01-copilot-chat/CHAT-IMG-02_%E8%87%AA%E7%A4%BE%E3%81%AE%E3%83%9B%E3%83%BC%E3%83%A0%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%8B%E3%82%89%E4%BC%81%E6%A5%AD%E7%B4%B9%E4%BB%8B%E3%82%A4%E3%83%B3%E3%83%95%E3%82%A9%E3%82%B0%E3%83%A9%E3%83%95%E3%82%A3%E3%83%83%E3%82%AF%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>29</b><span>DOOR</span></span>
    <span class="c30-title">自社のホームページから企業紹介インフォグラフィックを作る</span>
    <span class="c30-subtitle">広報・営業</span>
    <span class="c30-meta">約 10 分</span>
  </a>
</div>

<section class="c30-sec w4" id="stop">
  <h3><i></i>立ち止まる ｜ 自分の定番を 1 つ決める</h3>
  <p class="c30-secnote">ここがこのプログラムの山場です。新しい使い方を増やすのではなく、<strong>もともと毎週・毎月やっている作業</strong>を 1 つに絞り、残りの期間は必ず Copilot から始めます。</p>
</section>
<div class="c30-grid w4">
  <a class="c30-door w4 is-key" href="../../contents/06-agent-builder/AGB-01_%E7%B9%B0%E3%82%8A%E8%BF%94%E3%81%97%E6%A5%AD%E5%8B%99%E3%82%92%E6%B4%97%E3%81%84%E5%87%BA%E3%81%97%E3%81%A61%E4%BB%B6%E3%81%AB%E7%B5%9E%E3%82%8B.html">
    <span class="c30-num"><b>30</b><span>DOOR</span></span>
    <span class="c30-title">繰り返し業務を洗い出して1件に絞る</span>
    <span class="c30-subtitle">「私の定番」を決める</span>
    <span class="c30-meta">約 15 分</span>
  </a>
  <a class="c30-door w4" href="../../contents/01-copilot-chat/CHAT-15_Copilot%E8%87%AA%E5%88%86%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9%E3%81%8B%E3%82%89%E3%83%A6%E3%83%BC%E3%82%B9%E3%82%B1%E3%83%BC%E3%82%B9%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>31</b><span>DOOR</span></span>
    <span class="c30-title">Copilot自分の使い方からユースケースを作る</span>
    <span class="c30-subtitle">任せる範囲と、自分で判断する範囲を分ける</span>
    <span class="c30-meta">約 10 分</span>
  </a>
</div>

<div class="c30-stop" markdown="1">

**「私の定番」を書き出す**

```text
私の定番
　作業名：
　発生頻度：（毎週 / 毎月 / 案件ごと）
　これまでの所要時間：
　最初に使うプロンプト：
```

向いているのは、毎週または毎月必ず発生し、毎回ゼロから書き始めていて、要約・下書き・整理から始まる作業です。判断や交渉そのものが本体の作業は向きません。

</div>

<section class="c30-sec w5" id="week4">
  <h3><i></i>Week 4 ｜ 仕組みにして、自分の型を固定する</h3>
  <p class="c30-secnote">決めた定番を、毎回ゼロから指示しなくてよい形にします。エージェントが作れない環境でも、<strong>鉄板プロンプト</strong>を持てば同じ効果が得られます。</p>
</section>
<div class="c30-grid w5">
  <a class="c30-door w5 is-key" href="../../contents/06-agent-builder/AGB-02_%E8%BB%BD%E9%87%8FAgent%20Builder%E4%BD%93%E9%A8%93.html">
    <span class="c30-num"><b>32</b><span>DOOR</span></span>
    <span class="c30-title">軽量Agent Builder体験</span>
    <span class="c30-subtitle">まずは軽く成功させる</span>
    <span class="c30-meta">約 25 分</span>
  </a>
  <a class="c30-door w5 is-key" href="../../contents/06-agent-builder/AGB-04_%E9%A1%A7%E5%AE%A2%E3%83%95%E3%82%A9%E3%83%AD%E3%83%BC%E3%82%A2%E3%83%83%E3%83%97%E7%94%A8%E3%82%A8%E3%83%BC%E3%82%B8%E3%82%A7%E3%83%B3%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>33</b><span>DOOR</span></span>
    <span class="c30-title">顧客フォローアップ用エージェントを作る</span>
    <span class="c30-subtitle">参考例：この型を自分の定番に流用する</span>
    <span class="c30-meta">約 20 分</span>
  </a>
  <a class="c30-door w5" href="../../contents/06-agent-builder/AGB-05_%E6%8F%90%E6%A1%88%E6%9B%B8%E4%BD%9C%E6%88%90%E3%82%A8%E3%83%BC%E3%82%B8%E3%82%A7%E3%83%B3%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>34</b><span>DOOR</span></span>
    <span class="c30-title">提案書作成エージェントを作る</span>
    <span class="c30-subtitle">参考例：2 つ目のエージェント</span>
    <span class="c30-meta">約 15 分</span>
  </a>
  <a class="c30-door w5" href="../../contents/06-agent-builder/AGB-03_%E3%83%9B%E3%83%AF%E3%82%A4%E3%83%88%E3%83%9C%E3%83%BC%E3%83%89%E5%86%99%E7%9C%9F%E3%81%8B%E3%82%89%E8%AD%B0%E4%BA%8B%E9%8C%B2%E3%81%A8%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%89%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>35</b><span>DOOR</span></span>
    <span class="c30-title">ホワイトボード写真から議事録とスライドを作るエージェント</span>
    <span class="c30-subtitle">共有会の見せ札に</span>
    <span class="c30-meta">約 30 分</span>
  </a>
  <a class="c30-door w5 is-key" href="../../contents/01-copilot-chat/CHAT-17_%E8%87%AA%E5%88%86%E5%B0%82%E7%94%A8%E3%81%AE%E3%80%8C%E9%89%84%E6%9D%BF%E3%83%97%E3%83%AD%E3%83%B3%E3%83%97%E3%83%88%E3%80%8D%E3%82%92%E4%BD%9C%E3%82%8B.html">
    <span class="c30-num"><b>36</b><span>DOOR</span></span>
    <span class="c30-title">自分専用の「鉄板プロンプト」を作る</span>
    <span class="c30-subtitle">ここが「なくなると困る」の核</span>
    <span class="c30-meta">約 20 分</span>
  </a>
  <a class="c30-door w5 is-key" href="../../contents/01-copilot-chat/CHAT-12_%E6%9C%9D%E3%81%BE%E3%81%9F%E3%81%AF%E5%A4%95%E6%96%B9%E3%81%AE%E3%83%97%E3%83%AD%E3%83%B3%E3%83%97%E3%83%88%E3%82%92%E5%AE%9A%E5%9E%8B%E5%8C%96%E3%81%99%E3%82%8B.html">
    <span class="c30-num"><b>37</b><span>DOOR</span></span>
    <span class="c30-title">朝または夕方のプロンプトを定型化する</span>
    <span class="c30-subtitle">毎営業日、呼び出すだけにする</span>
    <span class="c30-meta">約 10 分</span>
  </a>
</div>

---

## はじめての方へ

<div class="c30-start" markdown="1">

1. Copilot Chat を開き、**Work** が選択されていることを確認する
2. 開けたい扉を 1 つ選び、**TRY — 手順**のプロンプトをそのまま貼り付ける
3. 出てきた答えを鵜呑みにせず、**根拠リンクを 1 つ開いて確認する**
4. 最後の **REFLECT — 振り返り**に、その日のうちに答える
5. ページ末尾に **NEXT** / **CONTINUE YOUR JOURNEY** があれば、そこから次の扉へ進む

</div>

各ページは「目的 / 所要 / 利用 / 入力 / 成果」→ シナリオ → TRY（手順とプロンプト）→ REFLECT → NEXT の順に並んでいます。
うまくいかなかった依頼にも価値があります。**どう指示を変えれば直るか**まで書き残してください。

---

## 続けるコツ

- **新しい扉は週 3 回**くらいで十分です。残りの日は、気に入ったプロンプトを繰り返し使ってください。
- 効いたプロンプトは保存して、毎営業日使えるようにします。
- 週に 1 回、チームのチャネルに「今週いちばん良かった 1 件」を投稿します。
- 時間短縮は**自分で計測**します。Copilot に見積もらせないでください。
- 最終日に「元の仕事の仕方へ戻るコスト」を自分の言葉で説明できれば成功です。

---

## 実施にあたって

- 自分の実データを使います。共有・公開する成果物に機密情報が含まれていないか、必ず確認してください。
- 実業務のデータを扱いにくい場合に備えて、プロンプトに題材を含んだ扉も用意しています（Week 1 の副題「自分のデータを使わずに試せる」）。
- 利用できる機能は、ライセンスとテナント設定によって異なります。
- Excel の扉は、ファイルを OneDrive に保存し AutoSave を有効にする必要があります。
- Researcher / Analyst / Agent Builder の扉は、管理者設定・テナント構成・ライセンスによって可否が異なります。事前に管理者へ確認してください。
- ハンズオンが難しい扉は、ファシリテーターのデモを見ながら進めてください。

---

<p class="c30-meta">運営・ファシリテーター向けの進行ルールと測定項目は <a href="./README.html">プログラム概要</a> にまとめています。</p>
