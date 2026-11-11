<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Mannuu ♡</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=Playfair+Display:ital,wght@0,500;0,600;1,500&display=swap');

:root {
  --pink: #f5c4d3;
  --dark-pink: #cc7795;
  --cream: #fff9f7;
  --text: #684b57;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--cream);
  color: var(--text);
  overflow-x: hidden;
}

button {
  font: inherit;
  cursor: pointer;
}

.background {
  position: fixed;
  inset: 0;
  z-index: -1;
  pointer-events: none;
  background:
    radial-gradient(circle at 10% 15%, #fce0e9 0, transparent 35%),
    radial-gradient(circle at 90% 70%, #f4d9eb 0, transparent 35%),
    #fff9f7;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 22px 7%;
}

.logo {
  font-family: 'Playfair Display', serif;
  font-size: 21px;
}

.music-btn {
  border: 1px solid #edc5d2;
  background: #fff8fa;
  color: var(--text);
  padding: 10px 16px;
  border-radius: 30px;
  font-size: 12px;
  transition: .3s;
}

.music-btn:hover {
  background: #f9dce6;
  transform: translateY(-2px);
}

.hero {
  min-height: 78vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 45px 22px 65px;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 4px;
  font-size: 10px;
  color: #b78397;
  margin-bottom: 22px;
}

h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(48px, 10vw, 90px);
  font-weight: 500;
  line-height: 1.1;
  color: #b96888;
}

h1 span {
  font-style: italic;
  color: #d995ad;
}

.subtitle {
  margin-top: 23px;
  font-size: 14px;
  line-height: 1.9;
  color: #987786;
}

.main-btn {
  margin-top: 30px;
  background: #d98eaa;
  color: white;
  border: none;
  padding: 15px 26px;
  border-radius: 30px;
  box-shadow: 0 8px 25px #e7b7c9;
  transition: .3s;
}

.main-btn:hover {
  transform: translateY(-3px);
  background: #c87998;
}

.tiny-note {
  margin-top: 15px;
  font-size: 11px;
  color: #b39aa4;
}

section {
  padding: 75px 22px;
  text-align: center;
}

.section-label {
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 3px;
  color: #bd8499;
  margin-bottom: 15px;
}

h2 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(30px, 6vw, 43px);
  font-weight: 500;
  margin-bottom: 14px;
}

.section-desc {
  font-size: 13px;
  line-height: 1.9;
  color: #9d8290;
  max-width: 420px;
  margin: 0 auto 35px;
}

.notes {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 17px;
  max-width: 850px;
  margin: auto;
}

.note {
  min-height: 180px;
  border: 1px solid #f0d5df;
  border-radius: 18px;
  background: rgba(255,255,255,.72);
  padding: 24px 13px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 15px;
  box-shadow: 0 8px 25px #dfb8c21c;
  transition: .3s;
}

.note:hover {
  transform: translateY(-5px) rotate(-1deg);
  background: #fff0f5;
}

.note .emoji {
  font-size: 30px;
}

.note h3 {
  font-family: 'Playfair Display', serif;
  font-size: 17px;
  font-weight: 500;
}

.note small {
  font-size: 10px;
  color: #b28b9a;
}

#messageArea {
  display: none;
  max-width: 520px;
  margin: 28px auto 0;
  padding: 30px 24px;
  background: #fff;
  border: 1px solid #f2d3df;
  border-radius: 20px;
  animation: appear .4s ease;
}

#messageArea p {
  font-family: 'Playfair Display', serif;
  font-size: 20px;
  line-height: 1.8;
  font-style: italic;
}

#messageArea button {
  margin-top: 18px;
  border: none;
  background: #fae4ec;
  padding: 9px 16px;
  border-radius: 20px;
  color: #895b6d;
  font-size: 12px;
}

.letter-section {
  background: linear-gradient(180deg, #fff4f7, #fff9f7);
}

.envelope {
  width: min(310px, 85vw);
  min-height: 195px;
  margin: 35px auto 20px;
  border: 1px solid #edc3d2;
  background: #f9dce6;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 12px;
  box-shadow: 0 12px 30px #d7a6b51f;
  transition: .3s;
}

.envelope:hover {
  transform: translateY(-4px);
}

.envelope .heart {
  font-size: 38px;
}

.envelope span:last-child {
  font-family: 'Playfair Display', serif;
  font-size: 21px;
}

.letter {
  display: none;
  max-width: 550px;
  margin: 30px auto 0;
  padding: 30px;
  background: #fff;
  border-radius: 5px;
  border: 1px solid #f0d8e0;
  text-align: left;
  line-height: 2;
  font-size: 14px;
  animation: appear .5s ease;
}

.letter h3 {
  font-family: 'Playfair Display', serif;
  font-size: 26px;
  margin-bottom: 15px;
  font-weight: 500;
}

.letter p + p {
  margin-top: 13px;
}

.question-card {
  max-width: 480px;
  margin: 30px auto 0;
  padding: 35px 22px;
  background: #fff;
  border: 1px solid #f0d5df;
  border-radius: 20px;
}

.question-card h3 {
  font-family: 'Playfair Display', serif;
  font-size: 24px;
  font-weight: 500;
  line-height: 1.6;
}

.answers {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 24px;
}

.answers button {
  padding: 12px 18px;
  border-radius: 25px;
  border: 1px solid #eac6d3;
  background: #fff4f7;
  color: #8e6072;
}

#answer {
  margin-top: 24px;
  line-height: 1.9;
  font-size: 14px;
}

