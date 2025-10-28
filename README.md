<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Devadathan - Chukkamani</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: "Poppins", sans-serif;
      background: linear-gradient(180deg, #ffe9b0, #ffc46b);
      color: #222;
      text-align: center;
    }
    h1 {
      font-size: 3rem;
      margin-top: 30px;
      color: #d63447;
    }
    h2 {
      font-size: 2rem;
      color: #444;
    }
    .photo {
      margin-top: 30px;
    }
    img {
      width: 350px;
      height: auto;
      border-radius: 15px;
      border: 6px solid #d63447;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }
    .tagline {
      margin-top: 20px;
      font-size: 1.5rem;
      font-weight: bold;
      color: #222;
    }
    footer {
      margin-top: 50px;
      font-size: 0.9rem;
      color: #555;
    }
  </style>
</head>
<body>
  <h1>Devadathan</h1>
  <h2>Maniveeran</h2>
  <div class="photo">
    <!-- Replace this filename with the one you upload -->
    <img src="WhatsApp Image 2025-10-28 at 18.20.21_af1f0ba0.jpg" alt="Devadathan photo">
  </div>
  <div class="tagline">EE website te Nadhan 😎</div>

  <footer>
    <p>Made just for fun — with full consent & good vibes only!</p>
  </footer>
</body>
</html>
<audio id="prankSound">
  <source src="sayip.mp3" type="audio/mpeg">
</audio>

<script>
  function playSound() {
    const sound = document.getElementById("prankSound");
    sound.currentTime = 0; // restart if clicked again
    sound.play();
  }
</script>



