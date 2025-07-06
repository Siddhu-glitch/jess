<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday, Jess✨</title>
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
<style>
  body {
    margin: 0;
    padding: 20px 10px;
    font-family: 'Quicksand', sans-serif;
    background: linear-gradient(135deg, #fdeff9, #ecb3ff);
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #5e3361;
    text-align: center;
    overflow-x: hidden;
  }
  h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 2.5em;
    margin-bottom: 10px;
    animation: glow 2s ease-in-out infinite alternate;
  }
  .verse-card {
    background: rgba(255, 255, 255, 0.85);
    padding: 15px 20px;
    border-radius: 15px;
    border: 2px solid #f8c8ec;
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    margin: 10px 0;
    font-style: italic;
    animation: fadeIn 1s ease forwards;
    max-width: 95%;
    font-size: 1em;
    transition: background 0.6s ease, border-color 0.6s ease;
  }
  .verse-card:hover {
    background: linear-gradient(135deg, #ffe4f3, #e0c3fc);
    border-color: #e0c3fc;
  }
  .fade {
    animation: fadeIn 1s ease forwards;
  }
  .personal-wish {
    margin: 10px 0;
    font-size: 1.1em;
    color: #5e3361;
    animation: fadeIn 2s ease forwards;
    max-width: 95%;
  }
  .message-bottom {
    background: rgba(255, 255, 255, 0.7);
    padding: 12px 15px;
    border-radius: 12px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.15);
    margin: 10px 0;
    max-width: 95%;
    font-size: 1em;
    animation: fadeIn 2s ease forwards;
  }
  button {
    margin: 10px 0;
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
  .sparkles {
    position: absolute;
    width: 100%;
    height: 100%;
    pointer-events: none;
    top: 0;
    left: 0;
  }
  .sparkle {
    position: absolute;
    width: 6px;
    height: 6px;
    border-radius: 50%;
    opacity: 0.8;
    animation: sparkleAnim 6s linear infinite;
  }
  .sparkle.pink { background: #fbcfe8; }
  .sparkle.lavender { background: #e9d5ff; }
  .sparkle.yellow { background: #fef9c3; }
  @keyframes glow {
    from { text-shadow: 0 0 8px #fff, 0 0 16px #d58cff, 0 0 24px #d58cff; }
    to   { text-shadow: 0 0 16px #fff, 0 0 24px #e6b3ff, 0 0 32px #e6b3ff; }
  }
  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(15px);}
    to   { opacity: 1; transform: translateY(0);}
  }
  @keyframes sparkleAnim {
    0%   { transform: translateY(0) scale(0.5); opacity: 1; }
    100% { transform: translateY(-100vh) scale(1); opacity: 0; }
  }
  @media (max-width: 480px) {
    h1 { font-size: 2em; }
    .verse-card, .message-bottom, .personal-wish { font-size: 0.95em; }
    button { font-size: 0.95em; padding: 8px 16px; }
  }
</style>
</head>
<body>
<div class="sparkles">
  <div class="sparkle pink" style="left: 10%; animation-delay: 0s;"></div>
  <div class="sparkle lavender" style="left: 25%; animation-delay: 1s;"></div>
  <div class="sparkle yellow" style="left: 40%; animation-delay: 2s;"></div>
  <div class="sparkle pink" style="left: 55%; animation-delay: 3s;"></div>
  <div class="sparkle lavender" style="left: 70%; animation-delay: 4s;"></div>
  <div class="sparkle yellow" style="left: 85%; animation-delay: 5s;"></div>
</div>
<h1>Happy Birthday, Jess✨</h1>
<div class="verse-card" id="verseCard">
  “May His light always guide your path and fill your heart with peace.” 🕊️
</div>
<button onclick="shuffleVerse()">✨ tap here !</button>
<div class="personal-wish">
  ✨ May your birthday bring laughter, blessings, and moments to cherish forever!
</div>
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
  "“For God so loved the world, that He gave His only begotten Son…” ✝️ (John 3:16)",
  "✨ Jess✨, may your heart always stay as kind & warm as today!",
  "🌸 Wishing Jess✨ endless smiles & sunshine on her path.",
  "💖 Jess✨, you’re a blessing to everyone around you!",
  "🌿 May your dreams grow and bloom just like spring flowers, Jess✨!"
  ];
  function shuffleVerse() {
    const card = document.getElementById('verseCard');
    card.classList.remove('fade'); // reset animation
    void card.offsetWidth; // force reflow
    const randomIndex = Math.floor(Math.random() * verses.length);
    card.innerText = verses[randomIndex];
    card.classList.add('fade'); // apply fade
  }
  window.onload = shuffleVerse;
</script>
</body>
</html>