footer {
  padding: 40px 20px;
  text-align: center;
  color: #ae8c9b;
  font-size: 11px;
  line-height: 2;
}

footer .footer-heart {
  color: #d98eaa;
  font-size: 20px;
}

.floating-heart {
  position: fixed;
  bottom: -30px;
  color: #e7a6bd;
  opacity: .7;
  pointer-events: none;
  z-index: 5;
  animation: floatUp linear forwards;
}

@keyframes floatUp {
  to {
    transform: translateY(-110vh) rotate(35deg);
    opacity: 0;
  }
}

@keyframes appear {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

@media (max-width: 600px) {
  nav { padding: 18px 5%; }
  .logo { font-size: 18px; }
  .music-btn { padding: 9px 12px; }
  .hero { min-height: 72vh; }
  .notes { grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 11px; }
  .note { min-height: 155px; padding: 17px 8px; }
  .note h3 { font-size: 15px; }
  section { padding: 60px 17px; }
  .letter { padding: 22px; }
}
</style>
</head>

<body>
<div class="background"></div>

<nav>
  <div class="logo">Mannuu ♡</div>
  <button class="music-btn" id="musicBtn" onclick="toggleMusic()">
    ♫ Play a little music
  </button>
</nav>

<main>
  <header class="hero">
    <p class="eyebrow">a tiny corner of the internet</p>

    <h1>For <span>Mannuu.</span></h1>

    <p class="subtitle">
      Not a confession. Not a love letter.<br>
      Just something I made. That's all. ♡
    </p>

    <button class="main-btn" onclick="goToNotes()">
      Nothing to see here ↗
    </button>

    <p class="tiny-note">and definitely nothing I'm trying to say</p>
  </header>

  <section id="notesSection">
    <p class="section-label">little things, apparently</p>
    <h2>Things I don't say.</h2>
    <p class="section-desc">
      Some thoughts are easier to hide in little boxes.
      Tap whichever one you want. 🎀
    </p>

    <div class="notes">
      <button class="note" onclick="showMessage(0)">
        <span class="emoji">🌷</span>
        <h3>Just a thought</h3>
        <small>tap to open</small>
      </button>

      <button class="note" onclick="showMessage(1)">
        <span class="emoji">☁️</span>
        <h3>Randomly...</h3>
        <small>tap to open</small>
      </button>

      <button class="note" onclick="showMessage(2)">
        <span class="emoji">🧸</span>
        <h3>One small thing</h3>
        <small>tap to open</small>
      </button>

      <button class="note" onclick="showMessage(3)">
        <span class="emoji">🌙</span>
        <h3>Late at night</h3>
        <small>tap to open</small>
      </button>

      <button class="note" onclick="showMessage(4)">
        <span class="emoji">🩷</span>
        <h3>If you knew</h3>
        <small>tap to open</small>
      </button>

      <button class="note" onclick="showMessage(5)">
        <span class="emoji">🦋</span>
        <h3>Anyway...</h3>
        <small>tap to open</small>
      </button>
    </div>

    <div id="messageArea" aria-live="polite">
      <p id="messageText"></p>
      <button onclick="closeMessage()">Okay, enough feelings ♡</button>
    </div>
  </section>

  <section class="letter-section">
    <p class="section-label">definitely not a letter</p>
    <h2>Something I won't say.</h2>
    <p class="section-desc">
      There's a little envelope here. It's probably nothing.
    </p>

    <button class="envelope" onclick="openLetter()">
      <span class="heart">💌</span>
      <span>For your eyes only</span>
      <small>tap to unfold</small>
    </button>

    <article class="letter" id="letter">
      <h3>Hey, Mannuu.</h3>

      <p>
        I don't really know why I made this.
        Maybe I had some free time. Maybe I just felt like it.
        Who knows? :)
      </p>

      <p>
        It's a little weird how someone can become such a familiar
        part of your days, and then suddenly there are things you
        want to tell them but don't know how anymore.
      </p>

      <p>
        Sometimes I come across something and think,
        "He would've laughed at this."
        And for a second, I forget that things aren't the same.
      </p>

      <p>
        I'm not asking for anything. You don't have to say anything
        back. I just wanted to leave these words somewhere.
      </p>

      <p>
        I hope life's being kind to you, genuinely.
        Take care of yourself, okay?
      </p>

      <p style="text-align:right; margin-top:24px;">
        anyway, that's enough from me ♡
      </p>
    </article>
  </section>

  <section>
    <p class="section-label">one last thing</p>
    <h2>A very important question.</h2>
    <p class="section-desc">
      Completely unrelated to anything above, obviously.
    </p>

    <div class="question-card">
      <h3>
        If an old memory made you smile today,
        would you smile a little longer?
      </h3>

      <div class="answers">
        <button onclick="answerQuestion('yes')">Maybe, yeah ♡</button>
        <button onclick="answerQuestion('no')">I'm not answering 😭</button>
      </div>

      <p id="answer" aria-live="polite"></p>
    </div>
  </section>
