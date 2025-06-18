<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="ZZONE99 PUBG Mobile Klan Sitesi - Since 2018" />
  <meta name="keywords" content="zzone99, pubg mobile, klan, başvuru" />
  <meta name="author" content="ZZONE99" />
  <title>ZZONE99 - Since 2018</title>
  <style>
    /* RESET + GLOBAL */
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #0f0f0f;
      color: #fff;
      overflow-x: hidden;
    }

    /* LOADING */
    #loading {
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      background: #0f0f0f;
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
    }

    .spinner {
      border: 6px solid #222;
      border-top: 6px solid #0ef;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    /* HEADER */
    header {
      text-align: center;
      padding: 60px 20px 20px;
      animation: fadeIn 2s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    #logo {
      width: 120px;
      margin-bottom: 10px;
    }

    h1 {
      font-size: 42px;
      margin-bottom: 10px;
      color: #0ef;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 20px;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      padding: 10px 20px;
      border: 1px solid #0ef;
      border-radius: 8px;
      transition: 0.3s;
    }

    nav a:hover {
      background: #0ef;
      color: #000;
    }

    section {
      max-width: 800px;
      margin: auto;
      padding: 40px 20px;
      animation: fadeIn 1.5s ease;
    }

    h2 {
      font-size: 28px;
      color: #0ef;
      margin-bottom: 10px;
    }

    p, label {
      font-size: 16px;
      margin-bottom: 10px;
    }

    form input, form select {
      width: 100%;
      padding: 10px;
      margin-bottom: 12px;
      border: none;
      border-radius: 6px;
      background: #1a1a1a;
      color: #fff;
    }

    .button {
      background: #0ef;
      color: #000;
      padding: 12px 24px;
      font-weight: bold;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }

    .button:hover {
      background: #0cf;
    }

    .social {
      display: flex;
      justify-content: center;
      gap: 40px;
      margin-top: 30px;
    }

    .social-icon {
      position: relative;
    }

    .social-icon img {
      width: 40px;
      cursor: pointer;
    }

    .popup {
      display: none;
      position: absolute;
      top: 50px;
      left: -20px;
      background: #111;
      color: white;
      padding: 8px 14px;
      border-radius: 6px;
      font-size: 14px;
      white-space: nowrap;
    }

    .social-icon:hover .popup {
      display: block;
    }

    .counter {
      text-align: center;
      font-size: 14px;
      opacity: 0.6;
      margin-top: 30px;
    }

    footer {
      text-align: center;
      padding: 30px;
      background: #111;
      color: #ccc;
      font-size: 14px;
    }

    /* RESPONSIVE */
    @media (max-width: 600px) {
      nav {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>

<!-- LOADING SCREEN -->
<div id="loading">
  <div class="spinner"></div>
</div>

<header>
  <img src="logo.png" id="logo" alt="ZZONE99 Logo">
  <h1>ZZONE99</h1>
  <p>Since 2018 • Für die GANG → AREA323 → ZZONE99</p>
</header>

<nav>
  <a href="#tanitim">Tanıtım</a>
  <a href="#basvuru">Başvuru</a>
  <a href="#iletisim">İletişim</a>
</nav>

<section id="tanitim">
  <h2>Klan Tanıtımı</h2>
  <p>ZZONE99, disiplinli ve vizyon sahibi oyuncuların toplandığı bir PUBG Mobile klanıdır. 2018’den bu yana sahnedeyiz.</p>
</section>

<section id="basvuru">
  <h2>Başvuru Formu</h2>
  <form action="https://formspree.io/f/xldnljve" method="POST">
    <label>Oyuncu Adı ve UID</label>
    <input type="text" name="Oyuncu Adı ve UID" required />
    <label>Yaş</label>
    <input type="number" name="Yaş" required />
    <label>Aktiflik Durumu</label>
    <select name="Aktiflik" required>
      <option value="">Seçiniz</option>
      <option>Her gün</option>
      <option>Haftalık</option>
      <option>Nadiren</option>
    </select>
    <label>Kullandığınız Cihaz</label>
    <input type="text" name="Cihaz" required />
    <button class="button" type="submit">Başvuru Yap</button>
  </form>
</section>

<section id="iletisim">
  <h2>İletişim / Sosyal Medya</h2>
  <p><strong>Oyun İçi:</strong> mAzz99 (516572604), yAzz99</p>
  <div class="social">
    <div class="social-icon">
      <img src="https://cdn-icons-png.flaticon.com/512/3046/3046123.png" alt="TikTok mAzz99">
      <div class="popup">@mAzz99theboss</div>
    </div>
    <div class="social-icon">
      <img src="https://cdn-icons-png.flaticon.com/512/3046/3046123.png" alt="TikTok yAzz99">
      <div class="popup">@babavizyondapm</div>
    </div>
  </div>
</section>

<div class="counter">
  Bu site <span id="visitor-count">0</span> defa ziyaret edildi.
</div>

<footer>
  Für die Famillia
</footer>

<script>
  // Loading ekranı
  window.addEventListener("load", function () {
    document.getElementById("loading").style.display = "none";
  });

  // Ziyaretçi Sayacı
  let count = localStorage.getItem("zzone_visit_count");
  count = count ? parseInt(count) + 1 : 1;
  localStorage.setItem("zzone_visit_count", count);
  document.getElementById("visitor-count").textContent = count;
</script>

</body>
