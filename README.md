<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PrintCraft — Customization, Merchandise &amp; Branded Experience Company</title>
<meta name="description" content="PrintCraft designs, sources and delivers customized merchandise, branded experiences and on-ground activation across corporate, personal and creator use cases in India.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Space+Grotesk:wght@500;600;700&family=Manrope:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
/* ==========================================================================
   PrintCraft — design tokens
   Palette (from logo):  --navy #1A1F36 (ink/primary)  --orange #FF6B00 (accent)
                          --cream #F7F4EE (surface)     --cream-tint #EFEADD
   Type:     Display  = Bebas Neue (matches logo wordmark, bold impact headings)
             Body     = Manrope
             Utility  = IBM Plex Mono (steps, labels, prices)
   Signature: every card/button/section edge carries one diagonal facet-cut
              corner — a nod to the diamond mark — plus an orange "price tag"
              corner on every catalogue card.
   ========================================================================== */

:root{
  --navy:#1A1F36;
  --navy-2:#262C4A;
  --navy-3:#333A63;
  --orange:#FF6B00;
  --orange-light:#FF9245;
  --orange-deep:#D9560A;
  --cream:#F7F4EE;
  --cream-tint:#EFE9DB;
  --ink:#1A1F36;
  --ink-soft:#5B5F70;
  --line:rgba(26,31,54,.14);
  --line-dark:rgba(247,244,238,.16);
  --white:#FFFFFF;

  --font-display:'Bebas Neue', 'Space Grotesk', sans-serif;
  --font-body:'Manrope', sans-serif;
  --font-mono:'IBM Plex Mono', monospace;

  --facet:12px;
  --shadow-soft: 0 20px 50px -30px rgba(26,31,54,.35);
}

*,*::before,*::after{ box-sizing:border-box; }
html{ scroll-behavior:smooth; }
body{
  margin:0;
  font-family:var(--font-body);
  color:var(--ink);
  background:var(--cream);
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}
img{ max-width:100%; display:block; }
a{ color:inherit; }
h1,h2,h3,h4{ font-family:var(--font-display); font-weight:400; letter-spacing:.01em; line-height:1.08; margin:0 0 .4em; color:var(--navy); }
p{ margin:0 0 1em; }
ul{ margin:0; padding:0; list-style:none; }
button{ font-family:inherit; cursor:pointer; }
:focus-visible{ outline:2px solid var(--orange); outline-offset:2px; }

@media (prefers-reduced-motion: reduce){
  *{ animation-duration:.001ms !important; animation-iteration-count:1 !important; transition-duration:.001ms !important; scroll-behavior:auto !important; }
}

.wrap{ max-width:1180px; margin:0 auto; padding:0 24px; }
.facet-cut{ clip-path: polygon(var(--facet) 0, 100% 0, 100% 100%, 0 100%, 0 var(--facet)); }

