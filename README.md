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
    --gold-btn:linear-gradient(45deg,#fdbb2d,#fcb045,#fd7e14);
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;background:var(--light-bg);color:#071622;overflow-x:hidden}
  a{text-decoration:none;color:inherit}
  section{min-height:100vh;width:100%;position:relative;display:flex;align-items:center;justify-content:center;padding:32px;overflow:hidden}
  .bg{position:absolute;inset:0;background-size:cover;background-position:center;filter:brightness(.9);z-index:0}
  .overlay{position:absolute;inset:0;z-index:1;pointer-events:none}
  .content{position:relative;z-index:6;max-width:1200px;width:100%;text-align:center;padding:28px}
  h1.title{font-weight:900;font-size:clamp(36px,8vw,96px);line-height:1;text-transform:uppercase;margin-bottom:10px}
  h2.subtitle{color:var(--muted);font-size:18px;font-weight:700;margin-bottom:14px}
  p.lead{color:var(--muted);line-height:1.7;max-width:980px;margin:auto}
  .light-text{color:#fff}
  .portrait{width:auto;height:60vh;max-height:760px;object-fit:contain;filter:drop-shadow(0 40px 90px rgba(6,12,20,.18));margin-bottom:20px}
  .float{position:absolute;z-index:5;pointer-events:none;width:46vw;max-width:760px;filter:drop-shadow(0 34px 90px rgba(3,9,16,0.55))}
  .topbar{position:fixed;right:18px;top:16px;z-index:99;display:flex;gap:10px}
  .btn{display:inline-flex;align-items:center;gap:8px;padding:10px 14px;border-radius:10px;font-weight:800;color:#fff;box-shadow:0 12px 30px rgba(2,8,10,0.12)}
  .btn.linkedin{background:var(--linkedin)}
  .btn.instagram{background:linear-gradient(45deg,#feda75,#fa7e1e,#d62976,#962fbf,#4f5bd5)}
  .btn.contact{background:linear-gradient(90deg,var(--accent-teal),#e6b66d);color:#052425}
  .btn.gold{background:var(--gold-btn)}
  .card{background:#fff;border-radius:12px;padding:32px;box-shadow:0 30px 80px rgba(8,12,18,0.06);color:#071622;text-align:left;max-width:1000px}
  #scroll-indicator{position:absolute;bottom:40px;left:50%;transform:translateX(-50%);font-size:24px;color:#071622;animation:bounce 1.5s infinite;z-index:10}
  @keyframes bounce{0%,100%{transform:translate(-50%,0)}50%{transform:translate(-50%,10px)}}
  footer{background:#031018;color:#dbe4e8;text-align:center;padding:16px;font-size:14px}
  @media(max-width:900px){.portrait{height:50vh}}
</style>
</head>
<body>
  <div class="topbar">
    <a class="btn linkedin" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank">LinkedIn</a>
    <a class="btn instagram" href="https://www.instagram.com/raghukadiyala/" target="_blank">Instagram</a>
    <a class="btn contact" href="mailto:venkata.france@gmail.com">Email</a>
  </div>

  <!-- HERO -->
  <section id="hero">
    <div class="bg" style="background-image:linear-gradient(180deg,#fff,#f3f6f8)"></div>
    <div class="overlay"></div>
    <div class="content">
      <img src="portrait.png" alt="Portrait" class="portrait" onerror="this.style.display='none'">
      <h1 class="title">VENKATA RAGHAVENDRA <span style="color:var(--accent-teal)">KADIYALA</span></h1>
      <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
      <p class="lead">☎ <a href="tel:+33755662821">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a></p>
    </div>
    <div id="scroll-indicator">▼</div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfd,#eef5f7)"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3>About — À propos</h3>
      <p class="lead"><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers, and ensure manufacturability with user-focused outcomes.</p>
      <p class="lead" style="margin-top:10px;"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>
      <div style="margin-top:14px;">
        <strong>Responsibilities & Project Management</strong>
        <ul style="line-height:1.7;color:var(--muted);margin-top:6px">
          <li>Project planning & scheduling</li>
          <li>Team leadership and coordination</li>
          <li>Budgeting, financing and cost control</li>
          <li>Procurement & supplier buying</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- EXPERIENCE SECTIONS (examples shown) -->
  <section id="osta">
    <div class="bg" style="background-image:url('ai_osta.jpg');filter:brightness(.8)"></div>
    <div class="overlay" style="background:rgba(0,0,0,0.45)"></div>
    <div class="content light-text">
      <h1 class="title">SEGULA — Project OSTA</h1>
      <p class="lead light-text">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
    </div>
  </section>

  <!-- Repeat other experience sections with similar structure ... -->

  <!-- EDUCATION -->
  <section id="education">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7)"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3>Education — Formation</h3>
      <p class="lead"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)<br>
      <strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <div class="bg" style="background-image:linear-gradient(180deg,#fbfbfb,#eef5f7)"></div>
    <div class="overlay"></div>
    <div class="content card">
      <h3>Skills & Tools — Compétences</h3>
      <ul style="line-height:1.7;color:var(--muted)">
        <li>CATIA V5, Ansys, HyperWorks / OptiStruct</li>
        <li>FEA, CAD Automation, PDM/DMA/SAM</li>
        <li>Project planning · Team management · Budget & procurement</li>
      </ul>
    </div>
  </section>

  <!-- PUBLICATION -->
  <section id="publication">
    <div class="bg" style="background-image:linear-gradient(180deg,#f9fafb,#eef3f6)"></div>
    <div class="overlay"></div>
    <div class="content card" style="text-align:left">
      <h3>Publication — Avril 2018</h3>
      <p class="lead">Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018. A study on increasing refrigeration effect using flue gases from a chimney.</p>
      <div style="margin-top:18px;">
        <a class="btn gold" href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="bg" style="background:linear-gradient(180deg,#071219,#031018)"></div>
    <div class="overlay"></div>
    <div class="content light-text">
      <h1 class="title light-text">Let's build something exceptional — Parlons</h1>
      <p class="lead light-text">Email: <a href="mailto:venkata.france@gmail.com" style="color:#fff">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#fff">+33 7 55 66 28 21</a></p>
    </div>
  </section>

  <footer>© Kadiyala Venkata Raghavendra</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
gsap.registerPlugin(ScrollTrigger);

// reveal animation per section
document.querySelectorAll('section').forEach(sec=>{
  const content=sec.querySelector('.content');
  if(content){
    gsap.from(content,{
      scrollTrigger:{trigger:sec,start:"top 80%",end:"top 50%",toggleActions:"play none none reverse"},
      y:40,autoAlpha:0,duration:.8,ease:"power3.out"
    });
  }
  const bg=sec.querySelector('.bg');
  if(bg){
    gsap.to(bg,{
      yPercent:6,ease:"none",
      scrollTrigger:{trigger:sec,start:"top bottom",end:"bottom top",scrub:0.8}
    });
  }
});
</script>
</body>
</html>
