<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Daniel Duarte - Servicios Contables</title>
  <meta name="description" content="Asesoría contable y financiera. Especialistas en declaración de renta de persona natural, outsourcing contable y asesoría tributaria.">
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap">

  <style>
    :root {
      --bg1: #071022;
      --bg2: #0b1730;
      --card: #0b1220;
      --accent: #0ea5a3;
      --muted: #94a3b8;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Inter', system-ui, sans-serif;
      color: #e6eef6;
      background: linear-gradient(-45deg, var(--bg1), var(--bg2), #0c213f, #05101f);
      background-size: 400% 400%;
      animation: moverFondo 12s ease infinite;
      overflow-x: hidden;
    }

    @keyframes moverFondo {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .container { max-width: 1100px; margin: 36px auto; padding: 20px; animation: fadeIn 1.5s ease; }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    header, .card, footer {
      animation: aparecer 1.2s ease forwards;
      opacity: 0;
    }
    @keyframes aparecer {
      to { opacity: 1; transform: none; }
    }

    header { display: flex; align-items: center; justify-content: space-between; gap: 20px; }
    .brand { display: flex; align-items: center; gap: 14px; }
    .logo {
      width: 64px; height: 64px; border-radius: 12px;
      background: linear-gradient(135deg, var(--accent), #2dd4bf);
      display: flex; align-items: center; justify-content: center;
      font-weight: 700; color: #062023;
      box-shadow: 0 0 12px rgba(14,165,163,0.4);
    }

    h1 { margin: 0; font-size: 22px; }
    p.lead { margin: 0; color: var(--muted); }
    nav a { color: var(--muted); text-decoration: none; margin-left: 16px; transition: 0.3s; }
    nav a:hover { color: var(--accent); text-shadow: 0 0 6px var(--accent); }

    .hero { display: grid; grid-template-columns: 1fr 360px; gap: 28px; margin-top: 28px; align-items: start; }
    .card {
      background: var(--card);
      padding: 22px; border-radius: 12px;
      box-shadow: 0 6px 18px rgba(3, 7, 18, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.05);
      transform: translateY(20px);
      transition: transform 0.4s ease, box-shadow 0.4s ease;
    }
    .card:hover {
      transform: translateY(0px) scale(1.02);
      box-shadow: 0 0 25px rgba(14,165,163,0.2);
    }

    .cta { display: flex; gap: 12px; margin-top: 14px; }
    .btn {
      background: var(--accent); color: #062023;
      padding: 10px 14px; border-radius: 10px;
      font-weight: 600; text-decoration: none;
      display: inline-block; transition: all 0.3s ease;
      position: relative; overflow: hidden;
    }
    .btn::after {
      content: "";
      position: absolute; top: 0; left: -75%;
      width: 50%; height: 100%;
      background: rgba(255,255,255,0.3);
      transform: skewX(-20deg);
      transition: left 0.5s;
    }
    .btn:hover::after { left: 125%; }
    .btn:hover { transform: scale(1.05); }

    .btn-outline {
      border: 1px solid rgba(255, 255, 255, 0.1);
      padding: 10px 14px; border-radius: 10px;
      color: var(--muted); text-decoration: none;
      transition: 0.3s;
    }
    .btn-outline:hover { border-color: var(--accent); color: var(--accent); }

    input, textarea {
      width: 100%; margin-top: 6px; margin-bottom: 10px;
      padding: 10px; border-radius: 8px;
      border: 1px solid #1e293b;
      background: #0f172a; color: #e6eef6;
      transition: border-color 0.3s;
    }
    input:focus, textarea:focus { border-color: var(--accent); outline: none; }
    .error { border-color: red !important; animation: shake 0.2s ease-in-out 2; }
    @keyframes shake {
      0%, 100% { transform: translateX(0); }
      25% { transform: translateX(-3px); }
      75% { transform: translateX(3px); }
    }

    .mensaje-exito {
      background: #0ea5a3; color: #062023;
      padding: 10px; border-radius: 8px; text-align: center;
      font-weight: 600; margin-top: 10px;
      opacity: 0; transform: scale(0.9);
      transition: all 0.4s ease;
    }
    .mensaje-exito.mostrar { opacity: 1; transform: scale(1); }

    #estado {
      color: var(--accent); font-weight: bold; margin-top: 10px;
      transition: 0.5s ease;
    }

    #consejo {
      margin-top: 10px;
      font-size: 15px;
      color: var(--muted);
      opacity: 0;
      transition: opacity 0.5s ease;
    }

    footer { margin-top: 28px; padding: 24px; text-align: center; color: var(--muted); font-size: 14px; }
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

    <section class="hero">
      <div>
        <div class="card">
          <h2 id="saludo"></h2>
          <p class="muted">Asesoría personalizada para personas naturales: planeación, optimización y presentación de tu declaración de renta.</p>
          <div class="cta">
            <a class="btn" href="tel:+573142144069">Llamar: 314-214-4069</a>
            <a class="btn-outline" href="#contacto">Solicitar asesoría</a>
          </div>
          <div id="estado"></div>
          <p id="consejo"></p>
        </div>
      </div>

      <aside class="card" id="contacto">
        <h3>Contacto</h3>
        <p class="muted">Contáctame para agendar una asesoría o revisar tu declaración.</p>
        <p><strong>Teléfono:</strong> <a href="tel:+573142144069">+57 314 214 4069</a></p>
        <p><strong>Correo:</strong> <a href="mailto:dd.contable46@gmail.com">dd.contable46@gmail.com</a></p>
      </aside>
    </section>

    <section id="form" style="margin-top:18px">
      <div class="card">
        <h3>Escríbeme</h3>
        <form id="contactForm">
          <label for="name">Nombre</label>
          <input id="name" placeholder="Tu nombre">
          <label for="phone">Teléfono</label>
          <input id="phone" placeholder="Ej: 3142144069">
          <label for="message">Mensaje</label>
          <textarea id="message" placeholder="Cuéntame en qué te puedo ayudar"></textarea>
          <div style="margin-top:12px">
            <button class="btn" type="submit">Preparar mensaje</button>
            <a class="btn-outline" href="tel:+573142144069">Llamar</a>
          </div>
          <div class="mensaje-exito" id="mensajeExito">✅ Tu mensaje ha sido preparado correctamente.</div>
        </form>
      </div>
    </section>

    <footer>
      <div class="muted">© <strong>Daniel Duarte</strong> — Servicios contables · Tel: 314-214-4069</div>
    </footer>
  </div>

  <script>
    // Efecto de escritura en saludo
    const saludo = document.getElementById("saludo");
    const textos = ["Te ayudo con tu declaración de renta", "Optimiza tus impuestos", "Planea tu declaración con confianza"];
    let i = 0, j = 0, actual = "", borrando = false;
    function escribir() {
      actual = textos[i];
      saludo.textContent = actual.substring(0, j);
      if (!borrando && j < actual.length) j++;
      else if (borrando && j > 0) j--;
      else if (!borrando && j === actual.length) { borrando = true; setTimeout(escribir, 1000); return; }
      else { borrando = false; i = (i + 1) % textos.length; }
      setTimeout(escribir, borrando ? 50 : 100);
    }
    escribir();

    // Estado horario
    const estado = document.getElementById("estado");
    let hora = new Date().getHours();
    if (hora >= 8 && hora <= 17) {
      estado.textContent = "🕓 Disponible — horario laboral";
    } else {
      estado.textContent = "🌙 Fuera del horario laboral — deja tu mensaje.";
      estado.style.color = "#f87171";
    }

    // Validación y animación de éxito
    document.getElementById("contactForm").addEventListener("submit", function(e) {
      e.preventDefault();
      let nombre = document.getElementById("name");
      let telefono = document.getElementById("phone");
      let mensaje = document.getElementById("message");
      let valido = true;

      [nombre, telefono, mensaje].forEach(campo => {
        campo.classList.remove("error");
        if (campo.value.trim() === "") {
          campo.classList.add("error");
          valido = false;
        }
      });

      const msgExito = document.getElementById("mensajeExito");
      if (valido) {
        msgExito.classList.add("mostrar");
        setTimeout(() => msgExito.classList.remove("mostrar"), 4000);
      } else {
        alert("⚠️ Completa todos los campos antes de continuar.");
      }
    });

    // Consejos animados
    const consejos = [
      "💡 Revisa tus deducciones anualmente.",
      "🗓️ Planea tu declaración con tiempo.",
      "📁 Guarda tus certificados de ingresos.",
      "✅ Evita sanciones cumpliendo los plazos."
    ];
    const consejoEl = document.getElementById("consejo");
    let c = 0;
    function mostrarConsejo() {
      consejoEl.style.opacity = 0;
      setTimeout(() => {
        consejoEl.textContent = consejos[c];
        consejoEl.style.opacity = 1;
        c = (c + 1) % consejos.length;
      }, 400);
    }
    mostrarConsejo();
    setInterval(mostrarConsejo, 5000);
  </script>
</body>
</html>
