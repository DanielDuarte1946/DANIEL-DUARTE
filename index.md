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
      --bg: #0f1724;
      --card: #0b1220;
      --accent: #0ea5a3;
      --muted: #94a3b8;
      --glass: rgba(255, 255, 255, 0.03);
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Inter', system-ui, sans-serif;
      color: #e6eef6;
      background: linear-gradient(180deg, #071022 0%, #0b1730 100%);
      overflow-x: hidden;
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
    h1 { margin: 0; font-size: 20px; }
    p.lead { margin: 0; color: var(--muted); }
    nav a { color: var(--muted); text-decoration: none; margin-left: 16px; }
    nav a:hover { color: var(--accent); }
    .hero { display: grid; grid-template-columns: 1fr 360px; gap: 28px; margin-top: 28px; align-items: start; }
    .card {
      background: var(--card);
      padding: 22px; border-radius: 12px;
      box-shadow: 0 6px 18px rgba(3, 7, 18, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.02);
      transition: transform 0.3s ease;
    }
    .card:hover { transform: scale(1.01); }
    .cta { display: flex; gap: 12px; margin-top: 14px; }
    .btn {
      background: var(--accent); color: #062023;
      padding: 10px 14px; border-radius: 10px;
      font-weight: 600; text-decoration: none;
      display: inline-block; transition: all 0.3s ease;
    }
    .btn:hover { background: #2dd4bf; transform: scale(1.05); }
    .btn-outline {
      border: 1px solid rgba(255, 255, 255, 0.06);
      padding: 10px 14px; border-radius: 10px;
      color: var(--muted); text-decoration: none;
    }
    input, textarea {
      width: 100%; margin-top: 6px; margin-bottom: 10px;
      padding: 10px; border-radius: 8px; border: 1px solid #1e293b;
      background: #0f172a; color: #e6eef6;
    }
    input:focus, textarea:focus { border-color: var(--accent); outline: none; }
    .error { border-color: red !important; }
    .mensaje-exito {
      background: #0ea5a3; color: #062023;
      padding: 10px; border-radius: 8px; text-align: center;
      font-weight: 600; margin-top: 10px; display: none;
    }
    #estado {
      color: var(--accent); font-weight: bold; margin-top: 10px;
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
        </div>
      </div>

      <aside class="card contact-card" id="contacto">
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
    // Animación de bienvenida
    const saludo = document.getElementById("saludo");
    const mensajes = ["Te ayudo con tu declaración de renta", "Optimiza tus impuestos", "Planea tu declaración con confianza"];
    let i = 0;
    function mostrarSaludo() {
      saludo.textContent = mensajes[i];
      i = (i + 1) % mensajes.length;
    }
    mostrarSaludo();
    setInterval(mostrarSaludo, 3000);

    // Mostrar estado laboral
    let hora = new Date().getHours();
    const estado = document.getElementById("estado");
    if (hora >= 8 && hora <= 17) {
      estado.textContent = "🕓 Disponible — horario laboral";
    } else {
      estado.textContent = "🌙 Fuera del horario laboral — deja tu mensaje y te responderé pronto.";
    }

    // Validación mejorada del formulario
    document.getElementById("contactForm").addEventListener("submit", function(e) {
      e.preventDefault();
      let nombre = document.getElementById("name");
      let telefono = document.getElementById("phone");
      let mensaje = document.getElementById("message");
      let campos = [nombre, telefono, mensaje];
      let valido = true;

      campos.forEach(campo => {
        campo.classList.remove("error");
        if (campo.value.trim() === "") {
          campo.classList.add("error");
          valido = false;
        }
      });

      if (!valido) {
        alert("⚠️ Por favor completa todos los campos.");
        return;
      }

      document.getElementById("mensajeExito").style.display = "block";
      console.log(`Nombre: ${nombre.value}, Teléfono: ${telefono.value}, Mensaje: ${mensaje.value}`);
    });

    // Consejos aleatorios cada 5 segundos
    const consejos = [
      "💡 Revisa tus deducciones anualmente.",
      "🗓️ Planea tu declaración con tiempo.",
      "📁 Guarda tus certificados de ingresos.",
      "✅ Evita sanciones cumpliendo los plazos."
    ];
    setInterval(() => {
      const consejo = consejos[Math.floor(Math.random() * consejos.length)];
      console.log("Consejo: " + consejo);
    }, 5000);
  </script>
</body>
</html>
