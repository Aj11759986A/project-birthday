<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday!</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      font-family: 'Poppins', sans-serif;
      overflow: hidden;
      perspective: 1000px;
    }

    h1 {
      text-align: center;
      margin-top: 40px;
      font-size: 3em;
      color: #fff;
      text-shadow: 2px 2px #ff6f61;
    }

    .card {
      width: 60%;
      margin: 50px auto;
      background: #fff;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.3);
      transform: rotateY(10deg) rotateX(5deg);
      transition: transform 0.5s;
    }

    .card:hover {
      transform: rotateY(0deg) rotateX(0deg) scale(1.05);
    }

    .card p {
      font-size: 1.2em;
      line-height: 1.6;
      color: #333;
    }

    .heart {
      position: absolute;
      color: red;
      font-size: 24px;
      animation: fall 5s linear infinite;
    }

    @keyframes fall {
      0% { transform: translateY(-10vh); opacity: 1; }
      100% { transform: translateY(100vh); opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>🎉 Happy Birthday 🎉</h1>
  <div class="card">
    <p>
      Dear Friend,<br><br>
      Wishing you a magical birthday filled with love, laughter, and unforgettable memories.  
      May your year ahead sparkle with happiness and success! 💖
    </p>
  </div>

  <script>
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * window.innerWidth + "px";
      heart.style.top = "-20px";
      heart.style.fontSize = Math.random() * 20 + 20 + "px";
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>
