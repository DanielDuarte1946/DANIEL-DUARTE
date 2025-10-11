<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Daniel Duarte - Servicios Contables</title>
  <meta name="description" content="Asesoría contable y financiera. Especialistas en declaración de renta de persona natural, outsourcing contable y asesoría tributaria.">

  <!-- Metadatos para SEO y redes -->
  <meta property="og:title" content="Daniel Duarte - Servicios Contables">
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://danielduarte1946.github.io/DANIEL-DUARTE/">
  <meta property="og:locale" content="es_CO">
  <meta property="og:site_name" content="Daniel Duarte">
  <meta name="twitter:card" content="summary">
  <meta name="twitter:title" content="Daniel Duarte - Servicios Contables">

  <!-- Estilos -->
  <style>
    :root {
      --bg: #0f1724;
      --card: #0b1220;
      --accent: #0ea5a3;
      --muted: #94a3b8;
      --glass: rgba(255,255,255,0.03);
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      color: #e6eef6;
      background: linear-gradient(180deg, #071022 0%, #0b1730 100%);
      -webkit-font-smoothing: antialiased;
    }
    .container { max-width: 1100px; margin: 36px auto; padding: 20px; }
    header { display: flex; align-items: center; justify-content: space-between; gap: 20px; }
    .brand { display: flex; align-items: center; gap: 14px; }
    .logo {
      width: 64px; height: 64px; border-radius: 12px;
      background: linear-gradient(135deg, var(--accent), #2dd4bf);
      display: flex; align-items: center; justify-content: center;
      font-weight: 700; color: #062023;
    }
    h1 { margin: 0; font-size: 22px; }
    p.lead { margin: 0; color: var(--muted); }
    nav a { color: var(--muted); text-decoration: none; margin-left: 16px; }
    .hero { display: grid; grid-template-columns: 1fr 360px; gap: 28px; margin-top: 28px; align-items: start; }
    .card {
      background: var(--card);
      padding: 22px;
      border-radius: 12px;
      box-shadow: 0 6px 18px rgba(3,7,18,0.6);
      border: 1px solid rgba(255,255,255,0.02);
    }
    .services ul { padding-left: 18px; margin: 10px 0; }
    .cta { display: flex; gap: 12px; margin-top: 14px; }
    .btn {
      background: var(--accent);
      color: #062023;
      padding: 10px 14px;
      border-radius: 10px;
      font-weight: 600;
      text-decoration: none;
      display: inline-block;
    }
    .btn-outline {
      border: 1px solid rgba(255,255,255,0.06);
      padding: 10px 14px;
      border-radius: 10px;
      color: var(--muted);
      text-decoration: none;
    }
    .muted { color: var(--muted); }
    .feature { display: flex; gap: 12px; align-items: flex-start; margin-top: 12px; }
    .feature .num {
      background: var(--glass);
      padding: 8px;
      border-radius: 8px;
      width: 42px; height: 42px;
      display: grid; place-items: center;
      color: var(--accent);
      font-weight: 700;
    }
    footer { margin-top: 28px; padding: 24px; text-align: center; color: var(--muted); font-size: 14px; }
    .faq { margin-top: 18px; }
    .grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
    @media(max-width:900px) {
      .hero { grid-template-columns: 1fr; }
      .grid-3 { grid-template-columns: 1fr; }
      .container { margin: 12px; }
    }
    label { display: block; font-size: 13px; margin: 8px 0 6px; color: var(--muted); }
    input, textarea {
      width: 100%; padding: 10px;
      border-radius: 8px;
      border: 1px solid rgba(255,255,255,0.03);
      background: transparent;
      color: inherit;
    }
    textarea { min-height: 120px; }
  </style>
</head>

<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">DD</div>
        <div>
          <h1>Daniel Duarte</h1>
          <p class="lead">Servicios contables — asesoría financiera y contable. Especialistas en declaración de renta persona natural.</p>
        </div>
      </div>
      <nav>
        <a href="#servicios">Servicios</a>
        <a href="#faq">Preguntas</a>
        <a href="#contacto">Contacto</a>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div>
          <div class="card">
            <h2>Te ayudo con tu declaración de renta</h2>
            <p class="muted">Asesoría personalizada para personas naturales: planeación, optimización y presentación de tu declaración de renta.</p>
            <div class="services">
              <h3>Servicios principales</h3>
              <ul>
                <li><strong>Declaración de renta - Persona natural</strong></li>
                <li>Asesoría contable y financiera</li>
                <li>Outsourcing contable y conciliaciones</li>
                <li>Asesoría en retenciones y cumplimiento tributario</li>
                <li>Preparación de estados financieros</li>
              </ul>
              <div class="cta">
                <a class="btn" href="tel:+573142144069">Llamar</a>
                <a class="btn-outline" href="#contacto">Solicitar asesoría</a>
              </div>
            </div>
          </div>

          <div class="card" style="margin-top:14px;">
            <h3>¿Por qué elegirnos?</h3>
            <div class="feature"><div class="num">1</div><div><strong>Especialización</strong><div class="muted">En renta de personas naturales.</div></div></div>
            <div class="feature"><div class="num">2</div><div><strong>Claridad</strong><div class="muted">Explicaciones simples y precisas.</div></div></div>
            <div class="feature"><div class="num">3</div><div><strong>Soporte práctico</strong><div class="muted">Acompañamiento financiero completo.</div></div></div>
          </div>
        </div>

        <aside class="card" id="contacto">
          <h3>Contacto</h3>
          <p class="muted">Agende su asesoría o revisión de declaración.</p>
          <p><strong>Teléfono:</strong> <a href="tel:+573142144069">+57 314 214 4069</a></p>
          <p><strong>Correo:</strong> <a href="mailto:dd.contable46@gmail.com">dd.contable46@gmail.com</a></p>
          <p><strong>Horario:</strong> Lunes a Viernes, 8:30 a.m. – 5:30 p.m.</p>
        </aside>
      </section>

      <section id="servicios">
        <div class="card">
          <h3>Servicios detallados</h3>
          <div class="grid-3">
            <div><h4>Declaración de renta</h4><p class="muted">Optimización de deducciones y presentación ante la DIAN.</p></div>
            <div><h4>Outsourcing contable</h4><p class="muted">Registro, conciliaciones y estados financieros.</p></div>
            <div><h4>Planeación tributaria</h4><p class="muted">Estrategias legales para optimizar impuestos.</p></div>
          </div>
        </div>
      </section>

      <section id="faq">
        <div class="card">
          <h3>Preguntas frecuentes</h3>
          <p><strong>¿Qué documentos debo traer?</strong> Certificados, extractos y facturas deducibles.</p>
          <p><strong>¿Cobran revisión previa?</strong> La primera revisión básica es gratuita.</p>
        </div>
      </section>

      <section id="form">
        <div class="card">
          <h3>Escríbeme</h3>
          <form onsubmit="event.preventDefault();alert('Formulario listo para copiar: Nombre: '+document.getElementById('name').value+'\nTel: '+document.getElementById('phone').value+'\nMensaje: '+document.getElementById('message').value)">
            <label for="name">Nombre</label>
            <input id="name" placeholder="Tu nombre">
            <label for="phone">Teléfono</label>
            <input id="phone" placeholder="Ej: 3142144069">
            <label for="message">Mensaje</label>
            <textarea id="message" placeholder="Cuéntame en qué te puedo ayudar"></textarea>
            <div class="cta">
              <button class="btn" type="submit">Preparar mensaje</button>
              <a class="btn-outline" href="tel:+573142144069">Llamar</a>
            </div>
          </form>
        </div>
      </section>
    </main>

    <footer>
      <p class="muted">© <strong>Daniel Duarte</strong> — Servicios contables · Tel: 314-214-4069</p>
    </footer>
  </div>

  <script>
    console.log("Página cargada correctamente");
  </script>
</body>
</html>
