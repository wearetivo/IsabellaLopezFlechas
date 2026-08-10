<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Isabella López Flechas · XV Años</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,700;1,600;1,700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --accent:#4a90e2;
    --accent-dark:#3a73b8;
    --accent-light:#87b8eb;
    --text:#1c1917;
    --muted:#6b7280;
    --surface:#ffffff;
    --shadow-card: 0 10px 15px -3px rgba(0,0,0,.10), 0 4px 6px -2px rgba(0,0,0,.05), 0 0 0 1px rgba(74,144,226,.06), 0 0 100px 0 rgba(74,144,226,.30);
    --shadow-btn: 0 10px 28px -10px rgba(74,144,226,.6), 0 2px 4px -2px rgba(0,0,0,.08);
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:'Poppins', sans-serif;
    color:var(--text);
    background:linear-gradient(180deg,#f6d9e6 0%, #e9d9f2 45%, #f3d3e3 100%);
  }
  h1,h2,h3,.serif{font-family:'Playfair Display', serif;}
  img{max-width:100%; display:block;}
  .wrap{ max-width:900px; margin:0 auto; padding:0 20px;}
  .section-pad{ padding-top:56px;}

  /* ===== HERO ===== */
  .hero{
    position:relative;
    height:100svh;
    min-height:560px;
    background:
      linear-gradient(rgba(0,0,0,.32), rgba(0,0,0,.32)),
      radial-gradient(120% 90% at 20% 10%, #6f7fb0 0%, #384164 55%, #1d2338 100%);
    display:flex; align-items:center; justify-content:center;
    color:#fff; text-align:center; padding:40px;
    overflow:hidden;
  }
  .hero-frame{
    position:absolute; inset:16px;
    border:1px solid rgba(255,255,255,.8);
    pointer-events:none;
  }
  .hero-frame::before, .hero-frame::after,
  .hero-corners span{ content:""; }
  .hero-corners{ position:absolute; inset:26px; pointer-events:none;}
  .hero-corners span{ position:absolute; width:22px; height:22px; border-color:rgba(255,255,255,.9); border-style:solid; border-width:0;}
  .c-tl{ top:0; left:0; border-top-width:2px; border-left-width:2px;}
  .c-tr{ top:0; right:0; border-top-width:2px; border-right-width:2px;}
  .c-bl{ bottom:0; left:0; border-bottom-width:2px; border-left-width:2px;}
  .c-br{ bottom:0; right:0; border-bottom-width:2px; border-right-width:2px;}
  .hero-inner{ position:relative; z-index:2; max-width:640px;}
  .hero-icon{ font-size:2.2rem; margin-bottom:14px; opacity:.95;}
  .hero h1{
    font-size:clamp(2.2rem, 6.5vw, 4rem);
    font-weight:700; line-height:1.15;
    text-shadow:0 1px 2px rgba(0,0,0,.4), 0 2px 6px rgba(0,0,0,.3);
  }

  /* ===== COUNTDOWN ===== */
  .countdown-band{
    width:100%;
    background:linear-gradient(135deg, rgba(74,144,226,.10), rgba(74,144,226,.16));
    padding:32px 20px;
    text-align:center;
  }
  .countdown-band h3{
    font-family:'Poppins',sans-serif; font-weight:500; font-size:1.4rem; margin-bottom:20px; color:#111;
  }
  .countdown-grid{ display:flex; justify-content:center; gap:16px; flex-wrap:wrap; max-width:640px; margin:0 auto;}
  .cd-unit{ display:flex; flex-direction:column; align-items:center;}
  .cd-pill{
    background:var(--accent);
    color:#fff; border-radius:16px;
    padding:12px 20px; min-width:74px; text-align:center;
    box-shadow:0 4px 10px rgba(74,144,226,.35);
  }
  .cd-pill .n{ font-size:1.9rem; font-weight:700; font-variant-numeric: tabular-nums;}
  .cd-unit .lbl{ margin-top:8px; font-size:.8rem; color:#333;}

  /* ===== CARD (reusable) ===== */
  .card{
    position:relative;
    background:var(--surface);
    border-radius:20px;
    padding:44px 30px 34px;
    box-shadow:var(--shadow-card);
    margin-top:70px;
  }
  .badge{
    position:absolute; top:-26px; left:30px;
    width:52px; height:52px; border-radius:50%;
    background:linear-gradient(135deg, var(--accent), var(--accent-dark));
    display:flex; align-items:center; justify-content:center;
    font-size:1.4rem; box-shadow:0 8px 18px rgba(74,144,226,.4);
  }
  .card h3.title{
    font-size:1.4rem; font-weight:700; color:#1c1917; margin-bottom:16px;
    display:flex; align-items:center; gap:8px;
  }
  .card h3.title .ic{ color:var(--accent); font-size:1.1rem;}

  /* content / message */
  .message-card p{ color:#374151; line-height:1.9; font-size:1rem;}
  .message-card p + p{ margin-top:16px;}

  /* gallery */
  .gallery-stack{ display:flex; flex-direction:column; align-items:center; padding-top:6px;}
  .polaroid{
    width:70%; max-width:280px; background:#fff; padding:10px 10px 34px;
    border-radius:6px; box-shadow:0 2px 4px rgba(0,0,0,.08), 0 12px 28px -8px rgba(0,0,0,.3);
    margin-top:-14%;
    font-family:'Playfair Display', serif; font-style:italic; text-align:center; color:#78716c; font-size:.85rem;
  }
  .polaroid:first-child{ margin-top:0; align-self:flex-start; transform:rotate(-3deg);}
  .polaroid:nth-child(2){ align-self:flex-end; transform:rotate(2.5deg);}
  .polaroid:nth-child(3){ align-self:flex-start; transform:rotate(-2deg);}
  .polaroid:nth-child(4){ align-self:flex-end; transform:rotate(3deg);}
  .polaroid:nth-child(5){ align-self:flex-start; transform:rotate(-2.5deg);}
  .polaroid .ph{
    aspect-ratio:4/5; border-radius:3px;
    background:linear-gradient(150deg,#f0e4ee,#dbe6f7);
    display:flex; align-items:center; justify-content:center;
    color:#9ca3af; font-family:'Poppins',sans-serif; font-style:normal; font-size:.72rem;
  }

  /* date/location rows */
  .info-row{ display:flex; gap:14px; align-items:flex-start; margin-bottom:16px;}
  .info-row .dot-ic{
    width:34px; height:34px; border-radius:50%; background:rgba(74,144,226,.15);
    display:flex; align-items:center; justify-content:center; flex-shrink:0; font-size:1rem;
  }
  .info-row .label{ font-size:.75rem; text-transform:uppercase; letter-spacing:.08em; color:var(--accent); font-weight:600; margin-bottom:2px;}
  .info-row .value{ font-size:1.05rem; font-weight:500; color:#1c1917;}
  .info-row .sub{ font-size:.82rem; color:var(--muted); margin-top:2px;}

  .btn{
    display:flex; align-items:center; justify-content:center; gap:8px;
    width:100%; margin-top:14px; padding:14px 20px; border-radius:100px;
    background:linear-gradient(135deg, var(--accent), var(--accent-dark));
    color:#fff; text-decoration:none; border:none; cursor:pointer;
    font-family:'Poppins'; font-weight:600; font-size:.95rem;
    box-shadow:var(--shadow-btn);
  }

  /* dresscode */
  .dresscode-photo{
    width:170px; margin:20px auto 0; background:#fff; padding:8px 8px 6px;
    border-radius:4px; box-shadow:0 10px 20px rgba(0,0,0,.15); transform:rotate(-2deg);
  }
  .dresscode-photo .ph{ aspect-ratio:3/4; border-radius:2px; background:linear-gradient(150deg,#dbe6f7,#f0e4ee); display:flex; align-items:center; justify-content:center; color:#9ca3af; font-size:.7rem;}
  .swatches{ display:flex; gap:10px; justify-content:center; margin-top:20px;}
  .swatch{ width:34px; height:34px; border-radius:50%; box-shadow:0 0 0 1px rgba(0,0,0,.08), 0 3px 8px rgba(0,0,0,.12);}

  /* RSVP */
  form{ display:flex; flex-direction:column; gap:16px; margin-top:6px;}
  label{ font-size:.86rem; font-weight:500; color:#374151; margin-bottom:6px; display:block;}
  input, select{
    width:100%; padding:12px 14px; border-radius:12px; border:2px solid #e7e5e4;
    background:#fafaf9; font-family:'Poppins'; font-size:.95rem; color:#1c1917;
  }
  input:focus, select:focus{ outline:none; border-color:var(--accent);}
  .attend-toggle{ display:grid; grid-template-columns:1fr 1fr; gap:12px;}
  .attend-btn{
    display:flex; flex-direction:column; align-items:center; gap:6px;
    padding:14px 10px; border-radius:16px; border:2px solid #e7e5e4; background:#fff;
    cursor:pointer; font-family:'Poppins'; font-weight:600; font-size:.85rem; color:#57534e;
    transition:.15s;
  }
  .attend-btn .circle{ width:30px; height:30px; border-radius:50%; background:#f3f4f6; display:flex; align-items:center; justify-content:center; font-size:.9rem;}
  .attend-btn.active{ border-color:var(--accent); background:rgba(74,144,226,.08); color:var(--accent);}
  .attend-btn.active .circle{ background:linear-gradient(135deg,var(--accent),var(--accent-dark)); color:#fff;}
  .rsvp-status{ text-align:center; font-size:.88rem; color:var(--accent-dark); min-height:1.2em; font-weight:500;}

  /* footer */
  footer{ text-align:center; padding:70px 20px 40px;}
  footer .flower{ font-size:1.8rem; margin-bottom:14px;}
  footer p{ color:#57534e; font-style:italic; font-family:'Playfair Display', serif; font-size:1.1rem;}
  footer .fine{ margin-top:26px; font-size:.72rem; color:#a8a29e; font-style:normal; font-family:'Poppins';}

  @media (max-width:480px){
    .polaroid{ width:78%; }
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-frame"></div>
  <div class="hero-corners">
    <span class="c-tl"></span><span class="c-tr"></span><span class="c-bl"></span><span class="c-br"></span>
  </div>
  <div class="hero-inner">
    <div class="hero-icon">💐</div>
    <h1>Isabella López Flechas</h1>
  </div>
</div>

<!-- COUNTDOWN -->
<div class="countdown-band">
  <h3>✨ Cuenta Regresiva ✨</h3>
  <div class="countdown-grid">
    <div class="cd-unit"><div class="cd-pill"><span class="n" id="cd-days">00</span></div><div class="lbl">Días</div></div>
    <div class="cd-unit"><div class="cd-pill"><span class="n" id="cd-hours">00</span></div><div class="lbl">Horas</div></div>
    <div class="cd-unit"><div class="cd-pill"><span class="n" id="cd-mins">00</span></div><div class="lbl">Minutos</div></div>
    <div class="cd-unit"><div class="cd-pill"><span class="n" id="cd-secs">00</span></div><div class="lbl">Segundos</div></div>
  </div>
</div>

<div class="wrap section-pad">

  <!-- WELCOME MESSAGE -->
  <div class="card message-card">
    <p>Su mamá, Johana Flechas Palomino, tiene el gusto de invitarte a celebrar los 15 años de su princesa. Te esperamos con mucha alegría.</p>
    <p>Hoy comienza una nueva etapa en mi vida, llena de sueños, ilusiones y nuevos caminos por recorrer. Miro hacia atrás con un corazón agradecido por cada abrazo, cada enseñanza y cada persona que ha hecho parte de mi historia.</p>
    <p>Cada sonrisa, cada consejo y cada momento compartido han dejado huellas que llevaré siempre conmigo. Gracias por acompañarme a crecer y por hacer de estos primeros quince años un tiempo tan especial.</p>
  </div>

  <!-- GALLERY -->
  <div class="card">
    <div class="badge">🖼️</div>
    <h3 class="title">Recuerdos Inolvidables</h3>
    <div class="gallery-stack">
      <div class="polaroid"><div class="ph">Añade tu foto</div></div>
      <div class="polaroid"><div class="ph">Añade tu foto</div></div>
      <div class="polaroid"><div class="ph">Añade tu foto</div></div>
      <div class="polaroid"><div class="ph">Añade tu foto</div></div>
      <div class="polaroid"><div class="ph">Añade tu foto</div></div>
    </div>
  </div>

  <!-- DATE -->
  <div class="card">
    <div class="badge">📅</div>
    <h3 class="title">Fecha y Hora</h3>
    <div class="info-row">
      <div class="dot-ic">📅</div>
      <div><div class="value">Sábado, 12 de septiembre de 2026</div></div>
    </div>
    <div class="info-row">
      <div class="dot-ic">🕕</div>
      <div><div class="value">6:00 p.m.</div></div>
    </div>
    <button class="btn" onclick="addToCalendar()">📅 &nbsp;Agregar al Calendario</button>
  </div>

  <!-- LOCATION -->
  <div class="card">
    <div class="badge">📍</div>
    <h3 class="title">Ubicación</h3>
    <div class="info-row">
      <div class="dot-ic">📍</div>
      <div>
        <div class="value">Conjunto Tabaku Central</div>
        <div class="sub">Cra. 82a #6-37, Kennedy, Bogotá, D.C., Colombia</div>
      </div>
    </div>
    <a class="btn" href="https://www.google.com/maps/search/?api=1&query=Conjunto+Tabaku+Central+Cra+82a+%236-37+Kennedy+Bogota" target="_blank" rel="noopener">🗺️ &nbsp;Ver mapa</a>
  </div>

  <!-- DRESS CODE -->
  <div class="card" style="text-align:center;">
    <div class="badge" style="left:50%; transform:translateX(-50%);">👗</div>
    <h3 class="title" style="justify-content:center;">Código de Vestimenta</h3>
    <p style="color:#374151; font-size:.95rem;">Formal elegante — tonos azules, dorados o neutros para acompañar la celebración.</p>
    <div class="dresscode-photo"><div class="ph">Añade tu foto</div></div>
    <div class="swatches">
      <div class="swatch" style="background:#2e3b6e;"></div>
      <div class="swatch" style="background:#4a90e2;"></div>
      <div class="swatch" style="background:#b8923f;"></div>
      <div class="swatch" style="background:#e9edf7;"></div>
      <div class="swatch" style="background:#1c2440;"></div>
    </div>
  </div>

  <!-- RSVP -->
  <div class="card">
    <div class="badge">✉️</div>
    <h3 class="title">Confirmar Asistencia</h3>
    <form id="rsvpForm">
      <div>
        <label for="name">Tu Nombre *</label>
        <input id="name" type="text" placeholder="Tu nombre completo" required>
      </div>
      <div>
        <label for="phone">Tu Teléfono *</label>
        <input id="phone" type="tel" placeholder="Tu número de teléfono" required>
      </div>
      <div>
        <label>¿Asistirás? *</label>
        <div class="attend-toggle">
          <div class="attend-btn active" id="btn-yes" onclick="setAttend(true)"><div class="circle">✓</div>Sí, asistiré</div>
          <div class="attend-btn" id="btn-no" onclick="setAttend(false)"><div class="circle">✕</div>No podré asistir</div>
        </div>
      </div>
      <div>
        <label for="guests">¿Cuántas personas asistirán? *</label>
        <select id="guests"><option>1</option><option>2</option><option>3</option><option>4</option></select>
      </div>
      <button type="submit" class="btn">✈️ &nbsp;Confirmar Asistencia</button>
      <div class="rsvp-status" id="rsvpStatus"></div>
    </form>
  </div>

</div>

<footer>
  <div class="flower">💐</div>
  <p>Esperamos celebrar contigo</p>
  <div class="fine">Invitación digital hecha a la medida para Isabella</div>
</footer>

<script>
  const target = new Date("2026-09-12T18:00:00-05:00").getTime();
  function updateCountdown(){
    const diff = target - new Date().getTime();
    const el = id => document.getElementById(id);
    if(diff <= 0){ ['cd-days','cd-hours','cd-mins','cd-secs'].forEach(id => el(id).textContent='00'); return; }
    const d = Math.floor(diff / 86400000);
    const h = Math.floor((diff % 86400000) / 3600000);
    const m = Math.floor((diff % 3600000) / 60000);
    const s = Math.floor((diff % 60000) / 1000);
    el('cd-days').textContent = String(d).padStart(2,'0');
    el('cd-hours').textContent = String(h).padStart(2,'0');
    el('cd-mins').textContent = String(m).padStart(2,'0');
    el('cd-secs').textContent = String(s).padStart(2,'0');
  }
  updateCountdown();
  setInterval(updateCountdown, 1000);

  function setAttend(val){
    document.getElementById('btn-yes').classList.toggle('active', val);
    document.getElementById('btn-no').classList.toggle('active', !val);
  }

  document.getElementById('rsvpForm').addEventListener('submit', function(e){
    e.preventDefault();
    const name = document.getElementById('name').value;
    document.getElementById('rsvpStatus').textContent = '¡Gracias, ' + name.split(' ')[0] + '! Tu respuesta fue registrada (demo).';
    this.reset();
    setAttend(true);
  });

  function addToCalendar(){
    const start = "20260912T230000Z";
    const end   = "20260913T030000Z";
    const text = encodeURIComponent("XV Años de Isabella López Flechas");
    const details = encodeURIComponent("Celebración de los XV años de Isabella");
    const location = encodeURIComponent("Conjunto Tabaku Central, Cra. 82a #6-37, Kennedy, Bogotá, Colombia");
    window.open(`https://calendar.google.com/calendar/render?action=TEMPLATE&text=${text}&dates=${start}/${end}&details=${details}&location=${location}`, '_blank');
  }
</script>

</body>
</html>
