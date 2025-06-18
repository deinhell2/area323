<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="ZZONE99 PUBG Mobile Klan Sitesi - Since 2018" />
  <meta name="keywords" content="zzone99, pubg mobile, klan, başvuru" />
  <meta name="author" content="ZZONE99" />
  <title>ZZONE99 - Since 2018</title>
  <style>
    :root {
      --bg-light: #f4f4f4;
      --bg-dark: #121212;
      --text-light: #fff;
      --text-dark: #111;
      --primary: #0ef;
      --btn-hover: #0df;
    }
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      transition: background 0.4s, color 0.4s;
      background: var(--bg-light);
      color: var(--text-dark);
    }
    body.dark {
      background: var(--bg-dark);
      color: var(--text-light);
    }
    header {
      text-align: center;
      padding: 60px 20px 20px;
    }
    #logo {
      width: 120px;
      animation: zoomIn 2s ease;
    }
    h1 {
      font-size: 36px;
      margin-top: 10px;
    }
    @keyframes zoomIn {
      from { transform: scale(0.2); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }
    .theme-toggle {
      position: fixed;
      top: 20px;
      right: 20px;
      background: var(--primary);
      color: #000;
      padding: 8px 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    .section {
      padding: 30px 20px;
      max-width: 800px;
      margin: auto;
    }
    .button {
      background: var(--primary);
      color: #000;
      padding: 12px 24px;
      border: none;
      border-radius: 10px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
    }
    .button:hover {
      background: var(--btn-hover);
    }
    form {
      display: flex;
      flex-direction: column;
      gap: 12px;
      margin-top: 20px;
    }
    input, select, textarea {
      padding: 10px;
      border-radius: 8px;
      border: none;
      font-size: 16px;
    }
    .social-links {
      display: flex;
      gap: 20px;
      justify-content: center;
      margin-top: 30px;
    }
    .social-icon {
      position: relative;
      display: inline-block;
      cursor: pointer;
    }
    .social-icon img {
      width: 40px;
    }
    .popup {
      display: none;
      position: absolute;
      top: 50px;
      left: -20px;
      background: #333;
      color: white;
      padding: 10px;
      border-radius: 8px;
      font-size: 14px;
      z-index: 10;
      white-space: nowrap;
    }
    .social-icon:hover .popup {
      display: block;
    }
    footer {
      text-align: center;
      padding: 20px;
      font-size: 14px;
      opacity: 0.6;
    }
  </style>
</head>
<body>
  <button class="theme-toggle" onclick="toggleTheme()">Tema Değiştir</button>
  <header>
    <img src="logo.png" id="logo" alt="ZZONE99 Logo" />
    <h1>ZZONE99</h1>
    <p><strong>Since 2018</strong><br>İlk çıkış ismi: Für die GANG → AREA323 → ZZONE99</p>
  </header>

  <section class="section">
    <h2>Klan Tanıtımı</h2>
    <p>ZZONE99, 2018'den bu yana aktif bir PUBG Mobile klanıdır. Disiplinli, eğlenceli ve organize yapısıyla öne çıkar.</p>
  </section>

  <section class="section">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="Oyuncu Adı ve UID" placeholder="Oyuncu Adı ve UID" required />
      <input type="number" name="Yaş" placeholder="Yaş" required />
      <select name="Aktiflik" required>
        <option value="">Aktiflik Durumu</option>
        <option>Her gün</option>
        <option>Haftada birkaç</option>
        <option>Nadiren</option>
      </select>
      <input type="text" name="Cihaz" placeholder="Kullandığınız Cihaz" required />
      <button class="button" type="submit">Başvuru Yap</button>
    </form>
  </section>

  <section class="section">
    <h2>Oyun İçi İletişim</h2>
    <p><strong>mAzz99:</strong> 516572604</p>
    <p><strong>yAzz99:</strong> TikTok üzerinden ulaşabilirsiniz</p>
  </section>

  <section class="section">
    <h2>İletişim / Sosyal Medya</h2>
    <div class="social-links">
      <div class="social-icon">
        <img src="https://cdn-icons-png.flaticon.com/512/3046/3046123.png" alt="TikTok mAzz99" />
        <div class="popup">@mAzz99theboss</div>
      </div>
      <div class="social-icon">
        <img src="https://cdn-icons-png.flaticon.com/512/3046/3046123.png" alt="TikTok yAzz99" />
        <div class="popup">@babavizyondapm</div>
      </div>
    </div>
  </section>

  <footer>
    Für die Famillia
  </footer>

  <script>
    function toggleTheme() {
      document.body.classList.toggle("dark");
    }
  </script>
</body>
