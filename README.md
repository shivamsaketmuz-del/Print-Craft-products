# Print-Craft-products

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



I am unable to 


1-click prompts

Web access

Claude is AI and can make mistakes. Please double-check responses.


Index · HTML
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
<link rel="stylesheet" href="style.css">
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
 
<script src="script.js"></script>
</body>
</html>
