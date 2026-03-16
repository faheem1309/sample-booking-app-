<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Bookr – README</title>
  <style>
    /* ── Reset & Base ── */
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
      font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
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
    }
    pre code { background: none; border: none; padding: 0; }
    h1 { font-size: 2rem; font-weight: 700; border-bottom: 1px solid #d0d7de; padding-bottom: 10px; margin-bottom: 16px; }
    h2 { font-size: 1.4rem; font-weight: 700; border-bottom: 1px solid #d0d7de; padding-bottom: 8px; margin-top: 36px; margin-bottom: 14px; }
    h3 { font-size: 1.1rem; font-weight: 700; margin-top: 24px; margin-bottom: 10px; }
    p { margin-bottom: 14px; }
    ul, ol { padding-left: 2em; margin-bottom: 14px; }
    li { margin-bottom: 6px; }
    table { width: 100%; border-collapse: collapse; margin-bottom: 20px; }
    th, td { border: 1px solid #d0d7de; padding: 8px 14px; text-align: left; font-size: 0.95em; }
    th { background: #f6f8fa; font-weight: 600; }
    tr:nth-child(even) td { background: #f6f8fa; }
    blockquote {
      border-left: 4px solid #d0d7de;
      color: #57606a;
      padding: 8px 16px;
      margin: 0 0 16px;
      background: #f6f8fa;
      border-radius: 0 6px 6px 0;
    }

    /* ── Badge / Sticker rows ── */
    .badges { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 18px; }
    .badges img { height: 28px; border-radius: 4px; }
    .badges a { display: inline-flex; align-items: center; }

    /* ── Hero banner ── */
    .hero {
      background: linear-gradient(135deg, #0f0e0c 0%, #2c2622 100%);
      border-radius: 12px;
      padding: 40px 32px;
      text-align: center;
      margin-bottom: 32px;
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
    .hero-title {
      font-size: 3.5rem;
      font-weight: 900;
      letter-spacing: -0.03em;
      color: #ffffff;
      margin-bottom: 6px;
    }
    .hero-title span { color: #c9572a; }
    .hero-sub {
      color: rgba(255,255,255,0.65);
      font-size: 1.05rem;
      margin-bottom: 24px;
    }
    .hero-links { display: flex; justify-content: center; gap: 12px; flex-wrap: wrap; }
    .hero-links img { height: 32px; border-radius: 6px; }

    /* ── Feature grid ── */
    .feature-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 14px;
      margin-bottom: 20px;
    }
    .feature-card {
      border: 1px solid #d0d7de;
      border-radius: 8px;
      padding: 14px 16px;
      background: #f6f8fa;
    }
    .feature-card .icon { font-size: 1.4rem; margin-bottom: 6px; }
    .feature-card h4 { font-size: 0.9rem; font-weight: 700; margin-bottom: 4px; }
    .feature-card p { font-size: 0.82rem; color: #57606a; margin: 0; }

    /* ── Screenshot placeholder ── */
    .screenshot {
      background: linear-gradient(135deg, #f5f0e8 0%, #e8dfc8 100%);
      border: 1px solid #d0d7de;
      border-radius: 10px;
      padding: 48px 32px;
      text-align: center;
      margin-bottom: 20px;
      color: #57606a;
      font-size: 0.9rem;
    }
    .screenshot .app-preview {
      max-width: 520px;
      margin: 0 auto;
      background: white;
      border-radius: 8px;
      border: 1px solid #d0d7de;
      overflow: hidden;
      box-shadow: 0 4px 24px rgba(0,0,0,0.1);
    }
    .preview-bar {
      background: #f5f0e8;
      border-bottom: 1px solid #d0d7de;
      padding: 10px 16px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .dot { width: 12px; height: 12px; border-radius: 50%; }
    .preview-logo {
      font-weight: 900;
      font-size: 1.1rem;
      color: #0f0e0c;
      margin-left: auto;
      margin-right: auto;
    }
    .preview-logo span { color: #c9572a; }
    .preview-body {
      padding: 20px;
      display: flex;
      gap: 12px;
    }
    .preview-sidebar {
      width: 120px;
      flex-shrink: 0;
    }
    .preview-service {
      background: #f5f0e8;
      border-radius: 4px;
      padding: 6px 8px;
      font-size: 0.65rem;
      margin-bottom: 6px;
      border: 1px solid #d8cfc0;
    }
    .preview-service.active {
      border-color: #c9572a;
      background: white;
    }
    .preview-service .name { font-weight: 600; font-size: 0.6rem; }
    .preview-service .price { color: #2a6b4a; font-size: 0.55rem; }
    .preview-main { flex: 1; }
    .preview-cal-header {
      display: flex;
      justify-content: space-between;
      font-size: 0.6rem;
      font-weight: 700;
      margin-bottom: 6px;
      color: #0f0e0c;
    }
    .preview-days {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 2px;
    }
    .preview-day {
      aspect-ratio: 1;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.5rem;
      border-radius: 3px;
      color: #4a4540;
    }
    .preview-day.sel { background: #c9572a; color: white; font-weight: 700; }
    .preview-day.today { outline: 1px solid #c9572a; color: #c9572a; font-weight: 700; }
    .preview-day.inactive { color: #d8cfc0; }
  </style>
</head>
<body>

<!-- ══════════════════════════════════════════════════════════════════════════
     HERO
══════════════════════════════════════════════════════════════════════════ -->
<div class="hero">
  <div class="hero-title">Bookr<span>.</span></div>
  <div class="hero-sub">A clean, elegant appointment booking web application — no backend required.</div>
  <div class="hero-links">
    <!-- Live Demo badge -->
    <a href="https://sample-booking-app-gray.vercel.app/" target="_blank">
      <img src="https://img.shields.io/badge/🚀%20Live%20Demo-sample--booking--app-c9572a?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Demo"/>
    </a>
    <!-- Repo badge -->
    <a href="https://github.com/faheem1309/sample-booking-app-.git" target="_blank">
      <img src="https://img.shields.io/badge/GitHub-faheem1309%2Fsample--booking--app-24292f?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Repo"/>
    </a>
    <!-- Vercel deploy status -->
    <a href="https://sample-booking-app-gray.vercel.app/" target="_blank">
      <img src="https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Deployed on Vercel"/>
    </a>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     STATUS BADGES
══════════════════════════════════════════════════════════════════════════ -->
<div class="badges">
  <img src="https://img.shields.io/badge/Status-Live-2a6b4a?style=flat-square&logo=statuspal&logoColor=white" alt="Status: Live"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-c8a94a?style=flat-square" alt="Version 1.0.0"/>
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License MIT"/>
  <img src="https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square" alt="PRs Welcome"/>
  <img src="https://img.shields.io/badge/Maintained-Yes-2a6b4a?style=flat-square" alt="Maintained: Yes"/>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     TECH STACK
══════════════════════════════════════════════════════════════════════════ -->
<h2>🛠️ Tech Stack</h2>
<div class="badges">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/Google%20Fonts-4285F4?style=for-the-badge&logo=google-fonts&logoColor=white" alt="Google Fonts"/>
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel"/>
  <img src="https://img.shields.io/badge/GitHub-24292f?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
</div>

<blockquote>
  <strong>Zero dependencies.</strong> No frameworks, no npm, no build step — just open the HTML file in any browser and it works.
</blockquote>

<!-- ══════════════════════════════════════════════════════════════════════════
     ABOUT
══════════════════════════════════════════════════════════════════════════ -->
<h2>📖 About the Project</h2>

<div class="screenshot">
  <div class="app-preview">
    <div class="preview-bar">
      <div class="dot" style="background:#ff5f57"></div>
      <div class="dot" style="background:#febc2e"></div>
      <div class="dot" style="background:#28c840"></div>
      <div class="preview-logo">Bookr<span>.</span></div>
    </div>
    <div class="preview-body">
      <div class="preview-sidebar">
        <div style="font-size:0.55rem;font-weight:700;letter-spacing:0.1em;color:#7a746e;margin-bottom:6px;text-transform:uppercase">Services</div>
        <div class="preview-service active"><div class="name">Consultation</div><div class="price">Free · 30 min</div></div>
        <div class="preview-service"><div class="name">Full Session</div><div class="price">$95 · 60 min</div></div>
        <div class="preview-service"><div class="name">Deep Dive</div><div class="price">$140 · 90 min</div></div>
        <div class="preview-service"><div class="name">Follow-up</div><div class="price">$45 · 20 min</div></div>
      </div>
      <div class="preview-main">
        <div class="preview-cal-header">
          <span>&#8592;</span><span>March 2026</span><span>&#8594;</span>
        </div>
        <div class="preview-days">
          <div class="preview-day inactive">Su</div><div class="preview-day inactive">Mo</div><div class="preview-day inactive">Tu</div><div class="preview-day inactive">We</div><div class="preview-day inactive">Th</div><div class="preview-day inactive">Fr</div><div class="preview-day inactive">Sa</div>
          <div class="preview-day inactive"></div><div class="preview-day inactive"></div><div class="preview-day inactive"></div><div class="preview-day inactive"></div><div class="preview-day inactive"></div><div class="preview-day inactive">1</div><div class="preview-day inactive">2</div>
          <div class="preview-day inactive">3</div><div class="preview-day inactive">4</div><div class="preview-day inactive">5</div><div class="preview-day inactive">6</div><div class="preview-day inactive">7</div><div class="preview-day inactive">8</div><div class="preview-day inactive">9</div>
          <div class="preview-day inactive">10</div><div class="preview-day inactive">11</div><div class="preview-day inactive">12</div><div class="preview-day inactive">13</div><div class="preview-day inactive">14</div><div class="preview-day inactive">15</div><div class="preview-day today">16</div>
          <div class="preview-day inactive">17</div><div class="preview-day inactive">18</div><div class="preview-day">19</div><div class="preview-day">20</div><div class="preview-day sel">21</div><div class="preview-day">22</div><div class="preview-day inactive">23</div>
          <div class="preview-day inactive">24</div><div class="preview-day inactive">25</div><div class="preview-day">26</div><div class="preview-day">27</div><div class="preview-day">28</div><div class="preview-day">29</div><div class="preview-day inactive">30</div>
          <div class="preview-day inactive">31</div>
        </div>
      </div>
    </div>
  </div>
  <p style="margin-top:12px;font-size:0.8rem">↑ Bookr UI preview — service selection + calendar picker</p>
</div>

<p>
  <strong>Bookr</strong> is a fully client-side appointment booking web application delivered as a <em>single HTML file</em>.
  It provides a complete, polished booking experience — from browsing services and choosing a provider, to picking a date &amp; time slot and confirming an appointment — with zero backend, zero build tools, and zero dependencies.
</p>
<p>
  Built with an editorial design aesthetic (warm cream tones, Playfair Display serif headings, terracotta accents), Bookr is ideal for freelancers, consultants, clinics, coaching businesses, and any service provider needing a lightweight self-serve booking solution.
</p>

<!-- ══════════════════════════════════════════════════════════════════════════
     QUICK LINKS
══════════════════════════════════════════════════════════════════════════ -->
<h2>🔗 Quick Links</h2>
<div class="badges">
  <a href="https://sample-booking-app-gray.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/▶%20View%20Live%20Demo-sample--booking--app--gray.vercel.app-c9572a?style=for-the-badge&logo=vercel&logoColor=white" alt="View Live Demo"/>
  </a>
  <a href="https://github.com/faheem1309/sample-booking-app-.git" target="_blank">
    <img src="https://img.shields.io/badge/⭐%20Star%20on%20GitHub-faheem1309-24292f?style=for-the-badge&logo=github&logoColor=white" alt="Star on GitHub"/>
  </a>
  <a href="https://github.com/faheem1309/sample-booking-app-/issues" target="_blank">
    <img src="https://img.shields.io/badge/🐛%20Report%20Bug-Issues-e74c3c?style=for-the-badge&logo=github&logoColor=white" alt="Report Bug"/>
  </a>
  <a href="https://github.com/faheem1309/sample-booking-app-/fork" target="_blank">
    <img src="https://img.shields.io/badge/🍴%20Fork%20Repo-Fork-2a6b4a?style=for-the-badge&logo=github&logoColor=white" alt="Fork Repo"/>
  </a>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     FEATURES
══════════════════════════════════════════════════════════════════════════ -->
<h2>✨ Features</h2>
<div class="feature-grid">
  <div class="feature-card">
    <div class="icon">🗂️</div>
    <h4>Service Selection</h4>
    <p>4 configurable services with duration and pricing — active state indicator included.</p>
  </div>
  <div class="feature-card">
    <div class="icon">👥</div>
    <h4>Staff / Provider Picker</h4>
    <p>Choose your preferred provider. Each staff member has independent slot availability.</p>
  </div>
  <div class="feature-card">
    <div class="icon">📅</div>
    <h4>Interactive Calendar</h4>
    <p>Monthly grid with past/weekend blocking, today highlight, and available day indicators.</p>
  </div>
  <div class="feature-card">
    <div class="icon">🕐</div>
    <h4>Time Slot Picker</h4>
    <p>AM/PM slots with pre-booked slots shown as strikethrough and non-selectable.</p>
  </div>
  <div class="feature-card">
    <div class="icon">📋</div>
    <h4>Booking Summary Bar</h4>
    <p>Animated sticky panel showing service, provider, date, time and price at a glance.</p>
  </div>
  <div class="feature-card">
    <div class="icon">✅</div>
    <h4>Confirmation Modal</h4>
    <p>Contact form with validation + animated success screen upon booking confirmation.</p>
  </div>
  <div class="feature-card">
    <div class="icon">📌</div>
    <h4>Appointments Manager</h4>
    <p>View and cancel your upcoming bookings from the Upcoming tab.</p>
  </div>
  <div class="feature-card">
    <div class="icon">📱</div>
    <h4>Fully Responsive</h4>
    <p>Works seamlessly on desktop, tablet, and mobile with a single-column layout on small screens.</p>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     GETTING STARTED
══════════════════════════════════════════════════════════════════════════ -->
<h2>🚀 Getting Started</h2>

<h3>Option 1 — Open directly (recommended)</h3>
<p>No installation required. Just download and open in your browser:</p>
<pre><code># Clone the repository
git clone https://github.com/faheem1309/sample-booking-app-.git

# Navigate into it
cd sample-booking-app-

# Open the HTML file
open index.html   # macOS
start index.html  # Windows
xdg-open index.html  # Linux</code></pre>

<h3>Option 2 — Serve locally</h3>
<pre><code># Using Python
python -m http.server 8080

# Using Node.js (npx)
npx serve .</code></pre>

<h3>Option 3 — View live</h3>
<p>The app is already deployed on Vercel:</p>
<div class="badges">
  <a href="https://sample-booking-app-gray.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/Open%20Live%20App%20→-sample--booking--app--gray.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Open Live App"/>
  </a>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     PROJECT STRUCTURE
══════════════════════════════════════════════════════════════════════════ -->
<h2>📂 Project Structure</h2>
<pre><code>sample-booking-app/
│
├── index.html          # ← Entire application (HTML + CSS + JS in one file)
│
├── README.md           # Project documentation
│
└── (no build files)    # Zero dependencies, no package.json needed</code></pre>

<table>
  <thead>
    <tr><th>Section in <code>index.html</code></th><th>Contents</th><th>~Lines</th></tr>
  </thead>
  <tbody>
    <tr><td><code>&lt;head&gt;</code></td><td>Google Fonts import + full CSS styles</td><td>~400</td></tr>
    <tr><td><code>&lt;body&gt; HTML</code></td><td>Header, tabs, sidebar, main, booking panel, modal</td><td>~120</td></tr>
    <tr><td><code>&lt;script&gt; JS</code></td><td>Data arrays, state, render functions, event handlers</td><td>~180</td></tr>
  </tbody>
</table>

<!-- ══════════════════════════════════════════════════════════════════════════
     TECH DEEP DIVE
══════════════════════════════════════════════════════════════════════════ -->
<h2>⚙️ Technology Details</h2>
<table>
  <thead>
    <tr><th>Technology</th><th>Badge</th><th>Usage</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>HTML5</strong></td>
      <td><img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5"/></td>
      <td>Semantic document structure, single-file architecture</td>
    </tr>
    <tr>
      <td><strong>CSS3</strong></td>
      <td><img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3"/></td>
      <td>Custom properties (variables), Grid, Flexbox, animations, transitions, responsive media queries</td>
    </tr>
    <tr>
      <td><strong>JavaScript ES6+</strong></td>
      <td><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"/></td>
      <td>State management, DOM rendering, event handling, calendar logic</td>
    </tr>
    <tr>
      <td><strong>Google Fonts</strong></td>
      <td><img src="https://img.shields.io/badge/Google%20Fonts-4285F4?style=flat-square&logo=google-fonts&logoColor=white" alt="Google Fonts"/></td>
      <td>Playfair Display (headings) + DM Sans (body text)</td>
    </tr>
    <tr>
      <td><strong>Vercel</strong></td>
      <td><img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel"/></td>
      <td>Static site hosting &amp; continuous deployment from GitHub</td>
    </tr>
    <tr>
      <td><strong>GitHub</strong></td>
      <td><img src="https://img.shields.io/badge/GitHub-24292f?style=flat-square&logo=github&logoColor=white" alt="GitHub"/></td>
      <td>Version control, repository hosting</td>
    </tr>
  </tbody>
</table>

<!-- ══════════════════════════════════════════════════════════════════════════
     DESIGN SYSTEM
══════════════════════════════════════════════════════════════════════════ -->
<h2>🎨 Design System</h2>
<table>
  <thead>
    <tr><th>Token</th><th>Hex</th><th>Usage</th></tr>
  </thead>
  <tbody>
    <tr><td><code>--accent</code></td><td><code>#C9572A</code> 🟠</td><td>Primary CTAs, active states, highlights</td></tr>
    <tr><td><code>--accent2</code></td><td><code>#2A6B4A</code> 🟢</td><td>Prices, confirmed badges, secondary actions</td></tr>
    <tr><td><code>--cream</code></td><td><code>#F5F0E8</code> 🟡</td><td>Main background</td></tr>
    <tr><td><code>--ink</code></td><td><code>#0F0E0C</code> ⚫</td><td>Primary text</td></tr>
    <tr><td><code>--border</code></td><td><code>#D8CFC0</code> ⬜</td><td>Dividers, card borders</td></tr>
  </tbody>
</table>
<p><strong>Fonts:</strong> <code>Playfair Display</code> (display/headings) · <code>DM Sans</code> (body/UI)</p>

<!-- ══════════════════════════════════════════════════════════════════════════
     ROADMAP
══════════════════════════════════════════════════════════════════════════ -->
<h2>🗺️ Roadmap</h2>
<ul>
  <li>✅ <strong>v1.0</strong> — Static booking UI, service/staff/date/time selection, modal confirmation, appointments tab</li>
  <li>🔲 <strong>v1.1</strong> — <code>localStorage</code> persistence for bookings across sessions</li>
  <li>🔲 <strong>v1.2</strong> — Email confirmation via EmailJS</li>
  <li>🔲 <strong>v2.0</strong> — Node.js + MongoDB backend with real-time availability</li>
  <li>🔲 <strong>v2.1</strong> — Stripe / Razorpay payment integration</li>
  <li>🔲 <strong>v2.2</strong> — Google Calendar two-way sync</li>
  <li>🔲 <strong>v3.0</strong> — Multi-tenant white-labelled SaaS platform</li>
</ul>

<!-- ══════════════════════════════════════════════════════════════════════════
     CONTRIBUTING
══════════════════════════════════════════════════════════════════════════ -->
<h2>🤝 Contributing</h2>
<p>Contributions, issues, and feature requests are welcome!</p>
<ol>
  <li>Fork the repository — <a href="https://github.com/faheem1309/sample-booking-app-/fork" target="_blank">click here to fork</a></li>
  <li>Create your feature branch: <code>git checkout -b feature/AmazingFeature</code></li>
  <li>Commit your changes: <code>git commit -m 'Add some AmazingFeature'</code></li>
  <li>Push to the branch: <code>git push origin feature/AmazingFeature</code></li>
  <li>Open a Pull Request</li>
</ol>

<div class="badges">
  <a href="https://github.com/faheem1309/sample-booking-app-/issues" target="_blank">
    <img src="https://img.shields.io/badge/🐛%20Open%20an%20Issue-GitHub%20Issues-e74c3c?style=for-the-badge&logo=github&logoColor=white" alt="Open an Issue"/>
  </a>
  <a href="https://github.com/faheem1309/sample-booking-app-/fork" target="_blank">
    <img src="https://img.shields.io/badge/🍴%20Fork%20this%20Repo-GitHub-24292f?style=for-the-badge&logo=github&logoColor=white" alt="Fork this Repo"/>
  </a>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     LICENSE
══════════════════════════════════════════════════════════════════════════ -->
<h2>📝 License</h2>
<p>
  Distributed under the <strong>MIT License</strong>. See
  <a href="https://github.com/faheem1309/sample-booking-app-/blob/main/LICENSE" target="_blank"><code>LICENSE</code></a>
  for more information.
</p>
<div class="badges">
  <img src="https://img.shields.io/badge/License-MIT-2a6b4a?style=flat-square" alt="MIT License"/>
</div>

<!-- ══════════════════════════════════════════════════════════════════════════
     AUTHOR
══════════════════════════════════════════════════════════════════════════ -->
<h2>👤 Author</h2>
<div class="badges">
  <a href="https://github.com/faheem1309" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-faheem1309-24292f?style=for-the-badge&logo=github&logoColor=white" alt="GitHub: faheem1309"/>
  </a>
  <a href="https://skillversetechnologies.talentlms.com" target="_blank">
    <img src="https://img.shields.io/badge/🎓%20Skillverse%20Technologies-Learning%20Portal-c9572a?style=for-the-badge" alt="Skillverse Technologies"/>
  </a>
</div>
<p style="margin-top:12px">
  Made with ❤️ by <strong>Faheem</strong> · <a href="https://skillversetechnologies.talentlms.com" target="_blank">Skillverse Technologies</a>
</p>

<hr/>

<p style="text-align:center;color:#57606a;font-size:0.85rem">
  ⭐ If you found this project helpful, consider giving it a star on
  <a href="https://github.com/faheem1309/sample-booking-app-.git" target="_blank">GitHub</a>!
</p>

</body>
</html>
