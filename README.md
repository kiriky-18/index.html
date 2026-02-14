# index.html<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Heidi Alejandra ❣️</title>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg,#ff4d6d,#ff99ac);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.card {
  background: #f5e6da;
  width: 92%;
  max-width: 620px;
  border-radius: 20px;
  padding: 28px;
  box-shadow: 0 12px 30px rgba(0,0,0,.25);
  position: relative;
}

h2 {
  margin-top: 0;
}

.name {
  font-size: 22px;
  font-weight: bold;
  color: #c9184a;
}

.tree {
  position: absolute;
  right: 15px;
  bottom: 15px;
  font-size: 90px;
}

.hearts {
  position: absolute;
  right: 40px;
  bottom: 120px;
  font-size: 26px;
  animation: float 3s infinite ease-in-out;
}

@keyframes float {
  0% { transform: translateY(0); opacity: 1; }
  50% { transform: translateY(-18px); opacity: .7; }
  100% { transform: translateY(0); opacity: 1; }
}

.timer {
  margin-top: 18px;
  font-weight: bold;
  font-size: 15px;
  background: #fff;
  padding: 10px;
  border-radius: 12px;
}
button {
  margin-top: 15px;
  padding: 10px 18px;
  border: none;
  border-radius: 12px;
  background: #ff4d6d;
  color: white;
  font-size: 16px;
  cursor: pointer;
}
</style>
</head>

<body>

<div class="card">
  <h2>Para <span class="name">Heidi Alejandra</span> ❣️</h2>

  <p>
    Si pudiera elegir un lugar seguro, sería a tu lado.<br><br>
    Cuanto más tiempo estoy contigo más te amo.<br><br>
    Eres mi persona favorita, hoy y siempre.
  </p>

  <b>— Te amo ❣️</b>

  <div class="timer" id="timer"></div>

  <button onclick="playMusic()">Reproducir nuestra canción 🎵</button>

  <div class="hearts">❣️ ❣️ ❣️</div>
  <div class="tree">🌳</div>
</div>

<!-- 🎵 PON AQUÍ TU ARCHIVO MP3 -->
<audio id="song" loop>
  <source src="quimica-mayor.mp3" type="audio/mpeg">
</audio>

<script>
// Fecha inicio relación
const startDate = new Date("2025-02-23T00:00:00");

function updateTimer() {
  const now = new Date();
  const diff = now - startDate;

  const days = Math.floor(diff / (1000*60*60*24));
  const hours = Math.floor((diff / (1000*60*60)) % 24);
  const minutes = Math.floor((diff / (1000*60)) % 60);
  const seconds = Math.floor((diff / 1000) % 60);

  document.getElementById("timer").innerText =
    "Nuestro amor comenzó hace: " +
    days + " días " +
    hours + " horas " +
    minutes + " minutos " +
    seconds + " segundos ❣️";
}

setInterval(updateTimer, 1000);
updateTimer();

function playMusic(){
  document.getElementById("song").play();
}
</script>

</body>
</html>
