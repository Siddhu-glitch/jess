<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday, Jess✨</title>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0 15px;
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(135deg, #fdeff9, #ecb3ff);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      color: #5e3361;
      text-align: center;
      overflow: hidden;
    }
    h1 {
      font-family: 'Great Vibes', cursive;
      font-size: 3em;
      margin-bottom: 10px;
      animation: glow 2s ease-in-out infinite alternate;
    }
    .verse-card {
      background: rgba(255, 255, 255, 0.8);
      padding: 20px 30px;
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.2);
      margin: 20px 0;
      font-style: italic;
      animation: fadeIn 2s ease forwards;
      max-width: 90%;
    }
    .blessing {
      font-family: 'Great Vibes', cursive;
      font-size: 2em;
      white-space: nowrap;
      border-right: 2px solid rgba(0,0,0,0.75);
      overflow: hidden;
      width: 0;
      animation: typing 4s steps(40, end) forwards, blink 0.75s step-end infinite;
      margin-top: 10px;
    }
    button {
      margin-top: 15px;
      background: #e8c7f3;
      border: none;
      padding: 10px 20px;
      border-radius: 8px;
      font-size: 1em;
      cursor: pointer;
      color: #5e3361;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
      transition: transform 0.2s;
    }
    button:hover {
      transform: scale(1.05);
    }
    .message-bottom {
      margin-top: auto;
      margin-bottom: 20px;
      background: rgba(255, 255, 255, 0.7);
      padding: 15px 20px;
      border-radius: 12px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.15);
      max-width: 90%;
      font-size: 1.1em;
      animation: fadeIn 3s ease forwards;
    }
    @keyframes glow {
      from { text-shadow: 0 0 10px #fff, 0 0 20px #d58cff, 0 0 30px #d58cff; }
      to   { text-shadow: 0 0 20px #fff, 0 0 30px #e6b3ff, 0 0 40px #e6b3ff; }
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px);}
      to   { opacity: 1; transform: translateY(0);}
    }
    @keyframes typing {
      from { width: 0; }
      to   { width: 100%; }
    }
    @keyframes blink {
      0%, 100% { border-color: transparent; }
      50%      { border-color: rgba(0,0,0,0.75); }
    }
    .sparkles {
      position: absolute;
      width: 100%;
      height: 100%;
      pointer-events: none;
    }
    .sparkle {
      position: absolute;
      width: 8px;
      height: 8px;
      background: white;
      border-radius: 50%;
      opacity: 0.8;
      animation: sparkleAnim 6s linear infinite;
    }
    @keyframes sparkleAnim {
      0%   { transform: translateY(0) scale(0.5); opacity: 1; }
      100% { transform: translateY(-100vh) scale(1); opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="sparkles">
    <div class="sparkle" style="left: 10%; animation-delay: 0s;"></div>
    <div class="sparkle" style="left: 30%; animation-delay: 1s;"></div>
    <div class="sparkle" style="left: 50%; animation-delay: 2s;"></div>
    <div class="sparkle" style="left: 70%; animation-delay: 3s;"></div>
    <div class="sparkle" style="left: 90%; animation-delay: 4s;"></div>
  </div>
  <h1>Happy Birthday, Jess✨</h1>
  <div class="verse-card" id="verseCard">
    “May His light always guide your path and fill your heart with peace.” 🕊️
  </div>
  <div class="blessing">God bless you abundantly, Jess✨</div>
  <button onclick="shuffleVerse()">Show another blessing ✨</button>
  <div class="message-bottom">
    🌸 “Jess✨, we haven’t met — but if Anjali calls you her best friend, you must be pure gold. Stay awesome & happy birthday!”
  </div>
  <script>
    const verses = [
      "“May His light always guide your path and fill your heart with peace.” 🕊️",
      "“The Lord bless you and keep you; the Lord make His face shine upon you.” ✨ (Numbers 6:24-25)",
      "“You are fearfully and wonderfully made.” 🌸 (Psalm 139:14)",
      "“The joy of the Lord is your strength.” 💖 (Nehemiah 8:10)",
      "“God’s plans for you are plans to prosper and give you hope.” 🌿 (Jeremiah 29:11)",
      "“May He give you the desire of your heart and make all your plans succeed.” ✨ (Psalm 20:4)",
      "“This is the day the Lord has made; let us rejoice and be glad in it.” ☀️ (Psalm 118:24)",
      "“For God so loved the world, that He gave His only begotten Son…” ✝️ (John 3:16)"
    ];
    function shuffleVerse() {
      const randomIndex = Math.floor(Math.random() * verses.length);
      document.getElementById('verseCard').innerText = verses[randomIndex];
    }
    window.onload = shuffleVerse;
  </script>
</body>
</html>
