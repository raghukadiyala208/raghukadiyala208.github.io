<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<meta name="description" content="Cinematic portfolio of Venkata Raghavendra KADIYALA — Mechanical Engineer & Creative Designer (EN/FR)" />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --day-1: #ffffff;
    --day-2: #f2f6f8;
    --sunset-1: #fff5ee;
    --sunset-2: #f1e6d6;
    --night-1: #061018;
    --night-2: #031018;
    --linkedin:#0077b5;
    --muted:#6b7780;
    --accent-teal:#17c3a2;
    --accent-gold:#e6b66d;
    --font:Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;
  }
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; font-family:var(--font); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale; background:var(--day-1); color:#071622;}
  a{color:inherit; text-decoration:none}

  /* App root: absolute panels, show only one panel at a time */
  #app{position:relative; height:100vh; width:100vw; overflow:hidden;}
  .panel {
    position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
    opacity:0; transform: translateY(30px) scale(.996); pointer-events:none;
    transition:opacity .6s ease, transform .6s cubic-bezier(.2,.9,.2,1);
    will-change:opacity, transform;
  }
  .panel.is-active{ opacity:1; transform:translateY(0) scale(1); pointer-events:auto; z-index:10; }

  /* stage centers content */
  .stage{ width:100%; max-width:1300px; margin:0 auto; padding:28px; height:100%; display:flex; align-items:center; justify-content:center; position:relative; }

  /* hero */
  .hero { text-align:center; }
  .portrait { display:block; width:auto; height:62vh; max-height:760px; filter: drop-shadow(0 40px 90px rgba(7,20,34,0.18)); }
  .hero-name { font-weight:900; font-size:clamp(40px,8vw,100px); letter-spacing:-1px; line-height:0.92; text-transform:uppercase; margin:18px 0 6px; }
  .hero-sub { color:var(--muted); font-weight:700; margin-bottom:12px; }

  /* social row */
  .social-row{ display:flex; gap:12px; justify-content:center; margin-top:8px; flex-wrap:wrap; }
  .btn { display:inline-flex; align-items:center; gap:10px; padding:12px 16px; border-radius:12px; font-weight:800; cursor:pointer; color:white; }
  .btn.linkedin{ background:var(--linkedin); box-shadow:0 12px 36px rgba(0,119,181,0.14); }
  .btn.instagram{ background:linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5); box-shadow:0 12px 36px rgba(150,43,191,0.12); }
  .btn.contact{ background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold)); color:#052425; box-shadow:0 18px 50px rgba(22,44,40,0.12); }

  /* About panel card */
  .about-card{ width:100%; max-width:1100px; background:rgba(255,255,255,0.98); border-radius:16px; padding:40px; box-shadow:0 30px 80px rgba(8,12,18,0.06); display:grid; grid-template-columns:1fr 380px; gap:24px; align-items:center;}
  .about-title{ font-weight:900; font-size:22px; }
  .about-text p{ color:var(--muted); line-height:1.7; }

  /* Work panels: background covers whole panel, overlays float */
  .work-stage{ width:100%; height:100%; position:relative; display:flex; align-items:center; justify-content:center; }
  .bg-image{ position:absolute; inset:0; background-size:cover; background-position:center; transform:scale(1.04); transition:transform 1400ms ease; }
  .work-stage.is-active .bg-image{ transform:scale(1); }
  .work-card{ position:relative; z-index:6; max-width:980px; padding:28px; border-radius:12px; background:linear-gradient(180deg, rgba(0,0,0,0.42), rgba(0,0,0,0.12)); color:#fff; text-align:center; box-shadow:0 30px 90px rgba(0,0,0,0.6); }
  .work-title{ font-size:40px; font-weight:900; margin:0 0 8px; text-shadow:0 12px 36px rgba(0,0,0,0.6); }
  .work-sub{ color:rgba(255,255,255,0.95); font-weight:700; margin-bottom:10px; }
  .work-desc{ color:rgba(255,255,255,0.93); line-height:1.6; font-size:17px; }

  /* floating overlay images (realistic PNGs): appear in foreground and drift */
  .float-img{
    position:absolute; z-index:8; pointer-events:none; will-change:transform, opacity;
    width:36vw; max-width:680px; opacity:0.98; transform-origin:center;
    filter: drop-shadow(0 20px 60px rgba(2,6,10,0.45));
  }
  /* smaller for mobile */
  @media(max-width:980px){ .float-img{ width:72vw; max-width:520px; } .work-title{ font-size:28px;} .portrait{ height:52vh; } }

  /* full-screen card style for education/skills/publications/certifications/contact */
  .full-card{ width:100%; max-width:980px; padding:36px; border-radius:12px; text-align:center; background:linear-gradient(180deg, rgba(255,255,255,0.98), rgba(255,255,255,0.96)); box-shadow:0 30px 80px rgba(8,12,18,0.06); }

  /* dark contact */
  .contact-card{ width:100%; max-width:920px; padding:36px; border-radius:12px; text-align:center; background:linear-gradient(180deg,#061018,#031018); color:#eef6f8; box-shadow:0 40px 100px rgba(0,0,0,0.6); }

  /* accessibility focus */
  a:focus{ outline:3px solid rgba(23,195,162,0.16); outline-offset:4px; border-radius:8px; }

</style>
</head>
<body>
<div id="app" aria-live="polite">
  <!-- Top small nav (keeps social visible) -->
  <div style="position:fixed;top:14px;left:18px;z-index:80"><strong style="font-weight:800">VR</strong></div>
  <div style="position:fixed;top:14px;right:18px;z-index:80;display:flex;gap:8px;">
    <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener" aria-label="LinkedIn">LinkedIn</a>
    <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener" aria-label="Instagram">Instagram</a>
  </div>

  <!-- Panels (one per scene) -->
  <!-- Panel 0: HERO -->
  <section id="panel-0" class="panel is-active" data-index="0" aria-label="Hero">
    <div class="stage hero">
      <div>
        <!-- floating portrait (no visible box) -->
        <img src="portrait.png" alt="Portrait of Venkata Raghavendra Kadiyala" class="portrait" id="portrait" loading="eager">
        <h1 class="hero-name">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
        <div class="hero-sub">Mechanical Engineer • Creative Designer — Train Interiors & Systems</div>

        <div class="social-row">
          <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">LinkedIn</a>
          <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank">Instagram</a>
          <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
        </div>

        <div style="margin-top:14px;color:var(--muted);font-weight:700">☎ +33 7 55 66 28 21 &nbsp; • &nbsp; venkata.france@gmail.com</div>
      </div>
    </div>
  </section>

  <!-- Panel 1: ABOUT -->
  <section id="panel-1" class="panel" data-index="1" aria-label="About">
    <div class="stage">
      <div class="about-card" role="article">
        <div>
          <div class="about-title">About — À propos</div>
          <h2 style="margin-top:12px; font-size:28px; font-weight:900">Design-minded engineering — clarity and craft</h2>
          <div class="about-text">
            <p><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability and clear user-focused outcomes.</p>
            <p style="margin-top:12px;"><strong>Français :</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>
          </div>
        </div>

        <aside>
          <div style="width:320px; height:220px; border-radius:12px; overflow:hidden; background:#f6f7f8; display:flex;align-items:center;justify-content:center;">
            <img src="ai_about.jpg" alt="" style="width:100%; height:100%; object-fit:cover;" loading="lazy">
          </div>
        </aside>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE PANELS: each full-screen, separate -->
  <!-- Panel 2: SEGULA — OSTA -->
  <section id="panel-2" class="panel" data-index="2" aria-label="SEGULA OSTA">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_osta.jpg');"></div>
      <img src="float_osta.png" class="float-img" style="right:5%; top:12%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">SEGULA — Project OSTA</div>
        <div class="work-sub">Front office • Train interior systems • M0 → M5</div>
        <p class="work-desc">Design and development of interior components (windows, blinds, sidewalls, intercoms, electrical cabinets, emergency handles, toilet piping, under-seat boxes). Delivery of validated 3D models (SAM) and supplier coordination.</p>
      </div>
    </div>
  </section>

  <!-- Panel 3: SEGULA — BaWu -->
  <section id="panel-3" class="panel" data-index="3" aria-label="SEGULA BaWu">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_bawu.jpg');"></div>
      <img src="float_bawu.png" class="float-img" style="left:8%; top:16%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">SEGULA — BaWu</div>
        <div class="work-sub">Validation & QA — Integration focus</div>
        <p class="work-desc">3D design validation, integration issue identification and prevention, QA management, KPI & OIL tracking, and CAD governance to ensure industrial handover quality.</p>
      </div>
    </div>
  </section>

  <!-- Panel 4: SEGULA — RER NG -->
  <section id="panel-4" class="panel" data-index="4" aria-label="SEGULA RER NG">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_rerng.jpg');"></div>
      <img src="float_rerng.png" class="float-img" style="right:10%; top:18%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">SEGULA — RER NG</div>
        <div class="work-sub">Change request engineering & on-site surveys</div>
        <p class="work-desc">Requirements analysis, mechanical integration resolution, site surveys and design of structural components in CATIA V5 with criticality reporting.</p>
      </div>
    </div>
  </section>

  <!-- Panel 5: SEGULA — DSB -->
  <section id="panel-5" class="panel" data-index="5" aria-label="SEGULA DSB">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_dsb.jpg');"></div>
      <img src="float_dsb.png" class="float-img" style="left:6%; top:12%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">SEGULA — DSB (Back office)</div>
        <div class="work-sub">Interior layout & integration</div>
        <p class="work-desc">Seat layout planning, under-seat boxes, cantilever and ceiling integration, 3D/2D/FTA modelling, and multi-discipline coordination for supplier deliverables.</p>
      </div>
    </div>
  </section>

  <!-- Panel 6: SNCF -->
  <section id="panel-6" class="panel" data-index="6" aria-label="SNCF">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_sncf.jpg');"></div>
      <img src="float_sncf.png" class="float-img" style="right:8%; top:10%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">SNCF</div>
        <div class="work-sub">FEA & Automation — Hyperworks / OptiStruct</div>
        <p class="work-desc">Automation of bolted assemblies with TCL, meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation with HyperWorks/OptiStruct.</p>
      </div>
    </div>
  </section>

  <!-- Panel 7: LAMIH -->
  <section id="panel-7" class="panel" data-index="7" aria-label="LAMIH">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_lamih.jpg');"></div>
      <img src="float_lamih.png" class="float-img" style="left:10%; top:14%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">LAMIH</div>
        <div class="work-sub">Behavioural analysis & safety concepts</div>
        <p class="work-desc">Accident analysis, proposals for signalling automation and prevention, data analysis and concepts for autonomous trains (ETCS / CBTC).</p>
      </div>
    </div>
  </section>

  <!-- Panel 8: PM DIMENSIONS -->
  <section id="panel-8" class="panel" data-index="8" aria-label="PM DIMENSIONS">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_pmdimensions.jpg');"></div>
      <img src="float_pmdimensions.png" class="float-img" style="right:8%; top:16%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">PM DIMENSIONS</div>
        <div class="work-sub">Part design & prototyping</div>
        <p class="work-desc">Part design for automotive components, 3D modelling (CATIA V5), prototype development and client conformity checks (Hyundai).</p>
      </div>
    </div>
  </section>

  <!-- Panel 9: Indian Railways internship -->
  <section id="panel-9" class="panel" data-index="9" aria-label="Indian Railways">
    <div class="stage work-stage">
      <div class="bg-image" style="background-image:url('ai_indianrail.jpg');"></div>
      <img src="float_indianrail.png" class="float-img" style="left:6%; top:16%;" alt="" loading="lazy">
      <div class="work-card">
        <div class="work-title">Indian Railways (Intern)</div>
        <div class="work-sub">Prototype coupling & maintenance optimisation</div>
        <p class="work-desc">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys modelling and structural analysis.</p>
      </div>
    </div>
  </section>

  <!-- Panel 10: Education -->
  <section id="panel-10" class="panel" data-index="10" aria-label="Education">
    <div class="stage">
      <div class="full-card" role="article">
        <h2 style="margin:0; font-weight:900">Education — Formation</h2>
        <div style="margin-top:14px; color:var(--muted); font-weight:700">
          <div style="margin-bottom:8px;"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019 — 2021)</div>
          <div><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014 — 2018)</div>
        </div>
        <div style="margin-top:12px; color:var(--muted)">Selected project: Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018</div>
      </div>
    </div>
  </section>

  <!-- Panel 11: Skills -->
  <section id="panel-11" class="panel" data-index="11" aria-label="Skills">
    <div class="stage">
      <div class="full-card">
        <h2 style="margin:0; font-weight:900">Skills & Tools — Compétences</h2>
        <div style="display:flex; gap:12px; margin-top:18px; flex-wrap:wrap; justify-content:center;">
          <div style="padding:12px 16px; border-radius:10px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06);"><strong>CATIA V5</strong></div>
          <div style="padding:12px 16px; border-radius:10px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06);"><strong>Ansys</strong></div>
          <div style="padding:12px 16px; border-radius:10px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06);"><strong>HyperWorks / OptiStruct</strong></div>
          <div style="padding:12px 16px; border-radius:10px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06);"><strong>PDM / DMA / SAM</strong></div>
          <div style="padding:12px 16px; border-radius:10px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06);"><strong>TCL • C • Java</strong></div>
        </div>
        <div style="margin-top:18px; color:var(--muted); line-height:1.6; text-align:left;">
          <ul>
            <li>Train interiors design & integration • Conception et intégration d’intérieurs ferroviaires</li>
            <li>Vehicle part design & packaging • Conception de pièces et intégration automobile</li>
            <li>FEA, meshing, static & dynamic analysis • Maillage, analyses statique & dynamique</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Panel 12: Publication -->
  <section id="panel-12" class="panel" data-index="12" aria-label="Publication">
    <div class="stage">
      <div class="full-card" style="text-align:left;">
        <h2 style="margin:0; font-weight:900">Publication — Publication</h2>
        <div style="margin-top:12px; color:var(--muted);">
          <strong>Enhancement of Refrigeration Effect Using Flue Gases from Chimney</strong> — April 2018.<br>
          A study on increasing refrigeration effect using flue gases from a chimney. <a href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the full paper (IAEME)</a>.
        </div>
      </div>
    </div>
  </section>

  <!-- Panel 13: Certifications -->
  <section id="panel-13" class="panel" data-index="13" aria-label="Certifications">
    <div class="stage">
      <div class="full-card">
        <h2 style="margin:0; font-weight:900">Certifications</h2>
        <div style="margin-top:14px; color:var(--muted); display:flex; gap:12px; justify-content:center; flex-wrap:wrap;">
          <div style="padding:12px 18px; border-radius:12px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>CATIA V5</strong></div>
          <div style="padding:12px 18px; border-radius:12px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>Ansys (FEA)</strong></div>
          <div style="padding:12px 18px; border-radius:12px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>HyperWorks / OptiStruct</strong></div>
          <div style="padding:12px 18px; border-radius:12px; background:#fff; box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>TCL Scripting</strong></div>
        </div>
      </div>
    </div>
  </section>

  <!-- Panel 14: CONTACT -->
  <section id="panel-14" class="panel" data-index="14" aria-label="Contact" style="background:linear-gradient(180deg,#071219,#031018);">
    <div class="stage">
      <div class="contact-card">
        <h2 style="margin:0; font-weight:900">Let's build something exceptional — Parlons</h2>
        <p style="margin-top:12px; color:rgba(238,246,248,0.9)">Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a> — Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
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

<!-- GSAP + ScrollTrigger CDN -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
/* GSAP-powered panel controller:
   - One full-screen panel visible at a time
   - Smooth wheel/keyboard/touch navigation
   - Each panel animates in (text + float images)
   - Color gradient transition from day → sunset → night (tied to scroll progress)
*/

gsap.registerPlugin(ScrollTrigger);

const panels = Array.from(document.querySelectorAll('.panel'));
const total = panels.length;
let current = 0;
let busy = false;
const duration = 0.75;

// helper: show panel by index
function showPanel(i, immediate=false){
  if(i < 0 || i >= total) return;
  if(busy && !immediate) return;
  busy = true;
  // deactivate all
  panels.forEach((p, idx)=>{
    p.classList.remove('is-active');
    // remove active class for work-stage bg
    const ws = p.querySelector('.work-stage');
    if(ws) ws.classList.remove('is-active');
  });
  const panel = panels[i];
  panel.classList.add('is-active');
  const ws = panel.querySelector('.work-stage');
  if(ws) ws.classList.add('is-active');
  current = i;
  // animate entrance (text & floating overlays)
  entranceAnim(panel);
  setTimeout(()=> busy=false, (duration*1000)+120);
  // update background color using mapped progress
  updateTheme(i);
}

// entrance animation for panel content
function entranceAnim(panel){
  // fade/slide children in
  const elems = panel.querySelectorAll('.work-card, .full-card, .about-card, .hero, .portrait, .work-title, .full-card > *');
  gsap.fromTo(elems, {autoAlpha:0, y:18, scale:0.998}, {autoAlpha:1, y:0, scale:1, duration:0.9, ease:"power3.out", stagger:0.06});
  // float images subtle parallax movement
  const floats = panel.querySelectorAll('.float-img');
  floats.forEach((f,i)=>{
    // reset transforms
    gsap.set(f, {x:0, y:0, rotation:0});
    gsap.to(f, {y: -24 - (i*6), x: (i%2===0?24:-24), duration:6 + i, ease:"sine.inOut", yoyo:true, repeat:-1});
  });
}

// theme mapping: light → sunset → night across panel index
function updateTheme(i){
  // compute progress 0..1
  const progress = i / (total - 1);
  // pick colors by ranges (0..0.4 day, 0.4..0.75 sunset, 0.75..1 night)
  if(progress < 0.4){
    gsap.to(document.documentElement, {duration:0.8, '--day-1': '#ffffff', '--day-2':'#f2f6f8'});
    document.body.style.color = '#071622';
  } else if(progress < 0.75){
    gsap.to(document.documentElement, {duration:0.9, '--day-1':'#fff7f3', '--day-2':'#f3e9da'});
    document.body.style.color = '#071622';
  } else {
    gsap.to(document.documentElement, {duration:1.0, '--day-1':'#061018', '--day-2':'#041018'});
    document.body.style.color = '#eef6f8';
  }
}

// Navigation: wheel (throttled), keyboard, touch
let wheelLock = false;
window.addEventListener('wheel', (e) => {
  if(wheelLock) return;
  wheelLock = true;
  setTimeout(()=> wheelLock=false, 350);
  if(e.deltaY > 8) nextPanel();
  if(e.deltaY < -8) prevPanel();
}, {passive:true});

window.addEventListener('keydown', (e)=>{
  if(e.key === 'ArrowDown' || e.key === 'PageDown') nextPanel();
  if(e.key === 'ArrowUp' || e.key === 'PageUp') prevPanel();
  if(e.key === 'Home') showPanel(0);
  if(e.key === 'End') showPanel(total-1);
});

// touch
let startY = null;
window.addEventListener('touchstart', e => startY = e.touches[0].clientY, {passive:true});
window.addEventListener('touchend', e => {
  if(!startY) return;
  const dy = e.changedTouches[0].clientY - startY;
  if(Math.abs(dy) > 60){
    if(dy < 0) nextPanel();
    else prevPanel();
  }
  startY = null;
}, {passive:true});

function nextPanel(){ showPanel(Math.min(total-1, current+1)); }
function prevPanel(){ showPanel(Math.max(0, current-1)); }

// initial entrance
showPanel(0,true);

// Accessibility fallback: if portrait fails to load, show initials
const portrait = document.getElementById('portrait');
portrait && portrait.addEventListener('error', ()=>{
  const wrap = portrait.parentNode;
  wrap.innerHTML = '<div style="width:360px;height:520px;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,var(--accent-teal),var(--accent-gold));color:#052425;font-weight:900;font-size:64px;border-radius:8px;">VR</div>';
});

// Optional: allow clicking top-left 'VR' to go home
document.querySelector('strong')?.addEventListener('click', ()=> showPanel(0));

/* Small performance note:
   The backgrounds are static images referenced with CSS style background-image (or <img>)
   For best performance, use optimized JPGs / webp trimmed to around 1200–2000px width.
*/

document.getElementById('year')?.textContent = new Date().getFullYear();
</script>
</body>
</html>
