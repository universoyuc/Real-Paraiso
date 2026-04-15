# Real-Paraiso
WEB bienes Raices
<!DOCTYPE html>
<html lang="es" class="lang-es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Real Paraíso | Master Plan Mérida–Progreso</title>
  <meta
    name="description"
    content="Real Paraíso: master plan con macro lotes para desarrollo, lotes de inversión y una avenida icónica en el corredor Mérida–Progreso."
  />
  <style>
    :root {
      --bg: #f7f1e7;
      --paper: #fffdf8;
      --ink: #1b3127;
      --muted: #617569;
      --green: #1f3d2b;
      --green-2: #2f5b42;
      --gold: #c8a96a;
      --gold-2: #e0c28b;
      --line: rgba(27, 49, 39, 0.12);
      --shadow: 0 20px 60px rgba(20, 30, 24, 0.12);
      --radius: 24px;
      --max: 1240px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background: linear-gradient(180deg, #f8f3ea 0%, #f5efe4 100%);
      color: var(--ink);
      font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.5;
    }

    h1, h2, h3, .brand {
      font-family: Georgia, "Times New Roman", serif;
      line-height: 1.05;
      margin: 0;
      letter-spacing: 0.02em;
    }

    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }

    .container {
      width: min(var(--max), calc(100% - 32px));
      margin: 0 auto;
    }

    .section { padding: 88px 0; }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      text-transform: uppercase;
      font-size: 12px;
      letter-spacing: 0.18em;
      font-weight: 700;
      color: var(--green-2);
      margin-bottom: 14px;
    }

    .eyebrow::before {
      content: "";
      width: 42px;
      height: 1px;
      background: var(--gold);
    }

    .nav {
      position: sticky;
      top: 0;
      z-index: 50;
      background: rgba(247, 241, 231, 0.8);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(27, 49, 39, 0.08);
    }

    .nav-inner {
      min-height: 78px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 18px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 14px;
      font-weight: 700;
    }

    .logo-mark {
      width: 52px;
      height: 52px;
      border-radius: 16px;
      background: linear-gradient(135deg, var(--green), #29553d);
      color: var(--gold-2);
      display: grid;
      place-items: center;
      box-shadow: var(--shadow);
      font-size: 20px;
      font-weight: 800;
    }

    .logo-text small {
      display: block;
      font-size: 12px;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--muted);
    }

    .menu {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      font-size: 14px;
      color: var(--muted);
      font-weight: 600;
    }

    .lang-toggle {
      display: inline-flex;
      border: 1px solid rgba(27, 49, 39, 0.12);
      border-radius: 999px;
      background: #fff;
      overflow: hidden;
    }

    .lang-toggle button {
      border: 0;
      padding: 10px 14px;
      background: transparent;
      cursor: pointer;
      font-weight: 700;
      color: var(--muted);
    }

    .lang-toggle button.active {
      background: var(--green);
      color: #fff;
    }

    .hero {
      min-height: 92vh;
      display: grid;
      align-items: end;
      color: #fff;
      background:
        linear-gradient(180deg, rgba(7, 14, 11, 0.08), rgba(7, 14, 11, 0.18) 55%, rgba(7, 14, 11, 0.62)),
        url("./hero-boulevard.jpg") center/cover no-repeat;
    }

    .hero .container { padding: 64px 0 72px; }

    .hero-card {
      width: min(780px, 100%);
      background: rgba(9, 18, 14, 0.34);
      border: 1px solid rgba(255, 255, 255, 0.14);
      backdrop-filter: blur(10px);
      padding: 32px;
      border-radius: 28px;
      box-shadow: var(--shadow);
    }

    .hero h1 {
      font-size: clamp(46px, 8vw, 88px);
      margin-bottom: 14px;
    }

    .hero p {
      font-size: clamp(18px, 2.2vw, 22px);
      max-width: 700px;
      margin: 0 0 24px;
      color: rgba(255, 255, 255, 0.92);
    }

    .btns {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      padding: 14px 22px;
      border-radius: 999px;
      font-weight: 700;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.12);
      border: 1px solid transparent;
      transition: transform 0.18s ease, background 0.18s ease;
      cursor: pointer;
    }

    .btn:hover { transform: translateY(-1px); }
    .btn.primary { background: var(--green); color: #fff; }
    .btn.secondary { background: #fff; color: var(--green); }
    .btn.gold { background: linear-gradient(135deg, var(--gold), var(--gold-2)); color: #18271f; }
    .btn.ghost { background: transparent; color: var(--green); border-color: rgba(27, 49, 39, 0.18); }

    .kpis {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 14px;
      margin-top: 22px;
    }

    .kpi {
      background: rgba(255, 255, 255, 0.09);
      border: 1px solid rgba(255, 255, 255, 0.14);
      padding: 14px 16px;
      border-radius: 18px;
    }

    .kpi strong { display: block; font-size: 24px; }
    .kpi span { font-size: 13px; color: rgba(255, 255, 255, 0.8); }

    .grid-2 {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 28px;
      align-items: center;
    }

    .lead {
      font-size: 19px;
      color: var(--muted);
      max-width: 760px;
    }

    .feature-list {
      display: grid;
      gap: 14px;
      margin-top: 20px;
    }

    .feature {
      display: grid;
      grid-template-columns: 42px 1fr;
      gap: 14px;
    }

    .feature i {
      width: 42px;
      height: 42px;
      border-radius: 14px;
      background: linear-gradient(135deg, rgba(200, 169, 106, 0.2), rgba(31, 61, 43, 0.08));
      display: grid;
      place-items: center;
      font-style: normal;
      font-weight: 800;
      color: var(--green);
    }

    .card {
      background: var(--paper);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .pad { padding: 28px; }

    .project-gallery {
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 24px;
    }

    .project-gallery img,
    .thumb-grid img,
    .gallery-grid img {
      border-radius: 24px;
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
      width: 100%;
      object-fit: cover;
    }

    .master-plan {
      display: grid;
      grid-template-columns: 1.08fr 0.92fr;
      gap: 26px;
      align-items: start;
    }

    .plan-wrap {
      position: relative;
      border-radius: 28px;
      overflow: hidden;
      border: 1px solid var(--line);
      background: #fff;
      box-shadow: var(--shadow);
    }

    .plan-stage {
      position: relative;
      aspect-ratio: 1.18 / 1;
      background: #faf8f3;
    }

    .plan-stage img {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: contain;
      padding: 18px;
    }

    .plan-svg { position: absolute; inset: 0; }

    .lot {
      fill: rgba(200, 169, 106, 0.16);
      stroke: rgba(31, 61, 43, 0.72);
      stroke-width: 3;
      cursor: pointer;
      transition: 0.18s ease;
    }

    .lot:hover,
    .lot.active {
      fill: rgba(200, 169, 106, 0.42);
      stroke: #163525;
      stroke-width: 3.6;
    }

    .lot-label {
      font-size: 16px;
      font-weight: 800;
      fill: #163525;
      text-anchor: middle;
      dominant-baseline: middle;
      pointer-events: none;
    }

    .lot-sub {
      font-size: 12px;
      font-weight: 700;
      fill: rgba(22, 53, 37, 0.88);
      text-anchor: middle;
      pointer-events: none;
    }

    .side-panel { position: sticky; top: 96px; }

    .lot-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 14px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(31, 61, 43, 0.06);
      color: var(--green);
      font-size: 13px;
      font-weight: 700;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 14px;
      margin-top: 20px;
    }

    .stat {
      background: linear-gradient(180deg, #fffdfa, #f6f1e7);
      border: 1px solid var(--line);
      padding: 16px;
      border-radius: 18px;
    }

    .stat strong { display: block; font-size: 24px; }
    .stat span { font-size: 13px; color: var(--muted); }

    .split-cards {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 22px;
    }

    .invest-card {
      position: relative;
      overflow: hidden;
      min-height: 300px;
      background: linear-gradient(180deg, rgba(31, 61, 43, 0.94), rgba(18, 34, 25, 0.98));
      color: #fff;
    }

    .invest-card.light {
      background: linear-gradient(180deg, #fffdfa, #f5efe4);
      color: var(--ink);
    }

    .invest-card .content { position: relative; padding: 28px; }

    .gallery-grid {
      display: grid;
      grid-template-columns: 1.15fr 0.85fr 0.85fr;
      gap: 18px;
      margin-top: 26px;
    }

    .gallery-grid img {
      aspect-ratio: 1.15 / 1;
    }

    .location-grid,
    .contact-wrap {
      display: grid;
      grid-template-columns: 0.95fr 1.05fr;
      gap: 24px;
    }

    .location-map {
      border-radius: 24px;
      overflow: hidden;
      border: 1px solid var(--line);
      box-shadow: var(--shadow);
    }

    .map-frame {
      width: 100%;
      min-height: 420px;
      border: 0;
      display: block;
    }

    .thumb-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 16px;
    }

    form { display: grid; gap: 14px; }

    .field-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 14px;
    }

    input, select, textarea {
      width: 100%;
      padding: 14px 16px;
      border-radius: 16px;
      border: 1px solid rgba(27, 49, 39, 0.12);
      font: inherit;
      background: #fff;
    }

    textarea {
      min-height: 140px;
      resize: vertical;
    }

    .contact-card {
      background: linear-gradient(180deg, rgba(31, 61, 43, 0.96), rgba(18, 34, 25, 0.98));
      color: #fff;
    }

    .contact-card p { color: rgba(255, 255, 255, 0.84); }

    .contact-link {
      display: flex;
      align-items: center;
      gap: 14px;
      padding: 14px 0;
      border-top: 1px solid rgba(255, 255, 255, 0.12);
    }

    .contact-link:first-of-type { border-top: 0; }

    .contact-link i {
      width: 44px;
      height: 44px;
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.08);
      display: grid;
      place-items: center;
      font-style: normal;
      color: #e6d1a7;
      font-weight: 800;
    }

    .footer {
      padding: 30px 0 48px;
      color: var(--muted);
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 24px;
      flex-wrap: wrap;
      border-top: 1px solid var(--line);
      padding-top: 24px;
    }

    .wa-float {
      position: fixed;
      right: 18px;
      bottom: 18px;
      z-index: 60;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      padding: 14px 18px;
      border-radius: 999px;
      background: #1f7d47;
      color: #fff;
      font-weight: 800;
      box-shadow: 0 20px 50px rgba(7, 24, 14, 0.28);
    }

    [data-lang] { display: none; }
    html.lang-es [data-lang="es"],
    html.lang-en [data-lang="en"] { display: block; }
    [data-inline] { display: none; }
    html.lang-es [data-inline="es"],
    html.lang-en [data-inline="en"] { display: inline; }

    @media (max-width: 1080px) {
      .grid-2,
      .project-gallery,
      .master-plan,
      .location-grid,
      .contact-wrap {
        grid-template-columns: 1fr;
      }

      .side-panel { position: static; }
      .kpis { grid-template-columns: repeat(2, minmax(0, 1fr)); }
      .gallery-grid { grid-template-columns: 1fr; }
    }

    @media (max-width: 820px) {
      .menu { display: none; }
      .split-cards,
      .field-grid,
      .stats,
      .kpis,
      .thumb-grid {
        grid-template-columns: 1fr;
      }

      .section { padding: 72px 0; }
    }
  </style>
</head>
<body>
  <header class="nav">
    <div class="container nav-inner">
      <a href="#top" class="logo">
        <div class="logo-mark">RP</div>
        <div class="logo-text">
          <div class="brand">REAL PARAÍSO</div>
          <small>Master plan Mérida–Progreso</small>
        </div>
      </a>

      <nav class="menu">
        <a href="#proyecto"><span data-inline="es">Proyecto</span><span data-inline="en">Project</span></a>
        <a href="#masterplan">Master Plan</a>
        <a href="#inversion"><span data-inline="es">Inversión</span><span data-inline="en">Investment</span></a>
        <a href="#ubicacion"><span data-inline="es">Ubicación</span><span data-inline="en">Location</span></a>
        <a href="#galeria"><span data-inline="es">Galería</span><span data-inline="en">Gallery</span></a>
        <a href="#contacto"><span data-inline="es">Contacto</span><span data-inline="en">Contact</span></a>
      </nav>

      <div class="lang-toggle">
        <button id="langEs" class="active">ES</button>
        <button id="langEn">EN</button>
      </div>
    </div>
  </header>

  <section class="hero" id="top">
    <div class="container">
      <div class="hero-card">
        <div class="eyebrow" data-lang="es">Corredor Mérida–Progreso</div>
        <div class="eyebrow" data-lang="en">Mérida–Progreso corridor</div>

        <h1>REAL PARAÍSO</h1>

        <p data-lang="es">
          Donde la visión se convierte en desarrollo y oportunidad. Un master plan con boulevard icónico,
          macro lotes para desarrollo y oportunidades de inversión en una zona con crecimiento real.
        </p>
        <p data-lang="en">
          Where vision becomes development and opportunity. A master plan with an iconic boulevard,
          macro development lots, and investment opportunities in a corridor with real growth momentum.
        </p>

        <div class="btns">
          <a href="#masterplan" class="btn gold"><span data-inline="es">Descubrir oportunidades</span><span data-inline="en">Discover opportunities</span></a>
          <a href="#contacto" class="btn secondary"><span data-inline="es">Solicitar información</span><span data-inline="en">Request information</span></a>
          <a class="btn primary" target="_blank" rel="noopener" href="https://wa.me/529992227538?text=Hola,%20quiero%20informaci%C3%B3n%20de%20Real%20Para%C3%ADso">WhatsApp</a>
        </div>

        <div class="kpis">
          <div class="kpi"><strong>6</strong><span data-lang="es">Macro lotes estratégicos</span><span data-lang="en">Strategic macro lots</span></div>
          <div class="kpi"><strong>90–130 mil m²</strong><span data-lang="es">Superficies principales</span><span data-lang="en">Main lot sizes</span></div>
          <div class="kpi"><strong>21.1819052</strong><span data-lang="es">Latitud</span><span data-lang="en">Latitude</span></div>
          <div class="kpi"><strong>-89.6241033</strong><span data-lang="es">Longitud</span><span data-lang="en">Longitude</span></div>
        </div>
      </div>
    </div>
  </section>

  <section class="section" id="proyecto">
    <div class="container grid-2">
      <div>
        <div class="eyebrow" data-lang="es">El proyecto</div>
        <div class="eyebrow" data-lang="en">The project</div>

        <h2 style="font-size:clamp(36px,5vw,62px);margin-bottom:18px;" data-lang="es">Un desarrollo que se vive desde su acceso</h2>
        <h2 style="font-size:clamp(36px,5vw,62px);margin-bottom:18px;" data-lang="en">A development defined from the moment you arrive</h2>

        <p class="lead" data-lang="es">
          Real Paraíso no se presenta como simple tierra en venta. Se presenta como un master plan con identidad,
          boulevard central, vocación de desarrollo y oportunidades para constructoras, inversionistas y compradores patrimoniales.
        </p>
        <p class="lead" data-lang="en">
          Real Paraíso is not presented as raw land. It is a master plan with identity,
          a signature boulevard, development potential, and opportunities for builders, investors, and long-term buyers.
        </p>

        <div class="feature-list">
          <div class="feature">
            <i>01</i>
            <div>
              <strong data-lang="es">Avenida icónica como diferenciador</strong>
              <strong data-lang="en">An iconic boulevard as the differentiator</strong>
              <div data-lang="es">El acceso principal se convierte en la imagen del proyecto y en el activo emocional de la marca.</div>
              <div data-lang="en">The main boulevard becomes the visual identity of the development and the emotional asset of the brand.</div>
            </div>
          </div>

          <div class="feature">
            <i>02</i>
            <div>
              <strong data-lang="es">Doble enfoque comercial</strong>
              <strong data-lang="en">Dual commercial strategy</strong>
              <div data-lang="es">Macro lotes para constructoras e inversionistas; lotes menores para público general.</div>
              <div data-lang="en">Macro lots for developers and investors; smaller lots for the general public.</div>
            </div>
          </div>

          <div class="feature">
            <i>03</i>
            <div>
              <strong data-lang="es">Ubicación con lectura de crecimiento</strong>
              <strong data-lang="en">Location aligned with growth</strong>
              <div data-lang="es">Corredor Mérida–Progreso, cercanía al Autódromo Yucatán y entorno con desarrollo en expansión.</div>
              <div data-lang="en">Mérida–Progreso corridor, close to Autódromo Yucatán, surrounded by expanding development.</div>
            </div>
          </div>
        </div>
      </div>

      <div class="project-gallery">
        <img src="./hero-boulevard.jpg" alt="Boulevard principal de Real Paraíso" />
        <div class="card pad">
          <h3 style="font-size:30px;margin-bottom:12px;" data-lang="es">Visión urbana + naturaleza premium</h3>
          <h3 style="font-size:30px;margin-bottom:12px;" data-lang="en">Urban vision + premium nature</h3>

          <p data-lang="es">
            El proyecto se apoya en un lenguaje visual sobrio y aspiracional: vegetación icónica, amplitud vial,
            orden, jerarquía y una experiencia pensada para reforzar percepción de valor desde el primer contacto.
          </p>
          <p data-lang="en">
            The project uses a sober and aspirational visual language: iconic vegetation, generous road width,
            order, hierarchy, and an arrival experience designed to reinforce value from the first contact.
          </p>

          <div class="lot-badges">
            <span class="badge">Lujo + naturaleza</span>
            <span class="badge">Bilingüe</span>
            <span class="badge">CRM ready</span>
          </div>

          <div class="stats">
            <div class="stat"><strong>3.2 km</strong><span data-lang="es">Aproximadamente desde km 24.1 hacia el interior</span><span data-lang="en">Approx. 3.2 km inland from km 24.1</span></div>
            <div class="stat"><strong>Mixto</strong><span data-lang="es">Desarrolladores + público general</span><span data-lang="en">Developers + general public</span></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="section" id="masterplan">
    <div class="container master-plan">
      <div class="plan-wrap">
        <div class="plan-stage">
          <img src="./master-plan.jpg" alt="Plano ilustrativo y master plan" />
          <svg class="plan-svg" viewBox="0 0 1000 850" preserveAspectRatio="none">
            <rect class="lot active" id="lot-2-1" x="70" y="140" width="260" height="150" rx="8"></rect>
            <text class="lot-label" x="200" y="205">LOTE 2.1</text>
            <text class="lot-sub" x="200" y="232">98,179 m²</text>

            <rect class="lot" id="lot-2-2" x="70" y="305" width="260" height="145" rx="8"></rect>
            <text class="lot-label" x="200" y="367">LOTE 2.2</text>
            <text class="lot-sub" x="200" y="394">100,884 m²</text>

            <rect class="lot" id="lot-2-3" x="70" y="468" width="260" height="165" rx="8"></rect>
            <text class="lot-label" x="200" y="540">LOTE 2.3</text>
            <text class="lot-sub" x="200" y="567">100,196 m²</text>

            <rect class="lot" id="lot-3-1" x="420" y="140" width="290" height="150" rx="8"></rect>
            <text class="lot-label" x="565" y="205">LOTE 3.1</text>
            <text class="lot-sub" x="565" y="232">90,566 m²</text>

            <rect class="lot" id="lot-3-2" x="420" y="305" width="290" height="145" rx="8"></rect>
            <text class="lot-label" x="565" y="367">LOTE 3.2</text>
            <text class="lot-sub" x="565" y="394">130,443 m²</text>

            <rect class="lot" id="lot-3-3" x="420" y="468" width="290" height="165" rx="8"></rect>
            <text class="lot-label" x="565" y="540">LOTE 3.3</text>
            <text class="lot-sub" x="565" y="567">124,735 m²</text>
          </svg>
        </div>
      </div>

      <aside class="side-panel">
        <div class="card pad">
          <div class="eyebrow">Master Plan</div>
          <h2 style="font-size:clamp(34px,4vw,52px);margin-bottom:14px;" data-lang="es">Explora cada oportunidad</h2>
          <h2 style="font-size:clamp(34px,4vw,52px);margin-bottom:14px;" data-lang="en">Explore every opportunity</h2>

          <p data-lang="es">
            Pasa el cursor o toca un lote para ver sus características. La selección abre una ficha comercial enfocada a desarrolladores,
            inversionistas o compradores patrimoniales.
          </p>
          <p data-lang="en">
            Hover or tap a lot to see its details. Each selection opens a commercial profile oriented to developers,
            investors, or patrimonial buyers.
          </p>

          <div class="card" style="margin-top:18px;border-radius:22px;padding:20px;background:#faf7f0;">
            <div style="font-size:12px;text-transform:uppercase;letter-spacing:.16em;color:var(--muted);font-weight:800;">
              <span data-inline="es">Lote seleccionado</span><span data-inline="en">Selected lot</span>
            </div>
            <h3 id="lot-name" style="font-size:34px;margin:8px 0 10px;">LOTE 2.1</h3>
            <div id="lot-size" style="font-size:18px;color:var(--muted);margin-bottom:10px;">98,179 m²</div>
            <p id="lot-copy" style="margin:0 0 14px;">Ideal para inversión estratégica o desarrollo por su escala, posición y lectura clara dentro del master plan.</p>
            <div class="lot-badges" id="lot-badges">
              <span class="badge">Macro lote</span>
              <span class="badge">Desarrollo</span>
              <span class="badge">Escala estratégica</span>
            </div>
          </div>

          <div class="btns" style="margin-top:18px;">
            <a href="#contacto" class="btn primary"><span data-inline="es">Solicitar información</span><span data-inline="en">Request information</span></a>
            <a target="_blank" rel="noopener" id="wa-lot" class="btn secondary" href="https://wa.me/529992227538?text=Hola,%20quiero%20informaci%C3%B3n%20del%20Lote%202.1%20de%20Real%20Para%C3%ADso">WhatsApp</a>
          </div>
        </div>
      </aside>
    </div>
  </section>

  <section class="section" id="inversion">
    <div class="container">
      <div class="eyebrow" data-lang="es">Inversión</div>
      <div class="eyebrow" data-lang="en">Investment</div>
      <h2 style="font-size:clamp(34px,5vw,58px);margin-bottom:14px;" data-lang="es">Dos rutas claras de oportunidad</h2>
      <h2 style="font-size:clamp(34px,5vw,58px);margin-bottom:14px;" data-lang="en">Two clear opportunity paths</h2>

      <p class="lead" data-lang="es">
        El proyecto está pensado para atender dos mercados distintos sin perder coherencia de marca:
        grandes superficies para desarrolladores y opciones más accesibles para compradores patrimoniales.
      </p>
      <p class="lead" data-lang="en">
        The project is designed to serve two distinct markets without losing brand coherence:
        large surfaces for developers and more accessible opportunities for long-term buyers.
      </p>

      <div class="split-cards" style="margin-top:28px;">
        <div class="card invest-card">
          <div class="content">
            <div class="eyebrow">Macro lots</div>
            <h3 style="font-size:40px;margin-bottom:12px;" data-lang="es">Para constructoras e inversionistas</h3>
            <h3 style="font-size:40px;margin-bottom:12px;" data-lang="en">For developers and investors</h3>
            <p data-lang="es">Superficies aproximadas de 9 a 13 hectáreas con lectura ideal para etapas, producto mixto, lotificación o desarrollo residencial.</p>
            <p data-lang="en">Approximate surfaces from 9 to 13 hectares, ideal for phasing, mixed-use concepts, subdivision or residential development.</p>
            <div class="lot-badges">
              <span class="badge" style="background:rgba(255,255,255,.12);color:#fff;">90,566–130,443 m²</span>
              <span class="badge" style="background:rgba(255,255,255,.12);color:#fff;">ROI potencial</span>
            </div>
          </div>
        </div>

        <div class="card invest-card light">
          <div class="content">
            <div class="eyebrow">Smaller lots</div>
            <h3 style="font-size:40px;margin-bottom:12px;" data-lang="es">Para público general</h3>
            <h3 style="font-size:40px;margin-bottom:12px;" data-lang="en">For the general public</h3>
            <p data-lang="es">Oportunidades pensadas para inversión patrimonial, compra anticipada y participación en una zona con consolidación progresiva.</p>
            <p data-lang="en">Opportunities designed for patrimonial investment, early entry, and participation in a corridor with progressive consolidation.</p>
            <div class="lot-badges">
              <span class="badge">Pre-venta</span>
              <span class="badge"><span data-inline="es">Solicitar</span><span data-inline="en">Request</span></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="section" id="galeria">
    <div class="container">
      <div class="eyebrow" data-lang="es">Galería</div>
      <div class="eyebrow" data-lang="en">Gallery</div>
      <h2 style="font-size:clamp(34px,5vw,58px);margin-bottom:14px;" data-lang="es">Imágenes que venden la visión del proyecto</h2>
      <h2 style="font-size:clamp(34px,5vw,58px);margin-bottom:14px;" data-lang="en">Images that sell the project vision</h2>
      <p class="lead" data-lang="es">Usa aquí renders del boulevard, master plan, accesos, glorietas y piezas comerciales que refuercen la identidad premium de Real Paraíso.</p>
      <p class="lead" data-lang="en">Use this section for boulevard renders, master plan views, access points, roundabouts, and commercial images that reinforce the premium identity of Real Paraíso.</p>

      <div class="gallery-grid">
        <img src="./hero-boulevard.jpg" alt="Boulevard principal" />
        <img src="./master-plan.jpg" alt="Master plan" />
        <img src="./zona-satelital.jpg" alt="Vista satelital" />
      </div>
    </div>
  </section>

  <section class="section" id="ubicacion">
    <div class="container location-grid">
      <div>
        <div class="eyebrow" data-lang="es">Ubicación estratégica</div>
        <div class="eyebrow" data-lang="en">Strategic location</div>
        <h2 style="font-size:clamp(34px,5vw,56px);margin-bottom:14px;" data-lang="es">Corredor Mérida–Progreso</h2>
        <h2 style="font-size:clamp(34px,5vw,56px);margin-bottom:14px;" data-lang="en">Mérida–Progreso corridor</h2>

        <p class="lead" data-lang="es">
          Real Paraíso se ubica cerca del km 24.1 de la carretera Mérida–Progreso, aproximadamente 3.2 km hacia el interior,
          en un entorno de proyectos existentes y en crecimiento, con cercanía al Autódromo Yucatán y buena lectura de expansión urbana.
        </p>
        <p class="lead" data-lang="en">
          Real Paraíso is located near km 24.1 of the Mérida–Progreso highway, approximately 3.2 km inland,
          in an area of existing and expanding developments, close to Autódromo Yucatán and with clear urban growth signals.
        </p>

        <div class="stats" style="margin-top:22px;">
          <div class="stat"><strong>21.1819052</strong><span>Latitude</span></div>
          <div class="stat"><strong>-89.6241033</strong><span>Longitude</span></div>
          <div class="stat"><strong data-lang="es">Zona en expansión</strong><strong data-lang="en">Growing corridor</strong><span data-lang="es">Desarrollo alrededor y conectividad estratégica</span><span data-lang="en">Surrounding development and strategic connectivity</span></div>
          <div class="stat"><strong data-lang="es">Lectura mixta</strong><strong data-lang="en">Mixed-use potential</strong><span data-lang="es">Desarrolladores + inversión patrimonial</span><span data-lang="en">Developers + patrimonial investment</span></div>
        </div>

        <div class="thumb-grid" style="margin-top:24px;">
          <img src="./zona-satelital.jpg" alt="Vista satelital" />
          <img src="./master-plan.jpg" alt="Plano ilustrativo" />
        </div>
      </div>

      <div class="location-map">
        <iframe class="map-frame" src="https://www.google.com/maps?q=21.1819052,-89.6241033&z=13&output=embed" loading="lazy"></iframe>
      </div>
    </div>
  </section>

  <section class="section" id="contacto">
    <div class="container contact-wrap">
      <div class="card contact-card pad">
        <div class="eyebrow">Contacto</div>
        <h2 style="font-size:clamp(34px,5vw,54px);margin-bottom:14px;" data-lang="es">Solicita información</h2>
        <h2 style="font-size:clamp(34px,5vw,54px);margin-bottom:14px;" data-lang="en">Request information</h2>

        <p data-lang="es">Cuéntanos si te interesan macro lotes, inversión patrimonial o información general del proyecto. El sistema está pensado para recibir tu solicitud y clasificarla automáticamente.</p>
        <p data-lang="en">Tell us whether you are interested in macro lots, patrimonial investment, or general project information. The system is designed to capture and classify your inquiry automatically.</p>

        <a class="contact-link" href="mailto:univeroyuc@gmail.com"><i>@</i><div><strong>Email</strong><div>univeroyuc@gmail.com</div></div></a>
        <a class="contact-link" target="_blank" rel="noopener" href="https://wa.me/529992227538?text=Hola,%20quiero%20informaci%C3%B3n%20de%20Real%20Para%C3%ADso"><i>W</i><div><strong>WhatsApp</strong><div>+52 999 222 7538</div></div></a>
        <div class="contact-link"><i>CRM</i><div><strong data-lang="es">Operación sugerida</strong><strong data-lang="en">Suggested operation</strong><div data-lang="es">Netlify Forms + HubSpot CRM + seguimiento por WhatsApp</div><div data-lang="en">Netlify Forms + HubSpot CRM + WhatsApp follow-up</div></div></div>
      </div>

      <div class="card pad">
        <div class="eyebrow">Formulario</div>

        <form name="real-paraiso-leads" method="POST" data-netlify="true" netlify-honeypot="bot-field">
          <input type="hidden" name="form-name" value="real-paraiso-leads" />
          <p style="display:none;"><label>Don’t fill this out: <input name="bot-field" /></label></p>

          <div class="field-grid">
            <input type="text" name="nombre" placeholder="Nombre / Name" required />
            <input type="text" name="telefono" placeholder="Teléfono / Phone" required />
          </div>

          <div class="field-grid">
            <input type="email" name="email" placeholder="Email" required />
            <input type="text" name="ciudad" placeholder="Ciudad / Country" />
          </div>

          <div class="field-grid">
            <select name="tipo_interes" required>
              <option value="">Tipo de interés / Interest type</option>
              <option>Macro lote / Macro lot</option>
              <option>Lote menor / Smaller lot</option>
              <option>Inversión general / General investment</option>
              <option>Información del proyecto / Project information</option>
            </select>

            <select name="lote_interes">
              <option value="">Lote de interés / Lot of interest</option>
              <option>LOTE 2.1</option>
              <option>LOTE 2.2</option>
              <option>LOTE 2.3</option>
              <option>LOTE 3.1</option>
              <option>LOTE 3.2</option>
              <option>LOTE 3.3</option>
            </select>
          </div>

          <textarea name="mensaje" placeholder="Cuéntanos qué estás buscando / Tell us what you're looking for"></textarea>

          <label style="display:flex;gap:10px;align-items:flex-start;font-size:14px;color:var(--muted);">
            <input type="checkbox" required style="width:auto;margin-top:4px;" />
            <span data-lang="es">Acepto ser contactado para recibir información de Real Paraíso.</span>
            <span data-lang="en">I agree to be contacted to receive information about Real Paraíso.</span>
          </label>

          <div class="btns">
            <button class="btn primary" type="submit"><span data-inline="es">Enviar solicitud</span><span data-inline="en">Send inquiry</span></button>
            <a class="btn secondary" target="_blank" rel="noopener" href="https://wa.me/529992227538?text=Hola,%20quiero%20informaci%C3%B3n%20de%20Real%20Para%C3%ADso">WhatsApp</a>
          </div>
        </form>
      </div>
    </div>
  </section>

  <footer class="footer">
    <div class="container footer-inner">
      <div>
        <strong>REAL PARAÍSO</strong>
        <div data-lang="es">Master plan inmobiliario | Mérida–Progreso</div>
        <div data-lang="en">Real estate master plan | Mérida–Progreso</div>
      </div>
      <div>univeroyuc@gmail.com · +52 999 222 7538</div>
    </div>
  </footer>

  <a class="wa-float" target="_blank" rel="noopener" href="https://wa.me/529992227538?text=Hola,%20quiero%20informaci%C3%B3n%20de%20Real%20Para%C3%ADso">WhatsApp</a>

  <script>
    const htmlEl = document.documentElement;
    const langEs = document.getElementById("langEs");
    const langEn = document.getElementById("langEn");

    function setLang(lang) {
      htmlEl.classList.remove("lang-es", "lang-en");
      htmlEl.classList.add("lang-" + lang);
      langEs.classList.toggle("active", lang === "es");
      langEn.classList.toggle("active", lang === "en");
      localStorage.setItem("realparaiso_lang", lang);
      const active = document.querySelector(".lot.active");
      if (active) renderLot(active.id);
    }

    langEs.onclick = () => setLang("es");
    langEn.onclick = () => setLang("en");
    setLang(localStorage.getItem("realparaiso_lang") || "es");

    const lots = {
      "lot-2-1": {
        name: "LOTE 2.1",
        size: "98,179 m²",
        copyEs: "Ideal para inversión estratégica o desarrollo por su escala, posición y lectura clara dentro del master plan.",
        copyEn: "Ideal for strategic investment or development due to its scale, position, and clear role inside the master plan.",
        badgesEs: ["Macro lote", "Desarrollo", "Escala estratégica"],
        badgesEn: ["Macro lot", "Development", "Strategic scale"]
      },
      "lot-2-2": {
        name: "LOTE 2.2",
        size: "100,884 m²",
        copyEs: "Superficie cercana a 10 hectáreas, con vocación clara para producto residencial, etapas o inversión de reserva.",
        copyEn: "Surface close to 10 hectares, well suited for residential product, phased development, or reserve investment.",
        badgesEs: ["10 ha aprox.", "Residencial", "Potencial de etapas"],
        badgesEn: ["Approx. 10 ha", "Residential", "Phased potential"]
      },
      "lot-2-3": {
        name: "LOTE 2.3",
        size: "100,196 m²",
        copyEs: "Una oportunidad balanceada para desarrolladores que busquen escala, flexibilidad y lectura comercial clara.",
        copyEn: "A balanced opportunity for developers seeking scale, flexibility, and clear commercial logic.",
        badgesEs: ["Macro lote", "Flexibilidad", "Inversión"],
        badgesEn: ["Macro lot", "Flexibility", "Investment"]
      },
      "lot-3-1": {
        name: "LOTE 3.1",
        size: "90,566 m²",
        copyEs: "La opción más compacta entre los macro lotes, ideal para un primer desarrollo o estrategia de entrada controlada.",
        copyEn: "The most compact of the macro lots, ideal for an initial development or a controlled entry strategy.",
        badgesEs: ["9 ha aprox.", "Entrada estratégica", "Desarrollo"],
        badgesEn: ["Approx. 9 ha", "Strategic entry", "Development"]
      },
      "lot-3-2": {
        name: "LOTE 3.2",
        size: "130,443 m²",
        copyEs: "La superficie más grande del master plan, con alto potencial para producto residencial o visión mixta de gran escala.",
        copyEn: "The largest surface in the master plan, with high potential for large-scale residential or mixed-use vision.",
        badgesEs: ["13 ha aprox.", "Gran escala", "Alto potencial"],
        badgesEn: ["Approx. 13 ha", "Large scale", "High potential"]
      },
      "lot-3-3": {
        name: "LOTE 3.3",
        size: "124,735 m²",
        copyEs: "Macro lote robusto para desarrolladores que buscan masa crítica, etapas y percepción premium desde el acceso.",
        copyEn: "A robust macro lot for developers seeking critical mass, phasing, and premium perception from the entrance boulevard.",
        badgesEs: ["12.4 ha aprox.", "Premium", "Constructoras"],
        badgesEn: ["Approx. 12.4 ha", "Premium", "Builders"]
      }
    };

    const lotName = document.getElementById("lot-name");
    const lotSize = document.getElementById("lot-size");
    const lotCopy = document.getElementById("lot-copy");
    const lotBadges = document.getElementById("lot-badges");
    const waLot = document.getElementById("wa-lot");

    function renderLot(id) {
      const currentLang = htmlEl.classList.contains("lang-en") ? "en" : "es";
      const data = lots[id];
      if (!data) return;

      document.querySelectorAll(".lot").forEach((el) => el.classList.remove("active"));
      document.getElementById(id).classList.add("active");

      lotName.textContent = data.name;
      lotSize.textContent = data.size;
      lotCopy.textContent = currentLang === "es" ? data.copyEs : data.copyEn;
      const badges = currentLang === "es" ? data.badgesEs : data.badgesEn;
      lotBadges.innerHTML = badges.map((b) => `<span class="badge">${b}</span>`).join("");
      waLot.href = `https://wa.me/529992227538?text=${encodeURIComponent("Hola, quiero información del " + data.name + " de Real Paraíso")}`;
    }

    document.querySelectorAll(".lot").forEach((el) => {
      el.addEventListener("mouseenter", () => renderLot(el.id));
      el.addEventListener("click", () => renderLot(el.id));
    });

    renderLot("lot-2-1");
  </script>
</body>
</html>
