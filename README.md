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
    --bg-top: #ffffff;
    --text-color: #071622;
    --muted:#6b7780;
    --accent-teal:#17c3a2;
    --accent-gold:#e6b66d;
    --linkedin:#0077b5;
    --duration:0.7;
    font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;
  }
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; background:var(--bg-top); color:var(--text-color); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;}
  a{color:inherit; text-decoration:none}
  /* App container */
  #app { position:relative; width:100vw; height:100vh; overflow:hidden; }

  /* panel base: each is full-viewport, absolutely stacked */
  .panel {
    position:absolute; inset:0; display:flex; align-items:center; justify-content:center;
    opacity:0; pointer-events:none; transform: translateY(40px); will-change:transform,opacity;
    transition: opacity var(--duration)s ease, transform var(--duration)s cubic-bezier(.2,.9,.2,1);
  }
  .panel.active { opacity:1; transform: translateY(0); pointer-events:auto; z-index:10; }

  /* background image */
  .bg {
    position:absolute; inset:0; background-size:cover; background-position:center; z-index:0;
    transform:scale(1.04); will-change:transform; transition: transform 1.4s ease;
  }
  /* overlay layer for contrast; uses per-panel color via CSS variable --overlay */
  .overlay {
    position:absolute; inset:0; z-index:1; background:linear-gradient(180deg, rgba(0,0,0,0.18), rgba(0,0,0,0.36));
    mix-blend-mode: normal; pointer-events:none;
  }
  /* stage content sits above overlay */
  .stage { position:relative; z-index:6; width:100%; height:100%; display:flex; align-items:center; justify-content:center; padding:28px; }

  /* main hero portrait floating (no frame) */
  .portrait {
    width:auto; height:68vh; max-height:820px; display:block; filter: drop-shadow(0 50px 120px rgba(6,12,20,0.35));
    transform-origin:center; will-change:transform;
  }

  /* titles large and centered */
  .title {
    font-weight:900; font-size:clamp(32px,6.8vw,84px); line-height:0.9; text-transform:uppercase; margin:18px 0 8px; text-align:center;
    color:var(--title-color, #fff);
  }
  .subtitle {
    font-weight:700; color:var(--subtitle-color, rgba(255,255,255,0.9)); text-align:center; font-size:18px; margin-bottom:18px;
  }
  .desc {
    max-width:1000px; color:var(--desc-color, rgba(255,255,255,0.92)); line-height:1.65; font-size:18px; text-align:center; margin-top:6px;
  }

  /* floating overlay images (foreground) */
  .float {
    position:absolute; z-index:8; pointer-events:none; will-change:transform, filter, opacity;
    width:46vw; max-width:760px; opacity:0.98;
    filter: drop-shadow(0 34px 90px rgba(3,9,16,0.55));
  }
  @media (max-width:980px){ .float{ width:78vw; max-width:480px } .portrait{ height:52vh } .title{ font-size:clamp(28px,9vw,52px)} }

  /* layout helpers for list panels */
  .full-card { max-width:1200px; width:100%; padding:32px; border-radius:12px; background:rgba(255,255,255,0.02); text-align:center; }
  .white-card { background: linear-gradient(180deg, #fff, #fbfbfb); color:#071622; box-shadow:0 30px 80px rgba(8,12,18,0.06); }

  /* social buttons top-right */
  .topbar { position:fixed; top:16px; right:18px; z-index:90; display:flex; gap:10px; }
  .btn { padding:10px 14px; border-radius:10px; font-weight:800; display:inline-flex; gap:8px; align-items:center; color:#fff; cursor:pointer; box-shadow:0 12px 36px rgba(0,0,0,0.12);}
  .btn.linkedin { background:var(--linkedin) }
  .btn.instagram { background: linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5) }
  .btn.contact { background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold)); color:#052425 }

  /* small responsive */
  @media (max-width:720px){
    .title{ font-size:28px }
    .desc{ font-size:15px }
  }
</style>
</head>
<body>
<div id="app" aria-live="polite">

  <!-- Topbar social -->
  <div class="topbar" role="navigation" aria-label="Social and contact">
    <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
    <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
    <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
  </div>

  <!-- Panel list: each panel is full-viewport -->
  <!-- Panel 0: HERO -->
  <section id="p-0" class="panel active" data-theme="day" aria-label="Hero">
    <div class="bg" style="background-image:url('ai_about.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.8), rgba(255,255,255,0.6)); mix-blend-mode:normal;"></div>
    <div class="stage">
      <div>
        <img src="portrait.png" alt="Portrait of Venkata Raghavendra KADIYALA" class="portrait" id="portrait" loading="eager">
        <div class="title" style="color:#071622">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></div>
        <div class="subtitle" style="color:var(--muted)">Mechanical Engineer · Creative Designer — Train interiors & systems</div>
        <div class="desc" style="color:var(--muted)">Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a> · Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a></div>
      </div>
    </div>
  </section>

  <!-- Panel 1: ABOUT -->
  <section id="p-1" class="panel" data-theme="light" aria-label="About">
    <div class="bg" style="background-image:url('ai_about.jpg'); filter:brightness(.92);"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.92), rgba(250,250,250,0.88));"></div>
    <div class="stage">
      <div class="white-card full-card">
        <h2 style="margin:0; font-weight:900">About — À propos</h2>
        <p style="margin-top:16px; color:var(--muted); line-height:1.7; font-size:17px; max-width:1000px; margin-left:auto; margin-right:auto;">
          <strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability and clear user-focused outcomes.<br><br>
          <strong>Français :</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.
        </p>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE PANELS: full viewport each, strong overlay, floating img -->
  <!-- Panel 2: SEGULA — OSTA -->
  <section id="p-2" class="panel" data-theme="steel" aria-label="SEGULA — OSTA">
    <div class="bg" style="background-image:url('ai_osta.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(4,10,14,0.48), rgba(2,6,10,0.6));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_osta.png" alt="" style="right:6%; top:14%;">
      <div>
        <div class="title">SEGULA — Project OSTA</div>
        <div class="subtitle">Front office • Train interior systems • M0 → M5</div>
        <div class="desc">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets, under-seat boxes. Delivery of validated 3D models (SAM) and supplier coordination.</div>
      </div>
    </div>
  </section>

  <!-- Panel 3: SEGULA — BaWu -->
  <section id="p-3" class="panel" data-theme="teal" aria-label="SEGULA — BaWu">
    <div class="bg" style="background-image:url('ai_bawu.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(6,12,12,0.48), rgba(4,8,8,0.6));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_bawu.png" alt="" style="left:8%; top:16%;">
      <div>
        <div class="title">SEGULA — BaWu</div>
        <div class="subtitle">Validation & QA — Integration focus</div>
        <div class="desc">3D validation, integration issue prevention, QA and KPI/OIL tracking, and CAD governance for industrial handover.</div>
      </div>
    </div>
  </section>

  <!-- Panel 4: SEGULA — RER NG -->
  <section id="p-4" class="panel" data-theme="steel2" aria-label="SEGULA — RER NG">
    <div class="bg" style="background-image:url('ai_rerng.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(5,8,12,0.5), rgba(3,6,10,0.62));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_rerng.png" alt="" style="right:10%; top:18%;">
      <div>
        <div class="title">SEGULA — RER NG</div>
        <div class="subtitle">Change request engineering & on-site surveys</div>
        <div class="desc">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</div>
      </div>
    </div>
  </section>

  <!-- Panel 5: SEGULA — DSB -->
  <section id="p-5" class="panel" data-theme="navy" aria-label="SEGULA — DSB">
    <div class="bg" style="background-image:url('ai_dsb.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(3,6,14,0.6), rgba(2,4,10,0.72));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_dsb.png" alt="" style="left:6%; top:12%;">
      <div>
        <div class="title">SEGULA — DSB</div>
        <div class="subtitle">Interior layout & integration</div>
        <div class="desc">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</div>
      </div>
    </div>
  </section>

  <!-- Panel 6: SNCF -->
  <section id="p-6" class="panel" data-theme="graphite" aria-label="SNCF">
    <div class="bg" style="background-image:url('ai_sncf.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(6,8,12,0.54), rgba(3,6,10,0.66));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_sncf.png" alt="" style="right:8%; top:10%;">
      <div>
        <div class="title">SNCF</div>
        <div class="subtitle">FEA & Automation — HyperWorks / OptiStruct</div>
        <div class="desc">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports and structural validation with HyperWorks/OptiStruct.</div>
      </div>
    </div>
  </section>

  <!-- Panel 7: LAMIH -->
  <section id="p-7" class="panel" data-theme="dusk" aria-label="LAMIH">
    <div class="bg" style="background-image:url('ai_lamih.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(30,18,36,0.36), rgba(4,6,10,0.6));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_lamih.png" alt="" style="left:10%; top:14%;">
      <div>
        <div class="title">LAMIH</div>
        <div class="subtitle">Behavioural analysis & safety concepts</div>
        <div class="desc">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</div>
      </div>
    </div>
  </section>

  <!-- Panel 8: PM DIMENSIONS -->
  <section id="p-8" class="panel" data-theme="silver" aria-label="PM DIMENSIONS">
    <div class="bg" style="background-image:url('ai_pmdimensions.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,250,240,0.06), rgba(6,6,8,0.18));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_pmdimensions.png" alt="" style="right:8%; top:16%;">
      <div>
        <div class="title" style="color:#071622">PM DIMENSIONS</div>
        <div class="subtitle" style="color:rgba(6,6,8,0.9)">Part design & prototyping</div>
        <div class="desc" style="color:rgba(6,6,8,0.9)">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</div>
      </div>
    </div>
  </section>

  <!-- Panel 9: INDIAN RAILWAYS internship -->
  <section id="p-9" class="panel" data-theme="sunset" aria-label="Indian Railways">
    <div class="bg" style="background-image:url('ai_indianrail.jpg');"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(8,6,4,0.14), rgba(6,4,6,0.28));"></div>
    <div class="stage work-stage">
      <img class="float" src="float_indianrail.png" alt="" style="left:6%; top:16%;">
      <div>
        <div class="title">Indian Railways (Intern)</div>
        <div class="subtitle">Prototype coupling & maintenance optimisation</div>
        <div class="desc">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</div>
      </div>
    </div>
  </section>

  <!-- Panel 10: EDUCATION -->
  <section id="p-10" class="panel" data-theme="light" aria-label="Education">
    <div class="bg" style="background-image:url('ai_about.jpg'); filter:brightness(.9)"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.92), rgba(250,250,250,0.88));"></div>
    <div class="stage">
      <div class="white-card full-card">
        <h2 style="margin:0; font-weight:900">Education — Formation</h2>
        <div style="margin-top:14px; color:var(--muted); font-weight:700">
          <div style="margin-bottom:8px;"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019 — 2021)</div>
          <div><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014 — 2018)</div>
        </div>
        <div style="margin-top:12px; color:var(--muted)">Selected project: Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018</div>
      </div>
    </div>
  </section>

  <!-- Panel 11: SKILLS -->
  <section id="p-11" class="panel" data-theme="light" aria-label="Skills">
    <div class="bg" style="background-image:url('ai_about.jpg'); filter:brightness(.95)"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.92), rgba(250,250,250,0.88));"></div>
    <div class="stage">
      <div class="white-card full-card">
        <h2 style="margin:0; font-weight:900">Skills & Tools — Compétences</h2>
        <div style="display:flex; gap:12px; margin-top:18px; flex-wrap:wrap; justify-content:center;">
          <div style="padding:12px 16px;border-radius:10px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>CATIA V5</strong></div>
          <div style="padding:12px 16px;border-radius:10px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>Ansys</strong></div>
          <div style="padding:12px 16px;border-radius:10px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>HyperWorks / OptiStruct</strong></div>
          <div style="padding:12px 16px;border-radius:10px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>PDM / DMA / SAM</strong></div>
          <div style="padding:12px 16px;border-radius:10px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>TCL • C • Java</strong></div>
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

  <!-- Panel 12: PUBLICATION -->
  <section id="p-12" class="panel" data-theme="paper" aria-label="Publication">
    <div class="bg" style="background-image:url('ai_publication.jpg'); filter:brightness(.85)"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.92), rgba(250,250,250,0.88));"></div>
    <div class="stage">
      <div class="white-card full-card" style="text-align:left;">
        <h2 style="margin:0; font-weight:900">Publication — Avril 2018</h2>
        <p style="margin-top:12px; color:var(--muted)"><strong>Enhancement of Refrigeration Effect Using Flue Gases from Chimney</strong> — April 2018. A study on increasing refrigeration effect using flue gases from a chimney. <a href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>.</p>
      </div>
    </div>
  </section>

  <!-- Panel 13: CERTIFICATIONS -->
  <section id="p-13" class="panel" data-theme="certs" aria-label="Certifications">
    <div class="bg" style="background-image:url('ai_about.jpg'); filter:brightness(.96)"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.94), rgba(250,250,250,0.9));"></div>
    <div class="stage">
      <div class="white-card full-card">
        <h2 style="margin:0; font-weight:900">Certifications</h2>
        <div style="margin-top:14px; display:flex; gap:12px; justify-content:center; flex-wrap:wrap;">
          <div style="padding:12px 18px;border-radius:12px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>CATIA V5</strong></div>
          <div style="padding:12px 18px;border-radius:12px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>Ansys (FEA)</strong></div>
          <div style="padding:12px 18px;border-radius:12px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>HyperWorks / OptiStruct</strong></div>
          <div style="padding:12px 18px;border-radius:12px;background:#fff;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>TCL Scripting</strong></div>
        </div>
      </div>
    </div>
  </section>

  <!-- Panel 14: CONTACT -->
  <section id="p-14" class="panel" data-theme="night" aria-label="Contact">
    <div class="bg" style="background:linear-gradient(180deg,#071219,#031018);"></div>
    <div class="overlay" style="background:linear-gradient(180deg, rgba(5,8,12,0.6), rgba(3,6,10,0.72));"></div>
    <div class="stage">
      <div class="contact-card full-card" style="background:linear-gradient(180deg,#061018,#031018); color:#eef6f8;">
        <h2 style="margin:0; font-weight:900">Let's build something exceptional — Parlons</h2>
        <p style="margin-top:12px; color:rgba(238,246,248,0.9)">Email: <a href="mailto:venkata.france@gmail.com" style="color:#fff">venkata.france@gmail.com</a> — Phone: <a href="tel:+33755662821" style="color:#fff">+33 7 55 66 28 21</a></p>
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

