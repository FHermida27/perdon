<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Perdóname (gatitos)</title>
  <style>
    :root{--bg:#fff7fb;--card:#ffffff;--accent:#ff6b97;--muted:#6b6b6b}
    *{box-sizing:border-box}
    body{font-family:system-ui,-apple-system,Segoe UI,Roboto,'Helvetica Neue',Arial;display:flex;align-items:center;justify-content:center;min-height:100vh;margin:0;background:linear-gradient(160deg,#fff7fb 0%, #fffef9 100%);}
    .card{width:min(720px,96%);background:var(--card);padding:28px;border-radius:18px;box-shadow:0 10px 30px rgba(0,0,0,.08);text-align:center;position:relative}
    h1{margin:0 0 8px;font-size:28px}
    p.lead{color:var(--muted);margin:0 0 18px}

    .kitty{font-size:56px;display:block;margin:14px auto}
    .buttons{display:flex;gap:14px;justify-content:center;margin-top:12px}
    button{padding:12px 20px;border-radius:12px;border:0;background:linear-gradient(90deg,var(--accent),#ff9bbd);color:white;font-weight:600;cursor:pointer;box-shadow:0 6px 18px rgba(255,107,151,.22);transition:transform .15s ease, box-shadow .15s ease}
    button.secondary{background:#e6e6ee;color:#333;box-shadow:0 6px 18px rgba(0,0,0,.06)}
    button:active{transform:translateY(2px)}

    .message{margin-top:18px;font-size:18px;min-height:40px}
    .sticker{font-size:64px;display:block;margin:12px auto}
    .hidden{display:none}

    /* happy animation */
    @keyframes floatUp{0%{transform:translateY(0)}50%{transform:translateY(-10px)}100%{transform:translateY(0)}}
    .happy .sticker{animation:floatUp 2s ease-in-out infinite}
    .hearts{position:absolute;left:50%;transform:translateX(-50%);top:-30px;pointer-events:none}
    .heart{font-size:28px;opacity:0;animation:heartPop 1s ease forwards}
    @keyframes heartPop{0%{transform:translateY(20px) scale(.6);opacity:0}50%{opacity:1;transform:translateY(-6px) scale(1.08)}100%{opacity:0;transform:translateY(-60px) scale(.9)}}

    /* sad animation */
    .sad .sticker{transform:translateY(0);animation:shake .8s ease-in-out}
    @keyframes shake{0%{transform:translateX(0)}25%{transform:translateX(-6px)}50%{transform:translateX(6px)}75%{transform:translateX(-4px)}100%{transform:translateX(0)}}

    /* responsive */
    @media (max-width:480px){.kitty{font-size:44px}.sticker{font-size:48px}}

    footer{font-size:12px;color:#999;margin-top:10px}
  </style>
</head>
<body>
  <main class="card" id="card">
    <h1>Mi amor... ¿me perdonas?</h1>
    <p class="lead">Sé que me equivoqué. Traje a los gatitos para pedirte disculpas 🐾</p>

    <div class="kitty" aria-hidden="true">😺😻</div>

    <div class="buttons" id="buttons">
      <button id="yesBtn">Sí 💖</button>
      <button id="noBtn" class="secondary">No 😿</button>
    </div>

    <div class="message" id="message"></div>
    <div class="sticker hidden" id="sticker">😺</div>

    <div class="hearts" id="hearts"></div>

    <footer>Consejo: si estás en celular, toca los botones. Si estás en PC, pasa el cursor sobre "No" después del segundo intento...</footer>
  </main>

  <script>
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');
    const message = document.getElementById('message');
    const sticker = document.getElementById('sticker');
    const hearts = document.getElementById('hearts');
    const card = document.getElementById('card');

    let noCount = 0;
    let evasive = false;

    function showHappy() {
      // clear evasive behavior
      evasive = false;
      noBtn.style.transform = '';
      noBtn.style.position = '';
      noBtn.style.left = '';
      noBtn.style.top = '';

      card.classList.remove('sad');
      card.classList.add('happy');
      sticker.classList.remove('hidden');
      sticker.textContent = '😺';
      message.innerHTML = 'Sabía que me perdonarías, amor 💖✨<br>Te quiero mucho <span aria-hidden>❤️🥰</span>';

      // little hearts animation
      hearts.innerHTML = '';
      for (let i=0;i<8;i++){
        const h = document.createElement('div');
        h.className = 'heart';
        h.style.left = (Math.random()*160-80)+'px';
        h.style.animationDelay = (i*120)+'ms';
        h.textContent = '❤️';
        hearts.appendChild(h);
        // remove after animation
        setTimeout(()=>h.remove(),1400);
      }

      // confetti-like burst using tiny emojis (simple)
      for (let i=0;i<16;i++){
        const e = document.createElement('div');
        e.textContent = ['🎉','✨','💞','🌟'][Math.floor(Math.random()*4)];
        e.style.position='absolute';
        e.style.left = (50 + (Math.random()-0.5)*60) + '%';
        e.style.top = (10 + Math.random()*60) + '%';
        e.style.fontSize = (10+Math.random()*18)+'px';
        e.style.opacity = 0.95;
        card.appendChild(e);
        setTimeout(()=>{ e.style.transition='all 900ms ease'; e.style.transform='translateY(-50px) scale(1.2)'; e.style.opacity=0; }, 50+Math.random()*200);
        setTimeout(()=>e.remove(),1200);
      }
    }

    function showPlease() {
      noCount++;
      card.classList.remove('happy');
      card.classList.add('sad');
      sticker.classList.remove('hidden');
      sticker.textContent = '😿';
      message.innerHTML = 'Porfa... no actualices la página, estoy intentando enmendarlo 🙏<br><em>¿Por favor?</em>';

      if (noCount >= 2) {
        // activate evasive mode
        evasive = true;
        message.innerHTML += '<br><strong>Ups — ya no puedo aceptar ese "No" tan fácil 😅</strong>';
        enableEvasiveNo();
      }
    }

    function randomPositionButton() {
      const parent = buttonsContainerBounds();
      const btnW = noBtn.offsetWidth;
      const btnH = noBtn.offsetHeight;
      // choose random inside card area
      const padding = 16;
      const maxX = parent.width - btnW - padding;
      const maxY = parent.height - btnH - padding;
      const x = Math.max(padding, Math.random()*maxX + parent.left);
      const y = Math.max(parent.top, Math.random()*maxY + parent.top);
      noBtn.style.position = 'absolute';
      noBtn.style.left = Math.min(x, parent.width - btnW) + 'px';
      noBtn.style.top = Math.min((y - parent.top), parent.height - btnH) + 'px';
    }

    function buttonsContainerBounds(){
      // bounding area inside card where button can move
      const rect = card.getBoundingClientRect();
      // create a safe area under the header
      return {left: 20, top: 120, width: rect.width - 40, height: rect.height - 160};
    }

    function enableEvasiveNo(){
      // on hover (desktop) move; on click/touch move as well
      noBtn.addEventListener('mouseover', evasiveHandler);
      noBtn.addEventListener('click', evasiveHandler);
      noBtn.addEventListener('touchstart', evasiveHandler);
      // make sure container allows absolute positioning
      noBtn.style.transition = 'left 220ms ease, top 220ms ease';
    }

    function evasiveHandler(e){
      if (!evasive) return;
      // if user clicked directly (maybe mobile), prevent click!
      e.preventDefault();
      moveNoRandomly();
    }

    function moveNoRandomly(){
      const area = buttonsContainerBounds();
      const btnW = noBtn.offsetWidth;
      const btnH = noBtn.offsetHeight;
      const x = Math.random() * (area.width - btnW);
      const y = Math.random() * (area.height - btnH);
      noBtn.style.position = 'absolute';
      noBtn.style.left = (area.left + x) + 'px';
      noBtn.style.top = (area.top + y - area.top) + 'px';
    }

    // attach to Yes
    yesBtn.addEventListener('click', ()=>{
      showHappy();
    });

    // attach to No
    noBtn.addEventListener('click', (e)=>{
      // if evasive is on, move and block actual 'No' action
      if (evasive){
        e.preventDefault();
        moveNoRandomly();
        return;
      }
      showPlease();
    });

    // extra: make sure layout works if button becomes absolute
    // wrap initial buttons in relative container
    (function prepareLayout(){
      const btns = document.getElementById('buttons');
      btns.style.position = 'relative';
      btns.style.minHeight = '56px';
    })();

    // Accessibility: allow keyboard
    noBtn.addEventListener('keydown', (ev)=>{
      if (ev.key === 'Enter' || ev.key === ' ') {
        ev.preventDefault();
        noBtn.click();
      }
    });

    yesBtn.addEventListener('keydown', (ev)=>{ if (ev.key==='Enter'||ev.key===' ') { ev.preventDefault(); yesBtn.click(); } });

  </script>
</body>
</html>
