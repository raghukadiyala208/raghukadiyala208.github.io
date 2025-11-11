<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<meta name="description" content="Portfolio — Venkata Raghavendra KADIYALA (Mechanical Engineer & Creative Designer) EN/FR" />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-day: #ffffff;
    --text-day: #071622;
    --muted: #6b7780;
    --accent-teal: #17c3a2;
    --linkedin: #0077b5;
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;background:var(--bg-day);color:var(--text-day);-webkit-font-smoothing:antialiased;}
  a{color:inherit;text-decoration:none}

  /* Layout: stacked sections, each full viewport */
  section { min-height:100vh; width:100%; position:relative; display:flex; align-items:center; justify-content:center; padding:32px; overflow:hidden; }
  .bg { position:absolute; inset:0; background-size:cover; background-position:center; filter:brightness(.92); z-index:0; }
  .bg.fallback { background:linear-gradient(180deg,#f6f8f9,#e9f0f2); }
  .overlay { position:absolute; inset:0; z-index:1; pointer-events:none; }
  .content { position:relative; z-index:6; width:100%; max-width:1200px; text-align:center; display:flex; flex-direction:column; align-items:center; justify-content:center; gap:18px; padding:28px; }

  /* Title / text */
  h1.title { margin:0; font-weight:900; font-size:clamp(36px,7.5vw,96px); line-height:0.92; text-transform:uppercase; }
  h2.subtitle { margin:0; font-weight:700; color:var(--muted); font-size:18px; }
  p.lead { margin:0; color:var(--muted); max-width:980px; line-height:1.7; font-size:16px; }

  /* portrait floating (no frame) */
  .portrait { display:block; width:auto; height:64vh; max-height:760px; object-fit:contain; filter: drop-shadow(0 40px 90px rgba(6,12,20,0.18)); }

  /* floating overlay images */
  .float { position:absolute; z-index:5; pointer-events:none; width:46vw; max-width:760px; filter:drop-shadow(0 34px 90px rgba(3,9,16,0.55)); }

  /* topbar */
  .topbar { position:fixed; right:18px; top:16px; z-index:98; display:flex; gap:10px; align-items:center; }
  .btn { display:inline-flex; align-items:center; gap:8px; padding:10px 14px; border-radius:10px; font-weight:800; color:#fff; cursor:pointer; text-decoration:none; box-shadow:0 12px 30px rgba(2,8,10,0.12); }
  .btn.linkedin { background:var(--linkedin) }
  .btn.instagram { background:linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5) }
  .btn.contact { background:linear-gradient(90deg,var(--accent-teal),#e6b66d); color:#052425; }

  /* small white cards for About / Publication / Education / Skills */
  .card { background:linear-gradient(180deg,#fff,#fbfbfb); border-radius:14px; padding:32px; box-shadow:0 30px 80px rgba(8,12,18,0.06); color:var(--text-day); max-width:1000px; text-align:left; }
  .card h3{ margin-top:0; }

  /* responsive */
  @media (max-width:980px){
    .float{ width:78vw; }
    .portrait{ height:52vh; }
    h1.title{ font-size:clamp(32px,10vw,56px); }
  }
</style>
</head>
<body>

<!-- topbar -->
<div class="topbar" role="navigation" aria-label="Social">
  <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
  <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
  <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
</div>

<!-- SECTION: HERO -->
<section id="hero" aria-label="Hero">
  <div class="bg" id="bg-hero" style="background-image:url('ai_about.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.9), rgba(255,255,255,0.7));"></div>

  <div class="content">
    <img src="portrait.png" alt="Portrait" class="portrait" id="portrait" loading="eager">
    <h1 class="title">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
    <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
    <p class="lead">☎ +33 7 55 66 28 21 · ✉ <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a></p>
  </div>
</section>

<!-- SECTION: ABOUT -->
<section id="about" aria-label="About">
  <div class="bg" id="bg-about" style="background-image:url('ai_about.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.94), rgba(250,250,250,0.9));"></div>

  <div class="content card" role="article" aria-labelledby="aboutTitle">
    <h3 id="aboutTitle">About — À propos</h3>
    <p class="lead"><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability and clear user-focused outcomes.</p>
    <p class="lead" style="margin-top:12px;"><strong>Français : </strong>J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>
  </div>
</section>

<!-- EXPERIENCE sections: each full viewport, with bg + overlay + float + centered text -->
<!-- SEGULA — OSTA -->
<section id="osta" aria-label="SEGULA OSTA">
  <div class="bg" style="background-image:url('ai_osta.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(4,10,14,0.52), rgba(2,6,10,0.66));"></div>

  <img src="float_osta.png" alt="" class="float" style="right:6%; top:14%;" loading="lazy">
  <div class="content">
    <h1 class="title">SEGULA — Project OSTA</h1>
    <h2 class="subtitle">Front office · Train interior systems · M0 → M5</h2>
    <p class="lead">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
  </div>
</section>

<!-- SEGULA — BaWu -->
<section id="bawu" aria-label="SEGULA BaWu">
  <div class="bg" style="background-image:url('ai_bawu.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(6,12,12,0.48), rgba(4,8,8,0.62));"></div>

  <img src="float_bawu.png" alt="" class="float" style="left:8%; top:16%;" loading="lazy">
  <div class="content">
    <h1 class="title">SEGULA — BaWu</h1>
    <h2 class="subtitle">Validation & QA · Integration focus</h2>
    <p class="lead">3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
  </div>
</section>

<!-- SEGULA — RER NG -->
<section id="rerng" aria-label="SEGULA RER NG">
  <div class="bg" style="background-image:url('ai_rerng.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(5,8,12,0.5), rgba(3,6,10,0.66));"></div>

  <img src="float_rerng.png" alt="" class="float" style="right:10%; top:18%;" loading="lazy">
  <div class="content">
    <h1 class="title">SEGULA — RER NG</h1>
    <h2 class="subtitle">Change requests · On-site surveys</h2>
    <p class="lead">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
  </div>
</section>

<!-- SEGULA — DSB -->
<section id="dsb" aria-label="SEGULA DSB">
  <div class="bg" style="background-image:url('ai_dsb.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(3,6,14,0.6), rgba(2,4,10,0.72));"></div>

  <img src="float_dsb.png" alt="" class="float" style="left:6%; top:12%;" loading="lazy">
  <div class="content">
    <h1 class="title">SEGULA — DSB</h1>
    <h2 class="subtitle">Interior layout · Integration</h2>
    <p class="lead">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
  </div>
</section>

<!-- SNCF -->
<section id="sncf" aria-label="SNCF">
  <div class="bg" style="background-image:url('ai_sncf.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(6,8,12,0.54), rgba(3,6,10,0.66));"></div>

  <img src="float_sncf.png" alt="" class="float" style="right:8%; top:10%;" loading="lazy">
  <div class="content">
    <h1 class="title">SNCF</h1>
    <h2 class="subtitle">FEA & Automation · HyperWorks / OptiStruct</h2>
    <p class="lead">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
  </div>
</section>

<!-- LAMIH -->
<section id="lamih" aria-label="LAMIH">
  <div class="bg" style="background-image:url('ai_lamih.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(30,18,36,0.36), rgba(4,6,10,0.6));"></div>

  <img src="float_lamih.png" alt="" class="float" style="left:10%; top:14%;" loading="lazy">
  <div class="content">
    <h1 class="title">LAMIH</h1>
    <h2 class="subtitle">Behavioural analysis · Safety concepts</h2>
    <p class="lead">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
  </div>
</section>

<!-- PM DIMENSIONS -->
<section id="pmdim" aria-label="PM DIMENSIONS">
  <div class="bg" style="background-image:url('ai_pmdimensions.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,250,240,0.06), rgba(6,6,8,0.18));"></div>

  <img src="float_pmdimensions.png" alt="" class="float" style="right:8%; top:16%;" loading="lazy">
  <div class="content">
    <h1 class="title" style="color:#071622">PM DIMENSIONS</h1>
    <h2 class="subtitle" style="color:rgba(6,6,8,0.9)">Part design · Prototyping</h2>
    <p class="lead" style="color:rgba(6,6,8,0.9)">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
  </div>
</section>

<!-- Indian Railways -->
<section id="indianrail" aria-label="Indian Railways">
  <div class="bg" style="background-image:url('ai_indianrail.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(8,6,4,0.14), rgba(6,4,6,0.28));"></div>

  <img src="float_indianrail.png" alt="" class="float" style="left:6%; top:16%;" loading="lazy">
  <div class="content">
    <h1 class="title">Indian Railways (Intern)</h1>
    <h2 class="subtitle">Prototype coupling · Maintenance optimisation</h2>
    <p class="lead">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
  </div>
</section>

<!-- Education -->
<section id="education" aria-label="Education">
  <div class="bg fallback"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.96), rgba(250,250,250,0.92));"></div>

  <div class="content card">
    <h3>Education — Formation</h3>
    <p class="lead"><strong>Master</strong> — International Transport & Energy — INSA Hauts-de-France (2019–2021)<br>
    <strong>Bachelor</strong> — Mechanical Engineering — KL University (2014–2018)</p>
    <p class="lead" style="margin-top:8px;">Selected project: <strong>Enhancement of Refrigeration Effect Using Flue Gases from Chimney</strong> — April 2018.</p>
  </div>
</section>

<!-- Skills -->
<section id="skills" aria-label="Skills">
  <div class="bg fallback"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.96), rgba(250,250,250,0.92));"></div>

  <div class="content card">
    <h3>Skills & Tools — Compétences</h3>
    <div style="display:flex;gap:10px;flex-wrap:wrap;margin-top:14px;">
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>CATIA V5</strong></div>
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>Ansys</strong></div>
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>HyperWorks / OptiStruct</strong></div>
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,0.06)"><strong>PDM / DMA / SAM</strong></div>
    </div>
    <ul style="text-align:left;color:var(--muted);line-height:1.6;margin-top:12px;">
      <li>Train interiors design & integration • Conception et intégration d’intérieurs ferroviaires</li>
      <li>Vehicle part design & packaging • Conception de pièces et intégration automobile</li>
      <li>FEA, meshing, static & dynamic analysis • Maillage, analyses statique & dynamique</li>
    </ul>
  </div>
</section>

<!-- Publication -->
<section id="publication" aria-label="Publication">
  <div class="bg" style="background-image:url('ai_publication.jpg'); filter:brightness(.9)"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.92), rgba(250,250,250,0.88));"></div>

  <div class="content card" style="text-align:left;">
    <h3>Publication — Avril 2018</h3>
    <p class="lead"><strong>Enhancement of Refrigeration Effect Using Flue Gases from Chimney</strong>. A study on increasing refrigeration effect using flue gases from a chimney. <a href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>.</p>
  </div>