<!-- GSAP -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
/* Cinematic panel controller with GSAP + ScrollTrigger.
   - Panels are absolute; we toggle .active to show one at a time.
   - Floating PNGs animate continuously; backgrounds have parallax on enter.
   - updateTheme changes top-level CSS variables for day/night effect.
*/

gsap.registerPlugin(ScrollTrigger);

const panels = Array.from(document.querySelectorAll('.panel'));
const total = panels.length;
let current = 0;
let busy = false;
const entranceDelay = 0.65;

// set initial active panel
function setActive(i, immediate=false){
  if(i < 0 || i >= total) return;
  if(busy && !immediate) return;
  busy = true;
  panels.forEach((p, idx) => {
    p.classList.toggle('active', idx === i);
  });
  current = i;
  animateEntrance(panels[i]);
  updateTheme(i);
  // delay release
  setTimeout(()=> busy = false, (entranceDelay*1000)+120);
}

// entrance animation for current panel
function animateEntrance(panel){
  // kill any existing anims for floats inside panel
  const floats = panel.querySelectorAll('.float');
  floats.forEach(f => gsap.killTweensOf(f));

  // reveal stage content
  const children = panel.querySelectorAll('.stage > * , .title, .subtitle, .desc, .work-card, .white-card, .contact-card');
  gsap.fromTo(children, {autoAlpha:0, y:18}, {autoAlpha:1, y:0, duration:0.9, ease:'power3.out', stagger:0.06});

  // background subtle scale to normal
  const bg = panel.querySelector('.bg');
  if(bg){
    gsap.fromTo(bg, {scale:1.06}, {scale:1.0, duration:1.4, ease:'power2.out'});
  }

  // loop floats gently for depth
  floats.forEach((f, idx)=>{
    gsap.set(f, {x:0, y:0, rotation:0});
    gsap.to(f, {y: (idx%2===0? -30 : 30), x: (idx%2===0? 22 : -22), duration:6 + idx, ease:'sine.inOut', yoyo:true, repeat:-1});
  });
}

