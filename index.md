---
layout: default
title: Copilot Experience Lab
description: 自分の仕事で試す、Microsoft 365 Copilot 体験ラボ

# 扉（カード）は、この groups の順に contents/<dir>/ 配下の実ファイルから
# 自動生成されます。コンテンツを追加・リネームしても index.md の修正は不要です。
#
# 各コンテンツ .md の front matter で見え方を調整できます（すべて任意）:
#   title:    カードの見出し（未指定ならファイル名から生成）
#   subtitle: 見出し下の一文
#   minutes:  所要分数（例: 10 -> 「約 10 分」）
#   duration: 自由記述の所要（minutes より優先）
#   key:      true にすると ★ が付きます
#
# 現在の contents/ 配下は front matter を持たないため、★ は下の key: 一覧で指定します。
# 体験 ID（例: SETUP-01）か、ファイル名から拡張子を除いた文字列を書いてください。
groups:
  - dir: "00-setup"
    cls: "g0"
    label: "Setup"
    lead: "はじめる前に。環境と進め方をそろえる"
  - dir: "01-copilot-chat"
    cls: "g1"
    label: "Copilot Chat"
    lead: "まず驚く。自分のデータで対話する"
  - dir: "02-outlook-teams"
    cls: "g2"
    label: "Outlook / Teams"
    lead: "毎日の面倒を減らす。メールと会議"
  - dir: "03-excel"
    cls: "g3"
    label: "Excel"
    lead: "数字から示唆を取り出す"
  - dir: "04-word"
    cls: "g4"
    label: "Word"
    lead: "文書をゼロから書かない"
  - dir: "05-researcher-analyst"
    cls: "g5"
    label: "Researcher / Analyst"
    lead: "調べる・分析するを任せる"
  - dir: "06-agent-builder"
    cls: "g6"
    label: "Agent Builder"
    lead: "自分専用のエージェントを作る"
  - dir: "07-powerpoint"
    cls: "g7"
    label: "PowerPoint"
    lead: "伝わる資料に仕上げる"
  - dir: "08-personas"
    cls: "g8"
    label: "Personas"
    lead: "役割別の使いどころ"

# ★ を付ける扉（プログラムで「必須」として使っている体験）
key:
  - "SETUP-01"
  - "CHAT-IMG-01"
  - "CHAT-05_自社ファイルを根拠に競合分析を自社視点へ引き上げる"
  - "CHAT-06"
  - "CATCH-01"
  - "MTG-01"
  - "XLS-01"
  - "WRD-01"
  - "AGB-04"

# プログラム（連続体験）のカード。リンク先は programs/<dir>/ の
# index.md（あれば）または README.md を自動で選びます。
programs:
  - dir: "copilot-in-30"
    cls: "g2"
    label: "Copilot in 30"
    lead: "30 日間で、繰り返し業務を 1 つ Copilot に置き換える"
    meta: "Day 0 〜 Day 21 ／ 週 1 回の伴走"
  - dir: "smb-guided-experience"
    cls: "g5"
    label: "SMB Guided Experience"
    lead: "Chat から Agent Builder までを一気通貫で体験する"
    meta: "約 90 分 ／ ハンズオンまたはデモ"
---

<!-- GitHub Pages (Jekyll 3.x) 用トップページ。
     扉のリンクは site.pages / site.static_files から自動生成しているため、
     ファイル名をここに書き写す必要はありません。
     Jekyll 4 専用の記法（where_exp の and/or、push フィルター）は使っていません。 -->

