# Jia-website<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Romantic Love Page</title>
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@500;700&family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      height: 100vh;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: linear-gradient(to bottom right, #ffe6eb, #ffd6e0);
      font-family: 'Poppins', sans-serif;
      text-align: center;
    }
  </style>
</head>
<body>

  <h1>“Aku mencintaimu selamanya ❤️”</h1>
  <button id="loveBtn">Klik untuk kejutan</button>

  <div class="popup" id="popup">
    <h2>“Kamu adalah alasan aku tersenyum setiap hari 💕”</h2>
  </div>

  <script>
  
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.textContent = '❤️';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (3 + Math.random() * 2) + 's';
      heart.style.fontSize = (12 + Math.random() * 24) + 'px';
      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 5000);
    }

    setInterval(createHeart, 300);

    // Popup kejutan
    const btn = document.getElementById('loveBtn');
    const popup = document.getElementById('popup');

    btn.addEventListener('click', () => {
      popup.classList.add('show');
      setTimeout(() => popup.classList.remove('show'), 3000);
    });
  </script>
</body>
</html>
