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
    --bg-light:#ffffff;
    --bg-mid:#f3f6f8;
    --bg-dark:#071219;
    --accent-teal:#17c3a2;
    --accent-gold:#e6b66d;
    --muted:#667076;
    --text-dark:#071622;
    --snap-duration:700ms;
    font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;
  }
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; background:linear-gradient(180deg,var(--bg-light),var(--bg-mid)); color:var(--text-dark); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;}
  a{color:inherit; text-decoration:none}
  /* container intentionally fills screen and disables default scroll-jank */
  body, #app { height:100vh; overflow:hidden; }

  /* Panel system: panels stacked vertically but only one is visible at a time */
  .panels { position:relative; height:100vh; width:100%; }
  section.panel {
    position:absolute;
    inset:0;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:40px;
    opacity:0;
    transform: translateY(20px) scale(.995);
    transition: opacity var(--snap-duration) cubic-bezier(.2,.9,.2,1), transform var(--snap-duration) cubic-bezier(.2,.9,.2,1);
    pointer-events:none;
    will-change:opacity, transform;
    background-size:cover;
    background-position:center;
    background-repeat:no-repeat;
  }
  /* active panel will be visible */
  section.panel.active {
    opacity:1;
    transform: translateY(0) scale(1);
    pointer-events:auto;
    z-index:10;
  }

  /* small nav bar fixed top-right */
  .topbar {
    position:fixed; top:18px; right:24px; z-index:60; display:flex; gap:10px; align-items:center;
    background:rgba(255,255,255,0.75); padding:6px 10px; border-radius:999px; box-shadow:0 10px 30px rgba(8,12,18,0.08);
    backdrop-filter: blur(6px);
  }
  .topbar.dark { background:rgba(6,8,12,0.7); color:#eef6f8; }

  /* social buttons - natural colors */
  .btn-linkedin{
    display:inline-flex; gap:8px; align-items:center; padding:10px 14px; border-radius:10px; color:white; font-weight:700;
    background:#0077b5; box-shadow:0 8px 22px rgba(0,119,181,0.18);
  }
  .btn-instagram{
    display:inline-flex; gap:8px; align-items:center; padding:10px 14px; border-radius:10px; color:white; font-weight:700;
    background: linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5);
    box-shadow:0 8px 22px rgba(150,43,191,0.12);
  }
  .btn-ghost{ display:inline-flex; gap:8px; align-items:center; padding:8px 12px; border-radius:8px; background:transparent; border:1px solid rgba(0,0,0,0.06); font-weight:700; }

  /* content centering for product-style reveal (full-screen) */
  .stage { width:100%; max-width:1400px; margin:0 auto; height:100%; display:flex; align-items:center; justify-content:center; position:relative; padding:28px; }

  /* HERO specifics */
  .hero-inner { text-align:center; display:flex; flex-direction:column; align-items:center; gap:28px; }
  .portrait { width:360px; height:360px; border-radius:50%; overflow:hidden; background:transparent; box-shadow: 0 30px 80px rgba(8,12,18,0.12); }
  .portrait img{ width:100%; height:100%; object-fit:cover; display:block; background:transparent; }

  .hero-name {
    font-weight:900;
    font-size:clamp(40px, 8vw, 110px);
    line-height:0.88;
    margin:0;
    letter-spacing: -1px;
    color:var(--text-dark);
    text-transform:uppercase;
  }
  .hero-sub { font-weight:700; color:var(--muted); font-size:18px; margin-top:6px; }

  /* large spacer to ensure no adjacent content shows — but we hide others fully via JS */
  .spacer { height:120px; }

  /* About / Story panel */
  .story-card {
    width:100%; max-width:1000px; background:linear-gradient(180deg,#ffffff,#fbfcfd); border-radius:18px; padding:42px; box-shadow:0 30px 80px rgba(8,12,18,0.06);
  }
  .story-grid { display:grid; grid-template-columns:1fr 380px; gap:28px; align-items:center; }
  .story-grid p { color:var(--muted); line-height:1.7; font-size:16px; }

  /* Work panels: big bold title + subtitle, image on background (sharp, not blurred) */
  .work-content { text-align:left; color:white; max-width:980px; margin:0 auto; padding:22px; background: linear-gradient(180deg, rgba(0,0,0,0.18), rgba(0,0,0,0.0)); border-radius:12px; }
  .work-title { font-weight:900; font-size:44px; margin:0 0 10px 0; color: #fff; text-shadow:0 10px 30px rgba(0,0,0,0.5); }
  .work-sub { color:rgba(255,255,255,0.9); font-weight:700; margin-bottom:12px; }
  .work-desc { color:rgba(255,255,255,0.92); line-height:1.6; font-size:18px; }

  /* Contact panel */
  .contact-card { text-align:center; max-width:900px; padding:36px; border-radius:18px; background:linear-gradient(180deg, rgba(3,6,10,0.9), rgba(6,8,12,0.95)); color:#eef6f8; box-shadow:0 40px 100px rgba(0,0,0,0.6); }
  .contact-card h2 { font-size:34px; margin:0 0 8px 0; font-weight:900; }

  /* Accessibility focus and outlines */
  a:focus, button:focus { outline:3px solid rgba(23,195,162,0.16); outline-offset:4px; border-radius:8px; }

  /* responsive */
  @media (max-width:980px){
    .portrait{ width:200px; height:200px; }
    .story-grid{ grid-template-columns:1fr; }
    .hero-name{ font-size:clamp(32px,10vw,72px); }
    .work-title{ font-size:32px; }
  }
</style>
</head>
<body>
<div id="app">
  <!-- small topbar with brand social - color adapts -->
  <div id="topbar" class="topbar" aria-hidden="false">
    <a href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener" class="btn-linkedin" aria-label="LinkedIn">
      <!-- LinkedIn icon -->
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M4 4h4v16H4zM6 2a2 2 0 110 4 2 2 0 010-4zM10 8h3.7v2.1h.1c.5-.9 1.7-2.1 3.6-2.1 3.8 0 4.5 2.5 4.5 5.7V20H18v-5.1c0-1.2 0-2.8-1.7-2.8-1.7 0-2 1.4-2 2.7V20h-4V8z" stroke="white" stroke-width="0.6" stroke-linecap="round" stroke-linejoin="round" /></svg>
      LinkedIn
    </a>
    <a href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener" class="btn-instagram" aria-label="Instagram">
      <!-- Instagram icon -->
      <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><rect x="3" y="3" width="18" height="18" rx="5" fill="white" opacity="0.0"/><circle cx="12" cy="12" r="3" stroke="white" stroke-width="1.2"/></svg>
      Instagram
    </a>
  </div>

  <!-- Panels -->
  <div class="panels" id="panels" aria-live="polite">
    <!-- Panel 1: HERO -->
    <section id="panel-1" class="panel active" role="region" aria-label="Hero: Venkata">
      <!-- Hero background: very light -->
      <div class="stage" style="justify-content:center; align-items:center;">
        <div class="hero-inner" role="main">
          <div class="portrait" aria-hidden="false">
            <!-- Replace with your transparent portrait file named "photo.png" in same folder -->
            <img src="photo.png" alt="Venkata Raghavendra Kadiyala portrait" id="portraitImg" loading="eager">
          </div>

          <h1 class="hero-name" aria-label="Full name">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
          <div class="hero-sub">Mechanical Engineer &amp; Creative Designer — Train interiors • Systems • CAD</div>

          <div style="display:flex; gap:14px; margin-top:18px; justify-content:center; align-items:center;">
            <a class="btn-linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
            <a class="btn-instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
          </div>

          <div style="margin-top:18px; color:var(--muted); font-weight:700">☎ +33 7 55 66 28 21 &nbsp; • &nbsp; ✉ <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a></div>
        </div>
      </div>
    </section>

    <!-- Panel 2: ABOUT / STORY -->
    <section id="panel-2" class="panel" role="region" aria-label="About me">
      <!-- background: subtle mid tone -->
      <div class="stage">
        <div class="story-card" role="article" aria-labelledby="storyTitle">
          <div class="story-grid">
            <div>
              <div id="storyTitle" style="font-weight:900; font-size:20px; color:var(--text-dark)">About — À propos</div>
              <h2 style="margin-top:12px; font-size:34px; font-weight:900; color:var(--text-dark)">Design-minded engineering — clarity and craft.</h2>
              <p style="margin-top:18px;">
                <strong>English:</strong> I combine mechanical engineering rigor with product-level design thinking. My work focuses on train interiors, component design and validated 3D model delivery (M0 → M5). I lead CAD teams, coordinate suppliers, and ensure manufacturability and user clarity.<br><br>
                <strong>Français :</strong> J’allie rigueur mécanique et pensée produit. Mon travail porte sur l’aménagement ferroviaire, la conception de pièces et la livraison de modèles 3D validés (M0 → M5). Pilotage CAO, coordination fournisseurs et fabricabilité sont au cœur des projets.
              </p>

              <div style="display:flex; gap:18px; margin-top:22px; flex-wrap:wrap;">
                <div style="padding:16px; border-radius:12px; background:linear-gradient(180deg,#fff,#f6f7f8); box-shadow:0 14px 36px rgba(6,12,18,0.06)">
                  <div style="font-weight:900; font-size:20px">5+</div>
                  <div style="color:var(--muted); font-weight:700">Years experience</div>
                </div>
                <div style="padding:16px; border-radius:12px; background:linear-gradient(180deg,#fff,#f6f7f8); box-shadow:0 14px 36px rgba(6,12,18,0.06)">
                  <div style="font-weight:900; font-size:20px">M0 → M5</div>
                  <div style="color:var(--muted); font-weight:700">Model maturity</div>
                </div>
                <div style="padding:16px; border-radius:12px; background:linear-gradient(180deg,#fff,#f6f7f8); box-shadow:0 14px 36px rgba(6,12,18,0.06)">
                  <div style="font-weight:900; font-size:20px">CAD & FEA</div>
                  <div style="color:var(--muted); font-weight:700">CATIA V5 • Hyperworks</div>
                </div>
              </div>
            </div>

            <aside style="display:flex; align-items:center; justify-content:center;">
              <div style="width:340px; padding:18px; border-radius:12px; background:linear-gradient(180deg,#fff,#f6f7f8); box-shadow:0 14px 36px rgba(6,12,18,0.06); text-align:center;">
                <div style="font-weight:900; font-size:20px; color:var(--text-dark)">What I care about</div>
                <div style="margin-top:12px; color:var(--muted); font-weight:700">Clarity • Manufacturability • Clean UX • Efficient CAD</div>
              </div>
            </aside>
          </div>
        </div>
      </div>
    </section>

    <!-- Panel 3: WORK - Project 1 (full-screen with sharp background) -->
    <section id="panel-3" class="panel" role="region" aria-label="Project OSTA"
      style="background-image: url('ai_osta.jpg');">
      <!-- NOTE: replace ai_osta.jpg with the AI image for Project OSTA -->
      <div class="stage">
        <div class="work-content" role="article" aria-labelledby="p3title" style="text-align:center;">
          <div id="p3title" class="work-title">SEGULA — Project OSTA</div>
          <div class="work-sub">Front office • Train interior systems • M0 → M5 model maturity</div>
          <p class="work-desc">Lead CAD deliveries for interior systems (windows, blinds, sidewalls, intercoms, electrical cabinets, under-seat systems). Supplier coordination and validation of production-ready 3D models.</p>
        </div>
      </div>
    </section>

    <!-- Panel 4: WORK - Project 2 -->
    <section id="panel-4" class="panel" role="region" aria-label="Project BaWu"
      style="background-image: url('ai_bawu.jpg');">
      <!-- NOTE: replace ai_bawu.jpg with the AI image for Project BaWu -->
      <div class="stage">
        <div class="work-content" role="article">
          <div class="work-title">SEGULA — BaWu</div>
          <div class="work-sub">Design validation, QA & CAD governance</div>
          <p class="work-desc">3D validation workflows, proactive integration issue resolution, KPI/OIL tracking, and industrial handover support.</p>
        </div>
      </div>
    </section>

    <!-- Panel 5: WORK - Project 3 -->
    <section id="panel-5" class="panel" role="region" aria-label="SNCF FEA"
      style="background-image: url('ai_scnf.jpg');">
      <!-- NOTE: replace ai_scnf.jpg with the AI image for SNCF/FEA -->
      <div class="stage">
        <div class="work-content" role="article">
          <div class="work-title">SNCF — FEA & Automation</div>
          <div class="work-sub">Hyperworks / Optistruct • TCL scripting</div>
          <p class="work-desc">Automation of bolted assemblies, mesh and static/non-static analysis for seat supports, plus structural validation and optimization.</p>
        </div>
      </div>
    </section>

    <!-- Panel 6: CONTACT / CTA -->
    <section id="panel-6" class="panel" role="region" aria-label="Contact"
      style="background:linear-gradient(180deg,#071219,#031018);">
      <div class="stage">
        <div class="contact-card" role="contentinfo">
          <h2>Let's build something exceptional — Parlons</h2>
          <p style="margin-top:12px; color:rgba(238,246,248,0.92)">Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a> — Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
          <div style="margin-top:20px; display:flex; gap:12px; justify-content:center; align-items:center; flex-wrap:wrap;">
            <a class="btn-linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
            <a class="btn-instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
            <a class="btn-primary" href="mailto:venkata.france@gmail.com" style="display:inline-flex; align-items:center; gap:10px; padding:12px 16px; border-radius:12px; font-weight:800; color:#072425; background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold));">Email me</a>
          </div>
          <div style="margin-top:18px; color:rgba(238,246,248,0.6)">© <span id="year"></span> Venkata Raghavendra KADIYALA</div>
        </div>
      </div>
    </section>

  </div>
</div>

<script>
/*
  Behavior:
  - Panels are stacked absolute; JS shows one at a time by toggling .active
  - Wheel / touch / keyboard navigate between panels (snapping)
  - Background images are full-bleed; replace ai_*.jpg and photo.png with real AI outputs
*/

/* Panel navigation */
(function(){
  const panelIds = ['panel-1','panel-2','panel-3','panel-4','panel-5','panel-6'];
  const panels = panelIds.map(id => document.getElementById(id));
  let index = 0;
  let animating = false;
  const ms = 700;

  function show(i, smooth=true){
    if(i < 0 || i >= panels.length) return;
    if(animating) return;
    animating = true;
    // hide all first
    panels.forEach((p, idx) => {
      if(idx === i){
        p.classList.add('active');
        // Bring to front
        p.style.zIndex = 10;
      } else {
        p.classList.remove('active');
        // push behind
        p.style.zIndex = 1;
      }
    });
    index = i;
    // After transition duration, allow navigation again
    setTimeout(()=>{ animating = false; }, ms + 60);
    // update topbar color for dark panels
    updateTopbar(i);
  }

  // initial show
  show(0,false);

  // map wheel / touch to next/prev
  let wheelThrottle = false;
  window.addEventListener('wheel', (e) => {
    if(wheelThrottle || animating) return;
    wheelThrottle = true;
    setTimeout(()=> wheelThrottle = false, 400);
    if(e.deltaY > 10) next();
    if(e.deltaY < -10) prev();
  }, {passive:true});

  // keyboard nav
  window.addEventListener('keydown', (e) => {
    if(e.key === 'ArrowDown' || e.key === 'PageDown') next();
    if(e.key === 'ArrowUp' || e.key === 'PageUp') prev();
    if(e.key === 'Home') show(0);
    if(e.key === 'End') show(panels.length - 1);
  });

  // touch support: swipe up/down
  let touchStartY = null;
  window.addEventListener('touchstart', (e) => { touchStartY = e.touches[0].clientY; }, {passive:true});
  window.addEventListener('touchend', (e) => {
    if(touchStartY === null) return;
    const dy = (e.changedTouches[0].clientY - touchStartY);
    if(Math.abs(dy) > 60){
      if(dy < 0) next();
      else prev();
    }
    touchStartY = null;
  }, {passive:true});

  function next(){ show(Math.min(panels.length-1, index+1)); }
  function prev(){ show(Math.max(0, index-1)); }

  // clickable topbar links could jump to a panel if you add handlers; example:
  // (not included to keep nav minimal)
  // function gotoPanel(n){ show(n); }

  // Update topbar appearance for readability (light vs dark)
  function updateTopbar(i){
    const topbar = document.getElementById('topbar');
    // panels 3..6 are darker (work + contact) so make topbar dark
    if(i >= 3) topbar.classList.add('dark');
    else topbar.classList.remove('dark');
  }
})();

/* small helper: if portrait fails to load, show initials */
(function(){
  const img = document.getElementById('portraitImg');
  if(!img) return;
  img.addEventListener('error', function(){
    const wrapper = img.parentElement;
    wrapper.innerHTML = '<div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,var(--accent-teal),var(--accent-gold));color:#052425;font-weight:900;font-size:64px;">VR</div>';
  });
})();

/* set current year */
document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>
