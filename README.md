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
    --bg-light:#ffffff;
    --bg-dark:#061018;
  }
  *{box-sizing:border-box}
  html,body{height:100%;margin:0;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;background:var(--bg-light);color:#071622;-webkit-font-smoothing:antialiased;}
  a{color:inherit}
  /* stacked sections, normal flow */
  section{min-height:100vh; width:100%; display:flex; align-items:center; justify-content:center; padding:36px; position:relative;}
  .bg { position:absolute; inset:0; background-size:cover; background-position:center; z-index:0; filter:brightness(.9); }
  .overlay { position:absolute; inset:0; z-index:1; pointer-events:none; }
  .content { position:relative; z-index:6; width:100%; max-width:1200px; text-align:center; padding:24px; }
  h1.title{ margin:0; font-weight:900; font-size:clamp(36px,7.5vw,84px); line-height:0.92; text-transform:uppercase; }
  p.lead{ margin:14px 0 0; color:var(--muted); max-width:1000px; margin-left:auto;margin-right:auto; line-height:1.6; }
  .portrait{ width:auto; height:64vh; max-height:720px; object-fit:contain; filter:drop-shadow(0 40px 90px rgba(6,12,20,.18)); display:block; margin:0 auto; }
  .float{ position:absolute; z-index:5; pointer-events:none; width:46vw; max-width:760px; filter:drop-shadow(0 30px 60px rgba(3,9,16,.45)); }
  .topbar{ position:fixed; right:18px; top:14px; z-index:99; display:flex; gap:10px; }
  .btn{ display:inline-flex; align-items:center; gap:8px; padding:10px 12px; border-radius:10px; font-weight:800; color:white; text-decoration:none; }
  .btn.linkedin{ background:var(--linkedin) }
  .btn.instagram{ background:linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5) }
  .btn.contact{ background:linear-gradient(90deg,var(--accent-teal),#e6b66d); color:#052425 }
  /* card style for text sections */
  .card{ background:linear-gradient(180deg,#fff,#fbfbfb); padding:28px; border-radius:12px; box-shadow:0 30px 80px rgba(8,12,18,.06); color:#071622; text-align:left; }
  /* responsive */
  @media(max-width:900px){
    .float{ width:78vw; }
    .portrait{ height:48vh; }
  }
</style>
</head>
<body>
  <div class="topbar" role="navigation" aria-label="Social">
    <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
    <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
    <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
  </div>

  <!-- HERO -->
  <section id="hero" aria-label="Hero">
    <div class="bg" style="background-image:linear-gradient(180deg,#fff,#f3f6f8);"></div>
    <div class="overlay"></div>
    <div class="content">
      <!-- portrait.png optional; if missing you'll still see text -->
      <img src="portrait.png" alt="Portrait" class="portrait" id="portrait" loading="eager" onerror="this.style.display='none'">
      <h1 class="title">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
      <p class="lead">Mechanical Engineer • Creative Designer — Train interiors & systems<br>☎ <a href="tel:+33755662821">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a></p>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about" aria-label="About">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfd,#eef5f7);"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3 id="aboutTitle" style="margin-top:0;font-weight:900;">About — À propos</h3>
      <p class="lead"><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability and clear user-focused outcomes.</p>
      <p class="lead" style="margin-top:12px;"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>
    </div>
  </section>

  <!-- SEGULA OSTA -->
  <section id="osta" aria-label="SEGULA OSTA">
    <div class="bg" style="background-image:linear-gradient(180deg,#e9f2f7,#dfeaf0);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(4,10,14,0.48),rgba(2,6,10,0.62));"></div>
    <img src="float_osta.png" class="float" alt="" style="right:6%; top:14%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#fff">SEGULA — Project OSTA</h1>
      <p class="lead" style="color:#fff">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
    </div>
  </section>

  <!-- SEGULA BaWu -->
  <section id="bawu" aria-label="SEGULA BaWu">
    <div class="bg" style="background-image:linear-gradient(180deg,#eaf6f4,#dff3f1);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(6,12,12,0.48),rgba(4,8,8,0.62));"></div>
    <img src="float_bawu.png" class="float" alt="" style="left:8%; top:16%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#fff">SEGULA — BaWu</h1>
      <p class="lead" style="color:#fff">3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
    </div>
  </section>

  <!-- SEGULA RER NG -->
  <section id="rerng" aria-label="SEGULA RER NG">
    <div class="bg" style="background-image:linear-gradient(180deg,#f0f2f5,#e6eaee);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(5,8,12,0.5),rgba(3,6,10,0.66));"></div>
    <img src="float_rerng.png" class="float" alt="" style="right:10%; top:18%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#fff">SEGULA — RER NG</h1>
      <p class="lead" style="color:#fff">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
    </div>
  </section>

  <!-- SEGULA DSB -->
  <section id="dsb" aria-label="SEGULA DSB">
    <div class="bg" style="background-image:linear-gradient(180deg,#eef1f6,#e2e7ec);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(3,6,14,0.58),rgba(2,4,10,0.72));"></div>
    <img src="float_dsb.png" class="float" alt="" style="left:6%; top:12%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#fff">SEGULA — DSB</h1>
      <p class="lead" style="color:#fff">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
    </div>
  </section>

  <!-- SNCF -->
  <section id="sncf" aria-label="SNCF">
    <div class="bg" style="background-image:linear-gradient(180deg,#eef3f7,#e6ecf1);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(6,8,12,0.54),rgba(3,6,10,0.66));"></div>
    <img src="float_sncf.png" class="float" alt="" style="right:8%; top:10%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#fff">SNCF</h1>
      <p class="lead" style="color:#fff">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
    </div>
  </section>

  <!-- LAMIH -->
  <section id="lamih" aria-label="LAMIH">
    <div class="bg" style="background-image:linear-gradient(180deg,#f3eef6,#ece7f0);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(30,18,36,0.36),rgba(4,6,10,0.6));"></div>
    <img src="float_lamih.png" class="float" alt="" style="left:10%; top:14%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#fff">LAMIH</h1>
      <p class="lead" style="color:#fff">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
    </div>
  </section>

  <!-- PM DIMENSIONS -->
  <section id="pmdim" aria-label="PM DIMENSIONS">
    <div class="bg" style="background-image:linear-gradient(180deg,#fffaf2,#fff5ea);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(255,250,240,0.06),rgba(6,6,8,0.18));"></div>
    <img src="float_pmdimensions.png" class="float" alt="" style="right:8%; top:16%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#071622">PM DIMENSIONS</h1>
      <p class="lead" style="color:#071622">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
    </div>
  </section>

  <!-- INDIAN RAILWAYS -->
  <section id="indian" aria-label="Indian Railways">
    <div class="bg" style="background-image:linear-gradient(180deg,#fff7ef,#fff0e6);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(8,6,4,0.14),rgba(6,4,6,0.28));"></div>
    <img src="float_indianrail.png" class="float" alt="" style="left:6%; top:16%;" onerror="this.style.display='none'">
    <div class="content">
      <h1 class="title" style="color:#071622">Indian Railways (Intern)</h1>
      <p class="lead" style="color:#071622">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
    </div>
  </section>

  <!-- Education -->
  <section id="education" aria-label="Education">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7);"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3 style="margin-top:0;font-weight:900">Education — Formation</h3>
      <p class="lead"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)<br><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
      <p class="lead" style="margin-top:10px;">Selected project: <strong>Enhancement of Refrigeration Effect Using Flue Gases from Chimney</strong> — April 2018. <a href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read paper</a></p>
    </div>
  </section>

  <!-- Skills -->
  <section id="skills" aria-label="Skills">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7);"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3 style="margin-top:0;font-weight:900">Skills & Tools — Compétences</h3>
      <ul style="color:var(--muted); line-height:1.7;">
        <li>CATIA V5 — advanced surfacing & assembly management</li>
        <li>Ansys, HyperWorks / OptiStruct — FEA & meshing</li>
        <li>PDM / DMA / SAM workflows</li>
        <li>TCL scripting, basic C / Java</li>
      </ul>
    </div>
  </section>

  <!-- Publication -->
  <section id="publication" aria-label="Publication">
    <div class="bg" style="background-image:linear-gradient(180deg,#f9fafb,#eef3f6);"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3 style="margin-top:0;font-weight:900">Publication — Avril 2018</h3>
      <p class="lead">Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018. <a href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>.</p>
    </div>
  </section>

  <!-- Certifications -->
  <section id="certs" aria-label="Certifications">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7);"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3 style="margin-top:0;font-weight:900">Certifications</h3>
      <p class="lead">CATIA V5 · Ansys (FEA) · HyperWorks / OptiStruct · TCL scripting</p>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" aria-label="Contact">
    <div class="bg" style="background:linear-gradient(180deg,#071219,#031018);"></div>
    <div class="overlay" style="background:linear-gradient(180deg,rgba(4,6,10,0.6),rgba(2,4,8,0.7));"></div>
    <div class="content" style="color:#eef6f8;">
      <h1 class="title" style="color:#eef6f8">Let's build something exceptional — Parlons</h1>
      <p class="lead" style="color:rgba(238,246,248,0.9)">Email: <a href="mailto:venkata.france@gmail.com" style="color:#fff">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#fff">+33 7 55 66 28 21</a></p>
    </div>
  </section>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