</section>

<!-- Certifications -->
<section id="certifications" aria-label="Certifications">
  <div class="bg fallback"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,255,255,0.96), rgba(250,250,250,0.92));"></div>

  <div class="content card">
    <h3>Certifications</h3>
    <p class="lead">CATIA V5 · Ansys (FEA) · HyperWorks / OptiStruct · TCL scripting</p>
  </div>
</section>

<!-- Contact -->
<section id="contact" aria-label="Contact">
  <div class="bg" style="background:linear-gradient(180deg,#071219,#031018);"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(6,8,12,0.6), rgba(3,6,10,0.72));"></div>

  <div class="content" style="color:#eef6f8;">
    <h1 class="title" style="color:#eef6f8">Let's build something exceptional — Parlons</h1>
    <p class="lead" style="color:rgba(238,246,248,0.9)">Email: <a href="mailto:venkata.france@gmail.com" style="color:#fff">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#fff">+33 7 55 66 28 21</a></p>
    <div style="display:flex;gap:10px;margin-top:12px;">
      <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">LinkedIn</a>
      <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank">Instagram</a>
      <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
    </div>
    <div style="margin-top:18px;color:rgba(238,246,248,0.6)">© <span id="year"></span> Venkata Raghavendra KADIYALA</div>
  </div>