</main>

<footer>
  <div class="footer-heart">♡</div>
  made with a little pink and a little too much thinking.<br>
  that's all. seriously.
</footer>

<script>
// Hidden messages
const messages = [
  "It's funny how the smallest things can remind you of someone.",
  "I saw something today that I would've told you about. Old habits, I guess.",
  "I hope you're eating properly, sleeping enough, and taking care of yourself.",
  "Some nights are a little quieter than others. That's all I'm saying.",
  "Maybe I don't say it, but some memories still mean a lot to me.",
  "Anyway, don't let this website give you any ideas. 🙄🩷"
];

function showMessage(index) {
  const area = document.getElementById("messageArea");
  document.getElementById("messageText").textContent = messages[index];
  area.style.display = "block";
  area.scrollIntoView({ behavior: "smooth", block: "nearest" });
}

function closeMessage() {
  document.getElementById("messageArea").style.display = "none";
}

function goToNotes() {
  document.getElementById("notesSection").scrollIntoView({
    behavior: "smooth"
  });
}

// Envelope letter
function openLetter() {
  const letter = document.getElementById("letter");
  const isOpen = letter.style.display === "block";

  letter.style.display = isOpen ? "none" : "block";

  if (!isOpen) {
    letter.scrollIntoView({ behavior: "smooth", block: "nearest" });
  }
}

// Final question
function answerQuestion(choice) {
  const answer = document.getElementById("answer");

  if (choice === "yes") {
    answer.textContent =
      "Yeah... some memories deserve a little smile. That's all. 🌷";
  } else {
    answer.textContent =
      "HAHA okay, keep your secrets then. I wasn't curious anyway. 🙄♡";
  }
}

// Gentle floating hearts
function createHeart() {
  const heart = document.createElement("span");
  heart.className = "floating-heart";
  heart.textContent = Math.random() > 0.5 ? "♡" : "✧";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.fontSize = (12 + Math.random() * 18) + "px";
  heart.style.animationDuration = (7 + Math.random() * 6) + "s";

  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 14000);
}

setInterval(createHeart, 1100);

// Built-in gentle melody: no music file needed
let audioContext = null;
let musicTimer = null;
let noteIndex = 0;
let musicPlaying = false;

const melody = [
  523.25, 659.25, 587.33, 493.88,
  523.25, 392.00, 440.00, 493.88
];

function playNote() {
  if (!audioContext || !musicPlaying) return;

  const oscillator = audioContext.createOscillator();
  const gain = audioContext.createGain();

  oscillator.type = "sine";
  oscillator.frequency.value = melody[noteIndex % melody.length];

  gain.gain.setValueAtTime(0.0001, audioContext.currentTime);
  gain.gain.exponentialRampToValueAtTime(
    0.045, audioContext.currentTime + 0.08
  );
  gain.gain.exponentialRampToValueAtTime(
    0.0001, audioContext.currentTime + 0.7
  );

  oscillator.connect(gain);
  gain.connect(audioContext.destination);

  oscillator.start();
  oscillator.stop(audioContext.currentTime + 0.75);

  noteIndex++;
}

async function toggleMusic() {
  const btn = document.getElementById("musicBtn");

  if (musicPlaying) {
    musicPlaying = false;
    clearInterval(musicTimer);
    musicTimer = null;
    btn.textContent = "♫ Play a little music";

    if (audioContext && audioContext.state === "running") {
      await audioContext.suspend();
    }
    return;
  }

  try {
    if (!audioContext) {
      const AudioContextClass =
        window.AudioContext || window.webkitAudioContext;

      if (!AudioContextClass) {
        btn.textContent = "Music isn't supported here";
        return;
      }

      audioContext = new AudioContextClass();
    }

    await audioContext.resume();

    musicPlaying = true;
    btn.textContent = "♫ Pause the music";

    playNote();
    musicTimer = setInterval(playNote, 650);
  } catch (error) {
    btn.textContent = "Tap to try music again";
  }
}
</script>
</body>
</html>
