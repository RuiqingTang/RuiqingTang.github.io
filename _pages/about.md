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
  /* ================= Sakura liquid-glass redesign =================
     Existing anime palette preserved. hp- prefixed classes are page-local. */

  @font-face { font-family:'M PLUS Rounded 1c'; font-style:normal; font-weight:400; font-display:swap;
    src:url("{{ '/assets/fonts/MPLUSRounded1c-400.woff2' | relative_url }}") format('woff2');
    unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD; }
  @font-face { font-family:'M PLUS Rounded 1c'; font-style:normal; font-weight:700; font-display:swap;
    src:url("{{ '/assets/fonts/MPLUSRounded1c-700.woff2' | relative_url }}") format('woff2');
    unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD; }
  @font-face { font-family:'M PLUS Rounded 1c'; font-style:normal; font-weight:800; font-display:swap;
    src:url("{{ '/assets/fonts/MPLUSRounded1c-800.woff2' | relative_url }}") format('woff2');
    unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD; }

  :root {
    --hp-sakura:#f26d9d;
    --hp-sakura-strong:#e05687;
    --hp-sakura-soft:#ffd3e3;
    --hp-plum:#7d5fbe;
    --hp-ink:#4a3640;
    --hp-motion-spring:cubic-bezier(.16,1.08,.28,1);
    --hp-motion-soft:cubic-bezier(.22,.68,0,1);
    --hp-stage-radius:30px;
  }

  html, body { overflow-x:clip; }
  body {
    background:#fff7fa url("{{ '/images/background_img.jpg' | relative_url }}") center / cover no-repeat fixed;
    font-family:'M PLUS Rounded 1c',-apple-system,BlinkMacSystemFont,'Segoe UI',Roboto,'Helvetica Neue',Arial,sans-serif;
  }
  body::before { content:''; position:fixed; inset:0; z-index:-2; pointer-events:none;
    background:linear-gradient(165deg,rgba(255,251,252,.34),rgba(255,243,249,.62) 58%,rgba(255,234,244,.5)); }
  body::after {
    content:''; position:fixed; inset:0; z-index:-1; pointer-events:none;
    background:
      radial-gradient(34vw 34vw at 12% 18%,rgba(255,166,202,.22),transparent 62%),
      radial-gradient(28vw 28vw at 82% 8%,rgba(197,175,255,.2),transparent 60%),
      radial-gradient(30vw 30vw at 68% 88%,rgba(255,214,227,.26),transparent 64%);
  }

  /* Floating liquid-glass stage behind all content */
  .hp-stage { position:relative; z-index:1; }
  .hp-stage::before {
    content:''; position:absolute; inset:-24px -20px; z-index:-1; border-radius:42px; pointer-events:none;
    background:linear-gradient(135deg,rgba(255,255,255,.28),rgba(255,229,241,.18) 50%,rgba(211,196,255,.2));
    -webkit-backdrop-filter:blur(8px) saturate(1.2); backdrop-filter:blur(8px) saturate(1.2);
    border:1px solid rgba(255,255,255,.44); box-shadow:0 30px 90px rgba(126,54,86,.1);
  }

  /* Masthead: keep theme's fixed bar (body has padding-top:70px from theme),
     only restyle it as a liquid-glass chrome. Full width so nothing overlaps. */
  .masthead {
    background:linear-gradient(180deg,rgba(255,248,251,.82),rgba(255,236,245,.66)) !important;
    -webkit-backdrop-filter:blur(22px) saturate(1.5); backdrop-filter:blur(22px) saturate(1.5);
    border-bottom:1px solid rgba(255,255,255,.6) !important;
    box-shadow:0 14px 34px rgba(126,54,86,.1),inset 0 1px 0 rgba(255,255,255,.9) !important;
  }
  .masthead::after { content:none; }
  .masthead__inner-wrap {
    background:transparent !important;
    border:none !important;
    box-shadow:none !important;
  }
  .masthead div,.masthead nav,.masthead ul,.masthead li,.masthead a,.masthead span { background:transparent !important; }
  .masthead .visible-links a,.masthead .hidden-links a { color:#b04a72 !important; font-weight:700; transition:transform .28s var(--hp-motion-spring),color .24s ease,text-shadow .24s ease; }
  .masthead .visible-links a:hover,.masthead .hidden-links a:hover { color:var(--hp-sakura-strong) !important; text-shadow:0 0 14px rgba(255,158,192,.8); }
  .masthead .masthead__menu-item--lg a { display:inline-block; }

  /* Sidebar: translucent avatar badge, not solid card */
  .sidebar div[itemscope] {
    position:relative; isolation:isolate; overflow:hidden; padding:1.15rem; border-radius:28px;
    background:linear-gradient(150deg,rgba(255,255,255,.5),rgba(255,224,238,.24) 58%,rgba(224,207,255,.22)),rgba(255,255,255,.16) !important;
    border:1px solid rgba(255,255,255,.7); box-shadow:0 22px 52px rgba(126,54,86,.11),inset 0 1px 0 rgba(255,255,255,.88);
    -webkit-backdrop-filter:blur(20px) saturate(1.45); backdrop-filter:blur(20px) saturate(1.45);
    text-shadow:none; transform-style:preserve-3d;
  }
  .sidebar div[itemscope]::before {
    content:''; position:absolute; inset:-1px; z-index:-1; pointer-events:none;
    background:linear-gradient(125deg,transparent 22%,rgba(255,255,255,.34) 47%,transparent 68%); opacity:.5;
  }
  .sidebar .author__avatar img {
    border-radius:24px; box-shadow:0 16px 34px rgba(98,43,67,.18),0 0 0 6px rgba(255,255,255,.38);
    transition:transform .45s var(--hp-motion-spring),box-shadow .35s ease;
  }
  .sidebar div[itemscope]:hover .author__avatar img { transform:translateY(-4px) rotateX(7deg) scale(1.02); box-shadow:0 24px 48px rgba(98,43,67,.2),0 0 0 7px rgba(255,255,255,.46); }
  .hp-side-ico { width:1em; height:1em; fill:currentColor; vertical-align:-.12em; margin-right:.4em; }

  /* Main layout and floating stage; fixed masthead clearance */
  #main { position:relative; z-index:2; perspective:1500px; }
  .page__inner-wrap { perspective:1300px; }
  @media (min-width: 925px) {
    #main { display:flex; align-items:flex-start; gap:2.8rem; }
    #main .sidebar { float:none !important; position:sticky !important; top:84px !important; margin-top:0 !important; width:auto !important;
      max-width:225px !important; flex:0 0 225px; margin:0 !important; padding:0 !important;
      max-height:calc(100vh - 96px); overflow-y:auto; overscroll-behavior:contain; scrollbar-width:thin; }
    #main .sidebar div[itemscope] { width:100%; }
    #main article.page { float:none !important; width:auto !important; margin:0 !important;
      padding:0 !important; flex:1 1 auto; min-width:0; }
    .sidebar,.sidebar p,.sidebar li,.sidebar a { overflow-wrap:anywhere; word-break:break-word; }
  }

  /* Shared liquid-glass material */
  .hp-glass {
    position:relative; isolation:isolate; overflow:hidden; box-sizing:border-box; transform-style:preserve-3d;
    background:
      radial-gradient(120% 75% at var(--hp-glow-x,18%) var(--hp-glow-y,0%),rgba(255,255,255,.5),transparent 46%),
      linear-gradient(152deg,rgba(255,255,255,.46),rgba(255,214,232,.2) 54%,rgba(212,197,255,.18)),
      rgba(255,255,255,.14) !important;
    border:1px solid rgba(255,255,255,.74) !important;
    box-shadow:0 24px 60px rgba(126,54,86,.13),0 6px 18px rgba(224,86,135,.09),inset 0 1px 0 rgba(255,255,255,.9),inset 0 -12px 26px rgba(224,86,135,.06) !important;
    -webkit-backdrop-filter:blur(24px) saturate(1.5); backdrop-filter:blur(24px) saturate(1.5);
    transition:transform .34s var(--hp-motion-spring),box-shadow .28s ease,border-color .28s ease;
  }
  .hp-glass::before {
    content:''; position:absolute; inset:-1px; z-index:-1; pointer-events:none; opacity:.85;
    background:
      radial-gradient(circle at var(--hp-glow-x,18%) var(--hp-glow-y,0%),rgba(255,255,255,.98) 0,rgba(255,255,255,.45) 11%,transparent 33%),
      linear-gradient(122deg,transparent 18%,rgba(255,255,255,.34) 44%,transparent 64%),
      linear-gradient(200deg,transparent 72%,rgba(255,176,208,.14));
  }
  .hp-glass::after {
    content:''; position:absolute; left:8%; right:8%; bottom:-14px; height:22px; z-index:-2; pointer-events:none;
    background:radial-gradient(50% 100% at 50% 0,rgba(126,54,86,.18),transparent 72%); filter:blur(7px);
  }
  .sidebar div[itemscope] { border-radius:28px; }
  .hp-intro,.hp-news li,.hp-exp,.hp-pub { border-radius:26px; }
  .hp-chip,.hp-btn { border-radius:999px; }
  /* Local controls (fallback) keep material even if hp-glass class absent */
  .hp-intro,.hp-news li,.hp-exp,.hp-pub,.hp-chip,.hp-btn {
    position:relative; isolation:isolate; overflow:hidden; transform-style:preserve-3d;
    background:
      radial-gradient(120% 75% at var(--hp-glow-x,18%) var(--hp-glow-y,0%),rgba(255,255,255,.5),transparent 46%),
      linear-gradient(152deg,rgba(255,255,255,.46),rgba(255,214,232,.2) 54%,rgba(212,197,255,.18)),
      rgba(255,255,255,.14) !important;
    border:1px solid rgba(255,255,255,.74) !important;
    box-shadow:0 24px 60px rgba(126,54,86,.13),0 6px 18px rgba(224,86,135,.09),inset 0 1px 0 rgba(255,255,255,.9),inset 0 -12px 26px rgba(224,86,135,.06) !important;
    -webkit-backdrop-filter:blur(24px) saturate(1.5); backdrop-filter:blur(24px) saturate(1.5);
    transition:transform .34s var(--hp-motion-spring),box-shadow .28s ease,border-color .28s ease;
  }
  .hp-intro::before,.hp-news li::before,.hp-exp::before,.hp-pub::before,.hp-chip::before,.hp-btn::before {
    content:''; position:absolute; inset:-1px; z-index:-1; pointer-events:none; opacity:.85;
    background:
      radial-gradient(circle at var(--hp-glow-x,18%) var(--hp-glow-y,0%),rgba(255,255,255,.98) 0,rgba(255,255,255,.45) 11%,transparent 33%),
      linear-gradient(122deg,transparent 18%,rgba(255,255,255,.34) 44%,transparent 64%);
  }

  /* Content styling retained from previous design */
  .hp-intro { font-size:1.07rem; line-height:1.75; margin:0 0 .8rem; padding:1.1rem 1.2rem; color:#57454e; }
  .hp-intro a { color:var(--hp-sakura-strong); }

  .hp-chips { display:flex; flex-wrap:wrap; gap:.55rem; margin:.95rem 0 .5rem; }
  .hp-chip { min-height:38px; display:inline-flex; align-items:center; font-size:.86rem; font-weight:600; padding:.3rem 1rem; color:#d4507f;
    transition:transform .42s var(--hp-motion-spring),box-shadow .32s ease,color .3s ease; }
  .hp-chip:hover { transform:translateY(-5px) scale(1.045); color:#c14570; box-shadow:0 18px 36px rgba(126,54,86,.16),inset 0 1px 0 rgba(255,255,255,.92) !important; }
  .hp-chip:nth-child(3n+2) { color:#8a6fd6; }
  .hp-chip:nth-child(3n+3) { color:#3d9968; }

  .hp-heading { display:flex; align-items:center; gap:.65rem; font-size:1.36rem; font-weight:800; color:var(--hp-ink);
    margin:2.4rem 0 1.2rem; padding-bottom:.55rem; position:relative; text-shadow:0 0 10px rgba(255,255,255,.95); }
  .hp-heading::after { content:''; position:absolute; left:0; bottom:0; width:100%; height:4px; border-radius:4px;
    background:linear-gradient(90deg,#ff9dc2,#ffd3e3 46%,rgba(255,211,227,0)); transform-origin:left center; transform:scaleX(0);
    transition:transform .75s var(--hp-motion-soft); }
  .hp-reveal.is-visible .hp-heading::after, .hp-heading.hp-reveal.is-visible::after,.hp-heading.is-visible::after { transform:scaleX(1); }
  .hp-sakura { width:1.2em; height:1.2em; flex:0 0 auto; transition:transform .5s var(--hp-motion-spring); }
  
  .hp-news { list-style:none; margin:0; padding:0; }
  .hp-news li { display:flex; align-items:baseline; gap:.75rem; margin-bottom:.55rem; padding:.72rem .85rem; }
  .hp-news li:hover { transform:translateY(-3px) translateZ(8px); }
  .hp-news-date { flex:0 0 auto; font-size:.8rem; font-weight:700; color:#d4507f; background:#ffe6ee;
    border-radius:10px; padding:.18rem .65rem; transform:translateZ(18px); box-shadow:0 6px 14px rgba(224,86,135,.14); }
  .hp-news a { color:var(--hp-sakura-strong); }

  .hp-exp,.hp-pub { padding:1.05rem 1.25rem; margin-bottom:1.05rem; will-change:transform; }
  .hp-exp:hover,.hp-pub:hover { border-color:rgba(255,186,212,.95) !important; filter:saturate(1.08); }
  /* Education / Work: compact header row -> logo badge inline with school/company name,
     meta (degree + dates) sits on the next line, indented to align under the name. */
  .hp-exp { display:flex; align-items:center; gap:1.1rem; }
  .hp-exp-logo { flex:0 0 88px; width:88px; height:88px; display:flex; align-items:center; justify-content:center;
    padding:9px; border-radius:20px !important;
    background:rgba(255,255,255,.6) !important; border:1px solid rgba(255,255,255,.85) !important;
    box-shadow:0 10px 22px rgba(111,65,86,.12),inset 0 1px 0 rgba(255,255,255,.94) !important;
    transform:translateZ(30px); transition:transform .34s var(--hp-motion-spring),box-shadow .28s ease; }
  .hp-exp:hover .hp-exp-logo { transform:translateZ(46px) scale(1.04); box-shadow:0 16px 30px rgba(111,65,86,.16),inset 0 1px 0 rgba(255,255,255,.95) !important; }
  .hp-exp-logo img { max-width:100%; max-height:100%; object-fit:contain; }
  .hp-exp-body { flex:1; min-width:0; line-height:1.55; transform:translateZ(14px); }
  .hp-exp-school { font-weight:700; font-size:1.04rem; margin:0 0 .34rem; color:#3f2e36; line-height:1.3; }
  .hp-exp-school a { color:inherit; text-decoration:none; border-bottom:1.5px dashed #ffc3d6; transition:color .25s ease,border-color .25s ease; }
  .hp-exp-school a:hover { color:var(--hp-sakura-strong); border-bottom-color:var(--hp-sakura-strong); }
  .hp-exp-meta { margin:0 0 .22rem; }
  .hp-exp-meta em { color:#8a6a76; }
  .hp-dates { display:inline-block; font-size:.82rem; font-weight:700; color:#7d5fbe; background:#f1ebff;
    padding:.14rem .65rem; border-radius:9px; margin-left:.45rem; box-shadow:0 6px 14px rgba(125,95,190,.12); }
  .hp-exp-major { margin:0; color:#96798a; font-size:.95rem; }
  .hp-pub-logo { transform:translateZ(38px); border-radius:20px !important;
    background:rgba(255,255,255,.56) !important; border:1px solid rgba(255,255,255,.8) !important;
    box-shadow:0 14px 28px rgba(111,65,86,.13),inset 0 1px 0 rgba(255,255,255,.92) !important;
    transition:transform .34s var(--hp-motion-spring),box-shadow .28s ease; }
  .hp-pub:hover .hp-pub-logo { transform:translateZ(58px) scale(1.03); }
  .hp-pub-body { transform:translateZ(16px); }

  .hp-pub { display:flex; align-items:stretch; gap:1.2rem; }
  .hp-pub-logo { flex:0 0 128px; display:flex; align-items:center; justify-content:center; padding:12px; }
  .hp-pub-logo img { max-width:100%; max-height:92px; object-fit:contain; }
  .hp-optica-lockup { display:flex; flex-direction:column; align-items:center; gap:9px; }
  .hp-optica-ring { width:46px; height:46px; flex:0 0 auto; }
  .hp-optica-lockup img { width:98px; height:auto; }
  .hp-pub-body { flex:1; min-width:0; line-height:1.5; }
  .hp-pub-title { font-weight:700; margin:0 0 .5rem; color:#3f2e36; }
  .hp-pub-authors { margin:0 0 .5rem; font-size:.95rem; color:#6d5560; }
  .hp-pub-authors strong { color:var(--hp-sakura-strong); }
  .hp-pub-venue { margin:0 0 .8rem; font-size:.95rem; color:#96798a; display:flex; align-items:center; flex-wrap:wrap; gap:.45rem; }
  .hp-badge { display:inline-block; font-size:.78rem; font-weight:700; letter-spacing:.02em; color:#fff;
    background:var(--hp-c,#ef6d9c); padding:.18rem .7rem; border-radius:9px; box-shadow:0 8px 18px rgba(126,54,86,.16); transform:translateZ(24px); }
  .hp-links { display:flex; gap:.55rem; flex-wrap:wrap; }
  .hp-btn { min-height:44px; display:inline-flex; align-items:center; gap:.45rem; font-size:.86rem; font-weight:700; justify-content:center;
    color:#d4507f !important; padding:.45rem 1.05rem; border-radius:999px !important; touch-action:manipulation;
    transition:transform .42s var(--hp-motion-spring),box-shadow .3s ease,color .28s ease,filter .3s ease; }
  .hp-btn:hover { background:linear-gradient(135deg,rgba(255,143,180,.94),rgba(242,109,157,.94)) !important; color:#fff !important;
    transform:translateY(-4px) scale(1.055); filter:saturate(1.1); box-shadow:0 18px 36px rgba(224,86,135,.25),inset 0 1px 0 rgba(255,255,255,.35) !important; text-decoration:none; }
  .hp-btn:active { transform:translateY(0) scale(.965); transition-duration:.12s; }
  .hp-ico { width:1em; height:1em; fill:currentColor; flex:0 0 auto; }
  .hp-btn:focus-visible,.hp-exp-school a:focus-visible,.hp-news a:focus-visible { outline:3px solid rgba(176,74,114,.75); outline-offset:3px; }
  .hp-contact { display:flex; flex-wrap:wrap; gap:.65rem; margin-top:1.15rem; }

  /* Cursor-reactive depth field: multiple parallax planes + rainbow caustics */
  .hp-depth-field { position:fixed; inset:0; z-index:0; overflow:hidden; pointer-events:none; perspective:1100px; transform-style:preserve-3d; }
  .hp-depth-plane { position:absolute; display:block; border:1px solid rgba(255,255,255,.5); opacity:.65; will-change:transform; }
  .hp-plane-1 { width:34vw; height:52vh; left:-11vw; top:10vh; transform:translate3d(calc(var(--px,0) * 14px),calc(var(--py,0) * 12px),-80px);
    background:linear-gradient(140deg,rgba(255,255,255,.16),rgba(255,174,207,.07) 55%,rgba(197,175,255,.08));
    clip-path:polygon(18% 0,100% 7%,82% 100%,0 88%); }
  .hp-plane-2 { width:36vw; height:38vh; right:-13vw; top:34vh; transform:translate3d(calc(var(--px,0) * -12px),calc(var(--py,0) * 16px),-60px);
    background:linear-gradient(150deg,rgba(255,255,255,.15),rgba(255,196,220,.08) 52%,rgba(255,226,181,.07));
    clip-path:polygon(10% 5%,92% 0,100% 90%,0 100%); }
  @keyframes hp-sheen { 0% { transform:translateX(-100%); } 55%,100% { transform:translateX(100%); } }

  /* Scroll reveal: 3D entrance with natural spring */
  .hp-motion-ready .hp-reveal { opacity:0; transform:translate3d(0,14px,0); }
  .hp-motion-ready .hp-reveal.is-visible { opacity:1; transform:translate3d(0,0,0);
    transition:opacity .28s ease,transform .34s var(--hp-motion-spring); transition-delay:var(--hp-delay,0ms); }
  .hp-motion-ready .hp-reveal.hp-tilting { transition:box-shadow .35s ease,border-color .3s ease,filter .3s ease; }

  #hp-sakura-canvas { position:fixed; inset:0; pointer-events:none; z-index:9999; }

  @supports not ((backdrop-filter:blur(1px)) or (-webkit-backdrop-filter:blur(1px))) {
    .hp-intro,.hp-news li,.hp-exp,.hp-pub,.hp-chip,.hp-btn,.sidebar div[itemscope] { background:rgba(255,249,252,.95) !important; }
  }
  @media (max-width:620px) {
    .hp-pub { flex-direction:column; }
    .hp-pub-logo { flex-basis:auto; width:100%; max-width:210px; height:105px; }
    .hp-exp { gap:.8rem; }
    .hp-exp-logo { flex:0 0 64px; width:64px; height:64px; border-radius:16px !important; }
    .hp-plane-2 { opacity:.25; }
    .hp-exp,.hp-pub,.hp-chip,.hp-btn { transform:none !important; }
  }
  @media (prefers-reduced-transparency:reduce),(prefers-contrast:more) {
    .hp-intro,.hp-news li,.hp-exp,.hp-pub,.hp-chip,.hp-btn,.sidebar div[itemscope] {
      background:rgba(255,250,253,.97) !important; -webkit-backdrop-filter:none; backdrop-filter:none; }
  }
  @media (prefers-reduced-motion:reduce) {
    body::after,.hp-sakura,.sidebar div[itemscope]::before { animation:none !important; }
    .hp-motion-ready .hp-reveal,.hp-motion-ready .hp-reveal.is-visible { opacity:1; transform:none; filter:none; transition:none; }
    .hp-exp,.hp-pub,.hp-chip,.hp-btn,.sidebar div[itemscope] { transform:none !important; transition:none !important; }
  }
</style>


<div class="hp-depth-field" aria-hidden="true">
  <span class="hp-depth-plane hp-plane-1"></span>
  <span class="hp-depth-plane hp-plane-2"></span>
</div>

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
/* Optimized spatial motion: tilt-free. Cursor gives light parallax + glow only. */
(function () {
  var reduce = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var depthField = document.querySelector('.hp-depth-field');
  var stage = document.querySelector('article.page');
  if (stage && !stage.classList.contains('hp-stage')) { stage.classList.add('hp-stage'); }
  if (depthField && depthField.parentNode !== document.body) { document.body.insertBefore(depthField, document.body.firstChild); }
  var canvas = document.getElementById('hp-sakura-canvas');
  if (canvas && canvas.parentNode !== document.body) { document.body.appendChild(canvas); }

  var revealItems = document.querySelectorAll('.hp-heading,.hp-news li,.hp-exp,.hp-pub,.hp-contact');
  for (var i = 0; i < revealItems.length; i++) {
    revealItems[i].classList.add('hp-reveal');
    revealItems[i].style.setProperty('--hp-delay', (i % 4) * 42 + 'ms');
  }
  if (!reduce && 'IntersectionObserver' in window) {
    document.documentElement.classList.add('hp-motion-ready');
    var observer = new IntersectionObserver(function (entries) {
      for (var j = 0; j < entries.length; j++) {
        if (entries[j].isIntersecting) {
          entries[j].target.classList.add('is-visible');
          observer.unobserve(entries[j].target);
        }
      }
    }, { threshold:.01, rootMargin:'0px 0px 12% 0px' });
    for (i = 0; i < revealItems.length; i++) { observer.observe(revealItems[i]); }
  }

  if (reduce || window.matchMedia('(pointer: coarse)').matches || innerWidth < 760) { return; }

  var planesRaf = 0, planes = document.querySelectorAll('.hp-depth-plane');
  var glowEls = document.querySelectorAll('.hp-intro,.hp-news li,.hp-chip,.hp-btn,.sidebar div[itemscope]');

  function planeFrame(event) {
    var nx = (event.clientX / innerWidth - .5), ny = (event.clientY / innerHeight - .5);
    for (var i = 0; i < planes.length; i++) {
      planes[i].style.setProperty('--px', nx.toFixed(3));
      planes[i].style.setProperty('--py', ny.toFixed(3));
    }
    planesRaf = 0;
  }

  window.addEventListener('pointermove', function (event) {
    if (!planesRaf) planesRaf = requestAnimationFrame(function () { planeFrame(event); });
    for (var i = 0; i < glowEls.length; i++) {
      var el = glowEls[i], r = el.getBoundingClientRect();
      if (event.clientX >= r.left && event.clientX <= r.right && event.clientY >= r.top && event.clientY <= r.bottom) {
        el.style.setProperty('--hp-glow-x', (((event.clientX - r.left) / r.width) * 100).toFixed(1) + '%');
        el.style.setProperty('--hp-glow-y', (((event.clientY - r.top) / r.height) * 100).toFixed(1) + '%');
      }
    }
  }, { passive:true });

  document.querySelectorAll('.hp-exp,.hp-pub').forEach(function (card) {
    var raf = 0, lift = 0, targetLift = 0, gx = 18, gy = 0, tgx = 18, tgy = 0, active = false;
    function tick() {
      lift += (targetLift - lift) * .16;
      gx += (tgx - gx) * .18;
      gy += (tgy - gy) * .18;
      card.style.setProperty('--hp-glow-x', gx.toFixed(1) + '%');
      card.style.setProperty('--hp-glow-y', gy.toFixed(1) + '%');
      if (active || Math.abs(targetLift - lift) > .05) {
        card.style.transform = 'perspective(1000px) translate3d(0,' + (-lift).toFixed(2) + 'px,' + (lift * 1.8).toFixed(2) + 'px)';
        raf = requestAnimationFrame(tick);
      } else {
        card.style.transform = active ? card.style.transform : '';
        raf = 0;
      }
    }
    card.addEventListener('pointerenter', function () {
      active = true; targetLift = 9; card.classList.add('hp-tilting');
      if (!raf) raf = requestAnimationFrame(tick);
    }, { passive:true });
    card.addEventListener('pointermove', function (event) {
      var r = card.getBoundingClientRect();
      tgx = ((event.clientX - r.left) / r.width) * 100;
      tgy = ((event.clientY - r.top) / r.height) * 100;
      if (!raf) raf = requestAnimationFrame(tick);
    }, { passive:true });
    card.addEventListener('pointerleave', function () {
      active = false; targetLift = 0; tgx = 18; tgy = 0; card.classList.remove('hp-tilting');
      if (!raf) raf = requestAnimationFrame(tick);
    }, { passive:true });
  });
})();
</script>
<script>
(function () {
  var reduce = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var cv = document.getElementById('hp-sakura-canvas');
  if (!cv || !cv.getContext || reduce) { if (cv) { cv.style.display = 'none'; } return; }
  if (cv.parentNode !== document.body) { document.body.appendChild(cv); }
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