</section>

<!-- GSAP + ScrollTrigger CDN -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
/* GSAP ScrollTrigger animations:
   - Animate headings/content in when section comes into view
   - Parallax for background and float elements
   - Day→sunset→night color tween based on scroll progress
*/
gsap.registerPlugin(ScrollTrigger);

const sections = document.querySelectorAll('section');

// Animate each section's content in when visible
sections.forEach((sec, i) => {
  const content = sec.querySelector('.content');
  const floats = sec.querySelectorAll('.float');
  const bg = sec.querySelector('.bg');

  // entrance for content
  if(content){
    gsap.from(content, {
      scrollTrigger: {
        trigger: sec,
        start: "top 65%",
        end: "top 40%",
        toggleActions: "play none none reverse"
      },
      y: 28,
      autoAlpha: 0,
      duration: 0.9,
      ease: "power3.out"
    });
  }

  // float parallax (continuous small movement tied to scroll)
  floats.forEach((f, idx) => {
    gsap.to(f, {
      y: (idx % 2 === 0 ? -40 : 40),
      x: (idx % 2 === 0 ? 22 : -22),
      ease: "none",
      scrollTrigger: {
        trigger: sec,
        start: "top bottom",
        end: "bottom top",
        scrub: 1
      }
    });
  });

  // background parallax (subtle)
  if(bg){
    gsap.to(bg, {
      yPercent: 6,
      ease: "none",
      scrollTrigger: {
        trigger: sec,
        start: "top bottom",
        end: "bottom top",
        scrub: 0.6
      }
    });
  }
});

// Page-wide color shift (day -> sunset -> night) mapped across document
const pageHeight = document.body.scrollHeight - window.innerHeight;
ScrollTrigger.create({
  start: 0,
  end: () => pageHeight,
  onUpdate: self => {
    const p = self.progress;
    if(p < 0.35){
      // day
      gsap.to(document.documentElement, {duration:0.6, '--bg-day': '#ffffff', '--text-day': '#071622'});
    } else if(p < 0.75){
      // sunset
      gsap.to(document.documentElement, {duration:0.8, '--bg-day': '#fff7f3', '--text-day': '#071622'});
    } else {
      // night
      gsap.to(document.documentElement, {duration:1.0, '--bg-day': '#061018', '--text-day': '#eef6f8'});
    }
  }
});

// keyboard: page up/down and arrows
window.addEventListener('keydown', (e) => {
  if(e.key === 'PageDown' || e.key === 'ArrowDown') {
    ScrollTrigger.getAll().forEach(t => t.kill()); // avoid double triggers
    window.scrollBy({top: window.innerHeight, behavior: 'smooth'});
    setTimeout(() => location.reload(), 600); // reload to re-init ScrollTrigger states
  }
  if(e.key === 'PageUp' || e.key === 'ArrowUp') {
    ScrollTrigger.getAll().forEach(t => t.kill());
    window.scrollBy({top: -window.innerHeight, behavior: 'smooth'});
    setTimeout(() => location.reload(), 600);
  }
});

// set year
document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>
