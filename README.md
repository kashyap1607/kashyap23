<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>For My Love</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to top right, #ff9a9e, #fad0c4);
      color: #fff;
      text-align: center;
      overflow: hidden;
    }
    h1 {
      font-size: 3em;
      margin-top: 50px;
    }
    p {
      font-size: 1.5em;
      width: 80%;
      max-width: 600px;
      margin: 20px auto;
    }
    .hearts {
      position: absolute;
      width: 100%;
      height: 100%;
      overflow: hidden;
      z-index: 0;
    }
    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      transform: rotate(45deg);
      animation: float 8s linear infinite;
      top: 100%;
    }
    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background: red;
      border-radius: 50%;
    }
    .heart::before {
      top: -10px;
      left: 0;
    }
    .heart::after {
      left: -10px;
      top: 0;
    }
    @keyframes float {
      0% {
        transform: translateY(0) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-1000px) rotate(45deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="hearts">
    <!-- Multiple hearts with random left positions -->
    <script>
      for (let i = 0; i < 30; i++) {
        let heart = document.createElement('div');
        heart.className = 'heart';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = 4 + Math.random() * 4 + 's';
        document.querySelector('.hearts').appendChild(heart);
      }
    </script>
  </div>

  <h1>Hi Love ❤️</h1>
  <p>
    I made this little corner of the internet just for you — because you deserve magic, beauty, and every bit of love this world can give.
  </p>
  <p>
    Every moment with you is my favorite. This site is a tiny reminder of how much you mean to me.
  </p>
</body>
</html>
