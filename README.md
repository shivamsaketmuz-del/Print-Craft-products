
Claude finished the response

Customization, Merchandise & Branded Experience Company Your company can serve corporates, SMEs, startups, event agencies, retailers, schools, creators, families, and individual customers for almost every physical customization requirement. There is no fixed upper limit on the number of products.

pasted

create a github code for a website which job is to provide below service to the customers. Also create a flow in the website itself to collect the requirement. My company email id is "info@printcraftproducts.com" & Contact detail is "+91 8210-7018668". Founder & CEO name is "Ruchi Singh".


Architected interactive dataset with filtering, wizard flow, and contact integration features
Architected interactive dataset with filtering, wizard flow, and contact integration features
Now let me create a README for the GitHub repo and quickly test the site renders correctly.


Created a file, ran a command
Created a file, ran a command

Create README for the GitHub repository
README.md
I should run a quick syntax check to catch any obvious errors like mismatched brackets in the code, probably using Node if it's available or falling back to Python's JSON validator.


Check script.js for syntax errors

Script
Done
Good, the JS checks out. Now let's copy everything to outputs and set up a git repo so it's ready to push to GitHub.


Ran a command, read a file
Ran a command, read a file
It's built. Here's what's in it:

Design — violet/gold palette with a diamond-facet motif (diagonal cut corners on every card, button, and section) tying back to your PrintCraft gem wordmark. Space Grotesk for headings, Manrope for body, IBM Plex Mono for labels.

Sections — hero, "For Business / Personal / Creators" quick nav, the 5 solution engines, a filterable catalogue of all 18 verticals (filter by Business/Personal/Both), the 8-step fulfilment flow, and the requirement wizard.

