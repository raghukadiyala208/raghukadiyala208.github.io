<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<meta name="description" content="Venkata Raghavendra KADIYALA — Mechanical Engineer & Creative Designer (Portfolio EN/FR)" />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-start: #ffffff;
    --bg-end: #081016;
    --accent-teal: #10b89a;
    --accent-gold: #e6b66d;
    --muted:#6b7780;
    --text-dark:#071622;
    --text-light:#eef6f8;
    --maxw:1400px;
    font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;
    scroll-behavior: smooth;
  }

  /* Reset */
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; color:var(--text-dark); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;}
  a{color:inherit; text-decoration:none}

  /* Viewport panels */
  .viewport{
    height:100vh;
    width:100%;
    overflow-y:auto;
    scroll-snap-type: y mandatory;
    -webkit-overflow-scrolling: touch;
    background: linear-gradient(180deg, var(--bg-start) 0%, #f2f5f6 35%, #cfe0df 60%, var(--bg-end) 100%);
  }

  section.panel{
    scroll-snap-align: start;
    width:100%;
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
    padding:0;
  }

  /* Center container for full screen */
  .stage{
    width:100%;
    max-width:var(--maxw);
    height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
    padding:48px;
  }

  /* HERO: full-screen centered name + portrait */
  .hero {
    color:var(--text-dark);
  }
  .hero-inner{
    text-align:center;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:28px;
    transform: translateY(0);
  }

  /* portrait: circular, centered, no background box */
  .portrait{
    width:320px;
    height:320px;
    border-radius:50%;
    overflow:hidden;
    display:inline-block;
    box-shadow: 0 30px 80px rgba(6,12,18,0.12);
    transition: transform 700ms cubic-bezier(.2,.9,.2,1);
    background:transparent;
  }
  .portrait img{ width:100%; height:100%; object-fit:cover; display:block; background:transparent; }

  .name {
    font-weight:800;
    font-size:clamp(36px, 7vw, 84px); /* big responsive */
    letter-spacing: -1px;
    line-height:0.95;
    margin:0;
    color:var(--text-dark);
    transform: translateY(0);
  }

  .tagline{
    font-weight:600;
    color:var(--muted);
    font-size:clamp(14px, 1.7vw, 18px);
    margin-top:6px;
  }

  /* social buttons under hero */
  .hero-actions{
    display:flex;
    gap:14px;
    align-items:center;
    justify-content:center;
    flex-wrap:wrap;
    margin-top:8px;
  }

  .btn-primary{
    display:inline-flex;
    align-items:center;
    gap:10px;
    padding:12px 18px;
    border-radius:14px;
    font-weight:800;
    font-size:14px;
    background: linear-gradient(90deg, var(--accent-teal), var(--accent-gold));
    color:#062422;
    box-shadow: 0 18px 50px rgba(16,40,36,0.12);
    transition: transform .18s ease;
  }
  .btn-primary:hover{ transform: translateY(-6px); }

  .btn-ghost{
    display:inline-flex;
    align-items:center;
    gap:10px;
    padding:10px 14px;
    border-radius:12px;
    font-weight:700;
    font-size:13px;
    background:transparent;
    border:1px solid rgba(6,12,18,0.06);
    color:var(--text-dark);
  }

  /* subtle animated underline for socials */
  .social-underline{
    height:4px; width:0; background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold)); border-radius:999px; transition: width .4s ease;
  }
  .btn-primary:hover + .social-underline, .btn-ghost:hover + .social-underline{ width:60px; }

  /* STORY panel (info) uses mostly light background */
  .story .stage{ align-items:center; justify-content:center; padding:72px; }
  .story-card{
    width:100%;
    max-width:1100px;
    background:rgba(255,255,255,0.96);
    border-radius:18px;
    padding:42px;
    box-shadow: 0 30px 80px rgba(6,12,18,0.06);
    color:var(--text-dark);
  }
  .story-grid{ display:grid; grid-template-columns:1fr 420px; gap:28px; align-items:start; }
  .story-grid p{ margin:0; color:var(--muted); line-height:1.7; font-size:16px; }
  .story-highlights{ display:flex; gap:18px; margin-top:18px; flex-wrap:wrap; }

  .stat{
    background:linear-gradient(180deg,#fff,#f6f7f8);
    padding:18px; border-radius:12px; min-width:140px; text-align:center; box-shadow:0 14px 36px rgba(10,18,24,0.06);
  }
  .stat .num{ font-weight:800; font-size:22px; color:var(--text-dark); }
  .stat .label{ color:var(--muted); font-weight:700; font-size:12px; margin-top:6px; }

  /* WORK panels: each project in its own panel or can be in one dark panel as smaller blocks */
  .work .stage{ align-items:center; justify-content:center; padding:72px; }
  .work-card{
    width:100%; max-width:1100px;
    background: linear-gradient(180deg, rgba(2,8,10,0.9), rgba(4,12,16,0.85));
    color:var(--text-light);
    padding:36px; border-radius:18px; box-shadow:0 30px 80px rgba(0,0,0,0.6);
  }

  .project {
    display:flex; gap:20px; align-items:center; justify-content:space-between; padding:18px; border-radius:12px;
    border:1px solid rgba(255,255,255,0.04); margin-top:12px; background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
  }
  .project .meta { flex:1; min-width:200px; }
  .project h3{ margin:0; color:var(--text-light); font-size:20px; }
  .project p{ margin:8px 0 0 0; color:rgba(238,246,248,0.85); line-height:1.5; }

  .project .art{ width:360px; height:180px; border-radius:10px; overflow:hidden; background:transparent; }
  .project .art img{ width:100%; height:100%; object-fit:cover; opacity:0.18; filter: blur(1px) saturate(1.02); }

  /* CONTACT panel - dark */
  .contact .stage{ align-items:center; justify-content:center; padding:72px; }
  .contact-card{
    width:100%; max-width:900px; padding:36px; border-radius:18px; text-align:center;
    background: linear-gradient(180deg, rgba(5,12,16,0.92), rgba(3,8,12,0.95));
    color:var(--text-light); box-shadow: 0 30px 80px rgba(0,0,0,0.6);
  }
  .contact-card h2{ margin:0 0 8px 0; font-size:26px; font-weight:800; }
  .contact-card p{ margin:8px 0 0 0; color:rgba(238,246,248,0.85); }

  /* Panel reveal animation */
  .panel .stage > * { opacity:0; transform: translateY(18px) scale(.996); transition: transform 680ms cubic-bezier(.2,.9,.2,1), opacity 680ms ease; }
  .panel.in-view .stage > * { opacity:1; transform: translateY(0) scale(1); }

  /* small screens */
  @media (max-width:980px){
    .portrait{ width:200px; height:200px; }
    .story-grid{ grid-template-columns: 1fr; }
    .project .art{ width:100%; height:140px; }
  }
</style>
</head>
<body>

<!-- Viewport / Panels -->
<div class="viewport" id="viewport" tabindex="0" aria-label="Portfolio panels">

  <!-- Panel 1: HERO -->
  <section class="panel hero" id="hero">
    <div class="stage">
      <div class="hero-inner" role="main" aria-labelledby="hero-name">
        <div class="portrait" aria-hidden="false">
          <!-- Replace photo.png with your portrait (transparent PNG recommended). Lazy load for performance -->
          <img src="photo.png" alt="Venkata Raghavendra KADIYALA" loading="lazy" id="mainPhoto">
        </div>

        <h1 id="hero-name" class="name">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
        <div class="tagline">Mechanical Engineer · Creative Designer — Train interiors & systems</div>

        <div class="hero-actions" aria-hidden="false">
          <a class="btn-primary" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener noreferrer">
            <!-- LinkedIn icon inline -->
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M4 4h4v16H4zM6 2a2 2 0 110 4 2 2 0 010-4zM10 8h3.7v2.1h.1c.5-.9 1.7-2.1 3.6-2.1 3.8 0 4.5 2.5 4.5 5.7V20H18v-5.1c0-1.2 0-2.8-1.7-2.8-1.7 0-2 1.4-2 2.7V20h-4V8z" stroke="#052425" stroke-width="0.6" stroke-linecap="round" stroke-linejoin="round" /></svg>
            LinkedIn
          </a>

          <a class="btn-primary" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener noreferrer">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><rect x="3" y="3" width="18" height="18" rx="5" stroke="#052425" stroke-width="0.6"/><circle cx="12" cy="12" r="3" stroke="#052425" stroke-width="0.6"/></svg>
            Instagram
          </a>

          <a class="btn-ghost" href="tel:+33755662821">☎ +33 7 55 66 28 21</a>
          <a class="btn-ghost" href="mailto:venkata.france@gmail.com">✉ venkata.france@gmail.com</a>
        </div>
      </div>
    </div>
  </section>

  <!-- Panel 2: STORY / DESCRIPTION -->
  <section class="panel story" id="story">
    <div class="stage">
      <div class="story-card" role="article" aria-labelledby="storyHeading">
        <div class="story-grid">
          <div>
            <div class="meta" style="display:flex; justify-content:space-between; align-items:center;">
              <div id="storyHeading" style="font-weight:800; font-size:18px">About — À propos</div>
              <div style="color:var(--muted); font-weight:700">Light → Depth</div>
            </div>

            <h2 style="margin-top:12px; font-size:26px; font-weight:800">I design engineering products with a refined user sense.</h2>

            <p style="margin-top:18px">
              <strong>English:</strong> I combine rigorous mechanical engineering with design sensibility to create train and vehicle interiors that are functional, manufacturable and visually precise. I lead CAD projects (CATIA V5), conduct FEA validations and coordinate suppliers to deliver production-ready 3D models.<br><br>
              <strong>Français :</strong> J'allie ingénierie mécanique et sens du design pour concevoir des intérieurs ferroviaires et véhicules fonctionnels et esthétiques. Pilotage CAO (CATIA V5), validations EF et coordination fournisseurs pour des modèles 3D prêts production.
            </p>

            <div class="story-highlights" aria-hidden="true">
              <div class="stat"><div class="num">5+</div><div class="label">Years experience</div></div>
              <div class="stat"><div class="num">M0 → M5</div><div class="label">Model maturity</div></div>
              <div class="stat"><div class="num">CAD & FEA</div><div class="label">CATIA V5 • Hyperworks</div></div>
            </div>
          </div>

          <aside style="display:flex; align-items:center; justify-content:center;">
            <div style="width:420px; background:linear-gradient(180deg,#ffffff,#f6f7f8); padding:18px; border-radius:12px; box-shadow:0 18px 40px rgba(6,12,18,0.06); text-align:center;">
              <div style="font-weight:800; font-size:20px; color:var(--text-dark)">What I focus on</div>
              <div style="margin-top:12px; color:var(--muted); font-weight:700">Train interiors • Component design • Integration • CAD governance • FEA</div>
            </div>
          </aside>
        </div>
      </div>
    </div>
  </section>

  <!-- Panel 3: EXPERIENCE - each project block inside, but whole panel shows them stacked (you can make each a panel if you prefer) -->
  <section class="panel work" id="work">
    <div class="stage">
      <div class="work-card" role="region" aria-labelledby="workHeading">
        <div style="display:flex; justify-content:space-between; align-items:center;">
          <div id="workHeading" style="font-weight:800; font-size:18px">Work — Projets sélectionnés</div>
          <div style="color:var(--muted); font-weight:700">Product-style presentation</div>
        </div>

        <!-- Project blocks -->
        <div class="project" role="article" aria-label="SEGULA Project OSTA">
          <div class="meta">
            <h3>SEGULA — Project OSTA (Front Office)</h3>
            <p>Lead interior delivery: windows, blinds, intercoms, electrical cabinets, under-seat systems. Supplier coordination and 3D model maturity (M0→M5).</p>
          </div>
          <div class="art" aria-hidden="true">
            <img src="photo.png" alt="soft background art" loading="lazy">
          </div>
        </div>

        <div class="project" role="article" aria-label="SEGULA BaWu">
          <div class="meta">
            <h3>SEGULA — BaWu (Validation & QA)</h3>
            <p>3D validation workflows, integration issue prevention, KPI & OIL tracking to ensure quality handover.</p>
          </div>
          <div class="art" aria-hidden="true"><img src="photo.png" alt="" loading="lazy"></div>
        </div>

        <div class="project" role="article" aria-label="SNCF">
          <div class="meta">
            <h3>SNCF — FEA & Automation</h3>
            <p>Automation for bolted assemblies, mesh & static/non-static analysis for seat supports. Tooling in Hyperworks/Optistruct and TCL scripting.</p>
          </div>
          <div class="art" aria-hidden="true"><img src="photo.png" alt="" loading="lazy"></div>
        </div>

        <!-- If you want each project as its own full-screen panel, we can split them into separate <section>s -->
      </div>
    </div>
  </section>

  <!-- Panel 4: CONTACT -->
  <section class="panel contact" id="contact">
    <div class="stage">
      <div class="contact-card" role="contentinfo" aria-labelledby="contactHeading">
        <h2 id="contactHeading">Let's build something exceptional — Parlons</h2>
        <p style="margin-top:12px; color:rgba(238,246,248,0.9)">Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a> — Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
        <div style="margin-top:18px; display:flex; gap:14px; align-items:center; justify-content:center; flex-wrap:wrap;">
          <a class="btn-primary" href="mailto:venkata.france@gmail.com">Email me</a>
          <a class="btn-primary" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
          <a class="btn-primary" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
        </div>
        <div style="margin-top:22px; color:var(--muted)">© <span id="year"></span> Venkata Raghavendra KADIYALA</div>
      </div>
    </div>
  </section>

</div>

<script>
  // set footer year
  document.getElementById('year').textContent = new Date().getFullYear();

  // IntersectionObserver to add .in-view class per panel
  (function(){
    const panels = document.querySelectorAll('.panel');
    const io = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('in-view');
        } else {
          // keep visible once entered (avoid flicker)
        }
      });
    }, { threshold: 0.5 });
    panels.forEach(p => io.observe(p));
  })();

  // Smooth one-panel snapping for wheel + keyboard
  (function(){
    const viewport = document.getElementById('viewport');
    let isThrottled = false;

    function snapTo(direction){
      const panels = Array.from(document.querySelectorAll('.panel'));
      // find index of panel nearest to viewport top
      const top = viewport.scrollTop;
      let closest = 0;
      let minDist = Infinity;
      panels.forEach((p, i) => {
        const d = Math.abs(p.offsetTop - top);
        if(d < minDist){ minDist = d; closest = i; }
      });
      let target = closest;
      if(direction === 'next') target = Math.min(panels.length - 1, closest + 1);
      if(direction === 'prev') target = Math.max(0, closest - 1);
      if(target !== closest) panels[target].scrollIntoView({behavior:'smooth'});
    }

    viewport.addEventListener('wheel', (e) => {
      if(isThrottled) return;
      isThrottled = true;
      setTimeout(()=> isThrottled = false, 450);
      if(e.deltaY > 10) snapTo('next');
      else if(e.deltaY < -10) snapTo('prev');
    }, {passive:true});

    window.addEventListener('keydown', (e) => {
      if(e.key === 'ArrowDown') snapTo('next');
      if(e.key === 'ArrowUp') snapTo('prev');
      if(e.key === 'Home') document.querySelector('.panel').scrollIntoView({behavior:'smooth'});
      if(e.key === 'End') {
        const panels = document.querySelectorAll('.panel');
        panels[panels.length-1].scrollIntoView({behavior:'smooth'});
      }
    });
  })();

  // Friendly: if photo.png fails to load, replace with initials
  (function(){
    const img = document.getElementById('mainPhoto');
    img.addEventListener('error', function(){
      const parent = img.parentNode;
      parent.innerHTML = '<div style="width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,var(--accent-teal),var(--accent-gold));color:#052422;font-weight:800;font-size:48px;">VR</div>';
    });
  })();
</script>
</body>
</html>
