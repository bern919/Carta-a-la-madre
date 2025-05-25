<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Feliz Día de las Madres</title>

  <!-- Tipografía Bodoni Moda -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Bodoni+Moda:ital,opsz,wght@0,6..96,400..900;1,6..96,400..900&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      padding: 0;
      background: #ffc0cb;
      font-family: 'Bodoni Moda', serif;
      overflow: hidden;
    }

    .particles {
      position: fixed;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 0;
    }

    .particle {
      position: absolute;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      animation: float 10s infinite linear;
      opacity: 0.8;
    }

    @keyframes float {
      0% {
        transform: translateY(100vh);
      }
      100% {
        transform: translateY(-10vh);
      }
    }

    .carta-container {
      position: relative;
      z-index: 1;
      width: 600px;
      margin: 100px auto;
    }

    .flores-traseras {
      position: absolute;
      top: -50px;
      left: -50px;
      width: 700px;
      height: 700px;
      background-image: url('/mnt/data/rosas.png'); /* Imagen de flores */
      background-repeat: no-repeat;
      background-size: contain;
      background-position: center;
      z-index: -1;
    }

    .carta {
      position: relative;
      background: #fff8f0;
      color: rgb(182, 138, 27); 
      text-align: center;
      padding: 60px;
      border-radius: 25px;
      box-shadow: 0 0 40px rgba(0, 0, 0, 0.15);
      font-size: 26px;
      line-height: 1.6;
      font-family: 'Bodoni Moda', serif;
      border: 10px solid transparent;
      background-image: url('URL_DE_TU_IMAGEN_DE_BORDE_DORADO'); /* Aún debes reemplazar esta URL si tienes borde */
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
    }

    .flores {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
      background-image: url('/mnt/data/rosas.png'); /* Imagen de flores */
      background-repeat: no-repeat;
      background-size: contain;
      pointer-events: none;
    }
  </style>
</head>
<body>

  <div class="particles" id="particles"></div>

  <div class="carta-container">
    <div class="flores-traseras"></div>
    <div class="carta">
      <strong>Querida mamá,</strong><br><br>
      ¡Feliz Día de las Madres! 💐<br><br>
      Gracias por cada abrazo, cada palabra de aliento y cada sacrificio silencioso. 
      Tu amor es la fuerza que guía mi vida y tu sonrisa, mi refugio. 
      Hoy celebramos no solo a una madre, sino a una mujer maravillosa, valiente y llena de luz. 
      Que este día esté lleno de alegría, paz y todo el amor que mereces. 
      ¡Te amo con todo mi corazón!
    </div>
  </div>

  <div class="flores"></div>

  <script>
    // Crear partículas rojas y blancas
    const particlesContainer = document.getElementById('particles');
    for (let i = 0; i < 120; i++) {
      const p = document.createElement('div');
      p.classList.add('particle');
      p.style.left = Math.random() * 100 + 'vw';
      p.style.top = Math.random() * 100 + 'vh';
      p.style.background = Math.random() > 0.5 ? 'red' : 'white';
      p.style.animationDuration = 5 + Math.random() * 10 + 's';
      particlesContainer.appendChild(p);
    }
  </script>

</body>
</html>
