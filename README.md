<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Te Amo Infinitamente</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background-color: #f9f9f9;
      font-family: 'Arial', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #mensaje {
      font-size: 24px;
      color: #ff1493;
      cursor: pointer;
      text-align: center;
    }

    .corazon {
      position: absolute;
      font-size: 24px;
      color: #ff1493;
      animation: flotar 5s infinite linear;
    }

    @keyframes flotar {
      0% {
        transform: translateY(0) rotate(0deg);
      }
      50% {
        transform: translateY(-100px) rotate(180deg);
      }
      100% {
        transform: translateY(0) rotate(360deg);
      }
    }
  </style>
</head>
<body>
  <div id="mensaje">Sabes cuánto te amo, si quieres saber cuánto te amo presiona aquí</div>

  <script>
    const mensaje = document.getElementById('mensaje');

    mensaje.addEventListener('click', () => {
      mensaje.style.display = 'none'; // Oculta el mensaje inicial

      // Crear corazones que se mueven
      for (let i = 0; i < 50; i++) {
        const corazon = document.createElement('div');
        corazon.classList.add('corazon');
        corazon.innerText = '❤ Te amo infinitamente';
        corazon.style.left = Math.random() * window.innerWidth + 'px';
        corazon.style.top = Math.random() * window.innerHeight + 'px';
        corazon.style.fontSize = Math.random() * 24 + 12 + 'px';
        corazon.style.animationDuration = Math.random() * 5 + 3 + 's';
        document.body.appendChild(corazon);
      }
    });
  </script>
</body>
</html>
