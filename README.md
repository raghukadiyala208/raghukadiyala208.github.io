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
    --linkedin:#0077b5;
    --muted:#6b7780;
    --light-bg:#ffffff;
    --dark-bg:#061018;
    --card-bg: #ffffff;
    --card-shadow: rgba(8,12,18,0.06);
    --glass-dark: rgba(2,6,10,0.56);
    font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;background:var(--light-bg);color:#071622;-webkit-font-smoothing:antialiased;}
  a{color:inherit}
  /* Sections stacked normally */
  section{min-height:100vh; width:100%; position:relative; display:flex; align-items:center; justify-content:center; padding:32px; overflow:hidden;}
  .bg{ position:absolute; inset:0; background-size:cover; background-position:center; z-index:0; filter:brightness(.88); }
  .overlay{ position:absolute; inset:0; z-index:1; pointer-events:none; }
  .content{ position:relative; z-index:6; width:100%; max-width:1200px; padding:28px; display:flex; flex-direction:column; gap:12px; align-items:center; justify-content:center; text-align:center; }
  /* Text color helpers */
  .light-text { color:#ffffff; }
  .dark-text { color:#071622; }
  /* Big hero title */
  h1.title{ margin:0; font-weight:900; font-size:clamp(36px,8.5vw,96px); line-height:0.92; text-transform:uppercase; }
  h2.subtitle{ margin:0; font-weight:700; color:var(--muted); font-size:18px; }
  p.lead{ margin:0; color:var(--muted); max-width:980px; line-height:1.7; }
  /* portrait */
  .portrait{ width:auto; height:62vh; max-height:760px; object-fit:contain; filter:drop-shadow(0 40px 90px rgba(6,12,20,.18)); display:block; margin:0 auto; }
  /* floating overlay */
  .float{ position:absolute; z-index:5; pointer-events:none; width:46vw; max-width:760px; filter:drop-shadow(0 34px 90px rgba(3,9,16,0.55)); }
  /* topbar */
  .topbar{ position:fixed; right:18px; top:16px; z-index:99; display:flex; gap:10px; align-items:center; }
  .btn{ display:inline-flex; align-items:center; gap:8px; padding:10px 14px; border-radius:10px; font-weight:800; color:#fff; text-decoration:none; box-shadow:0 12px 30px rgba(2,8,10,0.12); }
  .btn.linkedin{ background:var(--linkedin) }
  .btn.instagram{ background:linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5) }
  .btn.contact{ background:linear-gradient(90deg,var(--accent-teal),#e6b66d); color:#052425 }
  /* cards */
  .card{ background:var(--card-bg); padding:28px; border-radius:12px; box-shadow:0 30px 80px var(--card-shadow); color:var(--dark-text); max-width:1000px; text-align:left; }
  .card h3{ margin:0 0 8px 0; }
  .list{ text-align:left; color:var(--muted); line-height:1.7; margin:8px 0 0 0; padding-left:18px; }
  /* responsive */
  @media (max-width:980px){
    .float{ width:78vw; }
    .portrait{ height:50vh; }
    h1.title{ font-size:clamp(32px,12vw,56px); }
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

<!-- HERO (light background, dark text) -->
<section id="hero" aria-label="Hero" class="section-hero">
  <div class="bg" style="background-image:linear-gradient(180deg,#fff,#f3f6f8);"></div>
  <div class="overlay"></div>

  <div class="content dark-text">
    <img src="portrait.png" alt="Portrait" class="portrait" id="portrait" loading="eager" onerror="this.style.display='none'">
    <h1 class="title">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
    <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
    <p class="lead">☎ <a href="tel:+33755662821">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a></p>
  </div>
</section>

<!-- ABOUT (light card, dark text) -->
<section id="about" aria-label="About">
  <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfd,#eef5f7);"></div>
  <div class="overlay"></div>

  <div class="content card">
    <h3 id="aboutTitle">About — À propos</h3>
    <p class="lead"><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability and clear user-focused outcomes.</p>
    <p class="lead" style="margin-top:10px;"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>

    <!-- Added business / management responsibilities -->
    <div style="margin-top:14px;">
      <strong>Responsibilities & Project Management</strong>
      <ul class="list">
        <li>Project planning & scheduling</li>
        <li>Team leadership and coordination (multi-discipline)</li>
        <li>Budgeting, financing overview and cost control</li>
        <li>Procurement / purchasing (supplier selection & buying)</li>
      </ul>
    </div>
  </div>
</section>

<!-- EXPERIENCE PANELS - each with clear overlay & readable text -->

<!-- SEGULA — OSTA (dark mood; white text) -->
<section id="osta" aria-label="SEGULA OSTA">
  <div class="bg" style="background-image:url('ai_osta.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(4,10,14,0.60), rgba(2,6,10,0.72));"></div>

  <img src="float_osta.png" class="float" alt="" style="right:6%; top:14%;" onerror="this.style.display='none'">
  <div class="content light-text">
    <h1 class="title">SEGULA — Project OSTA</h1>
    <h2 class="subtitle light-text">Front office · Train interior systems · M0 → M5</h2>
    <p class="lead light-text">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
  </div>
</section>

<!-- SEGULA — BaWu (dark mood; white text) -->
<section id="bawu" aria-label="SEGULA BaWu">
  <div class="bg" style="background-image:url('ai_bawu.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(6,12,12,0.56), rgba(4,8,8,0.72));"></div>

  <img src="float_bawu.png" class="float" alt="" style="left:8%; top:16%;" onerror="this.style.display='none'">
  <div class="content light-text">
    <h1 class="title">SEGULA — BaWu</h1>
    <h2 class="subtitle light-text">Validation & QA · Integration focus</h2>
    <p class="lead light-text">3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
  </div>
</section>

<!-- SEGULA — RER NG (dark mood; white text) -->
<section id="rerng" aria-label="SEGULA RER NG">
  <div class="bg" style="background-image:url('ai_rerng.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(5,8,12,0.56), rgba(3,6,10,0.72));"></div>

  <img src="float_rerng.png" class="float" alt="" style="right:10%; top:18%;" onerror="this.style.display='none'">
  <div class="content light-text">
    <h1 class="title">SEGULA — RER NG</h1>
    <h2 class="subtitle light-text">Change request engineering & on-site surveys</h2>
    <p class="lead light-text">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
  </div>
</section>

<!-- SEGULA — DSB (dark mood; white text) -->
<section id="dsb" aria-label="SEGULA DSB">
  <div class="bg" style="background-image:url('ai_dsb.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(3,6,14,0.66), rgba(2,4,10,0.82));"></div>

  <img src="float_dsb.png" class="float" alt="" style="left:6%; top:12%;" onerror="this.style.display='none'">
  <div class="content light-text">
    <h1 class="title">SEGULA — DSB</h1>
    <h2 class="subtitle light-text">Interior layout & integration</h2>
    <p class="lead light-text">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
  </div>
</section>

<!-- SNCF (dark mood; white text) -->
<section id="sncf" aria-label="SNCF">
  <div class="bg" style="background-image:url('ai_sncf.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(6,8,12,0.60), rgba(3,6,10,0.76));"></div>

  <img src="float_sncf.png" class="float" alt="" style="right:8%; top:10%;" onerror="this.style.display='none'">
  <div class="content light-text">
    <h1 class="title">SNCF</h1>
    <h2 class="subtitle light-text">FEA & Automation · HyperWorks / OptiStruct</h2>
    <p class="lead light-text">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
  </div>
</section>

<!-- LAMIH (darker purple dusk; white text) -->
<section id="lamih" aria-label="LAMIH">
  <div class="bg" style="background-image:url('ai_lamih.jpg');"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(30,18,36,0.44), rgba(4,6,10,0.7));"></div>

  <img src="float_lamih.png" class="float" alt="" style="left:10%; top:14%;" onerror="this.style.display='none'">
  <div class="content light-text">
    <h1 class="title">LAMIH</h1>
    <h2 class="subtitle light-text">Behavioural analysis & safety concepts</h2>
    <p class="lead light-text">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
  </div>
</section>

<!-- PM DIMENSIONS (light card) -->
<section id="pmdim" aria-label="PM DIMENSIONS">
  <div class="bg" style="background-image:url('ai_pmdimensions.jpg'); filter:brightness(.96);"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,250,240,0.06), rgba(6,6,8,0.12));"></div>

  <img src="float_pmdimensions.png" class="float" alt="" style="right:8%; top:16%;" onerror="this.style.display='none'">
  <div class="content dark-text">
    <h1 class="title" style="color:#071622">PM DIMENSIONS</h1>
    <h2 class="subtitle" style="color:var(--muted)">Part design & prototyping</h2>
    <p class="lead" style="color:var(--muted)">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
  </div>
</section>

<!-- Indian Railways (light) -->
<section id="indian" aria-label="Indian Railways">
  <div class="bg" style="background-image:url('ai_indianrail.jpg'); filter:brightness(.96);"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(255,250,244,0.04), rgba(6,6,8,0.12));"></div>

  <img src="float_indianrail.png" class="float" alt="" style="left:6%; top:16%;" onerror="this.style.display='none'">
  <div class="content dark-text">
    <h1 class="title" style="color:#071622">Indian Railways (Intern)</h1>
    <h2 class="subtitle" style="color:var(--muted)">Prototype coupling & maintenance optimisation</h2>
    <p class="lead" style="color:var(--muted)">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
  </div>
</section>

<!-- EDUCATION (remove the incorrect selected project line) -->
<section id="education" aria-label="Education">
  <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7);"></div>
  <div class="overlay"></div>

  <div class="content card">
    <h3 style="margin-top:0;font-weight:900">Education — Formation</h3>
    <p class="lead"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)<br>
    <strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
  </div>