/* ---------------- buttons ---------------- */
.btn{
  position:relative; overflow:hidden;
  display:inline-flex; align-items:center; gap:.5em;
  font-family:var(--font-mono); font-weight:600; font-size:.85rem;
  letter-spacing:.02em; text-decoration:none; text-transform:uppercase;
  padding:.95em 1.6em; border:1px solid transparent;
  clip-path: polygon(14px 0, 100% 0, 100% 100%, 0 100%, 0 14px);
  transition: transform .18s ease, background .18s ease, border-color .18s ease, box-shadow .18s ease;
}
.btn::before{
  content:""; position:absolute; inset:0; translate:-120% 0;
  background:linear-gradient(100deg, transparent, rgba(255,255,255,.4) 45%, transparent 90%);
  transition:translate .5s ease;
}
.btn:hover::before{ translate:120% 0; }
.btn:hover{ transform:translateY(-2px); }
.btn-small{ padding:.75em 1.3em; font-size:.75rem; clip-path: polygon(10px 0, 100% 0, 100% 100%, 0 100%, 0 10px); }
.btn-primary{ background:var(--orange); color:#fff; box-shadow:0 12px 28px -12px rgba(255,107,0,.55); }
.btn-primary:hover{ background:var(--orange-deep); box-shadow:0 16px 34px -10px rgba(255,107,0,.65); }
.btn-ghost{ background:transparent; color:var(--navy); border-color:var(--line); }
.btn-ghost:hover{ border-color:var(--navy); }
.btn-whatsapp{ background:#1E9E5A; color:#fff; box-shadow:0 10px 24px -12px rgba(30,158,90,.6); }
.btn-whatsapp:hover{ background:#177B47; }
.btn-pulse{ animation: btnPulse 2.6s ease-in-out infinite; }
@keyframes btnPulse{ 0%,100%{ box-shadow:0 12px 28px -12px rgba(255,107,0,.55); } 50%{ box-shadow:0 12px 34px -6px rgba(255,107,0,.85); } }

/* ---------------- header ---------------- */
.site-header{ position:sticky; top:0; z-index:50; background:rgba(247,244,238,.92); backdrop-filter:blur(8px); border-bottom:1px solid var(--line); }
.header-inner{ display:flex; align-items:center; gap:28px; padding:10px 24px; }
.logo{ display:flex; align-items:center; gap:10px; text-decoration:none; margin-right:auto; }
.logo-icon{ width:38px; height:44px; flex:none; display:block; }
.logo-word{ font-family:var(--font-display); font-weight:400; letter-spacing:.05em; color:var(--navy); font-size:1.35rem; line-height:1; }
.logo-word em{ font-style:normal; color:var(--orange); }
.site-nav{ display:flex; gap:24px; font-size:.92rem; font-weight:600; }
.site-nav a{ text-decoration:none; color:var(--ink-soft); }
.site-nav a:hover{ color:var(--orange); }
.nav-toggle{ display:none; background:none; border:0; width:30px; height:22px; flex-direction:column; justify-content:space-between; padding:0; }
.nav-toggle span{ display:block; height:2px; background:var(--navy); border-radius:2px; }

/* ---------------- hero ---------------- */
.hero{
  position:relative; overflow:hidden; color:#fff; padding:100px 0 80px;
  background:linear-gradient(160deg, var(--navy) 0%, var(--navy-2) 45%, var(--navy-3) 100%, var(--navy) 160%);
  background-size:200% 200%;
  animation: heroDrift 18s ease-in-out infinite;
}
@keyframes heroDrift{ 0%,100%{ background-position:0% 0%; } 50%{ background-position:100% 60%; } }
.hero-facets{ position:absolute; inset:0; pointer-events:none; }
.facet{ position:absolute; background:linear-gradient(135deg, var(--orange), transparent 70%); filter:blur(.5px); }
.facet.f1{ width:340px; height:340px; top:-120px; right:-80px; clip-path:polygon(50% 0,100% 40%,80% 100%,20% 100%,0 40%); opacity:.22; animation: facetSpin 26s linear infinite; }
.facet.f2{ width:180px; height:180px; bottom:-60px; left:10%; clip-path:polygon(0 0,100% 20%,70% 100%,10% 80%); background:linear-gradient(135deg,#fff,transparent 70%); opacity:.08; animation: facetFloat 9s ease-in-out infinite; }
.facet.f3{ width:120px; height:120px; top:20%; left:-40px; clip-path:polygon(50% 0,100% 100%,0 100%); opacity:.16; animation: facetFloat 7s ease-in-out infinite reverse; }
.facet.f4{ width:220px; height:220px; bottom:10%; right:8%; clip-path:polygon(50% 0,100% 50%,50% 100%,0 50%); opacity:.12; background:linear-gradient(135deg,#fff,transparent 70%); animation: facetSpin 34s linear infinite reverse; }
@keyframes facetSpin{ from{ transform:rotate(0deg); } to{ transform:rotate(360deg); } }
@keyframes facetFloat{ 0%,100%{ transform:translateY(0) scale(1); } 50%{ transform:translateY(-18px) scale(1.06); } }
.hero-inner{ position:relative; max-width:780px; }
.eyebrow{ font-family:var(--font-mono); text-transform:uppercase; letter-spacing:.12em; font-size:.78rem; color:var(--orange-light); margin-bottom:1em; display:flex; align-items:center; gap:.6em; }
.eyebrow::before{ content:""; width:8px; height:8px; background:var(--orange); clip-path:polygon(50% 0,100% 50%,50% 100%,0 50%); animation: pulseGlow 2.4s ease-in-out infinite; }
@keyframes pulseGlow{ 0%,100%{ opacity:.5; transform:scale(.85); } 50%{ opacity:1; transform:scale(1.15); } }
.hero h1{ color:#fff; font-size:clamp(2.6rem, 5.6vw, 4.4rem); margin-bottom:.35em; text-shadow:0 20px 60px rgba(0,0,0,.25); letter-spacing:.01em; }
.hero h1 em{ font-style:normal; background:linear-gradient(90deg, var(--orange), #ffb066 50%, var(--orange)); -webkit-background-clip:text; background-clip:text; color:transparent; }
.hero-sub{ color:rgba(255,255,255,.82); font-size:1.1rem; max-width:640px; }
.hero-cta{ display:flex; gap:16px; flex-wrap:wrap; margin:32px 0 48px; }
.hero .btn-ghost{ background:rgba(255,255,255,.06); color:#fff; border-color:rgba(255,255,255,.35); backdrop-filter:blur(6px); }
.hero .btn-ghost:hover{ border-color:var(--orange); }
.hero-stats{ display:flex; gap:40px; flex-wrap:wrap; border-top:1px solid rgba(255,255,255,.18); padding-top:28px; }
.hero-stats strong{ display:block; font-family:var(--font-display); font-size:2rem; color:#fff; letter-spacing:.02em; }
.hero-stats span{ font-size:.82rem; color:rgba(255,255,255,.65); }

.hero-sticker{ position:absolute; background:#fff; color:var(--navy); padding:10px 16px; font-family:var(--font-mono); font-size:.78rem; font-weight:600; clip-path: polygon(10px 0, 100% 0, 100% 100%, 0 100%, 0 10px); box-shadow:0 20px 40px -14px rgba(0,0,0,.4); display:flex; flex-direction:column; gap:2px; z-index:2; }
.hero-sticker strong{ color:var(--orange-deep); font-family:var(--font-mono); font-size:.85rem; }
.sticker-1{ top:14%; right:6%; animation: stickerFloat 5s ease-in-out infinite; }
.sticker-2{ bottom:16%; right:16%; animation: stickerFloat 6.5s ease-in-out infinite 1s; }
@keyframes stickerFloat{ 0%,100%{ transform:translateY(0) rotate(-2deg); } 50%{ transform:translateY(-10px) rotate(1deg); } }
@media (max-width: 980px){ .hero-sticker{ display:none; } }

/* ---------------- facet ticker ---------------- */
.ticker{ background:var(--navy); overflow:hidden; padding:14px 0; border-bottom:1px solid rgba(255,255,255,.08); }
.ticker-track{ display:flex; gap:2.5em; white-space:nowrap; width:max-content; animation: tickerScroll 38s linear infinite; }
.ticker-track span{ font-family:var(--font-mono); font-size:.82rem; letter-spacing:.04em; color:rgba(255,255,255,.6); display:flex; align-items:center; gap:2.5em; }
.ticker-track span b{ color:var(--orange-light); font-weight:600; }
.ticker-track span::after{ content:"◆"; color:var(--orange); margin-left:2.5em; font-size:.7em; }
@keyframes tickerScroll{ from{ transform:translateX(0); } to{ transform:translateX(-50%); } }
.ticker:hover .ticker-track{ animation-play-state:paused; }

/* ---------------- sample products ---------------- */
.products{ padding:88px 0 70px; background:var(--cream); }
.products h2{ font-size:clamp(2rem,4vw,2.8rem); max-width:760px; }
.section-intro.dark-text{ color:var(--ink-soft); }
.product-grid{ display:grid; grid-template-columns:repeat(auto-fill,minmax(240px,1fr)); gap:20px; margin-top:28px; }
.product-card{ background:#fff; border:1px solid var(--line); clip-path: polygon(14px 0, 100% 0, 100% 100%, 0 100%, 0 14px); overflow:hidden; transition:transform .2s ease, box-shadow .2s ease, border-color .2s ease; display:flex; flex-direction:column; }
.product-card:hover{ transform:translateY(-6px); box-shadow:0 28px 54px -26px rgba(26,31,54,.4); border-color:var(--orange-light); }
.product-media{ position:relative; aspect-ratio:1/1; background:linear-gradient(160deg, var(--cream-tint), #fff); display:flex; align-items:center; justify-content:center; overflow:hidden; }
.product-media svg{ width:62%; height:62%; transition:transform .3s ease; }
.product-card:hover .product-media svg{ transform:scale(1.08) rotate(-2deg); }
.product-badge{ position:absolute; top:10px; left:10px; background:var(--navy); color:#fff; font-family:var(--font-mono); font-size:.65rem; text-transform:uppercase; letter-spacing:.05em; padding:.35em .7em; clip-path: polygon(6px 0, 100% 0, 100% 100%, 0 100%, 0 6px); }
.product-body{ padding:18px 20px 20px; display:flex; flex-direction:column; gap:.4em; flex:1; }
.product-cat{ font-family:var(--font-mono); font-size:.68rem; text-transform:uppercase; letter-spacing:.06em; color:var(--orange-deep); }
.product-body h3{ font-size:1.05rem; margin:0; }
.product-price{ font-family:var(--font-mono); font-weight:700; color:var(--navy); font-size:1rem; margin-top:.2em; }
.product-price span{ font-weight:500; color:var(--ink-soft); font-size:.78rem; text-transform:uppercase; letter-spacing:.03em; margin-left:.4em; }
.product-cta{ margin-top:auto; padding-top:10px; font-family:var(--font-mono); font-size:.78rem; font-weight:600; color:var(--navy); text-decoration:none; border-bottom:1px solid var(--navy); align-self:flex-start; }
.product-cta:hover{ color:var(--orange-deep); border-color:var(--orange-deep); }
.product-grid[data-empty]::after{ content:"No sample products in this category yet — ask us in the form below."; color:var(--ink-soft); font-size:.9rem; }

/* ---------------- use cases ---------------- */
.usecases{ padding:80px 0 60px; }
.section-label{ font-family:var(--font-mono); text-transform:uppercase; letter-spacing:.1em; font-size:.78rem; color:var(--orange-deep); margin-bottom:.8em; }
.section-label.light{ color:var(--orange-light); }
.usecase-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:32px; }
.usecase-col h3{ font-size:1.5rem; border-bottom:2px solid var(--line); padding-bottom:.4em; margin-bottom:.7em; }
.usecase-col li{ border-bottom:1px solid var(--line); }
.usecase-col a{ display:block; padding:.7em 0; text-decoration:none; color:var(--ink); font-weight:600; font-size:.95rem; transition:color .15s, padding-left .15s; }
.usecase-col a:hover{ color:var(--orange-deep); padding-left:6px; }

/* ---------------- engines ---------------- */
.engines{ background:var(--navy); color:#fff; padding:88px 0; }
.engines h2{ color:#fff; font-size:clamp(2rem,4vw,2.8rem); max-width:720px; }
.section-intro{ color:rgba(255,255,255,.75); max-width:640px; }
.engine-grid{ display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:20px; margin-top:36px; }
.engine-card{ background:rgba(255,255,255,.06); border:1px solid var(--line-dark); padding:26px 22px; clip-path: polygon(16px 0, 100% 0, 100% 100%, 0 100%, 0 16px); backdrop-filter:blur(6px); transition:transform .25s ease, background .25s ease, box-shadow .25s ease; }
.engine-card:hover{ transform:translateY(-6px); background:rgba(255,255,255,.1); box-shadow:0 24px 50px -20px rgba(0,0,0,.45), 0 0 0 1px rgba(255,107,0,.4); }
.engine-num{ font-family:var(--font-mono); color:var(--orange); font-size:.85rem; }
.engine-card h3{ color:#fff; font-size:1.25rem; margin:.5em 0 .3em; letter-spacing:.02em; }
.engine-card p{ color:rgba(255,255,255,.68); font-size:.9rem; margin:0; }

/* ---------------- verticals / catalogue ---------------- */
.verticals{ padding:88px 0; background:var(--cream-tint); position:relative; }
.verticals h2{ font-size:clamp(2rem,4vw,2.8rem); max-width:760px; }
.filter-bar{ display:flex; gap:10px; flex-wrap:wrap; margin:28px 0; }
.filter-btn{ background:#fff; border:1px solid var(--line); padding:.5em 1.1em; font-family:var(--font-mono); font-size:.78rem; text-transform:uppercase; letter-spacing:.05em; border-radius:20px; color:var(--ink-soft); transition:background .15s, color .15s, border-color .15s; }
.filter-btn.is-active, .filter-btn:hover{ background:var(--navy); color:#fff; border-color:var(--navy); }
.vertical-grid{ display:grid; grid-template-columns:repeat(auto-fill,minmax(270px,1fr)); gap:18px; }
.vertical-card{ position:relative; background:#fff; border:1px solid var(--line); padding:22px; padding-top:44px; clip-path: polygon(14px 0, 100% 0, 100% 100%, 0 100%, 0 14px); transition:transform .2s ease, box-shadow .2s ease, border-color .2s ease; }
.vertical-card:hover{ transform:translateY(-5px); box-shadow:0 26px 50px -28px rgba(26,31,54,.4); border-color:var(--orange-light); }
.vertical-card .v-price{ position:absolute; top:0; right:0; background:var(--orange); color:#fff; font-family:var(--font-mono); font-size:.72rem; font-weight:700; padding:.5em .8em; clip-path: polygon(10px 0, 100% 0, 100% 100%, 0 100%); }
.vertical-card .v-tag{ font-family:var(--font-mono); font-size:.7rem; text-transform:uppercase; letter-spacing:.06em; color:var(--orange-deep); }
.vertical-card h3{ font-size:1.15rem; margin:.35em 0 .4em; }
.vertical-card p{ font-size:.87rem; color:var(--ink-soft); margin:0 0 .8em; }
.vertical-card .v-link{ font-family:var(--font-mono); font-size:.78rem; font-weight:600; color:var(--navy); text-decoration:none; border-bottom:1px solid var(--navy); padding-bottom:1px; }
.vertical-card .v-link:hover{ color:var(--orange-deep); border-color:var(--orange-deep); }
.vertical-card[hidden]{ display:none; }
.price-note{ font-size:.82rem; color:var(--ink-soft); margin-top:-8px; margin-bottom:28px; max-width:640px; }

/* ---------------- how it works ---------------- */
.how{ background:var(--navy-2); color:#fff; padding:88px 0; }
.how h2{ color:#fff; font-size:clamp(2rem,4vw,2.8rem); max-width:760px; }
.flow{ display:grid; grid-template-columns:repeat(auto-fill,minmax(230px,1fr)); gap:20px; margin:36px 0 0; padding:0; }
.flow li{ display:flex; gap:14px; background:rgba(255,255,255,.05); border:1px solid var(--line-dark); padding:20px; clip-path: polygon(12px 0, 100% 0, 100% 100%, 0 100%, 0 12px); }
.flow-step{ font-family:var(--font-mono); font-weight:700; font-size:.95rem; color:var(--navy); background:var(--orange); width:28px; height:28px; border-radius:50%; display:flex; align-items:center; justify-content:center; flex:none; }
.flow h4{ color:#fff; font-size:1.05rem; margin:0 0 .3em; letter-spacing:.01em; }
.flow p{ color:rgba(255,255,255,.65); font-size:.85rem; margin:0; }

/* ---------------- requirement wizard ---------------- */
.requirement{ padding:88px 0; position:relative; }
.requirement h2{ font-size:clamp(2rem,4vw,2.8rem); max-width:720px; }
.wizard{ position:relative; background:#fff; border:1px solid var(--line); margin-top:36px; padding:44px clamp(20px,4vw,52px) 40px; clip-path: polygon(24px 0, 100% 0, 100% 100%, 0 100%, 0 24px); box-shadow:0 40px 80px -40px rgba(26,31,54,.4); }
.wizard::before{ content:""; position:absolute; top:0; left:24px; right:0; height:4px; background:linear-gradient(90deg, var(--navy), var(--orange)); }
.wizard-progress{ display:flex; align-items:center; gap:0; margin-bottom:36px; }
.prog-step{ width:32px; height:32px; border-radius:50%; border:2px solid var(--line); display:flex; align-items:center; justify-content:center; font-family:var(--font-mono); font-size:.85rem; font-weight:700; color:var(--ink-soft); flex:none; background:#fff; }
.prog-step.is-active, .prog-step.is-done{ border-color:var(--orange); color:var(--orange-deep); }
.prog-step.is-done{ background:var(--orange); color:#fff; }
.prog-line{ flex:1; height:2px; background:var(--line); margin:0 4px; }

.wizard-step{ display:none; }
.wizard-step.is-active{ display:block; animation:fadeIn .3s ease; }
@keyframes fadeIn{ from{ opacity:0; transform:translateY(6px);} to{ opacity:1; transform:none; } }
.wizard-step h3{ font-size:1.7rem; margin-bottom:.6em; }

.option-grid{ display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:16px; }
.option-card{ position:relative; overflow:hidden; text-align:left; background:var(--cream); border:1px solid var(--line); padding:20px; clip-path: polygon(10px 0, 100% 0, 100% 100%, 0 100%, 0 10px); display:flex; flex-direction:column; gap:.3em; transition:transform .18s ease, border-color .18s ease, box-shadow .18s ease; }
.option-card strong{ font-family:var(--font-display); font-weight:400; letter-spacing:.02em; color:var(--navy); font-size:1.15rem; }
.option-card span{ font-size:.85rem; color:var(--ink-soft); }
.option-card:hover{ border-color:var(--orange); transform:translateY(-3px); box-shadow:0 18px 34px -22px rgba(26,31,54,.4); }
.option-card.is-selected{ border-color:var(--orange); background:var(--cream-tint); box-shadow:inset 0 0 0 1px var(--orange), 0 18px 34px -22px rgba(26,31,54,.4); }
.option-card.is-selected::after{ content:"◆"; position:absolute; top:12px; right:14px; color:var(--orange); font-size:.75rem; }

.form-grid{ display:grid; grid-template-columns:1fr 1fr; gap:20px; margin-top:8px; }
.form-grid label{ display:flex; flex-direction:column; gap:.4em; font-size:.85rem; font-weight:600; color:var(--ink-soft); }
.form-grid label.full{ grid-column:1 / -1; }
.form-grid input, .form-grid textarea{
  font-family:var(--font-body); font-size:.95rem; color:var(--ink);
  border:1px solid var(--line); background:var(--cream); padding:.8em 1em; border-radius:2px;
}
.form-grid input:focus, .form-grid textarea:focus{ border-color:var(--orange); outline:none; }
.wizard-actions{ display:flex; gap:12px; margin-top:28px; flex-wrap:wrap; }
.wizard-back{ margin-right:auto; }
.send-actions{ align-items:center; }

.review-box{ background:var(--cream-tint); border:1px solid var(--line); padding:22px 26px; font-size:.92rem; clip-path: polygon(12px 0, 100% 0, 100% 100%, 0 100%, 0 12px); }
.review-box dl{ margin:0; display:grid; grid-template-columns:160px 1fr; gap:8px 16px; }
.review-box dt{ font-family:var(--font-mono); font-size:.78rem; text-transform:uppercase; letter-spacing:.04em; color:var(--ink-soft); }
.review-box dd{ margin:0; }
.copy-confirm{ color:var(--orange-deep); font-family:var(--font-mono); font-size:.85rem; margin-top:10px; }

/* ---------------- floating CTA ---------------- */
.float-cta{ position:fixed; bottom:24px; right:24px; z-index:60; box-shadow:0 20px 45px -14px rgba(26,31,54,.5); }
@media (max-width:640px){ .float-cta{ bottom:16px; right:16px; padding:.7em 1.1em; } }

/* ---------------- scroll reveal ---------------- */
.reveal{ opacity:0; transform:translateY(28px); transition:opacity .7s ease, transform .7s ease; }
.reveal.in-view{ opacity:1; transform:none; }
.reveal-stagger.in-view{ transition-delay:calc(var(--stagger, 0) * 70ms); }

.verticals::before, .requirement::before{
  content:""; position:absolute; inset:0; pointer-events:none; opacity:.5;
  background-image:
    linear-gradient(135deg, rgba(26,31,54,.05) 25%, transparent 25%),
    linear-gradient(225deg, rgba(26,31,54,.05) 25%, transparent 25%);
  background-size:64px 64px;
  background-position:0 0, 32px 0;
  mask-image: linear-gradient(to bottom, black, transparent 70%);
}
.verticals > .wrap, .requirement > .wrap{ position:relative; }

/* ---------------- footer ---------------- */
.site-footer{ background:var(--ink); color:rgba(255,255,255,.7); padding:64px 0 0; }
.footer-inner{ display:grid; grid-template-columns:1.4fr 1fr 1fr; gap:40px; padding-bottom:40px; border-bottom:1px solid rgba(255,255,255,.12); }
.footer-brand .footer-logo{ width:120px; height:auto; margin-bottom:14px; }
.footer-brand p{ margin-top:14px; max-width:320px; font-size:.9rem; }
.site-footer h4{ color:#fff; font-size:.85rem; text-transform:uppercase; letter-spacing:.08em; font-family:var(--font-mono); margin-bottom:1em; }
.footer-contact p, .footer-links a{ display:block; margin-bottom:.6em; text-decoration:none; font-size:.92rem; }
.footer-contact a{ text-decoration:none; }
.footer-contact a:hover, .footer-links a:hover{ color:#fff; }
.founder{ color:var(--orange-light); font-weight:600; }
.footer-bottom{ padding:22px 24px; font-size:.8rem; text-align:center; color:rgba(255,255,255,.4); }

/* ---------------- responsive ---------------- */
@media (max-width: 860px){
  .usecase-grid{ grid-template-columns:1fr; }
  .footer-inner{ grid-template-columns:1fr; }
  .form-grid{ grid-template-columns:1fr; }
  .site-nav{ display:none; }
  .nav-toggle{ display:flex; }
}

</style>
</head>
<body>

<!-- ============ NAV ============ -->
<header class="site-header" id="top">
  <div class="wrap header-inner">
    <a class="logo" href="#top" aria-label="PrintCraft home">
      <svg class="logo-icon" viewBox="130 25 140 160" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <rect x="130" y="25" width="140" height="160" fill="#F7F4EE"/>
        <polygon points="200,40  252,90  148,90" fill="#1A1F36"/>
        <polygon points="148,90  200,40  176,90" fill="#1A1F36" opacity="0.45"/>
        <polygon points="252,90  200,40  224,90" fill="#1A1F36" opacity="0.65"/>
        <line x1="200" y1="40"  x2="200" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="148" y1="90"  x2="252" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="200" y1="40"  x2="148" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="200" y1="40"  x2="252" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <polygon points="148,90  252,90  200,172" fill="#FF6B00"/>
        <polygon points="148,90  200,172  174,90"  fill="#1A1F36" opacity="0.12"/>
        <polygon points="252,90  200,172  226,90"  fill="#FF6B00" opacity="0.45"/>
        <line x1="200" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="148" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="252" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="174" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="0.8" opacity="0.6"/>
        <line x1="226" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="0.8" opacity="0.6"/>
      </svg>
      <span class="logo-word">PRINT<em>CRAFT</em></span>
    </a>
    <nav class="site-nav" aria-label="Primary">
      <a href="#products">Sample Products</a>
      <a href="#engines">Solutions</a>
      <a href="#verticals">Verticals</a>
      <a href="#how-it-works">How it works</a>
      <a href="#contact">Contact</a>
    </nav>
    <a class="btn btn-primary btn-small" href="#requirement">Start your requirement</a>
    <button class="nav-toggle" id="navToggle" aria-label="Open menu" aria-expanded="false">
      <span></span><span></span><span></span>
    </button>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero">
  <div class="hero-facets" aria-hidden="true">
    <span class="facet f1"></span>
    <span class="facet f2"></span>
    <span class="facet f3"></span>
    <span class="facet f4"></span>
  </div>
  <div class="hero-sticker sticker-1" aria-hidden="true">Onboarding kits<strong>from ₹500</strong></div>
  <div class="hero-sticker sticker-2" aria-hidden="true">Custom apparel<strong>from ₹150</strong></div>
  <div class="wrap hero-inner">
    <p class="eyebrow">One-stop customization &amp; execution platform</p>
    <h1>Every physical touchpoint your brand needs, <em>cut to spec.</em></h1>
    <p class="hero-sub">From a 500-employee onboarding rollout to a single wedding welcome box — PrintCraft designs, sources and delivers customized merchandise, retail branding and on-ground activation, city by city, across India.</p>
    <div class="hero-cta">
      <a href="#requirement" class="btn btn-primary">Start your requirement</a>
      <a href="#verticals" class="btn btn-ghost">Explore what we craft</a>
    </div>
    <div class="hero-stats">
      <div><strong>18</strong><span>business verticals</span></div>
      <div><strong>100+</strong><span>product categories</span></div>
      <div><strong>500–1,000+</strong><span>possible SKUs</span></div>
    </div>
  </div>
</section>

<!-- ============ TICKER ============ -->
<div class="ticker" aria-hidden="true">
  <div class="ticker-track" id="tickerTrack"></div>
</div>

<!-- ============ SAMPLE PRODUCTS ============ -->
<section class="products" id="products">
  <div class="wrap">
    <p class="section-label">A few things we make</p>
    <h2>Browse sample products, then customize yours.</h2>
    <p class="section-intro dark-text">Illustrative examples from across our catalogue — every product shown here can be branded, personalized and quoted for your exact quantity.</p>

    <div class="filter-bar" id="productFilterBar" role="tablist" aria-label="Filter sample products">
      <button class="filter-btn is-active" data-pfilter="all" role="tab" aria-selected="true">All</button>
      <button class="filter-btn" data-pfilter="corporate" role="tab" aria-selected="false">Corporate</button>
      <button class="filter-btn" data-pfilter="personal" role="tab" aria-selected="false">Personal</button>
      <button class="filter-btn" data-pfilter="apparel" role="tab" aria-selected="false">Apparel</button>
      <button class="filter-btn" data-pfilter="packaging" role="tab" aria-selected="false">Packaging &amp; POSM</button>
    </div>

    <div class="product-grid" id="productGrid">
      <!-- populated by script.js from PRODUCTS data -->
    </div>
  </div>
</section>

<!-- ============ FOR BUSINESS / PERSONAL / CREATORS ============ -->
<section class="usecases">
  <div class="wrap">
    <p class="section-label">Start with what you're trying to do</p>
    <div class="usecase-grid">

      <div class="usecase-col">
        <h3>For Business</h3>
        <ul>
          <li><a href="#requirement" data-role="business" data-vertical="Employee Onboarding Kits">Welcome new employees</a></li>
          <li><a href="#requirement" data-role="business" data-vertical="Employee Gifting &amp; Rewards">Reward your team</a></li>
          <li><a href="#requirement" data-role="business" data-vertical="Corporate Events &amp; Conferences">Launch a product or event</a></li>
          <li><a href="#requirement" data-role="business" data-vertical="On-Ground Marketing / BTL Activation">Run an on-ground activation</a></li>
          <li><a href="#requirement" data-role="business" data-vertical="Festival Corporate Gifting">Gift your clients</a></li>
          <li><a href="#requirement" data-role="business" data-vertical="Retail Branding &amp; POSM">Brand your retail stores</a></li>
        </ul>
      </div>

      <div class="usecase-col">
        <h3>For Personal</h3>
        <ul>
          <li><a href="#requirement" data-role="personal" data-vertical="Wedding Customization">Plan a wedding</a></li>
          <li><a href="#requirement" data-role="personal" data-vertical="Birthday &amp; Personal Celebrations">Celebrate a birthday</a></li>
          <li><a href="#requirement" data-role="personal" data-vertical="Home Décor &amp; Personalized Interiors">Decorate your home</a></li>
          <li><a href="#requirement" data-role="personal" data-vertical="Birthday &amp; Personal Celebrations">Create personalized gifts</a></li>
        </ul>
      </div>

      <div class="usecase-col">
        <h3>For Creators</h3>
        <ul>
          <li><a href="#requirement" data-role="creator" data-vertical="Creator &amp; Influencer Merchandise">Launch your merchandise</a></li>
          <li><a href="#requirement" data-role="creator" data-vertical="Creator &amp; Influencer Merchandise">Build your fan store</a></li>
          <li><a href="#requirement" data-role="creator" data-vertical="Sports Teams, Clubs &amp; Communities">Kit out your team or club</a></li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- ============ 5 SOLUTION ENGINES ============ -->
<section class="engines" id="engines">
  <div class="wrap">
    <p class="section-label light">Five engines. One platform.</p>
    <h2>We sell solutions, not SKUs.</h2>
    <p class="section-intro">Ask for "200 T-shirts" and you're comparing ₹180 to ₹190. Ask for a complete employee joining experience, and you're buying an outcome. Everything we build sits inside one of five engines:</p>

    <div class="engine-grid">
      <article class="engine-card">
        <span class="engine-num">01</span>
        <h3>Corporate Merchandise &amp; Employee Experience</h3>
        <p>Joining kits, employee gifting, rewards &amp; recognition, festival gifting, leadership gifts.</p>
      </article>
      <article class="engine-card">
        <span class="engine-num">02</span>
        <h3>On-Ground Activation &amp; BTL</h3>
        <p>FOS kits, canopies, event T-shirts, signage, dealer branding, kiosk kits, activation merchandise.</p>
      </article>
      <article class="engine-card">
        <span class="engine-num">03</span>
        <h3>Events &amp; Conferences</h3>
        <p>Complete event branding, delegate kits, merchandise, awards, stage &amp; venue dressing.</p>
      </article>
      <article class="engine-card">
        <span class="engine-num">04</span>
        <h3>Personal Celebrations</h3>
        <p>Weddings, birthdays, baby showers and home functions, from invitations to return gifts.</p>
      </article>
      <article class="engine-card">
        <span class="engine-num">05</span>
        <h3>Packaging &amp; D2C Brand Solutions</h3>
        <p>Boxes, labels, stickers, inserts and branded packaging for D2C and marketplace sellers.</p>
      </article>
    </div>
  </div>
</section>

<!-- ============ 18 VERTICALS ============ -->
<section class="verticals" id="verticals">
  <div class="wrap">
    <p class="section-label">The full catalogue</p>
    <h2>18 verticals, 100+ categories, one vendor network.</h2>
    <p class="price-note">Indicative starting prices based on current Indian market rates for comparable customization work — your exact quote depends on quantity, material and finish. Get an exact number with the form below.</p>

    <div class="filter-bar" role="tablist" aria-label="Filter verticals by buyer">
      <button class="filter-btn is-active" data-filter="all" role="tab" aria-selected="true">All</button>
      <button class="filter-btn" data-filter="B2B" role="tab" aria-selected="false">Business</button>
      <button class="filter-btn" data-filter="B2C" role="tab" aria-selected="false">Personal</button>
      <button class="filter-btn" data-filter="Both" role="tab" aria-selected="false">Both</button>
    </div>

    <div class="vertical-grid" id="verticalGrid">
      <!-- populated by script.js from VERTICALS data -->
    </div>
  </div>
</section>

<!-- ============ HOW IT WORKS ============ -->
<section class="how" id="how-it-works">
  <div class="wrap">
    <p class="section-label light">How an order actually moves</p>
    <h2>Demand, catalogue, design, vendor network, quality, fulfilment.</h2>
    <p class="section-intro">We are not a printing factory. We are the layer that turns a requirement into an approved vendor order, quality-checked and delivered — or installed — wherever it needs to land.</p>

    <ol class="flow">
      <li><span class="flow-step">1</span><div><h4>Tell us the use case</h4><p>Onboarding, activation, wedding, packaging — whatever the occasion.</p></div></li>
      <li><span class="flow-step">2</span><div><h4>Choose product &amp; package</h4><p>Pick from a curated set or build a custom package across SKUs.</p></div></li>
      <li><span class="flow-step">3</span><div><h4>Share logo, photo or text</h4><p>Upload your branding and personalization details.</p></div></li>
      <li><span class="flow-step">4</span><div><h4>Design preview &amp; quotation</h4><p>We route it to the right vendor and price it for you.</p></div></li>
      <li><span class="flow-step">5</span><div><h4>Approve &amp; pay</h4><p>Sign off on the design and confirm the order.</p></div></li>
      <li><span class="flow-step">6</span><div><h4>Order routing engine</h4><p>Your order goes to our approved vendor network for production.</p></div></li>
      <li><span class="flow-step">7</span><div><h4>Quality check &amp; consolidation</h4><p>Every batch is checked and consolidated centrally before dispatch.</p></div></li>
      <li><span class="flow-step">8</span><div><h4>Delivery or installation</h4><p>Pan-India delivery, or on-site installation for activations and events.</p></div></li>
    </ol>
  </div>
</section>

<!-- ============ REQUIREMENT WIZARD ============ -->
<section class="requirement" id="requirement">
  <div class="wrap">
    <p class="section-label">Get a quote</p>
    <h2>Tell us what you need. We'll take it from there.</h2>
    <p class="section-intro">This takes about two minutes. At the end, you can send your requirement straight to our team by email or WhatsApp — no account needed.</p>

    <div class="wizard" id="wizard" data-step="1">

      <div class="wizard-progress" aria-hidden="true">
        <span class="prog-step is-active" data-progress="1">1</span>
        <span class="prog-line"></span>
        <span class="prog-step" data-progress="2">2</span>
        <span class="prog-line"></span>
        <span class="prog-step" data-progress="3">3</span>
        <span class="prog-line"></span>
        <span class="prog-step" data-progress="4">4</span>
        <span class="prog-line"></span>
        <span class="prog-step" data-progress="5">5</span>
      </div>

      <!-- STEP 1: ROLE -->
      <div class="wizard-step is-active" data-step-panel="1">
        <h3>Who is this for?</h3>
        <div class="option-grid" id="roleOptions">
          <button class="option-card" data-role="business">
            <strong>Business</strong><span>Corporate, SME, startup, agency</span>
          </button>
          <button class="option-card" data-role="personal">
            <strong>Personal</strong><span>Wedding, birthday, home, family</span>
          </button>
          <button class="option-card" data-role="creator">
            <strong>Creator</strong><span>Influencer, team, community</span>
          </button>
        </div>
      </div>

      <!-- STEP 2: VERTICAL -->
      <div class="wizard-step" data-step-panel="2">
        <h3>Which of these is closest to your need?</h3>
        <div class="option-grid" id="verticalOptions"></div>
        <button class="btn btn-ghost btn-small wizard-back" data-back="1">Back</button>
      </div>

      <!-- STEP 3: DETAILS -->
      <div class="wizard-step" data-step-panel="3">
        <h3>A few details</h3>
        <div class="form-grid">
          <label>
            <span>Approximate quantity / order size</span>
            <input type="text" id="fieldQuantity" placeholder="e.g. 500 units, or not sure yet">
          </label>
          <label>
            <span>Needed by</span>
            <input type="date" id="fieldDate">
          </label>
          <label class="full">
            <span>Describe what you have in mind</span>
            <textarea id="fieldDescription" rows="4" placeholder="Products, branding details, cities involved, budget range — anything that helps us scope this."></textarea>
          </label>
        </div>
        <div class="wizard-actions">
          <button class="btn btn-ghost btn-small wizard-back" data-back="2">Back</button>
          <button class="btn btn-primary btn-small wizard-next" data-next="4">Continue</button>
        </div>
      </div>

      <!-- STEP 4: CONTACT -->
      <div class="wizard-step" data-step-panel="4">
        <h3>Where should we send the quotation?</h3>
        <div class="form-grid">
          <label>
            <span>Your name</span>
            <input type="text" id="fieldName" placeholder="Full name">
          </label>
          <label>
            <span>Company / organization <em>(optional)</em></span>
            <input type="text" id="fieldCompany" placeholder="Leave blank if personal">
          </label>
          <label>
            <span>Email</span>
            <input type="email" id="fieldEmail" placeholder="you@company.com">
          </label>
          <label>
            <span>Phone / WhatsApp</span>
            <input type="tel" id="fieldPhone" placeholder="+91 ...">
          </label>
          <label class="full">
            <span>City</span>
            <input type="text" id="fieldCity" placeholder="Where should this be delivered or installed?">
          </label>
        </div>
        <div class="wizard-actions">
          <button class="btn btn-ghost btn-small wizard-back" data-back="3">Back</button>
          <button class="btn btn-primary btn-small" id="reviewBtn">Review requirement</button>
        </div>
      </div>

      <!-- STEP 5: REVIEW & SEND -->
      <div class="wizard-step" data-step-panel="5">
        <h3>Review &amp; send</h3>
        <div class="review-box" id="reviewBox"></div>
        <div class="wizard-actions send-actions">
          <button class="btn btn-ghost btn-small wizard-back" data-back="4">Back</button>
          <a class="btn btn-primary btn-small" id="sendEmailBtn" href="#">Send by email</a>
          <a class="btn btn-whatsapp btn-small" id="sendWhatsappBtn" href="#" target="_blank" rel="noopener">Send on WhatsApp</a>
          <button class="btn btn-ghost btn-small" id="copyBtn">Copy details</button>
        </div>
        <p class="copy-confirm" id="copyConfirm" hidden>Copied to clipboard.</p>
      </div>

    </div>
  </div>
</section>

<!-- ============ CONTACT / FOOTER ============ -->
<footer class="site-footer" id="contact">
  <div class="wrap footer-inner">
    <div class="footer-brand">
      <svg class="footer-logo" width="140" height="112" viewBox="0 0 400 320" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <rect width="400" height="320" fill="#F7F4EE"/>
        <polygon points="200,40  252,90  148,90" fill="#1A1F36"/>
        <polygon points="148,90  200,40  176,90" fill="#1A1F36" opacity="0.45"/>
        <polygon points="252,90  200,40  224,90" fill="#1A1F36" opacity="0.65"/>
        <line x1="200" y1="40"  x2="200" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="148" y1="90"  x2="252" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="200" y1="40"  x2="148" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="200" y1="40"  x2="252" y2="90"  stroke="#F7F4EE" stroke-width="1.4"/>
        <polygon points="148,90  252,90  200,172" fill="#FF6B00"/>
        <polygon points="148,90  200,172  174,90"  fill="#1A1F36" opacity="0.12"/>
        <polygon points="252,90  200,172  226,90"  fill="#FF6B00" opacity="0.45"/>
        <line x1="200" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="148" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="252" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="1.4"/>
        <line x1="174" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="0.8" opacity="0.6"/>
        <line x1="226" y1="90"  x2="200" y2="172" stroke="#F7F4EE" stroke-width="0.8" opacity="0.6"/>
        <text x="200" y="244" text-anchor="middle" font-family="'Bebas Neue','Arial Black',Impact,sans-serif" font-size="72" fill="#1A1F36" letter-spacing="8">PRINT</text>
        <text x="200" y="308" text-anchor="middle" font-family="'Bebas Neue','Arial Black',Impact,sans-serif" font-size="72" fill="#FF6B00" letter-spacing="8">CRAFT</text>
      </svg>
      <p>Customization, merchandise &amp; branded experience — designed, sourced and delivered across India.</p>
    </div>
    <div class="footer-contact">
      <h4>Talk to us</h4>
      <p><a href="mailto:info@printcraftproducts.com">info@printcraftproducts.com</a></p>
      <p><a href="tel:+918210718668">+91 8210-7018668</a></p>
      <p class="founder">Ruchi Singh, Founder &amp; CEO</p>
    </div>
    <div class="footer-links">
      <h4>Explore</h4>
      <a href="#engines">Solutions</a>
      <a href="#verticals">Verticals</a>
      <a href="#requirement">Get a quote</a>
    </div>
  </div>
  <div class="wrap footer-bottom">
    <p>&copy; <span id="year"></span> PrintCraft. All rights reserved.</p>
  </div>
</footer>

<a href="#requirement" class="btn btn-primary float-cta btn-pulse">Get instant quote</a>

<script>
/* ==========================================================================
   PrintCraft — site behaviour
   1) Renders the 18-vertical catalogue + filter bar
   2) Drives the requirement-collection wizard
   3) Builds an email / WhatsApp handoff from the collected requirement
   ========================================================================== */

const COMPANY_EMAIL = "info@printcraftproducts.com";
const COMPANY_PHONE = "918210718668"; // digits only, for wa.me / tel links

/* ---------------- 1. Verticals data ---------------- */
const VERTICALS = [
  { name:"Corporate Stationery & Business Printing", buyer:"B2B", role:"business", price:"₹3 – ₹15 /card",
    desc:"Business cards, letterheads, ID cards, brochures and everyday branded stationery." },
  { name:"Employee Onboarding Kits", buyer:"B2B", role:"business", price:"₹500 – ₹5,000+ /kit",
    desc:"Welcome boxes, apparel, tech accessories and ID kits for new joiners at every level." },
  { name:"Employee Gifting & Rewards", buyer:"B2B", role:"business", price:"₹800 – ₹6,000+ /gift",
    desc:"Trophies, hampers and recognition gifts for birthdays, anniversaries and milestones." },
  { name:"Festival Corporate Gifting", buyer:"B2B", role:"business", price:"₹500 – ₹5,000+ /hamper",
    desc:"Diwali, Christmas and regional festival hampers, sweet boxes and branded packaging." },
  { name:"Corporate Events & Conferences", buyer:"B2B", role:"business", price:"₹800 – ₹4,000+ /delegate",
    desc:"Complete delegate kits, stage branding, badges and souvenirs for a full event." },
  { name:"On-Ground Marketing / BTL Activation", buyer:"B2B", role:"business", price:"₹25K – ₹5L+ /activation",
    desc:"Canopies, standees, FOS kits, vehicle branding and field-activation merchandise." },
  { name:"Retail Branding & POSM", buyer:"B2B", role:"business", price:"₹150 – ₹800 /fixture",
    desc:"Shelf strips, displays, floor and window graphics for multi-store rollouts." },
  { name:"Customized Apparel & Uniforms", buyer:"Both", role:"business", price:"₹150 – ₹900 /piece",
    desc:"T-shirts, uniforms and workwear across screen print, DTF, embroidery and sublimation." },
  { name:"Promotional Merchandise", buyer:"B2B", role:"business", price:"₹15 – ₹500 /piece",
    desc:"Pens, bottles, bags and tech accessories for giveaways, incentives and loyalty programs." },
  { name:"Packaging Customization", buyer:"B2B", role:"business", price:"₹4 – ₹50 /box",
    desc:"Shipping boxes, labels, stickers and inserts for D2C and marketplace sellers." },
  { name:"Wedding Customization", buyer:"B2C", role:"personal", price:"₹10 – ₹600 /card",
    desc:"Invitations, welcome boards, hampers, return gifts and everything in between." },
  { name:"Birthday & Personal Celebrations", buyer:"B2C", role:"personal", price:"₹5K – ₹50K+ /event",
    desc:"Banners, return gifts, photo products and personalized decoration kits." },
  { name:"Home Décor & Personalized Interiors", buyer:"B2C", role:"personal", price:"₹500 – ₹15,000 /piece",
    desc:"Photo frames, canvas prints, name plates and personalized home accents." },
  { name:"Schools & Colleges", buyer:"B2B", role:"business", price:"₹20 – ₹60 /ID card",
    desc:"ID cards, uniforms, annual-day merchandise, yearbooks and graduation products." },
  { name:"Sports Teams, Clubs & Communities", buyer:"Both", role:"creator", price:"₹350 – ₹900 /jersey",
    desc:"Jerseys, medals, trophies and fan merchandise for teams and community groups." },
  { name:"Creator & Influencer Merchandise", buyer:"B2B", role:"creator", price:"₹300 – ₹900 /piece",
    desc:"Print-on-demand apparel and accessories, from storefront to fulfilment." },
  { name:"Hospitality, Restaurants & Hotels", buyer:"B2B", role:"business", price:"₹200 – ₹2,000 /piece",
    desc:"Menus, staff uniforms, room signage and branded packaging for guest experience." },
  { name:"Industrial, Logistics & Field Workforce", buyer:"B2B", role:"business", price:"₹350 – ₹1,500 /piece",
    desc:"Reflective jackets, safety gear, ID kits and signage for field and warehouse teams." },
];

/* ---------------- 2. Sample products (illustrative — original vector icons, no photos) ---------------- */
const ICONS = {
  mug: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M25 30h40v40a10 10 0 0 1-10 10H35a10 10 0 0 1-10-10V30z" fill="#1A1F36"/><path d="M65 40h8a10 10 0 0 1 0 20h-8V40z" fill="none" stroke="#1A1F36" stroke-width="5"/><rect x="25" y="30" width="40" height="10" fill="#FF6B00"/><path d="M33 22c0-4 4-4 4-8s-4-4-4-8" fill="none" stroke="#FF6B00" stroke-width="3" stroke-linecap="round"/><path d="M45 22c0-4 4-4 4-8s-4-4-4-8" fill="none" stroke="#FF6B00" stroke-width="3" stroke-linecap="round"/></svg>`,
  frame: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><rect x="18" y="14" width="64" height="76" rx="2" fill="#1A1F36"/><rect x="27" y="23" width="46" height="58" fill="#F7F4EE"/><polygon points="50,38 62,58 38,58" fill="#FF6B00" opacity=".85"/><circle cx="44" cy="48" r="4" fill="#FF6B00"/></svg>`,
  tshirt: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M35 18 20 28l6 14 9-5v45h30V37l9 5 6-14-15-10a15 15 0 0 1-30 0z" fill="#1A1F36"/><polygon points="50,50 58,66 42,66" fill="#FF6B00"/></svg>`,
  box: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><polygon points="50,12 86,30 86,70 50,88 14,70 14,30" fill="#1A1F36"/><polygon points="50,12 86,30 50,48 14,30" fill="#333A63"/><polygon points="50,48 86,30 86,70 50,88" fill="#0E1224"/><polygon points="50,48 50,88 14,70 14,30" fill="#262C4A"/><rect x="45" y="12" width="10" height="76" fill="#FF6B00" opacity=".85"/></svg>`,
  trophy: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M35 20h30v20a15 15 0 0 1-30 0V20z" fill="#FF6B00"/><path d="M35 24h-10a10 10 0 0 0 10 16" fill="none" stroke="#1A1F36" stroke-width="4"/><path d="M65 24h10a10 10 0 0 1-10 16" fill="none" stroke="#1A1F36" stroke-width="4"/><rect x="46" y="52" width="8" height="16" fill="#1A1F36"/><polygon points="35,68 65,68 70,80 30,80" fill="#1A1F36"/></svg>`,
  card: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><rect x="12" y="26" width="76" height="48" rx="4" fill="#1A1F36"/><circle cx="32" cy="44" r="8" fill="#FF6B00"/><rect x="48" y="38" width="30" height="4" fill="#F7F4EE"/><rect x="48" y="48" width="24" height="4" fill="#F7F4EE" opacity=".6"/><rect x="22" y="58" width="20" height="4" fill="#F7F4EE" opacity=".6"/></svg>`,
  jacket: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M32 16 18 24l6 16 8-4v46h36V36l8 4 6-16-14-8a14 14 0 0 1-28 0z" fill="#1A1F36"/><rect x="30" y="46" width="40" height="6" fill="#FF6B00"/><rect x="30" y="62" width="40" height="6" fill="#FF6B00"/></svg>`,
  cushion: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M20 24c8 8 52 8 60 0 6 10 6 42 0 52-8 8-52 8-60 0-6-10-6-42 0-52z" fill="#1A1F36"/><path d="M20 24c4 6 8 10 10 10M80 24c-4 6-8 10-10 10M20 76c4-6 8-10 10-10M80 76c-4-6-8-10-10-10" stroke="#F7F4EE" stroke-width="2" fill="none"/><circle cx="50" cy="50" r="12" fill="#FF6B00"/></svg>`,
  keychain: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><circle cx="35" cy="28" r="14" fill="none" stroke="#1A1F36" stroke-width="6"/><rect x="42" y="44" width="24" height="40" rx="4" fill="#FF6B00"/><rect x="48" y="52" width="12" height="4" fill="#1A1F36"/><rect x="48" y="60" width="12" height="4" fill="#1A1F36"/></svg>`,
  nameplate: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><rect x="14" y="38" width="72" height="26" fill="#1A1F36"/><rect x="14" y="38" width="72" height="6" fill="#FF6B00"/><rect x="24" y="48" width="52" height="4" fill="#F7F4EE"/><rect x="34" y="56" width="32" height="3" fill="#F7F4EE" opacity=".6"/></svg>`,
  hamper: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M20 44h60l-6 38a6 6 0 0 1-6 5H32a6 6 0 0 1-6-5z" fill="#1A1F36"/><path d="M20 44l4-8h52l4 8z" fill="#333A63"/><path d="M38 36c0-12 6-20 12-20s12 8 12 20" fill="none" stroke="#FF6B00" stroke-width="4"/></svg>`,
  jersey: `<svg viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M35 18 20 28l6 14 9-5v45h30V37l9 5 6-14-15-10a15 15 0 0 1-30 0z" fill="#FF6B00"/><text x="50" y="66" text-anchor="middle" font-family="Arial" font-size="24" font-weight="700" fill="#1A1F36">7</text></svg>`,
};

const PRODUCTS = [
  { name:"Personalized Photo Mug", cat:"personal", role:"personal", vertical:"Birthday & Personal Celebrations", price:"₹249 onwards", icon:"mug" },
  { name:"Custom Name Photo Frame", cat:"personal", role:"personal", vertical:"Home Décor & Personalized Interiors", price:"₹399 onwards", icon:"frame" },
  { name:"Branded Onboarding T-Shirt", cat:"apparel", role:"business", vertical:"Employee Onboarding Kits", price:"₹199 onwards", icon:"tshirt" },
  { name:"Employee Welcome Kit Box", cat:"corporate", role:"business", vertical:"Employee Onboarding Kits", price:"₹799 onwards", icon:"box" },
  { name:"Recognition Trophy", cat:"corporate", role:"business", vertical:"Employee Gifting & Rewards", price:"₹899 onwards", icon:"trophy" },
  { name:"Wedding Invitation Card", cat:"personal", role:"personal", vertical:"Wedding Customization", price:"₹15 onwards / card", icon:"card" },
  { name:"Reflective Field Jacket", cat:"apparel", role:"business", vertical:"Industrial, Logistics & Field Workforce", price:"₹599 onwards", icon:"jacket" },
  { name:"Custom Photo Cushion", cat:"personal", role:"personal", vertical:"Home Décor & Personalized Interiors", price:"₹449 onwards", icon:"cushion" },
  { name:"Engraved Keychain Combo", cat:"corporate", role:"business", vertical:"Promotional Merchandise", price:"₹99 onwards", icon:"keychain" },
  { name:"Desk Name Plate", cat:"corporate", role:"business", vertical:"Corporate Stationery & Business Printing", price:"₹349 onwards", icon:"nameplate" },
  { name:"Festival Gift Hamper", cat:"corporate", role:"business", vertical:"Festival Corporate Gifting", price:"₹699 onwards", icon:"hamper" },
  { name:"Team Jersey with Number", cat:"apparel", role:"creator", vertical:"Sports Teams, Clubs & Communities", price:"₹449 onwards", icon:"jersey" },
  { name:"Printed Shipping Box (set of 25)", cat:"packaging", role:"business", vertical:"Packaging Customization", price:"₹249 onwards", icon:"box" },
  { name:"Retail Counter Display Card", cat:"packaging", role:"business", vertical:"Retail Branding & POSM", price:"₹199 onwards", icon:"card" },
];

const productGrid = document.getElementById("productGrid");
function renderProducts(filter){
  productGrid.innerHTML = "";
  const items = PRODUCTS.filter(p => filter === "all" || p.cat === filter);
  productGrid.toggleAttribute("data-empty", items.length === 0);
  items.forEach(p => {
    const card = document.createElement("article");
    card.className = "product-card";
    card.innerHTML = `
      <div class="product-media">
        <span class="product-badge">Customizable</span>
        ${ICONS[p.icon] || ""}
      </div>
      <div class="product-body">
        <span class="product-cat">${p.cat}</span>
        <h3>${p.name}</h3>
        <div class="product-price">${p.price}</div>
        <a class="product-cta" href="#requirement" data-role="${p.role}" data-vertical="${p.vertical}">Customize this &rarr;</a>
      </div>
    `;
    productGrid.appendChild(card);
  });
}
renderProducts("all");

document.querySelectorAll("#productFilterBar .filter-btn").forEach(btn => {
  btn.addEventListener("click", () => {
    document.querySelectorAll("#productFilterBar .filter-btn").forEach(b => { b.classList.remove("is-active"); b.setAttribute("aria-selected","false"); });
    btn.classList.add("is-active");
    btn.setAttribute("aria-selected","true");
    renderProducts(btn.dataset.pfilter);
  });
});

/* ---------------- 3. Verticals catalogue render ---------------- */
const grid = document.getElementById("verticalGrid");
function renderVerticals(filter){
  grid.innerHTML = "";
  VERTICALS.forEach(v => {
    if (filter !== "all" && v.buyer !== filter) return;
    const card = document.createElement("article");
    card.className = "vertical-card";
    card.innerHTML = `
      <span class="v-price">${v.price}</span>
      <span class="v-tag">${v.buyer === "Both" ? "Business & Personal" : v.buyer === "B2B" ? "Business" : "Personal"}</span>
      <h3>${v.name}</h3>
      <p>${v.desc}</p>
      <a class="v-link" href="#requirement" data-role="${v.role}" data-vertical="${v.name}">Get a quote &rarr;</a>
    `;
    grid.appendChild(card);
  });
}
renderVerticals("all");

document.querySelectorAll(".filter-btn").forEach(btn => {
  btn.addEventListener("click", () => {
    document.querySelectorAll(".filter-btn").forEach(b => { b.classList.remove("is-active"); b.setAttribute("aria-selected","false"); });
    btn.classList.add("is-active");
    btn.setAttribute("aria-selected","true");
    renderVerticals(btn.dataset.filter);
  });
});

/* ---------------- 4. Wizard state ---------------- */
const state = { role:null, vertical:null, quantity:"", date:"", description:"", name:"", company:"", email:"", phone:"", city:"" };

function goToStep(step){
  document.querySelectorAll(".wizard-step").forEach(p => p.classList.toggle("is-active", Number(p.dataset.stepPanel) === step));
  document.querySelectorAll(".prog-step").forEach(p => {
    const n = Number(p.dataset.progress);
    p.classList.toggle("is-active", n === step);
    p.classList.toggle("is-done", n < step);
  });
  document.getElementById("wizard").dataset.step = step;
  document.getElementById("wizard").scrollIntoView({ behavior:"smooth", block:"start" });
}

function renderVerticalOptions(role){
  const container = document.getElementById("verticalOptions");
  container.innerHTML = "";
  VERTICALS.filter(v => v.role === role || (role !== "personal" && v.buyer === "Both")).forEach(v => {
    const btn = document.createElement("button");
    btn.className = "option-card";
    btn.dataset.vertical = v.name;
    btn.innerHTML = `<strong>${v.name}</strong><span>${v.price}</span>`;
    btn.addEventListener("click", () => {
      state.vertical = v.name;
      document.querySelectorAll("#verticalOptions .option-card").forEach(o => o.classList.remove("is-selected"));
      btn.classList.add("is-selected");
      goToStep(3);
    });
    container.appendChild(btn);
  });
}

// Step 1: role selection
document.querySelectorAll("#roleOptions .option-card").forEach(btn => {
  btn.addEventListener("click", () => {
    state.role = btn.dataset.role;
    document.querySelectorAll("#roleOptions .option-card").forEach(o => o.classList.remove("is-selected"));
    btn.classList.add("is-selected");
    renderVerticalOptions(state.role);
    goToStep(2);
  });
});

// Shortcut links anywhere on the page (use-case list, vertical cards) that jump straight in
document.body.addEventListener("click", (e) => {
  const link = e.target.closest("[data-role][data-vertical]");
  if (!link) return;
  state.role = link.dataset.role;
  state.vertical = link.dataset.vertical;
  renderVerticalOptions(state.role);
  goToStep(3);
});

// Back buttons
document.querySelectorAll(".wizard-back").forEach(btn => {
  btn.addEventListener("click", () => goToStep(Number(btn.dataset.back)));
});

// Step 3 -> 4
document.querySelector('[data-next="4"]').addEventListener("click", () => {
  state.quantity = document.getElementById("fieldQuantity").value.trim();
  state.date = document.getElementById("fieldDate").value;
  state.description = document.getElementById("fieldDescription").value.trim();
  goToStep(4);
});

// Step 4 -> 5 (review)
document.getElementById("reviewBtn").addEventListener("click", () => {
  state.name = document.getElementById("fieldName").value.trim();
  state.company = document.getElementById("fieldCompany").value.trim();
  state.email = document.getElementById("fieldEmail").value.trim();
  state.phone = document.getElementById("fieldPhone").value.trim();
  state.city = document.getElementById("fieldCity").value.trim();

  if (!state.name || !state.email) {
    alert("Please share at least your name and email so we can send the quotation.");
    return;
  }
  buildReview();
  goToStep(5);
});

function buildReview(){
  const rows = [
    ["Role", state.role || "—"],
    ["Vertical", state.vertical || "—"],
    ["Quantity", state.quantity || "Not specified"],
    ["Needed by", state.date || "Not specified"],
    ["Details", state.description || "—"],
    ["Name", state.name],
    ["Company", state.company || "—"],
    ["Email", state.email],
    ["Phone", state.phone || "—"],
    ["City", state.city || "—"],
  ];
  const box = document.getElementById("reviewBox");
  box.innerHTML = "<dl>" + rows.map(([k,v]) => `<dt>${k}</dt><dd>${escapeHtml(v)}</dd>`).join("") + "</dl>";

  const messageBody = buildMessageText();

  const subject = encodeURIComponent(`New enquiry — ${state.vertical || "PrintCraft requirement"}`);
  document.getElementById("sendEmailBtn").href =
    `mailto:${COMPANY_EMAIL}?subject=${subject}&body=${encodeURIComponent(messageBody)}`;

  document.getElementById("sendWhatsappBtn").href =
    `https://wa.me/${COMPANY_PHONE}?text=${encodeURIComponent(messageBody)}`;

  document.getElementById("copyBtn").onclick = () => {
    navigator.clipboard.writeText(messageBody).then(() => {
      const note = document.getElementById("copyConfirm");
      note.hidden = false;
      setTimeout(() => { note.hidden = true; }, 3000);
    });
  };
}

function buildMessageText(){
  return [
    `New PrintCraft enquiry`,
    ``,
    `Role: ${state.role || "-"}`,
    `Vertical: ${state.vertical || "-"}`,
    `Quantity / order size: ${state.quantity || "Not specified"}`,
    `Needed by: ${state.date || "Not specified"}`,
    `Details: ${state.description || "-"}`,
    ``,
    `Name: ${state.name}`,
    `Company: ${state.company || "-"}`,
    `Email: ${state.email}`,
    `Phone: ${state.phone || "-"}`,
    `City: ${state.city || "-"}`,
  ].join("\n");
}

function escapeHtml(str){
  const div = document.createElement("div");
  div.textContent = str;
  return div.innerHTML;
}

/* ---------------- 5. Facet ticker ---------------- */
const tickerTrack = document.getElementById("tickerTrack");
const tickerItems = VERTICALS.map(v => `${v.name} <b>${v.price}</b>`);
[...tickerItems, ...tickerItems].forEach(html => {
  const span = document.createElement("span");
  span.innerHTML = html;
  tickerTrack.appendChild(span);
});

/* ---------------- 6. Scroll reveal ---------------- */
const revealTargets = document.querySelectorAll(
  ".usecase-col, .engine-card, .vertical-card, .product-card, .flow li, .wizard, section > .wrap > h2, section > .wrap > .section-intro"
);
revealTargets.forEach((el, i) => {
  el.classList.add("reveal", "reveal-stagger");
  el.style.setProperty("--stagger", i % 8);
});

const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting){
      entry.target.classList.add("in-view");
      revealObserver.unobserve(entry.target);
    }
  });
}, { threshold: 0.12, rootMargin: "0px 0px -40px 0px" });

revealTargets.forEach(el => revealObserver.observe(el));

/* ---------------- 7. Count-up hero stats ---------------- */
function animateCount(el){
  const raw = el.textContent.trim();
  const match = raw.match(/[\d,]+/);
  if (!match) return; // non-numeric stat (e.g. ranges), leave as-is
  const target = parseInt(match[0].replace(/,/g, ""), 10);
  const prefix = raw.slice(0, match.index);
  const suffix = raw.slice(match.index + match[0].length);
  const duration = 1200;
  const start = performance.now();
  function tick(now){
    const progress = Math.min((now - start) / duration, 1);
    const eased = 1 - Math.pow(1 - progress, 3);
    const value = Math.round(target * eased);
    el.textContent = `${prefix}${value.toLocaleString("en-IN")}${suffix}`;
    if (progress < 1) requestAnimationFrame(tick);
  }
  requestAnimationFrame(tick);
}
const statObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting){
      entry.target.querySelectorAll(".hero-stats strong").forEach(animateCount);
      statObserver.unobserve(entry.target);
    }
  });
}, { threshold: 0.4 });
const heroStatsEl = document.querySelector(".hero-stats");
if (heroStatsEl) statObserver.observe(heroStatsEl);

/* ---------------- 8. Misc ---------------- */
document.getElementById("year").textContent = new Date().getFullYear();

// Mobile nav toggle
const navToggle = document.getElementById("navToggle");
const siteNav = document.querySelector(".site-nav");
navToggle.addEventListener("click", () => {
  const open = siteNav.style.display === "flex";
  siteNav.style.display = open ? "none" : "flex";
  siteNav.style.flexDirection = "column";
  siteNav.style.position = "absolute";
  siteNav.style.top = "64px";
  siteNav.style.left = "0";
  siteNav.style.right = "0";
  siteNav.style.background = "var(--surface)";
  siteNav.style.padding = "16px 24px";
  siteNav.style.borderBottom = "1px solid var(--line)";
  navToggle.setAttribute("aria-expanded", String(!open));
});

</script>
</body>
</html>
