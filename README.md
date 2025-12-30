<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Happy New Year, Saumya ♡</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --bg1: #0b1024;
      --bg2: #26163f;
      --bg3: #43235f;
      --soft-pink: #ffb6d5;
      --soft-purple: #c6a4ff;
      --soft-blue: #96c5ff;
      --card-bg: rgba(15, 12, 35, 0.82);
      --accent: #ffd6f6;
      --text-main: #fdf7ff;
      --text-soft: #f3e3ff;
      --glass: rgba(255, 255, 255, 0.06);
      --border-soft: rgba(255, 255, 255, 0.18);
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.65);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      min-height: 100vh;
      color: var(--text-main);
      background: radial-gradient(circle at top, #283b84 0, transparent 55%),
        radial-gradient(circle at 20% 80%, #522658 0, transparent 55%),
        linear-gradient(135deg, var(--bg1), var(--bg3));
      overflow-x: hidden;
    }

    /* soft moving background stars / hearts */
    .floating-particles {
      position: fixed;
      inset: 0;
      overflow: hidden;
      pointer-events: none;
      z-index: 0;
    }

    .particle {
      position: absolute;
      width: 12px;
      height: 12px;
      background: radial-gradient(circle, #ffd6f6 0, transparent 70%);
      opacity: 0.7;
      border-radius: 50%;
      animation: floatUp 18s linear infinite;
      filter: blur(0.5px);
    }

    .particle.heart {
      width: 14px;
      height: 14px;
      background: none;
      position: absolute;
    }

    .particle.heart::before,
    .particle.heart::after {
      content: "";
      position: absolute;
      width: 8px;
      height: 12px;
      background: radial-gradient(circle at 30% 30%, #ffd6f6 0, #ff9fd0 45%, transparent 70%);
      border-radius: 8px 8px 0 0;
    }

    .particle.heart::before {
      transform: rotate(-45deg);
      transform-origin: 0 100%;
      left: 4px;
    }

    .particle.heart::after {
      transform: rotate(45deg);
      transform-origin: 100% 100%;
      left: 0;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(100vh) translateX(0);
        opacity: 0;
      }
      10% {
        opacity: 0.5;
      }
      90% {
        opacity: 0.5;
      }
      100% {
        transform: translateY(-10vh) translateX(12px);
        opacity: 0;
      }
    }

    /* subtle moving road / horizon */
    .midnight-road {
      position: fixed;
      inset: auto 0 0 0;
      height: 40vh;
      background: linear-gradient(to top, rgba(2, 3, 10, 0.95), transparent),
        repeating-linear-gradient(
          -8deg,
          rgba(255, 255, 255, 0.04),
          rgba(255, 255, 255, 0.04) 2px,
          transparent 2px,
          transparent 12px
        );
      mask-image: linear-gradient(to top, black 0, transparent 70%);
      z-index: 0;
    }

    .road-line {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      bottom: 0;
      width: 2px;
      height: 100%;
      background: linear-gradient(
        to top,
        rgba(255, 255, 255, 0),
        rgba(255, 255, 255, 0.6),
        rgba(255, 255, 255, 0)
      );
      opacity: 0.6;
      filter: blur(0.5px);
    }

    .fairy-lights {
      position: fixed;
      top: 0;
      left: 0;
      width: 120%;
      transform: translateX(-10%);
      height: 120px;
      background-image: radial-gradient(circle, #ffd6f6 0, transparent 60%),
        radial-gradient(circle, #c6a4ff 0, transparent 60%),
        radial-gradient(circle, #96c5ff 0, transparent 60%);
      background-size: 40px 40px;
      background-position: 0 40px, 20px 70px, 40px 50px;
      opacity: 0.5;
      mix-blend-mode: screen;
      filter: blur(1px);
      animation: lightsWaves 16s ease-in-out infinite;
      pointer-events: none;
      z-index: 1;
    }

    @keyframes lightsWaves {
      0%,
      100% {
        transform: translateX(-10%) translateY(0);
      }
      50% {
        transform: translateX(-6%) translateY(4px);
      }
    }

    .overlay-gradient {
      position: fixed;
      inset: 0;
      background: radial-gradient(circle at 10% 0, rgba(255, 182, 213, 0.16), transparent 60%),
        radial-gradient(circle at 90% 20%, rgba(150, 197, 255, 0.16), transparent 60%);
      mix-blend-mode: screen;
      pointer-events: none;
      z-index: 0;
    }

    main {
      position: relative;
      z-index: 2;
      max-width: 960px;
      margin: 0 auto;
      padding: 26px 18px 40px;
      display: flex;
      flex-direction: column;
      gap: 26px;
    }

    @media (min-width: 768px) {
      main {
        padding: 46px 28px 64px;
        gap: 32px;
      }
    }

    .glass-card {
      background: linear-gradient(135deg, rgba(255, 255, 255, 0.14), rgba(255, 255, 255, 0.02));
      border-radius: 24px;
      border: 1px solid var(--border-soft);
      box-shadow: var(--shadow-soft);
      padding: 20px 18px 22px;
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
      position: relative;
      overflow: hidden;
    }

    @media (min-width: 768px) {
      .glass-card {
        padding: 26px 24px 32px;
      }
    }

    .glass-card::before {
      content: "";
      position: absolute;
      inset: -40%;
      background: radial-gradient(circle at 0 0, rgba(255, 182, 213, 0.18), transparent 60%),
        radial-gradient(circle at 100% 0, rgba(198, 164, 255, 0.2), transparent 60%);
      opacity: 0.6;
      pointer-events: none;
    }

    .glass-inner {
      position: relative;
      z-index: 1;
    }

    .title-line {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 8px;
    }

    .title-main {
      font-size: 1.5rem;
      font-weight: 700;
      letter-spacing: 0.02em;
      color: var(--text-main);
    }

    .title-chip {
      font-size: 0.8rem;
      padding: 3px 9px;
      border-radius: 999px;
      background: rgba(10, 8, 28, 0.78);
      border: 1px solid rgba(255, 214, 246, 0.42);
      color: var(--accent);
      display: inline-flex;
      align-items: center;
      gap: 4px;
    }

    .title-chip span {
      font-size: 0.75rem;
      opacity: 0.9;
    }

    .subtitle {
      font-size: 0.9rem;
      color: var(--text-soft);
      opacity: 0.88;
      margin-bottom: 6px;
    }

    .subtitle strong {
      font-weight: 600;
    }

    .main-message {
      margin-top: 16px;
      font-size: 0.96rem;
      line-height: 1.8;
      color: var(--text-soft);
      position: relative;
    }

    @media (min-width: 768px) {
      .title-main {
        font-size: 1.9rem;
      }
      .subtitle {
        font-size: 1rem;
      }
      .main-message {
        font-size: 1.02rem;
      }
    }

    .message-line {
      opacity: 0;
      transform: translateY(8px);
      animation: fadeInUp 0.8s ease forwards;
    }

    .message-line:nth-child(1) {
      animation-delay: 0.1s;
    }
    .message-line:nth-child(2) {
      animation-delay: 0.4s;
    }
    .message-line:nth-child(3) {
      animation-delay: 0.8s;
    }
    .message-line:nth-child(4) {
      animation-delay: 1.2s;
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(8px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .typing-cursor {
      display: inline-block;
      width: 1px;
      background: rgba(255, 255, 255, 0.78);
      margin-left: 3px;
      animation: cursorBlink 1.1s steps(1) infinite;
      vertical-align: baseline;
    }

    @keyframes cursorBlink {
      0%,
      50% {
        opacity: 1;
      }
      50.01%,
      100% {
        opacity: 0;
      }
    }

    /* Love notes */
    .notes-section-title {
      font-size: 1.15rem;
      font-weight: 600;
      margin-bottom: 6px;
      color: var(--text-main);
    }

    .notes-hint {
      font-size: 0.86rem;
      color: var(--text-soft);
      opacity: 0.82;
      margin-bottom: 14px;
    }

    .notes-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
      margin-bottom: 18px;
    }

    @media (min-width: 640px) {
      .notes-grid {
        grid-template-columns: repeat(3, minmax(0, 1fr));
      }
    }

    @media (min-width: 900px) {
      .notes-grid {
        grid-template-columns: repeat(4, minmax(0, 1fr));
      }
    }

    .note-btn {
      position: relative;
      border: none;
      outline: none;
      cursor: pointer;
      padding: 10px 8px 12px;
      border-radius: 18px;
      background: radial-gradient(circle at 0 0, rgba(255, 182, 213, 0.22), transparent 60%),
        radial-gradient(circle at 100% 100%, rgba(150, 197, 255, 0.26), transparent 60%),
        rgba(14, 8, 40, 0.92);
      border: 1px solid rgba(255, 214, 246, 0.38);
      color: var(--text-main);
      font-size: 0.8rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 6px;
      transition: transform 0.15s ease-out, box-shadow 0.15s ease-out,
        border-color 0.15s ease-out, background 0.18s ease-out;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.65);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
    }

    .note-btn span.emoji {
      font-size: 1.1rem;
      filter: drop-shadow(0 0 4px rgba(255, 255, 255, 0.4));
    }

    .note-btn span.label {
      opacity: 0.95;
    }

    .note-btn span.index {
      font-size: 0.7rem;
      opacity: 0.7;
      letter-spacing: 0.04em;
    }

    .note-btn:hover {
      transform: translateY(-3px) scale(1.02);
      box-shadow: 0 16px 40px rgba(0, 0, 0, 0.78);
      border-color: rgba(255, 255, 255, 0.75);
    }

    .note-btn:active {
      transform: translateY(0) scale(0.99);
      box-shadow: 0 10px 26px rgba(0, 0, 0, 0.75);
    }

    .note-btn.active {
      border-color: #ffffff;
      background: radial-gradient(circle at 10% 0, rgba(255, 214, 246, 0.46), transparent 60%),
        radial-gradient(circle at 100% 80%, rgba(150, 197, 255, 0.42), transparent 60%),
        rgba(14, 8, 40, 0.96);
    }

    .note-display {
      position: relative;
      margin-top: 2px;
      padding: 14px 12px 16px;
      border-radius: 18px;
      border: 1px solid rgba(255, 214, 246, 0.45);
      background: radial-gradient(circle at 0 0, rgba(255, 182, 213, 0.1), transparent 60%),
        radial-gradient(circle at 100% 100%, rgba(150, 197, 255, 0.12), transparent 60%),
        rgba(5, 3, 16, 0.92);
      min-height: 115px;
      overflow: hidden;
    }

    @media (min-width: 768px) {
      .note-display {
        padding: 18px 16px 20px;
        min-height: 130px;
      }
    }

    .note-display-label {
      font-size: 0.78rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: rgba(255, 246, 255, 0.78);
      opacity: 0.8;
      margin-bottom: 6px;
    }

    .note-display-text {
      font-size: 0.9rem;
      line-height: 1.8;
      color: var(--text-soft);
      white-space: pre-wrap;
      position: relative;
    }

    .note-placeholder {
      opacity: 0.7;
      font-size: 0.87rem;
    }

    /* fireworks */
    .fireworks-layer {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 3;
      overflow: visible;
    }

    .firework {
      position: absolute;
      width: 4px;
      height: 4px;
      border-radius: 50%;
      opacity: 0;
      background: radial-gradient(circle, #ffd6f6 0, transparent 70%);
      box-shadow: 0 0 10px rgba(255, 255, 255, 0.9);
      animation: boom 1.6s ease-out forwards;
    }

    .firework::before,
    .firework::after {
      content: "";
      position: absolute;
      inset: 0;
      border-radius: 50%;
      background: inherit;
    }

    .firework::before {
      transform: scale(1.6);
      opacity: 0.7;
    }

    .firework::after {
      transform: scale(2.1);
      opacity: 0.45;
    }

    @keyframes boom {
      0% {
        transform: scale(0.2);
        opacity: 0;
      }
      15% {
        opacity: 1;
      }
      60% {
        opacity: 0.95;
      }
      100% {
        transform: scale(1.9);
        opacity: 0;
      }
    }

    .firework.trail {
      width: 2px;
      height: 16px;
      border-radius: 999px;
      background: linear-gradient(
        to top,
        rgba(255, 255, 255, 0),
        rgba(255, 255, 255, 0.8),
        rgba(255, 255, 255, 0)
      );
      animation: trailUp 0.9s ease-out forwards;
      box-shadow: none;
    }

    @keyframes trailUp {
      0% {
        transform: translateY(20px);
        opacity: 0;
      }
      30% {
        opacity: 0.9;
      }
      100% {
        transform: translateY(-18px);
        opacity: 0;
      }
    }

    /* small footer text */
    .footer-text {
      margin-top: 6px;
      font-size: 0.78rem;
      color: rgba(247, 238, 255, 0.75);
      text-align: right;
      opacity: 0.8;
    }

    .footer-text span {
      color: var(--soft-pink);
    }
  </style>
</head>
<body>
  <!-- dreamy moving background -->
  <div class="floating-particles" id="particles"></div>
  <div class="midnight-road">
    <div class="road-line"></div>
  </div>
  <div class="fairy-lights"></div>
  <div class="overlay-gradient"></div>
  <div class="fireworks-layer" id="fireworks"></div>

  <main>
    <!-- MAIN NEW YEAR WISH -->
    <section class="glass-card">
      <div class="glass-inner">
        <div class="title-line">
          <h1 class="title-main">Happy New Year, Saumya 🤍</h1>
          <div class="title-chip">
            ✨
            <span>midnight, soft &amp; real</span>
          </div>
        </div>
        <p class="subtitle">
          Ek <strong>chhota sa</strong> saal‑ka‑pehla letter, sirf tumhare liye.
        </p>

        <div class="main-message" id="mainMessage">
          <p class="message-line" data-full-text="Yeh naya saal tumhari zindagi me shanti, strength aur khushiyan le aaye."></p>
          <p class="message-line" data-full-text="Main bas yeh kehna chahta hoon ke main hamesha aapke saath hoon — har situation me, har phase me."></p>
          <p class="message-line" data-full-text="Jaise aaj tumse pyaar karta hoon, waise hi hamesha karta rahunga — simple, pure aur dil se."></p>
        </div>

        <p class="footer-text">
          from <span>someone</span> jisko tum pehle se zyada matter karti ho.
        </p>
      </div>
    </section>

    <!-- INTERACTIVE LOVE NOTES -->
    <section class="glass-card">
      <div class="glass-inner">
        <h2 class="notes-section-title">11 chhoti‑chhoti love notes 💌</h2>
        <p class="notes-hint">
          Har envelope me ek alag feeling hai. Jo tum open karogi, woh sirf tumhare liye type hoga — dheere, araam se.
        </p>

        <div class="notes-grid">
          <!-- 11 buttons -->
          <button class="note-btn" data-index="0">
            <span class="emoji">✉️</span>
            <span class="label">Soft roshni</span>
            <span class="index">note 01</span>
          </button>
          <button class="note-btn" data-index="1">
            <span class="emoji">💌</span>
            <span class="label">Respect &amp; pyaar</span>
            <span class="index">note 02</span>
          </button>
          <button class="note-btn" data-index="2">
            <span class="emoji">✨</span>
            <span class="label">Comfort thought</span>
            <span class="index">note 03</span>
          </button>
          <button class="note-btn" data-index="3">
            <span class="emoji">🌙</span>
            <span class="label">Teri muskaan</span>
            <span class="index">note 04</span>
          </button>
          <button class="note-btn" data-index="4">
            <span class="emoji">📖</span>
            <span class="label">Real moments</span>
            <span class="index">note 05</span>
          </button>
          <button class="note-btn" data-index="5">
            <span class="emoji">💟</span>
            <span class="label">Tu ek feeling</span>
            <span class="index">note 06</span>
          </button>
          <button class="note-btn" data-index="6">
            <span class="emoji">🤍</span>
            <span class="label">Bina expectation</span>
            <span class="index">note 07</span>
          </button>
          <button class="note-btn" data-index="7">
            <span class="emoji">🌌</span>
            <span class="label">Dil ki jagah</span>
            <span class="index">note 08</span>
          </button>
          <button class="note-btn" data-index="8">
            <span class="emoji">🕊️</span>
            <span class="label">Soft future</span>
            <span class="index">note 09</span>
          </button>
          <button class="note-btn" data-index="9">
            <span class="emoji">💫</span>
            <span class="label">Deep feeling</span>
            <span class="index">note 10</span>
          </button>
          <button class="note-btn" data-index="10">
            <span class="emoji">🎆</span>
            <span class="label">Tera hi dil</span>
            <span class="index">note 11</span>
          </button>
        </div>

        <div class="note-display">
          <p class="note-display-label">OPEN LETTER</p>
          <div class="note-display-text">
            <span class="note-placeholder">
              Jo envelope tum touch karogi, ussi moment se ek naya note tumhare liye type hona shuru ho jayega.
            </span>
            <span class="typing-cursor" id="noteCursor" style="display:none;"></span>
          </div>
        </div>
      </div>
    </section>
  </main>

  <script>
    // --- floating particles (stars + hearts) ---
    (function createParticles() {
      const container = document.getElementById("particles");
      const total = 28;
      for (let i = 0; i < total; i++) {
        const el = document.createElement("div");
        const isHeart = Math.random() < 0.45;
        el.className = "particle" + (isHeart ? " heart" : "");
        const left = Math.random() * 100;
        const delay = Math.random() * -18;
        const duration = 16 + Math.random() * 10;
        const size = 8 + Math.random() * 10;
        el.style.left = left + "vw";
        el.style.animationDuration = duration + "s";
        el.style.animationDelay = delay + "s";
        if (!isHeart) {
          el.style.width = size + "px";
          el.style.height = size + "px";
          el.style.opacity = 0.35 + Math.random() * 0.4;
        }
        container.appendChild(el);
      }
    })();

    // --- typing for main New Year message (line by line) ---
    const mainLines = document.querySelectorAll("#mainMessage .message-line");
    const typingSpeedMain = 40;

    function typeLine(el, text, index, cb) {
      el.textContent = "";
      let i = 0;
      function step() {
        if (i <= text.length) {
          el.textContent = text.slice(0, i);
          i++;
          setTimeout(step, typingSpeedMain);
        } else if (typeof cb === "function") {
          cb();
        }
      }
      step();
    }

    function typeMainSequential(lines, idx = 0) {
      if (idx >= lines.length) return;
      const el = lines[idx];
      const text = el.getAttribute("data-full-text") || "";
      typeLine(el, text, idx, () => typeMainSequential(lines, idx + 1));
    }

    window.addEventListener("load", () => {
      setTimeout(() => typeMainSequential(mainLines), 650);
    });
// --- notes content ---
    const notes = [
      "Tumhari presence meri zindagi me ek soft si roshni ki tarah hai — jo zyada dikhai nahi deti, par andheron me bhi raasta dikha deti hai. Tumhari baatein, tumhari soch, sab kuch mujhe shant karta hai.",
      "Main tumse sirf pyaar nahi karta, main tumhari respect karta hoon. Tumhare decisions, tumhare sapne aur tumhari growth mere liye bahut important hain.",
      "Kabhi-kabhi baatein kam hoti hain, par mere dil me tumhari jagah kabhi kam nahi hoti. Tumhara khayal aana bhi mere liye ek comfort hota hai.",
      "Tumhari khushi meri priority hai. Agar tum muskurati ho, toh mujhe lagta hai jaise sab kuch theek hai — bina kisi wajah ke.",
      "Main tumhare saath har moment ko perfect banane ki koshish nahi karta, bas real rehna chahta hoon — jahan pyaar ho, samajh ho aur patience ho.",
      "Tum mere liye sirf ek person nahi ho, tum ek feeling ho — jo dheere-dheere strong hoti gayi aur kabhi kam nahi hui.",
      "Main tumse bina kisi expectation ke pyaar karta hoon. Bas yeh chahta hoon ke jo connection aur care humare beech hai, woh bana rahe.",
      "Tumhari importance meri zindagi me words se zyada hai. Kabhi bolta hoon, kabhi chup rehta hoon — par dil hamesha tumhara hi khayal rakhta hai.",
      "Chahe future jo bhi ho, jo bhi pace ho — mera pyaar tumhare liye hamesha soft, genuine aur loyal rahega.",
      "Main tumse bahut pyaar karta hoon, Saumya. Yeh pyaar time pass nahi, ek deep feeling hai jo main har din mehsoos karta hoon — bina kisi shor ke.",
      "Tum mere dil ke bahut kareeb ho. Main tumhe khona nahi chahta, kyunki jo jagah tumne meri zindagi me banayi hai, woh koi aur kabhi nahi bhar sakta."
    ];

    const buttons = document.querySelectorAll(".note-btn");
    const noteDisplay = document.querySelector(".note-display-text");
    const notePlaceholder = document.querySelector(".note-placeholder");
    const noteCursor = document.getElementById("noteCursor");

    let typingTimeout = null;
    let currentIndex = -1;

    function clearTyping() {
      if (typingTimeout) {
        clearTimeout(typingTimeout);
        typingTimeout = null;
      }
    }

    function startNoteTyping(text) {
      clearTyping();
      noteDisplay.innerHTML = "";
      const span = document.createElement("span");
      noteDisplay.appendChild(span);
      noteDisplay.appendChild(noteCursor);
      noteCursor.style.display = "inline-block";
      const chars = text.split("");
      let i = 0;

      function step() {
        if (i <= chars.length) {
          span.textContent = chars.slice(0, i).join("");
          i++;
          typingTimeout = setTimeout(step, 26);
        } else {
          noteCursor.style.display = "inline-block";
        }
      }
      step();
    }

    buttons.forEach((btn) => {
      btn.addEventListener("click", () => {
        const idx = parseInt(btn.getAttribute("data-index"), 10);
        if (idx === currentIndex) return;
        currentIndex = idx;

        buttons.forEach((b) => b.classList.remove("active"));
        btn.classList.add("active");

        if (notePlaceholder) notePlaceholder.remove();

        const text = notes[idx] || "";
        startNoteTyping(text);
        triggerFireworks();
      });
    });

    // --- soft fireworks when a note opens ---
    const fireworksLayer = document.getElementById("fireworks");

    function createSingleFirework() {
      const fw = document.createElement("div");
      fw.className = "firework";
      const x = 20 + Math.random() * 60; // between 20 and 80 vw
      const y = 15 + Math.random() * 40; // between 15 and 55 vh
      fw.style.left = x + "vw";
      fw.style.top = y + "vh";

      const hue = 270 + Math.random() * 40; // soft purples/pinks
      fw.style.background = `radial-gradient(circle, hsl(${hue},90%,85%) 0, transparent 70%)`;
      fw.style.boxShadow = `0 0 14px hsla(${hue},100%,90%,0.95)`;

      fireworksLayer.appendChild(fw);
      setTimeout(() => fw.remove(), 1700);

      const trail = document.createElement("div");
      trail.className = "firework trail";
      trail.style.left = x + "vw";
      trail.style.top = y + 18 + "vh";
      fireworksLayer.appendChild(trail);
      setTimeout(() => trail.remove(), 1000);
    }

    function triggerFireworks() {
      const bursts = 3 + Math.floor(Math.random() * 3);
      for (let i = 0; i < bursts; i++) {
        setTimeout(createSingleFirework, i * 180);
      }
    }
  </script>
</body>
</html>
    
