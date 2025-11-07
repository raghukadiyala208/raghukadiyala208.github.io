<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<meta name="description" content="Portfolio of Venkata Raghavendra KADIYALA — Mechanical Engineer & Creative Designer (EN/FR)" />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --white:#ffffff;
    --muted:#6f7b82;
    --accent-teal:#17c3a2;
    --accent-gold:#e6b66d;
    --linkedin:#0077b5;
    --snap-duration:700ms;
    --font:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;
  }
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; font-family:var(--font); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale; background:#fff; color:#071622}
  a{color:inherit; text-decoration:none}
  /* App is single-view; panels are absolute and we show one at a time */
  #app { height:100vh; width:100vw; overflow:hidden; position:relative; }
  .panel {
    position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
    /* start hidden */
    opacity:0; transform: translateY(30px) scale(.996); pointer-events:none;
    transition: opacity var(--snap-duration) cubic-bezier(.2,.9,.2,1), transform var(--snap-duration) cubic-bezier(.2,.9,.2,1);
    will-change: opacity, transform;
    overflow:hidden;
  }
  .panel.active { opacity:1; transform: translateY(0) scale(1); pointer-events:auto; z-index:20; }

  /* Stage: full-bleed content centered */
  .stage { width:100%; max-width:1400px; margin:0 auto; padding:40px; height:100%; display:flex; align-items:center; justify-content:center; position:relative; }

  /* HERO */
  .hero { background: linear-gradient(180deg,#fff,#fbfbfd); }
  .hero-inner { text-align:center; display:flex; flex-direction:column; gap:28px; align-items:center; }
  .portrait {
    width:380px; height:540px; /* portrait taller to feel floating "in air" */
    background:transparent; overflow:visible; display:block; transform:translateY(-6px);
    filter: drop-shadow(0 32px 60px rgba(7,20,34,0.12));
    will-change:transform;
  }
  .portrait img{ width:auto; height:100%; display:block; margin:0 auto; object-fit:contain; background:transparent; }
  /* make portrait float slightly */
  .portrait.float { animation: floaty 6s ease-in-out infinite; }
  @keyframes floaty { 0%{ transform: translateY(-6px) } 50%{ transform: translateY(8px) } 100%{ transform: translateY(-6px) } }

  .hero-name { font-weight:900; font-size:clamp(44px, 8vw, 110px); letter-spacing:-1px; line-height:0.88; text-transform:uppercase; margin:0; }
  .hero-tag { font-weight:700; color:var(--muted); margin-top:6px; font-size:18px; }

  /* social buttons natural brand colors */
  .social-row { display:flex; gap:14px; align-items:center; justify-content:center; margin-top:12px; flex-wrap:wrap; }
  .btn { display:inline-flex; align-items:center; gap:10px; padding:12px 18px; border-radius:14px; font-weight:800; cursor:pointer; box-shadow:0 18px 50px rgba(10,20,28,0.08); }
  .btn.linkedin { background:var(--linkedin); color:white; }
  .btn.instagram { background: linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5); color:white; }
  .btn.contact { background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold)); color:#072425; }

  /* About panel: light card style */
  .about-card { width:100%; max-width:1100px; background:#fff; border-radius:16px; padding:46px; box-shadow:0 30px 80px rgba(8,12,18,0.06); display:grid; grid-template-columns:1fr 420px; gap:28px; align-items:center; }
  .about-text h2{ margin:0; font-size:32px; font-weight:900; }
  .about-text p{ margin-top:14px; color:var(--muted); line-height:1.7; font-size:16px; }
  .highlights { display:flex; gap:18px; margin-top:20px; flex-wrap:wrap; }
  .stat { background:linear-gradient(180deg,#fff,#f6f7f8); padding:16px; min-width:140px; border-radius:12px; text-align:center; box-shadow:0 12px 36px rgba(10,18,24,0.06); }
  .stat .num { font-weight:900; font-size:20px; }

  /* Work panels: full-screen background image + centered text block */
  .work-stage { width:100%; height:100%; display:flex; align-items:center; justify-content:center; position:relative; }
  .work-bg { position:absolute; inset:0; background-size:cover; background-position:center; transform:scale(1.04); transition: transform 1200ms ease; will-change:transform; }
  .work-stage.active .work-bg { transform:scale(1); }
  .work-card { position:relative; z-index:5; max-width:980px; padding:28px; border-radius:12px; background:linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.02)); color:#fff; text-align:center; box-shadow:0 30px 80px rgba(0,0,0,0.6); }
  .work-title { font-size:38px; font-weight:900; margin:0 0 6px 0; text-shadow:0 12px 36px rgba(0,0,0,0.6); }
  .work-sub { font-weight:700; opacity:0.92; margin-bottom:12px; }
  .work-desc { line-height:1.6; opacity:0.95; font-size:18px; }

  /* Skill & Education panels */
  .full-card { width:100%; max-width:980px; padding:36px; border-radius:12px; background:linear-gradient(180deg,#fff,#fbfbfd); box-shadow:0 30px 80px rgba(8,12,18,0.06); text-align:center; }
  .grid-tiles { display:flex; gap:18px; justify-content:center; flex-wrap:wrap; margin-top:18px; }

  /* Contact final */
  .contact-panel { display:flex; flex-direction:column; gap:18px; align-items:center; justify-content:center; text-align:center; color:#eef6f8; }
  .contact-panel h2 { font-size:36px; font-weight:900; margin:0; }

  /* make transitions feel product-like when panels change */
  .panel.hide-when-active { pointer-events:none; }

  /* responsive */
  @media (max-width:980px){
    .portrait{ width:260px; height:370px; }
    .about-card { grid-template-columns:1fr; padding:28px; }
    .hero-name { font-size: clamp(36px, 12vw, 64px); }
    .work-title { font-size:30px; }
  }
</style>
</head>
<body>
<div id="app" aria-live="polite">
  <!-- top-right small contact quick -->
  <div style="position:fixed;top:18px;right:18px;z-index:60;display:flex;gap:10px;align-items:center">
    <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">LinkedIn</a>
    <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener noreferrer" aria-label="Instagram">Instagram</a>
  </div>

  <!-- Panels: one per experience + hero + about + skills + education + contact -->
  <!-- Panel index order below: 0 hero, 1 about, 2 SEGULA OSTA, 3 SEGULA BaWu, 4 SEGULA RER NG, 5 SEGULA DSB, 6 SNCF, 7 LAMIH, 8 PM DIMENSIONS, 9 Indian Railways, 10 Education, 11 Skills, 12 Contact -->
  <section id="p-0" class="panel active hero" role="region" aria-label="Hero panel">
    <div class="stage">
      <div class="hero-inner" aria-hidden="false">
        <div class="portrait float" aria-hidden="false">
          <!-- Professional realistic T-shirt portrait: replace portrait.png with your image (transparent background recommended) -->
          <img src="portrait.png" alt="Portrait of Venkata Raghavendra Kadiyala" loading="eager" id="portraitMain">
        </div>
        <h1 class="hero-name">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
        <div class="hero-tag">Mechanical Engineer & Creative Designer — Train interiors • CAD • FEA</div>

        <div class="social-row">
          <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">LinkedIn</a>
          <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank">Instagram</a>
          <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
        </div>

        <div style="margin-top:10px; color:var(--muted); font-weight:700">☎ +33 7 55 66 28 21 &nbsp; • &nbsp; venkata.france@gmail.com</div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="p-1" class="panel" role="region" aria-label="About panel">
    <div class="stage">
      <div class="about-card" role="article" aria-labelledby="aboutTitle">
        <div class="about-text">
          <div id="aboutTitle" style="font-weight:900; font-size:20px; color:var(--text-dark)">About — À propos</div>
          <h2 style="margin-top:12px; font-size:28px; font-weight:900">Design-minded engineering — clarity and craft</h2>
          <p>
            <strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability and clear user-focused outcomes.<br><br>
            <strong>Français :</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.
          </p>

          <div class="highlights" aria-hidden="true">
            <div class="stat"><div class="num">5+</div><div class="label" style="color:var(--muted);font-weight:700">Years experience</div></div>
            <div class="stat"><div class="num">M0 → M5</div><div class="label" style="color:var(--muted);font-weight:700">Model maturity</div></div>
            <div class="stat"><div class="num">CATIA V5</div><div class="label" style="color:var(--muted);font-weight:700">CAD & FEA</div></div>
          </div>
        </div>

        <aside style="display:flex;align-items:center;justify-content:center">
          <!-- optional subtle about background: replace ai_about.jpg if available -->
          <div style="width:340px; height:260px; border-radius:12px; overflow:hidden; background:linear-gradient(180deg,#f6f7f8,#fff); box-shadow:0 12px 30px rgba(8,12,18,0.06); display:flex; align-items:center; justify-content:center">
            <img src="ai_about.jpg" alt="" style="width:100%; height:100%; object-fit:cover; opacity:0.95" loading="lazy">
          </div>
        </aside>
      </div>
    </div>
  </section>

  <!-- EXPERIENCES: each experience gets its own panel. background image fills the panel (sharp) -->
  <!-- SEGULA — Project OSTA -->
  <section id="p-2" class="panel" role="region" aria-label="SEGULA Project OSTA"
    style="background-image:url('ai_osta.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_osta.jpg');"></div>
      <div class="work-card" role="article" style="backdrop-filter: blur(6px); background:linear-gradient(180deg, rgba(2,6,8,0.45), rgba(2,6,8,0.22));">
        <div class="work-title">SEGULA — Project OSTA</div>
        <div class="work-sub">Front office • Train interior systems • M0 → M5</div>
        <p class="work-desc">Design and development of interior components (windows, blinds, sidewalls, intercoms, electrical cabinets, emergency handles, toilet piping, under-seat boxes). Delivery of validated 3D models (SAM) and coordination with suppliers and CDS Interiors.</p>
      </div>
    </div>
  </section>

  <!-- SEGULA — BaWu -->
  <section id="p-3" class="panel" role="region" aria-label="SEGULA BaWu"
    style="background-image:url('ai_bawu.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_bawu.jpg');"></div>
      <div class="work-card">
        <div class="work-title">SEGULA — BaWu</div>
        <div class="work-sub">Validation & QA — Integration focus</div>
        <p class="work-desc">3D design validation; identification and prevention of integration issues; QA management with KPI/OIL tracking; CAD governance and supplier validation processes.</p>
      </div>
    </div>
  </section>

  <!-- SEGULA — RER NG (Change request) -->
  <section id="p-4" class="panel" role="region" aria-label="SEGULA RER NG"
    style="background-image:url('ai_rerng.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_rerng.jpg');"></div>
      <div class="work-card">
        <div class="work-title">SEGULA — RER NG</div>
        <div class="work-sub">Change request engineering & on-site surveys</div>
        <p class="work-desc">Requirements analysis, mechanical integration resolution, on-site surveys, and structural part design in CATIA V5 with criticality reporting to client and industrial teams.</p>
      </div>
    </div>
  </section>

  <!-- SEGULA — DSB (Back office) -->
  <section id="p-5" class="panel" role="region" aria-label="SEGULA DSB"
    style="background-image:url('ai_dsb.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_dsb.jpg');"></div>
      <div class="work-card">
        <div class="work-title">SEGULA — DSB</div>
        <div class="work-sub">Back office • Interior layout & integration</div>
        <p class="work-desc">Interior layouts, seat arrangements, under-seat box design, cantilever and ceiling integration, and delivery of 3D/2D/FTA models with CDS Interiors.</p>
      </div>
    </div>
  </section>

  <!-- SNCF -->
  <section id="p-6" class="panel" role="region" aria-label="SNCF"
    style="background-image:url('ai_sncf.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_sncf.jpg');"></div>
      <div class="work-card">
        <div class="work-title">SNCF</div>
        <div class="work-sub">FEA & Automation — Hyperworks / Optistruct</div>
        <p class="work-desc">Automation of bolted assemblies using TCL; mesh, static and non-static analysis for seat supports (Thalys); modelling in CATIA V5 and validation of structural results.</p>
      </div>
    </div>
  </section>

  <!-- LAMIH -->
  <section id="p-7" class="panel" role="region" aria-label="LAMIH"
    style="background-image:url('ai_lamih.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_lamih.jpg');"></div>
      <div class="work-card">
        <div class="work-title">LAMIH</div>
        <div class="work-sub">Behavioural analysis & safety concepts</div>
        <p class="work-desc">Accident analysis, automated solutions for signalling and prevention, data analysis and concepts for autonomous trains (ETCS / CBTC).</p>
      </div>
    </div>
  </section>

  <!-- PM DIMENSIONS -->
  <section id="p-8" class="panel" role="region" aria-label="PM DIMENSIONS"
    style="background-image:url('ai_pmdimensions.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_pmdimensions.jpg');"></div>
      <div class="work-card">
        <div class="work-title">PM DIMENSIONS</div>
        <div class="work-sub">Part design & prototyping</div>
        <p class="work-desc">Design and verification of mechanical parts, 3D CAD modelling (CATIA V5), prototype development and project support for clients (Hyundai).</p>
      </div>
    </div>
  </section>

  <!-- Indian Railways internship -->
  <section id="p-9" class="panel" role="region" aria-label="Indian Railways internship"
    style="background-image:url('ai_indianrail.jpg'); background-size:cover; background-position:center;">
    <div class="stage work-stage">
      <div class="work-bg" aria-hidden="true" style="background-image:url('ai_indianrail.jpg');"></div>
      <div class="work-card">
        <div class="work-title">Indian Railways (Intern)</div>
        <div class="work-sub">Prototype coupling & maintenance optimisation</div>
        <p class="work-desc">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys modelling / structural analysis.</p>
      </div>
    </div>
  </section>

  <!-- EDUCATION -->
  <section id="p-10" class="panel" role="region" aria-label="Education" style="background:linear-gradient(180deg,#fff,#f1f3f4);">
    <div class="stage">
      <div class="full-card">
        <h2 style="margin:0; font-weight:900">Education — Formation</h2>
        <div style="margin-top:16px; color:var(--muted); font-weight:700">
          <div style="margin-bottom:8px;"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019 — 2021)</div>
          <div><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014 — 2018)</div>
        </div>
        <div style="margin-top:14px; color:var(--muted)">Selected project: Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018</div>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="p-11" class="panel" role="region" aria-label="Skills" style="background:linear-gradient(180deg,#fff,#f6f7f8);">
    <div class="stage">
      <div class="full-card">
        <h2 style="margin:0; font-weight:900">Skills & Tools — Compétences</h2>
        <div class="grid-tiles" style="margin-top:18px;">
          <div style="padding:14px; border-radius:12px; background:#fff; min-width:180px; box-shadow:0 12px 36px rgba(8,12,18,0.06)"><strong>CATIA V5</strong></div>
          <div style="padding:14px; border-radius:12px; background:#fff; min-width:180px; box-shadow:0 12px 36px rgba(8,12,18,0.06)"><strong>Ansys</strong></div>
          <div style="padding:14px; border-radius:12px; background:#fff; min-width:180px; box-shadow:0 12px 36px rgba(8,12,18,0.06)"><strong>Hyperworks / Optistruct</strong></div>
          <div style="padding:14px; border-radius:12px; background:#fff; min-width:180px; box-shadow:0 12px 36px rgba(8,12,18,0.06)"><strong>PDM / SAM / CDS Interiors</strong></div>
          <div style="padding:14px; border-radius:12px; background:#fff; min-width:180px; box-shadow:0 12px 36px rgba(8,12,18,0.06)"><strong>C • Java • TCL</strong></div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="p-12" class="panel" role="region" aria-label="Contact" style="background:linear-gradient(180deg,#071219,#031018);">
    <div class="stage">
      <div class="contact-card" style="text-align:center; padding:36px; border-radius:12px;">
        <h2 style="margin:0; color:#eef6f8; font-weight:900">Let's build something exceptional — Parlons</h2>
        <p style="margin-top:14px; color:rgba(238,246,248,0.9)">Email: <a href="mailto:venkata.france@gmail.com" style="color:#fff">venkata.france@gmail.com</a> — Phone: <a href="tel:+33755662821" style="color:#fff">+33 7 55 66 28 21</a></p>
        <div style="margin-top:18px; display:flex; gap:12px; justify-content:center; align-items:center; flex-wrap:wrap;">
          <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">LinkedIn</a>
          <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank">Instagram</a>
          <a class="btn contact" href="mailto:venkata.france@gmail.com">Email me</a>
        </div>
        <div style="margin-top:18px; color:rgba(238,246,248,0.6)">© <span id="year"></span> Venkata Raghavendra KADIYALA</div>
      </div>
    </div>
  </section>

</div>

<script>
/* Panel controller: shows exactly one panel at a time, keyboard/wheel/touch navigation,
   panel transition is locked while animating to avoid overlap. Panels are absolute, so
   user never sees other panels while current is active. */

(function(){
  const ids = [
    'p-0','p-1','p-2','p-3','p-4','p-5','p-6','p-7','p-8','p-9','p-10','p-11','p-12'
  ];
  const panels = ids.map(id => document.getElementById(id));
  let index = 0;
  let animating = false;
  const duration = 720;

  function show(i){
    if(i < 0 || i >= panels.length) return;
    if(animating) return;
    animating = true;
    panels.forEach((p, idx) => {
      if(idx === i){
        p.classList.add('active');
        p.style.zIndex = 20;
        // add active class for work-stage background subtle zoom
        const ws = p.querySelector('.work-stage');
        if(ws) ws.classList.add('active');
      } else {
        p.classList.remove('active');
        p.style.zIndex = 1;
        const ws = p.querySelector('.work-stage');
        if(ws) ws.classList.remove('active');
      }
    });
    index = i;
    // small delay + reserve for animation
    setTimeout(()=> animating = false, duration + 80);
  }

  // init
  show(0);

  // wheel navigation (throttle)
  let wheelLock = false;
  window.addEventListener('wheel', (e) => {
    if(wheelLock || animating) return;
    wheelLock = true;
    setTimeout(()=> wheelLock = false, 400);
    if(e.deltaY > 8) next();
    if(e.deltaY < -8) prev();
  }, {passive:true});

  // keyboard navigation
  window.addEventListener('keydown', (e) => {
    if(e.key === 'ArrowDown' || e.key === 'PageDown') next();
    if(e.key === 'ArrowUp' || e.key === 'PageUp') prev();
    if(e.key === 'Home') show(0);
    if(e.key === 'End') show(panels.length-1);
  });

  // touch swipe
  let startY = null;
  window.addEventListener('touchstart', (ev) => { startY = ev.touches[0].clientY; }, {passive:true});
  window.addEventListener('touchend', (ev) => {
    if(startY === null) return;
    const dy = ev.changedTouches[0].clientY - startY;
    if(Math.abs(dy) > 60){
      if(dy < 0) next();
      else prev();
    }
    startY = null;
  }, {passive:true});

  function next(){ show(Math.min(panels.length - 1, index + 1)); }
  function prev(){ show(Math.max(0, index - 1)); }

  // clickable navigation (optional) — map topbar LinkedIn to keep visible; don't change panels.
  // set year
  document.getElementById('year').textContent = new Date().getFullYear();

  // graceful fallback: if portrait fails to load, show initials floating block
  const portrait = document.getElementById('portraitMain');
  if(portrait){
    portrait.addEventListener('error', function(){
      const wrap = portrait.parentElement;
      wrap.innerHTML = '<div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,var(--accent-teal),var(--accent-gold));color:#052425;font-weight:900;font-size:64px;">VR</div>';
    });
  }

})();
</script>
</body>
</html>
