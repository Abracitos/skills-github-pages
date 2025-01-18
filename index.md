<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Will You Be My Valentine?</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #ffe6f2;
      text-align: center;
      margin: 0;
      padding: 0;
    }

    h1 {
      color: #ff4d94;
      font-size: 3rem;
      margin-top: 50px;
    }

    p {
      color: #b30059;
      font-size: 1.2rem;
      margin-bottom: 40px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }

    .button {
      padding: 15px 30px;
      font-size: 1.2rem;
      border: none;
      border-radius: 25px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }

    .yes {
      background-color: #ff4d94;
      color: white;
    }

    .yes:hover {
      background-color: #e63977;
      transform: scale(1.1);
    }

    .no {
      background-color: #b30059;
      color: white;
      position: absolute;
    }

    .no:hover {
      left: calc(10% + (Math.random() * 80%));
      top: calc(10% + (Math.random() * 80%));
    }

    footer {
      margin-top: 50px;
      color: #b30059;
    }
  </style>
</head>
<body>
  <h1>Will You Be My Valentine? 💖</h1>
  <p>There's only one correct answer. 😊</p>

  <div class="buttons">
    <button class="button yes" onclick="showLoveMessage()">Yes! 💕</button>
    <button class="button no">No 😢</button>
  </div>

  <footer>
    <p>Made with love by Nikki 💌</p>
  </footer>

  <script>
    // Prevent the "No" button from being clicked
    const noButton = document.querySelector('.no');
    noButton.addEventListener('mouseover', () => {
      const randomX = Math.random() * (window.innerWidth - noButton.offsetWidth);
      const randomY = Math.random() * (window.innerHeight - noButton.offsetHeight);
      noButton.style.left = `${randomX}px`;
      noButton.style.top = `${randomY}px`;
    });

    // Function for the "Yes" button
    function showLoveMessage() {
      alert("Yay! I knew you'd say yes! 💖 You're the best Valentine ever! 🥰");
    }
  </script>
</body>
</html>