</section>

<!-- SKILLS & BUSINESS (includes planning, team mgmt, financing, buying) -->
<section id="skills" aria-label="Skills">
  <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7);"></div>
  <div class="overlay"></div>

  <div class="content card">
    <h3 style="margin:0 0 8px 0;font-weight:900">Skills & Tools — Compétences</h3>
    <div style="display:flex;gap:10px;flex-wrap:wrap;margin-top:8px;">
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,.06)"><strong>CATIA V5</strong></div>
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,.06)"><strong>Ansys</strong></div>
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,.06)"><strong>HyperWorks / OptiStruct</strong></div>
      <div style="background:#fff;padding:10px 14px;border-radius:8px;box-shadow:0 10px 30px rgba(8,12,18,.06)"><strong>PDM / DMA / SAM</strong></div>
    </div>

    <div style="margin-top:16px;">
      <strong>Domain & Processes</strong>
      <ul class="list">
        <li>Train interiors & vehicle part design (integration & packaging)</li>
        <li>FEA: meshing, static & dynamic analysis</li>
        <li>CAD automation & scripting (TCL, basics C/Java)</li>
      </ul>
    </div>

    <div style="margin-top:12px;">
      <strong>Management & Business</strong>
      <ul class="list">
        <li>Project planning & scheduling</li>
        <li>Team leadership & multidisciplinary coordination</li>
        <li>Budgeting, financing oversight and cost control</li>
        <li>Procurement & supplier buying (technical specification, negotiation)</li>
      </ul>
    </div>
  </div>
