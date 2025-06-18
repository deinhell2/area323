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
      background: linear-gradient(-45deg, #e0f7fa, #ffffff, #f1f8e9, #e3f2fd);
      background-size: 400% 400%;
      animation: bgAnim 15s ease infinite;
      color: #222;
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
      background: #00bcd4;
      color: white;
      padding: 1rem 2rem;
      border: none;
      border-radius: 8px;
      margin-top: 2rem;
      cursor: pointer;
      font-size: 1rem;
      transition: all 0.3s ease;
    }
    .button:hover {
      background: #008c9e;
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
      border: 1px solid #ccc;
      border-radius: 10px;
      font-size: 1rem;
    }

    footer {
      background: rgba(0,0,0,0.05);
      text-align: center;
      padding: 1.5rem;
      font-size: 0.9rem;
    }

    .socials a {
      display: inline-block;
      margin: 0.5rem;
      color: #00bcd4;
      text-decoration: none;
      font-weight: bold;
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
    <button class="button" onclick="showSection('basvuru')">Başvuru Yap</button>
    <button class="button" onclick="showSection('iletisim')">İletişim</button>
    <button class="button" onclick="showSection('acilis')">Çıkış</button>
  </section>

  <!-- Başvuru Formu -->
  <section id="basvuru" class="hidden">
    <h1>Başvuru Formu</h1>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="oyuncu_id" placeholder="Oyuncu ID" required>
      <input type="text" name="oyun_suresi" placeholder="Ne zamandır oynuyorsun?" required>
      <input type="text" name="eski_klanlar" placeholder="Eski Clan'ların" required>
      <input type="text" name="cihaz" placeholder="Kullandığın cihaz" required>
      <button class="button" type="submit">Gönder</button>
    </form>
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
    <p>&copy; 2025 ZZONE99. Tüm hakları saklıdır.</p>
  </footer>
</body>
