---
layout: default
title: M365 Copilot + Agents SMB Guided Experience
description: Copilot Chat から Agent Builder までを約 90 分で体験するワークショップ
---

<style>
:root {
  --cp-surface: #ffffff;
  --cp-surface-soft: #f2f4f7;
  --cp-border: #e3e6ea;
  --cp-border-strong: #aab2bf;
  --cp-text: #1b1b1b;
  --cp-text-muted: #61697a;
  --cp-accent: #1668b8;
  --cp-accent-hover: #0f579c;
  --cp-accent-soft: #e8f1fa;
  --cp-accent-fg: #ffffff;
  --cp-success: #16a34a;
}

.smb-page{color:var(--cp-text);}
.smb-hero{padding:2rem 1.6rem;margin:0 0 1.25rem;border-radius:14px;color:#fff;background:linear-gradient(135deg,#0f3d6e 0%,#1668b8 55%,#2aa3a3 100%);}
.smb-hero h1{margin:0 0 .5rem;font-size:1.9rem;line-height:1.25;color:#fff;border:0;letter-spacing:0;}
.smb-hero p{margin:.35rem 0;line-height:1.7;color:#fff;}
.smb-tag{display:inline-block;margin-top:.75rem;padding:.25rem .65rem;border:0;border-radius:999px;background:rgba(255,255,255,.18);font-size:.78rem;color:#fff;}
.smb-story{display:grid;grid-template-columns:minmax(0,1.3fr) minmax(240px,.7fr);gap:1rem;margin:0 0 1.5rem;}
.smb-panel{padding:1rem 1.2rem;border:1px solid #cfe3f5;border-radius:12px;background:#f6fbff;}
.smb-panel h2{margin:0 0 .5rem;font-size:1.1rem;color:var(--cp-text);border:0;letter-spacing:0;}
.smb-panel p{margin:.3rem 0;line-height:1.7;color:var(--cp-text-muted);}
.smb-people{grid-column:1/-1;overflow-x:auto;}
.smb-people table{width:100%;margin:.5rem 0 0;border-collapse:collapse;font-size:.84rem;}
.smb-people th,.smb-people td{padding:.55rem .65rem;border:1px solid var(--cp-border);text-align:left;vertical-align:top;}
.smb-people th{background:var(--cp-surface-soft);color:var(--cp-text);}
.smb-people td{color:var(--cp-text-muted);}
.smb-download{display:inline-block;margin-top:.7rem;padding:.5rem .8rem;border-radius:.625rem;background:var(--cp-accent);color:var(--cp-accent-fg)!important;text-decoration:none;font-weight:600;}
.smb-download:hover{background:var(--cp-accent-hover);text-decoration:none;}
.smb-nav{display:flex;flex-wrap:wrap;gap:.5rem;margin:0 0 1.5rem;padding:0;list-style:none;}
.smb-nav li:nth-child(1),#stage0{--c:#475569;}
.smb-nav li:nth-child(2),#stage1{--c:#c2410c;}
.smb-nav li:nth-child(3),#stage2{--c:#1668b8;}
.smb-nav li:nth-child(4),#stage3{--c:#0f766e;}
.smb-nav li:nth-child(5),#stage4{--c:#6d28d9;}
.smb-nav a{display:block;padding:.4rem .7rem;border:1px solid var(--cp-border);border-left:4px solid var(--c);border-radius:.625rem;background:var(--cp-surface-soft);color:var(--cp-text);text-decoration:none;font-size:.82rem;}
.smb-nav a:hover{border-color:var(--c);color:var(--c);}
.smb-stage{margin:0 0 2rem;scroll-margin-top:1rem;}
.smb-stage h2{margin:0 0 .25rem;padding:0 0 .45rem;border-bottom:2px solid var(--c);font-size:1.2rem;color:var(--cp-text);letter-spacing:0;}
.smb-stage>p{margin:.45rem 0 .9rem;color:var(--cp-text-muted);line-height:1.65;}
.smb-rule{margin:.55rem 0 .9rem;padding:.45rem .65rem;border:1px solid var(--cp-border);border-left:4px solid var(--c);border-radius:.375rem;background:var(--cp-surface-soft);color:var(--cp-text-muted);font-size:.82rem;font-weight:400;line-height:1.5;}
.smb-rule strong{color:var(--cp-text);font-weight:600;}
.smb-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(210px,1fr));gap:.8rem;}
.smb-card{display:flex;position:relative;min-height:142px;flex-direction:column;padding:1rem;border:1px solid var(--cp-border);border-radius:12px;background:var(--cp-surface);color:var(--cp-text);text-decoration:none;overflow:hidden;transition:transform .15s ease,box-shadow .15s ease,border-color .15s ease;}
.smb-card:before{content:"";position:absolute;top:0;bottom:0;left:0;width:5px;background:var(--c);}
.smb-card:hover{transform:translateY(-3px);border-color:var(--c);box-shadow:0 8px 18px rgba(16,32,60,.14);text-decoration:none;}
.smb-cardhead{display:flex;align-items:center;justify-content:space-between;gap:.5rem;}
.smb-id{font-size:.75rem;font-weight:700;color:var(--c);}
.smb-status{padding:.15rem .45rem;border:1px solid var(--c);border-radius:999px;background:#fff;font-size:.68rem;color:var(--c);}
.smb-card strong{display:block;margin:.6rem 0 .35rem;font-size:.92rem;line-height:1.5;color:var(--cp-text);}
.smb-card small{margin-top:auto;color:var(--cp-text-muted);line-height:1.45;}
.smb-close{margin:2.4rem 0 0;}
.smb-close h2{margin:0 0 .8rem;padding:0 0 .45rem;border:0;border-bottom:2px solid #0f766e;font-size:1.2rem;color:#0f766e;letter-spacing:0;}
.smb-close ol{margin:0;padding:1rem 1.2rem 1rem 2.5rem;border:1px solid #e3e6ea;border-radius:12px;background:#fafbfc;}
.smb-close li{margin:.3rem 0;line-height:1.6;}
@media(max-width:680px){.smb-story{grid-template-columns:1fr}.smb-hero{padding:1.4rem 1.1rem}.smb-hero h1{font-size:1.55rem}.smb-grid{grid-template-columns:1fr}}
</style>

<div class="smb-page">
  <header class="smb-hero">
    <h1>M365 Copilot + Agents SMB Guided Experience</h1>
    <p>Copilot Chat から Microsoft 365 Copilot、Researcher / Analyst、Agent Builder までを、ひとつのビジネス ストーリーで体験します。</p>
    <span class="smb-tag">約 90 分 ／ ハンズオンまたはデモ</span>
  </header>

  <div class="smb-story">
    <section class="smb-panel">
      <h2>今日のストーリー</h2>
      <p>架空の小売企業 <strong>レイクショア</strong>は、春の「スプリングアウトドア」ラインを 6 週間後に発売します。各部門の仕事を進めながら、AI がどこで力を発揮するかを確かめます。</p>
    </section>
    <aside class="smb-panel">
      <h2>始める前に</h2>
      <p>進行役の案内に従い、利用できる体験から進めてください。Outlook / Teams では、機密性のない自分の業務データだけを使用します。</p>
      <a class="smb-download" href="https://github.com/miookawa/copilot-experience-lab/releases/download/lakeshore-sample-data-ja-v1.0.0/lakeshore-sample-data-ja.zip">サンプルデータ一式をダウンロード</a>
    </aside>
    <section class="smb-panel smb-people">
      <h2>登場人物と担当する体験</h2>
      <table>
        <thead><tr><th>登場人物</th><th>役割</th><th>担当する体験</th></tr></thead>
        <tbody>
          <tr><td>曽根拓海</td><td>商品企画部長</td><td>CHAT-01 / CHAT-06 / XLS-01</td></tr>
          <tr><td>大沢澪</td><td>マーケティング部長</td><td>CHAT-02 / WRD-01</td></tr>
          <tr><td>遠藤淳也</td><td>カスタマーサポート責任者</td><td>CHAT-03 / AGB-04</td></tr>
          <tr><td>松吉優香</td><td>パートナー連携責任者</td><td>CHAT-04 / AGB-04 / AGB-05</td></tr>
          <tr><td>山本夏帆</td><td>店舗運営部長</td><td>MTG-01</td></tr>
          <tr><td>リーダーシップ チーム</td><td>経営陣</td><td>AGT-01 / AGT-02</td></tr>
        </tbody>
      </table>
    </section>
  </div>

  <nav aria-label="体験ステージ">
    <ul class="smb-nav">
      <li><a href="#stage0">0 信頼の土台</a></li>
      <li><a href="#stage1">1 早く着手する</a></li>
      <li><a href="#stage2">2 業務コンテキストを活用する</a></li>
      <li><a href="#stage3">3 大きな仕事を委任する</a></li>
      <li><a href="#stage4">4 繰り返し業務を仕組み化する</a></li>
    </ul>
  </nav>

  <section class="smb-stage" id="stage0">
    <h2>0 ｜ 信頼とストーリーの土台</h2>
    <p>正しい職場アカウントでサインインし、安全に体験を進める準備を整えます。</p>
    <div class="smb-rule"><strong>完了条件：</strong>SETUP-01 を完了する</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/00-setup/SETUP-01_サインイン確認と安全なAI利用の土台づくり.html">
        <span class="smb-cardhead"><span class="smb-id">SETUP-01</span><span class="smb-status">必須</span></span>
        <strong>サインイン確認と安全なAI利用の土台づくり</strong>
        <small>全員のアカウントとデータの扱いを確認</small>
      </a>
    </div>
  </section>

  <section class="smb-stage" id="stage1">
    <h2>1 ｜ 早く着手する</h2>
    <p>調査、執筆、要約、発想を Copilot Chat で始め、最初の成功体験を作ります。</p>
    <div class="smb-rule"><strong>完了条件：</strong>4 つの体験から 3 つを選んで完了する</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-01_競合3社のメモを比較表と示唆に変える.html"><span class="smb-cardhead"><span class="smb-id">CHAT-01</span><span class="smb-status">選択</span></span><strong>競合3社のメモを比較表と示唆に変える</strong><small>商品企画 ／ 比較と示唆</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-02_キャンペーンブリーフと役員向けプレゼン骨子を作る.html"><span class="smb-cardhead"><span class="smb-id">CHAT-02</span><span class="smb-status">選択</span></span><strong>キャンペーンブリーフと役員向けプレゼン骨子を作る</strong><small>マーケティング ／ 初稿作成</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-03_顧客クレームを論点整理し返信案まで作る.html"><span class="smb-cardhead"><span class="smb-id">CHAT-03</span><span class="smb-status">選択</span></span><strong>顧客クレームを論点整理し返信案まで作る</strong><small>カスタマーサポート ／ 要約と返信</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-04_パートナー提案書を要約し確認すべき質問を洗い出す.html"><span class="smb-cardhead"><span class="smb-id">CHAT-04</span><span class="smb-status">選択</span></span><strong>パートナー提案書を要約し確認すべき質問を洗い出す</strong><small>パートナー連携 ／ 会議準備</small></a>
    </div>
  </section>

  <section class="smb-stage" id="stage2">
    <h2>2 ｜ 業務コンテキストを活用する</h2>
    <p>社内ファイル、メール、会議、データを使い、業務コンテキストに根ざした回答を体験します。</p>
    <div class="smb-rule"><strong>完了条件：</strong>5 つの体験から 2 つを選んで完了する</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/02-outlook-teams/CATCH-01_メールとチャットから未対応のフォローアップを洗い出す.html"><span class="smb-cardhead"><span class="smb-id">CATCH-01</span><span class="smb-status">選択</span></span><strong>メールとチャットから未対応のフォローアップを洗い出す</strong><small>Outlook / Teams ／ 自分の業務データ</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-06_自社ファイルを根拠に競合分析を自社視点へ引き上げる.html"><span class="smb-cardhead"><span class="smb-id">CHAT-06</span><span class="smb-status">選択</span></span><strong>自社ファイルを根拠に競合分析を自社視点へ引き上げる</strong><small>Copilot Chat ／ 社内ファイル</small></a>
      <a class="smb-card" href="../../contents/03-excel/XLS-01_売上データから地域別の弱点と価格施策を導く.html"><span class="smb-cardhead"><span class="smb-id">XLS-01</span><span class="smb-status">選択</span></span><strong>売上データから地域別の弱点と価格施策を導く</strong><small>Excel ／ 売上分析</small></a>
      <a class="smb-card" href="../../contents/04-word/WRD-01_短いブリーフを10章のローンチ文書に展開する.html"><span class="smb-cardhead"><span class="smb-id">WRD-01</span><span class="smb-status">選択</span></span><strong>短いブリーフを10章のローンチ文書に展開する</strong><small>Word ／ 文書作成</small></a>
      <a class="smb-card" href="../../contents/02-outlook-teams/MTG-01_会議を要約しフォローアップ連絡文を作る.html"><span class="smb-cardhead"><span class="smb-id">MTG-01</span><span class="smb-status">選択</span></span><strong>会議を要約しフォローアップ連絡文を作る</strong><small>Teams ／ 自分の会議</small></a>
    </div>
  </section>

  <section class="smb-stage" id="stage3">
    <h2>3 ｜ 大きな仕事を委任する</h2>
    <p>時間のかかる調査や分析をエージェントへ委任します。</p>
    <div class="smb-rule"><strong>完了条件：</strong>2 つの体験から 1 つ以上を選び、自分で操作するかデモを視聴する</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/06-researcher-analyst/AGT-01_Researcherに市場調査ブリーフを委任する.html"><span class="smb-cardhead"><span class="smb-id">AGT-01</span><span class="smb-status">選択</span></span><strong>Researcherに市場調査ブリーフを委任する</strong><small>Researcher ／ 市場調査</small></a>
      <a class="smb-card" href="../../contents/06-researcher-analyst/AGT-02_Analystにリスクの高いSKU特定を委任する.html"><span class="smb-cardhead"><span class="smb-id">AGT-02</span><span class="smb-status">選択</span></span><strong>Analystにリスクの高いSKU特定を委任する</strong><small>Analyst ／ リスク分析</small></a>
    </div>
  </section>

  <section class="smb-stage" id="stage4">
    <h2>4 ｜ 繰り返し業務を仕組み化する</h2>
    <p>定型業務を再利用可能なアシスタントにします。</p>
    <div class="smb-rule"><strong>完了条件：</strong>AGB-04 を完了する。時間に余裕があれば AGB-05 にも取り組む</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/07-agent-builder/AGB-04_顧客フォローアップ用エージェントを作る.html"><span class="smb-cardhead"><span class="smb-id">AGB-04</span><span class="smb-status">必須</span></span><strong>顧客フォローアップ用エージェントを作る</strong><small>Agent Builder ／ 定型業務の再利用</small></a>
      <a class="smb-card" href="../../contents/07-agent-builder/AGB-05_提案書作成エージェントを作る.html"><span class="smb-cardhead"><span class="smb-id">AGB-05</span><span class="smb-status">発展</span></span><strong>提案書作成エージェントを作る</strong><small>Agent Builder ／ 時間があれば</small></a>
    </div>
  </section>

  <section class="smb-close">
    <h2>振り返りと次の一歩</h2>
    <ol>
      <li>一番使えそうだった体験を 1 つ選び、自分の業務ならどう使うかを言葉にする</li>
      <li>自社で最初に作るエージェントの候補を 1 つ決める</li>
    </ol>
  </section>
</div>