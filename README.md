<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Bookr – README</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
      font-size: 16px;
      line-height: 1.7;
      color: #24292f;
      background: #ffffff;
      max-width: 860px;
      margin: 0 auto;
      padding: 40px 24px 80px;
    }
    a { color: #0969da; text-decoration: none; }
    a:hover { text-decoration: underline; }
    hr { border: none; border-top: 1px solid #d0d7de; margin: 32px 0; }
    code {
      font-family: "SFMono-Regular", Consolas, monospace;
      font-size: 0.875em;
      background: #f6f8fa;
      border: 1px solid #d0d7de;
      border-radius: 6px;
      padding: 0.2em 0.4em;
    }
    pre {
      background: #f6f8fa;
      border: 1px solid #d0d7de;
      border-radius: 6px;
      padding: 16px;
      overflow-x: auto;
      font-size: 0.875em;
      line-height: 1.6;
      margin-bottom: 16px;
    }
    pre code { background: none; border: none; padding: 0; }
    h2 { font-size: 1.4rem; font-weight: 700; border-bottom: 1px solid #d0d7de; padding-bottom: 8px; margin-top: 36px; margin-bottom: 14px; }
    h3 { font-size: 1rem; font-weight: 700; margin-top: 20px; margin-bottom: 8px; }
    p { margin-bottom: 14px; }
    ul, ol { padding-left: 2em; margin-bottom: 14px; }
    li { margin-bottom: 6px; }

    /* Hero */
    .hero {
      background: linear-gradient(135deg, #0f0e0c 0%, #2c2622 100%);
      border-radius: 12px;
      padding: 40px 32px;
      text-align: center;
      margin-bottom: 28px;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(ellipse at 70% 30%, rgba(201,87,42,0.25) 0%, transparent 60%);
      pointer-events: none;
    }
    .hero-title { font-size: 3.2rem; font-weight: 900; letter-spacing: -0.03em; color: #fff; margin-bottom: 6px; }
    .hero-title span { color: #c9572a; }
    .hero-sub { color: rgba(255,255,255,0.6); font-size: 1rem; margin-bottom: 24px; }
    .hero-links { display: flex; justify-content: center; gap: 10px; flex-wrap: wrap; }
    .hero-links img { height: 30px; border-radius: 5px; }

    /* Badges */
    .badges { display: flex; flex-wrap: wrap; gap: 7px; margin-bottom: 18px; }
    .badges img { height: 26px; border-radius: 4px; }
    .badges a { display: inline-flex; align-items: center; }

    /* Features */
    .feature-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
      gap: 12px;
      margin-bottom: 20px;
    }
    .feature-card {
      border: 1px solid #d0d7de;
      border-radius: 8px;
      padding: 12px 14px;
      background: #f6f8fa;
    }
    .feature-card .icon { font-size: 1.2rem; margin-bottom: 4px; }
    .feature-card h4 { font-size: 0.88rem; font-weight: 700; margin-bottom: 3px; }
    .feature-card p { font-size: 0.8rem; color: #57606a; margin: 0; }
  </style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-title">Bookr<span>.</span></div>
  <div class="hero-sub">A clean, elegant appointment booking web app — no backend required.</div>
  <div class="hero-links">
    <a href="https://sample-booking-app-gray.vercel.app/" target="_blank">
      <img src="https://img.shields.io/badge/🚀%20Live%20Demo-Vercel-c9572a?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Demo"/>
    </a>
    <a href="https://github.com/faheem1309/sample-booking-app-.git" target="_blank">
      <img src="https://img.shields.io/badge/GitHub-faheem1309%2Fsample--booking--app-24292f?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Repo"/>
    </a>
  </div>
</div>

<!-- STATUS -->
<div class="badges">
  <img src="https://img.shields.io/badge/Status-Live-2a6b4a?style=flat-square" alt="Live"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-c8a94a?style=flat-square" alt="Version"/>
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="MIT"/>
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square" alt="PRs Welcome"/>
</div>

<!-- TECH STACK -->
<h2>🛠️ Tech Stack</h2>
<div class="badges">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/Google%20Fonts-4285F4?style=for-the-badge&logo=google-fonts&logoColor=white" alt="Google Fonts"/>
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel"/>
  <img src="https://img.shields.io/badge/GitHub-24292f?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</div>

<!-- ABOUT -->
<h2>📖 About</h2>
<p>
  <strong>Bookr</strong> is a fully client-side appointment booking app delivered as a <em>single HTML file</em> — no frameworks, no npm, no build step.
  It covers the complete booking flow: service selection → provider → date → time slot → confirmation. Ideal for freelancers, clinics, consultants, and coaches.
</p>

<!-- FEATURES -->
<h2>✨ Features</h2>
<div class="feature-grid">
  <div class="feature-card"><div class="icon">🗂️</div><h4>Service Selection</h4><p>4 services with duration & pricing.</p></div>
  <div class="feature-card"><div class="icon">👥</div><h4>Staff Picker</h4><p>Choose a provider with independent slot availability.</p></div>
  <div class="feature-card"><div class="icon">📅</div><h4>Interactive Calendar</h4><p>Past/weekend blocked, today highlighted, dots for available days.</p></div>
  <div class="feature-card"><div class="icon">🕐</div><h4>Time Slot Picker</h4><p>AM/PM slots; booked slots shown as strikethrough.</p></div>
  <div class="feature-card"><div class="icon">📋</div><h4>Booking Summary Bar</h4><p>Animated sticky panel before checkout.</p></div>
  <div class="feature-card"><div class="icon">✅</div><h4>Confirmation Modal</h4><p>Contact form + animated success screen.</p></div>
  <div class="feature-card"><div class="icon">📌</div><h4>Appointments Tab</h4><p>View and cancel upcoming bookings.</p></div>
  <div class="feature-card"><div class="icon">📱</div><h4>Fully Responsive</h4><p>Works on desktop, tablet, and mobile.</p></div>
</div>

<!-- GETTING STARTED -->
<h2>🚀 Getting Started</h2>
<h3>Clone & Open</h3>
<pre><code>git clone https://github.com/faheem1309/sample-booking-app-.git
cd sample-booking-app-
open index.html</code></pre>

<h3>Or view live →</h3>
<div class="badges">
  <a href="https://sample-booking-app-gray.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/Open%20Live%20App-sample--booking--app--gray.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Open Live App"/>
  </a>
</div>

<!-- ROADMAP -->
<h2>🗺️ Roadmap</h2>
<ul>
  <li>✅ <strong>v1.0</strong> — Complete booking UI (current)</li>
  <li>🔲 <strong>v1.1</strong> — <code>localStorage</code> persistence</li>
  <li>🔲 <strong>v1.2</strong> — Email confirmation via EmailJS</li>
  <li>🔲 <strong>v2.0</strong> — Node.js + MongoDB backend</li>
  <li>🔲 <strong>v2.1</strong> — Stripe / Razorpay payments</li>
  <li>🔲 <strong>v3.0</strong> — Multi-tenant SaaS platform</li>
</ul>

<!-- AUTHOR -->
<h2>👤 Author</h2>
<div class="badges">
  <a href="https://github.com/faheem1309" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-faheem1309-24292f?style=for-the-badge&logo=github&logoColor=white" alt="faheem1309"/>
  </a>
  <a href="https://skillversetechnologies.talentlms.com" target="_blank">
    <img src="https://img.shields.io/badge/🎓%20Skillverse%20Technologies-Portal-c9572a?style=for-the-badge" alt="Skillverse Technologies"/>
  </a>
</div>
<p style="margin-top:10px">Made with ❤️ by <strong>Faheem</strong> · <a href="https://skillversetechnologies.talentlms.com" target="_blank">Skillverse Technologies</a></p>

<hr/>
<p style="text-align:center;color:#57606a;font-size:0.82rem">⭐ If this helped you, give it a star on <a href="https://github.com/faheem1309/sample-booking-app-.git" target="_blank">GitHub</a>!</p>

</body>
</html>
