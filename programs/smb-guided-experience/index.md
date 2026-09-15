---
layout: default
title: M365 Copilot + Agents SMB Guided Experience
description: Copilot Chat から Agent Builder までを約 90 分で体験するワークショップ
---

<script>
  (() => {
    const param = new URLSearchParams(window.location.search).get("scoutTheme");
    const theme =
      param || (window.matchMedia("(prefers-color-scheme: dark)").matches ? "dark" : "light");
    document.documentElement.setAttribute("data-theme", theme);
  })();
</script>

<style>
:root {
  color-scheme: light;
  --cp-bg: #f7f4ef;
  --cp-bg-elevated: #fcfbf8;
  --cp-surface: #ffffff;
  --cp-surface-soft: #f5f5f5;
  --cp-border: #dedede;
  --cp-border-strong: #919191;
  --cp-text: #242424;
  --cp-text-muted: #5c5c5c;
  --cp-text-soft: #6f6f6f;
  --cp-accent: #b11f4b;
  --cp-accent-hover: #9a1a41;
  --cp-accent-soft: rgba(177, 31, 75, 0.08);
  --cp-accent-fg: #ffffff;
  --cp-success: #16a34a;
  --cp-danger: #dc2626;
  --cp-warning: #f59e0b;
  --cp-link: #0078d4;
  --cp-shadow: 0 18px 48px rgba(0, 0, 0, 0.12);
  --cp-overlay: rgba(255, 255, 255, 0.8);
  --cp-panel: rgba(255, 255, 255, 0.86);
  --cp-panel-strong: rgba(255, 255, 255, 0.96);
  --cp-sheen: rgba(255, 255, 255, 0.55);
  --cp-highlight: rgba(177, 31, 75, 0.12);
}
html[data-theme="dark"] {
  color-scheme: dark;
  --cp-bg: #3d3b3a;
  --cp-bg-elevated: #343231;
  --cp-surface: #292929;
  --cp-surface-soft: #2e2e2e;
  --cp-border: #474747;
  --cp-border-strong: #5f5f5f;
  --cp-text: #dedede;
  --cp-text-muted: #919191;
  --cp-text-soft: #b0b0b0;
  --cp-accent: #fd8ea1;
  --cp-accent-hover: #fb7b91;
  --cp-accent-soft: rgba(253, 142, 161, 0.14);
  --cp-accent-fg: #1a1a1a;
  --cp-success: #4ade80;
  --cp-danger: #f87171;
  --cp-warning: #fbbf24;
  --cp-link: #4da6ff;
  --cp-shadow: 0 18px 48px rgba(0, 0, 0, 0.32);
  --cp-overlay: rgba(41, 41, 41, 0.88);
  --cp-panel: rgba(41, 41, 41, 0.72);
  --cp-panel-strong: rgba(41, 41, 41, 0.96);
  --cp-sheen: rgba(255, 255, 255, 0.04);
  --cp-highlight: rgba(253, 142, 161, 0.12);
}