<style>
.cel-hero{padding:2rem 1.6rem;margin:0 0 1.6rem;border-radius:14px;color:#fff;
  background:linear-gradient(135deg,#0f3d6e 0%,#1668b8 55%,#2aa3a3 100%);}
.cel-hero h1{margin:0 0 .4rem;font-size:1.9rem;line-height:1.3;color:#fff;border:0;}
.cel-hero p{margin:.3rem 0 0;opacity:.94;line-height:1.7;}
.cel-hero .cel-tag{display:inline-block;margin-top:.9rem;padding:.25rem .7rem;border-radius:999px;
  background:rgba(255,255,255,.18);font-size:.8rem;}

.cel-legend{display:flex;flex-wrap:wrap;gap:.5rem;margin:0 0 1.6rem;padding:0;list-style:none;}
.cel-legend li{display:flex;align-items:center;gap:.45rem;padding:.35rem .7rem;border-radius:999px;
  background:#f2f4f7;font-size:.82rem;color:#333;}
.cel-legend a{color:#333;text-decoration:none;}
.cel-legend a:hover{text-decoration:underline;}
.cel-legend i{width:.7rem;height:.7rem;border-radius:50%;display:inline-block;background:var(--c);}

.cel-sec{margin:0 0 2.2rem;scroll-margin-top:1rem;}
.cel-sec h2{display:flex;align-items:center;gap:.55rem;margin:0 0 .15rem;font-size:1.15rem;
  padding-bottom:.35rem;border-bottom:2px solid var(--c);}
.cel-sec h2 i{width:.7rem;height:.7rem;border-radius:50%;display:inline-block;background:var(--c);}
.cel-sec h2 em{margin-left:auto;font-style:normal;font-size:.72rem;font-weight:400;color:#61697a;}
.cel-lead{margin:.45rem 0 .9rem;font-size:.85rem;color:#61697a;line-height:1.6;}

.cel-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(158px,1fr));gap:.8rem;margin:0;}
.cel-door{display:block;position:relative;padding:.9rem .9rem 1rem;border-radius:12px;text-decoration:none;
  border:1px solid #e3e6ea;background:#fff;color:#1b1b1b;overflow:hidden;
  transition:transform .15s ease,box-shadow .15s ease,border-color .15s ease;}
.cel-door:before{content:"";position:absolute;top:0;bottom:0;left:0;width:5px;background:var(--c);}
.cel-door:hover{transform:translateY(-3px);box-shadow:0 8px 18px rgba(16,32,60,.14);
  border-color:var(--c);text-decoration:none;}
.cel-num{display:flex;align-items:baseline;gap:.35rem;font-weight:700;color:var(--c);letter-spacing:.02em;}
.cel-num b{font-size:1.6rem;line-height:1;}
.cel-num span{font-size:.72rem;opacity:.75;}
.cel-title{display:block;margin:.5rem 0 .3rem;font-size:.86rem;line-height:1.45;font-weight:600;color:#1b1b1b;}
.cel-subtitle{display:block;margin:0 0 .5rem;font-size:.73rem;line-height:1.45;color:#3f4757;}
.cel-meta{font-size:.72rem;color:#61697a;}
.cel-door.is-key:after{content:"\2605";position:absolute;top:.6rem;right:.7rem;font-size:.8rem;color:var(--c);}

.cel-start{border:1px solid #e3e6ea;border-radius:12px;padding:1rem 1.2rem;background:#fafbfc;}
.cel-start ol{margin:.4rem 0 0;padding-left:1.2rem;}
.cel-start li{margin:.25rem 0;line-height:1.7;}

.g0{--c:#475569;} .g1{--c:#c2410c;} .g2{--c:#1668b8;} .g3{--c:#0f766e;} .g4{--c:#15803d;}
.g5{--c:#1d4ed8;} .g6{--c:#6d28d9;} .g7{--c:#b91c1c;} .g8{--c:#b45309;} .g9{--c:#9d174d;}

@media (max-width:480px){.cel-grid{grid-template-columns:repeat(auto-fill,minmax(136px,1fr));gap:.6rem;}}
</style>

<div class="cel-hero">
  <h1>Copilot Experience Lab</h1>
  <p>1 つずつ、扉を開けるように試す体験ラボ。<br>
  使うのはサンプルデータではなく、<strong>あなた自身のメール・会議・チャット・ファイル</strong>です。</p>
  <p class="cel-tag">所要 5〜30 分 / 1 コンテンツ &nbsp;·&nbsp; Microsoft 365 Copilot</p>
</div>

## 今日の扉を開ける

順番どおりでなくて構いません。**開けたい扉から開けてください**。
★ の付いた扉は、期間中に何度も繰り返す価値のある体験です。

{% comment %}
  front matter 付きページと素の .md を 1 つの配列にまとめる。
  GitHub Pages の jekyll-optional-front-matter は、front matter を持たない .md を
  ページへ変換したうえで、既定では元の .md を静的ファイルとしても出力します。
  そのため同じファイルが site.pages と site.static_files の両方に現れ、
  そのまま並べると扉が二重に描画されます。以下ではファイル名で重複を除外し、
  先に来るページ側（正しい .html リンクを持つ方）だけを採用しています。
{% endcomment %}
{% assign celall = site.pages | concat: site.static_files %}
{% assign celkeys = page.key | join: "," | prepend: "," | append: "," %}

{% comment %} ---------- 凡例（件数付き） ---------- {% endcomment %}
{% assign celtotal = 0 %}
<ul class="cel-legend">
{%- for g in page.groups -%}
  {%- assign dirkey = "contents/" | append: g.dir | append: "/" -%}
  {%- assign pool = celall | where_exp: "p", "p.path contains dirkey" -%}
  {%- assign cnt = 0 -%}
  {%- assign seen = "," -%}
  {%- for p in pool -%}
    {%- assign ok = false -%}
    {%- if p.extname -%}
      {%- if p.extname == ".md" -%}{%- assign ok = true -%}{%- endif -%}
    {%- else -%}
      {%- assign ok = true -%}
    {%- endif -%}
    {%- if p.name == "index.md" -%}{%- assign ok = false -%}{%- endif -%}
    {%- if p.name == "README.md" -%}{%- assign ok = false -%}{%- endif -%}
    {%- assign namekey = p.name | prepend: "," | append: "," -%}
    {%- if seen contains namekey -%}{%- assign ok = false -%}{%- endif -%}
    {%- if ok -%}
      {%- assign seen = seen | append: p.name | append: "," -%}
      {%- assign cnt = cnt | plus: 1 -%}
    {%- endif -%}
  {%- endfor -%}
  {%- assign celtotal = celtotal | plus: cnt -%}
  {%- if cnt > 0 -%}
  <li class="{{ g.cls }}"><i></i><a href="#{{ g.dir }}">{{ g.label }}</a>（{{ cnt }}）</li>
  {%- endif -%}
{%- endfor -%}
</ul>

<p class="cel-lead">現在 {{ celtotal }} 件の扉があります。自分のデータを使いにくい扉は、架空企業「レイクショア」の<a href="{{ '/contents/assets/lakeshore-sample-data-ja.zip' | relative_url }}">サンプルデータ一式</a>でも試せます。</p>

{% comment %} ---------- セクションごとの扉グリッド ---------- {% endcomment %}
{% for g in page.groups %}
  {%- assign dirkey = "contents/" | append: g.dir | append: "/" -%}
  {%- assign pool = celall | where_exp: "p", "p.path contains dirkey" -%}

  {%- assign cnt = 0 -%}
  {%- assign seen = "," -%}
  {%- for p in pool -%}
    {%- assign ok = false -%}
    {%- if p.extname -%}
      {%- if p.extname == ".md" -%}{%- assign ok = true -%}{%- endif -%}
    {%- else -%}
      {%- assign ok = true -%}
    {%- endif -%}
    {%- if p.name == "index.md" -%}{%- assign ok = false -%}{%- endif -%}
    {%- if p.name == "README.md" -%}{%- assign ok = false -%}{%- endif -%}
    {%- assign namekey = p.name | prepend: "," | append: "," -%}
    {%- if seen contains namekey -%}{%- assign ok = false -%}{%- endif -%}
    {%- if ok -%}
      {%- assign seen = seen | append: p.name | append: "," -%}
      {%- assign cnt = cnt | plus: 1 -%}
    {%- endif -%}
  {%- endfor -%}

  {%- if cnt > 0 -%}
<section class="cel-sec {{ g.cls }}" id="{{ g.dir }}">
  <h2><i></i>{{ g.label }}<em>{{ g.dir }} ／ {{ cnt }} 件</em></h2>
  <p class="cel-lead">{{ g.lead }}</p>
  <div class="cel-grid">

  {%- comment -%} 同じファイル名を 2 度描画しないための記録（ページ側を優先） {%- endcomment -%}
  {%- assign drawn = "," -%}

  {%- comment -%} 第 1 パス：ファイル名先頭の連番（例 CHAT-05_）で昇順に描画 {%- endcomment -%}
  {%- for n in (0..59) -%}
    {%- assign pad = n | prepend: "0" | slice: -2, 2 -%}
    {%- for p in pool -%}
      {%- assign ok = false -%}
      {%- if p.extname -%}
        {%- if p.extname == ".md" -%}{%- assign ok = true -%}{%- endif -%}
      {%- else -%}
        {%- assign ok = true -%}
      {%- endif -%}
      {%- if p.name == "index.md" -%}{%- assign ok = false -%}{%- endif -%}
      {%- if p.name == "README.md" -%}{%- assign ok = false -%}{%- endif -%}
      {%- if ok -%}
        {%- assign stem = p.name | replace: ".markdown", "" | replace: ".md", "" | replace: ".html", "" -%}
        {%- assign seg = stem | split: "_" -%}
        {%- assign code = seg | first -%}
        {%- assign cp = code | split: "-" -%}
        {%- assign num = cp | last -%}
        {%- assign chk = num | plus: 0 | prepend: "0" | slice: -2, 2 -%}
        {%- if cp.size > 1 and chk == num and num == pad -%}
        {%- assign numsuffix = num | prepend: "-" -%}
        {%- assign kind = code | replace_first: numsuffix, "" -%}
        {%- assign fallback = stem | remove_first: code | remove_first: "_" -%}
        {%- assign iskey = false -%}
        {%- if p.key -%}{%- assign iskey = true -%}{%- endif -%}
        {%- assign kstem = stem | prepend: "," | append: "," -%}
        {%- assign kcode = code | prepend: "," | append: "," -%}
        {%- if celkeys contains kstem -%}{%- assign iskey = true -%}{%- endif -%}
        {%- if celkeys contains kcode -%}{%- assign iskey = true -%}{%- endif -%}
        {%- assign namekey = p.name | prepend: "," | append: "," -%}
        {%- unless drawn contains namekey -%}
        {%- assign drawn = drawn | append: p.name | append: "," -%}
    <a class="cel-door {{ g.cls }}{% if iskey %} is-key{% endif %}" href="{{ p.url | default: p.path | relative_url }}">
      <span class="cel-num"><b>{{ num }}</b><span>{{ kind }}</span></span>
      <span class="cel-title">{{ p.title | default: fallback }}</span>
      {%- if p.subtitle %}<span class="cel-subtitle">{{ p.subtitle }}</span>{% endif -%}
      <span class="cel-meta">{% if p.duration %}{{ p.duration }}{% elsif p.minutes %}約 {{ p.minutes }} 分{% else %}体験コンテンツ{% endif %}</span>
    </a>
        {%- endunless -%}
        {%- endif -%}
      {%- endif -%}
    {%- endfor -%}
  {%- endfor -%}

  {%- comment -%} 第 2 パス：連番を持たないファイルを末尾に描画 {%- endcomment -%}
  {%- for p in pool -%}
    {%- assign ok = false -%}
    {%- if p.extname -%}
      {%- if p.extname == ".md" -%}{%- assign ok = true -%}{%- endif -%}
    {%- else -%}
      {%- assign ok = true -%}
    {%- endif -%}
    {%- if p.name == "index.md" -%}{%- assign ok = false -%}{%- endif -%}
    {%- if p.name == "README.md" -%}{%- assign ok = false -%}{%- endif -%}
    {%- if ok -%}
      {%- assign stem = p.name | replace: ".markdown", "" | replace: ".md", "" | replace: ".html", "" -%}
      {%- assign seg = stem | split: "_" -%}
      {%- assign code = seg | first -%}
      {%- assign cp = code | split: "-" -%}
      {%- assign num = cp | last -%}
      {%- assign chk = num | plus: 0 | prepend: "0" | slice: -2, 2 -%}
      {%- assign numbered = false -%}
      {%- if cp.size > 1 and chk == num -%}{%- assign numbered = true -%}{%- endif -%}
      {%- unless numbered -%}
      {%- assign iskey = false -%}
      {%- if p.key -%}{%- assign iskey = true -%}{%- endif -%}
      {%- assign kstem = stem | prepend: "," | append: "," -%}
      {%- if celkeys contains kstem -%}{%- assign iskey = true -%}{%- endif -%}
      {%- assign namekey = p.name | prepend: "," | append: "," -%}
      {%- unless drawn contains namekey -%}
      {%- assign drawn = drawn | append: p.name | append: "," -%}
    <a class="cel-door {{ g.cls }}{% if iskey %} is-key{% endif %}" href="{{ p.url | default: p.path | relative_url }}">
      <span class="cel-num"><b>+</b><span>DOOR</span></span>
      <span class="cel-title">{{ p.title | default: stem }}</span>
      {%- if p.subtitle %}<span class="cel-subtitle">{{ p.subtitle }}</span>{% endif -%}
      <span class="cel-meta">{% if p.duration %}{{ p.duration }}{% elsif p.minutes %}約 {{ p.minutes }} 分{% else %}体験コンテンツ{% endif %}</span>
    </a>
      {%- endunless -%}
      {%- endunless -%}
    {%- endif -%}
  {%- endfor -%}

  </div>
</section>
  {%- endif -%}
{% endfor %}

{% if celtotal == 0 %}
<p class="cel-meta">扉が 1 つも見つかりませんでした。<code>contents/</code> 配下のフォルダ名が、この index.md の front matter にある <code>groups:</code> の <code>dir:</code> と一致しているかご確認ください。</p>
{% endif %}

---

## はじめての方へ

<div class="cel-start" markdown="1">

1. Copilot Chat を開き、**Work** が選択されていることを確認する（<a href="#00-setup">Setup</a> の扉から）
2. 今日の扉を開き、**TRY — 手順**のプロンプトをそのまま貼り付ける
3. 出てきた答えを鵜呑みにせず、**根拠リンクを 1 つ開いて確認する**
4. 最後の **REFLECT — 振り返り**に、その日のうちに答える

</div>

各ページは「目的 / 所要 / 利用 / 入力 / 成果」→ シナリオ → TRY（手順とプロンプト）→ REFLECT → NEXT の順に並んでいます。
うまくいかなかった依頼にも価値があります。**どう指示を変えれば直るか**まで書き残してください。

---

## プログラム（連続体験）

単発で試すだけでなく、期間を決めて続ける進め方も用意しています。

{% assign progpages = site.pages | where_exp: "p", "p.path contains 'programs/'" %}
<div class="cel-grid">
{%- for pr in page.programs -%}
  {%- assign idxkey = "programs/" | append: pr.dir | append: "/index" -%}
  {%- assign rdkey = "programs/" | append: pr.dir | append: "/README" -%}
  {%- assign turl = "" -%}
  {%- for p in progpages -%}
    {%- if p.path contains idxkey -%}{%- assign turl = p.url -%}{%- endif -%}
  {%- endfor -%}
  {%- if turl == "" -%}
    {%- for p in progpages -%}
      {%- if p.path contains rdkey -%}{%- assign turl = p.url -%}{%- endif -%}
    {%- endfor -%}
  {%- endif -%}
  {%- if turl != "" -%}
  <a class="cel-door {{ pr.cls }}" href="{{ turl | relative_url }}">
    <span class="cel-num"><b>&#9654;</b><span>PROGRAM</span></span>
    <span class="cel-title">{{ pr.label }}</span>
    {%- if pr.lead %}<span class="cel-subtitle">{{ pr.lead }}</span>{% endif -%}
    <span class="cel-meta">{{ pr.meta | default: pr.dir }}</span>
  </a>
  {%- endif -%}
{%- endfor -%}
</div>

---

## 続けるコツ

- **新しい扉は週 3 回**くらいで十分です。残りの日は、気に入ったプロンプトを繰り返し使ってください。
- 効いたプロンプトは保存して、毎営業日使えるようにします。
- 週に 1 回、チームのチャネルに「今週いちばん良かった 1 件」を投稿します。
- 時間短縮は**自分で計測**します。Copilot に見積もらせないでください。

---

## 実施にあたって

- 自分の実データを使います。共有・公開する成果物に機密情報が含まれていないか、必ず確認してください。
- 利用できる機能は、ライセンスとテナント設定によって異なります。
- Excel の体験は、ファイルを OneDrive に保存し AutoSave を有効にする必要があります。
- エージェントの作成・共有は、管理者設定・テナント構成・ライセンスによって可否が異なります。事前に管理者へ確認してください。
- ハンズオンが難しい回は、ファシリテーターのデモを見ながら進めてください。

---

<p class="cel-meta">コンテンツとプログラムの全一覧、追加のルールは <a href="{{ '/README.html' | relative_url }}">リポジトリの README</a> にまとめています。</p>
