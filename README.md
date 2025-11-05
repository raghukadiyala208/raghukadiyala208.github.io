<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Venkata Raghavendra KADIYALA — Profile / Profil</title>
  <meta name="description" content="Bilingual portfolio of Venkata Raghavendra KADIYALA — Mechanical Engineer / Ingénieur Mécanique" />
  <meta name="author" content="Venkata Raghavendra KADIYALA" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg1:#031226;
      --bg2:#052b36;
      --accent1:#1dd3b0; /* teal */
      --accent2:#e6b66d; /* gold */
      --muted:#99a6b0;
      --card: rgba(255,255,255,0.03);
      --glass: rgba(255,255,255,0.02);
      --text:#eef6f8;
      --maxw:1200px;
      --radius:14px;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }

    *{box-sizing:border-box}
    body{
      margin:0;
      min-height:100vh;
      color:var(--text);
      background: radial-gradient(800px 400px at 10% 10%, rgba(29,211,176,0.06), transparent),
                  linear-gradient(180deg,var(--bg1),var(--bg2));
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    .container{ max-width:var(--maxw); margin:28px auto; padding:22px; }

    header{
      display:flex; gap:18px; align-items:center; justify-content:space-between; margin-bottom:18px;
    }
    .brand{ display:flex; gap:14px; align-items:center; }
    .photo{
      width:84px; height:84px; border-radius:12px; overflow:hidden; border:2px solid rgba(255,255,255,0.04);
      background:linear-gradient(135deg, rgba(29,211,176,0.12), rgba(230,182,109,0.06)); display:flex; align-items:center; justify-content:center;
      font-weight:800; font-size:30px; color:var(--accent1);
    }
    .name{
      line-height:1; 
    }
    .name h1{ margin:0; font-size:20px; letter-spacing:0.6px; }
    .name p{ margin:3px 0 0 0; color:var(--muted); font-size:13px; }

    .contact-inline{ display:flex; gap:10px; align-items:center; }
    .chip{
      background:var(--glass); padding:8px 10px; border-radius:10px; font-weight:600; font-size:13px; border:1px solid rgba(255,255,255,0.02);
      display:inline-flex; gap:8px; align-items:center;
    }
    .btn-ghost{ background:transparent; border:1px solid rgba(255,255,255,0.04); padding:8px 12px; border-radius:10px; color:var(--text); text-decoration:none; font-weight:700; }
    .btn-primary{ background:linear-gradient(90deg,var(--accent1),var(--accent2)); color:#052428; padding:9px 14px; border-radius:10px; text-decoration:none; font-weight:800; }

    main{ display:grid; grid-template-columns: 1fr; gap:22px; }

    /* Hero / bilingual intro */
    .hero{
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      border-radius:14px; padding:20px; border:1px solid rgba(255,255,255,0.02); display:flex; gap:18px; align-items:center;
      overflow:hidden;
    }
    .hero .text{ flex:1; }
    .hero h2{ margin:0 0 6px 0; font-size:18px; }
    .hero p{ margin:0; color:var(--muted) }

    .hero .langs{ display:flex; gap:8px; margin-top:12px; }
    .lang-pill{ padding:6px 10px; border-radius:999px; background:rgba(255,255,255,0.02); color:var(--muted); font-weight:600; font-size:13px; border:1px solid rgba(255,255,255,0.02); }

    /* Experience timeline - alternating */
    .timeline{ display:flex; flex-direction:column; gap:22px; }

    .exp{
      display:grid; grid-template-columns: 1fr 420px; gap:18px; align-items:stretch;
      border-radius:12px; overflow:hidden; position:relative; min-height:220px;
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00)); border:1px solid rgba(255,255,255,0.02);
      transform-origin:center;
    }

    .exp.alt{ grid-template-columns: 420px 1fr; } /* alternate layout */

    .exp .media{
      position:relative; overflow:hidden; min-height:220px;
      display:flex; align-items:center; justify-content:center;
    }
    .exp .media img{ width:100%; height:100%; object-fit:cover; display:block; transform:scale(1.03); transition:transform .9s cubic-bezier(.2,.9,.2,1); }

    .exp:hover .media img{ transform:scale(1.08); }

    .exp .content{ padding:20px; display:flex; flex-direction:column; justify-content:flex-start; gap:10px; }
    .meta{ color:var(--muted); font-size:13px; display:flex; gap:8px; align-items:center; }
    .title{ margin:0; font-size:16px; font-weight:700; }
    .desc{ margin:0; color:var(--muted); font-size:14px; }

    /* vibes - different backgrounds for alternating mood */
    .exp.vibe-1::before{
      content:""; position:absolute; inset:0; background:linear-gradient(120deg, rgba(29,211,176,0.03), transparent 40%); pointer-events:none;
    }
    .exp.vibe-2::before{
      content:""; position:absolute; inset:0; background:linear-gradient(120deg, rgba(230,182,109,0.03), transparent 40%); pointer-events:none;
    }
    .exp.vibe-3::before{
      content:""; position:absolute; inset:0; background:linear-gradient(120deg, rgba(120,140,255,0.035), transparent 40%); pointer-events:none;
    }

    /* small cards inside */
    .tags{ display:flex; gap:8px; flex-wrap:wrap; margin-top:6px; }
    .tag{ padding:6px 8px; border-radius:999px; background:rgba(255,255,255,0.02); border:1px solid rgba(255,255,255,0.02); color:var(--muted); font-weight:600; font-size:13px; }

    /* alternating animation classes */
    .slide-in-left{ transform: translateX(-36px); opacity:0; transition:transform .8s cubic-bezier(.2,.9,.2,1), opacity .8s ease; }
    .slide-in-right{ transform: translateX(36px); opacity:0; transition:transform .8s cubic-bezier(.2,.9,.2,1), opacity .8s ease; }
    .in-view{ transform: translateX(0) scale(1); opacity:1; }

    /* skills, edu, languages */
    .grid-3{ display:grid; grid-template-columns: repeat(3, 1fr); gap:14px; }
    .card{ padding:14px; border-radius:10px; background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00)); border:1px solid rgba(255,255,255,0.02); }
    .chip{ display:inline-block; padding:8px 10px; border-radius:999px; background:rgba(255,255,255,0.02); color:var(--muted); margin:6px 6px 0 0; font-weight:700; }

    /* contact block */
    .contact-card{ display:flex; gap:12px; align-items:center; justify-content:space-between; flex-wrap:wrap; padding:14px; border-radius:10px; }
    .contact-left{ display:flex; gap:12px; align-items:center; }

    footer{ text-align:center; color:var(--muted); margin-top:8px; font-size:13px; }

    @media (max-width:980px){
      .exp, .exp.alt{ grid-template-columns: 1fr; }
      .container{ padding:12px; }
      .grid-3{ grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="photo" id="photoBox" aria-hidden="false">VR</div>
        <div class="name">
          <h1>Venkata Raghavendra KADIYALA</h1>
          <p>Ingénieur Mécanique • Mechanical Engineer</p>
        </div>
      </div>

      <div class="contact-inline" aria-hidden="false">
        <a class="chip" href="mailto:venkata.france@gmail.com" title="Email">✉ venkata.france@gmail.com</a>
        <a class="chip" href="tel:+33755662821" title="Phone">☎ +33 7 55 66 28 21</a>
        <a class="btn-ghost" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener noreferrer">LinkedIn</a>
        <a class="btn-primary" id="instaHref" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener noreferrer">Instagram</a>
      </div>
    </header>

    <main>
      <!-- hero with bilingual short summary -->
      <section class="hero card">
        <div class="text">
          <h2>About / À propos</h2>
          <p>
            Mechanical engineer with 5+ years of experience in train interior design, CAD modelling (CATIA V5), FEA and multidisciplinary integration. Lead CAD teams, coordinate suppliers, deliver mature 3D models (M0→M5). — <em>Ingénieur mécanique avec plus de 5 ans d'expérience en aménagement ferroviaire, CAO (CATIA V5), analyse EF et intégration multidisciplinaire.</em>
          </p>
          <div class="langs" aria-hidden="false">
            <span class="lang-pill">English / Français</span>
            <span class="lang-pill">Train Design</span>
            <span class="lang-pill">FEA & CAD</span>
          </div>
        </div>
        <div style="width:320px; text-align:right;">
          <div style="font-weight:700; font-size:13px; color:var(--muted);">Download CV</div>
          <div style="margin-top:10px;">
            <a class="btn-primary" id="downloadCV">Download CV</a>
            <div style="font-size:12px; color:var(--muted); margin-top:6px;">English & Français • Text & PDF</div>
          </div>
        </div>
      </section>

      <!-- timeline / experiences -->
      <section>
        <h2 style="margin:0 0 6px 0;">Experience — Expérience</h2>
        <p style="margin:0 0 12px 0; color:var(--muted)">Projects pulled from CV. Scroll to see each section animate in with a distinct vibe.</p>

        <div class="timeline">

          <!-- SEGULA — Project OSTA (current) -->
          <article class="exp vibe-1" data-animate="left">
            <div class="content slide-in-left">
              <div class="meta"><strong>SEGULA</strong> • March 2024 — Present • Front office (ALSTOM VPF, Project OSTA)</div>
              <h3 class="title">Mechanical Engineer & Interior Designer — Front office</h3>
              <p class="desc">
                English: Design and development of interior components (windows, blinds, sidewalls, intercoms, electrical cabinets, emergency brake handles, toilet piping, under-seat boxes). Delivery of validated 3D models (SAM) to suppliers. Technical leadership: CAO team pilot, model maturity (M0→M5), coordination, CDR/PDR/DDR.
              </p>
              <p class="desc"><em>Français:</em> Conception et développement des composants intérieurs (fenêtres, stores, cloisons, intercoms, coffrets électriques, poignées d'urgence, plomberie toilettes, boîtes sous siège). Livraison des modèles 3D (SAM) au fournisseur. Pilotage technique : équipe CAO, maturité M0→M5, coordination, CDR/PDR/DDR.</p>
              <div class="tags">
                <span class="tag">CATIA V5</span>
                <span class="tag">DMA / SAM</span>
                <span class="tag">Project leadership</span>
              </div>
            </div>

            <div class="media slide-in-right" aria-hidden="false">
              <!-- train interior image (stock) -->
              <img src="https://images.unsplash.com/photo-1520975910042-7e4f3c1e0c1a?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=15f8f6b2b9a4e1f9fa8f2f72f995a5d1" alt="Train interior design">
            </div>
          </article>

          <!-- SEGULA — BaWu -->
          <article class="exp alt vibe-2" data-animate="right">
            <div class="media slide-in-left">
              <img src="https://images.unsplash.com/photo-1508896694512-f0f2b1d76b8b?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=47f8d5d1f7b2cbe0f26d6a6d0b0f3f2b" alt="Design review and modelling">
            </div>
            <div class="content slide-in-right">
              <div class="meta"><strong>SEGULA</strong> • May 2023 — Feb 2024 • Front office (Project BaWu)</div>
              <h3 class="title">Mechanical Engineer & Interior Designer — Validation & QA</h3>
              <p class="desc">
                English: 3D design validation, identify integration issues, propose preventive actions, quality resolution, manage 3D models and CDS Interiors validations. Project & team management with KPI / OIL tracking.
              </p>
              <p class="desc"><em>Français:</em> Vérification et validation de la conception 3D, identification des problèmes d'intégration, actions préventives, résolution qualité, gestion modèles 3D et validations CDS, gestion de projet et suivi KPI/OIL.</p>
              <div class="tags">
                <span class="tag">Quality control</span>
                <span class="tag">OIL / KPI</span>
                <span class="tag">CAD management</span>
              </div>
            </div>
          </article>

          <!-- SEGULA — RER NG change request -->
          <article class="exp vibe-3" data-animate="left">
            <div class="content slide-in-left">
              <div class="meta"><strong>SEGULA</strong> • Mar 2023 — Apr 2023 • Front office</div>
              <h3 class="title">Change Request Engineer — RER NG</h3>
              <p class="desc">
                English: Requirements analysis, mechanical integration resolution, site surveys, design of structural parts in CATIA V5 and criticality reporting.
              </p>
              <p class="desc"><em>Français:</em> Étude du cahier des charges, résolution d'intégration mécanique, survey sur site, conception de pièces structurelles sous CATIA V5, rapport de criticité au client et équipe industrielle.</p>
              <div class="tags">
                <span class="tag">Survey</span>
                <span class="tag">CATIA V5</span>
              </div>
            </div>

            <div class="media slide-in-right">
              <img src="https://images.unsplash.com/photo-1549921296-3d7af3d6c9a3?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=cea6124e3a12c5a2d3e2c4ff4da6a3a3" alt="Technical survey">
            </div>
          </article>

          <!-- SEGULA — Back office (DSB) -->
          <article class="exp alt vibe-1" data-animate="right">
            <div class="media slide-in-left">
              <img src="https://images.unsplash.com/photo-1541807084-5c52b6b9b6a8?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=b3d2a12d469b9a6d6f6b1d9a3e4f9b8c" alt="Seat layout and interior">
            </div>
            <div class="content slide-in-right">
              <div class="meta"><strong>SEGULA</strong> • Jan 2022 — Feb 2023 • Back office (Project DSB)</div>
              <h3 class="title">Mechanical Engineer & Interior Designer — Back office</h3>
              <p class="desc">
                English: Interior layout, seat arrangement, under-seat box design, cantilevers and ceiling integration, 3D/2D/FTA modelling and coordination across disciplines.
              </p>
              <p class="desc"><em>Français:</em> Aménagement intérieur, agencement sièges, boîtes sous siège, intégration cantilevers / plafonds, modélisation 3D/2D/FTA et coordination inter-métiers.</p>
              <div class="tags">
                <span class="tag">3D / 2D / FTA</span>
                <span class="tag">Integration</span>
              </div>
            </div>
          </article>

          <!-- SNCF — FEA -->
          <article class="exp vibe-2" data-animate="left">
            <div class="content slide-in-left">
              <div class="meta"><strong>SNCF</strong> • Apr 2021 — Oct 2021</div>
              <h3 class="title">Mechanical Engineer — Finite Element Analysis</h3>
              <p class="desc">
                English: Automation of bolted assemblies using TCL, mesh, static & non-static analysis for seat supports (Thalys), modelling in CATIA V5 and validation of structural results (Hyperworks / Optistruct).
              </p>
              <p class="desc"><em>Français:</em> Automatisation des assemblages boulonnés (TCL), maillage et analyses statique / non statique pour supports de sièges (Thalys), modélisation sous CATIA V5 et validation (Hyperworks / Optistruct).</p>
              <div class="tags">
                <span class="tag">Hyperworks</span>
                <span class="tag">Optistruct</span>
                <span class="tag">TCL</span>
              </div>
            </div>

            <div class="media slide-in-right">
              <img src="https://images.unsplash.com/photo-1518779578993-ec3579fee39f?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=4f0b0c5d5aa9d7f3e4a8d1a6c1f3b5c7" alt="FEA analysis">
            </div>
          </article>

          <!-- LAMIH -->
          <article class="exp alt vibe-3" data-animate="right">
            <div class="media slide-in-left">
              <img src="https://images.unsplash.com/photo-1517976487492-5750f3195933?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=8e3c6c0b2f2a6b9c1f1f3f6e4b6a1e3" alt="Research & data">
            </div>
            <div class="content slide-in-right">
              <div class="meta"><strong>LAMIH</strong> • Sep 2019 — Jan 2020</div>
              <h3 class="title">Mechanical Engineer — Behavioural & Safety Analysis</h3>
              <p class="desc">
                English: Accident analysis, automated solutions for signalling and prevention, data analysis for autonomous train concepts, ETCS / CBTC research.
              </p>
              <p class="desc"><em>Français:</em> Analyse d'accidents, propositions d'automatisation pour signalisation et prévention, analyse de données et concepts pour trains autonomes (ETCS / CBTC).</p>
              <div class="tags">
                <span class="tag">ETCS / CBTC</span>
                <span class="tag">Data analysis</span>
              </div>
            </div>
          </article>

          <!-- PM DIMENSIONS -->
          <article class="exp vibe-1" data-animate="left">
            <div class="content slide-in-left">
              <div class="meta"><strong>PM DIMENSIONS</strong> • Jun 2018 — Aug 2019</div>
              <h3 class="title">Mechanical Integration Engineer — Part designer</h3>
              <p class="desc">
                English: Part design for mechanical components, 3D modelling (CATIA V5), prototype development, verification and client conformity checks (Hyundai).
              </p>
              <p class="desc"><em>Français:</em> Conception de pièces mécaniques, modélisation 3D (CATIA V5), développement de prototypes, vérification conformité client (Hyundai).</p>
              <div class="tags">
                <span class="tag">Prototyping</span>
                <span class="tag">CATIA V5</span>
              </div>
            </div>

            <div class="media slide-in-right">
              <img src="https://images.unsplash.com/photo-1525609004556-c46c7d6cf023?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=2c3f6b2b1c7a9a6f5e4b3d2c1a0a9f2b" alt="Mechanical parts design">
            </div>
          </article>

          <!-- Indian Railways internship -->
          <article class="exp alt vibe-2" data-animate="right">
            <div class="media slide-in-left">
              <img src="https://images.unsplash.com/photo-1532298420385-65c6dc9b88f9?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=1d6f2c7e1f3b9e8a9c4b2d1f6e7c9a3b" alt="Railway prototype">
            </div>
            <div class="content slide-in-right">
              <div class="meta"><strong>Indian Railways (intern)</strong> • Mar 2016 — Jul 2016</div>
              <h3 class="title">Assistant Engineering (Intern)</h3>
              <p class="desc">
                English: Coupling prototype development, wagon inspection, maintenance optimisation, Ansys modelling and structural analysis.
              </p>
              <p class="desc"><em>Français:</em> Développement prototype de couplage, inspection wagons, optimisation maintenance, modélisation Ansys et analyse structurelle.</p>
              <div class="tags">
                <span class="tag">Ansys</span>
                <span class="tag">Maintenance</span>
              </div>
            </div>
          </article>

        </div>
      </section>

      <!-- Skills / Education / Languages -->
      <section style="display:flex; gap:18px; flex-wrap:wrap;">
        <div class="card" style="flex:1; min-width:260px;">
          <h3 style="margin:0 0 6px 0;">Skills & Tools — Compétences & Outils</h3>
          <div style="margin-top:8px;">
            <span class="chip">CATIA V5</span>
            <span class="chip">DMA 2.3 / 2.2</span>
            <span class="chip">SAM / CDS Interiors</span>
            <span class="chip">Ansys</span>
            <span class="chip">Hyperworks / Optistruct</span>
            <span class="chip">SolidWorks</span>
            <span class="chip">Autocad</span>
            <span class="chip">PDM</span>
            <span class="chip">C, Java, TCL</span>
          </div>
        </div>

        <div class="card" style="width:320px;">
          <h3 style="margin:0 0 6px 0;">Education — Formation</h3>
          <p style="margin:6px 0 0 0;"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019 — 2021)</p>
          <p style="margin:6px 0 0 0;"><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014 — 2018)</p>
          <p style="margin:10px 0 0 0; color:var(--muted); font-size:13px;">Selected project: Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018</p>
        </div>

        <div class="card" style="width:320px;">
          <h3 style="margin:0 0 6px 0;">Languages — Langues</h3>
          <ul style="margin:0; padding-left:18px; color:var(--muted)">
            <li><strong>English</strong> — Bilingual</li>
            <li><strong>Hindi</strong> — Native</li>
            <li><strong>Telugu</strong> — Native</li>
            <li><strong>Français</strong> — Intermediate (B1/B2)</li>
          </ul>
        </div>
      </section>

      <!-- Contact -->
      <section class="card contact-card" id="contactSection">
        <div class="contact-left">
          <div style="font-weight:700">Contact — Contact</div>
          <div style="color:var(--muted); font-size:13px; margin-top:6px;">
            Email: <a href="mailto:venkata.france@gmail.com" style="color:var(--text); text-decoration:none;">venkata.france@gmail.com</a><br>
            Phone: <a href="tel:+33755662821" style="color:var(--text); text-decoration:none;">+33 7 55 66 28 21</a><br>
            LinkedIn: <a href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener noreferrer" style="color:var(--text)">venkata-kadiyala</a><br>
            Instagram: <a href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener noreferrer" style="color:var(--text)">@raghukadiyala</a>
          </div>
        </div>

        <div style="display:flex; gap:8px; align-items:center;">
          <a class="btn-primary" href="mailto:venkata.france@gmail.com">Email</a>
          <a class="btn-ghost" href="tel:+33755662821">Call</a>
          <a class="btn-ghost" href="#top" onclick="window.scrollTo({top:0,behavior:'smooth'})">Back to top</a>
        </div>
      </section>

      <footer>© <span id="year"></span> Venkata Raghavendra KADIYALA — Mechanical Engineer • Watermark-free</footer>
    </main>
  </div>

  <script>
    // Fill year
    document.getElementById('year').textContent = new Date().getFullYear();

    // IntersectionObserver for slide-in animations & parallax subtle effect
    (function(){
      const options = { root: null, rootMargin: '0px', threshold: 0.18 };
      const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
          const el = entry.target;
          if (entry.isIntersecting) {
            el.classList.add('in-view');
            // When in view, also animate its paired media/content
            const left = el.querySelector('.slide-in-left');
            const right = el.querySelector('.slide-in-right');
            if (left) left.classList.add('in-view');
            if (right) right.classList.add('in-view');
            // slow reveal for images too
            const img = el.querySelector('img');
            if (img) { img.style.transition = 'transform 1s cubic-bezier(.2,.9,.2,1), opacity 0.9s ease'; img.style.opacity = '1'; }
            observer.unobserve(el);
          }
        });
      }, options);

      // register each .exp element
      document.querySelectorAll('.exp').forEach((exp) => {
        // initial: set classes so CSS will animate to in-view
        exp.querySelectorAll('.slide-in-left, .slide-in-right').forEach(node => {
          // keep them with translateX initially (CSS already sets this)
        });
        // set images slightly transparent until view
        const img = exp.querySelector('img');
        if (img) { img.style.opacity = '0.5'; }
        observer.observe(exp);
      });
    })();

    // CV download: create bilingual text file and a simple PDF-like blob (text)
    (function(){
      document.getElementById('downloadCV').addEventListener('click', function(e){
        e.preventDefault();
        const content = [
          "Venkata Raghavendra KADIYALA",
          "Mechanical Engineer — Train Design & Integration",
          "",
          "Contact:",
          "  Email: venkata.france@gmail.com",
          "  Phone: +33 7 55 66 28 21",
          "",
          "SUMMARY (EN):",
          "Mechanical engineer with 5+ years experience specialized in train interior design, CAD modelling (CATIA V5), FEA and project coordination.",
          "",
          "RÉSUMÉ (FR):",
          "Ingénieur mécanique avec plus de 5 ans d'expérience, spécialisé en aménagement intérieur ferroviaire, CAO (CATIA V5) et analyse structurelle.",
          "",
          "Experience — see online portfolio for full details."
        ].join("\\n");
        const blob = new Blob([content], {type:'text/plain;charset=utf-8'});
        const url = URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = url;
        a.download = 'Venkata_Raghavendra_KADIYALA_CV.txt';
        document.body.appendChild(a);
        a.click();
        a.remove();
        URL.revokeObjectURL(url);
      });
    })();

    // Photo: when you replace the placeholder div innerHTML with <img src="..." />, it will display.
    // Quick helper: if you have a file 'photo.jpg' next to index.html, uncomment to auto-load:
    // document.getElementById('photoBox').innerHTML = '<img src="photo.jpg" alt="Venkata Raghavendra KADIYALA" style="width:100%;height:100%;object-fit:cover">';

    // Accessibility & keyboard: allow focus on links
    (function(){ 
      const links = document.querySelectorAll('a');
      links.forEach(l => l.setAttribute('tabindex','0'));
    })();
  </script>
</body>
</html>
