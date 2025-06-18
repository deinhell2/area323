<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZZONE99 - PUBG Klanı</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: 'Inter', sans-serif;
      background: radial-gradient(circle at 10% 20%, #111927, #0d1117, #1a1f2b);
      background-size: 400% 400%;
      animation: bgAnim 20s ease infinite;
      color: #f0f0f0;
      overflow-x: hidden;
    }
    @keyframes bgAnim {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    section {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 2rem;
      text-align: center;
      background: rgba(0, 0, 0, 0.3);
      backdrop-filter: blur(10px);
    }

    .logo {
      width: 140px;
      animation: spinLogo 4s infinite ease-in-out;
    }
    @keyframes spinLogo {
      0% { transform: rotate(0deg); }
      50% { transform: rotate(3deg) scale(1.05); }
      100% { transform: rotate(0deg); }
    }

    h1 {
      font-size: 3rem;
      margin: 1rem 0;
      font-weight: 700;
      animation: fadeIn 2s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .button {
      background: rgba(255, 255, 255, 0.1);
      color: #ffffff;
      padding: 1rem 2rem;
      border: 1px solid #ffffff33;
      border-radius: 12px;
      margin-top: 1.2rem;
      cursor: pointer;
      font-size: 1rem;
      transition: all 0.3s ease;
      backdrop-filter: blur(5px);
    }
    .button:hover {
      background: rgba(255, 255, 255, 0.25);
      transform: scale(1.05);
    }

    .hidden { display: none; }

    .content {
      max-width: 800px;
      padding: 2rem;
      font-size: 1.1rem;
      line-height: 1.6;
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      max-width: 500px;
      width: 100%;
      margin: 2rem auto;
    }

    input, textarea {
      padding: 1rem;
      border: 1px solid #555;
      border-radius: 10px;
      background: rgba(255, 255, 255, 0.1);
      color: white;
      font-size: 1rem;
    }

    footer {
      background: rgba(255, 255, 255, 0.05);
      text-align: center;
      padding: 1.5rem;
      font-size: 0.9rem;
    }

    .socials a {
      display: inline-block;
      margin: 0.5rem;
      color: #00e5ff;
      text-decoration: none;
      font-weight: bold;
    }

    .members {
      margin-top: 2rem;
    }
    .members h2 {
      font-size: 1.8rem;
      margin-bottom: 1rem;
    }
    .members ul {
      list-style: none;
      font-size: 1.1rem;
    }

    @media (max-width: 600px) {
      h1 { font-size: 2.2rem; }
      .button { width: 90%; }
    }
  </style>
  <script>
    function showSection(id) {
      document.querySelectorAll('section').forEach(s => s.classList.add('hidden'));
      document.getElementById(id).classList.remove('hidden');
    }
    window.onload = () => showSection('acilis');
  </script>
</head>
<body>
  <!-- Açılış Sayfası -->
  <section id="acilis">
    <img src="logo.png" alt="ZZONE99 Logo" class="logo">
    <h1>ZZONE99</h1>
    <button class="button" onclick="showSection('anasayfa')">Giriş</button>
  </section>

  <!-- Ana Sayfa -->
  <section id="anasayfa" class="hidden">
    <img src="logo.png" alt="ZZONE99 Logo" class="logo">
    <h1>ZZONE99</h1>
    <div class="content">
      <p><strong>Since 2018</strong> - Klanın ilk çıkış ismi <strong>Für die GANG</strong>, sonrasında <strong>AREA323</strong> ve yeni bir vizyon ile <strong>ZZONE99</strong> olarak devam edecektir.</p>
    </div>
    <button class="button" onclick="showSection('uyeler')">Üyeler</button>
    <button class="button" onclick="showSection('basvuru')">Başvuru Yap</button>
    <button class="button" onclick="showSection('iletisim')">İletişim</button>
    <button class="button" onclick="showSection('acilis')">Çıkış</button>
  </section>

  <!-- Üyeler Kısmı -->
  <section id="uyeler" class="hidden">
    <h1>Üyeler</h1>
    <div class="members">
      <h2>Lider Kadrosu</h2>
      <ul><li>mAzz99</li><li>yAzz99</li></ul>
      <h2>Yönetici Kadrosu</h2>
      <ul><li>iSzz99</li></ul>
    </div>
    <button class="button" onclick="showSection('anasayfa')">Geri Dön</button>
  </section>

  <!-- Başvuru Formu -->
  <section id="basvuru" class="hidden">
    <h1>Başvuru Formu</h1>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="oyuncu_adi_uid" placeholder="Oyuncu Adı ve UID" required>
      <input type="number" name="yas" placeholder="Yaş" required>
      <input type="text" name="aktiflik" placeholder="Aktiflik durumu (gün/saat)" required>
      <input type="text" name="cihaz" placeholder="Kullandığı cihaz" required>
      <button class="button" type="submit">Gönder</button>
    </form>
    <div class="content">
      <p><strong>Oyun içi iletişim:</strong> mAzz99 - 516572604</p>
    </div>
    <button class="button" onclick="showSection('anasayfa')">Geri Dön</button>
  </section>

  <!-- İletişim -->
  <section id="iletisim" class="hidden">
    <h1>İletişim</h1>
    <div class="socials">
      <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">@mAzz99theboss</a>
      <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a>
    </div>
    <button class="button" onclick="showSection('anasayfa')">Geri Dön</button>
  </section>

  <footer>
    <p>&copy; 2025 ZZONE99. Tüm hakları saklıdır. | für die famillia</p>
  </footer>
</body>
