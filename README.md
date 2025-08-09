## Hi there 👋

<!--
**UrbexRyan/UrbexRyan** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>UrbexRyan | Lost & Forgotten</title>
  <meta name="description" content="I'm UrbexRyan, I explore the lost and forgotten about abandoned places, documenting their existence before they're lost to time." />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Inter:wght@300;400;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0b0f10;
      --card:#101619cc;
      --text:#dfe6e9;
      --muted:#9aa4a7;
      --accent:#6ee7b7; /* vine glow */
      --danger:#cbd5e1; /* glass edges */
      --yt:#ff0033;
      --fb:#1877f2;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      color:var(--text);
      background: radial-gradient(1200px 800px at 60% -10%, #2c3e5015, transparent),
                  linear-gradient(180deg, #0b0f10 0%, #060809 100%);
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, Noto Sans, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
      overflow-x:hidden;
    }

    /* Subtle film grain */
    .noise{position:fixed;inset:0;pointer-events:none;opacity:.07;mix-blend-mode:soft-light;filter:contrast(140%)}
    .noise:before{content:"";position:absolute;inset:-10%;background-image:url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAQAAAAEACAYAAABccqhmAAAAGXRFWHRTb2Z0d2FyZQBQbmczIE5vaXNlIEdlbmVyYXRvciB2MS4wAAABv0lEQVR4nO3RAQ0AAAgDINc/9G2YgQ0t8Q0AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA4DqQbQAB2X9b0QAAAABJRU5ErkJggg==');background-size:256px 256px;animation:grain 1.5s steps(4) infinite}
    @keyframes grain{0%{transform:translate(0,0)}25%{transform:translate(-3%,2%)}50%{transform:translate(2%,-2%)}75%{transform:translate(-2%,1%)}100%{transform:translate(0,0)}}

    /* Overgrown vines (SVG) */
    .vines{position:fixed;inset:0;pointer-events:none;opacity:.25;filter:drop-shadow(0 0 8px #1f3e2e)}
    .vines svg{position:absolute}
    .vines .left{left:-60px;top:-40px;width:40vw;max-width:540px}
    .vines .right{right:-60px;bottom:-80px;width:50vw;max-width:700px;transform:scaleX(-1) rotate(-6deg)}

    /* Broken glass overlay */
    .cracks{position:fixed;inset:0;pointer-events:none;opacity:.18}
    .cracks svg{width:100%;height:100%}

    /* Content */
    .wrap{min-height:100%;display:grid;place-items:center;padding:4rem 1rem}

    .card{
      width:min(900px, 92vw);
      background:linear-gradient(180deg, #0c1215cc, #0b0f10dd);
      border:1px solid #22323a;
      border-radius:22px;
      box-shadow:0 20px 60px #0008, inset 0 1px 0 #ffffff0d;
      backdrop-filter: blur(6px) saturate(120%);
      -webkit-backdrop-filter: blur(6px) saturate(120%);
      overflow:hidden;
    }

    header{display:flex;gap:1rem;align-items:center;padding:1rem 1.25rem;border-bottom:1px solid #1c2a30;background:linear-gradient(0deg,#0d1417,transparent)}
    .avatar{width:58px;height:58px;border-radius:50%;background:#22323a;display:grid;place-items:center;flex:0 0 auto;border:2px solid #2b3d45;box-shadow:inset 0 0 0 1px #000}
    .avatar span{font-family:"Playfair Display", serif;font-weight:700;font-size:26px;letter-spacing:.5px}
    .title{line-height:1}
    .title h1{font-family:"Playfair Display", serif;font-weight:700;margin:.1rem 0;font-size:clamp(22px, 3.4vw, 34px)}
    .title p{margin:.1rem 0;color:var(--muted);font-size:14px}

    main{display:grid;gap:1.25rem;padding:1.25rem}
    .hero{position:relative;border-radius:18px;overflow:hidden;border:1px solid #1f2d33;background:radial-gradient(900px 400px at 50% -10%, #29413a22, transparent), linear-gradient(180deg,#0c1416,#0a0e10)}
    .hero:before{content:"";position:absolute;inset:0;background:
      repeating-linear-gradient(145deg, #0000 0 8px, #0002 8px 9px),
      radial-gradient(1200px 600px at 120% 0%, #6ee7b710, #0000 70%),
      radial-gradient(1200px 600px at -20% 100%, #6ee7b710, #0000 70%);
      mix-blend-mode:overlay;opacity:.6}
    .hero img{display:block;width:100%;height:280px;object-fit:cover;filter:grayscale(.9) contrast(110%) brightness(80%) saturate(70%) blur(.2px)}
    .bio{padding:1rem 1.1rem 1.2rem;font-size:clamp(15px, 1.9vw, 18px);line-height:1.65;color:#d7e0e1}
    .bio strong{color:#e7f7ef}

    .actions{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:.8rem;padding:0 1.1rem 1.2rem}
    .btn{
      display:flex;align-items:center;gap:.6rem;justify-content:center;
      padding:0.9rem 1rem;border-radius:14px;border:1px solid #26363d;background:#0d1417;
      color:var(--text);text-decoration:none;font-weight:600;letter-spacing:.2px;
      box-shadow:0 8px 24px #0006, inset 0 1px 0 #ffffff10;
      transition:transform .08s ease, box-shadow .2s ease, border-color .2s ease;
    }
    .btn:hover{transform:translateY(-2px);border-color:#2f4a54;box-shadow:0 14px 30px #0008, inset 0 1px 0 #ffffff15}
    .btn svg{width:20px;height:20px}
    .yt{--brand:var(--yt)}
    .fb{--brand:var(--fb)}
    .btn .dot{width:9px;height:9px;border-radius:50%;background:var(--brand);box-shadow:0 0 12px var(--brand)}

    .contact{display:grid;gap:.6rem;padding:0 1.1rem 1.4rem;border-top:1px dashed #1f2d33}
    .contact h3{font-family:"Playfair Display", serif;font-weight:700;letter-spacing:.3px;margin:1rem 0 .2rem;font-size:20px}
    .contact .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:.6rem}
    .contact a, .contact span{display:flex;align-items:center;gap:.6rem;padding:.7rem .9rem;border:1px solid #203038;border-radius:12px;background:#0c1316;text-decoration:none;color:#dfe6e9;white-space:nowrap}
    .contact a:hover{border-color:#2f4a54}
    .contact small{color:#8b969a}

    footer{padding:1rem 1.25rem;border-top:1px solid #1c2a30;color:#8b969a;font-size:12px;display:flex;justify-content:space-between;align-items:center}
    .homebase{display:flex;align-items:center;gap:.5rem}

    /* Mobile polish */
    @media (max-width:480px){
      .hero img{height:220px}
    }
  </style>
</head>
<body>
  <!-- atmospheric layers -->
  <div class="noise" aria-hidden="true"></div>
  <div class="vines" aria-hidden="true">
    <!-- Left vine -->
    <svg class="left" viewBox="0 0 400 800" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M40 0 C60 120, 30 240, 90 360 S150 600, 110 760" stroke="#4ade80" stroke-width="2.5" stroke-opacity=".6"/>
      <g fill="#22c55e">
        <path d="M70 110 c18 -28 40 -30 50 0 c-18 28 -40 30 -50 0z" opacity=".8"/>
        <path d="M110 260 c20 -30 44 -32 56 0 c-20 30 -44 32 -56 0z" opacity=".7"/>
        <path d="M90 410 c18 -28 40 -30 50 0 c-18 28 -40 30 -50 0z" opacity=".75"/>
        <path d="M130 560 c18 -28 40 -30 50 0 c-18 28 -40 30 -50 0z" opacity=".85"/>
      </g>
    </svg>
    <!-- Right vine (mirrored) -->
    <svg class="right" viewBox="0 0 500 900" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M60 0 C120 140, 80 280, 160 420 S260 700, 220 880" stroke="#4ade80" stroke-width="2.5" stroke-opacity=".55"/>
      <g fill="#16a34a">
        <path d="M120 150 c20 -30 44 -32 56 0 c-20 30 -44 32 -56 0z" opacity=".85"/>
        <path d="M160 320 c20 -30 44 -32 56 0 c-20 30 -44 32 -56 0z" opacity=".75"/>
        <path d="M200 500 c22 -32 48 -34 60 0 c-22 32 -48 34 -60 0z" opacity=".8"/>
      </g>
    </svg>
  </div>
  <div class="cracks" aria-hidden="true">
    <svg viewBox="0 0 1200 800" xmlns="http://www.w3.org/2000/svg">
      <g stroke="var(--danger)" stroke-opacity=".4" stroke-width="1.2">
        <path d="M200 60 L230 130 L180 210 L260 260"/>
        <path d="M900 40 L860 120 L920 180 L870 240 L940 310"/>
        <path d="M520 140 L560 220 L500 260 L560 340 L520 420"/>
        <path d="M300 520 L360 560 L320 600 L380 640"/>
        <path d="M1000 520 L940 600 L980 660 L920 720"/>
      </g>
    </svg>
  </div>

  <div class="wrap">
    <div class="card" role="region" aria-label="UrbexRyan landing card">
      <header>
        <div class="avatar" aria-hidden="true"><span>UR</span></div>
        <div class="title">
          <h1>UrbexRyan</h1>
          <p>Exploring the lost & forgotten • Central Texas</p>
        </div>
      </header>

      <main>
        <figure class="hero" aria-label="abandoned building mood image">
          <!-- Optional: swap src with your own background photo URL later -->
          <img alt="Eerie abandoned interior with overgrown vines" src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?q=80&w=1600&auto=format&fit=crop" />
        </figure>

        <section class="bio">
          <p><strong>Bio:</strong> I'm UrbexRyan, I explore the lost and forgotten about abandoned places, documenting their existence before they're lost to time.</p>
        </section>

        <nav class="actions" aria-label="Primary social links">
          <a class="btn yt" href="https://www.youtube.com/@urbexryan9613" target="_blank" rel="noopener noreferrer" aria-label="Go to YouTube channel">
            <span class="dot" aria-hidden="true"></span>
            Visit YouTube
            <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M10 8l6 4-6 4V8z" fill="currentColor"/></svg>
          </a>
          <a class="btn fb" href="https://www.facebook.com/profile.php?id=61578564995252" target="_blank" rel="noopener noreferrer" aria-label="Go to Facebook page">
            <span class="dot" aria-hidden="true"></span>
            Visit Facebook
            <svg viewBox="0 0 24 24" fill="none" aria-hidden="true"><path d="M13 10h3V7h-3V6a2 2 0 012-2h1V1h-2a4 4 0 00-4 4v2H8v3h3v9h2v-9z" fill="currentColor"/></svg>
          </a>
        </nav>

        <section class="contact" aria-label="Contact details">
          <h3>Contact</h3>
          <div class="grid">
            <a href="tel:+19152241038" aria-label="Call phone number">📞 <strong>(915) 224-1038</strong></a>
            <a href="mailto:urbex.ryan.yt@gmail.com" aria-label="Send email">✉️ <strong>urbex.ryan.yt@gmail.com</strong></a>
            <span>📍 <strong>Home Base:</strong> <small>Central Texas</small></span>
          </div>
        </section>
      </main>

      <footer>
        <div class="homebase">☠️ Eerie vibes • Overgrowth • Broken glass</div>
        <div>© <span id="y"></span> UrbexRyan</div>
      </footer>
    </div>
  </div>

  <script>
    // Current year
    document.getElementById('y').textContent = new Date().getFullYear();
  </script>
</body>
</html>
