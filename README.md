<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>For You 💖</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <div class="container fade-in">
    <h1>Hey you 🌷</h1>
    <p class="sub">
      This little space is just for you.
    </p>

    <div class="card slide-up">
      <p>No big reason…<br>just wanted to make you smile today ✨</p>
    </div>

    <div class="card slide-up delay1">
      <p>You make ordinary days feel special.</p>
    </div>

    <div class="card slide-up delay2">
      <p>Your smile has a way of making everything better 💗</p>
    </div>

    <button onclick="showMessage()">Tap here 💌</button>

    <p id="hiddenMsg" class="hidden">
      Always cheering for you,<br>
      in ways you may never notice 🌙
    </p>

    <footer>
      Made with care & a lot of smiles 🤍
    </footer>
  </div>

  <script src="script.js"></script>
</body>
</html>* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  background: linear-gradient(135deg, #ffd6e8, #c9f7ff);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Segoe UI', sans-serif;
}

.container {
  background: white;
  width: 90%;
  max-width: 360px;
  padding: 25px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 15px 40px rgba(0,0,0,0.15);
}

h1 {
  margin-bottom: 5px;
}

.sub {
  color: #666;
  margin-bottom: 20px;
}

.card {
  background: #fff5fa;
  margin: 12px 0;
  padding: 14px;
  border-radius: 15px;
  font-size: 15px;
}

button {
  margin-top: 15px;
  padding: 10px 18px;
  border: none;
  border-radius: 20px;
  background: #ff6f91;
  color: white;
  font-size: 14px;
  cursor: pointer;
}

button:hover {
  transform: scale(1.05);
}

.hidden {
  display: none;
  margin-top: 15px;
  font-size: 14px;
  color: #444;
}

footer {
  margin-top: 18px;
  font-size: 12px;
  color: #777;
}

/* Animations */
.fade-in {
  animation: fadeIn 1.2s ease;
}

.slide-up {
  animation: slideUp 1s ease forwards;
  opacity: 0;
}

.delay1 {
  animation-delay: 0.3s;
}

.delay2 {
  animation-delay: 0.6s;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes slideUp {
  from {
    transform: translateY(20px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}function showMessage() {
  document.getElementById("hiddenMsg").style.display = "block";
}
