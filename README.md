<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --accent-teal:#17c3a2;
    --gold-grad:linear-gradient(45deg,#fdbb2d,#fcb045,#fd7e14);
    --muted:#9fb0bb;
    --bg-top:#0c3042;
    --bg-bottom:#031018;
    --glass: rgba(255,255,255,0.06);
    --content-width:1200px;
  }
  /* Reset & base */
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%;width:100%;overflow:hidden;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));-webkit-font-smoothing:antialiased;color:#eaf6f8}
  a{color:inherit;text-decoration:none}
  /* Main vertical container with snap */
  main{height:100vh;width:100vw;overflow-y:auto;scroll-snap-type:y mandatory; -webkit-overflow-scrolling:touch;}
  /* Prevent horizontal scroll */
  body,html,main{overflow-x:hidden}
  /* Each section = full viewport */
  section{min-height:100vh;height:100vh;width:100%;position:relative;display:flex;align-items:center;justify-content:center;padding:36px;scroll-snap-align:start}
  /* unified backdrop & overlay ensure same colour */
  .backdrop{position:absolute;inset:0;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));z-index:0}
  .overlay{position:absolute;inset:0;z-index:1;pointer-events:none;background:linear-gradient(180deg, rgba(2,8,12,0.08), rgba(0,0,0,0.54))}
  .content{position:relative;z-index:6;max-width:var(--content-width);width:100%;padding:24px;text-align:center;display:flex;flex-direction:column;gap:12px;align-items:center;justify-content:center}
  /* Titles & text */
  h1.title{font-weight:900;font-size:clamp(34px,7.6vw,84px);line-height:0.96;text-transform:uppercase;letter-spacing:-1px}
  h2.subtitle{font-weight:700;color:var(--muted);font-size:18px}
  p.lead{color:var(--muted);max-width:980px;line-height:1.6;font-size:16px}
  /* portrait and floats */
  .portrait{height:62vh;max-height:760px;object-fit:contain;filter:drop-shadow(0 48px 120px rgba(0,0,0,0.6));border-radius:8px}
  .float{position:absolute;z-index:5;pointer-events:none;width:46vw;max-width:760px;filter:drop-shadow(0 34px 90px rgba(0,0,0,0.6))}
  /* top-right hamburger (always visible) */
  .hamburger{
    position:fixed;right:18px;top:16px;z-index:120;display:flex;align-items:center;gap:10px;
  }
  .hambutton{
    width:48px;height:44px;border-radius:10px;background:rgba(255,255,255,0.04);backdrop-filter:blur(8px);display:flex;align-items:center;justify-content:center;border:1px solid rgba(255,255,255,0.04);cursor:pointer;color:#eaf6f8;box-shadow:0 8px 30px rgba(0,0,0,0.45)
  }
  /* menu dropdown (glass blur) */
  .menu{
    position:fixed;right:18px;top:70px;z-index:119;min-width:220px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.02));backdrop-filter:blur(10px);box-shadow:0 20px 60px rgba(0,0,0,0.6);overflow:hidden;transform-origin:top right;opacity:0;visibility:hidden;transition:all .28s ease;
  }
  .menu.open{opacity:1;visibility:visible;transform:translateY(0)}
  .menu a{display:flex;align-items:center;justify-content:space-between;padding:12px 16px;color:#eaf6f8;border-bottom:1px solid rgba(255,255,255,0.02);font-weight:700}
  .menu a:last-child{border-bottom:0}
  .menu a:hover{background:rgba(255,255,255,0.02)}
  .menu .arrow{opacity:0.9}
  /* Buttons used inside sections */
  .btn{display:inline-flex;align-items:center;gap:10px;padding:12px 18px;border-radius:12px;font-weight:800;color:#052425;background:var(--gold-grad);box-shadow:0 18px 50px rgba(0,0,0,0.5);cursor:pointer}
  .social-row{display:flex;gap:12px;align-items:center;justify-content:center;margin-top:8px}
  .social-link{padding:8px 12px;border-radius:10px;background:rgba(255,255,255,0.04);font-weight:700}
  /* subtle card for text blocks */
  .card{background:rgba(255,255,255,0.02);border-radius:12px;padding:26px;box-shadow:0 30px 80px rgba(0,0,0,0.5);max-width:1000px;text-align:left}
  .card h3{color:#eaf6f8;margin:0 0 8px 0}
  .card p, .card li{color:var(--muted)}
  /* scroll indicator */
  #scroll-indicator{position:absolute;bottom:24px;left:50%;transform:translateX(-50%);z-index:11;color:#dfeef3;font-size:20px;animation:scroll-bob 1.6s infinite}
  @keyframes scroll-bob{0%{transform:translate(-50%,0)}50%{transform:translate(-50%,10px)}100%{transform:translate(-50%,0)}}
  footer{padding:16px;text-align:center;color:#cfe3ea;background:linear-gradient(180deg,transparent,rgba(0,0,0,0.08))}
  /* responsive */
  @media(max-width:980px){.float{width:78vw}.portrait{height:50vh}.menu{right:12px;left:auto;min-width:calc(100% - 32px)}}
</style>
</head>
<body>

  <!-- Hamburger menu (always visible, Apple-style transparent blur) -->
  <div class="hamburger" aria-hidden="false">
    <div class="hambutton" id="hambutton" role="button" aria-label="Open menu" aria-expanded="false" tabindex="0">☰</div>
    <nav class="menu" id="menu" aria-label="Main menu" role="navigation">
      <a href="#about" data-target="about">About Me <span class="arrow">▸</span></a>
      <a href="#experiences" data-target="experiences">Experiences <span class="arrow">▸</span></a>
      <a href="#publication" data-target="publication">Publication <span class="arrow">▸</span></a>
      <a href="#skills" data-target="skills">Skills <span class="arrow">▸</span></a>
      <a href="#contact" data-target="contact">Contact <span class="arrow">▸</span></a>
    </nav>
  </div>

  <!-- Main vertical scroll container (snap) -->
  <main id="site-main" role="main" aria-live="polite">

    <!-- HERO -->
    <section id="hero" aria-label="Hero">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content" role="region" aria-labelledby="heroTitle">
        <img src="portrait.png" alt="Portrait of Venkata Raghavendra Kadiyala" class="portrait" onerror="this.style.display='none'">
        <h1 class="title" id="heroTitle">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
        <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
        <p class="lead">☎ <a href="tel:+33755662821" style="color:#e7f7f1">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com" style="color:#e7f7f1">venkata.france@gmail.com</a></p>

        <div class="social-row" aria-hidden="false">
          <a class="social-link" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
          <a class="social-link" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
        </div>
      </div>

      <div id="scroll-indicator" aria-hidden="true">▼</div>
    </section>

    <!-- ABOUT -->
    <section id="about" aria-label="About">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card" role="article" aria-labelledby="aboutTitle">
        <h3 id="aboutTitle">About — À propos</h3>
        <p><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability with user-focused outcomes.</p>
        <p style="margin-top:10px;"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>

        <div style="margin-top:14px;">
          <strong>Responsibilities & Project Management</strong>
          <ul style="margin-top:8px; color:var(--muted); line-height:1.6;">
            <li>Project planning & scheduling</li>
            <li>Team leadership and coordination (multi-discipline)</li>
            <li>Budgeting, financing oversight and cost control</li>
            <li>Procurement & supplier buying (technical specification, negotiation)</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- EXPERIENCES - container anchor first -->
    <section id="experiences" aria-label="Experiences">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card" role="region" aria-labelledby="expTitle" style="text-align:left;">
        <h3 id="expTitle">Experiences</h3>
        <p style="color:var(--muted); margin-top:8px">Scroll down — each experience occupies one full screen. (OSTA → BaWu → RER NG → DSB → SNCF → LAMIH → PM DIMENSIONS → Indian Railways)</p>
      </div>
    </section>

    <!-- SEGULA — OSTA -->
    <section id="osta" aria-label="SEGULA OSTA">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_osta.png" alt="" style="right:6%; top:14%;" onerror="this.style.display='none'">
      <div class="content" role="article">
        <h1 class="title">SEGULA — Project OSTA</h1>
        <p class="lead">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
      </div>
    </section>

    <!-- SEGULA — BaWu -->
    <section id="bawu" aria-label="SEGULA BaWu">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_bawu.png" alt="" style="left:8%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — BaWu</h1>
        <p class="lead">3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
      </div>
    </section>

    <!-- SEGULA — RER NG -->
    <section id="rerng" aria-label="SEGULA RER NG">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_rerng.png" alt="" style="right:10%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — RER NG</h1>
        <p class="lead">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
      </div>
    </section>

    <!-- SEGULA — DSB -->
    <section id="dsb" aria-label="SEGULA DSB">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_dsb.png" alt="" style="left:6%; top:12%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — DSB</h1>
        <p class="lead">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
      </div>
    </section>

    <!-- SNCF -->
    <section id="sncf" aria-label="SNCF">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_sncf.png" alt="" style="right:8%; top:10%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SNCF</h1>
        <p class="lead">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
      </div>
    </section>

    <!-- LAMIH -->
    <section id="lamih" aria-label="LAMIH">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_lamih.png" alt="" style="left:10%; top:14%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">LAMIH</h1>
        <p class="lead">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
      </div>
    </section>

    <!-- PM DIMENSIONS -->
    <section id="pmdim" aria-label="PM DIMENSIONS">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_pmdimensions.png" alt="" style="right:8%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">PM DIMENSIONS</h1>
        <p class="lead">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
      </div>
    </section>

    <!-- Indian Railways -->
    <section id="indian" aria-label="Indian Railways">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_indianrail.png" alt="" style="left:6%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">Indian Railways (Intern)</h1>
        <p class="lead">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
      </div>
    </section>

    <!-- EDUCATION -->
    <section id="education" aria-label="Education">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card">
        <h3>Education — Formation</h3>
        <p style="color:var(--muted);margin-top:8px"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)</p>
        <p style="color:var(--muted);margin-top:8px"><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" aria-label="Skills">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card">
        <h3>Skills & Tools — Compétences</h3>
        <ul style="margin-top:8px;color:var(--muted);line-height:1.6">
          <li>CATIA V5, Ansys, HyperWorks / OptiStruct</li>
          <li>FEA, CAD Automation, PDM / DMA / SAM</li>
          <li>Project planning · Team leadership · Budgeting & procurement</li>
        </ul>
      </div>
    </section>

    <!-- PUBLICATION -->
    <section id="publication" aria-label="Publication">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card" style="text-align:left">
        <h3>Publication — Avril 2018</h3>
        <p style="color:var(--muted);margin-top:8px">Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018.</p>
        <div style="margin-top:18px">
          <a class="btn" href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" aria-label="Contact">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content">
        <h1 class="title">Let's build something exceptional — Parlons</h1>
        <p class="lead">Email: <a href="mailto:venkata.france@gmail.com" style="color:#e7f7f1">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#e7f7f1">+33 7 55 66 28 21</a></p>
        <div class="social-row" style="margin-top:14px">
          <a class="social-link" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
          <a class="social-link" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
        </div>
      </div>
    </section>

  </main>

  <footer>© Kadiyala Venkata Raghavendra</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
/* Menu behavior + scroll + GSAP reveal + parallax. */

(() => {
  // menu open/close
  const hambutton = document.getElementById('hambutton');
  const menu = document.getElementById('menu');
  const main = document.getElementById('site-main');

  function toggleMenu(open){
    if(open){
      menu.classList.add('open');
      hambutton.setAttribute('aria-expanded','true');
    } else {
      menu.classList.remove('open');
      hambutton.setAttribute('aria-expanded','false');
    }
  }

  hambutton.addEventListener('click', ()=> toggleMenu(!menu.classList.contains('open')));
  hambutton.addEventListener('keydown', (e)=> { if(e.key==='Enter' || e.key===' ') { e.preventDefault(); toggleMenu(!menu.classList.contains('open')); }});

  // menu links scroll
  menu.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', (ev) => {
      ev.preventDefault();
      const target = document.getElementById(a.getAttribute('data-target'));
      toggleMenu(false);
      if(target){
        target.scrollIntoView({behavior:'smooth', block:'start'});
      }
    });
  });

  // clicking outside menu closes it
  document.addEventListener('click', (e) => {
    if(!menu.contains(e.target) && !hambutton.contains(e.target) && menu.classList.contains('open')) toggleMenu(false);
  });

  // GSAP animations
  try {
    gsap.registerPlugin(ScrollTrigger);

    // reveal each section's content
    document.querySelectorAll('main section').forEach(sec => {
      const content = sec.querySelector('.content');
      const floatEl = sec.querySelector('.float');
      const backdrop = sec.querySelector('.backdrop');

      if(content){
        gsap.fromTo(content, {y:30, autoAlpha:0}, {
          y:0, autoAlpha:1, duration:0.9, ease:'power3.out',
          scrollTrigger: { trigger: sec, start: 'top 70%', toggleActions: 'play none none reverse' }
        });
      }

      if(floatEl){
        // small parallax tied to scroll
        gsap.to(floatEl, {
          y: (Math.random()>0.5? -36:36),
          x: (Math.random()>0.5? 18:-18),
          ease:'sine.inOut',
          scrollTrigger: { trigger: sec, start: 'top bottom', end: 'bottom top', scrub:1 }
        });
      }

      if(backdrop){
        gsap.to(backdrop, {
          yPercent:6, ease:'none',
          scrollTrigger: { trigger: sec, start: 'top bottom', end: 'bottom top', scrub:0.6 }
        });
      }
    });

    // hide scroll indicator after first scroll
    const scInd = document.getElementById('scroll-indicator');
    if(scInd){
      ScrollTrigger.create({
        start: 30,
        onEnter: ()=> gsap.to(scInd, {autoAlpha:0, duration:0.45})
      });
    }
  } catch(e){ console.error('GSAP failed: ', e); }

  // ensure keyboard navigation works with snap (PageUp / PageDown / Arrow keys)
  window.addEventListener('keydown', (e) => {
    const sections = Array.from(document.querySelectorAll('main section'));
    const top = document.documentElement.scrollTop || document.body.scrollTop || document.querySelector('main').scrollTop;
    const vh = window.innerHeight;
    if(['ArrowDown','PageDown'].includes(e.key)){
      e.preventDefault();
      const cur = Math.round(top / vh);
      const next = Math.min(sections.length-1, cur+1);
      sections[next].scrollIntoView({behavior:'smooth'});
    } else if(['ArrowUp','PageUp'].includes(e.key)){
      e.preventDefault();
      const cur = Math.round(top / vh);
      const prev = Math.max(0, cur-1);
      sections[prev].scrollIntoView({behavior:'smooth'});
    }
  });

})();
</script>
</body>
</html>
