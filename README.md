
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Voice of Muzamil</title>
  <style>
    body {
      background: #0f0f0f;
      color: #fff;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .voice-button {
      background: linear-gradient(145deg, #00ffd5, #0057ff);
      border: none;
      border-radius: 50%;
      width: 120px;
      height: 120px;
      display: flex;
      justify-content: center;
      align-items: center;
      box-shadow: 0 0 30px rgba(0, 255, 255, 0.6);
      animation: pulse 2s infinite;
      cursor: pointer;
    }
    .voice-button:hover {
      box-shadow: 0 0 40px rgba(0, 255, 255, 1);
    }
    @keyframes pulse {
      0% { box-shadow: 0 0 15px rgba(0, 255, 255, 0.3); }
      50% { box-shadow: 0 0 40px rgba(0, 255, 255, 0.9); }
      100% { box-shadow: 0 0 15px rgba(0, 255, 255, 0.3); }
    }
    .text {
      margin-top: 20px;
      font-size: 1.2em;
      opacity: 0;
      transition: opacity 1s ease;
    }
    .text.visible {
      opacity: 1;
    }
  </style>
</head>
<body>
  <button class="voice-button" onclick="playVoice()">
    <img src="https://img.icons8.com/ios-filled/50/ffffff/microphone.png" alt="Play" />
  </button>
  <div class="text" id="voiceText">Hey, what's up? I'm Muzamil.</div><audio id="muzamilAudio" src="/mnt/data/20250411-104313.mp3"></audio>

  <script>
    function playVoice() {
      const audio = document.getElementById('muzamilAudio');
      const text = document.getElementById('voiceText');
      audio.play();
      text.classList.add('visible');
    }
  </script></body>
</html>
