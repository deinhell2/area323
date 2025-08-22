
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EXILE323</title>
  <style>
    /* GENEL AYARLAR */
    * {margin:0; padding:0; box-sizing:border-box; font-family: 'Orbitron', sans-serif;}
    body {background:#0a0a0f; color:#fff; overflow-x:hidden;}
    a {color:#0ff; text-decoration:none; transition:0.3s;}
    a:hover {color:#fff; text-shadow:0 0 10px #0ff;}

    /* LOADING SCREEN */
    #loading {
      position:fixed; width:100%; height:100%;
      background:#000; display:flex; align-items:center; justify-content:center;
      z-index:9999; flex-direction:column;
    }
    #loading img {width:120px; animation:pulse 2s infinite;}
    @keyframes pulse {0%{transform:scale(1);} 50%{transform:scale(1.2);} 100%{transform:scale(1);}}

    /* HEADER */
    header {position:fixed; top:0; width:100%; display:flex; justify-content:space-between; 
      align-items:center; padding:20px; background:rgba(0,0,0,0.6); backdrop-filter:blur(10px); z-index:100;}
    header h1 {font-size:22px; color:#0ff; text-shadow:0 0 10px #0ff;}
    nav {display:flex; gap:20px;}
    nav a {font-weight:bold;}
    
    /* BURGER MENU */
    .burger {display:none; cursor:pointer; flex-direction:column; gap:5px;}
    .burger div {width:25px; height:3px; background:#0ff;}

    @media(max-width:768px){
      nav {display:none; flex-direction:column; position:absolute; top:70px; right:20px; background:#111; padding:15px; border-radius:10px;}
      nav.active {display:flex;}
      .burger {display:flex;}
    }

    /* HERO */
    .hero {
      height:100vh; display:flex; flex-direction:column; justify-content:center; align-items:center;
      background:radial-gradient(circle at center, #0ff2, #000 70%);
      text-align:center;
    }
    .hero h2 {font-size:40px; margin-bottom:15px; text-shadow:0 0 20px #0ff;}
    .hero p {font-size:18px; max-width:600px; margin:auto; color:#ccc;}

    /* HAKKIMIZDA */
    section {padding:80px 20px; text-align:center;}
    section h2 {font-size:30px; margin-bottom:20px; text-shadow:0 0 15px #0ff;}
    section p {max-width:700px; margin:auto; color:#bbb; line-height:1.6;}

    /* LİDERLER */
    .leaders {display:flex; justify-content:center; flex-wrap:wrap; gap:30px;}
    .leader-card {
      background:#111; padding:20px; border-radius:15px; width:250px;
      transition:0.3s; box-shadow:0 0 15px #0ff5;
    }
    .leader-card:hover {transform:scale(1.05); box-shadow:0 0 25px #0ff;}
    .leader-card img {width:100%; border-radius:10px; margin-bottom:10px;}
    .leader-card h3 {color:#0ff;}
    .leader-card p {color:#ccc;}

    /* BAŞVURU FORMU */
    form {max-width:500px; margin:auto; display:flex; flex-direction:column; gap:15px;}
    input, textarea {padding:12px; border:none; border-radius:8px; outline:none;}
    button {
      background:#0ff; color:#000; border:none; padding:12px; border-radius:8px;
      cursor:pointer; font-weight:bold; transition:0.3s;
    }
    button:hover {background:#000; color:#0ff; box-shadow:0 0 15px #0ff;}

    /* FOOTER */
    footer {
      text-align:center; padding:30px; background:#000; border-top:1px solid #0ff3;
      margin-top:50px; font-size:14px; color:#aaa;
    }
  </style>
</head>
<body>
  <!-- LOADING -->
  <div id="loading">
    <img src="logo.png" alt="logo">
    <p style="color:#0ff; margin-top:10px;">Yükleniyor...</p>
  </div>

  <!-- HEADER -->
  <header>
    <h1>EXILE323</h1>
    <div class="burger" onclick="document.querySelector('nav').classList.toggle('active')">
      <div></div><div></div><div></div>
    </div>
    <nav>
      <a href="#hakkimizda">Hakkımızda</a>
      <a href="#liderler">Liderler</a>
      <a href="#basvuru">Başvuru</a>
      <a href="#iletisim">İletişim</a>
    </nav>
  </header>

  <!-- HERO -->
  <div class="hero">
    <h2>Für die Famillia</h2>
    <p>SINCE 2018 - PUBG MOBILE klanımızı temsil eden resmi sayfa</p>
  </div>

  <!-- HAKKIMIZDA -->
  <section id="hakkimizda">
    <h2>Hakkımızda</h2>
    <p>EXILE323 klanı, 2018’den beri PUBG Mobile sahnesinde aktif olan, disiplin, dostluk ve başarı üzerine kurulmuş bir topluluktur. 
    Her üye bir ailenin parçasıdır ve hedefimiz her zaman birlikte yükselmektir.</p>
  </section>

  <!-- LİDERLER -->
  <section id="liderler">
    <h2>Liderler</h2>
    <div class="leaders">
      <div class="leader-card">
        <img src="exile.png" alt="EXILE323">
        <h3>EXILE323</h3>
        <p>ID: 516572604</p>
      </div>
    </div>
  </section>

  <!-- BAŞVURU -->
  <section id="basvuru">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xqalrayd" method="POST">
      <input type="text" name="isim" placeholder="Oyun İsmi" required>
      <input type="text" name="uid" placeholder="UID" required>
      <input type="number" name="yas" placeholder="Yaş" required>
      <input type="text" name="cihaz" placeholder="Cihaz" required>
      <textarea name="aktiflik" placeholder="Aktiflik durumun" rows="3"></textarea>
      <button type="submit">Başvur</button>
    </form>
  </section>

  <!-- İLETİŞİM -->
  <section id="iletisim">
    <h2>İletişim</h2>
    <p>TikTok: <a href="https://www.tiktok.com/@exile323" target="_blank">@exile323</a></p>
  </section>

  <!-- FOOTER -->
  <footer>
    Für die Famillia | SINCE 2018
  </footer>

  <script>
    // LOADING SCREEN KAPANMASI
    window.addEventListener("load", () => {
      setTimeout(() => {
        document.getElementById("loading").style.display = "none";
      }, 2000); // 2 saniye
    });
  </script>
</body>
</html>
