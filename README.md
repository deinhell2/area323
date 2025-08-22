
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AREA323</title>
  <style>
    /* GENEL STİL */
    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      color: #fff;
      overflow-x: hidden;
      background: black;
    }
    header {
      text-align: center;
      padding: 30px 0;
      position: relative;
    }
    header img.logo {
      width: 120px;
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0%, 100% { transform: scale(1);}
      50% { transform: scale(1.1);}
    }
    h1 {
      font-size: 2.5rem;
      text-shadow: 0 0 15px cyan;
    }

    /* Dinamik Slogan */
    .slogan {
      font-size: 1.2rem;
      margin-top: 10px;
      height: 30px;
    }

    /* Glitch Button */
    .glitch-btn {
      display: inline-block;
      padding: 15px 40px;
      margin-top: 20px;
      background: transparent;
      color: cyan;
      border: 2px solid cyan;
      font-size: 1.2rem;
      text-transform: uppercase;
      position: relative;
      overflow: hidden;
      cursor: pointer;
    }
    .glitch-btn::before, .glitch-btn::after {
      content: attr(data-text);
      position: absolute;
      left: 0;
      width: 100%;
      height: 100%;
      background: black;
      overflow: hidden;
      clip: rect(0, 0, 0, 0);
    }
    .glitch-btn::before {
      left: 2px;
      text-shadow: -2px 0 red;
      animation: glitch 2s infinite linear alternate-reverse;
    }
    .glitch-btn::after {
      left: -2px;
      text-shadow: -2px 0 blue;
      animation: glitch 3s infinite linear alternate-reverse;
    }
    @keyframes glitch {
      0% { clip: rect(0, 900px, 0, 0); }
      20% { clip: rect(0, 900px, 100px, 0); }
      40% { clip: rect(0, 900px, 50px, 0); }
      60% { clip: rect(0, 900px, 150px, 0); }
      80% { clip: rect(0, 900px, 80px, 0); }
      100% { clip: rect(0, 900px, 120px, 0); }
    }

    /* Liderler Pop-up */
    .popup {
      position: fixed;
      top: 20px;
      right: 20px;
      background: rgba(0,0,0,0.8);
      border: 2px solid cyan;
      padding: 15px;
      border-radius: 10px;
      display: none;
      z-index: 1000;
    }
    .popup.active {
      display: block;
    }
    .popup h3 {
      margin: 0;
      font-size: 1rem;
      color: cyan;
    }

    /* Başvuru Formu */
    form {
      max-width: 400px;
      margin: 40px auto;
      display: flex;
      flex-direction: column;
      gap: 10px;
      background: rgba(0,0,0,0.7);
      padding: 20px;
      border-radius: 10px;
      border: 2px solid cyan;
    }
    form input, form select, form button {
      padding: 10px;
      border: none;
      outline: none;
      border-radius: 5px;
    }
    form input, form select {
      background: #111;
      color: #fff;
    }
    form button {
      background: cyan;
      color: black;
      font-weight: bold;
      cursor: pointer;
    }
    .success-msg {
      text-align: center;
      font-size: 1.2rem;
      color: lime;
      display: none;
      animation: fadeIn 2s forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0;}
      to { opacity: 1;}
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
      background: rgba(0,0,0,0.8);
      margin-top: 40px;
    }

    /* Burger Menü */
    .burger {
      display: none;
      position: absolute;
      top: 20px;
      left: 20px;
      cursor: pointer;
      z-index: 2000;
    }
    .burger div {
      width: 30px;
      height: 3px;
      background: cyan;
      margin: 5px;
    }
    .menu {
      display: none;
      position: fixed;
      top: 0; left: 0;
      height: 100%; width: 200px;
      background: #111;
      padding-top: 60px;
      z-index: 1500;
    }
    .menu a {
      display: block;
      color: white;
      padding: 10px;
      text-decoration: none;
      border-bottom: 1px solid cyan;
    }

    @media(max-width:768px) {
      .burger { display: block;}
    }

    /* Neon Grid Background */
    .grid {
      position: fixed;
      top:0; left:0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle, rgba(0,255,255,0.05) 1px, transparent 1px);
      background-size: 40px 40px;
      z-index: -1;
      animation: move 20s linear infinite;
    }
    @keyframes move {
      from { background-position: 0 0; }
      to { background-position: 100px 100px; }
    }
  </style>
</head>
<body>
  <div class="grid"></div>

  <!-- Burger Menü -->
  <div class="burger" onclick="toggleMenu()">
    <div></div><div></div><div></div>
  </div>
  <div class="menu" id="menu">
    <a href="#">Ana Sayfa</a>
    <a href="#form">Başvuru</a>
    <a href="#" onclick="togglePopup()">Liderler</a>
  </div>

  <header>
    <img src="logo.png" alt="logo" class="logo">
    <h1>AREA323</h1>
    <div class="slogan" id="slogan"></div>
    <button class="glitch-btn" data-text="Katıl">Klana Katıl</button>
  </header>

  <!-- Başvuru Formu -->
  <form id="form" action="https://formspree.io/f/xldnljve" method="POST" onsubmit="showSuccess(event)">
    <input type="text" name="Ad" placeholder="Ad" required>
    <input type="text" name="Nick" placeholder="Nick" required>
    <input type="number" name="FPS" placeholder="FPS" required>
    <input type="number" name="Yaş" placeholder="Yaş" required>
    <select name="Cihaz" required>
      <option value="">Cihaz Seç</option>
      <option value="Telefon">Telefon</option>
      <option value="Tablet">Tablet</option>
      <option value="Emülatör">Emülatör</option>
    </select>
    <input type="text" name="Aktiflik" placeholder="Aktiflik (gün/saat)" required>
    <input type="text" name="Tecrübe" placeholder="Tecrübe" required>
    <button type="submit">Gönder</button>
  </form>
  <div class="success-msg" id="success-msg">✅ Başvurun alındı! Kontrol edildikten sonra bilgilendirileceksin.</div>

  <!-- Liderler Pop-up -->
  <div class="popup" id="popup">
    <h3>Liderler</h3>
    <p>EXILE323 - TikTok: exile323</p>
    <p>BABAVIZYONDA - TikTok: babavizyondapm</p>
  </div>

  <footer>
    Für die Familia – Since 2018
  </footer>

  <script>
    // Dinamik Slogan
    const slogans = [
      "SINCE 2018",
      "Für die Familia",
      "AREA323 ELİT TAKIM",
      "PUBG MOBILE BEST"
    ];
    let idx = 0;
    const sloganEl = document.getElementById("slogan");
    setInterval(()=>{
      sloganEl.textContent = slogans[idx];
      idx = (idx + 1) % slogans.length;
    }, 3000);

    // Burger Menü
    function toggleMenu() {
      document.getElementById("menu").style.display =
        document.getElementById("menu").style.display === "block" ? "none" : "block";
    }

    // Popup Liderler
    function togglePopup() {
      document.getElementById("popup").classList.toggle("active");
    }

    // Form Başarı Mesajı
    function showSuccess(e){
      e.preventDefault();
      document.getElementById("form").style.display="none";
      document.getElementById("success-msg").style.display="block";
    }
  </script>
</body>
