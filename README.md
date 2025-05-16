# Poj-wied-mini-
Wiedznini z adhd 
<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <title>Rekrutacja Wiedźminów ADHD</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: monospace;
      background: #111;
      color: #0f0;
      text-align: center;
    }
    .container {
      padding-top: 100px;
    }
    input, button {
      font-size: 18px;
      margin: 10px;
      padding: 10px;
      background: #222;
      color: #fff;
      border: 2px solid #0f0;
    }
    .small-text {
      font-size: 12px;
      color: #777;
    }
    .blackout {
      position: fixed;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: black;
      color: yellow;
      font-size: 28px;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 9999;
      flex-direction: column;
      display: none;
    }
    .fire {
      font-size: 100px;
      color: red;
      animation: burn 0.8s infinite alternate;
    }
    @keyframes burn {
      0% { text-shadow: 0 0 10px orange; }
      100% { text-shadow: 0 0 20px red; transform: scale(1.1); }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Łysa Pała z Rivii rekrutuje!</h1>
    <p>Podaj dane, żeby zostać pojebanym Wiedźminem ADHD:</p>
    <input type="text" id="name" placeholder="Imię">
    <input type="text" id="nickname" placeholder="Ksywka pojeba">
    <br>
    <button onclick="submitForm()">Wyślij zgłoszenie</button>
    <div class="small-text">(Strona dla jaj, nie traktuj tego jak rekrutacji do GROMu)</div>
  </div>

  <div id="blackout" class="blackout">
    <div class="fire">IGNI!</div>
    <p>WITAM POJEBA<br>ZOSTAŁEŚ JEBANYM WIEDŹMINEM</p>
    <audio id="igni-sound" autoplay>
      <source src="https://cdn.pixabay.com/audio/2021/08/08/audio_c1a400a39b.mp3" type="audio/mpeg">
    </audio>
  </div>

  <script>
    function submitForm() {
      const name = document.getElementById("name").value.trim();
      const nickname = document.getElementById("nickname").value.trim();
      if (name === "" || nickname === "") {
        alert("Wpisz imię i ksywkę, pojebie!");
        return;
      }
      document.getElementById("blackout").style.display = "flex";
      const audio = document.getElementById("igni-sound");
      audio.volume = 1;
      audio.play();
    }
  </script>
</body>
</html>