/* Lightweight, robust ScrollTrigger animations. No toggling/hiding other sections. */
try {
  gsap.registerPlugin(ScrollTrigger);
  document.querySelectorAll('section').forEach((sec) => {
    const content = sec.querySelector('.content');
    const floatEl = sec.querySelector('.float');
    const bg = sec.querySelector('.bg');

    if(content){
      gsap.from(content, {
        scrollTrigger: {
          trigger: sec,
          start: 'top 70%',
          end: 'top 40%',
          toggleActions: 'play none none reverse'
        },
        y: 30,
        autoAlpha: 0,
        duration: 0.9,
        ease: 'power3.out'
      });
    }

    if(floatEl){
      gsap.to(floatEl, {
        y: -40,
        x: 20,
        ease: 'sine.inOut',
        scrollTrigger: {
          trigger: sec,
          start: 'top bottom',
          end: 'bottom top',
          scrub: 1
        }
      });
    }

    if(bg){
      gsap.to(bg, {
        yPercent: 6,
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

  // Page color transition (simple)
  const allSections = document.querySelectorAll('section');
  const total = allSections.length;
  ScrollTrigger.create({
    start: 0,
    end: () => document.body.scrollHeight - window.innerHeight,
    onUpdate: (self) => {
      const p = self.progress;
      if(p < 0.35){
        gsap.to(document.documentElement, {duration:0.6, '--bg-light': '#ffffff'});
      } else if(p < 0.75){
        gsap.to(document.documentElement, {duration:0.8, '--bg-light': '#fff7f3'});
      } else {
        gsap.to(document.documentElement, {duration:1.0, '--bg-light': '#061018'});
      }
    }
  });
} catch (err) {
  // If GSAP fails, log for debugging but keep page usable
  console.error('Animation init error:', err);
}
</script>
</body>
</html>
