<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abhishek764 / README.md</title>
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  /* ══════════════════════════════════
     STRICT BLACK & WHITE PALETTE ONLY
     ══════════════════════════════════ */
  :root {
    --black:       #000000;
    --gray-950:    #080808;
    --gray-900:    #111111;
    --gray-850:    #181818;
    --gray-800:    #222222;
    --gray-750:    #2a2a2a;
    --gray-700:    #333333;
    --gray-600:    #444444;
    --gray-500:    #666666;
    --gray-400:    #888888;
    --gray-300:    #aaaaaa;
    --gray-200:    #cccccc;
    --gray-100:    #e8e8e8;
    --gray-50:     #f2f2f2;
    --white:       #ffffff;

    /* Semantic aliases */
    --bg-page:     var(--gray-950);
    --bg-card:     var(--gray-900);
    --bg-inner:    var(--gray-850);
    --border:      var(--gray-700);
    --border-dim:  var(--gray-800);
    --accent:      var(--white);          /* replaces all blue/color accents */
    --accent-dim:  var(--gray-300);
    --text:        var(--gray-100);
    --text-muted:  var(--gray-400);
    --text-dim:    var(--gray-500);

    --font-mono: 'Fira Code', 'Consolas', monospace;
    --font-ui:   -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  }

  body {
    background: var(--bg-page);
    color: var(--text);
    font-family: var(--font-ui);
    font-size: 14px;
    line-height: 1.5;
    min-height: 100vh;
  }

  /* ── TOP BAR ── */
  .topbar {
    background: var(--black);
    border-bottom: 1px solid var(--border);
    padding: 9px 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-muted);
    position: sticky; top: 0; z-index: 100;
  }
  .topbar .path { display: flex; gap: 4px; align-items: center; }
  .topbar .path .name { color: var(--white); }
  .topbar .path .sep  { color: var(--gray-500); }
  .topbar .path .file { color: var(--gray-200); }
  .topbar .path .ext  { color: var(--gray-500); }
  .topbar .edit-btn {
    background: none; border: 1px solid var(--border);
    color: var(--text-muted); padding: 4px 9px;
    border-radius: 5px; font-size: 11px; cursor: pointer;
  }
  .topbar .edit-btn:hover { border-color: var(--gray-400); }

  /* ── LAYOUT ── */
  .layout {
    display: flex;
    max-width: 900px;
    margin: 0 auto;
    min-height: calc(100vh - 42px);
  }

  /* ── MAIN ── */
  .main { flex: 1; padding: 24px 32px; min-width: 0; }

  /* ── HERO ── */
  .hero {
    border-radius: 8px; overflow: hidden;
    margin-bottom: 14px;
    border: 1px solid var(--border);
    height: 200px; position: relative;
  }
  .hero svg { width: 100%; height: 100%; display: block; }

  /* ── CARDS ── */
  .card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px 22px;
    margin-bottom: 12px;
  }

  .card-title {
    font-family: var(--font-mono);
    font-size: 13px; font-weight: 600;
    color: var(--white);
    display: flex; align-items: center; gap: 8px;
    margin-bottom: 14px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border-dim);
  }

  /* ── SOCIAL BADGES ── */
  .social-row {
    display: flex; flex-wrap: wrap; gap: 8px; justify-content: center;
  }
  .social-badge {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 5px 13px;
    border-radius: 4px;
    font-family: var(--font-mono);
    font-size: 11px; font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border: 1px solid var(--gray-600);
    background: var(--gray-800);
    color: var(--gray-200);
    text-decoration: none;
    transition: background 0.15s, border-color 0.15s;
  }
  .social-badge:hover { background: var(--gray-750); border-color: var(--gray-400); color: var(--white); }

  /* ── ABOUT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: 20px; align-items: center;
  }
  .about-text { font-size: 13px; color: var(--text); line-height: 1.8; margin-bottom: 14px; }
  .about-text strong { color: var(--white); }
  .about-list { list-style: none; }
  .about-list li {
    font-size: 12.5px; color: var(--text-muted);
    margin-bottom: 5px;
    display: flex; align-items: center; gap: 8px;
  }

  /* ── ASTRONAUT ── */
  .astronaut-wrap {
    width: 108px; height: 108px; flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
  }

  /* ── TECH BADGES ── */
  .tech-grid { display: flex; flex-wrap: wrap; gap: 7px; }
  .tech-badge {
    display: inline-flex; align-items: center; gap: 5px;
    padding: 4px 11px;
    border-radius: 4px;
    font-family: var(--font-mono);
    font-size: 11px; font-weight: 500;
    letter-spacing: 0.04em;
    border: 1px solid var(--gray-600);
    background: var(--gray-800);
    color: var(--gray-200);
    cursor: default;
    transition: background 0.12s, border-color 0.12s, color 0.12s;
  }
  .tech-badge:hover {
    background: var(--gray-700);
    border-color: var(--gray-400);
    color: var(--white);
  }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr auto auto auto;
    gap: 10px; align-items: stretch;
  }

  .stat-table {
    background: var(--bg-inner);
    border: 1px solid var(--border-dim);
    border-radius: 6px;
    padding: 12px 14px;
  }
  .stat-table .tbl-head {
    font-family: var(--font-mono); font-size: 11px;
    font-weight: 600; color: var(--gray-300);
    margin-bottom: 10px;
  }
  .stat-row {
    display: flex; justify-content: space-between; gap: 16px;
    margin-bottom: 5px; font-size: 12px;
  }
  .stat-row .sk { color: var(--text-muted); }
  .stat-row .sv { color: var(--white); font-weight: 600; }

  .stat-ring-card {
    background: var(--bg-inner);
    border: 1px solid var(--border-dim);
    border-radius: 6px;
    padding: 12px 14px;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    min-width: 88px;
  }
  .ring {
    width: 54px; height: 54px;
    border-radius: 50%;
    border: 3px solid var(--gray-700);
    border-top-color: var(--white);
    display: flex; align-items: center; justify-content: center;
    font-family: var(--font-mono);
    font-size: 17px; font-weight: 700; color: var(--white);
    margin-bottom: 6px;
    animation: spin-once 1.4s ease-out 0.4s both;
  }
  @keyframes spin-once {
    from { transform: rotate(-90deg); opacity: 0; }
    to   { transform: rotate(0deg); opacity: 1; }
  }
  .ring-label { font-size: 10px; color: var(--text-muted); }

  .stat-big-card {
    background: var(--bg-inner);
    border: 1px solid var(--border-dim);
    border-radius: 6px;
    padding: 12px 14px;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    min-width: 78px; text-align: center;
  }
  .big-num {
    font-family: var(--font-mono);
    font-size: 26px; font-weight: 700;
    color: var(--white); line-height: 1;
    margin-bottom: 4px;
  }
  .big-lbl { font-size: 10px; color: var(--text-muted); }
  .big-sub { font-size: 9px; color: var(--gray-500); margin-top: 2px; }

  .streak-stack { display: flex; flex-direction: column; gap: 10px; }

  /* ── CONTRIBUTION GRAPH ── */
  .contrib-card {
    background: var(--bg-card);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 18px 22px;
  }

  /* ── ANIMATIONS ── */
  .card, .contrib-card { animation: rise 0.45s ease both; }
  .card:nth-child(2) { animation-delay: 0.06s; }
  .card:nth-child(3) { animation-delay: 0.12s; }
  .card:nth-child(4) { animation-delay: 0.18s; }
  @keyframes rise {
    from { opacity: 0; transform: translateY(10px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── REPO ROWS ── */
  .repo-row {
    padding: 16px 0;
    border-bottom: 1px solid var(--border-dim);
  }
  .repo-row:last-child { border-bottom: none; }
  .repo-link {
    font-family: var(--font-mono);
    font-size: 13px; font-weight: 600;
    color: var(--white);
    text-decoration: none;
  }
  .repo-link:hover { text-decoration: underline; color: var(--gray-200); }
  .repo-stat  { font-family: var(--font-mono); font-size: 11px; color: var(--text-muted); }
  .repo-lang  { font-family: var(--font-mono); font-size: 11px; color: var(--text-muted); }
  .repo-lang-dot { width:10px; height:10px; border-radius:50%; display:inline-block; }
  .repo-desc  { font-size: 12px; color: var(--text-muted); line-height: 1.7; margin-bottom: 8px; }
  .repo-bar-wrap {
    width: 100%; height: 4px;
    background: var(--gray-800);
    border-radius: 2px; overflow: hidden;
    margin-bottom: 4px;
  }
  .repo-bar {
    height: 100%;
    background: linear-gradient(90deg, var(--gray-600), var(--white));
    border-radius: 2px;
    animation: bar-grow 1s ease both;
  }
  @keyframes bar-grow { from { width: 0 !important; } }
  .repo-tag {
    font-family: var(--font-mono);
    font-size: 10px;
    color: var(--gray-300);
    background: var(--gray-800);
    border: 1px solid var(--gray-700);
    border-radius: 3px;
    padding: 2px 7px;
    display: inline-block;
  }

  /* ── QUOTE CATEGORY PILLS ── */
  .cat-pill {
    font-family: var(--font-mono);
    font-size: 10px; font-weight: 500;
    letter-spacing: 0.05em;
    padding: 4px 11px;
    border-radius: 20px;
    border: 1px solid var(--gray-600);
    background: var(--gray-800);
    color: var(--gray-400);
    cursor: pointer;
    transition: all 0.15s;
  }
  .cat-pill:hover  { border-color: var(--gray-400); color: var(--gray-200); }
  .cat-pill.active { border-color: var(--white); color: var(--white); background: var(--gray-700); }

  /* ── RESPONSIVE ── */
  @media (max-width: 680px) {
    .stats-grid { grid-template-columns: 1fr 1fr; }
    .about-grid { grid-template-columns: 1fr; }
    .astronaut-wrap { display: none; }
  }
</style>
</head>
<body>

<!-- TOP FILE BAR -->
<div class="topbar">
  <div class="path">
    <span class="name">Abhishek764</span>
    <span class="sep">/</span>
    <span class="file">README</span>
    <span class="ext">.md</span>
  </div>
  <button class="edit-btn">✏</button>
</div>

<div class="layout">

  <!-- ══ MAIN ══ -->
  <main class="main">

    <!-- HERO BANNER — pure greyscale mountains -->
    <div class="hero">
      <svg viewBox="0 0 720 200" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice">
        <defs>
          <linearGradient id="bw-sky" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"   stop-color="#000000"/>
            <stop offset="100%" stop-color="#111111"/>
          </linearGradient>
          <radialGradient id="moon-aura" cx="80%" cy="25%" r="20%">
            <stop offset="0%"   stop-color="#444444" stop-opacity="0.3"/>
            <stop offset="100%" stop-color="transparent"/>
          </radialGradient>
          <filter id="blur1"><feGaussianBlur stdDeviation="1.2"/></filter>
          <filter id="glow-w">
            <feGaussianBlur stdDeviation="4" result="b"/>
            <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
          </filter>
          <filter id="text-glow">
            <feGaussianBlur stdDeviation="5" result="b"/>
            <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
          </filter>
        </defs>

        <!-- Background -->
        <rect width="720" height="200" fill="url(#bw-sky)"/>
        <rect width="720" height="200" fill="url(#moon-aura)"/>

        <!-- Stars — whites and greys -->
        <g>
          <circle cx="42"  cy="14" r="0.9" fill="#ffffff" opacity="0.9"/>
          <circle cx="108" cy="8"  r="1.1" fill="#ffffff" opacity="0.75"/>
          <circle cx="175" cy="20" r="0.7" fill="#dddddd" opacity="0.8"/>
          <circle cx="240" cy="7"  r="1.0" fill="#ffffff" opacity="0.6"/>
          <circle cx="305" cy="15" r="0.9" fill="#ffffff" opacity="0.9"/>
          <circle cx="382" cy="5"  r="0.8" fill="#cccccc" opacity="0.7"/>
          <circle cx="451" cy="18" r="1.2" fill="#ffffff" opacity="0.5"/>
          <circle cx="524" cy="10" r="0.9" fill="#dddddd" opacity="0.8"/>
          <circle cx="595" cy="17" r="0.7" fill="#ffffff" opacity="0.9"/>
          <circle cx="660" cy="8"  r="1.0" fill="#ffffff" opacity="0.65"/>
          <circle cx="78"  cy="33" r="0.6" fill="#aaaaaa" opacity="0.5"/>
          <circle cx="325" cy="30" r="0.7" fill="#cccccc" opacity="0.6"/>
          <circle cx="565" cy="28" r="0.8" fill="#bbbbbb" opacity="0.5"/>
          <circle cx="195" cy="38" r="0.5" fill="#999999" opacity="0.4"/>
          <circle cx="495" cy="36" r="0.6" fill="#aaaaaa" opacity="0.5"/>
          <circle cx="155" cy="45" r="0.4" fill="#888888" opacity="0.4"/>
          <circle cx="420" cy="42" r="0.5" fill="#999999" opacity="0.4"/>
          <circle cx="635" cy="38" r="0.6" fill="#aaaaaa" opacity="0.35"/>
        </g>

        <!-- Moon — bright white -->
        <circle cx="590" cy="32" r="17" fill="#ffffff" opacity="0.92" filter="url(#glow-w)"/>
        <circle cx="584" cy="29" r="13" fill="#111111" opacity="0.18"/>
        <!-- Moon craters -->
        <circle cx="594" cy="27" r="2.5" fill="#e0e0e0" opacity="0.25"/>
        <circle cx="583" cy="36" r="1.8" fill="#e0e0e0" opacity="0.2"/>

        <!-- Far mountains — near black -->
        <polygon
          points="0,148 45,90 95,122 155,66 215,108 275,55 335,92 395,46 455,82 515,40 572,76 625,50 682,80 720,62 720,200 0,200"
          fill="#0d0d0d" filter="url(#blur1)"/>

        <!-- Mid mountains — very dark grey -->
        <polygon
          points="0,168 32,128 82,150 142,102 202,138 262,90 322,128 382,76 442,118 502,72 558,112 620,80 678,110 720,92 720,200 0,200"
          fill="#161616"/>

        <!-- Snow caps mid -->
        <polygon points="262,90 272,98 282,91 292,99 282,70" fill="#ffffff" opacity="0.65"/>
        <polygon points="382,76 392,85 402,78 412,86 402,56" fill="#ffffff" opacity="0.60"/>
        <polygon points="502,72 512,81 522,73 532,82 522,52" fill="#ffffff" opacity="0.55"/>

        <!-- Near mountains — dark, slightly lighter than mid -->
        <polygon
          points="0,182 42,158 92,168 152,140 212,165 272,142 330,170 390,144 448,174 510,147 562,172 622,150 678,172 720,158 720,200 0,200"
          fill="#1e1e1e"/>

        <!-- Horizon mist — very subtle white line -->
        <line x1="0" y1="182" x2="720" y2="182" stroke="#333333" stroke-width="0.5" opacity="0.5"/>

        <!-- River/reflection in valley — grey shimmer -->
        <path d="M260,192 Q360,178 460,192" stroke="#333333" stroke-width="1.5" fill="none" opacity="0.5"/>
        <path d="M290,196 Q360,184 430,196" stroke="#2a2a2a" stroke-width="1" fill="none" opacity="0.4"/>

        <!-- HERO TEXT -->
        <text x="360" y="110" text-anchor="middle"
          font-family="'Fira Code', monospace"
          font-size="23" font-weight="700"
          fill="#ffffff" filter="url(#text-glow)"
          letter-spacing="0.5">
          Welcome to Abhishek's GitHub
        </text>
        <text x="360" y="140" text-anchor="middle"
          font-family="'Fira Code', monospace"
          font-size="19" font-weight="300"
          fill="#888888" letter-spacing="3">
          &lt;/&gt;
        </text>
      </svg>
    </div>

    <!-- SOCIAL LINKS -->
    <div class="card" style="padding:13px 20px; margin-bottom:12px;">
      <div class="social-row">
        <a class="social-badge" href="https://www.linkedin.com/in/abhishek-kumar-831056237/" target="_blank">in linkedin</a>
        <a class="social-badge" href="https://github.com/Abhishek764" target="_blank">&#128008; github</a>
        <a class="social-badge" href="https://mac-os-portfolio-orpin.vercel.app/" target="_blank">&#127760; portfolio</a>
        <a class="social-badge" href="/cdn-cgi/l/email-protection#1e7f7c76776d767b75306d6e766d2e2f5e79737f7772307d7173">@ email</a>
        <a class="social-badge" href="tel:+917645990776">&#128222; +91 7645990776</a>
      </div>
    </div>

    <!-- ABOUT ME -->
    <div class="card">
      <div class="card-title">&#128100; About me</div>
      <div class="about-grid">
        <div>
          <p class="about-text">
            Hey there! I'm <strong>Abhishek Kumar</strong>, a Computer Science student at Lovely Professional University
            and a passionate <strong>Full-Stack & DevOps engineer</strong>. I build cloud-native systems, automate CI/CD pipelines,
            and deploy production-grade apps on AWS. Currently diving deep into <strong>DevSecOps, Kubernetes, and GitOps</strong>.
          </p>
          <ul class="about-list">
            <li><span>&#127891;</span> B.Tech CSE @ Lovely Professional University, Punjab (Since Aug 2020 · CGPA 6.72)</li>
            <li><span>&#128205;</span> Punjab, India</li>
            <li><span>&#128187;</span> Full Stack Dev Training — CipherSchools (Jun – Jul 2024)</li>
            <li><span>&#9729;</span> Cloud-native deployments on AWS EKS, EC2, S3, Lambda, ECS</li>
            <li><span>&#128272;</span> DevSecOps — SonarQube, Trivy, Prometheus, Grafana, ArgoCD</li>
            <li><span>&#128640;</span> GitOps · IaC with Terraform · Jenkins · GitHub Actions</li>
          </ul>
        </div>
        <!-- ASTRONAUT — greyscale SVG -->
        <div class="astronaut-wrap">
          <svg viewBox="0 0 110 130" xmlns="http://www.w3.org/2000/svg">
            <g transform="translate(55,66)">
              <ellipse cx="0" cy="20" rx="22" ry="28" fill="#c0c0c0"/>
              <circle cx="0" cy="-14" r="22" fill="#c8c8c8"/>
              <ellipse cx="0" cy="-14" rx="14" ry="13" fill="#1a1a1a"/>
              <ellipse cx="-3" cy="-18" rx="5" ry="4" fill="#333333" opacity="0.6"/>
              <ellipse cx="0" cy="-1" rx="22" ry="5" fill="#a0a0a0"/>
              <ellipse cx="-28" cy="8"  rx="8" ry="14" fill="#c0c0c0" transform="rotate(-15 -28 8)"/>
              <ellipse cx="28"  cy="8"  rx="8" ry="14" fill="#c0c0c0" transform="rotate(15 28 8)"/>
              <ellipse cx="-32" cy="20" rx="7" ry="5" fill="#888888"/>
              <ellipse cx="32"  cy="20" rx="7" ry="5" fill="#888888"/>
              <ellipse cx="-10" cy="46" rx="9" ry="14" fill="#b8b8b8"/>
              <ellipse cx="10"  cy="46" rx="9" ry="14" fill="#b8b8b8"/>
              <ellipse cx="-11" cy="58" rx="10" ry="5" fill="#555555"/>
              <ellipse cx="11"  cy="58" rx="10" ry="5" fill="#555555"/>
              <rect x="-8" y="10" width="16" height="14" rx="3" fill="#666666"/>
              <circle cx="-3" cy="15" r="2" fill="#dddddd"/>
              <circle cx="3"  cy="15" r="2" fill="#aaaaaa"/>
              <rect x="-5" y="19" width="10" height="2" rx="1" fill="#999999"/>
              <rect x="22" y="2" width="2" height="8" fill="#777777"/>
              <rect x="24" y="2" width="8" height="5" fill="#555555"/>
            </g>
            <circle cx="10" cy="15" r="1.5" fill="#ffffff" opacity="0.7">
              <animate attributeName="opacity" values="0.7;0.1;0.7" dur="2.1s" repeatCount="indefinite"/>
            </circle>
            <circle cx="96" cy="25" r="1.0" fill="#cccccc" opacity="0.5">
              <animate attributeName="opacity" values="0.5;0.05;0.5" dur="1.8s" repeatCount="indefinite"/>
            </circle>
            <circle cx="18" cy="112" r="1.2" fill="#ffffff" opacity="0.4">
              <animate attributeName="opacity" values="0.4;0.05;0.4" dur="2.5s" repeatCount="indefinite"/>
            </circle>
            <path d="M78 52 Q92 32 102 10" stroke="#666666" stroke-width="1.5" fill="none" opacity="0.5"/>
          </svg>
        </div>
      </div>
    </div>

    <!-- TECHNOLOGIES -->
    <div class="card">
      <div class="card-title">&#9881; Technologies</div>
      <div class="tech-grid">
        <!-- Languages -->
        <span class="tech-badge">⬡ C++</span>
        <span class="tech-badge">◈ JAVASCRIPT</span>
        <span class="tech-badge">▲ PYTHON</span>
        <!-- Frontend -->
        <span class="tech-badge">◈ HTML / CSS</span>
        <span class="tech-badge">◈ TAILWIND</span>
        <span class="tech-badge">⚛ REACT</span>
        <!-- Backend -->
        <span class="tech-badge">⬡ NODE.JS</span>
        <span class="tech-badge">⬡ EXPRESS.JS</span>
        <!-- Databases -->
        <span class="tech-badge">⬡ MYSQL</span>
        <span class="tech-badge">◆ MONGODB</span>
        <!-- Cloud -->
        <span class="tech-badge">☁ AWS EC2</span>
        <span class="tech-badge">☁ AWS S3</span>
        <span class="tech-badge">☁ AWS EKS</span>
        <span class="tech-badge">☁ AWS ECS</span>
        <span class="tech-badge">☁ LAMBDA</span>
        <!-- DevOps -->
        <span class="tech-badge">⬡ DOCKER</span>
        <span class="tech-badge">⬡ KUBERNETES</span>
        <span class="tech-badge">⬡ TERRAFORM</span>
        <span class="tech-badge">⬡ JENKINS</span>
        <span class="tech-badge">⬡ GITHUB ACTIONS</span>
        <span class="tech-badge">⬡ ARGOCD</span>
        <span class="tech-badge">⎇ GIT</span>
        <!-- Observability -->
        <span class="tech-badge">◆ PROMETHEUS</span>
        <span class="tech-badge">◆ GRAFANA</span>
        <span class="tech-badge">◆ JAEGER</span>
        <span class="tech-badge">◆ OPENTELEMETRY</span>
        <span class="tech-badge">◆ KIBANA</span>
        <!-- Security / Quality -->
        <span class="tech-badge">★ SONARQUBE</span>
        <span class="tech-badge">★ TRIVY</span>
      </div>
    </div>

    <!-- RANDOM QUOTE GENERATOR -->
    <div class="card" id="quote-card">
      <div class="card-title">&#10075; Dev Quote of the Day</div>
      <div style="position:relative; min-height:110px;">
        <!-- Quote display -->
        <div id="quote-display" style="padding:10px 0 18px;">
          <div style="
            font-family:var(--font-mono);
            font-size:13px;
            color:var(--gray-100);
            line-height:1.9;
            font-style:italic;
            border-left:3px solid var(--gray-600);
            padding-left:16px;
            margin-bottom:12px;
            transition: opacity 0.4s ease;
          " id="quote-text">
            "First, solve the problem. Then, write the code."
          </div>
          <div style="
            font-family:var(--font-mono);
            font-size:11px;
            color:var(--gray-500);
            padding-left:19px;
          " id="quote-author">— John Johnson</div>
        </div>

        <!-- Controls row -->
        <div style="display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:10px;">
          <!-- Category pills -->
          <div style="display:flex; gap:6px; flex-wrap:wrap;" id="cat-pills">
            <button onclick="setCategory('all')"      class="cat-pill active" data-cat="all">All</button>
            <button onclick="setCategory('devops')"   class="cat-pill" data-cat="devops">DevOps</button>
            <button onclick="setCategory('code')"     class="cat-pill" data-cat="code">Code</button>
            <button onclick="setCategory('mindset')"  class="cat-pill" data-cat="mindset">Mindset</button>
            <button onclick="setCategory('cloud')"    class="cat-pill" data-cat="cloud">Cloud</button>
          </div>
          <!-- Generate button -->
          <button onclick="newQuote()" id="gen-btn" style="
            font-family:var(--font-mono);
            font-size:11px;
            font-weight:600;
            letter-spacing:0.06em;
            padding:6px 16px;
            background:var(--gray-800);
            border:1px solid var(--gray-500);
            color:var(--white);
            border-radius:5px;
            cursor:pointer;
            transition:background 0.15s, border-color 0.15s;
            display:flex; align-items:center; gap:6px;
          " onmouseover="this.style.background='var(--gray-700)'" onmouseout="this.style.background='var(--gray-800)'">
            &#8635; New Quote
          </button>
        </div>
      </div>
    </div>

    <!-- TOP REPO CONTRIBUTIONS -->
    <div class="card">
      <div class="card-title">&#127381; Top Repository Contributions</div>
      <div style="display:flex; flex-direction:column; gap:0;" id="repo-list">

        <!-- Repo 1 -->
        <div class="repo-row">
          <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:5px;">
            <div style="display:flex; align-items:center; gap:8px;">
              <span style="font-size:13px;">&#128218;</span>
              <a href="https://github.com/Abhishek764" target="_blank" class="repo-link">Starbucks-DevSecOps-EKS</a>
            </div>
            <div style="display:flex; gap:12px; align-items:center;">
              <span class="repo-stat">&#9733; 0</span>
              <span class="repo-lang-dot" style="background:#555;"></span>
              <span class="repo-lang">HCL / Terraform</span>
            </div>
          </div>
          <p class="repo-desc">End-to-end DevSecOps pipeline on Amazon EKS with Jenkins, SonarQube, Trivy, Prometheus & Grafana.</p>
          <div class="repo-bar-wrap"><div class="repo-bar" style="width:88%;"></div></div>
          <div style="display:flex; gap:8px; margin-top:8px; flex-wrap:wrap;">
            <span class="repo-tag">Jenkins</span><span class="repo-tag">Kubernetes</span><span class="repo-tag">AWS EKS</span><span class="repo-tag">Terraform</span><span class="repo-tag">SonarQube</span><span class="repo-tag">Trivy</span>
          </div>
        </div>

        <!-- Repo 2 -->
        <div class="repo-row">
          <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:5px;">
            <div style="display:flex; align-items:center; gap:8px;">
              <span style="font-size:13px;">&#128218;</span>
              <a href="https://github.com/Abhishek764" target="_blank" class="repo-link">Retail-Microservices-GitOps</a>
            </div>
            <div style="display:flex; gap:12px; align-items:center;">
              <span class="repo-stat">&#9733; 0</span>
              <span class="repo-lang-dot" style="background:#777;"></span>
              <span class="repo-lang">YAML / Docker</span>
            </div>
          </div>
          <p class="repo-desc">Cloud-native retail platform (UI, catalog, cart, orders, checkout) with GitOps via ArgoCD & GitHub Actions on AWS EKS.</p>
          <div class="repo-bar-wrap"><div class="repo-bar" style="width:74%;"></div></div>
          <div style="display:flex; gap:8px; margin-top:8px; flex-wrap:wrap;">
            <span class="repo-tag">ArgoCD</span><span class="repo-tag">GitHub Actions</span><span class="repo-tag">Docker</span><span class="repo-tag">Kubernetes</span><span class="repo-tag">GitOps</span>
          </div>
        </div>

        <!-- Repo 3 -->
        <div class="repo-row">
          <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:5px;">
            <div style="display:flex; align-items:center; gap:8px;">
              <span style="font-size:13px;">&#128218;</span>
              <a href="https://github.com/Abhishek764" target="_blank" class="repo-link">MERN-Blog-Platform</a>
            </div>
            <div style="display:flex; gap:12px; align-items:center;">
              <span class="repo-stat">&#9733; 0</span>
              <span class="repo-lang-dot" style="background:#999;"></span>
              <span class="repo-lang">JavaScript</span>
            </div>
          </div>
          <p class="repo-desc">Full-stack blog platform with JWT auth, rich text editor, and user dashboard built with MERN stack.</p>
          <div class="repo-bar-wrap"><div class="repo-bar" style="width:60%;"></div></div>
          <div style="display:flex; gap:8px; margin-top:8px; flex-wrap:wrap;">
            <span class="repo-tag">React</span><span class="repo-tag">Node.js</span><span class="repo-tag">MongoDB</span><span class="repo-tag">JWT</span><span class="repo-tag">Express</span>
          </div>
        </div>

      </div>
    </div>

    <!-- STATISTICS -->
    <div class="card">
      <div class="card-title">&#128202; Statistics</div>
      <div class="stats-grid">

        <!-- Stats table -->
        <div class="stat-table">
          <div class="tbl-head">Abhishek's GitHub Stats</div>
          <div class="stat-row"><span class="sk">GitHub Username:</span><span class="sv">Abhishek764</span></div>
          <div class="stat-row"><span class="sk">Cloud Platforms:</span><span class="sv">AWS (EKS · EC2 · S3)</span></div>
          <div class="stat-row"><span class="sk">DevOps Tools:</span><span class="sv">8+</span></div>
          <div class="stat-row"><span class="sk">Observability Stack:</span><span class="sv">Prometheus · Grafana</span></div>
          <div class="stat-row"><span class="sk">Certifications:</span><span class="sv">2</span></div>
        </div>

        <!-- Grade ring -->
        <div class="stat-ring-card">
          <div class="ring">A</div>
          <div class="ring-label" style="color:#e8e8e8; font-weight:600;">Rank</div>
        </div>

        <!-- Projects count -->
        <div class="stat-big-card">
          <div class="big-num">2</div>
          <div class="big-lbl">Cloud-Native<br>Projects</div>
          <div class="big-sub">EKS · DevSecOps · GitOps</div>
        </div>

        <!-- Certs + tools -->
        <div class="streak-stack">
          <div class="stat-big-card" style="min-width:72px;">
            <div class="big-num" style="font-size:22px;">2</div>
            <div class="big-lbl">Certificates</div>
            <div class="big-sub">NPTEL · CipherSchools</div>
          </div>
          <div class="stat-big-card" style="min-width:72px;">
            <div class="big-num" style="font-size:22px;">15+</div>
            <div class="big-lbl">DevOps<br>Tools</div>
            <div class="big-sub">Jenkins · K8s · Terraform</div>
          </div>
        </div>
      </div>
    </div>

    <!-- CONTRIBUTION GRAPH -->
    <div class="contrib-card">
      <div class="card-title" style="border-bottom:1px solid var(--border-dim); margin-bottom:14px; padding-bottom:10px;">
        &#128200; Abhishek's Contribution Graph
      </div>
      <svg viewBox="0 0 680 120" xmlns="http://www.w3.org/2000/svg" width="100%" style="display:block;">
        <defs>
          <linearGradient id="area-fill" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%"   stop-color="#ffffff" stop-opacity="0.18"/>
            <stop offset="100%" stop-color="#ffffff" stop-opacity="0.01"/>
          </linearGradient>
        </defs>

        <!-- Grid lines -->
        <g stroke="#2a2a2a" stroke-width="0.5">
          <line x1="20" y1="90" x2="665" y2="90"/>
          <line x1="20" y1="68" x2="665" y2="68"/>
          <line x1="20" y1="46" x2="665" y2="46"/>
          <line x1="20" y1="24" x2="665" y2="24"/>
        </g>

        <!-- Y-axis labels -->
        <g font-family="'Fira Code', monospace" font-size="9" fill="#555555">
          <text x="5" y="93">0</text>
          <text x="5" y="71">1</text>
          <text x="5" y="49">2</text>
          <text x="5" y="27">3</text>
        </g>

        <!-- Area fill -->
        <polygon fill="url(#area-fill)" points="
          20,90  30,90  40,90  50,90  60,90
          70,68  80,90  90,90  100,90 110,90
          120,90 130,90 140,90 150,68 160,90
          170,90 180,90 190,90 200,90 210,90
          220,68 230,46 240,90 250,90 260,90
          270,90 280,68 290,90 300,90 310,68
          320,90 330,90 340,68 350,46 360,24
          370,46 380,90 390,90 400,90 410,90
          420,68 430,46 440,68 450,90 460,90
          470,90 480,68 490,90 500,90 510,68
          520,90 530,90 540,68 550,46 560,68
          570,90 580,90 590,68 600,46 610,68
          620,90 630,90 640,68 650,90 660,90
          660,90 20,90"/>

        <!-- Line — white -->
        <polyline fill="none" stroke="#ffffff" stroke-width="1.6"
          stroke-linecap="round" stroke-linejoin="round"
          points="
            20,90  30,90  40,90  50,90  60,90
            70,68  80,90  90,90  100,90 110,90
            120,90 130,90 140,90 150,68 160,90
            170,90 180,90 190,90 200,90 210,90
            220,68 230,46 240,90 250,90 260,90
            270,90 280,68 290,90 300,90 310,68
            320,90 330,90 340,68 350,46 360,24
            370,46 380,90 390,90 400,90 410,90
            420,68 430,46 440,68 450,90 460,90
            470,90 480,68 490,90 500,90 510,68
            520,90 530,90 540,68 550,46 560,68
            570,90 580,90 590,68 600,46 610,68
            620,90 630,90 640,68 650,90 660,90"/>

        <!-- Peak dots — white -->
        <g fill="#ffffff">
          <circle cx="70"  cy="68" r="2.5"/>
          <circle cx="150" cy="68" r="2.5"/>
          <circle cx="220" cy="68" r="2.5"/>
          <circle cx="230" cy="46" r="2.5"/>
          <circle cx="280" cy="68" r="2.5"/>
          <circle cx="310" cy="68" r="2.5"/>
          <circle cx="350" cy="46" r="2.5"/>
          <circle cx="360" cy="24" r="3.5" stroke="#ffffff" stroke-width="1.5" fill="none"/>
          <circle cx="360" cy="24" r="1.8"/>
          <circle cx="430" cy="46" r="2.5"/>
          <circle cx="480" cy="68" r="2.5"/>
          <circle cx="510" cy="68" r="2.5"/>
          <circle cx="550" cy="46" r="2.5"/>
          <circle cx="600" cy="46" r="2.5"/>
        </g>

        <!-- Month labels -->
        <g font-family="'Fira Code', monospace" font-size="8" fill="#555555">
          <text x="18"  y="112">Jan</text>
          <text x="75"  y="112">Feb</text>
          <text x="133" y="112">Mar</text>
          <text x="193" y="112">Apr</text>
          <text x="250" y="112">May</text>
          <text x="308" y="112">Jun</text>
          <text x="365" y="112">Jul</text>
          <text x="423" y="112">Aug</text>
          <text x="480" y="112">Sep</text>
          <text x="538" y="112">Oct</text>
          <text x="595" y="112">Nov</text>
          <text x="650" y="112">Dec</text>
        </g>
      </svg      </svg>
    </div>

  </main>
</div>

<script>
  const QUOTES = {
    all: [],
    devops: [
      { text: "Automate everything you do more than twice.", author: "DevOps Principle" },
      { text: "In DevOps, the goal is not to eliminate humans from the loop — it is to keep humans in the right parts of the loop.", author: "Gene Kim" },
      { text: "Infrastructure as code means your infrastructure is just as testable as your application code.", author: "Kief Morris" },
      { text: "If it hurts, do it more often. And bring the pain forward.", author: "Jez Humble" },
      { text: "The pipeline is the product.", author: "DevOps Community" },
      { text: "You build it, you run it.", author: "Werner Vogels, AWS CTO" },
      { text: "Monitoring is not optional. It is the feedback loop that drives improvement.", author: "SRE Handbook" },
      { text: "Configuration drift is the enemy of consistency.", author: "HashiCorp" },
      { text: "GitOps is the best practice for deploying to Kubernetes at scale.", author: "Weaveworks" },
    ],
    code: [
      { text: "First, solve the problem. Then, write the code.", author: "John Johnson" },
      { text: "Any fool can write code that a computer can understand. Good programmers write code that humans can understand.", author: "Martin Fowler" },
      { text: "Clean code always looks like it was written by someone who cares.", author: "Robert C. Martin" },
      { text: "Make it work, make it right, make it fast.", author: "Kent Beck" },
      { text: "Debugging is twice as hard as writing the code in the first place.", author: "Brian W. Kernighan" },
      { text: "The best code is no code at all.", author: "Jeff Atwood" },
      { text: "Code is read much more often than it is written.", author: "Guido van Rossum" },
      { text: "Simplicity is the soul of efficiency.", author: "Austin Freeman" },
      { text: "Before software can be reusable it first has to be usable.", author: "Ralph Johnson" },
    ],
    mindset: [
      { text: "The expert in anything was once a beginner.", author: "Helen Hayes" },
      { text: "Stay hungry, stay foolish.", author: "Steve Jobs" },
      { text: "Done is better than perfect.", author: "Sheryl Sandberg" },
      { text: "Fall seven times, stand up eight.", author: "Japanese Proverb" },
      { text: "The difference between a novice and an expert is the number of mistakes they have made.", author: "Unknown" },
      { text: "Consistency is the mother of mastery.", author: "Robin Sharma" },
      { text: "Push yourself, because no one else is going to do it for you.", author: "Unknown" },
    ],
    cloud: [
      { text: "The cloud is not a place; it is a way of doing IT.", author: "David Linthicum" },
      { text: "Containers are the new unit of deployment.", author: "Kubernetes Community" },
      { text: "Kubernetes is the Linux of the cloud.", author: "Jim Zemlin" },
      { text: "Design for failure. Everything fails, all the time.", author: "Werner Vogels" },
      { text: "Immutable infrastructure is the key to reproducible deployments.", author: "Chad Fowler" },
      { text: "Treat your servers like cattle, not pets.", author: "Bill Baker" },
      { text: "Multi-region is not a luxury; it is a reliability strategy.", author: "AWS Well-Architected" },
    ],
  };

  QUOTES.all = [...QUOTES.devops, ...QUOTES.code, ...QUOTES.mindset, ...QUOTES.cloud];

  let currentCategory = 'all';
  let lastIndex = -1;

  function setCategory(cat) {
    currentCategory = cat;
    lastIndex = -1;
    document.querySelectorAll('.cat-pill').forEach(p => {
      p.classList.toggle('active', p.dataset.cat === cat);
    });
    newQuote();
  }

  function newQuote() {
    const pool = QUOTES[currentCategory];
    let idx;
    do { idx = Math.floor(Math.random() * pool.length); } while (idx === lastIndex && pool.length > 1);
    lastIndex = idx;
    const q = pool[idx];

    const textEl   = document.getElementById('quote-text');
    const authorEl = document.getElementById('quote-author');

    textEl.style.opacity = '0';
    authorEl.style.opacity = '0';

    setTimeout(() => {
      textEl.textContent   = '"' + q.text + '"';
      authorEl.textContent = '— ' + q.author;
      textEl.style.transition   = 'opacity 0.4s ease';
      authorEl.style.transition = 'opacity 0.4s ease';
      textEl.style.opacity   = '1';
      authorEl.style.opacity = '1';
    }, 280);

    const btn = document.getElementById('gen-btn');
    btn.style.transition = 'transform 0.4s ease';
    btn.style.transform  = 'rotate(360deg)';
    setTimeout(() => { btn.style.transform = 'rotate(0deg)'; }, 420);
  }

  setInterval(newQuote, 12000);
  window.addEventListener('DOMContentLoaded', newQuote);
</script>
</body>
</html>
