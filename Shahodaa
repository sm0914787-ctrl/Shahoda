
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Letter for You 💌</title>

<style>
* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 24px 16px;
  font-family: Arial, sans-serif;
  text-align: center;
  color: #713b50;
  background: linear-gradient(135deg, #ffe5ef, #fff4f7, #ffd6e4);
  overflow-x: hidden;
}

.card {
  width: 100%;
  max-width: 420px;
  background: rgba(255,255,255,.91);
  padding: 30px 22px;
  border-radius: 25px;
  box-shadow: 0 12px 40px #c85f8020;
  border: 1px solid #ffffff;
  position: relative;
  z-index: 2;
}

.envelope { font-size: 65px; }

h1 {
  font-size: 27px;
  color: #d94f7d;
  margin: 12px 0;
}

p {
  line-height: 2;
  font-size: 16px;
}

button {
  border: none;
  border-radius: 30px;
  padding: 13px 22px;
  margin: 8px 4px;
  font-size: 15px;
  font-weight: bold;
  cursor: pointer;
  background: #e85b89;
  color: white;
  box-shadow: 0 5px 12px #e85b8930;
}

button:active { transform: scale(.97); }

.secondary {
  background: #fff0f5;
  color: #c84170;
  border: 1px solid #f5c1d2;
}

#letter {
  display: none;
  animation: appear .8s ease;
}

#musicArea {
  display: none;
  margin-top: 18px;
}

#musicArea audio {
  width: 100%;
}

.heart {
  position: fixed;
  bottom: -30px;
  pointer-events: none;
  animation: floatUp 5s linear forwards;
  z-index: 1;
}

@keyframes floatUp {
  to {
    transform: translateY(-110vh) rotate(25deg);
    opacity: 0;
  }
}

@keyframes appear {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}

footer {
  margin-top: 22px;
  font-size: 12px;
  color: #b87b91;
}
</style>
</head>

<body>
<main class="card">
  <div class="envelope">💌</div>

  <h1>A Letter for You</h1>
  <p>في حاجة صغيرة عايز/ة أقولها لك... ❤️</p>

  <button id="openBtn" onclick="openLetter()">
    اضغط هنا يا جميل 💗
  </button>

  <section id="letter">
    <p>
      مش لازم يكون فيه مناسبة عشان أقولك إنك شخص مميز عندي 🥹❤️
    </p>

    <p>
      وجودك بيفرق، وكلامك بيخلّي اليوم ألطف،
      وضحكتك من الحاجات اللي بتفرّحني.
      أتمنى دايمًا تفضل مبسوط،
      وتكون أيامك كلها راحة وفرحة.
    </p>

    <p>دي رسالة صغيرة، بس معمولة بكل حب ليك 🎀</p>

    <p>With love, just for you 💕</p>

    <button onclick="toggleMusic()">🎵 تشغيل الأغنية</button>

    <div id="musicArea">
      <p>أغنيتنا 🎶</p>
      <audio id="song" controls preload="none">
        <source src="song.mp3" type="audio/mpeg">
        المتصفح لا يدعم تشغيل الصوت.
      </audio>
      <p style="font-size:12px">
        لو الأغنية مش شغالة، تأكدي إن ملف الصوت مضاف للموقع.
      </p>
    </div>
  </section>

  <footer>Made with love ♡</footer>
</main>

<script>
function openLetter() {
  document.getElementById("letter").style.display = "block";
  document.getElementById("openBtn").style.display = "none";
  makeHearts();
}

function makeHearts() {
  for (let i = 0; i < 22; i++) {
    setTimeout(() => {
      const heart = document.createElement("span");
      heart.className = "heart";
      heart.textContent = ["💗", "💕", "❤️", "💖", "🎀"][
        Math.floor(Math.random() * 5)
      ];
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.fontSize = (16 + Math.random() * 20) + "px";
      heart.style.animationDuration = (3 + Math.random() * 3) + "s";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6500);
    }, i * 130);
  }
}

async function toggleMusic() {
  const area = document.getElementById("musicArea");
  const song = document.getElementById("song");

  area.style.display = "block";

  if (song.paused) {
    try {
      await song.play();
    } catch (error) {
      alert("أضيفي ملف song.mp3 المسموح باستخدامه إلى ملفات الموقع، ثم جرّبي تاني.");
    }
  } else {
    song.pause();
  }
}
</script>
</body>
</html>
