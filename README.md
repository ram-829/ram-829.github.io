<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>For Saumya 💗</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&family=Sacramento&display=swap" rel="stylesheet" />

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --pink-light: #ffe6f4;
      --pink-main: #ff8ac2;
      --pink-deep: #ff4b8b;
      --bg-dark: #170718;
      --text-main: #351227;
      --glass: rgba(255, 255, 255, 0.14);
    }

    body {
      min-height: 100vh;
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      background:
        radial-gradient(circle at top, #ffd9f2 0%, #ffb7dd 35%, #ff9ac2 55%, #f2629b 80%, #2a042f 100%);
      color: var(--text-main);
      overflow: hidden;
      position: relative;
    }

    /* Gradient blobs / glassy anime vibe */
    .blob {
      position: absolute;
      border-radius: 50%;
      filter: blur(18px);
      opacity: 0.9;
      mix-blend-mode: screen;
      animation: blobFloat 18s ease-in-out infinite alternate;
    }

    .blob.b1 {
      width: 360px;
      height: 360px;
      background: radial-gradient(circle at 30% 30%, #ff9bcf, #f24692);
      top: -80px;
      left: -40px;
    }

    .blob.b2 {
      width: 420px;
      height: 420px;
      background: radial-gradient(circle at 30% 30%, #ffc7eb, #ff8ac2);
      bottom: -120px;
      right: -40px;
      animation-delay: 1.4s;
    }

    .blob.b3 {
      width: 260px;
      height: 260px;
      background: radial-gradient(circle at 30% 30%, #ffeaf7, #ff9ad2);
      top: 50%;
      left: 65%;
      transform: translate(-50%, -50%);
      animation-delay: 2.6s;
    }

    @keyframes blobFloat {
      0% { transform: translate3d(0, 0, 0) scale(1); }
      50% { transform: translate3d(20px, -25px, 0) scale(1.05); }
      100% { transform: translate3d(-10px, 15px, 0) scale(1.02); }
    }

    /* Floating hearts */
    .floating-heart {
      position: absolute;
      font-size: 18px;
      animation: heartFloat 8s ease-in-out infinite;
      opacity: 0.8;
      pointer-events: none;
    }

    .floating-heart:nth-child(1) { top: 14%; left: 15%; animation-delay: 0s; }
    .floating-heart:nth-child(2) { top: 20%; right: 18%; animation-delay: 1.2s; }
    .floating-heart:nth-child(3) { bottom: 12%; left: 12%; animation-delay: 2.4s; }
    .floating-heart:nth-child(4) { bottom: 22%; right: 22%; animation-delay: 3.6s; }
    .floating-heart:nth-child(5) { top: 50%; left: 6%; animation-delay: 4.4s; }

    @keyframes heartFloat {
      0% { transform: translateY(0); opacity: 0.25; }
      40% { transform: translateY(-18px); opacity: 0.85; }
      80% { transform: translateY(-32px); opacity: 0.4; }
      100% { transform: translateY(0); opacity: 0.25; }
    }

    /* Main layout */
    .shell {
      position: relative;
      width: 100%;
      max-width: 960px;
      padding: 22px;
    }

    .card {
      position: relative;
      width: 100%;
      background: rgba(255, 255, 255, 0.14);
      border-radius: 26px;
      border: 1px solid rgba(255, 255, 255, 0.7);
      backdrop-filter: blur(22px);
      box-shadow:
        0 18px 40px rgba(88, 5, 52, 0.45),
        0 0 0 1px rgba(255, 255, 255, 0.35) inset;
      padding: 26px 26px 22px;
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      gap: 18px;
      overflow: hidden;
    }

    @media (max-width: 780px) {
      .card {
        grid-template-columns: minmax(0, 1fr);
        padding: 20px 16px 18px;
      }
    }

    /* Left side — title + main note + buttons */
    .left-col {
      display: flex;
      flex-direction: column;
      gap: 14px;
    }

    .tagline {
      font-size: 10px;
      letter-spacing: 2.2px;
      text-transform: uppercase;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: #ffecf7;
      opacity: 0.9;
    }

    .tag-dot {
      width: 9px;
      height: 9px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 30%, #fff, #ff4b8b);
      box-shadow: 0 0 10px rgba(255, 185, 220, 0.9);
    }

    .main-title {
      font-family: "Sacramento", cursive;
      font-size: 40px;
      letter-spacing: 0.8px;
      color: #fff5fb;
      text-shadow: 0 6px 14px rgba(82, 3, 46, 0.7);
      margin-top: 2px;
    }

    .subtitle {
      font-size: 13px;
      color: #fce5f5;
      opacity: 0.93;
      max-width: 360px;
    }

    .pill-info {
      margin-top: 8px;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 11px;
      padding: 5px 10px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.16);
      color: #fff;
    }

    .pill-info span.icon {
      font-size: 13px;
    }

    .main-note {
      margin-top: 12px;
      padding: 14px 14px;
      border-radius: 16px;
      background: linear-gradient(135deg, rgba(255, 240, 252, 0.9), rgba(255, 220, 244, 0.96));
      border: 1px dashed rgba(255, 150, 210, 0.8);
      font-size: 13px;
      line-height: 1.6;
      color: #491131;
    }

    .main-note .name {
      color: #ff2e7b;
      font-weight: 600;
    }

    .buttons-wrap {
      margin-top: 10px;
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 8px;
      max-width: 420px;
    }

    .love-btn {
      position: relative;
      border: none;
      border-radius: 14px;
      padding: 9px 6px;
      cursor: pointer;
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 6px;
      color: #fff;
      background: radial-gradient(circle at 0 0, #ffe3ff 0, #ff8ac2 28%, #f13f82 90%);
      box-shadow:
        0 6px 18px rgba(255, 30, 131, 0.5),
        0 0 0 1px rgba(255, 255, 255, 0.14) inset;
      transform: translateY(0);
      transition: transform 0.14s ease, box-shadow 0.14s ease, filter 0.14s ease;
    }

    .love-btn span.icon {
      font-size: 15px;
    }

    .love-btn.small {
      font-size: 10px;
      padding: 7px 4px;
    }

    .love-btn.sorry {
      background: radial-gradient(circle at 0 0, #ffe8d8 0, #ffac7a 28%, #f1665c 90%);
      box-shadow:
        0 6px 18px rgba(240, 90, 70, 0.5),
        0 0 0 1px rgba(255, 255, 255, 0.16) inset;
    }

    .love-btn:hover {
      transform: translateY(-1px);
      filter: brightness(1.05);
      box-shadow:
        0 10px 22px rgba(255, 30, 131, 0.55),
        0 0 0 1px rgba(255, 255, 255, 0.22) inset;
    }

    .love-btn:active {
      transform: translateY(1px) scale(0.97);
      filter: brightness(0.97);
      box-shadow:
        0 3px 10px rgba(255, 30, 131, 0.4),
        0 0 0 1px rgba(255, 255, 255, 0.18) inset;
    }

    /* Right side — letter box */
    .right-col {
      position: relative;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .note-card {
      position: relative;
      flex: 1;
      border-radius: 20px;
      background: rgba(255, 249, 254, 0.94);
      border: 1px solid rgba(255, 163, 210, 0.9);
      padding: 16px 16px 14px;
      overflow: hidden;
      box-shadow:
        0 14px 26px rgba(129, 17, 76, 0.38),
        0 0 0 1px rgba(255, 255, 255, 0.65) inset;
    }

    .note-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 6px;
    }

    .note-chip {
      font-size: 11px;
      padding: 4px 10px;
      border-radius: 999px;
      background: rgba(255, 188, 223, 0.7);
      color: #721a45;
    }

    .note-meta {
      font-size: 10px;
      color: #a64f7f;
      opacity: 0.9;
    }

    .note-body {
      margin-top: 6px;
      min-height: 110px;
      font-size: 13px;
      line-height: 1.7;
      color: #421129;
      white-space: pre-line;
    }

    .typing-cursor {
      display: inline-block;
      width: 2px;
      height: 14px;
      margin-left: 1px;
      background: #ff4b8b;
      vertical-align: middle;
      animation: blink 0.9s infinite;
    }

    @keyframes blink {
      0%, 50% { opacity: 1; }
      51%, 100% { opacity: 0; }
    }

    .note-footer {
      margin-top: 8px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 10px;
      color: #a14a7a;
    }

    .note-footer .label {
      display: inline-flex;
      align-items: center;
      gap: 5px;
      padding: 3px 8px;
      border-radius: 999px;
      background: rgba(255, 210, 236, 0.9);
    }

    .note-footer .tiny {
      opacity: 0.9;
    }

    .corner-heart {
      position: absolute;
      right: 12px;
      bottom: 10px;
      font-size: 18px;
      opacity: 0.4;
    }

    /* Bottom tiny text */
    .bottom-note {
      margin-top: 6px;
      font-size: 10px;
      color: #f6e0f1;
      opacity: 0.85;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .bottom-note span.highlight {
      color: #ffe9ff;
    }
  </style>
</head>
<body>
  <!-- background blobs -->
  <div class="blob b1"></div>
  <div class="blob b2"></div>
  <div class="blob b3"></div>

  <!-- floating hearts -->
  <div class="floating-heart">💗</div>
  <div class="floating-heart">💖</div>
  <div class="floating-heart">💕</div>
  <div class="floating-heart">💘</div>
  <div class="floating-heart">💞</div>

  <div class="shell">
    <div class="card">
      <!-- LEFT -->
      <div class="left-col">
        <div>
          <div class="tagline">
            <span class="tag-dot"></span>
            PRIVATE LITTLE UNIVERSE
          </div>
          <h1 class="main-title">For Saumya, with every heartbeat.</h1>
          <p class="subtitle">
            Har line, har button, har letter sirf itna hi prove karne ke liye hai:
            tum sirf special nahi ho, tum meri poori duniya ho.
          </p>
          <div class="pill-info">
            <span class="icon">🩷</span>
            <span>Tap any button &amp; read what my heart really feels.</span>
          </div>
        </div>

        <div class="main-note">
          Dear <span class="name">Saumya</span>,  
          kabhi kabhi shayad main words me perfect na ho paun,  
          isliye socha ek chhota sa digital space banaun,
          jahan tum jab bhi aao, tumhe wahi feel mile:
          ki koi hai jo tumhe loudly nahi, lekin *pure dil se* love karta hai – every single day.
        </div>

        <div class="buttons-wrap">
          <button class="love-btn" data-index="0">
            <span class="icon">❤️</span>
            LOVE 1
          </button>
          <button class="love-btn" data-index="1">
            <span class="icon">💘</span>
            LOVE 2
          </button>
          <button class="love-btn" data-index="2">
            <span class="icon">💖</span>
            LOVE 3
          </button>
          <button class="love-btn small" data-index="3">
            <span class="icon">💞</span>
            LOVE 4
          </button>
          <button class="love-btn small" data-index="4">
            <span class="icon">💕</span>
            LOVE 5
          </button>
          <button class="love-btn sorry small" data-index="5">
            <span class="icon">🥺</span>
            SORRY
          </button>
        </div>
      </div>

      <!-- RIGHT -->
      <div class="right-col">
        <div class="note-card">
          <div class="note-header">
            <div class="note-chip" id="noteLabel">Love letter 1 · just for you</div>
            <div class="note-meta" id="noteMeta">tap different buttons to open new letters</div>
          </div>

          <div class="note-body" id="typingText"></div>
          <span class="typing-cursor" id="cursor"></span>

          <div class="note-footer">
            <div class="label">
              <span>From me</span> · <span style="font-weight: 500;">to only you</span>
            </div>
            <div class="tiny">read slowly, feel deeply 🕊️</div>
          </div>

          <div class="corner-heart">⌣ ❤️</div>
        </div>

        <div class="bottom-note">
          <span>Built once, but meant to be read again and again.</span>
          <span class="highlight">Promise: it’s always you. ♾️</span>
        </div>
      </div>
    </div>
  </div>

  <script>
    const notes = [
`LOVE LETTER 1 🥹💗

Saumya, sach bolu to,
jab bhi apka naam screen par dikhta hai,
andar se ek ajeeb si shanti milti hai –
jaise din chahe kitna bhi random ho,
par end me sab theek ho jayega,
kyunki "tum ho".

Tum sirf meri life ka part nahi ho,
tum vo feeling ho jo life ko soft bana deti hai.`,

`LOVE LETTER 2 🌸

apki smile literally mera favourite aesthetic hai.
Na filter chahiye, na edit –
sirf tum normal hasi se bhi
mere poore mood ka vibe change ho jata hai.

Agar kabhi tumhe lage ki tum enough nahi ho,
to bas yaad rakhna:
mere liye tum always "more than enough" ho.`,

`LOVE LETTER 3 ✨

Agar kabhi future ka sochta hoon,
to scene kuch aisa hota hai:
normal din, normal ghar, normal moments –
bas ek cheez special hoti hai: tum ho.

Mujhe expensive cheeze nahi chahiye,
mujhe sirf vo daily chhote-chhote moments chahiye
jahan main tumhe dekh kar sochu:
"haan, yehi meri jagah hai."`,

`LOVE LETTER 4 🌙

Late night chats,
random jealousy,
thode se fights,
phir "achha theek hai, gussa mat ho" type patch-up –
ye sab cheeze cute isliye lagti hain
kyunki end me hum dono phir se
ek dusre ko choose kar lete hain.

Mere liye love ka matlab perfect couple nahi,
love ka matlab hai:
hum dono, apni saari imperfections ke saath,
phir bhi ek dusre ke saath rehna choose karte rahna.`,

`LOVE LETTER 5 💌

Kabhi kabhi sochta hoon,
agar mere dil ke andar jo feelings chalti hain
vo direct screen par type ho sake,
to shayad yeh page kabhi khatam hi na ho.

Short version me bas itna:
I’m proud of you,
I’m soft for you,
and I’m madly in love with you,
Saumya.`,

`SORRY LETTER 🥺💔

Saumya, meri har galti ke liye
genuinely, honestly sorry.

Jab mera dil heavy ho jata hai,
ya emotions control se bahar ho jate hain,
tab main kabhi kabhi aise react kar deta hoon
jo bilkul bhi theek nahi hota –
especially tumhare liye.

Tumhe hurt karna kabhi intention nahi hota,
par jab tum upset hoti ho,
mujhe lagta hai jaise main hi
apne favourite insaan ko tod raha hoon.
Aur ye thought hi sabse zyada dard deta hai.

Please meri uss version ko maaf kar dena
jo kabhi kabhi impulsive ho jata hai,
aur us version ko ek chance dena
jo seekhne, sudharne aur
tumhare liye better banne ki poori koshish kar raha hai.

Tum meri life ka sabse gentle,
sabse precious part ho.
Main promise nahi kar sakta ki
kabhi bhi galti nahi hogi,
par itna zaroor promise kar sakta hoon
ki har galti ke baad main aur zyada
mature, patient aur careful banne ki try karunga –
sirf tumhare liye.

I’m really, deeply sorry, Saumya.
And I love you – more than these words, more than this page, more than you can imagine. ♾️`
    ];

    const typingTextEl = document.getElementById("typingText");
    const cursorEl = document.getElementById("cursor");
    const noteLabelEl = document.getElementById("noteLabel");
    const noteMetaEl = document.getElementById("noteMeta");
    const buttons = document.querySelectorAll(".love-btn");

    let typingInterval = null;

    function startTyping(text) {
      clearInterval(typingInterval);
      typingTextEl.textContent = "";
      cursorEl.style.display = "inline-block";

      let i = 0;
      typingInterval = setInterval(() => {
        if (i < text.length) {
          typingTextEl.textContent += text.charAt(i);
          i++;
        } else {
          clearInterval(typingInterval);
        }
      }, 26);
    }

    buttons.forEach(btn => {
      btn.addEventListener("click", () => {
        const idx = parseInt(btn.getAttribute("data-index"), 10);

        if (idx === 5) {
          noteLabelEl.textContent = "Sorry letter · from a very guilty heart";
          noteMetaEl.textContent = "read this slowly, and please… thoda sa maaf bhi kar dena";
        } else {
          noteLabelEl.textContent = "Love letter " + (idx + 1) + " · just for you";
          noteMetaEl.textContent = "tap different buttons to open new letters";
        }

        if ("vibrate" in navigator) {
          navigator.vibrate(80);
        }

        startTyping(notes[idx]);
      });
    });

    window.addEventListener("load", () => {
      noteLabelEl.textContent = "Love letter 1 · just for you";
      startTyping(notes[0]);
    });
  </script>
</body>
</html>
