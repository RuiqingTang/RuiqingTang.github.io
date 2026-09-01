---
permalink: /
title: "About me"
seo_title: "Ruiqing Tang - About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>
  /* ================= Sakura / anime theme =================
     hp- prefixed classes are used only on this page.
     Icons are inline SVG (Font Awesome Free 6.5.2, CC BY 4.0). */

  @font-face { font-family:'M PLUS Rounded 1c'; font-style:normal; font-weight:400; font-display:swap;
    src:url("{{ '/assets/fonts/MPLUSRounded1c-400.woff2' | relative_url }}") format('woff2');
    unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD; }
  @font-face { font-family:'M PLUS Rounded 1c'; font-style:normal; font-weight:700; font-display:swap;
    src:url("{{ '/assets/fonts/MPLUSRounded1c-700.woff2' | relative_url }}") format('woff2');
    unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD; }
  @font-face { font-family:'M PLUS Rounded 1c'; font-style:normal; font-weight:800; font-display:swap;
    src:url("{{ '/assets/fonts/MPLUSRounded1c-800.woff2' | relative_url }}") format('woff2');
    unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD; }

  body {
    background:#fff7fa url("{{ '/images/background_img.jpg' | relative_url }}") center / cover no-repeat fixed;
    font-family:'M PLUS Rounded 1c',-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,'Helvetica Neue',Arial,sans-serif;
  }
  /* soft veil so text stays readable over the wallpaper */
  body::before { content:''; position:fixed; inset:0; z-index:-1; pointer-events:none;
    background:linear-gradient(180deg,rgba(255,251,252,.52) 0%,rgba(255,249,251,.32) 55%,rgba(255,247,250,.46) 100%); }

  /* ===== masthead: frosted sakura glass ===== */
  .masthead { background:rgba(255,243,248,.8) !important;
    -webkit-backdrop-filter:blur(12px) saturate(1.5); backdrop-filter:blur(12px) saturate(1.5);
    border-bottom:1.5px solid rgba(255,197,219,.9) !important; box-shadow:0 1px 12px rgba(233,110,155,.10); }
  .masthead div, .masthead nav, .masthead ul, .masthead li, .masthead a, .masthead span { background:transparent !important; }
  .masthead .hidden-links { background:rgba(255,246,250,.97) !important; border:1.5px solid #ffd3e2; border-radius:10px; }
  .masthead .visible-links a, .masthead .hidden-links a { color:#b04a72 !important; font-weight:700; }
  .masthead .visible-links a:hover, .masthead .hidden-links a:hover { color:#e05687 !important; }
  .navicon, .navicon::before, .navicon::after { background:#b04a72 !important; }

  /* ===== sidebar: blend into the wallpaper, no card box ===== */
  .sidebar div[itemscope] { background:transparent; border:none; box-shadow:none; padding:0;
    text-shadow:0 0 6px #fff, 0 1px 10px rgba(255,255,255,.95); }
  .hp-side-ico { width:1em; height:1em; fill:currentColor; vertical-align:-.12em; margin-right:.4em; }

  /* ===== flex layout: sidebar can never overlap the main column =====
     Replaces the theme's Susy float grid (prone to sub-pixel overflow when
     zooming) with flex columns. Applies at the theme's $large breakpoint. */
  @media (min-width: 925px) {
    #main { display:flex; align-items:flex-start; gap:2.4rem; }
    #main .sidebar { float:none !important; position:static !important; width:auto !important;
      max-width:215px !important; flex:0 0 215px; margin:0 !important; padding:0 !important;
      max-height:none !important; overflow:visible !important; }
    #main .sidebar div[itemscope] { width:100%; }
    #main article.page { float:none !important; width:auto !important; margin:0 !important;
      padding:0 !important; flex:1 1 auto; min-width:0; }
    .sidebar, .sidebar p, .sidebar li, .sidebar a { overflow-wrap:anywhere; word-break:break-word; }
  }

  .hp-intro { font-size:1.06rem; line-height:1.75; margin:0 0 .7rem; color:#57454e;
    background:rgba(255,255,255,.78); border:1.5px solid #ffe3ec; border-radius:16px; padding:.85rem 1.1rem; }
  .hp-intro a { color:#e05687; }

  .hp-chips { display:flex; flex-wrap:wrap; gap:.5rem; margin:.9rem 0 .4rem; }
  .hp-chip { font-size:.85rem; font-weight:500; padding:.28rem .9rem; border-radius:999px;
    background:#fff; border:1.5px solid #ffd3e1; color:#d4507f; box-shadow:0 1px 5px rgba(233,110,155,.10); }
  .hp-chip:nth-child(3n+2) { border-color:#e2d8ff; color:#8a6fd6; background:#fbfaff; }
  .hp-chip:nth-child(3n+3) { border-color:#c9ecd9; color:#3d9968; background:#f7fdfa; }

  .hp-heading { display:flex; align-items:center; gap:.6rem; font-size:1.35rem; font-weight:800;
    color:#4a3640; margin:2.3rem 0 1.15rem; padding-bottom:.5rem; position:relative;
    text-shadow:0 0 6px #fff, 0 1px 10px rgba(255,255,255,.9), 0 0 18px rgba(255,255,255,.8); }
  .hp-heading::after { content:''; position:absolute; left:0; bottom:0; width:100%; height:3px; border-radius:3px;
    background:linear-gradient(90deg,#ff9dc2,#ffd3e3 45%,rgba(255,211,227,0)); }
  .hp-sakura { width:1.15em; height:1.15em; flex:0 0 auto; animation:hp-spin 16s linear infinite; }
  @keyframes hp-spin { to { transform:rotate(360deg); } }

  .hp-news { list-style:none; margin:0; padding:0; }
  .hp-news li { display:flex; align-items:baseline; gap:.75rem; margin-bottom:.45rem;
    background:rgba(255,255,255,.75); border:1.5px solid #ffe3ec; border-radius:12px; padding:.42rem .7rem; }
  .hp-news-date { flex:0 0 auto; font-size:.8rem; font-weight:700; color:#d4507f;
    background:#ffe6ee; border-radius:8px; padding:.14rem .6rem; }
  .hp-news a { color:#e05687; }

  .hp-exp { display:flex; align-items:center; gap:1.1rem; background:rgba(255,255,255,.93);
    border:1.5px solid #ffdde8; border-radius:16px; padding:1rem 1.2rem; margin-bottom:1rem;
    box-shadow:0 2px 10px rgba(233,110,155,.06); transition:all .22s ease; }
  .hp-exp:hover { transform:translateY(-2px); border-color:#ffb1cc; box-shadow:0 6px 20px rgba(233,110,155,.14); }
  .hp-exp-logo { flex:0 0 86px; width:86px; height:86px; background:linear-gradient(135deg,#fff,#fff5f8);
    border:1.5px solid #ffe0ea; border-radius:12px; display:flex; align-items:center; justify-content:center;
    padding:8px; box-sizing:border-box; }
  .hp-exp-logo img { max-width:100%; max-height:100%; object-fit:contain; }
  .hp-exp-body { flex:1; min-width:0; line-height:1.55; }
  .hp-exp-school { font-weight:700; font-size:1.03rem; margin:0 0 .28rem; color:#3f2e36; }
  .hp-exp-school a { color:inherit; text-decoration:none; border-bottom:1.5px dashed #ffc3d6; }
  .hp-exp-school a:hover { color:#e05687; border-bottom-color:#e05687; }
  .hp-exp-meta { margin:0 0 .25rem; }
  .hp-exp-meta em { color:#8a6a76; }
  .hp-dates { display:inline-block; font-size:.82rem; font-weight:700; color:#7d5fbe;
    background:#f1ebff; padding:.12rem .6rem; border-radius:8px; margin-left:.45rem; }
  .hp-exp-major { margin:0; color:#96798a; font-size:.95rem; }

  .hp-pub { display:flex; align-items:stretch; gap:1.2rem; background:rgba(255,255,255,.93);
    border:1.5px solid #ffdde8; border-radius:16px; padding:1.15rem 1.25rem; margin-bottom:1.1rem;
    box-shadow:0 2px 10px rgba(233,110,155,.06); transition:all .22s ease; }
  .hp-pub:hover { transform:translateY(-2px); border-color:#ffb1cc; box-shadow:0 6px 20px rgba(233,110,155,.14); }
  .hp-pub-logo { flex:0 0 128px; background:linear-gradient(135deg,#fff,#fff5f8);
    border:1.5px solid #ffe0ea; border-radius:12px; display:flex; align-items:center; justify-content:center;
    padding:12px; box-sizing:border-box; }
  .hp-pub-logo img { max-width:100%; max-height:92px; object-fit:contain; }
  .hp-optica-lockup { display:flex; flex-direction:column; align-items:center; gap:9px; }
  .hp-optica-ring { width:46px; height:46px; flex:0 0 auto; }
  .hp-optica-lockup img { width:98px; height:auto; }
  .hp-pub-body { flex:1; min-width:0; line-height:1.5; }
  .hp-pub-title { font-weight:700; margin:0 0 .45rem; color:#3f2e36; }
  .hp-pub-authors { margin:0 0 .45rem; font-size:.95rem; color:#6d5560; }
  .hp-pub-authors strong { color:#e05687; }
  .hp-pub-venue { margin:0 0 .75rem; font-size:.95rem; color:#96798a; display:flex; align-items:center; flex-wrap:wrap; gap:.45rem; }
  .hp-badge { display:inline-block; font-size:.78rem; font-weight:700; letter-spacing:.02em; color:#fff;
    background:var(--hp-c,#ef6d9c); padding:.16rem .65rem; border-radius:8px; }
  .hp-links { display:flex; gap:.5rem; flex-wrap:wrap; }
  .hp-btn { display:inline-flex; align-items:center; gap:.45rem; font-size:.85rem; font-weight:700;
    color:#d4507f !important; background:#fff; border:1.5px solid #ffb9ce; padding:.26rem .95rem;
    border-radius:999px; transition:all .18s ease; }
  .hp-btn:hover { background:linear-gradient(135deg,#ff8fb4,#f26d9d); color:#fff !important;
    border-color:transparent; transform:translateY(-1px); box-shadow:0 4px 12px rgba(233,110,155,.28); text-decoration:none; }
  .hp-ico { width:1em; height:1em; fill:currentColor; flex:0 0 auto; }

  .hp-contact { display:flex; flex-wrap:wrap; gap:.6rem; margin-top:1.1rem; }

  #hp-sakura-canvas { position:fixed; inset:0; pointer-events:none; z-index:9999; }

  @media (max-width:620px) {
    .hp-pub { flex-direction:column; }
    .hp-pub-logo { flex-basis:auto; width:100%; max-width:200px; height:100px; }
  }
  @media (prefers-reduced-motion:reduce) { .hp-sakura { animation:none; } }
</style>

<p class="hp-intro">I am an algorithm engineer at <a href="https://www.yuanjingos.com/">YuanJing</a>. I received my master's degree in Communication Engineering from the <a href="https://www.ustb.edu.cn/">University of Science and Technology, Beijing</a>, in 2026. My research interests focus on 3D AIGC, spatial intelligence, and AI agents.</p>

<div class="hp-chips">
  <span class="hp-chip">3D AIGC</span>
  <span class="hp-chip">Spatial Intelligence</span>
  <span class="hp-chip">AI Agent</span>
  <span class="hp-chip">Digital Human</span>
</div>

<h2 class="hp-heading"><svg class="hp-sakura" viewBox="0 0 24 24" aria-hidden="true"><g fill="#ff9dc2"><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(72 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(144 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(216 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(288 12 12)"/></g><circle cx="12" cy="12" r="1.6" fill="#ffd66b"/></svg>News</h2>
<ul class="hp-news">
  <li><span class="hp-news-date">2026.08</span><span>One paper accepted to <a href="https://doi.org/10.1016/j.yofte.2026.104780">Optical Fiber Technology</a>.</span></li>
  <li><span class="hp-news-date">2026.08</span><span>One paper accepted to <a href="https://doi.org/10.1364/OE.610520">Optics Express</a>.</span></li>
  <li><span class="hp-news-date">2026.08</span><span>One paper accepted to <a href="https://doi.org/10.1109/JSEN.2026.3709836">IEEE Sensors Journal</a>.</span></li>
  <li><span class="hp-news-date">2026.03</span><span>One paper accepted to <a href="https://doi.org/10.1109/TIM.2026.3682837">IEEE Transactions on Instrumentation and Measurement</a>.</span></li>
  <li><span class="hp-news-date">2025.09</span><span>One paper accepted to <a href="https://doi.org/10.1016/j.measurement.2025.118927">Measurement</a>.</span></li>
</ul>

<h2 class="hp-heading"><svg class="hp-sakura" viewBox="0 0 24 24" aria-hidden="true"><g fill="#ff9dc2"><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(72 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(144 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(216 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(288 12 12)"/></g><circle cx="12" cy="12" r="1.6" fill="#ffd66b"/></svg>Education Experience</h2>
<div class="hp-exp">
  <div class="hp-exp-logo"><img src="{{ '/images/ustb1.png' | relative_url }}" alt="USTB Logo" loading="lazy"></div>
  <div class="hp-exp-body">
    <p class="hp-exp-school">University of Science and Technology, Beijing (USTB)</p>
    <p class="hp-exp-meta"><em>Master's Degree</em><span class="hp-dates">2023 – 2026</span></p>
    <p class="hp-exp-major">Major: Communication Engineering</p>
  </div>
</div>

<div class="hp-exp">
  <div class="hp-exp-logo"><img src="{{ '/images/ustb1.png' | relative_url }}" alt="USTB Logo" loading="lazy"></div>
  <div class="hp-exp-body">
    <p class="hp-exp-school">University of Science and Technology, Beijing (USTB)</p>
    <p class="hp-exp-meta"><em>Bachelor's Degree</em><span class="hp-dates">2019 – 2023</span></p>
    <p class="hp-exp-major">Major: Communication Engineering</p>
  </div>
</div>

<h2 class="hp-heading"><svg class="hp-sakura" viewBox="0 0 24 24" aria-hidden="true"><g fill="#ff9dc2"><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(72 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(144 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(216 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(288 12 12)"/></g><circle cx="12" cy="12" r="1.6" fill="#ffd66b"/></svg>Work Experience</h2>
<div class="hp-exp">
  <div class="hp-exp-logo"><img src="{{ '/images/yj.png' | relative_url }}" alt="YuanJing Logo" loading="lazy"></div>
  <div class="hp-exp-body">
    <p class="hp-exp-school"><a href="https://www.yuanjingos.com/">YuanJing, Alibaba Group</a>, Shanghai, China</p>
    <p class="hp-exp-meta"><em>3D AIGC Algorithm Engineer</em><span class="hp-dates">2026.07 – present</span></p>
  </div>
</div>

<div class="hp-exp">
  <div class="hp-exp-logo"><img src="{{ '/images/yj.png' | relative_url }}" alt="YuanJing Logo" loading="lazy"></div>
  <div class="hp-exp-body">
    <p class="hp-exp-school"><a href="https://www.yuanjingos.com/">YuanJing, Alibaba Group</a>, Beijing, China</p>
    <p class="hp-exp-meta"><em>3D AIGC Internship</em><span class="hp-dates">2026.03 – 2026.06</span></p>
  </div>
</div>

<div class="hp-exp">
  <div class="hp-exp-logo"><img src="{{ '/images/yaww.png' | relative_url }}" alt="AiShiWeiLai Logo" loading="lazy"></div>
  <div class="hp-exp-body">
    <p class="hp-exp-school"><a href="https://www.aitutor100.com/">AiShiWeiLai AI Research</a>, Beijing, China</p>
    <p class="hp-exp-meta"><em>Digital Human Internship</em><span class="hp-dates">2025.07 – 2025.12</span></p>
  </div>
</div>

<div class="hp-exp">
  <div class="hp-exp-logo"><img src="{{ '/images/cubevi.png' | relative_url }}" alt="CubeVI Logo" loading="lazy"></div>
  <div class="hp-exp-body">
    <p class="hp-exp-school"><a href="https://www.openstageai.com/">Cube Vision Intelligence, CubeVi</a>, Beijing, China</p>
    <p class="hp-exp-meta"><em>AIGC Internship</em><span class="hp-dates">2024.05 – 2025.06</span></p>
  </div>
</div>

<h2 class="hp-heading"><svg class="hp-sakura" viewBox="0 0 24 24" aria-hidden="true"><g fill="#ff9dc2"><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(72 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(144 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(216 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(288 12 12)"/></g><circle cx="12" cy="12" r="1.6" fill="#ffd66b"/></svg>Publications</h2>

<div class="hp-pub">
  <a class="hp-pub-logo" href="https://doi.org/10.1016/j.yofte.2026.104780"><img src="{{ '/images/elsevier.png' | relative_url }}" alt="Elsevier logo" loading="lazy"></a>
  <div class="hp-pub-body">
    <p class="hp-pub-title">Automatic hydraulic fracture hit events recognition with low-frequency DAS data based on object detection</p>
    <p class="hp-pub-authors">M. K. Shuvo, X. Huang, F. Liu, G. Zhu, <strong>R. Tang</strong>, K. Zhang, and X. Zhou</p>
    <p class="hp-pub-venue"><span class="hp-badge" style="--hp-c:#ff6c00;">Optical Fiber Technology</span><span>vol. 103, Art. no. 104780, 2026</span></p>
    <div class="hp-links"><a class="hp-btn" href="https://doi.org/10.1016/j.yofte.2026.104780"><svg class="hp-ico" viewBox="0 0 384 512" aria-hidden="true"><path d="M64 0C28.7 0 0 28.7 0 64V448c0 35.3 28.7 64 64 64H320c35.3 0 64-28.7 64-64V160H256c-17.7 0-32-14.3-32-32V0H64zM256 0V128H384L256 0zM112 256H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>Paper</a></div>
  </div>
</div>

<div class="hp-pub">
  <a class="hp-pub-logo" href="https://doi.org/10.1364/OE.610520">
    <span class="hp-optica-lockup">
      <svg class="hp-optica-ring" viewBox="0 0 512 512" aria-hidden="true"><circle cx="256" cy="256" r="256" fill="#0d0d10"/><path d="M 142.8 225.7 A 117.2 117.2 0 1 1 142.8 286.3" fill="none" stroke="#ffffff" stroke-width="32"/></svg>
      <img src="{{ '/images/optica-wordmark.png' | relative_url }}" alt="Optica" loading="lazy">
    </span>
  </a>
  <div class="hp-pub-body">
    <p class="hp-pub-title">High-precision DAS vibration event recognition via a coupled wavelet transform-CNN framework</p>
    <p class="hp-pub-authors">Huayang Lv, <strong>Ruiqing Tang</strong>, Tong Zhou, Yi Shi, Fei Liu, Xin Huang, Guo Zhu, Isaack Kamanga, Xian Zhou</p>
    <p class="hp-pub-venue"><span class="hp-badge" style="--hp-c:#6f42a8;">Optics Express</span><span>vol. 34, no. 17, pp. 32662–32676, 2026</span></p>
    <div class="hp-links"><a class="hp-btn" href="https://doi.org/10.1364/OE.610520"><svg class="hp-ico" viewBox="0 0 384 512" aria-hidden="true"><path d="M64 0C28.7 0 0 28.7 0 64V448c0 35.3 28.7 64 64 64H320c35.3 0 64-28.7 64-64V160H256c-17.7 0-32-14.3-32-32V0H64zM256 0V128H384L256 0zM112 256H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>Paper</a></div>
  </div>
</div>

<div class="hp-pub">
  <a class="hp-pub-logo" href="https://doi.org/10.1109/JSEN.2026.3709836"><img src="{{ '/images/ieee.png' | relative_url }}" alt="IEEE logo" loading="lazy"></a>
  <div class="hp-pub-body">
    <p class="hp-pub-title">Toward Open-Set Fault Diagnosis for Belt Conveyors Using Distributed Acoustic Sensing</p>
    <p class="hp-pub-authors">Huayang Lv, Fei Liu, <strong>Ruiqing Tang</strong>, Isaack Kamanga, Guo Zhu, Yunshen Chen, Aokang Zhang, Xu Yang, Xian Zhou</p>
    <p class="hp-pub-venue"><span class="hp-badge" style="--hp-c:#00629b;">IEEE Sensors Journal</span><span>vol. 26, no. 16, pp. 23956–23969, 2026</span></p>
    <div class="hp-links"><a class="hp-btn" href="https://doi.org/10.1109/JSEN.2026.3709836"><svg class="hp-ico" viewBox="0 0 384 512" aria-hidden="true"><path d="M64 0C28.7 0 0 28.7 0 64V448c0 35.3 28.7 64 64 64H320c35.3 0 64-28.7 64-64V160H256c-17.7 0-32-14.3-32-32V0H64zM256 0V128H384L256 0zM112 256H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>Paper</a></div>
  </div>
</div>

<div class="hp-pub">
  <a class="hp-pub-logo" href="https://doi.org/10.1109/TIM.2026.3682837"><img src="{{ '/images/ieee.png' | relative_url }}" alt="IEEE logo" loading="lazy"></a>
  <div class="hp-pub-body">
    <p class="hp-pub-title">A Lightweight Neural Network for Pipeline Flow Rate Measurement Using Distributed Acoustic Sensing</p>
    <p class="hp-pub-authors"><strong>Ruiqing Tang</strong>, Yi Shi, Fei Liu, Xin Huang, Isaack Kamanga, Huayang Lv, Tong Zhou, Guozhen Tan, Guo Zhu, Hao Zeng, Yuanyuan Li, Xian Zhou</p>
    <p class="hp-pub-venue"><span class="hp-badge" style="--hp-c:#00629b;">IEEE TIM</span><span>vol. 75, pp. 1–13, 2026</span></p>
    <div class="hp-links"><a class="hp-btn" href="https://doi.org/10.1109/TIM.2026.3682837"><svg class="hp-ico" viewBox="0 0 384 512" aria-hidden="true"><path d="M64 0C28.7 0 0 28.7 0 64V448c0 35.3 28.7 64 64 64H320c35.3 0 64-28.7 64-64V160H256c-17.7 0-32-14.3-32-32V0H64zM256 0V128H384L256 0zM112 256H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>Paper</a></div>
  </div>
</div>

<div class="hp-pub">
  <a class="hp-pub-logo" href="https://doi.org/10.1016/j.measurement.2025.118927"><img src="{{ '/images/elsevier.png' | relative_url }}" alt="Elsevier logo" loading="lazy"></a>
  <div class="hp-pub-body">
    <p class="hp-pub-title">Performance enhancement of Φ-OTDR event classification via dynamic MFCCs and multi-scale discriminator-based FastGAN data augmentation</p>
    <p class="hp-pub-authors">Isaack Kamanga, <strong>Ruiqing Tang</strong>, Zhi Wang, Guo Zhu, Fei Liu, Xian Zhou</p>
    <p class="hp-pub-venue"><span class="hp-badge" style="--hp-c:#ff6c00;">Measurement</span><span>vol. 257, Art. no. 118927, 2026</span></p>
    <div class="hp-links"><a class="hp-btn" href="https://doi.org/10.1016/j.measurement.2025.118927"><svg class="hp-ico" viewBox="0 0 384 512" aria-hidden="true"><path d="M64 0C28.7 0 0 28.7 0 64V448c0 35.3 28.7 64 64 64H320c35.3 0 64-28.7 64-64V160H256c-17.7 0-32-14.3-32-32V0H64zM256 0V128H384L256 0zM112 256H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16zm0 64H272c8.8 0 16 7.2 16 16s-7.2 16-16 16H112c-8.8 0-16-7.2-16-16s7.2-16 16-16z"/></svg>Paper</a></div>
  </div>
</div>

<h2 class="hp-heading"><svg class="hp-sakura" viewBox="0 0 24 24" aria-hidden="true"><g fill="#ff9dc2"><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(72 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(144 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(216 12 12)"/><path d="M12 2.4c1.7 0 2.9 2.3 2.4 4.6-.4 1.7-1.3 2.9-2.4 2.9s-2-1.2-2.4-2.9C9 4.7 10.3 2.4 12 2.4z" transform="rotate(288 12 12)"/></g><circle cx="12" cy="12" r="1.6" fill="#ffd66b"/></svg>Contact</h2>
<div class="hp-contact">
  <a class="hp-btn" href="{{ '/assets/RuiqingTang_Eng.pdf' | relative_url }}"><svg class="hp-ico" viewBox="0 0 512 512" aria-hidden="true"><path d="M0 64C0 28.7 28.7 0 64 0L224 0l0 128c0 17.7 14.3 32 32 32l128 0 0 144-208 0c-35.3 0-64 28.7-64 64l0 144-48 0c-35.3 0-64-28.7-64-64L0 64zm384 64l-128 0L256 0 384 128zM176 352l32 0c30.9 0 56 25.1 56 56s-25.1 56-56 56l-16 0 0 32c0 8.8-7.2 16-16 16s-16-7.2-16-16l0-48 0-80c0-8.8 7.2-16 16-16zm32 80c13.3 0 24-10.7 24-24s-10.7-24-24-24l-16 0 0 48 16 0zm96-80l32 0c26.5 0 48 21.5 48 48l0 64c0 26.5-21.5 48-48 48l-32 0c-8.8 0-16-7.2-16-16l0-128c0-8.8 7.2-16 16-16zm32 128c8.8 0 16-7.2 16-16l0-64c0-8.8-7.2-16-16-16l-16 0 0 96 16 0zm80-112c0-8.8 7.2-16 16-16l48 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-32 0 0 32 32 0c8.8 0 16 7.2 16 16s-7.2 16-16 16l-32 0 0 48c0 8.8-7.2 16-16 16s-16-7.2-16-16l0-64 0-64z"/></svg>Curriculum Vitae</a>
  <a class="hp-btn" href="mailto:tangruiqing123@gmail.com"><svg class="hp-ico" viewBox="0 0 512 512" aria-hidden="true"><path d="M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z"/></svg>Email</a>
  <a class="hp-btn" href="https://github.com/RuiqingTang"><svg class="hp-ico" viewBox="0 0 496 512" aria-hidden="true"><path d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z"/></svg>GitHub</a>
  <a class="hp-btn" href="{{ '/images/wechat.png' | relative_url }}"><svg class="hp-ico" viewBox="0 0 576 512" aria-hidden="true"><path d="M385.2 167.6c6.4 0 12.6.3 18.8 1.1C387.4 90.3 303.3 32 207.7 32 100.5 32 13 104.8 13 197.4c0 53.4 29.3 97.5 77.9 131.6l-19.3 58.6 68-34.1c24.4 4.8 43.8 9.7 68.2 9.7 6.2 0 12.1-.3 18.3-.8-4-12.9-6.2-26.6-6.2-40.8-.1-84.9 72.9-154 165.3-154zm-104.5-52.9c14.5 0 24.2 9.7 24.2 24.4 0 14.5-9.7 24.2-24.2 24.2-14.8 0-29.3-9.7-29.3-24.2.1-14.7 14.6-24.4 29.3-24.4zm-136.4 48.6c-14.5 0-29.3-9.7-29.3-24.2 0-14.8 14.8-24.4 29.3-24.4 14.8 0 24.4 9.7 24.4 24.4 0 14.6-9.6 24.2-24.4 24.2zM563 319.4c0-77.9-77.9-141.3-165.4-141.3-92.7 0-165.4 63.4-165.4 141.3S305 460.7 397.6 460.7c19.3 0 38.9-5.1 58.6-9.9l53.4 29.3-14.8-48.6C534 402.1 563 363.2 563 319.4zm-219.1-24.5c-9.7 0-19.3-9.7-19.3-19.6 0-9.7 9.7-19.3 19.3-19.3 14.8 0 24.4 9.7 24.4 19.3 0 10-9.7 19.6-24.4 19.6zm107.1 0c-9.7 0-19.3-9.7-19.3-19.6 0-9.7 9.7-19.3 19.3-19.3 14.5 0 24.4 9.7 24.4 19.3.1 10-9.9 19.6-24.4 19.6z"/></svg>WeChat</a>
</div>

<canvas id="hp-sakura-canvas" aria-hidden="true"></canvas>
<script>
(function () {
  var reduce = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var cv = document.getElementById('hp-sakura-canvas');
  if (!cv || !cv.getContext || reduce) { if (cv) { cv.style.display = 'none'; } return; }
  var ctx = cv.getContext('2d'), W, H, petals = [], trail = [], ripples = [];
  var COLORS = ['#ffb7cd', '#ffc9da', '#ffe0ea', '#ffffff'];
  var TAU = Math.PI * 2;
  function rnd(a, b) { return a + Math.random() * (b - a); }

  /* ---- ambient falling petals ---- */
  function Petal(init) { this.reset(init); }
  Petal.prototype.reset = function (init) {
    this.x = rnd(0, W); this.y = init ? rnd(-H, H) : rnd(-50, -10);
    this.s = rnd(4, 9); this.vy = rnd(.4, 1.1);
    this.rot = rnd(0, TAU); this.vr = rnd(-.02, .02);
    this.phase = rnd(0, TAU);
    this.c = COLORS[Math.floor(Math.random() * COLORS.length)];
    this.o = rnd(.45, .8);
  };
  Petal.prototype.step = function () {
    this.y += this.vy; this.x += Math.sin(this.phase + this.y * .012) * .7; this.rot += this.vr;
    if (this.y > H + 16) { this.reset(false); }
  };
  Petal.prototype.draw = function () {
    ctx.save(); ctx.translate(this.x, this.y); ctx.rotate(this.rot);
    ctx.globalAlpha = this.o; ctx.fillStyle = this.c;
    ctx.beginPath(); ctx.moveTo(0, -this.s);
    ctx.bezierCurveTo(this.s * .95, -this.s * .45, this.s * .75, this.s * .62, 0, this.s);
    ctx.bezierCurveTo(-this.s * .75, this.s * .62, -this.s * .95, -this.s * .45, 0, -this.s);
    ctx.fill(); ctx.restore();
  };

  /* ---- cursor trail: mini petals + star sparkles ---- */
  function Spark(x, y, burst) {
    this.x = x + rnd(-4, 4); this.y = y + rnd(-4, 4);
    if (burst) {
      var a = rnd(0, TAU), sp = rnd(1, 2.6);
      this.vx = Math.cos(a) * sp; this.vy = Math.sin(a) * sp - .6;
    } else {
      this.vx = rnd(-.7, .7); this.vy = rnd(-1.1, -.2);
    }
    this.s = rnd(2.5, 5.5); this.rot = rnd(0, TAU); this.vr = rnd(-.1, .1);
    this.life = 1; this.decay = rnd(.012, .024);
    this.star = !burst && Math.random() < .3;
    this.c = COLORS[Math.floor(Math.random() * (COLORS.length - 1))];
  }
  Spark.prototype.step = function () {
    this.x += this.vx; this.y += this.vy; this.vy += .028;
    this.rot += this.vr; this.life -= this.decay;
    return this.life > 0;
  };
  Spark.prototype.draw = function () {
    ctx.save(); ctx.translate(this.x, this.y); ctx.rotate(this.rot);
    ctx.globalAlpha = Math.max(this.life, 0);
    if (this.star) {
      ctx.strokeStyle = '#ff9dc2'; ctx.lineWidth = 1.2; ctx.lineCap = 'round';
      ctx.beginPath();
      ctx.moveTo(0, -this.s * 1.8); ctx.lineTo(0, this.s * 1.8);
      ctx.moveTo(-this.s * 1.8, 0); ctx.lineTo(this.s * 1.8, 0);
      ctx.stroke();
    } else {
      ctx.fillStyle = this.c;
      ctx.beginPath(); ctx.moveTo(0, -this.s);
      ctx.bezierCurveTo(this.s * .95, -this.s * .45, this.s * .75, this.s * .62, 0, this.s);
      ctx.bezierCurveTo(-this.s * .75, this.s * .62, -this.s * .95, -this.s * .45, 0, -this.s);
      ctx.fill();
    }
    ctx.restore();
  };

  /* ---- click ripples ---- */
  function Ripple(x, y, delay) { this.x = x; this.y = y; this.r = 4; this.delay = delay || 0; }
  Ripple.prototype.step = function () {
    if (this.delay > 0) { this.delay--; return true; }
    this.r += 2.6; return this.r < 64;
  };
  Ripple.prototype.draw = function () {
    if (this.delay > 0) return;
    ctx.save();
    ctx.globalAlpha = Math.max(0, .55 - this.r / 110);
    ctx.strokeStyle = '#f26d9d'; ctx.lineWidth = 2;
    ctx.beginPath(); ctx.arc(this.x, this.y, this.r, 0, TAU); ctx.stroke();
    ctx.restore();
  };

  function spawnTrail(x, y) { if (trail.length < 130) { trail.push(new Spark(x, y, false)); } }
  function spawnRipple(x, y) {
    ripples.push(new Ripple(x, y, 0), new Ripple(x, y, 10));
    if (trail.length < 130) { for (var i = 0; i < 6; i++) { trail.push(new Spark(x, y, true)); } }
  }
  var lastX = -1, lastY = -1;
  function onMove(x, y) {
    if (lastX < 0) { lastX = x; lastY = y; return; }
    var dx = x - lastX, dy = y - lastY;
    if (dx * dx + dy * dy > 784) { lastX = x; lastY = y; spawnTrail(x, y); }
  }
  window.addEventListener('mousemove', function (e) { onMove(e.clientX, e.clientY); }, { passive: true });
  window.addEventListener('touchmove', function (e) { var t = e.touches[0]; if (t) { onMove(t.clientX, t.clientY); } }, { passive: true });
  window.addEventListener('click', function (e) { spawnRipple(e.clientX, e.clientY); }, { passive: true });
  window.addEventListener('touchstart', function (e) { var t = e.touches[0]; if (t) { spawnRipple(t.clientX, t.clientY); } }, { passive: true });

  function init() {
    W = cv.width = window.innerWidth; H = cv.height = window.innerHeight;
    petals = [];
    var n = Math.max(8, Math.min(20, Math.floor(W / 80)));
    for (var i = 0; i < n; i++) { petals.push(new Petal(true)); }
  }
  function tick() {
    ctx.clearRect(0, 0, W, H);
    var i;
    for (i = ripples.length - 1; i >= 0; i--) { if (!ripples[i].step()) { ripples.splice(i, 1); } }
    for (i = 0; i < ripples.length; i++) { ripples[i].draw(); }
    for (i = 0; i < petals.length; i++) { petals[i].step(); petals[i].draw(); }
    for (i = trail.length - 1; i >= 0; i--) { if (!trail[i].step()) { trail.splice(i, 1); } }
    for (i = 0; i < trail.length; i++) { trail[i].draw(); }
    requestAnimationFrame(tick);
  }
  window.addEventListener('resize', init);
  init(); tick();
})();
</script>

<script>
/* Replace sidebar font icons with inline SVGs (font files can fail to load) */
(function () {
  var map = {
    'fa-location-dot':     { vb: '0 0 384 512', d: 'M215.7 499.2C267 435 384 279.4 384 192C384 86 298 0 192 0S0 86 0 192c0 87.4 117 243 168.3 307.2c12.3 15.3 35.1 15.3 47.4 0zM192 128a64 64 0 1 1 0 128 64 64 0 1 1 0-128z' },
    'fa-building-columns': { vb: '0 0 512 512', d: 'M243.4 2.6l-224 96c-14 6-21.8 21-18.7 35.8S16.8 160 32 160v8c0 13.3 10.7 24 24 24H456c13.3 0 24-10.7 24-24v-8c15.2 0 28.3-10.7 31.3-25.6s-4.8-29.9-18.7-35.8l-224-96c-8-3.4-17.2-3.4-25.2 0zM128 224H64V420.3c-.6 .3-1.2 .7-1.8 1.1l-48 32c-11.7 7.8-17 22.4-12.9 35.9S17.9 512 32 512H480c14.1 0 26.5-9.2 30.6-22.7s-1.1-28.1-12.9-35.9l-48-32c-.6-.4-1.2-.7-1.8-1.1V224H384V416H344V224H280V416H232V224H168V416H128V224zM256 64a32 32 0 1 1 0 64 32 32 0 1 1 0-64z' },
    'fa-envelope':         { vb: '0 0 512 512', d: 'M48 64C21.5 64 0 85.5 0 112c0 15.1 7.1 29.3 19.2 38.4L236.8 313.6c11.4 8.5 27 8.5 38.4 0L492.8 150.4c12.1-9.1 19.2-23.3 19.2-38.4c0-26.5-21.5-48-48-48H48zM0 176V384c0 35.3 28.7 64 64 64H448c35.3 0 64-28.7 64-64V176L294.4 339.2c-22.8 17.1-54 17.1-76.8 0L0 176z' },
    'fa-github':           { vb: '0 0 496 512', d: 'M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z' }
  };
  var icons = document.querySelectorAll('.sidebar i[class*="fa-"]');
  for (var i = 0; i < icons.length; i++) {
    var el = icons[i], key = null, cls = el.classList;
    for (var j = 0; j < cls.length; j++) { if (map[cls[j]]) { key = cls[j]; break; } }
    if (!key) { continue; }
    var NS = 'http://www.w3.org/2000/svg';
    var svg = document.createElementNS(NS, 'svg');
    svg.setAttribute('viewBox', map[key].vb);
    svg.setAttribute('class', 'hp-side-ico');
    svg.setAttribute('aria-hidden', 'true');
    var path = document.createElementNS(NS, 'path');
    path.setAttribute('fill', 'currentColor');
    path.setAttribute('d', map[key].d);
    svg.appendChild(path);
    el.replaceWith(svg);
  }
})();
</script>
