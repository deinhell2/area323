<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ZZONE99 | PUBG Mobile Klanı</title>
  <link rel="icon" href="logo.png" />
  <style>
    /* Reset ve Tema */
    * { margin: 0; padding: 0; box-sizing: border-box; scroll-behavior: smooth; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(-45deg, #0d0d0d, #11161b, #0a0f1d);
      color: #f2f2f2;
      overflow-x: hidden;
    }
    h1, h2, h3 { text-align: center; color: #00d4ff; margin: 20px 0; }
    p { text-align: center; max-width: 700px; margin: 0 auto 20px; line-height: 1.6; }
    .logo {
      width: 150px;
      animation: float 3s ease-in-out infinite;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    /* Giriş ekranı */
    #preloader {
      background-color: #000;
      width: 100%;
      height: 100vh;
      position: fixed;
      top: 0; left: 0;
      z-index: 9999;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* Bölümler */
    section {
      padding: 60px 20px;
      border-bottom: 1px solid rgba(255, 255, 255, 0.05);
    }

    /* Butonlar */
    .btn {
      background: transparent;
      border: 2px solid #00d4ff;
      padding: 10px 20px;
      color: #00d4ff;
      font-size: 16px;
      margin: 10px;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }
    .btn:hover {
      background: #00d4ff;
      color: #000;
    }

    /* Başvuru pop-up */
    #formModal {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.8);
      justify-content: center;
      align-items: center;
      z-index: 10;
    }
    #formModal .form-box {
      background: #1a1a1a;
      padding: 30px;
      border-radius: 10px;
      width: 90%;
      max-width: 500px;
    }
    #formModal input, #formModal textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      background: #333;
      border: none;
      color: #fff;
      border-radius: 5px;
    }

    /* TikTok Panel */
    #ttPanel {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #111;
      padding: 15px;
      border-radius: 10px;
      border: 2px solid #00d4ff;
      display: none;
    }
    .tt-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #00d4ff;
      padding: 10px;
      border-radius: 50%;
      color: #000;
      font-size: 20px;
      cursor: pointer;
    }

    /* Karakter kartları */
    .characters {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 40px;
      margin-top: 20px;
    }
    .char-box {
      text-align: center;
    }
    .char-box img {
      width: 120px;
      height: auto;
      background: #0f0f0f;
      border-radius: 12px;
    }
    .char-box span {
      display: block;
      margin-top: 10px;
      font-size: 18px;
      color: #00d4ff;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 30px 10px;
      font-size: 14px;
      color: #777;
      background: #0a0a0a;
    }

    /* Ziyaretçi sayacı */
    .counter {
      text-align: center;
      font-size: 16px;
      margin-top: 20px;
    }

    @media (max-width: 600px) {
      .characters { flex-direction: column; align-items: center; }
    }
  </style>
</head>
<body>

<!-- Yüklenme ekranı -->
<div id="preloader">
  <img src="logo.png" class="logo" alt="ZZONE99 Logo">
</div>

<!-- Giriş -->
<section>
  <img src="logo.png" class="logo" alt="Logo" />
  <h1 id="siteTitle">ZZONE99</h1>
  <div class="btn-group" style="text-align:center;">
    <button class="btn" onclick="showSection('tanitim')">Tanıtım</button>
    <button class="btn" onclick="openForm()">KLANA KATIL</button>
    <button class="btn" onclick="toggleTT()">İletişim</button>
  </div>
</section>

<!-- Tanıtım -->
<section id="tanitim">
  <h2>TANITIM</h2>
  <p>
    PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur. İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş, bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir. Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmak.
  </p>
  <div class="characters">
    <div class="char-box">
      <img src="mazz.png" alt="mAzz99" />
      <span>mAzz99</span>
    </div>
    <div class="char-box">
      <img src="yazz.png" alt="yAzz99" />
      <span>yAzz99</span>
    </div>
  </div>
</section>

<!-- Pop-up Başvuru Formu -->
<div id="formModal">
  <div class="form-box">
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="oyuncu" placeholder="Oyuncu Adı & UID" required />
      <input type="text" name="isim" placeholder="İsminiz" required />
      <input type="number" name="yas" placeholder="Yaş" required />
      <input type="text" name="cihaz" placeholder="Kullandığınız Cihaz" required />
      <textarea name="aktiflik" placeholder="Aktiflik (Günlük/Saat)" required></textarea>
      <button class="btn" type="submit">Başvuru Yap</button>
    </form>
    <button class="btn" onclick="closeForm()">Kapat</button>
  </div>
</div>

<!-- TikTok Panel -->
<div id="ttPanel">
  <p><strong>TikTok:</strong></p>
  <p>mAzz99 – <a href="https://tiktok.com/@mazz99theboss" target="_blank">@mazz99theboss</a></p>
  <p>yAzz99 – <a href="https://tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a></p>
</div>
<div class="tt-btn" onclick="toggleTT()">📱</div>

<!-- Sayaç ve Footer -->
<div class="counter" id="visitorCount">Ziyaretçi: 1</div>

<footer>
  <p>Für die Famiilla • SINCE 2018 • ZZONE99</p>
</footer>

<!-- JS -->
<script>
  // Yüklenme animasyonu
  window.addEventListener("load", () => {
    document.getElementById("preloader").style.display = "none";
  });

  // Sayfa gösterimi
  function showSection(id) {
    const el = document.getElementById(id);
    el.scrollIntoView({ behavior: 'smooth' });
  }

  // Pop-up
  function openForm() {
    document.getElementById("formModal").style.display = "flex";
  }
  function closeForm() {
    document.getElementById("formModal").style.display = "none";
  }

  // TikTok paneli
  function toggleTT() {
    const panel = document.getElementById("ttPanel");
    panel.style.display = panel.style.display === "block" ? "none" : "block";
  }

  // Ziyaretçi sayacı (fake basit)
  const count = localStorage.getItem("visitorCount") || 1;
  document.getElementById("visitorCount").innerText = "Ziyaretçi: " + count;
  localStorage.setItem("visitorCount", parseInt(count) + 1);
</script>
</body>
