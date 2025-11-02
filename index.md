
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
    }
    * { box-sizing: border-box; scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: 'Inter', system-ui, sans-serif;
      color: #e6eef6;
      background: linear-gradient(180deg, #071022 0%, #0b1730 100%);
      transition: background 0.5s ease-in-out;
    }
    .container { max-width: 1100px; margin: 36px auto; padding: 20px; }
    header {
      display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap;
      opacity: 0; animation: fadeIn 1s forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .brand { display: flex; align-items: center; gap: 14px; }
    .logo {
      width: 64px; height: 64px; border-radius: 12px;
      background: linear-gradient(135deg, var(--accent), #2dd4bf);
      display: flex; align-items: center; justify-content: center;
      font-weight: 700; color: #062023;
      box-shadow: 0 0 20px rgba(14,165,163,0.4);
      transition: transform 0.3s;
    }
    .logo:hover { transform: rotate(8deg) scale(1.05); }
    h1 { margin: 0; font-size: 22px; }
    nav a {
      color: var(--muted); text-decoration: none; margin-left: 16px;
      transition: color 0.3s, transform 0.3s;
    }
    nav a:hover { color: var(--accent); transform: scale(1.1); }
    .hero {
      display: grid; grid-template-columns: 1fr 360px; gap: 28px;
      margin-top: 28px; align-items: start;
      opacity: 0; animation: fadeIn 1.2s 0.3s forwards;
    }
    .card {
      background: rgba(11, 18, 32, 0.95);
      padding: 22px; border-radius: 12px;
      box-shadow: 0 6px 18px rgba(3, 7, 18, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.06);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 22px rgba(14, 165, 163, 0.25);
    }
    .btn {
      background: var(--accent); color: #062023;
      padding: 10px 14px; border-radius: 10px;
      font-weight: 600; text-decoration: none;
      display: inline-block; transition: transform 0.3s, box-shadow 0.3s;
    }
    .btn:hover {
      transform: scale(1.05);
      box-shadow: 0 0 14px rgba(14, 165, 163, 0.6);
    }
    .btn-outline {
      border: 1px solid rgba(255, 255, 255, 0.2);
      padding: 10px 14px; border-radius: 10px;
      color: var(--muted); text-decoration: none;
      transition: all 0.3s;
    }
    .btn-outline:hover { border-color: var(--accent); color: var(--accent); }
    input, textarea {
      width: 100%; margin-top: 6px; margin-bottom: 10px;
      padding: 8px; border-radius: 8px; border: none;
      background: rgba(255, 255, 255, 0.07); color: white;
      font-size: 15px; transition: all 0.3s;
    }
    input:focus, textarea:focus {
      outline: 2px solid var(--accent);
      background: rgba(255, 255, 255, 0.1);
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
          <p>Servicios contables — Asesoría financiera y declaración de renta para persona natural.</p>
        </div>
      </div>
      <nav>
        <a href="#servicios">Servicios</a>
        <a href="#form">Contacto</a>
        <a href="#faq">Preguntas</a>
      </nav>
    </header>

    <section class="hero">
      <div class="card">
        <h2>Te ayudo con tu declaración de renta</h2>
        <p>Asesoría personalizada para personas naturales: planeación, optimización y presentación de tu declaración.</p>
        <div class="cta">
          <a class="btn" href="tel:+573142144069">Llamar: 314-214-4069</a>
          <a class="btn-outline" href="#form">Solicitar asesoría</a>
        </div>
      </div>

      <aside class="card" id="contacto">
        <h3>Contacto directo</h3>
        <p><strong>Teléfono:</strong> <a href="tel:+573142144069">+57 314 214 4069</a></p>
        <p><strong>Correo:</strong> <a href="mailto:dd.contable46@gmail.com">dd.contable46@gmail.com</a></p>
      </aside>
    </section>

    <section id="form" style="margin-top:20px">
      <div class="card">
        <h3>Escríbeme</h3>
        <form id="contactForm">
          <label>Nombre</label>
          <input id="name" placeholder="Tu nombre">
          <label>Teléfono</label>
          <input id="phone" placeholder="Ej: 3142144069">
          <label>Mensaje</label>
          <textarea id="message" placeholder="Cuéntame en qué te puedo ayudar"></textarea>
          <div style="margin-top:12px">
            <button class="btn" type="submit">Preparar mensaje</button>
            <a class="btn-outline" href="tel:+573142144069">Llamar</a>
          </div>
        </form>
      </div>
    </section>

    <footer>
      © <strong>Daniel Duarte</strong> — Servicios contables · Tel: 314-214-4069
    </footer>
  </div>

  <script>
    // Animación de bienvenida
    document.addEventListener("DOMContentLoaded", () => {
      setTimeout(() => {
        alert("👋 ¡Bienvenido a la página de Daniel Duarte — Servicios Contables!");
      }, 400);
    });

    // Validación de formulario
    document.getElementById("contactForm").addEventListener("submit", e => {
      e.preventDefault();
      const nombre = document.getElementById("name").value.trim();
      const telefono = document.getElementById("phone").value.trim();
      const mensaje = document.getElementById("message").value.trim();

      if (!nombre || !telefono || !mensaje) {
        alert("⚠️ Por favor, completa todos los campos antes de continuar.");
        return;
      }

      if (confirm("¿Deseas revisar tu mensaje antes de enviarlo?")) {
        alert(`📋 Copia este mensaje:\n\nNombre: ${nombre}\nTeléfono: ${telefono}\nMensaje: ${mensaje}`);
      } else {
        alert("Puedes seguir editando tu mensaje antes de enviarlo.");
      }
    });

    // Efecto parpadeo de botón
    const btn = document.querySelector(".btn");
    setInterval(() => {
      btn.style.boxShadow = "0 0 20px rgba(14,165,163,0.6)";
      setTimeout(() => btn.style.boxShadow = "none", 500);
    }, 2500);
  </script>
</body>
</html>