// theme mapping: day -> sunset -> night across panels, but also per-panel accent can be used
function updateTheme(i){
  // simple mapping: early panels light, middle panels sunset/dark
  const progress = i / (total - 1);
  if(progress < 0.35){
    // day
    gsap.to(document.documentElement, {duration:0.9, '--bg-top':'#ffffff', '--text-color':'#071622'});
  } else if(progress < 0.75){
    // sunset
    gsap.to(document.documentElement, {duration:0.9, '--bg-top':'#fff7f3', '--text-color':'#071622'});
  } else {
    // night
    gsap.to(document.documentElement, {duration:1.0, '--bg-top':'#061018', '--text-color':'#eef6f8'});
  }
}

// Navigation handlers: wheel, keyboard, touch
let wheelLock = false;
window.addEventListener('wheel', (e) => {
  if(wheelLock) return;
  wheelLock = true;
  setTimeout(()=> wheelLock = false, 360);
  if(e.deltaY > 8) nextPanel();
  if(e.deltaY < -8) prevPanel();
}, {passive:true});

window.addEventListener('keydown', (e) => {
  if(e.key === 'ArrowDown' || e.key === 'PageDown') nextPanel();
  if(e.key === 'ArrowUp' || e.key === 'PageUp') prevPanel();
  if(e.key === 'Home') setActive(0, true);
  if(e.key === 'End') setActive(total - 1, true);
});

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

function nextPanel(){ setActive(Math.min(total - 1, current + 1)); }
function prevPanel(){ setActive(Math.max(0, current - 1)); }

// Initialize first panel animations
setActive(0, true);

// Make panels navigable by clicking (optional) -- clicking center goes next
document.querySelectorAll('.panel').forEach(p => {
  p.addEventListener('click', (e) => {
    // only if clicking empty space (not a link)
    if(e.target.tagName.toLowerCase() === 'a') return;
    nextPanel();
  });
});

// Accessibility fallback: portrait error -> initials block
const portrait = document.getElementById('portrait');
portrait && portrait.addEventListener('error', function(){
  const parent = portrait.parentElement;
  parent.innerHTML = '<div style="width:360px;height:520px;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,var(--accent-teal),var(--accent-gold));color:#052425;font-weight:900;font-size:64px;border-radius:6px;">VR</div>';
});

// ensure year
document.getElementById('year')?.textContent = new Date().getFullYear();
</script>
</body>
</html>
