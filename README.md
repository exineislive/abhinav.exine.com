# exine.web.io
Exine
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ExineisLive | YouTube Channel</title>
  <meta name="description" content="Welcome to ExineisLive — official YouTube channel website. Watch, subscribe, and join our Discord!">
  <style>
    body {
      font-family: "Poppins", Arial, sans-serif;
      margin: 0;
      background: linear-gradient(135deg, #111, #1e1e1e);
      color: white;
      text-align: center;
    }
    header {
      padding: 3rem 1rem;
      background: #202020;
      box-shadow: 0 2px 10px rgba(0,0,0,0.4);
    }
    h1 {
      font-size: 2.5rem;
      color: #ff4444;
      margin: 0;
    }
    p {
      color: #ccc;
      max-width: 600px;
      margin: 1rem auto;
    }
    .btn {
      background: #ff0000;
      color: white;
      padding: 0.75rem 1.5rem;
      border-radius: 8px;
      text-decoration: none;
      display: inline-block;
      font-weight: 600;
      margin: 0.5rem;
      transition: 0.2s;
    }
    .btn:hover {
      transform: scale(1.05);
    }
    .discord-btn { background: #7289da; }
    .content { padding: 3rem 1rem; }
    iframe { width: 90%; max-width: 560px; height: 315px; border-radius: 12px; box-shadow: 0 0 15px rgba(255,0,0,0.3); }
    footer { margin-top: 3rem; padding: 1.5rem; font-size: 0.9rem; background: #181818; color: #777; }
  </style>
</head>
<body>
  <header>
    <h1>ExineisLive</h1>
    <p>🎮 Gaming, commentary, and live entertainment — welcome to the official ExineisLive website!</p>
    <a class="btn" href="https://www.youtube.com/@ExineisLive" target="_blank">▶ Visit Channel</a>
    <a class="btn discord-btn" href="https://discord.gg/zARyzCgWzj" target="_blank">💬 Join Discord</a>
    <div style="margin-top: 1rem;">
      <!-- Live subscriber count widget -->
      <iframe src="https://www.subscribercounter.com/channel/UCxxxxxx" 
              frameborder="0" 
              scrolling="no" 
              width="200" 
              height="60">
      </iframe>
    </div>
  </header>

  <section class="content">
    <h2>Latest Upload</h2>
    <!-- Replace VIDEO_ID below with your latest YouTube video ID -->
    <iframe src="https://www.youtube.com/embed/VIDEO_ID" 
            title="YouTube video player" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
    </iframe>
  </section>

  <footer>
    © 2025 ExineisLive | Built with ❤️ using GitHub Pages
  </footer>
</body>
</html>
