<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>The Personality Color</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }

    body {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: background 0.8s ease;
      background: #f5f5f5;
      overflow: hidden;
    }

    .container {
      text-align: center;
      z-index: 2;
    }

    input {
      padding: 14px 20px;
      width: 280px;
      border: none;
      border-radius: 8px;
      outline: none;
      font-size: 16px;
      text-align: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    button {
      margin-top: 15px;
      padding: 10px 20px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      background: #333;
      color: #fff;
      transition: 0.3s;
    }

    button:hover {
      background: #555;
    }

    .message {
      margin-top: 10px;
      font-size: 14px;
      color: #333;
    }

    /* Animations */
    .overlay {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }

    /* API (marah) */
    .fire {
      background: radial-gradient(circle, rgba(255,0,0,0.3), transparent);
      animation: fireMove 2s infinite alternate;
    }

    @keyframes fireMove {
      from { transform: translateY(0); opacity: 0.6; }
      to { transform: translateY(-20px); opacity: 1; }
    }

    /* Ombak (tenang) */
    .wave {
      background: repeating-linear-gradient(
        0deg,
        rgba(255,255,255,0.2) 0px,
        rgba(255,255,255,0.2) 2px,
        transparent 2px,
        transparent 6px
      );
      animation: waveMove 3s linear infinite;
    }

    @keyframes waveMove {
      from { background-position: 0 0; }
      to { background-position: 0 50px; }
    }

    /* Hujan (sedih) */
    .rain {
      background-image: linear-gradient(rgba(255,255,255,0.3) 2px, transparent 2px);
      background-size: 2px 10px;
      animation: rainFall 0.5s linear infinite;
    }

    @keyframes rainFall {
      from { background-position: 0 0; }
      to { background-position: 0 10px; }
    }

    /* Sparkle (bahagia) */
    .sparkle {
      background: radial-gradient(circle, rgba(255,255,255,0.7) 2px, transparent 3px);
      background-size: 30px 30px;
      animation: sparkleMove 2s linear infinite;
    }

    @keyframes sparkleMove {
      from { background-position: 0 0; }
      to { background-position: 30px 30px; }
    }

    /* Glitch (cemas) */
    .glitch {
      animation: glitchAnim 0.2s infinite;
    }

    @keyframes glitchAnim {
      0% { transform: translate(0,0); }
      25% { transform: translate(2px,-2px); }
      50% { transform: translate(-2px,2px); }
      75% { transform: translate(2px,2px); }
      100% { transform: translate(0,0); }
    }

    /* Energi (semangat) */
    .energy {
      background: radial-gradient(circle, rgba(255,255,255,0.3), transparent);
      animation: energyPulse 1s infinite alternate;
    }

    @keyframes energyPulse {
      from { transform: scale(1); opacity: 0.5; }
      to { transform: scale(1.2); opacity: 1; }
    }

  </style>
</head>

<body>

<div class="overlay" id="overlay"></div>

<div class="container">
  <input type="text" id="input" placeholder="Describe your feeling today in one word..." />
  <br>
  <button onclick="resetMood()">Reset Mood</button>
  <div class="message" id="message"></div>
</div>

<script>
  const input = document.getElementById("input");
  const body = document.body;
  const overlay = document.getElementById("overlay");
  const message = document.getElementById("message");

  input.addEventListener("change", applyMood);

  function applyMood() {
    let mood = input.value.toLowerCase().trim();

    overlay.className = "overlay";
    message.textContent = "";

    switch (mood) {
      case "marah":
        body.style.background = "#b71c1c";
        overlay.classList.add("fire");
        break;

      case "tenang":
        body.style.background = "#1565c0";
        overlay.classList.add("wave");
        break;

      case "sedih":
        body.style.background = "#424242";
        overlay.classList.add("rain");
        break;

      case "bahagia":
        body.style.background = "#fdd835";
        overlay.classList.add("sparkle");
        break;

      case "cemas":
        body.style.background = "#4a148c";
        overlay.classList.add("glitch");
        break;

      case "semangat":
        body.style.background = "#ef6c00";
        overlay.classList.add("energy");
        break;

      default:
        body.style.background = "#f5f5f5";
        message.textContent = "Emotion not recognized, try another word.";
    }
  }

  function resetMood() {
    body.style.background = "#f5f5f5";
    overlay.className = "overlay";
    input.value = "";
    message.textContent = "";
  }
</script>

</body>
</html>
