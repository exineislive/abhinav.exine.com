<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ExineisLive | Gaming & Commentary</title>
  <style>
    /* Reset and base */
    body, html {
      margin: 0; padding: 0;
      height: 100%; width: 100%;
      overflow: hidden;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #fff;
      background: #111;
      display: flex; align-items: center; justify-content: center;
      text-align: center;
    }
    #particles {
      position: absolute; width: 100%; height: 100%;
      top: 0; left: 0;
      z-index: 0;
    }
    .content {
      position: relative; z-index: 1;
      padding: 0 20px;
    }
    h1 {
      font-size: 3rem;
      margin: 0;
      opacity: 0;
      transform: translateY(40px);
      animation: fadeUp 1.5s ease-out forwards;
    }
    p {
      font-size: 1.2rem;
      margin: 20px 0 40px;
      opacity: 0;
      animation: fadeUp 1.5s ease-out forwards;
      animation-delay: 0.5s;
    }
    .btn {
      display: inline-block;
      padding: 12px 30px;
      font-size: 1rem;
      color: #fff;
      border: 2px solid #58a6ff;
      text-decoration: none;
      background: transparent;
      transition: background 0.3s, color 0.3s;
      opacity: 0;
      animation: fadeUp 1.5s ease-out forwards;
      animation-delay: 1s;
    }
    .btn:hover {
      background: #58a6ff; color: #111;
    }
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <canvas id="particles"></canvas>

  <div class="content">
    <h1>Welcome to ExineisLive</h1>
    <p>Gaming • Commentary • Live Entertainment</p>
    <a class="btn" href="https://www.youtube.com/yourchannel" target="_blank">Visit Our Channel</a>
  </div>

  <script>
    /** Simple particle background script **/
    const canvas = document.getElementById('particles');
    const ctx = canvas.getContext('2d');
    let particlesArray;
    let w, h;

    // resize
    function initCanvas() {
      w = canvas.width = window.innerWidth;
      h = canvas.height = window.innerHeight;
      particlesArray = [];
      const numParticles = Math.floor((w*h) / 15000);
      for (let i = 0; i < numParticles; i++) {
        particlesArray.push({
          x: Math.random()*w,
          y: Math.random()*h,
          size: Math.random()*2 + 1,
          speedX: (Math.random() * 0.6) - 0.3,
          speedY: (Math.random() * 0.6) - 0.3
        });
      }
    }

    function animateParticles() {
      ctx.clearRect(0,0,w,h);
      for (let p of particlesArray) {
        ctx.beginPath();
        ctx.arc(p.x, p.y, p.size, 0, Math.PI*2);
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

    window.addEventListener('resize', () => initCanvas());
    initCanvas();
    animateParticles();
  </script>

</body>
</html>


