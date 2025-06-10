<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Contador de Amor</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      height: 100%;
      font-family: 'Arial', sans-serif;
      color: white;
      text-shadow: 2px 2px 4px #000;
    }

    body {
      background-image: url('FOTO_DO_CASAL.jpg');
      background-size: cover;
      background-position: center;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .contador {
      background: rgba(0, 0, 0, 0.5);
      padding: 40px;
      border-radius: 20px;
      text-align: center;
    }

    .contador h1 {
      font-size: 2em;
      margin-bottom: 20px;
    }

    .tempo {
      font-size: 1.5em;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="contador">
    <h1>Juntos desde 02/02/2025 💖</h1>
    <div class="tempo" id="tempo-decorrido"></div>
  </div>

  <script>
    const dataInicio = new Date("2025-02-02T00:00:00");

    function atualizarTempo() {
      const agora = new Date();
      let diff = agora - dataInicio;

      const minutos = Math.floor(diff / 1000 / 60);
      const dias = Math.floor(minutos / 1440);
      const horas = Math.floor((minutos % 1440) / 60);
      const mins = minutos % 60;

      document.getElementById("tempo-decorrido").innerText =
        `${dias} dias, ${horas} horas e ${mins} minutos juntos 💞`;
    }

    atualizarTempo();
    setInterval(atualizarTempo, 60000);
  </script>
</body>
</html>
