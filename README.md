<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Venkata Raghavendra KADIYALA — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
<style>
  :root{
    --teal-start:#14b6a0;
    --teal-end:#0da58f;
    --muted:#58636b;
    --bg-top:#ffffff;
    --bg-bottom:#f5f6f8;
    --card-bg:#ffffff;
    --card-shadow:0 18px 50px rgba(6,12,16,0.06);
    --glass: rgba(255,255,255,0.78);
    --content-width:1100px;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%;width:100%;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));color:#0b1a1f;-webkit-font-smoothing:antialiased;overflow:hidden}
  a{color:inherit;text-decoration:none}
  main{height:100vh;width:100vw;overflow-y:auto;overflow-x:hidden; -webkit-overflow-scrolling:touch; scroll-behavior:smooth;}
  main::-webkit-scrollbar{display:none}
  html { scrollbar-width: none; -ms-overflow-style: none; }
  section{min-height:100vh;height:100vh;width:100%;position:relative;display:flex;align-items:center;justify-content:center;padding:36px;scroll-snap-align:start}
  .backdrop{position:absolute;inset:0;background:linear-gradient(180deg,var(--bg-top),var(--bg-bottom));z-index:0}
  .underlay{position:absolute;inset:0;z-index:1;pointer-events:none;background:linear-gradient(180deg, rgba(11,26,31,0.02), rgba(6,12,14,0.03));}
  .content{position:relative;z-index:6;max-width:var(--content-width);width:100%;padding:24px;display:flex;flex-direction:column;gap:12px;align-items:center;justify-content:center}
  .card{background:var(--card-bg);border-radius:14px;padding:28px;box-shadow:var(--card-shadow);max-width:1000px;width:100%;text-align:left;color:#0b1a1f}
  .card h3{margin:0 0 10px 0;font-size:20px}
  .card p{margin:8px 0;color:var(--muted);line-height:1.6}
  .card ul{margin:6px 0 0 18px;color:var(--muted);line-height:1.6}
  h1.title{font-weight:900;font-size:clamp(32px,7vw,72px);line-height:1;text-transform:uppercase;margin:10px 0}
  h2.subtitle{font-weight:700;color:var(--muted);font-size:18px;margin:0}
  p.lead{color:var(--muted);max-width:980px;line-height:1.6;font-size:16px;margin:0}
  .portrait{height:56vh;max-height:700px;object-fit:cover;border-radius:10px;box-shadow:0 30px 80px rgba(6,12,16,0.06)}
  .hamburger{position:fixed;right:18px;top:14px;z-index:140;display:flex;align-items:center;gap:10px}
  .hambutton{width:50px;height:44px;border-radius:10px;background:var(--glass);backdrop-filter:blur(8px);display:flex;align-items:center;justify-content:center;border:1px solid rgba(6,12,16,0.04);cursor:pointer;color:#0b1a1f;box-shadow:0 8px 30px rgba(6,12,16,0.06)}
  .menu{position:fixed;right:18px;top:72px;z-index:139;min-width:240px;border-radius:12px;background:var(--glass);backdrop-filter:blur(10px);box-shadow:0 20px 60px rgba(6,12,16,0.06);overflow:hidden;opacity:0;visibility:hidden;transform-origin:top right;transition:all .22s ease}
  .menu.open{opacity:1;visibility:visible;transform:translateY(0)}
  .menu a{display:flex;align-items:center;justify-content:space-between;padding:12px 16px;color:#0b1a1f;border-bottom:1px solid rgba(6,12,16,0.02);font-weight:700}
  .menu a:last-child{border-bottom:0}
  .menu a:hover{background:rgba(6,12,16,0.02)}
  .btn{display:inline-flex;align-items:center;gap:10px;padding:12px 18px;border-radius:12px;font-weight:800;color:white;background:linear-gradient(90deg,var(--teal-start),var(--teal-end));box-shadow:0 14px 40px rgba(13,77,64,0.08);cursor:pointer}
  .social-row{display:flex;gap:12px;align-items:center;justify-content:center;margin-top:8px}
  .social-link{padding:8px 12px;border-radius:10px;background:rgba(6,12,16,0.03);font-weight:700;color:#0b1a1f}
  #scroll-indicator{position:absolute;bottom:24px;left:50%;transform:translateX(-50%);z-index:10;color:var(--muted);font-size:20px;animation:scroll-bob 1.6s infinite}
  @keyframes scroll-bob{0%{transform:translate(-50%,0)}50%{transform:translate(-50%,10px)}100%{transform:translate(-50%,0)}}
  footer{padding:16px;text-align:center;color:var(--muted);background:linear-gradient(180deg,transparent,rgba(0,0,0,0.01))}
  @media(max-width:980px){.portrait{height:44vh}.menu{right:10px;min-width:calc(100% - 20px)}}
</style>
</head>
<body>
  <!-- hamburger -->
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
      <div class="underlay" aria-hidden="true"></div>
      <div class="content" role="region" aria-labelledby="heroTitle">
        <div class="card" style="text-align:center">
          <!-- IMPORTANT: upload your portrait and name it portrait.jpg in repo root -->
          <img src="portrait.jpg" alt="Portrait of Venkata" class="portrait" onerror="this.style.display='none'">
          <h1 class="title" id="heroTitle">VENKATA RAGHAVENDRA <span style="color:#0aa589">KADIYALA</span></h1>
          <h2 class="subtitle">Mechanical Engineer · Creative Designer — Train interiors & systems</h2>
          <p class="lead">☎ <a href="tel:+33755662821" style="color:#0b1a1f">+33 7 55 66 28 21</a> · ✉ <a href="mailto:venkata.france@gmail.com" style="color:#0b1a1f">venkata.france@gmail.com</a></p>
          <div class="social-row">
            <a class="social-link" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
            <a class="social-link" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
          </div>
        </div>
      </div>
      <div id="scroll-indicator" aria-hidden="true">▼</div>
    </section>

    <!-- ABOUT -->
    <section id="about" aria-label="About">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3 id="aboutTitle">About — À propos</h3>
          <p><strong>English:</strong> I combine mechanical engineering rigor with product design thinking. I deliver production-ready 3D models (M0 → M5), lead CAD teams, coordinate suppliers and ensure manufacturability with user-focused outcomes.</p>
          <p style="margin-top:8px"><strong>Français:</strong> J’allie rigueur mécanique et pensée produit. Livraison de modèles 3D validés (M0 → M5), pilotage CAO, coordination fournisseurs et focus sur la fabricabilité et l’usage.</p>
          <div style="margin-top:12px">
            <strong>Responsibilities & Project Management</strong>
            <ul>
              <li>Project planning & scheduling</li>
              <li>Team leadership and coordination (multi-discipline)</li>
              <li>Budgeting, financing oversight and cost control</li>
              <li>Procurement & supplier buying (technical specification, negotiation)</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- EXPERIENCES anchor -->
    <section id="experiences" aria-label="Experiences">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3 id="expTitle">Experiences</h3>
          <p style="margin-top:8px;color:var(--muted)">Scroll down — each experience occupies a full screen in sequence.</p>
        </div>
      </div>
    </section>

    <!-- OSTA -->
    <section id="osta" aria-label="SEGULA OSTA">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>SEGULA — Project OSTA</h3>
          <p>Design & development of interior components — windows, blinds, sidewalls, intercoms, electrical cabinets and under-seat boxes. Delivery of validated 3D models and supplier coordination.</p>
        </div>
      </div>
    </section>

    <!-- BaWu -->
    <section id="bawu" aria-label="SEGULA BaWu">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>SEGULA — BaWu</h3>
          <p>3D validation, integration issue prevention, QA management, KPI & OIL tracking, and CAD governance for industrial handover.</p>
        </div>
      </div>
    </section>

    <!-- RER NG -->
    <section id="rerng" aria-label="SEGULA RER NG">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>SEGULA — RER NG</h3>
          <p>Requirements analysis, mechanical integration resolution, on-site surveys and structural part design in CATIA V5 with criticality reporting.</p>
        </div>
      </div>
    </section>

    <!-- DSB -->
    <section id="dsb" aria-label="SEGULA DSB">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>SEGULA — DSB</h3>
          <p>Seat layout planning, under-seat boxes, cantilever & ceiling integration, 3D/2D/FTA modelling and supplier coordination.</p>
        </div>
      </div>
    </section>

    <!-- SNCF -->
    <section id="sncf" aria-label="SNCF">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>SNCF</h3>
          <p>Automation of bolted assemblies (TCL), meshing, static & non-static analyses for seat supports, modelling in CATIA V5 and structural validation.</p>
        </div>
      </div>
    </section>

    <!-- LAMIH -->
    <section id="lamih" aria-label="LAMIH">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>LAMIH</h3>
          <p>Accident analysis, signalling automation proposals and prevention measures, data-driven concepts for autonomous train systems (ETCS / CBTC).</p>
        </div>
      </div>
    </section>

    <!-- PM DIMENSIONS -->
    <section id="pmdim" aria-label="PM DIMENSIONS">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>PM DIMENSIONS</h3>
          <p>3D part design, prototype development and client conformity checks (Hyundai). CATIA V5 modelling and verification.</p>
        </div>
      </div>
    </section>

    <!-- INDIAN RAILWAYS -->
    <section id="indian" aria-label="Indian Railways">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>Indian Railways (Intern)</h3>
          <p>Coupling prototype development, wagon inspection, maintenance optimisation and Ansys-based structural analysis.</p>
        </div>
      </div>
    </section>

    <!-- EDUCATION -->
    <section id="education" aria-label="Education">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>Education — Formation</h3>
          <p><strong>Master</strong> — International Transport & Energy, INSA Hauts-de-France (2019–2021)</p>
          <p style="margin-top:6px"><strong>Bachelor</strong> — Mechanical Engineering, KL University (2014–2018)</p>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" aria-label="Skills">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>Skills & Tools — Compétences</h3>
          <ul>
            <li>CATIA V5, Ansys, HyperWorks / OptiStruct</li>
            <li>FEA, CAD Automation, PDM / DMA / SAM</li>
            <li>Project planning · Team leadership · Budgeting & procurement</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- PUBLICATION -->
    <section id="publication" aria-label="Publication">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card">
          <h3>Publication — Avril 2018</h3>
          <p>Enhancement of Refrigeration Effect Using Flue Gases from Chimney — April 2018.</p>
          <div style="margin-top:14px">
            <a class="btn" href="https://iaeme.com/MasterAdmin/Journal_uploads/IJMET/VOLUME_9_ISSUE_4/IJMET_09_04_041.pdf" target="_blank" rel="noopener">Read the paper (IAEME)</a>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" aria-label="Contact">
      <div class="backdrop" aria-hidden="true"></div>
      <div class="underlay" aria-hidden="true"></div>
      <div class="content">
        <div class="card" style="text-align:center">
          <h3>Contact</h3>
          <p>Email: <a href="mailto:venkata.france@gmail.com">venkata.france@gmail.com</a> · Phone: <a href="tel:+33755662821">+33 7 55 66 28 21</a></p>
          <div style="margin-top:12px" class="social-row">
            <a class="social-link" href="https://www.linkedin.com/in/venkata-kadiyala" target="_blank" rel="noopener">LinkedIn</a>
            <a class="social-link" href="https://www.instagram.com/raghukadiyala/" target="_blank" rel="noopener">Instagram</a>
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer>© Kadiyala Venkata Raghavendra</footer>

<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
<script>
(() => {
  // menu toggle
  const hambutton = document.getElementById('hambutton');
  const menu = document.getElementById('menu');

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
  hambutton.addEventListener('keydown', (e)=> { if(e.key==='Enter' || e.key===' '){ e.preventDefault(); toggleMenu(!menu.classList.contains('open')); }});

  // menu links scroll
  menu.querySelectorAll('a').forEach(a => {
    a.addEventListener('click', (ev) => {
      ev.preventDefault();
      const target = document.getElementById(a.getAttribute('data-target'));
      toggleMenu(false);
      if(target){
        target.scrollIntoView({behavior:'smooth', block:'start'});
      }
    });
  });

  // close menu when clicking outside
  document.addEventListener('click', (e) => {
    if(!menu.contains(e.target) && !hambutton.contains(e.target) && menu.classList.contains('open')) toggleMenu(false);
  });

  // GSAP reveals + subtle parallax for portrait (only if visible)
  try {
    gsap.registerPlugin(ScrollTrigger);
    const secs = document.querySelectorAll('main section');

    secs.forEach(sec => {
      const card = sec.querySelector('.card');
      const portrait = sec.querySelector('.portrait');
      const backdrop = sec.querySelector('.backdrop');

      if(card){
        gsap.fromTo(card, {y:28, autoAlpha:0}, {
          y:0, autoAlpha:1, duration:0.8, ease:'power3.out',
          scrollTrigger: { trigger: sec, start: 'top 80%', toggleActions: 'play none none reverse' }
        });
      }

      // subtle parallax on portrait when it's in hero
      if(portrait && sec.id==='hero'){
        gsap.to(portrait, {
          y: -24,
          ease: 'sine.inOut',
          scrollTrigger: { trigger: sec, start: 'top bottom', end: 'bottom top', scrub: 0.8 }
        });
      }

      if(backdrop){
        gsap.to(backdrop, {
          yPercent: 3,
          ease: 'none',
          scrollTrigger: { trigger: sec, start: 'top bottom', end: 'bottom top', scrub: 0.6 }
        });
      }
    });

    // hide scroll indicator after first scroll
    const sc = document.getElementById('scroll-indicator');
    if(sc){
      ScrollTrigger.create({ start: 30, onEnter: () => gsap.to(sc, {autoAlpha: 0, duration: .45}) });
    }
  } catch(e){
    console.error('GSAP init error', e);
  }

  // keyboard navigation (PageUp/PageDown/Arrow)
  window.addEventListener('keydown', (e) => {
    const sections = Array.from(document.querySelectorAll('main section'));
    const main = document.querySelector('main');
    const top = main.scrollTop;
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
