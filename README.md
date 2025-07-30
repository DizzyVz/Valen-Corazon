# Valen-Corazon
:c
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Te adoro 💗</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background: #fff0f5;
      font-family: 'Arial', sans-serif;
      user-select: none;
      cursor: pointer;
    }
    .mensaje {
      position: absolute;
      font-size: 24px;
      color: #d63384;
      animation: caer 3s linear forwards;
      white-space: nowrap;
    }
    @keyframes caer {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
    .texto-central {
      position: absolute;
      top: 40%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 30px;
      color: #c2185b;
      text-align: center;
    }
  </style>
</head>
<body onclick="lluvia()">
  <div class="texto-central">Te adoro💗 te adoro💕 te adoro 💞</div>
  <script>
    function lluvia() {
      for (let i = 0; i < 20; i++) {
        const mensaje = document.createElement('div');
        mensaje.className = 'mensaje';
        mensaje.textContent = 'Te adoro 💗';
        mensaje.style.left = Math.random() * window.innerWidth + 'px';
        mensaje.style.top = '-40px';
        mensaje.style.fontSize = (20 + Math.random() * 20) + 'px';
        document.body.appendChild(mensaje);
        setTimeout(() => {
          mensaje.remove();
        }, 3000);
      }
    }
  </script>
</body>
</html>
