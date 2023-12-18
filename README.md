
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>OperationBonçuk</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #F8C8DC; /* Hintergrundfarbe anpassen */
    }

    .header_text {
      font-family: 'Nunito';
      font-size: 50px;
      font-weight: bold;
      color: white;
      text-align: center;
      margin-top: 20px;
      margin-bottom: 0px;
    }

    .buttons {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      margin-top: 20px;
      margin-left: 20px;
    }

    .btn {
      background-color: #FFB6C1;
      color: white;
      padding: 15px 32px;
      text-align: center;
      display: inline-block;
      font-size: 16px;
      margin: 4px 2px;
      cursor: pointer;
      border: none;
      border-radius: 12px;
      transition: background-color 0.3s ease;
    }

    .btn:hover {
      background-color: #FAF9F6;
    }

    .start_gif_container {
      display: flex;
      justify-content: center;
      align-items: center;
      margin-left: 90px;
    }

    .start_gif_container img {
      max-width: 70%; /* Maximal 70% der Container-Breite */
      max-height: 70%; /* Maximal 70% der Container-Höhe */
    }

    .ergebnis_gif_container {
      display: none; /* Anfangs ausblenden */
      justify-content: center;
      align-items: center;
      margin-left: 90px;
    }
  </style>
</head>
<body>

<div class="header_text">Ich vermisse dich, du Minnie Panda. Wollen wir uns demnächst treffen? :)</div>

<div class="buttons">
  <button class="btn" onclick="antwort('Evet')">Evet</button>
  <button class="btn" onmouseover="moveButton()" onclick="antwort('Hayir')" id="hayir">Hayir</button>
</div>

<div class="start_gif_container" id="start_gif">
  <img src="https://media1.tenor.com/m/tModFkF0ErMAAAAd/seulisasoo.gif" alt="Start-GIF">
</div>

<div class="ergebnis_gif_container" id="ergebnis_gif">
  <img src="https://media1.tenor.com/m/L-Gv7FI-nqMAAAAd/jinmiran-hahaha.gif" alt="Neues GIF">
</div>

<script>
  function antwort(antwort) {
    if (antwort === 'Evet') {
      document.querySelector('.header_text').innerHTML = 'hihihi, gute Entscheidung';
      document.getElementById('hayir').style.pointerEvents = 'none';
      document.querySelector('.buttons').style.display = 'none';
      document.querySelector('.start_gif_container').style.display = 'none'; /* Start-GIF ausblenden */
      document.querySelector('.ergebnis_gif_container').style.display = 'flex'; /* Einblenden */
    }
  }

  function moveButton() {
    var hayirButton = document.getElementById('hayir');
    var randomX = Math.floor(Math.random() * window.innerWidth);
    var randomY = Math.floor(Math.random() * window.innerHeight);

    hayirButton.style.position = 'absolute';
    hayirButton.style.left = randomX + 'px';
    hayirButton.style.top = randomY + 'px';
  }
</script>

</body>
</html>
