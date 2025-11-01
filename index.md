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

    body {
      margin: 0;
      font-family: 'Inter', sans-serif;
      color: #e6eef6;
      background: linear-gradient(180deg, #071022 0%, #0b1730 100%);
      transition: background 0.6s ease;
    }

    body.modo-claro {
      background: #f5f7fa;
      color: #1a1a1a;
    }

    .container { max-width: 1100px; margin: 36px auto; padding: 20px; }
    header, footer { text-align: center; margin-bottom: 20px; }

    .btn {
      background: var(--accent);
      color: #062023;
      padding: 10px 16px;
      border-radius: 8px;
      border: none;
      cursor: pointer;
      font-weight: 600;
      transition: transform 0.2s ease, opacity 0.3s;
    }
    .btn:hover { transform: scale(1.05); opacity: 0.9; }

    .card {
      background: var(--card);
      padding: 22px;
      border-radius: 12px;
      margin: 14px 0;
      box-shadow: 0 6px 18px rgba(3, 7, 18, 0.6);
    }

    .modo-claro .card {
      background: #ffffff;
      color: #1a1a1a;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    label { display: block; margin-top: 10px; }
    input, textarea {
      width: 100%; padding: 10px; border-radius: 8px; border: 1px solid #ccc;
      background: transparent; color: inherit;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>👋 Bienvenido a Daniel Duarte - Servicios Contables</h1>
      <p>Optimiza tus impuestos y mejora tu planeación financiera.</p>
      <button id="saludoBtn" class="btn">Saludar al usuario</button>
      <button id="modoBtn" class="btn">Cambiar modo</button>
    </header>

    <section class="card">
      <h2>Formulario de contacto</h2>
      <form id="contactForm">
        <label>Nombre</label>
        <input type="text" id="nombre" placeholder="Tu nombre">

        <label>Teléfono</label>
        <input type="text" id="telefono" placeholder="Ej: 3142144069">

        <label>Mensaje</label>
        <textarea id="mensaje" placeholder="Cuéntame en qué te puedo ayudar"></textarea>

        <button type="submit" class="btn" style="margin-top:12px">Enviar mensaje</button>
      </form>
    </section>

    <section class="card">
      <h2>Información adicional</h2>
      <p id="contadorText"></p>
      <button id="contadorBtn" class="btn">Ver contador</button>
    </section>

    <footer>
      <p>© 2025 Daniel Duarte — Servicios contables</p>
    </footer>
  </div>

  <script>
    // ALERTA DE BIENVENIDA
    alert("Bienvenido a la página de Daniel Duarte — Servicios Contables");

    // FUNCIÓN DE SALUDO CON CONDICIONAL
    document.getElementById("saludoBtn").addEventListener("click", function() {
      let nombre = prompt("¿Cuál es tu nombre?");
      if (nombre === "" || nombre === null) {
        alert("No ingresaste tu nombre. ¡Inténtalo de nuevo!");
      } else {
        alert("¡Hola " + nombre + "! Gracias por visitar la página 😊");
      }
    });

    // FUNCIÓN PARA CAMBIAR MODO CLARO/OSCURO CON OPERADOR DE IGUALDAD
    const body = document.body;
    document.getElementById("modoBtn").addEventListener("click", function() {
      if (body.className == "modo-claro") {
        body.className = "";
        alert("Has activado el modo oscuro 🌙");
      } else {
        body.className = "modo-claro";
        alert("Has activado el modo claro ☀️");
      }
    });

    // VALIDACIÓN SIMPLE DEL FORMULARIO (if, else)
    document.getElementById("contactForm").addEventListener("submit", function(event) {
      event.preventDefault();

      let nombre = document.getElementById("nombre").value;
      let telefono = document.getElementById("telefono").value;
      let mensaje = document.getElementById("mensaje").value;

      if (nombre == "" || telefono == "" || mensaje == "") {
        alert("⚠️ Por favor completa todos los campos antes de enviar.");
      } else if (telefono.length < 8) {
        alert("📞 El número de teléfono parece demasiado corto.");
      } else {
        alert("✅ Mensaje preparado para enviar:\n\nNombre: " + nombre + "\nTeléfono: " + telefono + "\nMensaje: " + mensaje);
      }
    });

    // CONTADOR USANDO BUCLE FOR Y OPERADOR DE INCREMENTO
    document.getElementById("contadorBtn").addEventListener("click", function() {
      let contador = 0;
      let texto = "Contando hasta 5:\n";
      for (let i = 1; i <= 5; i++) {
        contador++;
        texto += "Número " + i + " (contador = " + contador + ")\n";
      }
      document.getElementById("contadorText").innerText = texto;
    });

    // DEMO DE BUCLE WHILE
    let intento = 0;
    while (intento < 1) {
      console.log("La página se cargó correctamente.");
      intento++;
    }

    // USO DE FUNCIONES: mostrar hora actual
    function mostrarHora() {
      let fecha = new Date();
      console.log("Hora actual: " + fecha.toLocaleTimeString());
    }
    mostrarHora(); // ejecuta la función
  </script>
</body>
</html>
