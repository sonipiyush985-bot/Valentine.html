<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Be My Valentine, Rasmalai 💝</title>
  <meta name="description" content="A valentine invite from Piyush to Rasmalai." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg1:#0f0c29; --bg2:#302b63; --bg3:#24243e;
      --rose:#ff4d6d; --rose-soft:#ff8fab; --gold:#ffd166; --white:#fff;
      --glass: rgba(255,255,255,0.12);
      --shadow: 0 10px 30px rgba(0,0,0,0.35);
    }
    *{box-sizing:border-box}
    html,body{
      height:100%;
      margin:0;
      font-family: "Poppins", system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      color: var(--white);
      overflow-x:hidden;
      background: radial-gradient(1200px 900px at 10% 10%, #3f355c 0%, transparent 60%) ,
                  radial-gradient(900px 700px at 90% 90%, #3f355c 0%, transparent 60%),
                  linear-gradient(135deg, var(--bg1), var(--bg2) 50%, var(--bg3));
    }
    .container{
      min-height:100%;
      display:flex;
      align-items:center;
      justify-content:center;
      padding: clamp(16px, 3vw, 32px);
      position:relative;
      isolation:isolate;
    }
    .card{
      width:min(920px, 96vw);
      background: linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.02));
      border: 1px solid rgba(255,255,255,0.15);
      border-radius: 24px;
      box-shadow: var(--shadow);
      backdrop-filter: blur(10px);
      padding: clamp(18px, 5vw, 36px);
      position:relative;
      overflow:hidden;
    }
    .glow{
      position:absolute;
      inset:-40%;
      background: radial-gradient(closest-side, rgba(255,77,109,0.25), transparent 70%);
      filter: blur(40px);
      z-index:-1;
      animation: pulse 6s ease-in-out infinite;
    }
    @keyframes pulse{
      0%,100%{transform: scale(1)}
      50%{transform: scale(1.08)}
    }
    header{
      text-align:center;
      margin-bottom: clamp(16px, 3vw, 24px);
    }
    .script{
      font-family: "Great Vibes", cursive;
      font-size: clamp(28px, 6vw, 64px);
      color: var(--rose);
      text-shadow: 0 6px 30px rgba(255,77,109,0.35);
      line-height:1.05;
      margin: 8px 0;
    }
    .subtitle{
      font-weight:300;
      opacity:0.9;
      letter-spacing:0.2px;
      margin-top: 6px;
    }
    .message{
      margin: 18px 0 26px;
      font-size: clamp(14px, 2.2vw, 18px);
      line-height:1.7;
      opacity:0.95;
      text-align:center;
    }

    /* Buttons */
    .actions{
      display:flex;
      gap:14px;
      flex-wrap:wrap;
      align-items:center;
      justify-content:center;
      margin-top: 8px;
    }
    button{
      appearance:none;
      border:none;
      border-radius: 999px;
      padding: 12px 22px;
      font-weight:600;
      cursor:pointer;
      transition: transform .2s ease, box-shadow .2s ease, background .2s ease, color .2s ease;
      box-shadow: 0 10px 20px rgba(0,0,0,0.25);
    }
    .btn-primary{
      background: linear-gradient(135deg, var(--rose), #ff6b8a);
      color: white;
    }
    .btn-primary:hover{ transform: translateY(-2px) scale(1.02) }
    .btn-ghost{
      background: rgba(255,255,255,0.08);
      color: #f9dfe6;
      border: 1px solid rgba(255,255,255,0.18);
    }
    .btn-ghost:hover{ background: rgba(255,255,255,0.14) }

    /* Floating Hearts */
    .heart{
      position: fixed;
      bottom: -40px;
      color: var(--rose-soft);
      animation: floatUp linear forwards;
      opacity: 0.85;
      filter: drop-shadow(0 6px 12px rgba(255,77,109,0.35));
      z-index: 0;
      user-select: none;
      pointer-events: none;
    }
    @keyframes floatUp{
      to{ transform: translateY(-120vh) rotate(360deg); opacity: 0 }
    }

    /* Modal */
    .modal{
      position: fixed; inset:0; display:none; align-items:center; justify-content:center;
      background: rgba(0,0,0,0.45); backdrop-filter: blur(6px); z-index: 5;
      padding: 20px;
    }
    .modal.show{ display:flex }
    .modal-card{
      background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,255,255,0.85));
      color:#311b2a;
      border-radius: 20px;
      max-width: 680px; width: min(92vw, 680px);
      padding: 26px;
      box-shadow: 0 30px 60px rgba(0,0,0,0.35);
      text-align:center;
      position:relative;
    }
    .modal-card h2{
      font-family:"Great Vibes", cursive;
      font-size: clamp(28px, 5.2vw, 56px);
      color:#c2185b;
      margin: 8px 0 6px;
    }
    .modal-card p{ margin: 6px 0 18px; font-size: clamp(14px, 2.2vw, 18px) }
    .modal-actions{
      display:flex; gap:12px; justify-content:center; flex-wrap:wrap;
    }

    /* Confetti */
    .confetti{
      position: fixed; inset: 0; pointer-events: none; overflow: hidden; z-index: 9;
    }

    /* Footer */
    footer{
      margin-top: 18px;
      text-align:center;
      font-size: 12px;
      opacity:0.8;
    }

    /* Music pill */
    .music-pill{
      position: fixed; right: 16px; bottom: 16px; z-index: 6;
      background: rgba(255,255,255,0.12);
      border: 1px solid rgba(255,255,255,0.22);
      border-radius: 999px;
      display:flex; align-items:center; gap:12px;
      padding:10px 14px;
      box-shadow: var(--shadow);
      backdrop-filter: blur(8px);
    }
    .dot{
      width:10px; height:10px; border-radius:999px; background:#bbb;
      box-shadow: 0 0 10px currentColor;
      transition: all .3s ease;
    }
    .dot.playing{ background:#54e589; box-shadow: 0 0 16px #54e589 }
    .music-pill button{ padding: 8px 14px }
    .hint{
      font-size:12px; opacity:0.8; margin-top:4px; text-align:center;
    }
    .signature{
      margin-top: 16px;
      font-size: 13px;
      opacity: 0.85;
    }

    /* Responsive tweaks */
    @media (max-width: 420px){
      .message{ text-align: left }
    }
  </style>
</head>
<body>
  <div class="container">
    <main class="card" role="main" aria-live="polite">
      <div class="glow" aria-hidden="true"></div>
      <header>
        <div class="script">Dear Rasmalai,</div>
        <h1 class="script" style="font-size:clamp(30px,7vw,72px); margin-top:-4px;">
          Will you be my Valentine?
        </h1>
        <p class="subtitle">This heart has chosen you—today and always. 💞</p>
      </header>

      <section class="message">
        Every love song reminds me of you, every star spells your name, and every day is brighter because you’re in it.  
        On this Valentine’s Day, I’d love to make new memories—just us, laughter, and a little bit of magic. ✨
      </section>

      <div class="actions">
        <button class="btn-primary" id="askBtn" aria-haspopup="dialog" aria-controls="askModal">Ask the Question 💘</button>
        <button class="btn-ghost" id="releaseHearts">Release Hearts 💗</button>
      </div>

      <p class="hint">Tip: click “Play Music” at the bottom for the full romantic vibe.</p>

      <footer>
        <div class="signature">With love, <strong>Piyush</strong> • <span id="today"></span></div>
      </footer>
    </main>

    <!-- Music Control -->
    <div class="music-pill" aria-label="music controls">
      <span class="dot" id="musicDot" aria-hidden="true"></span>
      <button class="btn-ghost" id="musicToggle" aria-pressed="false">Play Music ▶️</button>
      <audio id="bgm" preload="auto" loop>
        <!-- Replace 'music.mp3' with your file or a royalty‑free URL -->
        <source src="music.mp3" type="audio/mpeg">
        <!-- Example of a royalty-free option:
        <source src="https://cdn.pixabay.com/download/audio/2022/03/24/audio_7a4e1b0fe3.mp3?filename=valentine-ambient.mp3" type="audio/mpeg">
        -->
        Your browser does not support the audio element.
      </audio>
    </div>
  </div>

  <!-- Ask Modal -->
  <div class="modal" id="askModal" role="dialog" aria-modal="true" aria-labelledby="askTitle">
    <div class="modal-card">
      <h2 id="askTitle">Be My Valentine, Rasmalai? 💖</h2>
      <p>
        How about a cozy date—good food, a little music, and a lot of smiles?  
        Say yes and I’m booking it! 😊
      </p>
      <div class="modal-actions">
        <button class="btn-primary" id="yesBtn">Yes! 💞</button>
        <button class="btn-ghost" id="noBtn">Umm... maybe later</button>
      </div>
    </div>
  </div>

  <!-- Confetti Layer -->
  <canvas class="confetti" id="confettiCanvas" width="1280" height="720" aria-hidden="true"></canvas>

  <script>
    // Set today’s date nicely
    const todayEl = document.getElementById('today');
    const now = new Date();
    todayEl.textContent = now.toLocaleDateString(undefined, {year:'numeric', month:'long', day:'numeric'});

    // Floating hearts generator
    const heartChars = ['❤','💕','💗','💖','💘','💝'];
    function spawnHeart(){
      const h = document.createElement('div');
      h.className = 'heart';
      h.textContent = heartChars[Math.floor(Math.random()*heartChars.length)];
      const left = Math.random()*100;
      const size = 18 + Math.random()*28;
      const dur = 6 + Math.random()*6;
      h.style.left = left + 'vw';
      h.style.fontSize = size + 'px';
      h.style.animationDuration = dur + 's';
      document.body.appendChild(h);
      setTimeout(()=> h.remove(), dur*1000);
    }
    function burstHearts(count=24){ for(let i=0;i<count;i++){ setTimeout(spawnHeart, i*100) } }
    document.getElementById('releaseHearts').addEventListener('click', ()=> burstHearts(30));
    // Idle hearts
    setInterval(()=> { if(Math.random()<0.3) spawnHeart(); }, 1200);

    // Modal logic
    const askBtn = document.getElementById('askBtn');
    const askModal = document.getElementById('askModal');
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');

    askBtn.addEventListener('click', ()=>{
      askModal.classList.add('show');
      // small heart burst when opening
      burstHearts(14);
    });
    askModal.addEventListener('click', (e)=>{
      if(e.target === askModal) askModal.classList.remove('show');
    });

    // No button dodges cursor
    noBtn.addEventListener('mousemove', (e)=>{
      const rect = noBtn.getBoundingClientRect();
      const x = (Math.random()*60 - 30); // random nudge
      const y = (Math.random()*60 - 30);
      noBtn.style.transform = `translate(${x}px, ${y}px)`;
    });
    noBtn.addEventListener('mouseleave', ()=> noBtn.style.transform = 'translate(0,0)');

    // Confetti on Yes
    function confetti(){
      const canvas = document.getElementById('confettiCanvas');
      const ctx = canvas.getContext('2d');
      const w = canvas.width = window.innerWidth;
      const h = canvas.height = window.innerHeight;
      const pieces = [];
      for(let i=0;i<220;i++){
        pieces.push({
          x: Math.random()*w,
          y: Math.random()*-h,
          r: 4+Math.random()*7,
          c: `hsl(${Math.random()*360}, 90%, 65%)`,
          s: 1+Math.random()*3,
          a: Math.random()*Math.PI
        });
      }
      let frame = 0;
      function draw(){
        ctx.clearRect(0,0,w,h);
        frame++;
        pieces.forEach(p=>{
          p.y += p.s + Math.cos((frame+p.x)*0.02);
          p.x += Math.sin((frame+p.y)*0.01);
          p.a += 0.08;
          ctx.save();
          ctx.translate(p.x, p.y);
          ctx.rotate(p.a);
          ctx.fillStyle = p.c;
          ctx.fillRect(-p.r/2, -p.r/2, p.r, p.r*0.6);
          ctx.restore();
          if(p.y > h+20) { p.y = -20; p.x = Math.random()*w; }
        });
        requestAnimationFrame(draw);
      }
      draw();
      setTimeout(()=> ctx.clearRect(0,0,w,h), 5000);
    }
    yesBtn.addEventListener('click', ()=>{
      askModal.classList.remove('show');
      burstHearts(40);
      confetti();
      // Sweet acknowledgement
      const t = document.createElement('div');
      t.className = 'card';
      t.style.position='fixed'; t.style.left='50%'; t.style.top='14%';
      t.style.transform='translateX(-50%)';
      t.style.maxWidth='min(92vw, 560px)'; t.style.textAlign='center';
      t.style.zIndex='8';
      t.innerHTML = `
        <div class="script" style="margin-bottom:6px;">Yay! 💞</div>
        <div style="opacity:0.95">You said <b>Yes</b>—can’t wait for our date, my sweetest <b>Rasmalai</b>!<br>
        I’ll make it unforgettable. ✨</div>
      `;
      document.body.appendChild(t);
      setTimeout(()=> t.remove(), 5200);
    });

    // Music control
    const audio = document.getElementById('bgm');
    const musicBtn = document.getElementById('musicToggle');
    const musicDot = document.getElementById('musicDot');

    musicBtn.addEventListener('click', async ()=>{
      try{
        if(audio.paused){
          await audio.play();
          musicBtn.textContent = 'Pause Music ⏸️';
          musicBtn.setAttribute('aria-pressed','true');
          musicDot.classList.add('playing');
        }else{
          audio.pause();
          musicBtn.textContent = 'Play Music ▶️';
          musicBtn.setAttribute('aria-pressed','false');
          musicDot.classList.remove('playing');
        }
      }catch(err){
        alert('Your browser blocked autoplay. Try clicking again or check sound settings.');
      }
    });

    // Improve keyboard accessibility
    document.addEventListener('keydown', (e)=>{
      if(e.key === 'Escape') askModal.classList.remove('show');
    });

    // Ensure canvas resizes
    window.addEventListener('resize', ()=>{
      const c = document.getElementById('confettiCanvas');
      c.width = window.innerWidth; c.height = window.innerHeight;
    });
  </script>
</body>
</html>
