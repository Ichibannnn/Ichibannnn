<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Gib Pangilinan – GitHub Profile</title>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
    :root {
      --bg: #f9f8f6;
      --surface: #ffffff;
      --surface-2: #f3f2ef;
      --border: rgba(0,0,0,0.08);
      --border-md: rgba(0,0,0,0.14);
      --text-primary: #1a1917;
      --text-secondary: #6b6862;
      --text-tertiary: #9e9992;
 
      --purple-bg: #EEEDFE;
      --purple-text: #3C3489;
      --purple-border: #AFA9EC;
      --blue-bg: #E6F1FB;
      --blue-text: #0C447C;
      --teal-bg: #E1F5EE;
      --teal-text: #085041;
      --coral-bg: #FAECE7;
      --coral-text: #712B13;
      --amber-bg: #FAEEDA;
      --amber-text: #633806;
      --pink-bg: #FBEAF0;
      --pink-text: #72243E;
 
      --radius-sm: 6px;
      --radius-md: 10px;
      --radius-lg: 14px;
      --radius-full: 999px;
 
      --font: 'DM Sans', sans-serif;
      --font-mono: 'DM Mono', monospace;
    }
 
    body {
      font-family: var(--font);
      background: var(--bg);
      color: var(--text-primary);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      padding: 2.5rem 1rem;
    }
 
    .wrapper {
      width: 100%;
      max-width: 680px;
    }
 
    /* ── Header ── */
    .header {
      display: flex;
      align-items: center;
      gap: 20px;
      margin-bottom: 1.6rem;
    }
 
    .avatar {
      width: 68px;
      height: 68px;
      border-radius: 50%;
      background: var(--purple-bg);
      border: 1.5px solid var(--purple-border);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      font-weight: 600;
      color: var(--purple-text);
      flex-shrink: 0;
      letter-spacing: 0.02em;
    }
 
    .header-info h1 {
      font-size: 22px;
      font-weight: 600;
      color: var(--text-primary);
      line-height: 1.2;
    }
 
    .header-info .role {
      font-size: 14px;
      color: var(--text-secondary);
      margin-top: 3px;
    }
 
    .header-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 10px;
    }
 
    /* ── Stat cards ── */
    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      margin-bottom: 1.6rem;
    }
 
    .stat-card {
      background: var(--surface);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-md);
      padding: 0.9rem 1rem;
      text-align: center;
    }
 
    .stat-num {
      font-size: 20px;
      font-weight: 600;
      color: var(--text-primary);
      line-height: 1;
    }
 
    .stat-lbl {
      font-size: 11px;
      color: var(--text-tertiary);
      margin-top: 5px;
      font-weight: 400;
    }
 
    /* ── Divider ── */
    .divider {
      border: none;
      border-top: 0.5px solid var(--border);
      margin: 1.4rem 0;
    }
 
    /* ── Section label ── */
    .section-label {
      font-size: 10.5px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.09em;
      color: var(--text-tertiary);
      margin-bottom: 12px;
    }
 
    /* ── About ── */
    .about-text {
      font-size: 14px;
      color: var(--text-secondary);
      line-height: 1.75;
    }
 
    .about-text strong {
      color: var(--text-primary);
      font-weight: 500;
    }
 
    /* ── Stack grid ── */
    .stack-grid {
      display: grid;
      gap: 14px;
    }
 
    .stack-row-label {
      font-size: 11.5px;
      color: var(--text-tertiary);
      margin-bottom: 6px;
    }
 
    /* ── Tags / Badges ── */
    .tag {
      display: inline-block;
      font-size: 11.5px;
      font-weight: 500;
      padding: 3px 9px;
      border-radius: var(--radius-sm);
      margin: 2px 3px 2px 0;
      font-family: var(--font);
    }
 
    .tag-purple { background: var(--purple-bg); color: var(--purple-text); }
    .tag-blue   { background: var(--blue-bg);   color: var(--blue-text); }
    .tag-teal   { background: var(--teal-bg);   color: var(--teal-text); }
    .tag-coral  { background: var(--coral-bg);  color: var(--coral-text); }
    .tag-amber  { background: var(--amber-bg);  color: var(--amber-text); }
    .tag-pink   { background: var(--pink-bg);   color: var(--pink-text); }
 
    /* ── Project card ── */
    .project-card {
      background: var(--surface);
      border: 0.5px solid var(--border);
      border-radius: var(--radius-lg);
      padding: 1.2rem 1.4rem;
    }
 
    .project-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 14px;
      margin-bottom: 12px;
    }
 
    .project-title {
      font-size: 16px;
      font-weight: 600;
      color: var(--text-primary);
    }
 
    .project-desc {
      font-size: 13px;
      color: var(--text-secondary);
      margin-top: 4px;
      line-height: 1.65;
    }
 
    .repo-btn {
      flex-shrink: 0;
      font-size: 12px;
      font-weight: 500;
      background: var(--surface-2);
      border: 0.5px solid var(--border-md);
      border-radius: var(--radius-sm);
      padding: 5px 11px;
      color: var(--text-secondary);
      text-decoration: none;
      white-space: nowrap;
      transition: background 0.15s;
    }
 
    .repo-btn:hover { background: #eae9e5; }
 
    .project-meta {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-bottom: 14px;
    }
 
    .meta-cell {
      background: var(--surface-2);
      border-radius: var(--radius-md);
      padding: 8px 11px;
    }
 
    .meta-cell-label {
      font-size: 10.5px;
      color: var(--text-tertiary);
      margin-bottom: 3px;
    }
 
    .meta-cell-value {
      font-size: 12.5px;
      font-weight: 500;
      color: var(--text-primary);
    }
 
    .project-features {
      border-top: 0.5px solid var(--border);
      padding-top: 12px;
    }
 
    .features-label {
      font-size: 10.5px;
      color: var(--text-tertiary);
      margin-bottom: 8px;
    }
 
    /* ── Footer ── */
    .footer {
      text-align: center;
      margin-top: 1.6rem;
      font-size: 12px;
      color: var(--text-tertiary);
    }
 
    /* ── Animations ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(10px); }
      to   { opacity: 1; transform: translateY(0); }
    }
 
    .wrapper > * {
      animation: fadeUp 0.4s ease both;
    }
 
    .header          { animation-delay: 0.05s; }
    .stats           { animation-delay: 0.12s; }
    .about-section   { animation-delay: 0.18s; }
    .stack-section   { animation-delay: 0.24s; }
    .project-section { animation-delay: 0.30s; }
    .footer          { animation-delay: 0.36s; }
  </style>
</head>
<body>
  <div class="wrapper">
 
    <!-- Header -->
    <div class="header">
      <div class="avatar">GP</div>
      <div class="header-info">
        <h1>Gib Pangilinan</h1>
        <p class="role">Front-End Developer &nbsp;·&nbsp; React · TypeScript</p>
        <div class="header-tags">
          <span class="tag tag-purple">React</span>
          <span class="tag tag-blue">TypeScript</span>
          <span class="tag tag-teal">SignalR</span>
          <span class="tag tag-coral">Real-time</span>
        </div>
      </div>
    </div>
 
    <!-- Stats -->
    <div class="stats">
      <div class="stat-card">
        <div class="stat-num">3+</div>
        <div class="stat-lbl">Years building</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">React</div>
        <div class="stat-lbl">Primary stack</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">MUI</div>
        <div class="stat-lbl">UI of choice</div>
      </div>
    </div>
 
    <hr class="divider"/>
 
    <!-- About -->
    <div class="about-section">
      <p class="section-label">About</p>
      <p class="about-text">
        Building scalable, responsive web applications focused on real-time systems, clean UI, and performance.
        Currently working with <strong>SignalR</strong> for live data, <strong>Material UI</strong> and
        <strong>Chakra UI</strong> for interfaces, and <strong>RTK Query</strong> for state and data management.
      </p>
    </div>
 
    <hr class="divider"/>
 
    <!-- Tech Stack -->
    <div class="stack-section">
      <p class="section-label">Tech stack</p>
      <div class="stack-grid">
        <div>
          <p class="stack-row-label">Front-End</p>
          <span class="tag tag-blue">React</span>
          <span class="tag tag-purple">TypeScript</span>
          <span class="tag tag-amber">JavaScript</span>
        </div>
        <div>
          <p class="stack-row-label">UI / Styling</p>
          <span class="tag tag-blue">Material UI</span>
          <span class="tag tag-teal">Chakra UI</span>
          <span class="tag tag-pink">SASS</span>
        </div>
        <div>
          <p class="stack-row-label">State & Data</p>
          <span class="tag tag-purple">Redux</span>
          <span class="tag tag-purple">RTK Query</span>
        </div>
        <div>
          <p class="stack-row-label">Tools</p>
          <span class="tag tag-purple">Vite</span>
          <span class="tag tag-teal">SignalR</span>
          <span class="tag tag-coral">Git</span>
        </div>
      </div>
    </div>
 
    <hr class="divider"/>
 
    <!-- Project -->
    <div class="project-section">
      <p class="section-label">Featured project</p>
      <div class="project-card">
        <div class="project-top">
          <div>
            <p class="project-title">MIS Helpdesk</p>
            <p class="project-desc">
              Centralized ticket management platform for internal IT and service requests — with
              role-based access, real-time status tracking, and file attachments.
            </p>
          </div>
          <a class="repo-btn" href="https://github.com/Ichibannnn/make-it-simple" target="_blank">View repo</a>
        </div>
 
        <div class="project-meta">
          <div class="meta-cell">
            <p class="meta-cell-label">Stack</p>
            <p class="meta-cell-value">React · RTK Query · MUI</p>
          </div>
          <div class="meta-cell">
            <p class="meta-cell-label">Type</p>
            <p class="meta-cell-value">Internal tooling · RBAC</p>
          </div>
        </div>
 
        <div class="project-features">
          <p class="features-label">Roles & Features</p>
          <span class="tag tag-purple">Requestor</span>
          <span class="tag tag-teal">Issue Handler</span>
          <span class="tag tag-coral">Admin</span>
          <span class="tag tag-blue">Ticket creation</span>
          <span class="tag tag-amber">Attachments</span>
          <span class="tag tag-pink">Status tracking</span>
        </div>
      </div>
    </div>
 
    <!-- Footer -->
    <p class="footer">🚀 Always learning. Always building.</p>
 
  </div>
</body>
</html>
