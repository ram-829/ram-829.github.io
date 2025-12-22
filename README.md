<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Saumya ❤️ Special</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Poppins", sans-serif;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at top, #ffe3f1 0%, #ffc1dc 35%, #ff9ac2 60%, #ff7da9 100%);
      overflow: hidden;
      position: relative;
      color: #3b0b2f;
    }

    .heart {
      position: absolute;
      width: 180px;
      height: 180px;
      background: radial-gradient(circle at 30% 30%, #ff4b6e, #ff0033);
      transform: rotate(-45deg);
      filter: blur(8px);
      opacity: 0.25;
      z-index: 0;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 180px;
      height: 180px;
      background: radial-gradient(circle at 30% 30%, #ff4b6e, #ff0033);
      border-radius: 50%;
    }

    .heart::before { top: -90px; left: 0; }
    .heart::after { left: 90px; top: 0; }

    .heart.h1 { top: -40px; left: -40px; }
    .heart.h2 { bottom: -60px; right: -20px; transform: rotate(-30deg); }
    .heart.h3 { top: 50%; left: 70%; transform: translate(-50%, -50%) rotate(-55deg); }

    .floating-heart {
      position: absolute;
      font-size: 18px;
      animation: float 6s ease-in-out infinite;
      opacity: 0.7;
    }

    .floating-heart:nth-child(1) { top: 10%; left: 20%; animation-delay: 0s; }
    .floating-heart:nth-child(2) { top: 20%; right: 15%; animation-delay: 1s; }
    .floating-heart:nth-child(3) { bottom: 15%; left: 10%; animation-delay: 2s; }
    .floating-heart:nth-child(4) { bottom: 25%; right: 25%; animation-delay: 3s; }
    .floating-heart:nth-child(5) { top: 50%; left: 5%; animation-delay: 4s; }

    @keyframes float {
      0% { transform: translateY(0); opacity: 0.4; }
      50% { transform: translateY(-15px); opacity: 1; }
      100% { transform: translateY(0); opacity: 0.4; }
    }

    .container {
      position: relative;
      z-index: 2;
      width: 95%;
      max-width: 900px;
      background: rgba(255, 255, 255, 0.86);
      border-radius: 24px;
      box-shadow: 0 18px 40px rgba(255, 0, 90, 0.25);
      padding: 24px 20px 26px;
      border: 1px solid rgba(255, 255, 255, 0.8);
      backdrop-filter: blur(14px);
    }

    .header {
      text-align: center;
      margin-bottom: 16px;
    }

    .tag {
      display: inline-block;
      padding: 4px 12px;
      border-radius: 999px;
      background: rgba(255, 143, 187, 0.3);
      font-size: 10px;
      letter-spacing: 2px;
      text-transform: uppercase;
      margin-bottom: 6px;
    }

    .title {
      font-size: 24px;
      font-weight: 600;
      color: #b1005d;
      margin-bottom: 2px;
    }

    .subtitle {
      font-size: 13px;
      color: #7a415e;
    }

    .main-note {
      margin: 14px auto 18px;
      max-width: 640px;
      padding: 14px 18px;
      background: linear-gradient(135deg, #ffe5f3 0%, #ffeef8 100%);
      border-radius: 16px;
      border: 1px dashed rgba(255, 105, 180, 0.6);
      font-size: 14px;
      text-align: center;
      line-height: 1.5;
    }

    .main-note span.name {
      color: #ff2e7b;
      font-weight: 600;
    }

    .buttons-row {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 10px;
      margin: 0 auto;
      max-width: 600px;
    }

    .love-btn {
      position: relative;
      padding: 10px 6px;
      border-radius: 14px;
      border: none;
      cursor: pointer;
      font-size: 12px;
      font-weight: 500;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      background: linear-gradient(135deg, #ff9ac2 0%, #ff4b8b 100%);
      color: #fff;
      box-shadow: 0 6px 14px rgba(255, 0, 90, 0.35);
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      transition: transform 0.12s ease, box-shadow 0.12s ease, filter 0.12s ease;
    }

    .love-btn span.icon { font-size: 16px; }

    .love-btn.small {
      font-size: 11px;
      padding: 8px 4px;
    }

    .love-btn.sorry {
      background: linear-gradient(135deg, #ffc48c 0%, #ff7c6a 100%);
      box-shadow: 0 6px 14px rgba(255, 94, 58, 0.35);
    }

    .love-btn:active {
      transform: scale(0.96);
      filter: brightness(0.97);
      box-shadow: 0 3px 9px rgba(255, 0, 90, 0.28);
    }

    .note-box {
      margin: 20px auto 0;
      max-width: 640px;
      min-height: 130px;
      padding: 14px 16px 16px;
      background: #fff9fd;
      border-radius: 18px;
      border: 1px solid rgba(255, 158, 204, 0.75);
      position: relative;
      overflow: hidden;
    }

    .note-label {
      position: absolute;
      top: 10px;
      right: 14px;
      font-size: 11px;
      color: #ff4b8b;
      opacity: 0.9;
    }

    .typing-text {
      font-size: 14px;
      line-height: 1.6;
      color: #4b1037;
      white-space: pre-line;
      min-height: 70px;
    }

    .typing-cursor {
      display: inline-block;
      width: 2px;
      height: 14px;
      margin-left: 2px;
      background: #ff4b8b;
      animation: blink 0.9s infinite;
      vertical-align: middle;
    }

    @keyframes blink {
      0%, 50% { opacity: 1; }
      51%, 100% { opacity: 0; }
    }

    .note-footer {
      margin-top: 8px;
      font-size: 11px;
      color: #a14a7a;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .note-footer .badge {
      padding: 3px 8px;
      border-radius: 999px;
      background: rgba(255, 188, 217, 0.5);
      font-size: 10px;
    }

    .note-footer .mini {
      font-size: 10px;
      opacity: 0.85;
    }

    .music-hint {
      position: absolute;
      left: 16px;
      bottom: 10px;
      font-size: 11px;
      color: #924269;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .music-hint span.dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: #ff4b8b;
      box-shadow: 0 0 8px rgba(255, 75, 139, 0.7);
      animation: pulse 1.4s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(1); opacity: 1; }
      70% { transform: scale(1.5); opacity: 0.2; }
      100% { transform: scale(1); opacity: 1; }
    }

    @media (max-width: 600px) {
      .container { padding: 18px 14px 20px; }
      .title { font-size: 20px; }
      .main-note { font-size: 13px; padding: 12px 14px; }
      .typing-text { font-size: 13px; }
      .buttons-row { gap: 8px; }
    }
  </style>
</head>
<body>

  <div class="heart h1"></div>
  <div class="heart h2"></div>
  <div class="heart h3"></div>

  <div class="floating-heart">💗</div>
  <div class="floating-heart">💕</div>
  <div class="floating-heart">💘</div>
  <div class="floating-heart">💞</div>
  <div class="floating-heart">💖</div>

  <!-- Cute calm English instrumental love song -->
  <audio id="bgMusic" loop>
    <source src="love-song.mp3" type="audio/mpeg" />
  </audio>

  <div class="container">
    <div class="header">
      <div class="tag">FOR MY FAVORITE HUMAN</div>
      <div class="title">Saumya, you are my world 💖</div>
      <div class="subtitle">Tiny website, big feelings – every letter here is a piece of my heart for you.</div>
    </div>

    <div class="main-note">
      Dear <span class="name">Saumya</span>,  
      ye chhota sa cute sa page isliye banaya hai,
      taaki jab bhi tumhe doubt ho na ki
      “koi mujhe itna deeply love karta hai ya nahi”,
      tum yahan aao aur feel karo:
      haan, koi karta hai – aur woh main hoon. 🤍
    </div>

    <div class="buttons-row">
      <button class="love-btn" data-index="0">
        <span class="icon">❤️</span> LOVE 1
      </button>
      <button class="love-btn" data-index="1">
        <span class="icon">💘</span> LOVE 2
      </button>
      <button class="love-btn" data-index="2">
        <span class="icon">💖</span> LOVE 3
      </button>
      <button class="love-btn small" data-index="3">
        <span class="icon">💞</span> LOVE 4
      </button>
      <button class="love-btn small" data-index="4">
        <span class="icon">💕</span> LOVE 5
      </button>
      <button class="love-btn sorry" data-index="5">
        <span class="icon">🥺</span> SORRY NOTE
      </button>
    </div>

    <div class="note-box">
      <div class="note-label" id="noteLabel">Tap any button 💌</div>
      <div class="typing-text" id="typingText"></div>
      <span class="typing-cursor" id="cursor"></span>

      <div class="note-footer">
        <div class="badge">From: the one who chooses you, everyday ♾️</div>
        <div class="mini">Alag–alag buttons tap karo, har baar naya letter milega ✨</div>
      </div>
    </div>

    <div class="music-hint">
      <span class="dot"></span>
      <span>Headphones on karo, soft English love song ke saath read karo… 🎧</span>
    </div>
  </div>

  <script>
    const notes = [
      `LOVE LETTER 1 🥹💗

Saumya, do you know something?
When I say "I love you", it’s not just a line.
It means: you are my safe place,
my soft corner, my favorite human in this entire world.

Tumhare bina bhi jee sakta hoon shayad,
par tumhare saath life actually jeene jaisi lagti hai.`,

      `LOVE LETTER 2 🌸

Your smile feels like a warm song on a cold day.
Thoda sa tum hasta na, to dil ke andar
ek cute sa "click" hota hai –
jaise universe bol raha ho: "yahi hai, yahi sahi hai."

Tumhari eyes, tumhari baatein, tumhara care –
sab milke mujhe yeh feel karwate hain
ki main genuinely lucky hoon, because I have you.`,

      `LOVE LETTER 3 ✨

If I could explain my love in one line,
it would be: “You feel like home.”

Chahe din kitna bhi messy ho,
chahe mood kitna bhi off ho,
tumhara naam phone pe dekhte hi
andar se ek calm sa, soft sa feeling aata hai,
jaise sab theek ho jayega, bas tum ho na.`,

      `LOVE LETTER 4 🌙

I don’t want perfect moments,
I want real moments with you –
late night talks,
random reels,
stupid fights,
aur phir ek tight sa sorry hug.

Mere liye romantic ka matlab sirf roses nahi,
romantic ka matlab hai:
tum + main + honest feelings, bas.`,

      `LOVE LETTER 5 💌

Kabhi kabhi sochta hoon,
agar dil me jo feel hota hai
vo words me properly likh paun,
to shayad pura ek novel ban jaye
sirf "I love you, Saumya" explain karne ke liye.

Bas itna jaan lo:
no matter kitna time badalta rahe,
mere liye "best decision" hamesha tum hi rahogi.`,

      `SORRY LETTER 🥺💔

Saumya, from the deepest part of my heart – I am sorry.

Kabhi kabhi mera dil heavy ho jata hai,
emotions control se bahar ho jate hain,
aur uss time main shayad
aise words bol deta hoon
ya aise react kar deta hoon
jo tum bilkul deserve nahi karti.

Intention kabhi bhi tumhe hurt karna nahi hota,
par phir bhi jab tum hurt hoti ho,
sabse zyada dard mujhe hi hota hai,
because "tum theek nahi ho" = "main theek nahi hoon".

Please meri har galti ke liye
mujhe dil se maaf kar dena –
chahe vo chhoti ho ya badi,
old ho ya recent.

Main honestly try kar raha hoon
ki main better version bannu,
jo tumhare liye hamesha soft, patient aur understanding rahe.

Tum meri life ka sabse precious part ho,
aur main nahi chahta
ki meri wajah se tumhari aankhon me kabhi aansu aaye.

I am really, really sorry, Saumya.
And I love you – today, tomorrow, and always. ♾️`
    ];

    const typingTextEl = document.getElementById("typingText");
    const cursorEl = document.getElementById("cursor");
    const noteLabelEl = document.getElementById("noteLabel");
    const buttons = document.querySelectorAll(".love-btn");
    const audio = document.getElementById("bgMusic");

    let charIndex = 0;
    let typingInterval = null;

    function startTyping(text) {
      clearInterval(typingInterval);
      typingTextEl.textContent = "";
      charIndex = 0;
      cursorEl.style.display = "inline-block";

      typingInterval = setInterval(() => {
        if (charIndex < text.length) {
          typingTextEl.textContent += text.charAt(charIndex);
          charIndex++;
        } else {
          clearInterval(typingInterval);
          cursorEl.style.display = "inline-block";
        }
      }, 30);
    }

    buttons.forEach(btn => {
      btn.addEventListener("click", () => {
        const idx = parseInt(btn.getAttribute("data-index"), 10);

        if (idx === 5) {
          noteLabelEl.textContent = "Sorry letter from a very guilty heart 🥺";
        } else {
          noteLabelEl.textContent = "Love letter " + (idx + 1) + " just for you 💗";
        }

        if ("vibrate" in navigator) {
          navigator.vibrate(80);
        }

        startTyping(notes[idx]);

        if (audio && audio.paused && audio.querySelector("source")) {
          audio.play().catch(() => {});
        }
      });
    });

    window.addEventListener("load", () => {
      startTyping(notes[0]);
      noteLabelEl.textContent = "Love letter 1 just for you 💗";
    });
  </script>
</body>
</html>
