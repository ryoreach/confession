<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dear Souling ❤️</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background: linear-gradient(135deg, #fce4ec, #f8bbd0);
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      color: #333;
      text-align: center;
      padding: 1rem;
      overflow: hidden;
    }

    .confession-box {
      background: white;
      padding: 2rem;
      border-radius: 1.5rem;
      box-shadow: 0 10px 20px rgba(0,0,0,0.1);
      max-width: 90%;
      width: 400px;
      z-index: 2;
      position: relative;
    }

    .confession-box h1 {
      font-size: 2rem;
      color: #d81b60;
      margin-bottom: 1.5rem;
    }

    .sticker {
      width: 80px;
      margin-bottom: 1rem;
    }

    .btn-container {
      display: flex;
      gap: 1rem;
      justify-content: center;
      flex-wrap: wrap;
      position: relative;
    }

    button {
      padding: 0.8rem 1.5rem;
      font-size: 1rem;
      border: none;
      border-radius: 2rem;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    #yesBtn {
      background-color: #f06292;
      color: white;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    }

    #yesBtn:hover {
      background-color: #ec407a;
    }

    #noBtn {
      background-color: #fce4ec;
      color: #d81b60;
      position: fixed;
    }

    #loveMsgContainer {
      display: none;
      align-items: center;
      justify-content: center;
      text-align: center;
      width: 100vw;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      z-index: 10;
      position: fixed;
      top: 0;
      left: 0;
      padding: 2rem;
    }

    #loveMsg {
      font-size: 2.5rem;
      color: #ffffff;
      animation: popIn 0.6s ease forwards;
      text-shadow: 2px 2px 5px rgba(0,0,0,0.2);
    }

    @keyframes popIn {
      0% {
        transform: scale(0.5);
        opacity: 0;
      }
      100% {
        transform: scale(1);
        opacity: 1;
      }
    }

    @media (max-width: 600px) {
      .confession-box h1 {
        font-size: 1.5rem;
      }

      button {
        font-size: 0.9rem;
        padding: 0.6rem 1.2rem;
      }

      #loveMsg {
        font-size: 2rem;
      }
    }
  </style>
</head>
<body>
  <!-- Background Music -->
  <audio autoplay loop>
    <source src="https://cdn.pixabay.com/audio/2022/03/15/audio_995c2973f3.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>

  <div class="confession-box" id="confessionBox">
    <img src="https://cdn-icons-png.flaticon.com/512/2589/2589175.png" alt="cute sticker" class="sticker" />
    <h1>Will you be my girlfriend? 🥺👉👈</h1>
    <div class="btn-container" id="btnContainer">
      <button id="yesBtn">Yes 💖</button>
      <button id="noBtn">No 😢</button>
    </div>
  </div>

  <div id="loveMsgContainer">
    <div id="loveMsg">I love you, darling! 💘💞</div>
  </div>

  <script>
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');
    const loveMsgContainer = document.getElementById('loveMsgContainer');
    const confessionBox = document.getElementById('confessionBox');

    yesBtn.addEventListener('click', () => {
      confessionBox.style.display = 'none';
      loveMsgContainer.style.display = 'flex';
    });

    function moveNoBtn() {
      const windowWidth = window.innerWidth - noBtn.offsetWidth;
      const windowHeight = window.innerHeight - noBtn.offsetHeight;
      const randomX = Math.floor(Math.random() * windowWidth);
      const randomY = Math.floor(Math.random() * windowHeight);
      noBtn.style.left = `${randomX}px`;
      noBtn.style.top = `${randomY}px`;
    }

    noBtn.addEventListener('mouseenter', moveNoBtn);
    noBtn.addEventListener('mousemove', moveNoBtn);
  </script>
</body>
</html>