The requirement-collection flow (#requirement) is a 5-step wizard:

Who it's for (Business/Personal/Creator)
Which vertical (auto-filtered from step 1)
Quantity, deadline, free-text details
Contact info (name, company, email, phone, city)
Review — generates a pre-filled mailto: to info@printcraftproducts.com, a pre-filled WhatsApp link to +91 8210-7018668, and a copy button
Every "Get a quote" link elsewhere on the page jumps straight to step 3 with role + vertical pre-selected. Founder/CEO name and contact details are in the footer.

For GitHub — since you already have a repo set up for PrintCraft, just drop these 4 files in and push:

bash
cd your-repo-folder
cp /path/to/index.html /path/to/style.css /path/to/script.js /path/to/README.md .
git add .
git commit -m "Add PrintCraft website with requirement wizard"
git push
It's a pure static site (no build step), so it'll deploy on Vercel as-is with no config changes needed.

One thing worth flagging: no backend exists yet, so submissions rely on the visitor's own email/WhatsApp app opening — if you want enquiries logged automatically (e.g. to a Google Sheet or CRM), that's a small addition to buildReview() in script.js whenever you're ready.


Index
Code · HTML 

Style
Code · CSS 

Script
JS 

Readme
Document · MD 
I have created the github repo but the page is very dull how to make it fancy


Orchestrated visual enhancements through animations, gradients, and interactive effects
Orchestrated visual enhancements through animations, gradients, and interactive effects
Let's punch up the visuals — add motion, depth, and some polish that the current flat build is missing. I'll add: scroll-reveal animations, a glowing animated hero, glassmorphism on cards, button shine effects, an infinite scrolling "facet ticker," and count-up stats.


Recalibrated request with proper parameters
Recalibrated request with proper parameters
Now let's add the button shine effect, card glow/lift on hover, and scroll-reveal utility classes:


Edited 3 files
Edited 3 files
Now let's add the reveal-on-scroll utility and a subtle background facet pattern, plus polish the option cards and wizard:


Add scroll-reveal utility classes and background facet texture
Add scroll-reveal utility classes and background facet texture
Now the ticker markup in HTML, right after the hero, plus reveal classes on key elements:


Debugging regex pattern matching and suffix handling logic
Debugging regex pattern matching and suffix handling logic
Now let's polish the wizard/option cards with a bit more depth, and add a diamond-shine hover to option cards to match the theme:


Envisioned visual enhancements through glowing borders and gold accents
Envisioned visual enhancements through glowing borders and gold accents
Now let's copy the updated files to outputs and do a final sanity check:


Ran a command, read a file
Ran a command, read a file
Here's what I added:

Animated hero — the gradient slowly drifts, the facet shapes rotate/float, and the eyebrow tag has a small pulsing diamond marker
Scrolling facet ticker — a marquee strip right under the hero, cycling through all 18 verticals with diamond dividers (pauses on hover)
Scroll-reveal — sections, cards, and the wizard now fade/slide in as you scroll, staggered slightly so groups of cards don't pop in all at once
Count-up stats — "18 / 100+ / 500–1,000+" animate upward when the hero stats come into view
Button shine sweep — a light diagonal glint sweeps across buttons on hover, plus proper drop shadows in the brand colors
Card depth — engine cards, vertical cards, and option cards now lift with a soft violet/gold-tinted shadow on hover instead of sitting flat
Wizard polish — a violet-to-gold accent bar across the top, a deeper shadow, and a small diamond mark on selected options
Subtle background texture — a faint diagonal facet pattern behind the catalogue and requirement sections, fading out toward the bottom
Everything still respects prefers-reduced-motion (all animations turn off), so it stays accessible.

To update your GitHub repo, replace the same three files (index.html, style.css, script.js) and push:

bash
cp /path/to/index.html /path/to/style.css /path/to/script.js .
git add .
git commit -m "Add motion, depth, and polish to the site"
git push
If you open it now, take a look and tell me what still feels flat — I can push further in a specific direction (more animation, a bolder color moment, real product imagery, etc.) once you've seen it live.


Index
Code · HTML 

Style
Code · CSS 

Script
JS 
consolidate all and give me one code to copy


Consolidated multiple components into unified, copyable code
Consolidated multiple components into unified, copyable code
All three files (HTML, CSS, JS) are merged into one printcraft-single-file.html — just save it as index.html in your repo and you're done, no separate style.css or script.js needed.


Printcraft single file
Code · HTML 






1-click prompts

Web access

Claude is AI and can make mistakes. Please double-check responses.


Printcraft single file · HTML
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PrintCraft — Customization, Merchandise &amp; Branded Experience Company</title>
<meta name="description" content="PrintCraft designs, sources and delivers customized merchandise, branded experiences and on-ground activation across corporate, personal and creator use cases in India.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Manrope:wght@400;500;600;700;800&family=IBM+Plex+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
/* ==========================================================================
   PrintCraft — design tokens
   Palette:  --violet-deep #2E1A56 (brand/hero)  --violet #6D3FC9 (interactive)
             --gold #C9A227 (facet accent, used sparingly) --surface #FBF9FF
             --tint #EEE8FA (alt section bg) --ink #201A33 (text) --line #DCD2F2
   Type:     Display  = Space Grotesk (faceted, geometric — the "cut" of the brand)
             Body     = Manrope
             Utility  = IBM Plex Mono (steps, labels, data)
   Signature: every card/button/section edge carries one diagonal facet-cut
              corner — a consistent nod to the diamond-gem mark, used once
              per element, never stacked.
   ========================================================================== */
 
:root{
  --violet-deep:#2E1A56;
  --violet-deep-2:#3D2470;
  --violet:#6D3FC9;
  --violet-light:#9B7AE0;
  --gold:#C9A227;
  --surface:#FBF9FF;
  --tint:#EEE8FA;
  --ink:#201A33;
  --ink-soft:#544C6B;
  --line:#DCD2F2;
  --line-dark:rgba(255,255,255,.16);
  --white:#FFFFFF;
 
  --font-display:'Space Grotesk', sans-serif;
  --font-body:'Manrope', sans-serif;
  --font-mono:'IBM Plex Mono', monospace;
 
  --facet:12px; /* corner cut size */
  --radius:2px;
  --shadow-soft: 0 20px 50px -30px rgba(46,26,86,.35);
}
 
*,*::before,*::after{ box-sizing:border-box; }
html{ scroll-behavior:smooth; }
body{
  margin:0;
  font-family:var(--font-body);
  color:var(--ink);
  background:var(--surface);
  line-height:1.55;
  -webkit-font-smoothing:antialiased;
}
img{ max-width:100%; display:block; }
a{ color:inherit; }
h1,h2,h3,h4{ font-family:var(--font-display); font-weight:600; line-height:1.15; margin:0 0 .5em; color:var(--violet-deep); }
p{ margin:0 0 1em; }
ul{ margin:0; padding:0; list-style:none; }
button{ font-family:inherit; cursor:pointer; }
:focus-visible{ outline:2px solid var(--gold); outline-offset:2px; }
 
@media (prefers-reduced-motion: reduce){
  *{ animation-duration:.001ms !important; animation-iteration-count:1 !important; transition-duration:.001ms !important; scroll-behavior:auto !important; }
}
 
.wrap{ max-width:1180px; margin:0 auto; padding:0 24px; }
 
/* facet-cut corner utility, one corner only */
.facet-cut{
  clip-path: polygon(var(--facet) 0, 100% 0, 100% 100%, 0 100%, 0 var(--facet));
}
 
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
  background:linear-gradient(100deg, transparent, rgba(255,255,255,.35) 45%, transparent 90%);
  transition:translate .5s ease;
}
.btn:hover::before{ translate:120% 0; }
.btn:hover{ transform:translateY(-2px); }
.btn-small{ padding:.75em 1.3em; font-size:.75rem; clip-path: polygon(10px 0, 100% 0, 100% 100%, 0 100%, 0 10px); }
.btn-primary{ background:var(--violet); color:#fff; box-shadow:0 10px 26px -12px rgba(109,63,201,.65); }
.btn-primary:hover{ background:var(--violet-deep); box-shadow:0 14px 30px -10px rgba(109,63,201,.75); }
.btn-ghost{ background:transparent; color:var(--violet-deep); border-color:var(--line); }
.btn-ghost:hover{ border-color:var(--violet); }
.btn-whatsapp{ background:#1E9E5A; color:#fff; box-shadow:0 10px 24px -12px rgba(30,158,90,.6); }
.btn-whatsapp:hover{ background:#177B47; }
 
/* ---------------- header ---------------- */
.site-header{ position:sticky; top:0; z-index:50; background:rgba(251,249,255,.9); backdrop-filter:blur(8px); border-bottom:1px solid var(--line); }
.header-inner{ display:flex; align-items:center; gap:28px; padding:16px 24px; }
.logo{ display:flex; align-items:center; gap:10px; text-decoration:none; margin-right:auto; }
.logo-mark{
  width:16px; height:16px; background:linear-gradient(135deg, var(--gold), var(--violet));
  clip-path: polygon(50% 0, 100% 35%, 82% 100%, 18% 100%, 0 35%);
  flex:none;
}
.logo-word{ font-family:var(--font-display); font-weight:700; letter-spacing:.08em; color:var(--violet-deep); font-size:1.05rem; }
.site-nav{ display:flex; gap:24px; font-size:.92rem; font-weight:600; }
.site-nav a{ text-decoration:none; color:var(--ink-soft); }
.site-nav a:hover{ color:var(--violet); }
.nav-toggle{ display:none; background:none; border:0; width:30px; height:22px; flex-direction:column; justify-content:space-between; padding:0; }
.nav-toggle span{ display:block; height:2px; background:var(--violet-deep); border-radius:2px; }
 
/* ---------------- hero ---------------- */
.hero{
  position:relative; overflow:hidden; color:#fff; padding:104px 0 84px;
  background:linear-gradient(160deg, var(--violet-deep) 0%, var(--violet-deep-2) 45%, var(--violet) 100%, var(--violet-deep) 160%);
  background-size:200% 200%;
  animation: heroDrift 18s ease-in-out infinite;
}
@keyframes heroDrift{ 0%,100%{ background-position:0% 0%; } 50%{ background-position:100% 60%; } }
.hero-facets{ position:absolute; inset:0; pointer-events:none; }
.facet{ position:absolute; background:linear-gradient(135deg, var(--gold), transparent 70%); filter:blur(.5px); }
.facet.f1{ width:340px; height:340px; top:-120px; right:-80px; clip-path:polygon(50% 0,100% 40%,80% 100%,20% 100%,0 40%); opacity:.2; animation: facetSpin 26s linear infinite; }
.facet.f2{ width:180px; height:180px; bottom:-60px; left:10%; clip-path:polygon(0 0,100% 20%,70% 100%,10% 80%); background:linear-gradient(135deg,#fff,transparent 70%); opacity:.1; animation: facetFloat 9s ease-in-out infinite; }
.facet.f3{ width:120px; height:120px; top:20%; left:-40px; clip-path:polygon(50% 0,100% 100%,0 100%); opacity:.15; animation: facetFloat 7s ease-in-out infinite reverse; }
.facet.f4{ width:220px; height:220px; bottom:10%; right:8%; clip-path:polygon(50% 0,100% 50%,50% 100%,0 50%); opacity:.12; background:linear-gradient(135deg,#fff,transparent 70%); animation: facetSpin 34s linear infinite reverse; }
@keyframes facetSpin{ from{ transform:rotate(0deg); } to{ transform:rotate(360deg); } }
@keyframes facetFloat{ 0%,100%{ transform:translateY(0) scale(1); } 50%{ transform:translateY(-18px) scale(1.06); } }
.hero-inner{ position:relative; max-width:780px; }
.eyebrow{ font-family:var(--font-mono); text-transform:uppercase; letter-spacing:.12em; font-size:.78rem; color:var(--gold); margin-bottom:1em; display:flex; align-items:center; gap:.6em; }
.eyebrow::before{ content:""; width:8px; height:8px; background:var(--gold); clip-path:polygon(50% 0,100% 50%,50% 100%,0 50%); animation: pulseGlow 2.4s ease-in-out infinite; }
@keyframes pulseGlow{ 0%,100%{ opacity:.5; transform:scale(.85); } 50%{ opacity:1; transform:scale(1.15); } }
.hero h1{ color:#fff; font-size:clamp(2.1rem, 4.6vw, 3.4rem); margin-bottom:.5em; text-shadow:0 20px 60px rgba(0,0,0,.25); }
.hero h1 em{ font-style:normal; background:linear-gradient(90deg, var(--gold), #f2d576 50%, var(--gold)); -webkit-background-clip:text; background-clip:text; color:transparent; }
.hero-sub{ color:rgba(255,255,255,.82); font-size:1.08rem; max-width:640px; }
.hero-cta{ display:flex; gap:16px; flex-wrap:wrap; margin:32px 0 48px; }
.hero .btn-ghost{ background:rgba(255,255,255,.06); color:#fff; border-color:rgba(255,255,255,.35); backdrop-filter:blur(6px); }
.hero .btn-ghost:hover{ border-color:var(--gold); }
.hero-stats{ display:flex; gap:40px; flex-wrap:wrap; border-top:1px solid rgba(255,255,255,.18); padding-top:28px; }
.hero-stats strong{ display:block; font-family:var(--font-display); font-size:1.6rem; color:#fff; }
.hero-stats span{ font-size:.82rem; color:rgba(255,255,255,.65); }
 
/* ---------------- facet ticker ---------------- */
.ticker{ background:var(--ink); overflow:hidden; padding:14px 0; border-bottom:1px solid rgba(255,255,255,.08); }
.ticker-track{ display:flex; gap:2.5em; white-space:nowrap; width:max-content; animation: tickerScroll 38s linear infinite; }
.ticker-track span{ font-family:var(--font-mono); font-size:.82rem; letter-spacing:.04em; color:rgba(255,255,255,.55); display:flex; align-items:center; gap:2.5em; }
.ticker-track span::after{ content:"◆"; color:var(--gold); margin-left:2.5em; font-size:.7em; }
@keyframes tickerScroll{ from{ transform:translateX(0); } to{ transform:translateX(-50%); } }
.ticker:hover .ticker-track{ animation-play-state:paused; }
 
/* ---------------- use cases ---------------- */
.usecases{ padding:80px 0 60px; }
.section-label{ font-family:var(--font-mono); text-transform:uppercase; letter-spacing:.1em; font-size:.78rem; color:var(--violet); margin-bottom:.8em; }
.section-label.light{ color:var(--gold); }
.usecase-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:32px; }
.usecase-col h3{ font-size:1.15rem; border-bottom:2px solid var(--line); padding-bottom:.5em; margin-bottom:.8em; }
.usecase-col li{ border-bottom:1px solid var(--line); }
.usecase-col a{ display:block; padding:.7em 0; text-decoration:none; color:var(--ink); font-weight:600; font-size:.95rem; transition:color .15s, padding-left .15s; }
.usecase-col a:hover{ color:var(--violet); padding-left:6px; }
 
/* ---------------- engines ---------------- */
.engines{ background:var(--violet-deep); color:#fff; padding:88px 0; }
.engines h2{ color:#fff; font-size:clamp(1.6rem,3vw,2.2rem); max-width:720px; }
.section-intro{ color:rgba(255,255,255,.75); max-width:640px; }
.engine-grid{ display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:20px; margin-top:36px; }
.engine-card{ background:rgba(255,255,255,.06); border:1px solid var(--line-dark); padding:26px 22px; clip-path: polygon(16px 0, 100% 0, 100% 100%, 0 100%, 0 16px); backdrop-filter:blur(6px); transition:transform .25s ease, background .25s ease, box-shadow .25s ease; }
.engine-card:hover{ transform:translateY(-6px); background:rgba(255,255,255,.1); box-shadow:0 24px 50px -20px rgba(0,0,0,.45), 0 0 0 1px rgba(201,162,39,.35); }
.engine-num{ font-family:var(--font-mono); color:var(--gold); font-size:.85rem; }
.engine-card h3{ color:#fff; font-size:1.05rem; margin:.5em 0 .4em; }
.engine-card p{ color:rgba(255,255,255,.68); font-size:.9rem; margin:0; }
 
/* ---------------- verticals ---------------- */
.verticals{ padding:88px 0; background:var(--tint); }
.verticals h2{ font-size:clamp(1.6rem,3vw,2.2rem); max-width:760px; }
.filter-bar{ display:flex; gap:10px; flex-wrap:wrap; margin:28px 0; }
.filter-btn{ background:#fff; border:1px solid var(--line); padding:.5em 1.1em; font-family:var(--font-mono); font-size:.78rem; text-transform:uppercase; letter-spacing:.05em; border-radius:20px; color:var(--ink-soft); }
.filter-btn.is-active, .filter-btn:hover{ background:var(--violet); color:#fff; border-color:var(--violet); }
.vertical-grid{ display:grid; grid-template-columns:repeat(auto-fill,minmax(260px,1fr)); gap:18px; }
.vertical-card{ background:#fff; border:1px solid var(--line); padding:22px; clip-path: polygon(14px 0, 100% 0, 100% 100%, 0 100%, 0 14px); transition:transform .2s ease, box-shadow .2s ease, border-color .2s ease; }
.vertical-card:hover{ transform:translateY(-5px); box-shadow:0 26px 50px -28px rgba(46,26,86,.45); border-color:var(--violet-light); }
.vertical-card .v-tag{ font-family:var(--font-mono); font-size:.7rem; text-transform:uppercase; letter-spacing:.06em; color:var(--gold); }
.vertical-card h3{ font-size:1.02rem; margin:.35em 0 .4em; }
.vertical-card p{ font-size:.87rem; color:var(--ink-soft); margin:0 0 .8em; }
.vertical-card .v-link{ font-family:var(--font-mono); font-size:.78rem; font-weight:600; color:var(--violet); text-decoration:none; }
.vertical-card .v-link:hover{ text-decoration:underline; }
.vertical-card[hidden]{ display:none; }
 
/* ---------------- how it works ---------------- */
.how{ background:var(--violet-deep-2); color:#fff; padding:88px 0; }
.how h2{ color:#fff; font-size:clamp(1.6rem,3vw,2.2rem); max-width:760px; }
.flow{ display:grid; grid-template-columns:repeat(auto-fill,minmax(230px,1fr)); gap:20px; margin:36px 0 0; padding:0; counter-reset:none; }
.flow li{ display:flex; gap:14px; background:rgba(255,255,255,.05); border:1px solid var(--line-dark); padding:20px; clip-path: polygon(12px 0, 100% 0, 100% 100%, 0 100%, 0 12px); }
.flow-step{ font-family:var(--font-mono); font-weight:700; font-size:.95rem; color:var(--violet-deep); background:var(--gold); width:28px; height:28px; border-radius:50%; display:flex; align-items:center; justify-content:center; flex:none; }
.flow h4{ color:#fff; font-size:.98rem; margin:0 0 .3em; }
.flow p{ color:rgba(255,255,255,.65); font-size:.85rem; margin:0; }
 
/* ---------------- requirement wizard ---------------- */
.requirement{ padding:88px 0; }
.requirement h2{ font-size:clamp(1.6rem,3vw,2.2rem); max-width:720px; }
.wizard{ position:relative; background:#fff; border:1px solid var(--line); margin-top:36px; padding:44px clamp(20px,4vw,52px) 40px; clip-path: polygon(24px 0, 100% 0, 100% 100%, 0 100%, 0 24px); box-shadow:0 40px 80px -40px rgba(46,26,86,.4); }
.wizard::before{ content:""; position:absolute; top:0; left:24px; right:0; height:4px; background:linear-gradient(90deg, var(--violet), var(--gold)); }
.wizard-progress{ display:flex; align-items:center; gap:0; margin-bottom:36px; }
.prog-step{ width:32px; height:32px; border-radius:50%; border:2px solid var(--line); display:flex; align-items:center; justify-content:center; font-family:var(--font-mono); font-size:.85rem; font-weight:700; color:var(--ink-soft); flex:none; background:#fff; }
.prog-step.is-active, .prog-step.is-done{ border-color:var(--violet); color:var(--violet); }
.prog-step.is-done{ background:var(--violet); color:#fff; }
.prog-line{ flex:1; height:2px; background:var(--line); margin:0 4px; }
 
.wizard-step{ display:none; }
.wizard-step.is-active{ display:block; animation:fadeIn .3s ease; }
@keyframes fadeIn{ from{ opacity:0; transform:translateY(6px);} to{ opacity:1; transform:none; } }
.wizard-step h3{ font-size:1.3rem; margin-bottom:1em; }
 
.option-grid{ display:grid; grid-template-columns:repeat(auto-fit,minmax(200px,1fr)); gap:16px; }
.option-card{ position:relative; overflow:hidden; text-align:left; background:var(--surface); border:1px solid var(--line); padding:20px; clip-path: polygon(10px 0, 100% 0, 100% 100%, 0 100%, 0 10px); display:flex; flex-direction:column; gap:.3em; transition:transform .18s ease, border-color .18s ease, box-shadow .18s ease; }
.option-card strong{ font-family:var(--font-display); color:var(--violet-deep); font-size:1.02rem; }
.option-card span{ font-size:.85rem; color:var(--ink-soft); }
.option-card:hover{ border-color:var(--violet); transform:translateY(-3px); box-shadow:0 18px 34px -22px rgba(46,26,86,.4); }
.option-card.is-selected{ border-color:var(--violet); background:var(--tint); box-shadow:inset 0 0 0 1px var(--violet), 0 18px 34px -22px rgba(46,26,86,.4); }
.option-card.is-selected::after{ content:"◆"; position:absolute; top:12px; right:14px; color:var(--violet); font-size:.75rem; }
 
.form-grid{ display:grid; grid-template-columns:1fr 1fr; gap:20px; margin-top:8px; }
.form-grid label{ display:flex; flex-direction:column; gap:.4em; font-size:.85rem; font-weight:600; color:var(--ink-soft); }
.form-grid label.full{ grid-column:1 / -1; }
.form-grid input, .form-grid textarea{
  font-family:var(--font-body); font-size:.95rem; color:var(--ink);
  border:1px solid var(--line); background:var(--surface); padding:.8em 1em; border-radius:var(--radius);
}
.form-grid input:focus, .form-grid textarea:focus{ border-color:var(--violet); outline:none; }
.wizard-actions{ display:flex; gap:12px; margin-top:28px; flex-wrap:wrap; }
.wizard-back{ margin-right:auto; }
.send-actions{ align-items:center; }
 
.review-box{ background:var(--tint); border:1px solid var(--line); padding:22px 26px; font-size:.92rem; clip-path: polygon(12px 0, 100% 0, 100% 100%, 0 100%, 0 12px); }
.review-box dl{ margin:0; display:grid; grid-template-columns:160px 1fr; gap:8px 16px; }
.review-box dt{ font-family:var(--font-mono); font-size:.78rem; text-transform:uppercase; letter-spacing:.04em; color:var(--ink-soft); }
.review-box dd{ margin:0; }
.copy-confirm{ color:var(--violet); font-family:var(--font-mono); font-size:.85rem; margin-top:10px; }
 
/* ---------------- footer ---------------- */
.site-footer{ background:var(--ink); color:rgba(255,255,255,.7); padding:64px 0 0; }
.footer-inner{ display:grid; grid-template-columns:1.4fr 1fr 1fr; gap:40px; padding-bottom:40px; border-bottom:1px solid rgba(255,255,255,.12); }
.footer-brand .logo-word{ color:#fff; }
.footer-brand p{ margin-top:14px; max-width:320px; font-size:.9rem; }
.site-footer h4{ color:#fff; font-size:.85rem; text-transform:uppercase; letter-spacing:.08em; font-family:var(--font-mono); margin-bottom:1em; }
.footer-contact p, .footer-links a{ display:block; margin-bottom:.6em; text-decoration:none; font-size:.92rem; }
.footer-contact a{ text-decoration:none; }
.footer-contact a:hover, .footer-links a:hover{ color:#fff; }
.founder{ color:var(--gold); font-weight:600; }
.footer-bottom{ padding:22px 24px; font-size:.8rem; text-align:center; color:rgba(255,255,255,.4); }
 
/* ---------------- scroll reveal ---------------- */
.reveal{ opacity:0; transform:translateY(28px); transition:opacity .7s ease, transform .7s ease; }
.reveal.in-view{ opacity:1; transform:none; }
.reveal-stagger.in-view{ transition-delay:calc(var(--stagger, 0) * 70ms); }
 
/* subtle repeating facet watermark on light sections */
.verticals, .requirement{ position:relative; }
.verticals::before, .requirement::before{
  content:""; position:absolute; inset:0; pointer-events:none; opacity:.5;
  background-image:
    linear-gradient(135deg, rgba(109,63,201,.05) 25%, transparent 25%),
    linear-gradient(225deg, rgba(109,63,201,.05) 25%, transparent 25%);
  background-size:64px 64px;
  background-position:0 0, 32px 0;
  mask-image: linear-gradient(to bottom, black, transparent 70%);
}
.verticals > .wrap, .requirement > .wrap{ position:relative; }
 
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
      <span class="logo-mark" aria-hidden="true"></span>
      <span class="logo-word">PRINTCRAFT</span>
    </a>
    <nav class="site-nav" aria-label="Primary">
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
      <span class="logo-mark" aria-hidden="true"></span>
      <span class="logo-word">PRINTCRAFT</span>
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
  { name:"Corporate Stationery & Business Printing", buyer:"B2B", role:"business",
    desc:"Business cards, letterheads, ID cards, brochures and everyday branded stationery." },
  { name:"Employee Onboarding Kits", buyer:"B2B", role:"business",
    desc:"Welcome boxes, apparel, tech accessories and ID kits for new joiners at every level." },
  { name:"Employee Gifting & Rewards", buyer:"B2B", role:"business",
    desc:"Trophies, hampers and recognition gifts for birthdays, anniversaries and milestones." },
  { name:"Festival Corporate Gifting", buyer:"B2B", role:"business",
    desc:"Diwali, Christmas and regional festival hampers, sweet boxes and branded packaging." },
  { name:"Corporate Events & Conferences", buyer:"B2B", role:"business",
    desc:"Complete delegate kits, stage branding, badges and souvenirs for a full event." },
  { name:"On-Ground Marketing / BTL Activation", buyer:"B2B", role:"business",
    desc:"Canopies, standees, FOS kits, vehicle branding and field-activation merchandise." },
  { name:"Retail Branding & POSM", buyer:"B2B", role:"business",
    desc:"Shelf strips, displays, floor and window graphics for multi-store rollouts." },
  { name:"Customized Apparel & Uniforms", buyer:"Both", role:"business",
    desc:"T-shirts, uniforms and workwear across screen print, DTF, embroidery and sublimation." },
  { name:"Promotional Merchandise", buyer:"B2B", role:"business",
    desc:"Pens, bottles, bags and tech accessories for giveaways, incentives and loyalty programs." },
  { name:"Packaging Customization", buyer:"B2B", role:"business",
    desc:"Shipping boxes, labels, stickers and inserts for D2C and marketplace sellers." },
  { name:"Wedding Customization", buyer:"B2C", role:"personal",
    desc:"Invitations, welcome boards, hampers, return gifts and everything in between." },
  { name:"Birthday & Personal Celebrations", buyer:"B2C", role:"personal",
    desc:"Banners, return gifts, photo products and personalized decoration kits." },
  { name:"Home Décor & Personalized Interiors", buyer:"B2C", role:"personal",
    desc:"Photo frames, canvas prints, name plates and personalized home accents." },
  { name:"Schools & Colleges", buyer:"B2B", role:"business",
    desc:"ID cards, uniforms, annual-day merchandise, yearbooks and graduation products." },
  { name:"Sports Teams, Clubs & Communities", buyer:"Both", role:"creator",
    desc:"Jerseys, medals, trophies and fan merchandise for teams and community groups." },
  { name:"Creator & Influencer Merchandise", buyer:"B2B", role:"creator",
    desc:"Print-on-demand apparel and accessories, from storefront to fulfilment." },
  { name:"Hospitality, Restaurants & Hotels", buyer:"B2B", role:"business",
    desc:"Menus, staff uniforms, room signage and branded packaging for guest experience." },
  { name:"Industrial, Logistics & Field Workforce", buyer:"B2B", role:"business",
    desc:"Reflective jackets, safety gear, ID kits and signage for field and warehouse teams." },
];
 
const grid = document.getElementById("verticalGrid");
function renderVerticals(filter){
  grid.innerHTML = "";
  VERTICALS.forEach(v => {
    if (filter !== "all" && v.buyer !== filter) return;
    const card = document.createElement("article");
    card.className = "vertical-card";
    card.innerHTML = `
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
 
/* ---------------- 2. Wizard state ---------------- */
const state = { role:null, vertical:null, quantity:"", date:"", description:"", name:"", company:"", email:"", phone:"", city:"" };
 
const VERTICALS_BY_ROLE = {
  business: VERTICALS.filter(v => v.role === "business" || v.buyer === "Both").map(v => v.name),
  personal: VERTICALS.filter(v => v.role === "personal").map(v => v.name),
  creator:  VERTICALS.filter(v => v.role === "creator" || v.buyer === "Both").map(v => v.name),
};
 
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
  (VERTICALS_BY_ROLE[role] || []).forEach(name => {
    const btn = document.createElement("button");
    btn.className = "option-card";
    btn.dataset.vertical = name;
    btn.innerHTML = `<strong>${name}</strong>`;
    btn.addEventListener("click", () => {
      state.vertical = name;
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
 
/* ---------------- 3. Facet ticker ---------------- */
const tickerTrack = document.getElementById("tickerTrack");
const names = VERTICALS.map(v => v.name);
// duplicate the list once so the marquee can loop seamlessly at -50%
[...names, ...names].forEach(name => {
  const span = document.createElement("span");
  span.textContent = name;
  tickerTrack.appendChild(span);
});
 
/* ---------------- 4. Scroll reveal ---------------- */
const revealTargets = document.querySelectorAll(
  ".usecase-col, .engine-card, .vertical-card, .flow li, .wizard, section > .wrap > h2, section > .wrap > .section-intro"
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
 
/* ---------------- 5. Count-up hero stats ---------------- */
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
 
/* ---------------- 6. Misc ---------------- */
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
 
