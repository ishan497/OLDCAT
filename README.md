<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>Shafna Is Getting Old 😼</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<style>
body {
  margin: 0;
  font-family: "Poppins", "Comic Sans MS", cursive;
  background: radial-gradient(circle at top, #ffe6f0, #ffd6a5, #fff);
  height: 100vh;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card {
  background: rgba(255,255,255,0.96);
  border-radius: 32px;
  padding: 30px;
  max-width: 460px;
  text-align: center;
  box-shadow: 0 25px 60px rgba(0,0,0,0.18);
  animation: float 5s ease-in-out infinite;
  z-index: 2;
}

@keyframes float {
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-14px)}
}

h1 {
  color: #ff5f87;
  font-size: 2.2rem;
}

.main-cat {
  font-size: 5.5rem;
  cursor: pointer;
  animation: wiggle 2s infinite;
}

@keyframes wiggle {
  0%,100%{transform:rotate(0)}
  25%{transform:rotate(7deg)}
  75%{transform:rotate(-7deg)}
}

button {
  margin: 6px;
  padding: 12px 20px;
  border: none;
  border-radius: 30px;
  cursor: pointer;
  font-size: 0.9rem;
  color: white;
  transition: 0.3s;
}

button:hover { transform: scale(1.08); }

.truth { background: linear-gradient(135deg,#ff6f91,#ff9671); }
.lie { background: linear-gradient(135deg,#7ed6df,#70a1ff); }
.scan { background: linear-gradient(135deg,#b983ff,#ff9ff3); }
.extra { background: linear-gradient(135deg,#feca57,#ff9f43); }

.message {
  margin-top: 15px;
  min-height: 55px;
  color: #ff5f87;
  font-size: 1rem;
}

/* Cats */
.bg-cat {
  position: absolute;
  font-size: 3rem;
  animation: walk linear infinite;
  cursor: pointer;
}

@keyframes walk {
  from { transform: translateX(-120px); }
  to { transform: translateX(110vw); }
}

.toast {
  position: fixed;
  bottom: 15px;
  right: 15px;
  background: white;
  padding: 10px 14px;
  border-radius: 15px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
  font-size: 0.9rem;
  display: none;
}
</style>
</head>

<body>

<!-- Walking cats -->
<div class="bg-cat" style="top:10%;animation-duration:18s;">🐈</div>
<div class="bg-cat" style="top:35%;animation-duration:22s;">🐈‍⬛</div>
<div class="bg-cat" style="top:65%;animation-duration:20s;">🐈</div>

<div class="card">
  <div class="main-cat" onclick="meow()">🐱</div>
  <h1>Shafna is getting old</h1>

  <p>Don’t panic 😌<br>It’s called <b>character development</b>.</p>

  <!-- Core teasing -->
  <button class="lie" onclick="lie()">Lie to me</button>
  <button class="truth" onclick="truth()">Tell me the truth</button>
  <button class="scan" onclick="scan()">Run age scanner 😈</button>

  <!-- Extra teasing -->
  <button class="extra" onclick="backInMyDay()">Back in my day…</button>
  <button class="extra" onclick="catJudge()">Ask cats</button>
  <button class="extra" onclick="catTime()">How cats see your age</button>
  <button class="extra" onclick="therapy()">Cat therapy</button>
  <button class="extra" onclick="youthQuestion()">Do you feel young?</button>
  <button class="extra" onclick="horoscope()">Cat horoscope</button>
  <button class="extra" onclick="tips()">Youth tips</button>

  <div class="message" id="message"></div>
</div>

<div class="toast" id="toast"></div>

<audio id="meowSound">
  <source src="https://www.myinstants.com/media/sounds/cat-meow.mp3">
</audio>

<script>
const msg = document.getElementById("message");
const toast = document.getElementById("toast");

function meow() {
  document.getElementById("meowSound").play();
  showToast("🔔 Reminder: stretch");
}

function lie() {
  show([
    "You haven’t aged at all 😇",
    "Scientists are confused by you ✨",
    "Age? Never heard of her."
  ]);
}

function truth() {
  show([
    "Still cute… just naps more 😏",
    "Your joints know things 🦴",
    "Wisdom unlocked. Energy pending 💤"
  ]);
}

function scan() {
  msg.innerText = "Loading… remembering youth ⏳";
  setTimeout(()=>msg.innerText="Retrieving teenage energy…",1200);
  setTimeout(()=>msg.innerText="Error: knees made a noise 😭",2200);
  setTimeout(()=>msg.innerText="Result: dangerously adorable 😈",3200);
}

function backInMyDay() {
  show([
    "Back in my day, phones had buttons.",
    "Back in my day, Wi-Fi wasn’t everywhere.",
    "Back in my day, we slept without pain."
  ]);
}

function catJudge() {
  show([
    "Cats discussed.",
    "Cats whispered.",
    "Verdict: still cute. Mandatory naps 🐾"
  ]);
}

function catTime() {
  msg.innerText = "To cats, you are ancient.\nBut warm. And useful.";
}

function therapy() {
  msg.innerText = "You are not old.\nYou are tired.\n— Cat Therapist 🐱";
}

function youthQuestion() {
  msg.innerText = "Correct answer: tired.";
}

function horoscope() {
  show([
    "Stars say: nap soon 🌙",
    "Avoid loud music after 10pm",
    "Luck improves after sleep 💤"
  ]);
}

function tips() {
  show([
    "Sleep before midnight (try).",
    "Stop calling back pain a joke.",
    "Drink water. Not vibes."
  ]);
}

function show(arr) {
  msg.innerText = arr[Math.floor(Math.random()*arr.length)];
}

function showToast(text) {
  toast.innerText = text;
  toast.style.display = "block";
  setTimeout(()=>toast.style.display="none",2000);
}
</script>

</body>
</html>
