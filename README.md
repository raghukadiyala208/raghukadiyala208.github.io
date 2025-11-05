
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio / Portfolio</title>
<meta name="description" content="Creative portfolio of Venkata Raghavendra KADIYALA — Mechanical Engineer & Designer — bilingual (EN/FR)." />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#071226;
    --muted:#9fb0bd;
    --text:#eef6f8;
    --accent1:#1dd3b0;
    --accent2:#e6b66d;
    --card: rgba(255,255,255,0.03);
    --glass: rgba(255,255,255,0.02);
    --radius:12px;
    --snap: y mandatory;
    --section-gap:48px;
    font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;
  }
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; color:var(--text); background:linear-gradient(180deg,#031426,#052835); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;}
  a{color:inherit; text-decoration:none}
  /* layout: full-screen panels with scroll-snap */
  .viewport{
    height:100vh;
    width:100%;
    overflow-y:scroll;
    scroll-snap-type: y var(--snap);
    -webkit-overflow-scrolling:touch;
  }
  section.panel{
    position:relative;
    min-height:calc(100vh - 48px);
    padding:48px;
    display:flex;
    align-items:center;
    justify-content:center;
    scroll-snap-align:center;
  }
  /* background artwork (light, behind content) */
  .bg-art{
    position:absolute; inset:0; z-index:0; opacity:0.16; pointer-events:none; filter: blur(8px) saturate(110%);
  }
  .bg-overlay{
    position:absolute; inset:0; z-index:0; background:linear-gradient(180deg, rgba(3,8,20,0.6), rgba(4,18,26,0.6));
    border-bottom: 1px solid rgba(255,255,255,0.02);
  }

  /* container card on each panel */
  .card{
    position:relative; z-index:5;
    width:min(1100px,92%);
    background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
    border-radius:14px;
    border:1px solid rgba(255,255,255,0.03);
    padding:28px; display:grid; grid-template-columns: 1fr 420px; gap:22px; align-items:start;
    box-shadow: 0 20px 60px rgba(2,6,18,0.6);
    backdrop-filter: blur(6px) saturate(1.02);
  }

  /* alternate layout for variety */
  .card.alt{ grid-template-columns: 420px 1fr; }

  /* left content */
  .meta{ color:var(--muted); font-size:13px; margin-bottom:6px; display:flex; justify-content:space-between; align-items:center; gap:10px; }
  h1.title{ margin:0; font-size:22px; letter-spacing:0.4px; }
  p.lead{ margin:8px 0 0 0; color:var(--muted); line-height:1.55; font-size:15px; }

  /* right pane: subtle card with details */
  .pane{ background:rgba(255,255,255,0.01); border-radius:10px; padding:14px; border:1px solid rgba(255,255,255,0.02); color:var(--muted); }
  .pane h4{ margin:0 0 8px 0; color:var(--text) }

  /* tags */
  .tags{ display:flex; gap:8px; flex-wrap:wrap; margin-top:12px }
  .tag{ padding:6px 10px; border-radius:999px; background:rgba(255,255,255,0.02); color:var(--muted); font-weight:700; font-size:13px; border:1px solid rgba(255,255,255,0.02); }

  /* header for page (fixed) */
  header.fixed{
    position:fixed; left:24px; right:24px; top:18px; z-index:40; display:flex; justify-content:space-between; align-items:center; gap:12px;
    pointer-events:auto;
  }
  .brand{ display:flex; gap:12px; align-items:center; background:transparent; padding:8px 12px; border-radius:999px; }
  .avatar{ width:56px; height:56px; border-radius:12px; background:linear-gradient(135deg,var(--accent1),var(--accent2)); display:flex; align-items:center; justify-content:center; font-weight:800; color:#072425; font-size:18px; box-shadow:0 6px 18px rgba(2,6,18,0.5); }
  .nav{ display:flex; gap:10px; align-items:center; }
  .nav a{ padding:8px 12px; border-radius:10px; background:rgba(255,255,255,0.02); border:1px solid rgba(255,255,255,0.02); font-weight:700; font-size:13px }

  /* transitions: each panel content slides in separately */
  .slide-left, .slide-right, .fade-in { opacity:0; transform:translateY(16px); transition: opacity 700ms cubic-bezier(.2,.9,.2,1), transform 700ms cubic-bezier(.2,.9,.2,1); }
  .in-viewport .slide-left { transform:translateX(0); opacity:1; transition-delay:120ms; transform:translateX(0); }
  .in-viewport .slide-right { transform:translateX(0); opacity:1; transition-delay:220ms; transform:translateX(0); }
  .in-viewport .fade-in { transform:translateY(0); opacity:1; transition-delay:160ms; }

  /* responsive */
  @media(max-width:980px){
    .card, .card.alt{ grid-template-columns: 1fr; padding:18px; }
    .pane{ order:2 }
  }

  /* subtle footer */
  footer{ text-align:center; color:var(--muted); font-size:13px; padding:18px 8px; }

  /* decorative separator between panels */
  .panel + .panel{ padding-top: var(--section-gap); padding-bottom: var(--section-gap); }

  /* ARIA focus outline */
  a:focus{ outline:3px solid rgba(29,211,176,0.18); outline-offset:4px; border-radius:8px; }

</style>
</head>
<body>
  <!-- Fixed header with contact and social -->
  <header class="fixed" role="banner" aria-label="Site header">
    <div class="brand" aria-hidden="false">
      <div class="avatar" id="avatarInitials">VR</div>
      <div style="color:var(--text); font-weight:700;">
        Venkata Raghavendra<br><span style="font-weight:600; color:var(--muted); font-size:13px">Ingénieur Mécanique • Mechanical Engineer</span>
      </div>
    </div>

    <nav class="nav" role="navigation" aria-label="Quick links">
      <a href="#about">About / À propos</a>
      <a href="#work">Work / Projets</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Main viewport: scroll-snap panels -->
  <div class="viewport" id="viewport" tabindex="0" aria-label="Portfolio panels">

    <!-- HERO / About panel -->
    <section class="panel" id="about" aria-labelledby="aboutTitle" role="region">
      <!-- light artistic background (procedural SVG) -->
      <div class="bg-art" aria-hidden="true">
        <!-- subtle geometric liquid art -->
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="g1" x1="0" x2="1">
              <stop offset="0" stop-color="#12d3b0" stop-opacity="0.6"/>
              <stop offset="1" stop-color="#e6b66d" stop-opacity="0.4"/>
            </linearGradient>
            <filter id="f1"><feGaussianBlur stdDeviation="40"/></filter>
          </defs>
          <g filter="url(#f1)">
            <circle cx="280" cy="200" r="260" fill="url(#g1)"/>
            <ellipse cx="1200" cy="300" rx="420" ry="220" fill="#6a78ff" fill-opacity="0.12"/>
            <rect x="900" y="420" width="700" height="320" rx="40" fill="#12d3b0" fill-opacity="0.06"/>
          </g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card" role="article" aria-labelledby="aboutTitle">
        <div>
          <div class="meta slide-left">
            <div id="aboutTitle" style="font-weight:800; color:var(--text)">About — À propos</div>
            <div style="color:var(--muted); font-size:13px">Creative • Technical • Bilingual</div>
          </div>

          <h1 class="title slide-left" style="margin-top:10px">I design mechanical systems that feel thoughtful — Je conçois des systèmes mécaniques pensés pour l'usage.</h1>

          <p class="lead fade-in">
            English: I blend mechanical engineering rigor with visual thinking — train interiors, part design and systems integration. I enjoy turning complex constraints into clear, elegant solutions.<br>
            <em style="color:var(--muted)">Français: J’allie rigueur mécanique et sens du design — aménagements ferroviaires, conception de pièces et intégration système. Je transforme contraintes complexes en solutions élégantes.</em>
          </p>

          <div class="tags slide-left" aria-hidden="false" style="margin-top:18px">
            <span class="tag">Train design</span>
            <span class="tag">CATIA V5</span>
            <span class="tag">FEA</span>
            <span class="tag">Project leadership</span>
          </div>
        </div>

        <aside class="pane slide-right" aria-label="Contact & quick actions">
          <h4>Contact / Contact</h4>
          <p style="margin:6px 0 12px 0; color:var(--muted)">Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a><br>Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
          <p style="margin:0 0 10px 0; color:var(--muted)">LinkedIn: <a href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">venkata-kadiyala</a><br>Instagram: <a href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">@raghukadiyala</a></p>
          <div style="display:flex; gap:8px; margin-top:12px">
            <a class="tag" id="downloadCVBtn" role="button">Download CV</a>
            <a class="tag" href="#work">See work / Voir les projets</a>
          </div>
        </aside>
      </article>
    </section>

    <!-- WORK: each experience is a separate scrolling scene -->
    <section class="panel" id="work" aria-labelledby="workTitle" role="region">
      <div class="bg-art" aria-hidden="true">
        <!-- light pattern for this scene -->
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><linearGradient id="g2" x1="0" x2="1"><stop offset="0" stop-color="#6a78ff"/><stop offset="1" stop-color="#12d3b0"/></linearGradient><filter id="f2"><feGaussianBlur stdDeviation="60"/></filter></defs>
          <g filter="url(#f2)">
            <path d="M0,300 C200,120 400,420 800,260 C1200,100 1400,420 1600,300 L1600,900 L0,900 Z" fill="url(#g2)" fill-opacity="0.08"/>
            <circle cx="1400" cy="140" r="160" fill="#e6b66d" fill-opacity="0.06"/>
          </g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card" role="article">
        <!-- Left: text content -->
        <div class="slide-left">
          <div class="meta"><strong>SEGULA — Project OSTA</strong> <span style="color:var(--muted)">March 2024 — Present</span></div>
          <h1 class="title">Train interiors — front office design (M0 → M5)</h1>
          <p class="lead">EN: Leading CAD deliveries for interior systems: windows, blinds, intercoms, electrical cabinets, under-seat systems. I coordinate suppliers and validate 3D models through maturity levels.<br>
            <em style="color:var(--muted)">FR: Pilotage des livraisons CAO: fenêtres, stores, intercoms, coffrets électriques, boîtes sous siège. Coordination fournisseurs et validation modèles 3D (M0→M5).</em>
          </p>
          <div class="tags"><span class="tag">CATIA V5</span><span class="tag">DMA / SAM</span><span class="tag">Model maturity</span></div>
        </div>

        <!-- Right: soft background image block (light) -->
        <aside class="pane slide-right" aria-hidden="false" style="display:flex; align-items:center; justify-content:center;">
          <!-- Background is subtle: replace inner <svg> with <img src="your-image.jpg" style="opacity:0.18"> to use a real image -->
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice" role="img" aria-hidden="true">
            <defs><linearGradient id="traing" x1="0" x2="1"><stop offset="0" stop-color="#0fb1a3"/><stop offset="1" stop-color="#e6b66d"/></linearGradient><filter id="b"><feGaussianBlur stdDeviation="26"/></filter></defs>
            <g filter="url(#b)"><rect x="0" y="0" width="800" height="400" rx="20" fill="url(#traing)" fill-opacity="0.16"/></g>
            <!-- subtle vector sketch lines -->
            <g stroke="#ffffff" stroke-opacity="0.06" stroke-width="2" fill="none">
              <path d="M40 300 L760 100" stroke-linecap="round"/>
              <path d="M40 260 L760 60" stroke-linecap="round"/>
            </g>
          </svg>
        </aside>
      </article>
    </section>

    <!-- Each subsequent experience gets its own panel. Panels alternate layout and vibe. -->

    <!-- BaWu panel -->
    <section class="panel" aria-labelledby="bawuTitle" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><linearGradient id="g3" x1="0" x2="1"><stop offset="0" stop-color="#e6b66d"/><stop offset="1" stop-color="#6a78ff"/></linearGradient><filter id="f3"><feGaussianBlur stdDeviation="48"/></filter></defs>
          <g filter="url(#f3)"><ellipse cx="300" cy="200" rx="360" ry="180" fill="url(#g3)" fill-opacity="0.08"/><rect x="900" y="320" width="580" height="300" rx="36" fill="#12d3b0" fill-opacity="0.04"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card alt" role="article">
        <div class="pane slide-left" style="display:flex;align-items:center;justify-content:center">
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice" aria-hidden="true">
            <defs><filter id="f4"><feGaussianBlur stdDeviation="28"/></filter></defs>
            <g filter="url(#f4)"><rect width="800" height="400" rx="20" fill="#6a78ff" fill-opacity="0.12"/></g>
            <g stroke="#fff" stroke-opacity="0.06"><path d="M80 320 L720 120" stroke-width="2"/></g>
          </svg>
        </div>

        <div class="slide-right">
          <div class="meta"><strong>SEGULA — BaWu</strong> <span style="color:var(--muted)">May 2023 — Feb 2024</span></div>
          <h1 class="title">Design validation & QA — integration focus</h1>
          <p class="lead">EN: 3D validation workflows, preventing integration issues and managing model QA with KPI/OIL tracking for smooth industrial handover.<br>
            <em style="color:var(--muted)">FR: Validation 3D, prévention des problèmes d’intégration, gestion QA et suivi KPI/OIL pour transfert industriel.</em>
          </p>
          <div class="tags"><span class="tag">Quality</span><span class="tag">OIL / KPI</span><span class="tag">CAD governance</span></div>
        </div>
      </article>
    </section>

    <!-- RER NG panel -->
    <section class="panel" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><linearGradient id="g4"><stop offset="0" stop-color="#7aa0ff"/><stop offset="1" stop-color="#12d3b0"/></linearGradient><filter id="f5"><feGaussianBlur stdDeviation="36"/></filter></defs>
          <g filter="url(#f5)"><rect x="0" y="120" width="1600" height="500" rx="40" fill="url(#g4)" fill-opacity="0.06"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card" role="article">
        <div>
          <div class="meta"><strong>SEGULA — RER NG</strong> <span style="color:var(--muted)">Mar 2023 — Apr 2023</span></div>
          <h1 class="title">Change requests & surveys — on-site work</h1>
          <p class="lead">EN: Requirements analysis, on-site surveys and structural part design in CATIA V5 with criticality reporting.<br>
            <em style="color:var(--muted)">FR: Étude cahier des charges, surveys sur site, conception sous CATIA V5 et rapport de criticité.</em>
          </p>
          <div class="tags"><span class="tag">Survey</span><span class="tag">CATIA V5</span></div>
        </div>

        <aside class="pane" aria-hidden="false">
          <!-- small art -->
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice" aria-hidden="true">
            <defs><filter id="f6"><feGaussianBlur stdDeviation="22"/></filter></defs>
            <g filter="url(#f6)"><rect width="800" height="400" rx="20" fill="#12d3b0" fill-opacity="0.08"/></g>
          </svg>
        </aside>
      </article>
    </section>

    <!-- DSB panel -->
    <section class="panel" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><filter id="f7"><feGaussianBlur stdDeviation="30"/></filter></defs>
          <g filter="url(#f7)"><rect x="120" y="120" width="1200" height="500" rx="40" fill="#e6b66d" fill-opacity="0.06"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card alt" role="article">
        <div class="pane">
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice" aria-hidden="true">
            <defs><filter id="f8"><feGaussianBlur stdDeviation="20"/></filter></defs>
            <g filter="url(#f8)"><rect width="800" height="400" rx="20" fill="#6a78ff" fill-opacity="0.08"/></g>
          </svg>
        </div>

        <div>
          <div class="meta"><strong>SEGULA — DSB</strong> <span style="color:var(--muted)">Jan 2022 — Feb 2023</span></div>
          <h1 class="title">Interior layout & integration — seats, cantilevers</h1>
          <p class="lead">EN: Seat layouts, under-seat boxes, cantilever & ceiling integration — full 3D/2D/FTA modelling to support supplier integration.<br>
            <em style="color:var(--muted)">FR: Agencement sièges, boîtes sous siège, intégration cantilevers/plafonds — modélisation 3D/2D/FTA et support fournisseur.</em>
          </p>
          <div class="tags"><span class="tag">Seats</span><span class="tag">Integration</span></div>
        </div>
      </article>
    </section>

    <!-- SNCF panel -->
    <section class="panel" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><filter id="f9"><feGaussianBlur stdDeviation="40"/></filter></defs>
          <g filter="url(#f9)"><rect x="0" y="220" width="1600" height="360" rx="40" fill="#12d3b0" fill-opacity="0.05"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card" role="article">
        <div>
          <div class="meta"><strong>SNCF</strong> <span style="color:var(--muted)">Apr 2021 — Oct 2021</span></div>
          <h1 class="title">FEA & automation — Hyperworks / Optistruct</h1>
          <p class="lead">EN: Automated bolted assemblies (TCL), mesh & static/non-static analysis for seat supports and validation of structure performance.<br>
            <em style="color:var(--muted)">FR: Automatisation des assemblages, maillages et analyses statiques/non-statiques pour supports de sièges, validation structurelle.</em>
          </p>
          <div class="tags"><span class="tag">Hyperworks</span><span class="tag">Optistruct</span><span class="tag">TCL</span></div>
        </div>

        <aside class="pane">
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice" aria-hidden="true">
            <defs><filter id="f10"><feGaussianBlur stdDeviation="18"/></filter></defs>
            <g filter="url(#f10)"><rect width="800" height="400" rx="20" fill="#6a78ff" fill-opacity="0.08"/></g>
          </svg>
        </aside>
      </article>
    </section>

    <!-- LAMIH panel -->
    <section class="panel" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><linearGradient id="g5"><stop offset="0" stop-color="#fda085"/><stop offset="1" stop-color="#12d3b0"/></linearGradient><filter id="f11"><feGaussianBlur stdDeviation="40"/></filter></defs>
          <g filter="url(#f11)"><ellipse cx="400" cy="220" rx="380" ry="160" fill="url(#g5)" fill-opacity="0.06"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card alt" role="article">
        <div class="pane">
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice">
            <defs><filter id="f12"><feGaussianBlur stdDeviation="26"/></filter></defs>
            <g filter="url(#f12)"><rect width="800" height="400" rx="20" fill="#e6b66d" fill-opacity="0.08"/></g>
          </svg>
        </div>

        <div>
          <div class="meta"><strong>LAMIH</strong> <span style="color:var(--muted)">Sep 2019 — Jan 2020</span></div>
          <h1 class="title">Behavioural analysis & safety concepts</h1>
          <p class="lead">EN: Accident analysis, signalling automation proposals (ETCS / CBTC), and prevention measures for improved safety.<br>
            <em style="color:var(--muted)">FR: Analyse d'accidents, propositions d'automatisation signalisation (ETCS / CBTC) et mesures de prévention.</em>
          </p>
          <div class="tags"><span class="tag">ETCS</span><span class="tag">Safety</span></div>
        </div>
      </article>
    </section>

    <!-- PM DIMENSIONS panel -->
    <section class="panel" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><filter id="f13"><feGaussianBlur stdDeviation="28"/></filter></defs>
          <g filter="url(#f13)"><rect x="220" y="180" width="1160" height="420" rx="40" fill="#6a78ff" fill-opacity="0.06"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card">
        <div>
          <div class="meta"><strong>PM DIMENSIONS</strong> <span style="color:var(--muted)">Jun 2018 — Aug 2019</span></div>
          <h1 class="title">Part design & prototyping — production-ready models</h1>
          <p class="lead">EN: 3D part design for automotive suppliers, prototype development, and verification for client conformity (Hyundai).<br>
            <em style="color:var(--muted)">FR: Conception pièces, prototypes et vérification conformité client (Hyundai).</em>
          </p>
          <div class="tags"><span class="tag">Prototyping</span><span class="tag">CATIA V5</span></div>
        </div>

        <aside class="pane">
          <svg width="100%" height="220" viewBox="0 0 800 400" preserveAspectRatio="xMidYMid slice">
            <defs><filter id="f14"><feGaussianBlur stdDeviation="30"/></filter></defs>
            <g filter="url(#f14)"><rect width="800" height="400" rx="20" fill="#e6b66d" fill-opacity="0.06"/></g>
          </svg>
        </aside>
      </article>
    </section>

    <!-- Internship panel -->
    <section class="panel" id="skills" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><filter id="f15"><feGaussianBlur stdDeviation="32"/></filter></defs>
          <g filter="url(#f15)"><rect x="0" y="160" width="1600" height="520" rx="40" fill="#12d3b0" fill-opacity="0.04"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card">
        <div>
          <div class="meta"><strong>Indian Railways (intern)</strong> <span style="color:var(--muted)">Mar 2016 — Jul 2016</span></div>
          <h1 class="title">Prototype coupling & maintenance optimisation</h1>
          <p class="lead">EN: Coupling prototype development, inspections, maintenance optimisation and Ansys-based structural analysis.<br>
            <em style="color:var(--muted)">FR: Développement prototype couplage, inspection wagons, optimisation maintenance et analyses Ansys.</em>
          </p>
          <div class="tags"><span class="tag">Ansys</span><span class="tag">Maintenance</span></div>
        </div>

        <aside class="pane">
          <h4 style="margin:0 0 8px 0">Skills — Compétences</h4>
          <div style="color:var(--muted); font-size:14px">
            CATIA V5 • DMA 2.3/2.2 • SAM / CDS Interiors • Ansys • Hyperworks / Optistruct • SolidWorks • Autocad • PDM • C, Java, TCL
            <div style="margin-top:10px">
              <strong style="color:var(--text)">Languages:</strong><br>
              English (Bilingual) • Hindi (Native) • Telugu (Native) • Français (B1/B2)
            </div>
          </div>
        </aside>
      </article>
    </section>

    <!-- Contact panel -->
    <section class="panel" id="contact" aria-labelledby="contactTitle" role="region">
      <div class="bg-art" aria-hidden="true">
        <svg width="100%" height="100%" viewBox="0 0 1600 900" preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
          <defs><filter id="f16"><feGaussianBlur stdDeviation="36"/></filter></defs>
          <g filter="url(#f16)"><ellipse cx="900" cy="240" rx="520" ry="210" fill="#6a78ff" fill-opacity="0.06"/></g>
        </svg>
      </div>
      <div class="bg-overlay" aria-hidden="true"></div>

      <article class="card" role="article" aria-labelledby="contactTitle">
        <div>
          <div class="meta"><div id="contactTitle" style="font-weight:800">Contact — Contact</div><div style="color:var(--muted)">Let's connect</div></div>
          <h1 class="title">Reach out — Parlons</h1>
          <p class="lead">Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a> — Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
          <p class="lead" style="margin-top:8px; color:var(--muted)">LinkedIn: <a href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">venkata-kadiyala</a> • Instagram: <a href="https://www.instagram.com/raghukadiyala/" target="_blank">@raghukadiyala</a></p>
          <div style="margin-top:16px; display:flex; gap:12px">
            <a class="tag" href="mailto:venkata.france@gmail.com">Email</a>
            <a class="tag" href="tel:+33755662821">Call</a>
            <a class="tag" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">LinkedIn</a>
          </div>
        </div>

        <aside class="pane" style="display:flex; align-items:center; justify-content:center">
          <div style="text-align:center">
            <div style="font-weight:800; font-size:40px; margin-bottom:6px">VR</div>
            <div style="color:var(--muted)">Creative designer • Mechanical engineer</div>
            <div style="margin-top:12px; color:var(--muted); font-size:13px">Available for freelance & collaborations</div>
          </div>
        </aside>
      </article>
    </section>

    <footer role="contentinfo">© <span id="yr"></span> Venkata Raghavendra KADIYALA — Portfolio (EN / FR).</footer>
  </div>

<script>
  // set year
  document.getElementById('yr').textContent = new Date().getFullYear();

  // helper: scroll-based intersection for per-panel reveal
  (function(){
    const panels = document.querySelectorAll('section.panel');
    const io = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('in-viewport');
        } else {
          // keep visible once entered so animations don't re-hide
          // (optional: if you want repeat toggling, uncomment next line)
          //entry.target.classList.remove('in-viewport');
        }
      });
    }, { threshold: 0.25 });

    panels.forEach(p => io.observe(p));
  })();

  // smooth keyboard & wheel navigation: snap to next panel on wheel / arrow key
  (function(){
    const viewport = document.getElementById('viewport');
    let isThrottled = false;
    function snapTo(direction){
      const panels = Array.from(document.querySelectorAll('section.panel'));
      const currentIndex = panels.findIndex(s => s.getBoundingClientRect().top >= -10 && s.getBoundingClientRect().top < window.innerHeight/2);
      let targetIndex = currentIndex;
      if(direction === 'next') targetIndex = Math.min(panels.length-1, currentIndex+1);
      if(direction === 'prev') targetIndex = Math.max(0, currentIndex-1);
      if(targetIndex !== currentIndex) {
        panels[targetIndex].scrollIntoView({behavior:'smooth', block:'center'});
      }
    }

    viewport.addEventListener('wheel', (e) => {
      if(isThrottled) return;
      isThrottled = true;
      setTimeout(()=> isThrottled=false, 300);
      if(e.deltaY > 10) snapTo('next');
      else if(e.deltaY < -10) snapTo('prev');
    }, {passive:true});

    window.addEventListener('keydown', (e) => {
      if(e.key === 'ArrowDown') snapTo('next');
      if(e.key === 'ArrowUp') snapTo('prev');
      if(e.key === 'Home') document.querySelector('section.panel').scrollIntoView({behavior:'smooth'});
      if(e.key === 'End') document.querySelectorAll('section.panel')[document.querySelectorAll('section.panel').length-1].scrollIntoView({behavior:'smooth'});
    });
  })();

  // Download CV (simple text file; replace with your hosted PDF if available)
  document.getElementById('downloadCVBtn').addEventListener('click', function(e){
    e.preventDefault();
    const text = [
      "Venkata Raghavendra KADIYALA",
      "Mechanical Engineer & Designer",
      "",
      "Email: venkata.france@gmail.com",
      "Phone: +33 7 55 66 28 21",
      "",
      "Portfolio: see online"
    ].join("\n");
    const blob = new Blob([text], {type:'text/plain'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'Venkata_KADIYALA_CV.txt';
    document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
  });

  // Accessibility: focus first link on load
  window.addEventListener('load', () => {
    const first = document.querySelector('header.fixed a');
    if(first) first.setAttribute('tabindex','0');
  });
</script>
</body>
</html>
