
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>EXILE323 | PUBG Mobile Clan</title>
  <style>
    /* Genel reset */
    * {margin:0; padding:0; box-sizing:border-box; font-family: 'Poppins', sans-serif;}
    body {
      background: linear-gradient(-45deg, #000, #111, #0f0f0f, #1a1a1a);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      color: white;
      overflow-x: hidden;
    }

    @keyframes gradientBG {
      0% {background-position:0% 50%;}
      50% {background-position:100% 50%;}
      100% {background-position:0% 50%;}
    }

    a {color:cyan; text-decoration:none; transition:0.3s;}
    a:hover {color:#0ff; text-shadow:0 0 10px cyan;}

    /* Loading screen */
    #loading {
      position: fixed; width:100%; height:100%;
      background:#000; display:flex; align-items:center; justify-content:center;
      z-index:9999; flex-direction:column; color:#0ff;
    }
    #loading h1 {
      font-size:3rem;
      text-shadow:0 0 10px #0ff, 0 0 20px #0ff;
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0%,100% {opacity:1;}
      50% {opacity:0.3;}
    }

    /* Navbar */
    nav {
      display:flex; justify-content:space-between; align-items:center;
      padding:15px 30px; background:rgba(0,0,0,0.7); position:sticky; top:0; z-index:1000;
    }
    nav .logo {font-size:1.8rem; font-weight:bold; color:#0ff; text-shadow:0 0 15px #0ff;}
    nav ul {list-style:none; display:flex; gap:20px;}
    nav ul li a {font-size:1rem; font-weight:500;}
    .burger {display:none; flex-direction:column; cursor:pointer;}
    .burger div {width:25px; height:3px; background:white; margin:4px;}

    @media (max-width:768px) {
      nav ul {display:none; flex-direction:column; background:#000; position:absolute; top:60px; right:0; width:200px; padding:20px;}
      nav ul.active {display:flex;}
      .burger {display:flex;}
    }

    /* Sections */
    section {padding:80px 20px; text-align:center;}
    section h2 {font-size:2.5rem; margin-bottom:20px; color:#0ff; text-shadow:0 0 15px cyan;}

    /* Hakkımızda */
    #about p {
      max-width:700px; margin:0 auto; font-size:1.2rem; line-height:1.8;
    }

    /* Liderler */
    .leaders {display:flex; justify-content:center; gap:40px; flex-wrap:wrap;}
    .leader {
      background:rgba(255,255,255,0.05); padding:20px; border-radius:15px;
      box-shadow:0 0 15px rgba(0,255,255,0.2); transition:0.3s;
    }
    .leader:hover {transform:scale(1.05); box-shadow:0 0 25px cyan;}

    /* Başvuru formu */
    form {
      max-width:500px; margin:0 auto; display:flex; flex-direction:column; gap:15px;
    }
    form input, form textarea {
      padding:10px; border:none; border-radius:8px;
    }
    form button {
      padding:12px; border:none; background:#0ff; color:#000;
      font-weight:bold; border-radius:8px; cursor:pointer;
      transition:0.3s;
    }
    form button:hover {background:#00aaff; color:white;}

    /* Footer */
    footer {
      background:#000; text-align:center; padding:30px 10px; margin-top:40px;
    }
    .slogan {
      font-size:1.2rem; font-weight:bold; color:#0ff;
      text-shadow:0 0 10px #0ff, 0 0 20px #00f;
      transition:opacity 0.5s ease;
    }

    /* Sayfa geçiş animasyonu */
    .fade {animation: fadeIn 1s;}
    @keyframes fadeIn {from{opacity:0;} to{opacity:1;}}
  </style>
</head>
<body class="fade">

  <!-- Loading Screen -->
  <div id="loading">
    <h1>EXILE323</h1>
    <p>Loading...</p>
  </div>

  <!-- Navbar -->
  <nav>
    <div class="logo">EXILE323</div>
    <ul>
      <li><a href="#about">Hakkımızda</a></li>
      <li><a href="#leaders">Liderler</a></li>
      <li><a href="#apply">Başvuru</a></li>
      <li><a href="https://www.tiktok.com/@exile323" target="_blank">TikTok</a></li>
    </ul>
    <div class="burger" onclick="toggleMenu()">
      <div></div><div></div><div></div>
    </div>
  </nav>

  <!-- Hakkımızda -->
  <section id="about">
    <h2>Hakkımızda</h2>
    <p>
      EXILE323, 2018’den bu yana PUBG Mobile sahnesinde aktif olan bir klan.  
      Amacımız dostluk, disiplin ve profesyonel oyun anlayışını birleştirerek güçlü bir ekip oluşturmaktır.  
      Her zaman “Für die Famillia” mottosuyla ilerliyoruz.
    </p>
  </section>

  <!-- Liderler -->
  <section id="leaders">
    <h2>Liderler</h2>
    <div class="leaders">
      <div class="leader">
        <h3>EXILE323</h3>
        <p>ID: 516572604</p>
      </div>
    </div>
  </section>

  <!-- Başvuru Formu -->
  <section id="apply">
    <h2>Klana Katıl</h2>
    <form action="https://formspree.io/f/xqalrayd" method="POST">
      <input type="text" name="isim" placeholder="İsmin" required>
      <input type="text" name="oyunismi" placeholder="Oyun İsmi" required>
      <input type="text" name="uid" placeholder="UID" required>
      <input type="number" name="yas" placeholder="Yaş" required>
      <input type="text" name="cihaz" placeholder="Kullandığın Cihaz" required>
      <textarea name="aktiflik" placeholder="Ne kadar aktifsin?" required></textarea>
      <button type="submit">Gönder</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p id="dynamic-slogan" class="slogan">Für die Famillia</p>
  </footer>

  <script>
    // Loading Screen
    window.addEventListener("load", () => {
      document.getElementById("loading").style.display = "none";
    });

    // Burger Menu
    function toggleMenu() {
      document.querySelector("nav ul").classList.toggle("active");
    }

    // Dinamik Slogan
    const slogans = ["Für die Famillia", "SINCE 2018", "EXILE323", "PUBG MOBILE CLAN"];
    let index = 0;
    const sloganElement = document.getElementById("dynamic-slogan");

    setInterval(() => {
      index = (index + 1) % slogans.length;
      sloganElement.textContent = slogans[index];
    }, 3000);
  </script>
</body>
