<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<meta name="description" content="Portfolio of Venkata Raghavendra KADIYALA — Mechanical Engineer & Creative Designer (EN / FR)" />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-light:#f7f6f4;
    --bg-mid:#e9eef0;
    --bg-dark:#0b1116;
    --accent-teal:#17c3a2;
    --accent-gold:#e6b66d;
    --muted:#6b7780;
    --text:#071622;
    --glass: rgba(255,255,255,0.6);
    --radius:14px;
    --snap: y mandatory;
    font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;
  }

  /* basic reset */
  *{box-sizing:border-box}
  html,body{height:100%; margin:0; background:linear-gradient(180deg,var(--bg-light),#eaeff1 30%, #cbd7dc 55%, var(--bg-dark)); color:var(--text); -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;}
  a{color:inherit; text-decoration:none}

  /* viewport panels — full screen, snap to each center */
  .viewport{
    height:100vh;
    overflow-y:auto;
    scroll-snap-type: y var(--snap);
    -webkit-overflow-scrolling:touch;
  }

  section.panel{
    position:relative;
    min-height:100vh;
    padding:48px 28px;
    display:flex;
    align-items:center;
    justify-content:center;
    scroll-snap-align:center;
  }

  /* hero: white -> mid */
  .hero {
    background: linear-gradient(180deg, #fff 0%, #f5f6f7 50%);
  }

  /* mid-dark sections will use overlay */
  .scene-dark {
    background: linear-gradient(180deg, rgba(6,12,20,0.9), rgba(3,8,15,0.95));
    color: #eef6f8;
  }

  /* content card centered on each panel */
  .card {
    position:relative;
    width:min(1100px,94%);
    display:grid;
    grid-template-columns: 1fr 420px;
    gap:26px;
    align-items:center;
    padding:28px;
    border-radius:18px;
    background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,255,255,0.88));
    box-shadow: 0 30px 80px rgba(16,24,32,0.12);
    border: 1px solid rgba(20,30,40,0.04);
    overflow:hidden;
  }
  .card.dark {
    background: linear-gradient(180deg, rgba(8,12,18,0.54), rgba(6,8,12,0.36));
    border: 1px solid rgba(255,255,255,0.03);
    box-shadow: 0 30px 80px rgba(1,2,6,0.6);
  }

  /* hero layout */
  .hero .card {
    grid-template-columns: 420px 1fr;
    background: transparent;
    box-shadow:none;
    border:none;
  }

  /* left column (image) */
  .photo-wrap {
    display:flex; align-items:center; justify-content:center;
  }
  .photo {
    width:360px; height:360px; border-radius:22px; overflow:hidden;
    border: 10px solid rgba(255,255,255,0.85);
    box-shadow: 0 18px 60px rgba(10,20,30,0.12);
    background: linear-gradient(135deg,var(--accent-teal),var(--accent-gold));
  }
  .photo img{ width:100%; height:100%; object-fit:cover; display:block; filter: contrast(105%) saturate(106%); }

  /* right column */
  .intro { padding:8px 4px; }
  h1.name { margin:0; font-size:36px; line-height:1; font-weight:800; letter-spacing:0.6px; color:var(--text); }
  .tag { margin-top:10px; color:var(--muted); font-weight:600; font-size:15px; }
  .cta-row { margin-top:18px; display:flex; gap:12px; align-items:center; flex-wrap:wrap; }

  .social-btn {
    display:inline-flex; align-items:center; gap:10px; padding:12px 16px; border-radius:12px; font-weight:800; font-size:14px;
    background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold)); color:#072425; box-shadow: 0 8px 30px rgba(22,44,40,0.12);
    transition: transform .18s ease, box-shadow .18s ease;
  }
  .social-btn:hover{ transform:translateY(-6px); box-shadow: 0 20px 60px rgba(22,44,40,0.14); }

  .social-ghost {
    display:inline-flex; align-items:center; gap:10px; padding:10px 14px; border-radius:10px; font-weight:700; font-size:13px;
    background:transparent; border:1px solid rgba(16,24,32,0.06);
  }
  .contact-row { margin-top:16px; color:var(--muted); display:flex; gap:14px; align-items:center; flex-wrap:wrap; font-weight:600; }

  /* story panel: cleaner white card */
  .story-card { grid-template-columns: 1fr; padding:42px; gap:18px; }
  .story-card p { margin:0; color:var(--muted); line-height:1.6; font-size:16px; }

  /* experience scenes use dark card */
  .work-card { grid-template-columns: 1fr; padding:36px; gap:20px; }
  .project {
    display:flex; gap:16px; align-items:center; justify-content:space-between; gap:22px; flex-wrap:wrap;
    padding:18px; border-radius:12px; border:1px solid rgba(255,255,255,0.04); background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
  }
  .project.dark { background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); }

  .project .text { flex:1; min-width:260px; }
  .project h3 { margin:0; font-size:20px; color:var(--text); }
  .project p { margin:8px 0 0 0; color:var(--muted); line-height:1.5; }

  .project .art {
    width:360px; height:180px; border-radius:10px; overflow:hidden; background:linear-gradient(90deg, rgba(23,195,162,0.12), rgba(230,182,109,0.08));
    display:flex; align-items:center; justify-content:center;
  }
  .project .art img { width:100%; height:100%; object-fit:cover; opacity:0.18; filter: blur(1px) saturate(1.02); }

  /* contact CTA */
  .contact-cta {
    display:flex; gap:12px; align-items:center; justify-content:center; flex-wrap:wrap;
    margin-top:14px;
  }
  .big-cta {
    padding:14px 22px; border-radius:14px; font-weight:800; font-size:16px;
    background:linear-gradient(90deg,var(--accent-teal),var(--accent-gold));
    color:#052425; box-shadow: 0 18px 50px rgba(20,40,36,0.12);
  }

  /* slide/fade animations triggered per panel */
  .panel .card, .panel .project, .panel .intro, .panel .photo { opacity:0; transform: translateY(24px) scale(.995); transition: opacity 700ms ease, transform 700ms cubic-bezier(.2,.95,.2,1); }
  .panel.in-view .card, .panel.in-view .project, .panel.in-view .intro, .panel.in-view .photo { opacity:1; transform: translateY(0) scale(1); }

  /* header fixed (small) */
  header.topbar { position:fixed; top:18px; left:24px; right:24px; z-index:80; display:flex; justify-content:space-between; align-items:center; padding:6px 12px; pointer-events:auto; }
  header.topbar .mini { display:flex; gap:12px; align-items:center; }
  .mini .icon { width:42px; height:42px; border-radius:10px; background:linear-gradient(135deg,var(--accent-teal),var(--accent-gold)); display:flex; align-items:center; justify-content:center; font-weight:800; color:#052425; box-shadow:0 12px 30px rgba(20,40,36,0.12); }

  /* responsive tweaks */
  @media (max-width:980px){
    .card, .card.dark { grid-template-columns: 1fr; }
    .hero .card { grid-template-columns: 1fr; gap:20px }
    .photo { width:240px; height:240px; border-radius:14px; }
    .project .art { width:100%; height:140px; }
  }
</style>
</head>
<body>

<!-- small floating topbar with social quick links -->
<header class="topbar" aria-hidden="false">
  <div class="mini">
    <div class="icon">VR</div>
    <div style="font-weight:700">Venkata Raghavendra KADIYALA</div>
  </div>
  <nav style="display:flex; gap:10px; align-items:center">
    <a class="social-ghost" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener noreferrer">LinkedIn</a>
    <a class="social-ghost" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener noreferrer">Instagram</a>
    <a class="social-ghost" href="mailto:venkata.france@gmail.com">Email</a>
  </nav>
</header>

<!-- panels container -->
<div class="viewport" id="viewport" tabindex="0" aria-label="Portfolio panels">

  <!-- HERO (panel 1) — full-screen landing -->
  <section class="panel hero" id="panel-hero" aria-label="Hero: About me">
    <div class="card" role="region" aria-labelledby="hero-title">
      <div class="photo-wrap">
        <div class="photo" aria-hidden="true">
          <!-- place the AI-generated image file in same folder as this index.html with exactly this name -->
          <img src="A_webpage_design_for_Venkata_Raghavendra_Kadiyala_.png" alt="Venkata Raghavendra Kadiyala portrait (AI-generated)">
        </div>
      </div>

      <div class="intro">
        <div id="hero-title" class="slide">
          <h1 class="name">Venkata Raghavendra <span style="color:var(--accent-teal)">KADIYALA</span></h1>
          <div class="tag">Mechanical Engineer • Creative Designer — Train interiors & systems</div>
        </div>

        <div class="cta-row" aria-hidden="false">
          <a class="social-btn" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener noreferrer" title="LinkedIn">
            <!-- small LinkedIn svg -->
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M4 4h4v16H4zM6 2a2 2 0 110 4 2 2 0 010-4zM10 8h3.7v2.1h.1c.5-.9 1.7-2.1 3.6-2.1 3.8 0 4.5 2.5 4.5 5.7V20H18v-5.1c0-1.2 0-2.8-1.7-2.8-1.7 0-2 1.4-2 2.7V20h-4V8z" stroke="#052425" stroke-width="0.6" stroke-linecap="round" stroke-linejoin="round" /></svg>
            LinkedIn
          </a>

          <a class="social-btn" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener noreferrer" title="Instagram">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" aria-hidden="true"><rect x="3" y="3" width="18" height="18" rx="5" stroke="#052425" stroke-width="0.6"/><circle cx="12" cy="12" r="3" stroke="#052425" stroke-width="0.6"/></svg>
            Instagram
          </a>

          <a class="social-ghost" href="tel:+33755662821" title="Call">☎ +33 7 55 66 28 21</a>
          <a class="social-ghost" href="mailto:venkata.france@gmail.com" title="Email">✉ venkata.france@gmail.com</a>
        </div>

        <div class="contact-row" style="margin-top:20px;">
          <div style="font-weight:800; font-size:13px; color:var(--muted)">Creative • Technical • Product thinking</div>
          <div style="margin-left:10px;color:var(--muted);font-weight:700;">Available for collaboration</div>
        </div>
      </div>
    </div>
  </section>

  <!-- PANEL 2: STORY / DESCRIPTION (distinct, not visible with hero) -->
  <section class="panel" id="panel-story" aria-label="Story: About and details">
    <div class="card story-card" role="region" aria-labelledby="story-title">
      <div style="grid-column:1/ -1;">
        <div class="meta" style="justify-content:space-between;">
          <div id="story-title" style="font-weight:800; font-size:18px">About — À propos</div>
          <div style="color:var(--muted); font-weight:700">Light → Depth</div>
        </div>

        <h1 style="margin-top:12px; font-size:28px">I design engineering experiences that look and feel refined.</h1>

        <p style="margin-top:14px; color:var(--muted); font-size:16px; line-height:1.6">
          English: I combine mechanical engineering and design thinking to produce robust, elegant solutions for rail and vehicle interiors.
          I lead CAD projects (CATIA V5), coordinate suppliers, and deliver production-ready 3D models and validated assemblies. I focus on clarity, manufacturability and user experience.<br><br>
          <em style="color:var(--muted)">Français : J’allie ingénierie mécanique et design pour produire des solutions robustes et élégantes pour l’aménagement ferroviaire et automobile.
          Pilotage CAO (CATIA V5), coordination fournisseurs et livraison de modèles 3D prêts production. Priorité à la clarté, la fabricabilité et l’expérience utilisateur.</em>
        </p>

        <div style="display:flex; gap:18px; margin-top:22px; flex-wrap:wrap;">
          <div style="background:linear-gradient(180deg,#fff,#f6f6f7); padding:18px; border-radius:12px; min-width:160px; box-shadow:0 12px 30px rgba(16,24,32,0.06)">
            <div style="font-weight:800; font-size:22px">5+</div>
            <div style="color:var(--muted); font-weight:700">Years experience</div>
          </div>

          <div style="background:linear-gradient(180deg,#fff,#f6f6f7); padding:18px; border-radius:12px; min-width:160px; box-shadow:0 12px 30px rgba(16,24,32,0.06)">
            <div style="font-weight:800; font-size:22px">M0 → M5</div>
            <div style="color:var(--muted); font-weight:700">3D model maturity</div>
          </div>

          <div style="background:linear-gradient(180deg,#fff,#f6f6f7); padding:18px; border-radius:12px; min-width:160px; box-shadow:0 12px 30px rgba(16,24,32,0.06)">
            <div style="font-weight:800; font-size:22px">CAD & FEA</div>
            <div style="color:var(--muted); font-weight:700">CATIA V5 • Hyperworks</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PANEL 3: EXPERIENCE (each project as separate block in its own panel) -->
  <section class="panel" id="panel-experience" aria-label="Experience overview" >
    <div class="card dark work-card" role="region" aria-labelledby="work-title">
      <div style="grid-column:1/-1;">
        <div class="meta" style="justify-content:space-between;">
          <div id="work-title" style="font-weight:800; color:var(--text); font-size:18px">Work highlights — Projets</div>
          <div style="color:var(--muted)">Selected projects, one scene at a time</div>
        </div>
      </div>

      <!-- Project 1 -->
      <div class="project" style="margin-top:12px;">
        <div class="text">
          <h3 style="color:var(--text)">SEGULA — Project OSTA (Front Office)</h3>
          <p>Lead interior design integration: windows, blinds, intercoms, electrical cabinets and under-seat systems. Deliver validated 3D models for supplier integration (M0→M5).</p>
        </div>
        <div class="art" aria-hidden="true">
          <!-- soft background art: use an image later for better realism -->
          <img src="A_webpage_design_for_Venkata_Raghavendra_Kadiyala_.png" alt="soft train art">
        </div>
      </div>

      <!-- Project 2 -->
      <div class="project" style="margin-top:18px;">
        <div class="text">
          <h3 style="color:var(--text)">SEGULA — BaWu (Validation & QA)</h3>
          <p>3D validation workflows, identification and prevention of integration issues, KPI and OIL tracking for quality handover.</p>
        </div>
        <div class="art" aria-hidden="true">
          <img src="A_webpage_design_for_Venkata_Raghavendra_Kadiyala_.png" alt="soft design art">
        </div>
      </div>

      <!-- Project 3 -->
      <div class="project" style="margin-top:18px;">
        <div class="text">
          <h3 style="color:var(--text)">SNCF — FEA & Automation</h3>
          <p>FEA, automation of bolted assemblies (TCL), static & non-static analyses for seat supports and validation using Hyperworks/Optistruct.</p>
        </div>
        <div class="art" aria-hidden="true">
          <img src="A_webpage_design_for_Venkata_Raghavendra_Kadiyala_.png" alt="soft engineering art">
        </div>
      </div>

    </div>
  </section>

  <!-- PANEL 4: CALL TO ACTION / CONTACT -->
  <section class="panel" id="panel-contact" aria-label="Contact">
    <div class="card dark" role="region" aria-labelledby="contact-title">
      <div style="grid-column:1/-1;">
        <div class="meta" style="justify-content:space-between;">
          <div id="contact-title" style="font-weight:800; color:var(--text); font-size:18px">Let's build something exceptional — Parlons</div>
          <div style="color:var(--muted)">Reach out — Contactez-moi</div>
        </div>
      </div>

      <div style="display:flex; gap:22px; align-items:center; justify-content:space-between; width:100%; flex-wrap:wrap;">
        <div style="flex:1; min-width:280px;">
          <h2 style="margin:0; color:var(--text)">Get in touch</h2>
          <p style="color:var(--muted); margin-top:8px">Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a><br>Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
          <div class="contact-cta">
            <a class="big-cta" href="mailto:venkata.france@gmail.com">Email me</a>
            <a class="social-btn" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
            <a class="social-btn" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
          </div>
        </div>

        <aside style="width:360px; min-width:240px;">
          <div style="background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); padding:18px; border-radius:12px; text-align:center;">
            <div style="font-weight:800; font-size:20px">Available for hire</div>
            <div style="color:var(--muted); margin-top:8px">Freelance and collaboration — open to product-focused roles</div>
            <div style="margin-top:16px; color:var(--muted); font-size:13px">© <span id="year"></span> Venkata Raghavendra KADIYALA</div>
          </div>
        </aside>
      </div>

    </div>
  </section>

</div>

<script>
  // set year
  document.getElementById('year').textContent = new Date().getFullYear();

  // IntersectionObserver to toggle .in-view per panel (panel-level animations)
  (function(){
    const panels = document.querySelectorAll('.panel');
    const io = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('in-view');
        } else {
          // keep once visible — this prevents panels from flickering on small scrolls
          // entry.target.classList.remove('in-view');
        }
      });
    }, { threshold: 0.45 });

    panels.forEach(p => io.observe(p));
  })();

  // Smooth wheel snapping between panels (makes experience feel like "one-panel at a time")
  (function(){
    const viewport = document.getElementById('viewport');
    let isThrottled = false;
    function snapTo(direction){
      const panels = Array.from(document.querySelectorAll('.panel'));
      // find the panel whose center is closest to viewport center
      const viewportCenter = viewport.scrollTop + (viewport.clientHeight / 2);
      let closestIndex = 0;
      let closestDist = Infinity;
      panels.forEach((p, i) => {
        const rect = p.getBoundingClientRect();
        const center = p.offsetTop + (rect.height/2);
        const dist = Math.abs(center - viewportCenter);
        if(dist < closestDist){ closestDist = dist; closestIndex = i; }
      });
      let targetIndex = closestIndex;
      if(direction === 'next') targetIndex = Math.min(panels.length - 1, closestIndex + 1);
      if(direction === 'prev') targetIndex = Math.max(0, closestIndex - 1);
      if(targetIndex !== closestIndex) panels[targetIndex].scrollIntoView({behavior:'smooth', block:'center'});
    }

    viewport.addEventListener('wheel', (e) => {
      if(isThrottled) return;
      isThrottled = true;
      setTimeout(()=> isThrottled=false, 420);
      if(e.deltaY > 10) snapTo('next');
      else if(e.deltaY < -10) snapTo('prev');
    }, {passive:true});

    // keyboard navigation
    window.addEventListener('keydown', (e) => {
      if(e.key === 'ArrowDown') snapTo('next');
      if(e.key === 'ArrowUp') snapTo('prev');
      if(e.key === 'Home') document.querySelector('.panel').scrollIntoView({behavior:'smooth', block:'center'});
      if(e.key === 'End') document.querySelectorAll('.panel')[document.querySelectorAll('.panel').length-1].scrollIntoView({behavior:'smooth', block:'center'});
    });
  })();

  // Accessibility: make header quick links focusable and announce on load
  window.addEventListener('load', () => {
    const firstLink = document.querySelector('header.topbar a');
    if(firstLink) firstLink.setAttribute('tabindex','0');
  });
</script>
</body>
</html>