.smb-page{font-family:"Segoe UI",Aptos,Calibri,-apple-system,BlinkMacSystemFont,sans-serif;color:var(--cp-text);}
.smb-hero{padding:2rem 1.6rem;margin:0 0 1.25rem;border:1px solid var(--cp-border);border-left:6px solid var(--cp-accent);border-radius:16px;background:var(--cp-bg-elevated);}
.smb-hero h1{margin:0 0 .5rem;font-size:1.9rem;line-height:1.25;color:var(--cp-text);border:0;letter-spacing:0;}
.smb-hero p{margin:.35rem 0;line-height:1.7;color:var(--cp-text-muted);}
.smb-tag{display:inline-block;margin-top:.75rem;padding:.25rem .65rem;border:1px solid var(--cp-border-strong);border-radius:.625rem;font-size:.78rem;color:var(--cp-text);}
.smb-story{display:grid;grid-template-columns:minmax(0,1.3fr) minmax(240px,.7fr);gap:1rem;margin:0 0 1.5rem;}
.smb-panel{padding:1rem 1.2rem;border:1px solid var(--cp-border);border-radius:16px;background:var(--cp-surface);}
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
.smb-nav a{display:block;padding:.4rem .7rem;border:1px solid var(--cp-border);border-radius:.625rem;background:var(--cp-surface-soft);color:var(--cp-text);text-decoration:none;font-size:.82rem;}
.smb-nav a:hover{border-color:var(--cp-accent);color:var(--cp-accent);}
.smb-stage{margin:0 0 2rem;scroll-margin-top:1rem;}
.smb-stage h2{margin:0 0 .25rem;padding:0 0 .45rem;border-bottom:2px solid var(--cp-accent);font-size:1.2rem;color:var(--cp-text);letter-spacing:0;}
.smb-stage>p{margin:.45rem 0 .9rem;color:var(--cp-text-muted);line-height:1.65;}
.smb-rule{margin:.7rem 0 .9rem;padding:.65rem .8rem;border-left:4px solid var(--cp-accent);background:var(--cp-accent-soft);color:var(--cp-text);font-weight:600;line-height:1.5;}
.smb-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(210px,1fr));gap:.8rem;}
.smb-card{display:flex;min-height:142px;flex-direction:column;padding:1rem;border:1px solid var(--cp-border);border-radius:16px;background:var(--cp-surface);color:var(--cp-text);text-decoration:none;box-shadow:0 0 2px var(--cp-border),0 1px 2px var(--cp-border);transition:transform .15s ease,border-color .15s ease;}
.smb-card:hover{transform:translateY(-2px);border-color:var(--cp-accent);text-decoration:none;}
.smb-cardhead{display:flex;align-items:center;justify-content:space-between;gap:.5rem;}
.smb-id{font-size:.75rem;font-weight:700;color:var(--cp-accent);}
.smb-status{padding:.15rem .45rem;border-radius:.625rem;background:var(--cp-accent-soft);font-size:.68rem;color:var(--cp-accent);}
.smb-card strong{display:block;margin:.6rem 0 .35rem;font-size:.92rem;line-height:1.5;color:var(--cp-text);}
.smb-card small{margin-top:auto;color:var(--cp-text-muted);line-height:1.45;}
.smb-close{padding:1rem 1.2rem;border:1px solid var(--cp-border);border-left:5px solid var(--cp-success);border-radius:16px;background:var(--cp-surface);}
.smb-close h2{margin:0 0 .5rem;font-size:1.1rem;color:var(--cp-text);border:0;letter-spacing:0;}
.smb-close ul{margin:.4rem 0 0;padding-left:1.2rem;}
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
      <li><a href="#stage2">2 業務につなげる</a></li>
      <li><a href="#stage3">3 大きな仕事を任せる</a></li>
      <li><a href="#stage4">4 繰り返しを再利用する</a></li>
    </ul>
  </nav>

  <section class="smb-stage" id="stage0">
    <h2>0 ｜ 信頼とストーリーの土台</h2>
    <p>正しい職場アカウントでサインインし、安全に体験を進める準備を整えます。</p>
    <div class="smb-rule">このステージ：必須の体験を 1 つ完了</div>
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
    <div class="smb-rule">このステージ：4 つの体験から 3 つ選択</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-01_競合3社のメモを比較表と示唆に変える.html"><span class="smb-cardhead"><span class="smb-id">CHAT-01</span><span class="smb-status">選択</span></span><strong>競合3社のメモを比較表と示唆に変える</strong><small>商品企画 ／ 比較と示唆</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-02_キャンペーンブリーフと役員向けプレゼン骨子を作る.html"><span class="smb-cardhead"><span class="smb-id">CHAT-02</span><span class="smb-status">選択</span></span><strong>キャンペーンブリーフと役員向けプレゼン骨子を作る</strong><small>マーケティング ／ 初稿作成</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-03_顧客クレームを論点整理し返信案まで作る.html"><span class="smb-cardhead"><span class="smb-id">CHAT-03</span><span class="smb-status">選択</span></span><strong>顧客クレームを論点整理し返信案まで作る</strong><small>カスタマーサポート ／ 要約と返信</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-04_パートナー提案書を要約し確認すべき質問を洗い出す.html"><span class="smb-cardhead"><span class="smb-id">CHAT-04</span><span class="smb-status">選択</span></span><strong>パートナー提案書を要約し確認すべき質問を洗い出す</strong><small>パートナー連携 ／ 会議準備</small></a>
    </div>
  </section>

  <section class="smb-stage" id="stage2">
    <h2>2 ｜ 自分の仕事につなげる</h2>
    <p>社内ファイル、メール、会議、データを使い、業務コンテキストに根ざした回答を体験します。</p>
    <div class="smb-rule">このステージ：5 つの体験から 2 つ選択</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/02-outlook-teams/CATCH-01_メールとチャットから未対応のフォローアップを洗い出す.html"><span class="smb-cardhead"><span class="smb-id">CATCH-01</span><span class="smb-status">選択</span></span><strong>メールとチャットから未対応のフォローアップを洗い出す</strong><small>Outlook / Teams ／ 自分の業務データ</small></a>
      <a class="smb-card" href="../../contents/01-copilot-chat/CHAT-06_自社ファイルを根拠に競合分析を自社視点へ引き上げる.html"><span class="smb-cardhead"><span class="smb-id">CHAT-06</span><span class="smb-status">選択</span></span><strong>自社ファイルを根拠に競合分析を自社視点へ引き上げる</strong><small>Copilot Chat ／ 社内ファイル</small></a>
      <a class="smb-card" href="../../contents/03-excel/XLS-01_売上データから地域別の弱点と価格施策を導く.html"><span class="smb-cardhead"><span class="smb-id">XLS-01</span><span class="smb-status">選択</span></span><strong>売上データから地域別の弱点と価格施策を導く</strong><small>Excel ／ 売上分析</small></a>
      <a class="smb-card" href="../../contents/04-word/WRD-01_短いブリーフを10章のローンチ文書に展開する.html"><span class="smb-cardhead"><span class="smb-id">WRD-01</span><span class="smb-status">選択</span></span><strong>短いブリーフを10章のローンチ文書に展開する</strong><small>Word ／ 文書作成</small></a>
      <a class="smb-card" href="../../contents/02-outlook-teams/MTG-01_会議を要約しフォローアップ連絡文を作る.html"><span class="smb-cardhead"><span class="smb-id">MTG-01</span><span class="smb-status">選択</span></span><strong>会議を要約しフォローアップ連絡文を作る</strong><small>Teams ／ 自分の会議</small></a>
    </div>
  </section>

  <section class="smb-stage" id="stage3">
    <h2>3 ｜ 大きな仕事を任せる</h2>
    <p>時間のかかる調査や分析をエージェントへ委任します。</p>
    <div class="smb-rule">このステージ：2 つの体験から 1 つ以上選択（体験またはデモ視聴）</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/06-researcher-analyst/AGT-01_Researcherに市場調査ブリーフを委任する.html"><span class="smb-cardhead"><span class="smb-id">AGT-01</span><span class="smb-status">選択</span></span><strong>Researcherに市場調査ブリーフを委任する</strong><small>Researcher ／ 市場調査</small></a>
      <a class="smb-card" href="../../contents/06-researcher-analyst/AGT-02_Analystにリスクの高いSKU特定を委任する.html"><span class="smb-cardhead"><span class="smb-id">AGT-02</span><span class="smb-status">選択</span></span><strong>Analystにリスクの高いSKU特定を委任する</strong><small>Analyst ／ リスク分析</small></a>
    </div>
  </section>

  <section class="smb-stage" id="stage4">
    <h2>4 ｜ 繰り返しを再利用する</h2>
    <p>定型業務を再利用可能なアシスタントにします。</p>
    <div class="smb-rule">このステージ：AGB-04 は必須。時間があれば AGB-05（発展）にも挑戦</div>
    <div class="smb-grid">
      <a class="smb-card" href="../../contents/07-agent-builder/AGB-04_顧客フォローアップ用エージェントを作る.html"><span class="smb-cardhead"><span class="smb-id">AGB-04</span><span class="smb-status">必須</span></span><strong>顧客フォローアップ用エージェントを作る</strong><small>Agent Builder ／ 定型業務の再利用</small></a>
      <a class="smb-card" href="../../contents/07-agent-builder/AGB-05_提案書作成エージェントを作る.html"><span class="smb-cardhead"><span class="smb-id">AGB-05</span><span class="smb-status">発展</span></span><strong>提案書作成エージェントを作る</strong><small>Agent Builder ／ 時間があれば</small></a>
    </div>
  </section>

  <section class="smb-close">
    <h2>振り返りと次の一歩</h2>
    <ul>
      <li>一番使えそうだった体験を 1 つ選び、自分の業務ならどう使うかを言葉にする</li>
      <li>自社で最初に作るエージェントの候補を 1 つ決める</li>
    </ul>
  </section>
</div>