</section>

<!-- PUBLICATION (with direct link placed below) -->
<section id="publication" aria-label="Publication">
  <div class="bg" style="background-image:linear-gradient(180deg,#f9fafb,#eef3f6);"></div>
  <div class="overlay"></div>

  <div class="content card" style="text-align:left;">
    <h3 style="margin-top:0;font-weight:900">Publication — Avril 2018</h3>
    <p class="lead">Enhancement of Refrigeration Effect Using Flue Gases from Chimney — a study on increasing refrigeration effect using flue gases from a chimney.</p>
    <p style="margin-top:12px;"><strong>Read the paper (IAEME):</strong><br>
      <a href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf</a>
    </p>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications" aria-label="Certifications">
  <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7);"></div>
  <div class="overlay"></div>

  <div class="content card">
    <h3 style="margin:0 0 8px 0;font-weight:900">Certifications</h3>
    <p class="lead">CATIA V5 · Ansys (FEA) · HyperWorks / OptiStruct · TCL scripting</p>
  </div>
</section>

<!-- CONTACT -->
<section id="contact" aria-label="Contact">
  <div class="bg" style="background:linear-gradient(180deg,#071219,#031018);"></div>
  <div class="overlay" style="background:linear-gradient(180deg, rgba(4,6,10,0.6), rgba(2,4,8,0.72));"></div>

  <div class="content light-text">
    <h1 class="title light-text">Let's build something exceptional — Parlons</h1>
    <p class="lead light-text">Email: <a href="mailto:venkata.france@gmail.com" style="color:#fff">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#fff">+33 7 55 66 28 21</a></p>
  </div>
</section>

<!-- GSAP + ScrollTrigger (animations) -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
try {
  gsap.registerPlugin(ScrollTrigger);

  document.querySelectorAll('section').forEach((sec) => {
    const content = sec.querySelector('.content');
    const floats = sec.querySelectorAll('.float');
    const bg = sec.querySelector('.bg');

    if(content){
      gsap.from(content, {
        scrollTrigger: {
          trigger: sec,
          start: 'top 72%',
          end: 'top 45%',
          toggleActions: 'play none none reverse'
        },
        y: 28, autoAlpha:0, duration:0.9, ease:'power3.out'
      });
    }

    floats.forEach((f, idx) => {
      gsap.to(f, {
        y: (idx % 2 === 0 ? -36 : 36),
        x: (idx % 2 === 0 ? 20 : -20),
        ease: 'sine.inOut',
        scrollTrigger: {
          trigger: sec,
          start: 'top bottom',
          end: 'bottom top',
          scrub: 1
        }
      });
    });

    if(bg){
      gsap.to(bg, {
        yPercent: 5,
        ease: 'none',
        scrollTrigger: {
          trigger: sec,
          start: 'top bottom',
          end: 'bottom top',
          scrub: 0.6
        }
      });
    }
  });

  // Optional: page-wide color tweak as you scroll (subtle)
  const pageEnd = () => document.body.scrollHeight - window.innerHeight;
  ScrollTrigger.create({
    start: 0,
    end: pageEnd,
    onUpdate: self => {
      const p = self.progress;
      if(p < 0.35){
        gsap.to(document.documentElement, {duration:0.6, '--light-bg':'#ffffff'});
      } else if(p < 0.75){
        gsap.to(document.documentElement, {duration:0.8, '--light-bg':'#fff7f3'});
      } else {
        gsap.to(document.documentElement, {duration:1, '--light-bg':'#061018'});
      }
    }
  });

} catch (e) {
  console.error('GSAP init error:', e);
}
</script>
</body>
</html>
