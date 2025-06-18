<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="ZZONE99 - PUBG Mobile klanı, kuruluş yılı 2018. Modern, açık ve güçlü bir vizyon.">
  <meta name="keywords" content="ZZONE99, PUBG Klanı, AREA323, Fur die GANG, Mobil Oyun">
  <meta name="author" content="ZZONE99">
  <title>ZZONE99 | Since 2018</title>
  <link rel="icon" type="image/png" href="logo.png">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary-color: #00ffff;
      --bg-dark: rgba(10, 10, 10, 0.9);
      --bg-blur: rgba(255, 255, 255, 0.05);
      --text-color: #e0f7fa;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Orbitron', sans-serif;
    }

    body, html {
      height: 100%;
      overflow-x: hidden;
      background: #000;
      color: var(--text-color);
    }

    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: radial-gradient(ellipse at center, #121212 0%, #000000 100%);
      animation: bgAnim 30s ease-in-out infinite alternate;
      z-index: -2;
    }

    @keyframes bgAnim {
      0% {
        filter: hue-rotate(0deg);
      }
      100% {
        filter: hue-rotate(360deg);
      }
    }

    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
      z-index: -1;
    }

    .centered {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 2rem;
      transition: opacity 1s ease-in-out;
    }

    .hidden {
      opacity: 0;
      pointer-events: none;
    }

    .logo {
      width: 180px;
      height: auto;
      animation: zoomIn 2s ease forwards;
      filter: drop-shadow(0 0 10px var(--primary-color));
    }

    @keyframes zoomIn {
      from {
        transform: scale(0.5);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    h1 {
      font-size: 3rem;
      margin-top: 1rem;
      color: var(--primary-color);
      text-shadow: 0 0 10px var(--primary-color);
    }

    .btn {
      margin-top: 2rem;
      padding: 1rem 2rem;
      background: transparent;
      border: 2px solid var(--primary-color);
      color: var(--text-color);
      font-size: 1.2rem;
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.3s ease;
    }

    .btn:hover {
      background: var(--primary-color);
      color: #000;
      box-shadow: 0 0 20px var(--primary-color);
    }

    #main-content {
      display: none;
      flex-direction: column;
      align-items: center;
      padding: 3rem 1rem;
      gap: 2rem;
      opacity: 0;
    }

    .section {
      background: var(--bg-blur);
      padding: 2rem;
      border-radius: 12px;
      backdrop-filter: blur(10px);
      box-shadow: 0 0 15px rgba(0, 255, 255, 0.1);
      max-width: 800px;
      width: 100%;
      text-align: center;
    }

    footer {
      margin-top: 4rem;
      font-size: 1rem;
      color: #aaa;
    }

    .counter {
      font-size: 2rem;
      color: var(--primary-color);
      margin-top: 1rem;
    }
  </style>
</head>
<body>
  <div class="centered" id="entry">
    <img src="logo.png" alt="ZZONE99 Logo" class="logo">
    <h1>ZZONE99</h1>
    <button class="btn" onclick="enterSite()">Giriş</button>
  </div>

  <div id="main-content" class="centered">
    <div class="section" id="tanitim">
      <h2>Tanıtım</h2>
      <p>Since 2018<br>Klanın ilk çıkış ismi <strong>Für die GANG</strong>, sonrasında <strong>AREA323</strong> ve yeni bir vizyon ile <strong>ZZONE99</strong> olarak devam edecektir.</p>
    </div>

    <div class="section" id="uyeler">
      <h2>Üyeler</h2>
      <p><strong>Lider Kadrosu:</strong> mAzz99, yAzz99<br><strong>Yönetici Kadrosu:</strong> iSzz99</p>
      <div class="counter" id="memberCount">Toplam Üye: yükleniyor...</div>
    </div>

    <div class="section" id="basvuru">
      <h2>Başvuru Formu</h2>
      <form action="https://formspree.io/f/xldnljve" method="POST">
        <input type="text" name="oyuncu_adi_uid" placeholder="Oyuncu Adı ve UID" required><br><br>
        <input type="number" name="yas" placeholder="Yaş" required><br><br>
        <input type="text" name="aktiflik" placeholder="Aktiflik (gün/saat)" required><br><br>
        <input type="text" name="cihaz" placeholder="Kullandığınız cihaz" required><br><br>
        <button class="btn" type="submit">Başvur</button>
      </form>
    </div>

    <div class="section" id="iletisim">
      <h2>İletişim</h2>
      <p>TikTok: <br>@mAzz99theboss<br>@babavizyondapm</p>
      <p>Oyun İçi İletişim: mAzz99 - 516572604</p>
    </div>

    <footer>für die famillia</footer>
  </div>

  <script>
    function enterSite() {
      const entry = document.getElementById("entry");
      const main = document.getElementById("main-content");
      entry.classList.add("hidden");
      setTimeout(() => {
        entry.style.display = "none";
        main.style.display = "flex";
        setTimeout(() => main.style.opacity = 1, 50);
        history.pushState(null, null, "#main");
      }, 1000);
    }

    // Dinamik üye sayısı (örnek JSON verisi simülasyonu)
    document.addEventListener("DOMContentLoaded", () => {
      const memberCount = document.getElementById("memberCount");
      // Simülasyon - Gerçek API varsa fetch ile değiştirilebilir
      const uyeler = ["mAzz99", "yAzz99", "iSzz99", "üyex", "üyey", "üyelz"];
      memberCount.innerText = `Toplam Üye: ${uyeler.length}`;

      // Sayfa yönlendirme için hash kontrolü
      if (window.location.hash === "#main") enterSite();
    });
  </script>
</body>
