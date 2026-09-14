<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Kallpa Biogás — Invierte en energía boliviana</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg-deep:#16302A;
    --bg-deep-2:#1F3D2B;
    --bg-cream:#F2ECDC;
    --green:#4C7A54;
    --green-light:#7FA37A;
    --amber:#D98C3D;
    --soil:#6B4226;
    --text-dark:#1B1F16;
    --text-light:#F2ECDC;
    --text-muted:#5C6A57;
    --line:rgba(242,236,220,0.16);
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Inter', sans-serif;
    color:var(--text-dark);
    background:var(--bg-cream);
    line-height:1.55;
    -webkit-font-smoothing:antialiased;
  }
  h1,h2,h3,.display{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    line-height:1.08;
    letter-spacing:-0.01em;
  }
  img,svg{display:block; max-width:100%;}
  a{color:inherit; text-decoration:none;}
  .wrap{
    max-width:1120px;
    margin:0 auto;
    padding:0 24px;
  }
  section{padding:88px 0;}
  @media (max-width:640px){ section{padding:56px 0;} }

  /* ---------- NAV ---------- */
  nav{
    position:sticky; top:0; z-index:50;
    background:var(--bg-deep);
    border-bottom:1px solid var(--line);
  }
  nav .wrap{
    display:flex; align-items:center; justify-content:space-between;
    padding-top:16px; padding-bottom:16px;
  }
  .logo{
    display:flex; align-items:center; gap:10px;
    color:var(--text-light);
    font-family:'Space Grotesk', sans-serif;
    font-weight:700;
    font-size:19px;
  }
  .logo svg{width:28px; height:28px;}
  .nav-cta{
    display:inline-flex; align-items:center; gap:8px;
    background:var(--amber);
    color:#1B1F16;
    padding:10px 18px;
    border-radius:3px;
    font-weight:600;
    font-size:14px;
  }
  .nav-cta:hover{background:#c97d2f;}

  /* ---------- HERO ---------- */
  .hero{
    background:linear-gradient(165deg, var(--bg-deep) 0%, var(--bg-deep-2) 100%);
    color:var(--text-light);
    padding:80px 0 100px;
    overflow:hidden;
  }
  .hero .wrap{
    display:grid;
    grid-template-columns:1.05fr 0.95fr;
    gap:56px;
    align-items:center;
  }
  @media (max-width:860px){
    .hero .wrap{grid-template-columns:1fr;}
    .hero{padding:56px 0 64px;}
  }
  .eyebrow-line{
    color:var(--green-light);
    font-size:15px;
    font-weight:500;
    margin-bottom:18px;
    max-width:34ch;
  }
  .hero h1{
    font-size:clamp(32px, 4.6vw, 50px);
    margin-bottom:22px;
  }
  .hero p.lead{
    font-size:17px;
    color:rgba(242,236,220,0.82);
    max-width:46ch;
    margin-bottom:34px;
  }
  .btn-row{display:flex; gap:14px; flex-wrap:wrap;}
  .btn{
    display:inline-flex; align-items:center; gap:9px;
    padding:14px 24px;
    border-radius:3px;
    font-weight:600;
    font-size:15px;
    border:1.5px solid transparent;
    cursor:pointer;
  }
  .btn-primary{background:var(--amber); color:#1B1F16;}
  .btn-primary:hover{background:#c97d2f;}
  .btn-outline{
    border-color:rgba(242,236,220,0.4);
    color:var(--text-light);
  }
  .btn-outline:hover{border-color:var(--text-light); background:rgba(242,236,220,0.06);}
  .hero-note{
    margin-top:22px;
    font-size:13px;
    color:rgba(242,236,220,0.55);
  }

  .diagram-box{
    background:rgba(242,236,220,0.04);
    border:1px solid var(--line);
    border-radius:6px;
    padding:24px;
  }
  .diagram-caption{
    display:flex; justify-content:space-between;
    margin-top:16px; font-size:12.5px;
    color:rgba(242,236,220,0.6);
  }

  /* ---------- PROBLEM ---------- */
  .problem .wrap{
    display:grid; grid-template-columns:1fr 1fr; gap:56px; align-items:start;
  }
  @media (max-width:860px){ .problem .wrap{grid-template-columns:1fr;} }
  .problem h2{font-size:clamp(26px,3.4vw,34px); margin-bottom:18px; color:var(--text-dark);}
  .problem p{color:var(--text-muted); font-size:15.5px; margin-bottom:14px; max-width:52ch;}
  .callout{
    border-left:3px solid var(--soil);
    background:#fff;
    padding:26px 28px;
    border-radius:2px;
  }
  .callout p{color:var(--text-dark); font-size:15.5px; margin:0;}
  .callout strong{color:var(--soil);}

  /* ---------- SOLUTION ---------- */
  .solution{background:var(--bg-deep-2); color:var(--text-light);}
  .solution h2{font-size:clamp(26px,3.4vw,34px); max-width:20ch; margin-bottom:48px;}
  .sol-grid{
    display:grid; grid-template-columns:repeat(3,1fr); gap:36px;
  }
  @media (max-width:860px){ .sol-grid{grid-template-columns:1fr;} }
  .sol-card svg{width:40px; height:40px; margin-bottom:18px;}
  .sol-card h3{font-size:19px; margin-bottom:10px; color:var(--text-light);}
  .sol-card p{font-size:14.5px; color:rgba(242,236,220,0.72);}

  /* ---------- HOW IT WORKS ---------- */
  .steps h2{font-size:clamp(26px,3.4vw,34px); margin-bottom:44px; max-width:24ch;}
  .step-list{
    display:grid; grid-template-columns:repeat(4,1fr); gap:0;
    border-top:1px solid #d9d0b6;
  }
  @media (max-width:860px){ .step-list{grid-template-columns:1fr;} }
  .step{
    padding:26px 20px 26px 0;
    border-right:1px solid #d9d0b6;
  }
  .step-list .step:last-child{border-right:none;}
  @media (max-width:860px){
    .step{border-right:none; border-bottom:1px solid #d9d0b6; padding:22px 0;}
  }
  .step .num{
    font-family:'Space Grotesk', sans-serif;
    font-weight:700; font-size:26px;
    color:var(--green);
    margin-bottom:10px;
    display:block;
  }
  .step h3{font-size:15.5px; font-weight:600; margin-bottom:8px; font-family:'Inter';}
  .step p{font-size:13.8px; color:var(--text-muted);}

  /* ---------- PACKAGES ---------- */
  .packages{background:var(--bg-deep); color:var(--text-light);}
  .packages h2{font-size:clamp(26px,3.4vw,34px); margin-bottom:10px;}
  .packages > .wrap > p.sub{color:rgba(242,236,220,0.65); font-size:15px; margin-bottom:44px; max-width:56ch;}
  .pkg-grid{
    display:grid; grid-template-columns:repeat(4, 1fr); gap:20px; align-items:stretch;
  }
  @media (max-width:960px){ .pkg-grid{grid-template-columns:1fr 1fr;} }
  @media (max-width:600px){ .pkg-grid{grid-template-columns:1fr;} }
  .pkg{
    background:rgba(242,236,220,0.03);
    border:1px solid var(--line);
    border-left:3px solid var(--green-light);
    border-radius:3px;
    padding:26px 22px;
    display:flex; flex-direction:column;
  }
  .pkg.featured{
    border-left:3px solid var(--amber);
    background:rgba(217,140,61,0.07);
    padding-top:22px;
  }
  .pkg-tag{
    font-size:12px; color:var(--amber); font-weight:600; margin-bottom:12px;
  }
  .pkg h3{font-family:'Space Grotesk'; font-size:20px; margin-bottom:4px; color:var(--text-light);}
  .pkg .range{font-size:13.5px; color:rgba(242,236,220,0.6); margin-bottom:18px;}
  .pkg .rate{
    font-family:'Space Grotesk'; font-weight:700; font-size:30px; color:var(--text-light);
    margin-bottom:2px;
  }
  .pkg .rate-label{font-size:12.5px; color:rgba(242,236,220,0.55); margin-bottom:20px;}
  .pkg ul{list-style:none; font-size:13.8px; color:rgba(242,236,220,0.82); flex:1;}
  .pkg li{padding:6px 0 6px 18px; position:relative;}
  .pkg li::before{
    content:"";
    position:absolute; left:0; top:13px;
    width:6px; height:6px; border-radius:50%;
    background:var(--green-light);
  }
  .pkg.featured li::before{background:var(--amber);}
  .pkg .pkg-btn{
    margin-top:20px;
    text-align:center;
    padding:11px;
    border-radius:3px;
    border:1px solid rgba(242,236,220,0.35);
    font-size:13.8px; font-weight:600;
  }
  .pkg.featured .pkg-btn{background:var(--amber); color:#1B1F16; border-color:var(--amber);}
  .pkg .pkg-btn:hover{background:rgba(242,236,220,0.08);}
  .pkg.featured .pkg-btn:hover{background:#c97d2f;}
  .disclaimer{margin-top:30px; font-size:12.5px; color:rgba(242,236,220,0.45); max-width:70ch;}

  /* ---------- FINAL CTA ---------- */
  .final-cta{
    background:var(--bg-cream);
    text-align:left;
  }
  .final-cta .box{
    background:#fff;
    border:1px solid #e3dcc4;
    border-radius:6px;
    padding:48px;
    display:grid; grid-template-columns:1.3fr 0.7fr; gap:32px; align-items:center;
  }
  @media (max-width:760px){
    .final-cta .box{grid-template-columns:1fr; padding:32px 24px; text-align:left;}
  }
  .final-cta h2{font-size:clamp(24px,3vw,30px); margin-bottom:10px;}
  .final-cta p{color:var(--text-muted); font-size:15px; max-width:48ch;}
  .final-cta .btn{justify-self:end; width:100%; justify-content:center;}
  @media (max-width:760px){ .final-cta .btn{justify-self:start; width:auto;} }

  /* ---------- FOOTER ---------- */
  footer{background:#0F231D; color:rgba(242,236,220,0.6); padding:44px 0 30px;}
  footer .wrap{
    display:flex; justify-content:space-between; flex-wrap:wrap; gap:20px;
    font-size:13.5px;
  }
  footer .logo{color:var(--text-light); margin-bottom:10px;}
  footer .col h4{color:var(--text-light); font-size:13px; margin-bottom:10px; font-weight:600;}
  footer .col p, footer .col a{display:block; font-size:13.5px; margin-bottom:6px;}

  /* ---------- WHATSAPP FLOATING BUTTON ---------- */
  .wa-float{
    position:fixed; bottom:22px; right:22px; z-index:60;
    display:flex; align-items:center; gap:10px;
    background:#25D366; color:#0b2013;
    padding:13px 18px 13px 14px;
    border-radius:30px;
    box-shadow:0 6px 20px rgba(0,0,0,0.25);
    font-weight:600; font-size:14px;
    animation:wa-pulse 2.6s ease-in-out infinite;
  }
  .wa-float svg{width:22px; height:22px;}
  @keyframes wa-pulse{
    0%,100%{box-shadow:0 6px 20px rgba(0,0,0,0.25), 0 0 0 0 rgba(37,211,102,0.5);}
    50%{box-shadow:0 6px 20px rgba(0,0,0,0.25), 0 0 0 10px rgba(37,211,102,0);}
  }
  @media (max-width:600px){
    .wa-float span{display:none;}
    .wa-float{padding:14px; border-radius:50%;}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap">
    <div class="logo">
      <svg viewBox="0 0 24 24" fill="none"><path d="M12 2c2 4 5 6.5 5 10.5A5 5 0 0 1 7 12.5C7 8.5 10 6 12 2Z" fill="#D98C3D"/><path d="M8 21c0-3 1.8-5 4-6 2.2 1 4 3 4 6H8Z" fill="#4C7A54"/></svg>
      Kallpa Biogás
    </div>
    <a class="nav-cta" href="https://wa.me/59162468066?text=Hola%2C%20quiero%20invertir%20en%20Kallpa%20Bioga%CC%81s" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" width="16" height="16" fill="#1B1F16"><path d="M12 2C6.5 2 2 6.3 2 11.6c0 1.9.6 3.7 1.6 5.2L2 22l5.4-1.4c1.5.8 3.2 1.2 4.9 1.2 5.5 0 10-4.3 10-9.6C22.3 6.4 17.8 2 12 2Zm5.7 13.6c-.2.6-1.3 1.2-1.8 1.3-.5.1-1.1.1-1.7-.1-.4-.1-.9-.3-1.6-.6-2.7-1.2-4.5-3.9-4.6-4.1-.1-.2-1.1-1.5-1.1-2.8 0-1.3.7-2 .9-2.2.2-.2.5-.3.7-.3h.5c.2 0 .4 0 .6.5.2.6.7 1.9.8 2 .1.2.1.3 0 .5-.1.2-.1.3-.3.5-.1.2-.3.4-.4.5-.2.2-.3.4-.1.7.2.3.8 1.3 1.8 2.1 1.2 1.1 2.2 1.4 2.6 1.6.3.1.5.1.6-.1.2-.2.7-.8.9-1.1.2-.3.4-.2.6-.1.2.1 1.5.7 1.7.8.2.1.4.2.4.3.1.2.1.7-.1 1.3Z"/></svg>
      WhatsApp
    </a>
  </div>
</nav>

<header class="hero">
  <div class="wrap">
    <div>
      <p class="eyebrow-line">Bolivia recorta la subvención a los combustibles año tras año.</p>
      <h1>El biogás no necesita subsidio. Se produce en la comunidad y no se acaba.</h1>
      <p class="lead">Invierte desde 1 dólar en biodigestores que transforman estiércol y residuos orgánicos en energía y en abono. Menos dependencia del GLP y el diésel, más ingresos para quien produce.</p>
      <div class="btn-row">
        <a class="btn btn-primary" href="#paquetes">Invertir desde $1</a>
        <a class="btn btn-outline" href="https://wa.me/59162468066?text=Hola%2C%20quiero%20informaci%C3%B3n%20sobre%20Kallpa%20Bioga%CC%81s" target="_blank" rel="noopener">Hablar por WhatsApp</a>
      </div>
      <p class="hero-note">Sin monto mínimo alto, sin letra chica. Reportes de producción cada mes.</p>
    </div>

    <div class="diagram-box">
      <svg viewBox="0 0 380 300" width="100%">
        <!-- residuos -->
        <g>
          <rect x="14" y="200" width="60" height="42" rx="4" fill="#6B4226" opacity="0.85"/>
          <text x="44" y="258" text-anchor="middle" font-family="Inter" font-size="11" fill="#D9D0B6">Residuos</text>
          <text x="44" y="270" text-anchor="middle" font-family="Inter" font-size="11" fill="#D9D0B6">orgánicos</text>
        </g>
        <!-- arrow to tank -->
        <path d="M78 220 H130" stroke="#7FA37A" stroke-width="2" marker-end="url(#arrow)"/>
        <!-- biodigestor tank -->
        <g>
          <ellipse cx="190" cy="150" rx="52" ry="18" fill="#4C7A54"/>
          <rect x="138" y="150" width="104" height="90" fill="#4C7A54"/>
          <ellipse cx="190" cy="240" rx="52" ry="18" fill="#3d6444"/>
          <ellipse cx="190" cy="150" rx="52" ry="18" fill="none" stroke="#2f5236" stroke-width="2"/>
          <text x="190" y="200" text-anchor="middle" font-family="Space Grotesk" font-weight="700" font-size="13" fill="#F2ECDC">Biodigestor</text>
        </g>
        <!-- arrow to flame -->
        <path d="M242 160 C 280 150, 290 110, 300 90" stroke="#D98C3D" stroke-width="2" fill="none" marker-end="url(#arrowAmber)"/>
        <g transform="translate(288,40)">
          <path d="M18 2c4 8 10 13 10 21a10 10 0 0 1-20 0C8 15 14 10 18 2Z" fill="#D98C3D"/>
          <path d="M18 34c-6 0-11-4-11-11 0 5 3 7 6 7-1-3 1-5 2-8 2 4 5 5 5 9s-1 3-2 3Z" fill="#F2ECDC"/>
          <text x="18" y="56" text-anchor="middle" font-family="Inter" font-weight="600" font-size="12" fill="#F2ECDC">Biogás</text>
        </g>
        <!-- arrow to abono -->
        <path d="M242 220 C 280 230, 290 250, 300 258" stroke="#B98A57" stroke-width="2" fill="none" marker-end="url(#arrowSoil)"/>
        <g transform="translate(285,258)">
          <ellipse cx="18" cy="18" rx="20" ry="12" fill="#6B4226"/>
          <path d="M10 12c3-6 9-8 15-6-2 5-8 8-15 6Z" fill="#7FA37A"/>
          <text x="18" y="44" text-anchor="middle" font-family="Inter" font-weight="600" font-size="12" fill="#F2ECDC">Abono</text>
        </g>
        <defs>
          <marker id="arrow" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#7FA37A"/></marker>
          <marker id="arrowAmber" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#D98C3D"/></marker>
          <marker id="arrowSoil" markerWidth="8" markerHeight="8" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 Z" fill="#B98A57"/></marker>
        </defs>
      </svg>
      <div class="diagram-caption">
        <span>Entrada: materia orgánica</span>
        <span>Salida: energía + fertilizante</span>
      </div>
    </div>
  </div>
</header>

<section class="problem">
  <div class="wrap">
    <div>
      <h2>Lo que está pasando con el subsidio</h2>
      <p>Bolivia ha reducido de forma gradual la subvención a los combustibles líquidos, mientras la producción interna de gas natural cae y el país depende cada vez más de importaciones pagadas en dólares. El resultado ya se siente: filas para cargar diésel, gasolina más cara y un GLP doméstico e industrial bajo presión.</p>
      <p>Para el agro, el transporte de carga y las familias que cocinan con garrafa, eso significa costos que suben sin aviso y sin control propio.</p>
    </div>
    <div class="callout">
      <p><strong>El biogás rompe esa dependencia.</strong> Se produce con lo que ya existe en el campo —estiércol, restos de cosecha, residuos orgánicos— y no depende de una política de subvención, del precio internacional del petróleo ni de una fila en el surtidor. Lo que se invierte hoy en un biodigestor genera energía y abono de forma continua, sin esperar a que el Estado decida cuánto subsidiar.</p>
    </div>
  </div>
</section>

<section class="solution">
  <div class="wrap">
    <h2>Una respuesta con tres beneficios, no solo uno</h2>
    <div class="sol-grid">
      <div class="sol-card">
        <svg viewBox="0 0 24 24" fill="none"><path d="M12 2c2 4 5 6.5 5 10.5A5 5 0 0 1 7 12.5C7 8.5 10 6 12 2Z" fill="#D98C3D"/></svg>
        <h3>Energía que no depende del surtidor</h3>
        <p>El biogás sustituye GLP y diésel en cocinas, motores y generadores de la propia comunidad productora, con un costo que no sube por decreto.</p>
      </div>
      <div class="sol-card">
        <svg viewBox="0 0 24 24" fill="none"><rect x="4" y="4" width="16" height="16" rx="2" fill="#7FA37A"/><path d="M8 12h8M12 8v8" stroke="#16302A" stroke-width="1.6"/></svg>
        <h3>Un ingreso que no depende del clima político</h3>
        <p>Tu aporte financia infraestructura física que sigue produciendo mientras haya residuos orgánicos que procesar, sin importar qué pase con la subvención.</p>
      </div>
      <div class="sol-card">
        <svg viewBox="0 0 24 24" fill="none"><ellipse cx="12" cy="12" rx="9" ry="6" fill="#6B4226"/><path d="M6 12c2-4 6-5 10-4-1.5 3-6 5-10 4Z" fill="#7FA37A"/></svg>
        <h3>Abono orgánico, no solo energía</h3>
        <p>El biol y el bioabono que resultan del proceso vuelven al productor y reemplazan fertilizante químico importado, cada vez más caro en dólares.</p>
      </div>
    </div>
  </div>
</section>

<section class="steps">
  <div class="wrap">
    <h2>Cómo se mueve tu inversión</h2>
    <div class="step-list">
      <div class="step">
        <span class="num">01</span>
        <h3>Elegís tu paquete</h3>
        <p>Desde 1 dólar hasta aportes institucionales, según cuánto querés comprometer.</p>
      </div>
      <div class="step">
        <span class="num">02</span>
        <h3>Se financia un biodigestor</h3>
        <p>El aporte se destina a construir u operar una planta comunitaria ya identificada.</p>
      </div>
      <div class="step">
        <span class="num">03</span>
        <h3>La planta produce</h3>
        <p>Biogás para uso y venta local, y biol/bioabono para los productores de la zona.</p>
      </div>
      <div class="step">
        <span class="num">04</span>
        <h3>Recibís tu retorno</h3>
        <p>En efectivo, en abono, o en ambos, según el paquete y con reporte periódico.</p>
      </div>
    </div>
  </div>
</section>

<section class="packages" id="paquetes">
  <div class="wrap">
    <h2>Paquetes de inversión</h2>
    <p class="sub">Todos parten desde 1 dólar. Cuanto mayor el compromiso, mayor la participación en la producción de abono y en el retorno estimado.</p>
    <div class="pkg-grid">
      <div class="pkg">
        <div class="pkg-tag">Ch'ipa · Semilla</div>
        <h3>Semilla</h3>
        <div class="range">Desde $1 hasta $49</div>
        <div class="rate">6%</div>
        <div class="rate-label">retorno anual estimado</div>
        <ul>
          <li>Reporte trimestral de producción</li>
          <li>Acceso a la comunidad de inversores</li>
          <li>Ideal para probar el modelo</li>
        </ul>
        <a class="pkg-btn" href="https://wa.me/59162468066?text=Quiero%20el%20paquete%20Semilla" target="_blank" rel="noopener">Elegir Semilla</a>
      </div>
      <div class="pkg">
        <div class="pkg-tag">Saphi · Raíz</div>
        <h3>Raíz</h3>
        <div class="range">De $50 a $499</div>
        <div class="rate">9%</div>
        <div class="rate-label">retorno anual estimado</div>
        <ul>
          <li>10 kg de abono orgánico al año</li>
          <li>Reporte mensual</li>
          <li>Prioridad en próximas plantas</li>
        </ul>
        <a class="pkg-btn" href="https://wa.me/59162468066?text=Quiero%20el%20paquete%20Ra%C3%ADz" target="_blank" rel="noopener">Elegir Raíz</a>
      </div>
      <div class="pkg featured">
        <div class="pkg-tag">Pallay · Cosecha — recomendado</div>
        <h3>Cosecha</h3>
        <div class="range">De $500 a $4,999</div>
        <div class="rate">12%</div>
        <div class="rate-label">retorno anual estimado</div>
        <ul>
          <li>50 kg de abono orgánico al año</li>
          <li>Biodigestor más cercano a tu zona</li>
          <li>Asesor asignado por WhatsApp</li>
        </ul>
        <a class="pkg-btn" href="https://wa.me/59162468066?text=Quiero%20el%20paquete%20Cosecha" target="_blank" rel="noopener">Elegir Cosecha</a>
      </div>
      <div class="pkg">
        <div class="pkg-tag">Kallpa Pro · Institucional</div>
        <h3>Kallpa Pro</h3>
        <div class="range">Desde $5,000</div>
        <div class="rate">15%</div>
        <div class="rate-label">retorno anual estimado</div>
        <ul>
          <li>Abono orgánico a granel</li>
          <li>Copropiedad del biodigestor</li>
          <li>Visita guiada a planta y auditoría</li>
        </ul>
        <a class="pkg-btn" href="https://wa.me/59162468066?text=Quiero%20el%20paquete%20Kallpa%20Pro" target="_blank" rel="noopener">Elegir Kallpa Pro</a>
      </div>
    </div>
    <p class="disclaimer">Los porcentajes de retorno son estimados y no garantizados: dependen de la producción real de biogás y abono, y del precio al que se comercialicen. Esta página es informativa y no constituye asesoría financiera. Revisa las condiciones completas antes de invertir.</p>
  </div>
</section>

<section class="final-cta">
  <div class="wrap">
    <div class="box">
      <div>
        <h2>Tu primer dólar puede empezar esto</h2>
        <p>No hace falta ser una empresa grande ni tener un biodigestor propio. Escríbenos por WhatsApp y te explicamos, paso por paso, en qué planta entra tu aporte.</p>
      </div>
      <a class="btn btn-primary" href="https://wa.me/59162468066?text=Hola%2C%20quiero%20empezar%20a%20invertir%20en%20Kallpa%20Bioga%CC%81s" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" width="16" height="16" fill="#1B1F16"><path d="M12 2C6.5 2 2 6.3 2 11.6c0 1.9.6 3.7 1.6 5.2L2 22l5.4-1.4c1.5.8 3.2 1.2 4.9 1.2 5.5 0 10-4.3 10-9.6C22.3 6.4 17.8 2 12 2Zm5.7 13.6c-.2.6-1.3 1.2-1.8 1.3-.5.1-1.1.1-1.7-.1-.4-.1-.9-.3-1.6-.6-2.7-1.2-4.5-3.9-4.6-4.1-.1-.2-1.1-1.5-1.1-2.8 0-1.3.7-2 .9-2.2.2-.2.5-.3.7-.3h.5c.2 0 .4 0 .6.5.2.6.7 1.9.8 2 .1.2.1.3 0 .5-.1.2-.1.3-.3.5-.1.2-.3.4-.4.5-.2.2-.3.4-.1.7.2.3.8 1.3 1.8 2.1 1.2 1.1 2.2 1.4 2.6 1.6.3.1.5.1.6-.1.2-.2.7-.8.9-1.1.2-.3.4-.2.6-.1.2.1 1.5.7 1.7.8.2.1.4.2.4.3.1.2.1.7-.1 1.3Z"/></svg>
        Escribir por WhatsApp
      </a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div class="col">
      <div class="logo">Kallpa Biogás</div>
      <p>Energía que nace de la tierra boliviana.</p>
    </div>
    <div class="col">
      <h4>Contacto</h4>
      <a href="https://wa.me/59162468066" target="_blank" rel="noopener">WhatsApp: 624 68066</a>
      <p>Bolivia</p>
    </div>
    <div class="col">
      <h4>Aviso</h4>
      <p style="max-width:32ch;">Toda inversión conlleva riesgo. Los retornos mostrados son estimados.</p>
    </div>
  </div>
</footer>

<a class="wa-float" href="https://wa.me/59162468066?text=Hola%2C%20quiero%20informaci%C3%B3n%20sobre%20Kallpa%20Bioga%CC%81s" target="_blank" rel="noopener">
  <svg viewBox="0 0 24 24" fill="#0b2013"><path d="M12 2C6.5 2 2 6.3 2 11.6c0 1.9.6 3.7 1.6 5.2L2 22l5.4-1.4c1.5.8 3.2 1.2 4.9 1.2 5.5 0 10-4.3 10-9.6C22.3 6.4 17.8 2 12 2Zm5.7 13.6c-.2.6-1.3 1.2-1.8 1.3-.5.1-1.1.1-1.7-.1-.4-.1-.9-.3-1.6-.6-2.7-1.2-4.5-3.9-4.6-4.1-.1-.2-1.1-1.5-1.1-2.8 0-1.3.7-2 .9-2.2.2-.2.5-.3.7-.3h.5c.2 0 .4 0 .6.5.2.6.7 1.9.8 2 .1.2.1.3 0 .5-.1.2-.1.3-.3.5-.1.2-.3.4-.4.5-.2.2-.3.4-.1.7.2.3.8 1.3 1.8 2.1 1.2 1.1 2.2 1.4 2.6 1.6.3.1.5.1.6-.1.2-.2.7-.8.9-1.1.2-.3.4-.2.6-.1.2.1 1.5.7 1.7.8.2.1.4.2.4.3.1.2.1.7-.1 1.3Z"/></svg>
  <span>WhatsApp</span>
</a>

</body>
</html>
