<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ExineisLive | Gaming & Commentary</title>
  <style>
    /* --- Base Reset --- */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body, html {
      height: 100%;
      background: radial-gradient(circle at center, #0a0a0a 0%, #000 100%);
      overflow: hidden;
      font-family: 'Poppins', sans-serif;
      color: #fff;
      display: flex; align-items: center; justify-content: center;
      text-align: center;
    }

    /* --- Particles Canvas --- */
    #particles {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: 0;
    }

    /* --- Content Container --- */
    .content {
      position: relative;
      z-index: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      animation: fadeIn 2s ease-out forwards;
    }

    /* --- Logo --- */
    .logo {
      width: 200px;
      border-radius: 20px;
      filter: drop-shadow(0 0 20px #00ffcc);
      transform: scale(0.7) rotate(-10deg);
      opacity: 0;
      animation: logoEnter 2s cubic-bezier(0.68, -0.55, 0.27, 1.55) forwards;
    }

    /* --- Text --- */
    h1 {
      font-size: 3rem;
      margin-top: 20px;
      letter-spacing: 2px;
      text-shadow: 0 0 20px rgba(88,166,255,0.6);
      opacity: 0;
      transform: translateY(40px);
      animation: fadeUp 1.5s ease-out forwards;
      animation-delay: 0.8s;
    }

    p {
      font-size: 1.2rem;
      margin: 20px 0 40px;
      color: #b3c7ff;
      opacity: 0;
      animation: fadeUp 1.5s ease-out forwards;
      animation-delay: 1.2s;
    }

    /* --- Button --- */
    .btn {
      display: inline-block;
      padding: 12px 30px;
      font-size: 1rem;
      color: #fff;
      border: 2px solid #58a6ff;
      text-decoration: none;
      border-radius: 8px;
      background: transparent;
      transition: all 0.3s ease;
      opacity: 0;
      animation: fadeUp 1.5s ease-out forwards;
      animation-delay: 1.8s;
    }

    .btn:hover {
      background: #58a6ff;
      color: #111;
      box-shadow: 0 0 20px #58a6ff;
      transform: scale(1.05);
    }

    /* --- Animations --- */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes logoEnter {
      0% { transform: scale(0.7) rotate(-10deg); opacity: 0; filter: blur(5px); }
      50% { transform: scale(1.1) rotate(10deg); opacity: 1; }
      100% { transform: scale(1) rotate(0deg); filter: blur(0); }
    }
  </style>
</head>
<body>

  <canvas id="particles"></canvas>

  <div class="content">
    <!-- 🔥 Replace with your actual logo image -->
    <img src="assets/logo.jpg" alt="ExineisLive Logo" class="logo">

    <h1>Welcome to ExineisLive</h1>
    <p>Gaming • Commentary • Live Entertainment</p>

    <!-- ✅ Working YouTube button -->
    <a class="btn" href="https://www.youtube.com/@ExineIsLive" target="_blank">
      Visit Our Channel
    </a>
  </div>

  <script>
    /** Particle Background **/
    const canvas = document.getElementById('particles');
    const ctx = canvas.getContext('2d');
    let particlesArray;
    let w, h;

    function initCanvas() {
      w = canvas.width = window.innerWidth;
      h = canvas.height = window.innerHeight;
      particlesArray = [];
      const numParticles = Math.floor((w * h) / 12000);
      for (let i = 0; i < numParticles; i++) {
        particlesArray.push({
          x: Math.random() * w,
          y: Math.random() * h,
          size: Math.random() * 2 + 1,
          speedX: (Math.random() * 0.6) - 0.3,
          speedY: (Math.random() * 0.6) - 0.3
        });
      }
    }

    function animateParticles() {
      ctx.clearRect(0, 0, w, h);
      for (let p of particlesArray) {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.size, 0, Math.PI * 2);
        ctx.fillStyle = '#58a6ff';
        ctx.fill();

        p.x += p.speedX;
        p.y += p.speedY;

        if (p.x < 0) p.x = w;
        if (p.x > w) p.x = 0;
        if (p.y < 0) p.y = h;
        if (p.y > h) p.y = 0;
      }
      requestAnimationFrame(animateParticles);
    }

    window.addEventListener('resize', initCanvas);
    initCanvas();
    animateParticles();
  </script>

</body>
</html>

