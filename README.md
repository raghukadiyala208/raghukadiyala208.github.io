<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --accent-teal: #17c3a2;
    --gold-grad: linear-gradient(45deg,#fdbb2d,#fcb045,#fd7e14);
    --muted: #98a6b0;
    --bg-top: #0b2a3f; /* steel-blue */
    --bg-bottom: #031018; /* midnight */
    --card-glass: rgba(255,255,255,0.04);
    --content-width: 1200px;
    --snap-gap: 0px;
    font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial;
  }

  *{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));color:#eef6f8; -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale; overflow:auto; scroll-behavior:smooth;}
  a{text-decoration:none; color:inherit}
  /* Layout with snap */
  main{height:100vh; width:100vw; overflow-y:auto; scroll-snap-type:y mandatory; -webkit-overflow-scrolling:touch;}
  section{min-height:100vh; height:100vh; width:100%; position:relative; display:flex; align-items:center; justify-content:center; padding:40px; scroll-snap-align:start;}
  /* unified backdrop fill — each section will have the same cinematic gradient base */
  .backdrop{position:absolute;inset:0; background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom)); z-index:0; pointer-events:none;}
  .overlay{position:absolute;inset:0; z-index:1; pointer-events:none; background:linear-gradient(180deg, rgba(2,8,12,0.12), rgba(0,0,0,0.5));}
  .content{position:relative; z-index:6; width:100%; max-width:var(--content-width); text-align:center; padding:28px; display:flex; flex-direction:column; gap:12px; align-items:center; justify-content:center;}
  h1.title{font-weight:900; font-size:clamp(34px,7.8vw,84px); line-height:0.92; text-transform:uppercase; letter-spacing:-1px;}
  h2.subtitle{font-weight:700; color:var(--muted); font-size:18px}
  p.lead{color:var(--muted); max-width:980px; line-height:1.6; font-size:16px}
  /* portrait floating no frame */
  .portrait{height:62vh; max-height:780px; object-fit:contain; filter:drop-shadow(0 48px 120px rgba(0,0,0,0.6));}
  /* floating foreground images */
  .float{position:absolute; z-index:5; pointer-events:none; width:46vw; max-width:760px; filter:drop-shadow(0 40px 110px rgba(0,0,0,0.65));}
  /* topbar */
  .topbar{position:fixed; top:16px; right:18px; z-index:90; display:flex; gap:10px; align-items:center;}
  .btn{display:inline-flex; gap:8px; align-items:center; padding:10px 14px; border-radius:12px; font-weight:800; color:white; box-shadow:0 12px 36px rgba(0,0,0,0.35); border:none; cursor:pointer;}
  .btn.linkedin{background:#0077b5}
  .btn.instagram{background:linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5)}
  .btn.email{background:linear-gradient(90deg,var(--accent-teal),#e6b66d); color:#052425}
  .btn.read{background:var(--gold-grad); color:#052425}
  /* card variant for text blocks inside content when needed (kept subtle) */
  .card{background:var(--card-glass); border-radius:12px; padding:28px; box-shadow:0 40px 100px rgba(0,0,0,0.45); width:100%; max-width:1000px; text-align:left; color:#e7eef2;}
  .card h3{margin:0 0 8px 0; color:#fff}
  .card p, .card li{color:var(--muted)}
  /* scroll indicator */
  #scroll-indicator{position:absolute; bottom:28px; left:50%; transform:translateX(-50%); z-index:12; color:#dfe9ee; font-size:22px; opacity:0.9; animation:scroll-bob 1.6s infinite;}
  @keyframes scroll-bob{0%{transform:translate(-50%,0)}50%{transform:translate(-50%,10px)}100%{transform:translate(-50%,0)}}
  footer{padding:18px; color:#cfe3e9; text-align:center; background:linear-gradient(180deg,transparent,rgba(0,0,0,0.2)); font-size:14px}
  /* responsive */
  @media(max-width:980px){ .float{width:78vw} .portrait{height:50vh} h1.title{font-size:34px} .card{text-align:left} .content{padding:18px} }
</style>
</head>
<body>
  <!-- topbar with social -->
  <div class="topbar" aria-label="Social and contact">
    <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
    <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
    <a class="btn email" href="mailto:venkata.france@gmail.com">Email</a>
  </div>

  <main id="site-main" aria-live="polite">
    <!-- HERO -->
    <section id="hero" aria-label="Hero — Venkata Raghavendra Kadiyala">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content">
        <!-- portrait.png optional -->
        <img src="portrait.png" alt="Portrait of Venkata Raghavendra Kadiyala" class="portrait" onerror="this.style.display='none'">
        <h1 class="title">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
        <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
        <p class="lead">☎ <a href="tel:+33755662821" style="color:#e7f7f1">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com" style="color:#e7f7f1">venkata.france@gmail.com</a></p>
      </div>
      <div id="scroll-indicator" aria-hidden="true">▼</div>
    </section>

    <!-- ABOUT: same cinematic backdrop -->
    <section id="about" aria-label="About">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content card" role="article" aria-labelledby="aboutTitle">
        <h3 id="aboutTitle">About — À propos</h3>
        <p style="margin-top:6px; color:#e9f3f6;"><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability with user-focused outcomes.</p>
        <p style="margin-top:10px; color:#e9f3f6;"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>

        <div style="margin-top:14px; color:#e9f3f6;">
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

    <!-- Experience sections: each fills full screen and uses the same cinematic backdrop.
         Use distinct background images if you have them (ai_*.jpg). Floating images optional. -->

    <section id="osta" aria-label="SEGULA — OSTA">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#083047,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.6));"></div>

      <img class="float" src="float_osta.png" alt="" style="right:6%; top:12%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — Project OSTA</h1>
        <p class="lead" style="color:#dfeef3">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
      </div>
    </section>

    <section id="bawu" aria-label="SEGULA — BaWu">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#0a374a,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_bawu.png" alt="" style="left:8%; top:14%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — BaWu</h1>
        <p class="lead" style="color:#dfeef3">3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
      </div>
    </section>

    <section id="rerng" aria-label="SEGULA — RER NG">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#0b3345,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_rerng.png" alt="" style="right:10%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — RER NG</h1>
        <p class="lead" style="color:#dfeef3">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
      </div>
    </section>

    <section id="dsb" aria-label="SEGULA — DSB">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#092f3f,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_dsb.png" alt="" style="left:6%; top:12%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — DSB</h1>
        <p class="lead" style="color:#dfeef3">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
      </div>
    </section>

    <section id="sncf" aria-label="SNCF">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#0b2735,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_sncf.png" alt="" style="right:8%; top:10%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SNCF</h1>
        <p class="lead" style="color:#dfeef3">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
      </div>
    </section>

    <section id="lamih" aria-label="LAMIH">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#271a2a,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_lamih.png" alt="" style="left:10%; top:14%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">LAMIH</h1>
        <p class="lead" style="color:#dfeef3">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
      </div>
    </section>

    <section id="pmdim" aria-label="PM DIMENSIONS">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#2a2a26,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_pmdimensions.png" alt="" style="right:8%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title" style="color:#dfeef3">PM DIMENSIONS</h1>
        <p class="lead" style="color:#dfeef3">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
      </div>
    </section>

    <section id="indian" aria-label="Indian Railways">
      <div class="backdrop" style="background-image:linear-gradient(180deg,#3a2b1b,#031018);"></div>
      <div class="overlay" style="background:linear-gradient(180deg, rgba(0,0,0,0.36), rgba(0,0,0,0.62));"></div>

      <img class="float" src="float_indianrail.png" alt="" style="left:6%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title" style="color:#dfeef3">Indian Railways (Intern)</h1>
        <p class="lead" style="color:#dfeef3">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
      </div>
    </section>

    <!-- Education (clean, same cinematic backdrop) -->
    <section id="education" aria-label="Education">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content card">
        <h3>Education — Formation</h3>
        <p style="color:var(--muted); margin-top:6px;"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)</p>
        <p style="color:var(--muted); margin-top:6px;"><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
      </div>
    </section>

    <!-- Skills (same cinematic backdrop) -->
    <section id="skills" aria-label="Skills">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content card">
        <h3>Skills & Tools — Compétences</h3>
        <ul style="margin-top:8px; color:var(--muted); line-height:1.6">
          <li>CATIA V5, Ansys, HyperWorks / OptiStruct</li>
          <li>FEA, CAD Automation, PDM/DMA/SAM</li>
          <li>Project planning · Team leadership · Budgeting & procurement</li>
        </ul>
      </div>
    </section>

    <!-- Publication: gold-orange button opens IAEME in new tab -->
    <section id="publication" aria-label="Publication">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content card" style="text-align:left;">
        <h3>Publication — Avril 2018</h3>
        <p style="margin-top:8px; color:var(--muted)">Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018.</p>
        <div style="margin-top:18px;">
          <a class="btn read" href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" aria-label="Contact">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content">
        <h1 class="title">Let's build something exceptional — Parlons</h1>
        <p class="lead" style="color:#dfeef3">Email: <a href="mailto:venkata.france@gmail.com" style="color:#dfeef3">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#dfeef3">+33 7 55 66 28 21</a></p>
      </div>
    </section>
  </main>

  <footer>© Kadiyala Venkata Raghavendra</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
/* GSAP + ScrollTrigger for reveal and subtle parallax.
   Sections use CSS scroll-snap to ensure single-section view.
*/
try {
  gsap.registerPlugin(ScrollTrigger);
  const secs = document.querySelectorAll('main section');

  secs.forEach((sec)=>{
    const content = sec.querySelector('.content');
    const floatEl = sec.querySelector('.float');
    const bg = sec.querySelector('.backdrop');

    if(content){
      gsap.fromTo(content, {y:40, autoAlpha:0}, {
        y:0, autoAlpha:1, duration:0.9, ease:'power3.out',
        scrollTrigger: { trigger: sec, start: 'top 70%', toggleActions: 'play none none reverse' }
      });
    }
    if(floatEl){
      gsap.to(floatEl, {
        y: (Math.random() > 0.5 ? -36 : 36),
        x: (Math.random() > 0.5 ? 20 : -20),
        ease: 'sine.inOut',
        scrollTrigger: { trigger: sec, start: 'top bottom', end: 'bottom top', scrub: 1 }
      });
    }
    if(bg){
      gsap.to(bg, {
        yPercent: 6,
        ease: 'none',
        scrollTrigger: { trigger: sec, start: 'top bottom', end: 'bottom top', scrub: 0.6 }
      });
    }
  });

  // optional: hide scroll indicator after first scroll
  const scInd = document.getElementById('scroll-indicator');
  if(scInd){
    ScrollTrigger.create({
      start: 10,
      onEnter: ()=> gsap.to(scInd, {autoAlpha:0, duration:0.5})
    });
  }
} catch(e){
  console.error('GSAP init failed', e);
}
</script>
</body>
</html>
