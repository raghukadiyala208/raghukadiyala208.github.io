<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --teal-grad: linear-gradient(90deg,#14b6a0,#0da58f);
    --muted:#58636b;
    --bg-top:#ffffff;
    --bg-bottom:#f5f6f8;
    --glass: rgba(255,255,255,0.6);
    --content-width:1200px;
  }

  /* Reset */
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%;width:100%;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));color:#0b1a1f;-webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;overflow:hidden}
  a{color:inherit;text-decoration:none}

  /* main free vertical scroll container */
  main{height:100vh;width:100vw;overflow-y:auto;overflow-x:hidden; -webkit-overflow-scrolling:touch; scroll-behavior:smooth;}
  /* hide native scrollbars while keeping scroll functional */
  main::-webkit-scrollbar{display:none}
  html { scrollbar-width: none; -ms-overflow-style: none; }

  /* section full viewport */
  section{min-height:100vh;height:100vh;width:100%;position:relative;display:flex;align-items:center;justify-content:center;padding:36px}
  .backdrop{position:absolute;inset:0;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));z-index:0}
  .overlay{position:absolute;inset:0;z-index:1;pointer-events:none;background:linear-gradient(180deg, rgba(11,26,31,0.03), rgba(6,12,14,0.06));}
  .content{position:relative;z-index:6;max-width:var(--content-width);width:100%;padding:24px;text-align:center;display:flex;flex-direction:column;gap:12px;align-items:center;justify-content:center}
  h1.title{font-weight:900;font-size:clamp(32px,7.2vw,72px);line-height:1;text-transform:uppercase}
  h2.subtitle{font-weight:700;color:var(--muted);font-size:17px}
  p.lead{color:var(--muted);max-width:980px;line-height:1.6;font-size:16px}
  .portrait{height:56vh;max-height:740px;object-fit:contain;border-radius:10px;box-shadow:0 30px 80px rgba(6,12,16,0.06)}
  .float{position:absolute;z-index:5;pointer-events:none;width:46vw;max-width:760px;opacity:0.95;filter:drop-shadow(0 30px 70px rgba(6,12,16,0.06))}
  /* top-right blur hamburger always visible */
  .hamburger{position:fixed;right:18px;top:14px;z-index:140;display:flex;align-items:center;gap:10px}
  .hambutton{width:50px;height:44px;border-radius:10px;background:rgba(255,255,255,0.6);backdrop-filter:blur(8px);display:flex;align-items:center;justify-content:center;border:1px solid rgba(12,20,24,0.06);cursor:pointer;color:#0b1a1f;box-shadow:0 8px 30px rgba(6,12,16,0.06)}
  .menu{position:fixed;right:18px;top:70px;z-index:139;min-width:220px;border-radius:12px;background:rgba(255,255,255,0.6);backdrop-filter:blur(8px);box-shadow:0 20px 60px rgba(6,12,16,0.06);overflow:hidden;opacity:0;visibility:hidden;transform-origin:top right;transition:all .22s ease}
  .menu.open{opacity:1;visibility:visible;transform:translateY(0)}
  .menu a{display:flex;align-items:center;justify-content:space-between;padding:12px 16px;color:#0b1a1f;border-bottom:1px solid rgba(6,12,16,0.03);font-weight:700}
  .menu a:last-child{border-bottom:0}
  .menu a:hover{background:rgba(6,12,16,0.03)}
  /* teal button style */
  .btn{display:inline-flex;align-items:center;gap:10px;padding:12px 18px;border-radius:12px;font-weight:800;color:white;background:var(--teal-grad);box-shadow:0 14px 40px rgba(13,77,64,0.12);cursor:pointer}
  .social-row{display:flex;gap:12px;align-items:center;justify-content:center;margin-top:8px}
  .social-link{padding:8px 12px;border-radius:10px;background:rgba(12,20,24,0.03);font-weight:700;color:#0b1a1f}
  .card{background:rgba(255,255,255,0.9);border-radius:12px;padding:26px;box-shadow:0 30px 60px rgba(6,12,16,0.04);max-width:1000px;text-align:left;color:#0b1a1f}
  .card h3{margin:0 0 8px 0}
  .card p,.card li{color:var(--muted)}
  #scroll-indicator{position:absolute;bottom:22px;left:50%;transform:translateX(-50%);z-index:11;color:var(--muted);font-size:20px;animation:scroll-bob 1.6s infinite}
  @keyframes scroll-bob{0%{transform:translate(-50%,0)}50%{transform:translate(-50%,10px)}100%{transform:translate(-50%,0)}}
  footer{padding:16px;text-align:center;color:var(--muted);background:linear-gradient(180deg,transparent,rgba(0,0,0,0.02))}
  @media(max-width:980px){.float{width:78vw}.portrait{height:48vh}.menu{right:10px;min-width:calc(100% - 20px)}}
</style>
</head>
<body>

  <!-- hamburger (always visible) -->
  <div class="hamburger" aria-hidden="false">
    <div class="hambutton" id="hambutton" role="button" aria-label="Open menu" aria-expanded="false" tabindex="0">☰</div>
    <nav class="menu" id="menu" aria-label="Main menu" role="navigation">
      <a href="#about" data-target="about">About Me <span>▸</span></a>
      <a href="#experiences" data-target="experiences">Experiences <span>▸</span></a>
      <a href="#publication" data-target="publication">Publication <span>▸</span></a>
      <a href="#skills" data-target="skills">Skills <span>▸</span></a>
      <a href="#contact" data-target="contact">Contact <span>▸</span></a>
    </nav>
  </div>

  <main id="site-main" aria-live="polite">

    <!-- HERO -->
    <section id="hero" aria-label="Hero">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content" role="region" aria-labelledby="heroTitle">
        <img src="portrait.png" alt="Portrait of Venkata" class="portrait" onerror="this.style.display='none'">
        <h1 class="title" id="heroTitle">VENKATA RAGHAVENDRA <span style="color:#0aa589">KADIYALA</span></h1>
        <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
        <p class="lead">☎ <a href="tel:+33755662821" style="color:#0b1a1f">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com" style="color:#0b1a1f">venkata.france@gmail.com</a></p>

        <div class="social-row" aria-hidden="false">
          <a class="social-link" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
          <a class="social-link" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
        </div>
      </div>

      <div id="scroll-indicator" aria-hidden="true">▼</div>
    </section>

    <!-- ABOUT -->
    <section id="about" aria-label="About">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card" role="article" aria-labelledby="aboutTitle">
        <h3 id="aboutTitle">About — À propos</h3>
        <p><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability with user-focused outcomes.</p>
        <p style="margin-top:10px;"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>

        <div style="margin-top:14px;">
          <strong>Responsibilities & Project Management</strong>
          <ul style="margin-top:8px; color:var(--muted); line-height:1.6;">
            <li>Project planning & scheduling</li>
            <li>Team leadership & coordination</li>
            <li>Budgeting, financing oversight & cost control</li>
            <li>Procurement & supplier buying</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- EXPERIENCES anchor -->
    <section id="experiences" aria-label="Experiences">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>
      <div class="content card" role="region" aria-labelledby="expTitle" style="text-align:left">
        <h3 id="expTitle">Experiences</h3>
        <p style="color:var(--muted); margin-top:8px">Scroll down — each experience occupies one full screen in sequence.</p>
      </div>
    </section>

    <!-- OSTA -->
    <section id="osta" aria-label="SEGULA OSTA">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_osta.png" alt="" style="right:6%; top:14%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — Project OSTA</h1>
        <p class="lead">Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
      </div>
    </section>

    <!-- BaWu -->
    <section id="bawu" aria-label="SEGULA BaWu">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_bawu.png" alt="" style="left:8%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — BaWu</h1>
        <p class="lead">3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
      </div>
    </section>

    <!-- RER NG -->
    <section id="rerng" aria-label="SEGULA RER NG">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_rerng.png" alt="" style="right:10%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — RER NG</h1>
        <p class="lead">Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
      </div>
    </section>

    <!-- DSB -->
    <section id="dsb" aria-label="SEGULA DSB">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_dsb.png" alt="" style="left:6%; top:12%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SEGULA — DSB</h1>
        <p class="lead">Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
      </div>
    </section>

    <!-- SNCF -->
    <section id="sncf" aria-label="SNCF">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_sncf.png" alt="" style="right:8%; top:10%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">SNCF</h1>
        <p class="lead">Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
      </div>
    </section>

    <!-- LAMIH -->
    <section id="lamih" aria-label="LAMIH">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_lamih.png" alt="" style="left:10%; top:14%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">LAMIH</h1>
        <p class="lead">Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
      </div>
    </section>

    <!-- PM DIMENSIONS -->
    <section id="pmdim" aria-label="PM DIMENSIONS">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_pmdimensions.png" alt="" style="right:8%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">PM DIMENSIONS</h1>
        <p class="lead">3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
      </div>
    </section>

    <!-- INDIAN RAILWAYS -->
    <section id="indian" aria-label="Indian Railways">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <img class="float" src="float_indianrail.png" alt="" style="left:6%; top:16%;" onerror="this.style.display='none'">
      <div class="content">
        <h1 class="title">Indian Railways (Intern)</h1>
        <p class="lead">Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
      </div>
    </section>

    <!-- EDUCATION -->
    <section id="education" aria-label="Education">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card">
        <h3>Education — Formation</h3>
        <p style="color:var(--muted);margin-top:8px"><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)</p>
        <p style="color:var(--muted);margin-top:8px"><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" aria-label="Skills">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card">
        <h3>Skills & Tools — Compétences</h3>
        <ul style="margin-top:8px;color:var(--muted);line-height:1.6">
          <li>CATIA V5, Ansys, HyperWorks / OptiStruct</li>
          <li>FEA, CAD Automation, PDM / DMA / SAM</li>
          <li>Project planning · Team leadership · Budgeting & procurement</li>
        </ul>
      </div>
    </section>

    <!-- PUBLICATION -->
    <section id="publication" aria-label="Publication">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content card" style="text-align:left">
        <h3>Publication — Avril 2018</h3>
        <p style="color:var(--muted);margin-top:8px">Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018.</p>
        <div style="margin-top:18px">
          <a class="btn" href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" aria-label="Contact">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="overlay" aria-hidden="true"></div>

      <div class="content">
        <h1 class="title">Let's build something exceptional — Parlons</h1>
        <p class="lead">Email: <a href="mailto:venkata.france@gmail.com" style="color:#0b1a1f">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821" style="color:#0b1a1f">+33 7 55 66 28 21</a></p>
        <div class="social-row" style="margin-top:14px">
          <a class="social-link" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
          <a class="social-link" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
        </div>
      </div>
    </section>

  </main>

  <footer>© Kadiyala Venkata Raghavendra</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
(() => {
  // Menu logic
  const hambutton = document.getElementById('hambutton');
  const menu = document.getElementById('menu');
  const main = document.getElementById('site-main');

  function toggleMenu(open){
    if(open){
      menu.classList.add('open');
      hambutton.setAttribute('aria-expanded','true');
    } else {
      menu.classList.remove('open');
      hambutton.setAttribute('aria-expanded','false');
    }
  }

  hambutton.addEventListener('click', ()=> toggleMenu(!menu.classList.contains('open')));
  hambutton.addEventListener('keydown', (e)=> { if(e.key==='Enter'||e.key===' '){ e.preventDefault(); toggleMenu(!menu.classList.contains('open')); }});

  // menu links scroll + close menu
  menu.querySelectorAll('a').forEach(a=>{
    a.addEventListener('click', (ev)=>{
      ev.preventDefault();
      const target = document.getElementById(a.getAttribute('data-target'));
      toggleMenu(false);
      if(target){
        target.scrollIntoView({behavior:'smooth', block:'start'});
      }
    });
  });

  // close on outside click
  document.addEventListener('click', (e)=>{
    if(!menu.contains(e.target) && !hambutton.contains(e.target) && menu.classList.contains('open')) toggleMenu(false);
  });

  // GSAP reveals + parallax
  try {
    gsap.registerPlugin(ScrollTrigger);
    document.querySelectorAll('main section').forEach(sec=>{
      const content = sec.querySelector('.content');
      const floatEl = sec.querySelector('.float');
      const backdrop = sec.querySelector('.backdrop');

      if(content){
        gsap.fromTo(content, {y:28, autoAlpha:0}, {
          y:0, autoAlpha:1, duration:0.85, ease:'power3.out',
          scrollTrigger: { trigger: sec, start:'top 75%', toggleActions:'play none none reverse' }
        });
      }
      if(floatEl){
        gsap.to(floatEl, {
          y: (Math.random()>0.5? -30:30),
          x: (Math.random()>0.5? 16:-16),
          ease:'sine.inOut',
          scrollTrigger: { trigger: sec, start:'top bottom', end:'bottom top', scrub:1 }
        });
      }
      if(backdrop){
        gsap.to(backdrop, {
          yPercent:4, ease:'none',
          scrollTrigger: { trigger: sec, start:'top bottom', end:'bottom top', scrub:0.6 }
        });
      }
    });

    // hide scroll indicator after first scroll
    const sc = document.getElementById('scroll-indicator');
    if(sc){
      ScrollTrigger.create({ start: 20, onEnter: ()=> gsap.to(sc,{autoAlpha:0,duration:.45}) });
    }
  } catch(e){
    console.error('GSAP init failed', e);
  }

  // keyboard nav (PageUp/PageDown/Arrows) — move to next/prev section
  window.addEventListener('keydown', (e)=>{
    const sections = Array.from(document.querySelectorAll('main section'));
    const top = document.documentElement.scrollTop || document.body.scrollTop || document.querySelector('main').scrollTop;
    const vh = window.innerHeight;
    if(['ArrowDown','PageDown'].includes(e.key)){
      e.preventDefault();
      const cur = Math.round(top / vh);
      const next = Math.min(sections.length-1, cur+1);
      sections[next].scrollIntoView({behavior:'smooth'});
    } else if(['ArrowUp','PageUp'].includes(e.key)){
      e.preventDefault();
      const cur = Math.round(top / vh);
      const prev = Math.max(0, cur-1);
      sections[prev].scrollIntoView({behavior:'smooth'});
    }
  });
})();
</script>
</body>
</html>
