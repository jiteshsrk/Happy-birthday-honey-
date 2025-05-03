<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday Madam Ji</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to top right, #ffe6e6, #fff5f5);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    h1 {
      text-align: center;
      color: crimson;
      margin-top: 30px;
      font-size: 3em;
      animation: glow 2s infinite alternate;
    }

    @keyframes glow {
      from {
        text-shadow: 0 0 10px crimson;
      }
      to {
        text-shadow: 0 0 20px red;
      }
    }

    .quotes {
      color: #333;
      text-align: center;
      margin: 40px 20px;
      font-size: 1.2em;
    }

    .roses {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }

    .rose {
      position: absolute;
      width: 50px;
      animation: fall linear infinite;
    }

    @keyframes fall {
      0% {
        transform: translateY(-100px) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }

    .baby {
      width: 200px;
      display: block;
      margin: 20px auto;
      border-radius: 20px;
      box-shadow: 0 0 20px pink;
    }

    .birds {
      position: absolute;
      top: 10px;
      right: 10px;
      width: 100px;
      z-index: 10;
    }
  </style>
</head>
<body>
  <h1>Happy Birthday Madam Ji!</h1>

  <img class="birds" src="https://i.gifer.com/7yD7.gif" alt="Flying Birds">

  <div class="quotes">
    <p>"Aap jaise log sirf ek baar paida hote hain. Khush rahiye hamesha!"</p>
    <p>"Har din aapka chehra muskurata rahe. Happy Birthday!"</p>
    <p>"Khushiyo se bhara har ek pal ho aapka. Janamdin ki dher saari shubhkamnayein!"</p>
  </div>

  <img class="baby" src="https://i.pinimg.com/originals/2c/f4/b0/2cf4b07a1e1b4e88a7a528cf332dad99.jpg" alt="Cute Baby Girl">

  <div class="roses" id="roses-container"></div>

  <audio autoplay loop>
    <source src="https://www.fesliyanstudios.com/play-mp3/387" type="audio/mp3">
    Your browser does not support the audio element.
  </audio>

  <script>
    const container = document.getElementById('roses-container');
    const roseURL = 'https://www.freeiconspng.com/uploads/rose-png-17.png';

    for (let i = 0; i < 20; i++) {
      let img = document.createElement('img');
      img.src = roseURL;
      img.className = 'rose';
      img.style.left = Math.random() * 100 + 'vw';
      img.style.animationDuration = (3 + Math.random() * 5) + 's';
      img.style.top = -100 + 'px';
      container.appendChild(img);
    }
  </script>
</body>
</html>
