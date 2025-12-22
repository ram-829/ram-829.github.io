# ram-829.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Saumya — From Ram</title>

<style>
body {
  margin: 0;
  min-height: 100vh;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(to bottom, #070b1e, #141a40);
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Stars */
.star {
  position: absolute;
  width: 2px;
  height: 2px;
  background: white;
  border-radius: 50%;
  animation: twinkle 2s infinite alternate;
}

@keyframes twinkle {
  from { opacity: 0.3; }
  to { opacity: 1; }
}

/* Shooting Star */
.shooting-star {
  position: absolute;
  font-size: 16px;
  animation: shoot 1.3s linear forwards;
  pointer-events: none;
}

@keyframes shoot {
  from {
    transform: translate(0,0) scale(1);
    opacity: 1;
  }
  to {
    transform: translate(140px,-140px) scale(0.2);
    opacity: 0;
  }
}

/* Card */
.container {
  position: relative;
  z-index: 10;
  background: rgba(255,255,255,0.12);
  backdrop-filter: blur(10px);
  width: 92%;
  max-width: 500px;
  padding: 30px;
  border-radius: 30px;
  text-align: center;
  box-shadow: 0 25px 60px rgba(0,0,0,0.45);
}

.heart {
  font-size: 36px;
  animation: beat 1.4s infinite;
}

@keyframes beat {
  0% { transform: scale(1); }
  50% { transform: scale(1.35); }
  100% { transform: scale(1); }
}

h1 {
  color: #ffd7e5;
  margin: 10px 0 5px;
}

.subtitle {
  font-size: 14px;
  color: #d6d6f5;
}

p {
  font-size: 14px;
  color: #e6e6ff;
  margin-top: 14px;
}

.buttons {
  margin-top: 22px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
}

button {
  border: none;
  background: #ff7fa1;
  color: white;
  padding: 12px;
  border-radius: 16px;
  font-size: 14px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #ff4f7b;
  transform: scale(1.07);
}

.note-box {
  margin-top: 26px;
  padding: 18px;
  min-height: 110px;
  background: rgba(255,255,255,0.18);
  border-radius: 18px;
  font-size: 15px;
  color: #ffffff;
  line-height: 1.7;
  font-style: italic;
}

footer {
  margin-top: 18px;
  font-size: 12px;
  color: #cfcfff;
}
</style>
</head>

<body>

<!-- Background Music -->
<audio autoplay loop>
  <source src="music.mp3" type="audio/mpeg">
</audio>

<!-- Stars -->
<script>
for(let i=0;i<100;i++){
  const star=document.createElement("div");
  star.className="star";
  star.style.top=Math.random()*100+"%";
  star.style.left=Math.random()*100+"%";
  star.style.animationDuration=(Math.random()*3+1)+"s";
  document.body.appendChild(star);
}
</script>

<div class="container">
  <div class="heart">🤍</div>

  <h1>Saumya</h1>
  <div class="subtitle">From Ram — always gentle</div>

  <p>
    Tap anywhere to make a wish ✨  
    Open letters slowly 🤍
  </p>

  <div class="buttons">
    <button onclick="showNote(0)">Letter 1</button>
    <button onclick="showNote(1)">Letter 2</button>
    <button onclick="showNote(2)">Letter 3</button>
    <button onclick="showNote(3)">Letter 4</button>
    <button onclick="showNote(4)">Letter 5</button>
    <button onclick="showNote(5)">Letter 6</button>
  </div>

  <div class="note-box" id="note">
    🌌 Waiting quietly…
  </div>

  <footer>
    Love that doesn’t force. Only stays.
  </footer>
</div>

<script>
/* Shooting stars + vibration */
document.addEventListener("click", function(e){
  const star = document.createElement("div");
  star.className = "shooting-star";
  star.innerText = "✨";
  star.style.left = e.clientX + "px";
  star.style.top = e.clientY + "px";
  document.body.appendChild(star);

  if(navigator.vibrate){
    navigator.vibrate(30);
  }

  setTimeout(()=>star.remove(),1300);
});

/* Notes typing */
const notes = [
`Saumya, even silence feels softer
when my heart remembers you.`,

`I don’t need constant talks.
Just knowing you’re okay
is already enough.`,

`Whatever we shared was real.
Those moments still feel warm.`,

`I respect your choices,
your pace, your dreams.`,

`Care doesn’t disappear.
It simply learns to stay quiet.`,

`I’m sorry for every time
my emotions felt heavy.
Everything came from love.
— Ram`
];

let typing;
function showNote(i){
  clearInterval(typing);
  const box=document.getElementById("note");
  box.innerText="";
  let t=notes[i], x=0;
  typing=setInterval(()=>{
    box.innerText+=t.charAt(x);
    x++;
    if(x>=t.length) clearInterval(typing);
  },35);
}
</script>

</body>
</html>
