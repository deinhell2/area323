<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="ZZONE99 PUBG Mobile Klanı Resmi Sitesi">
  <title>ZZONE99</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #0f0f0f, #1a1a1a);
      color: white;
      overflow-x: hidden;
    }

    /* Giriş Ekranı */
    #intro {
      position: fixed;
      z-index: 9999;
      width: 100vw;
      height: 100vh;
      background-color: black;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      animation: fadeOut 2s ease 2s forwards;
    }
    #intro img {
      width: 100px;
      height: auto;
      animation: pulse 2s infinite;
    }
    #intro h1 {
      margin-top: 20px;
      font-size: 2.5rem;
      color: #0ff;
    }
    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.1); }
    }
    @keyframes fadeOut {
      to { opacity: 0; visibility: hidden; }
    }

    header {
      padding: 40px 20px;
      text-align: center;
    }

    header img {
      width: 120px;
      height: auto;
      margin-bottom: 10px;
    }

    header h2 {
      font-size: 2.2rem;
      color: #0ff;
      text-shadow: 0 0 8px #0ff;
    }

    section {
      padding: 40px 20px;
      text-align: center;
    }

    .button {
      display: inline-block;
      padding: 12px 24px;
      margin: 10px;
      font-size: 1rem;
      background-color: #0ff;
      color: #000;
      border: none;
      border-radius: 6px;
      transition: 0.3s;
      cursor: pointer;
    }

    .button:hover {
      background-color: #0cc;
    }

    /* Liderler */
    .leaders {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 40px;
    }

    .leader-card {
      background-color: rgba(255,255,255,0.05);
      border: 1px solid #0ff;
      padding: 20px;
      border-radius: 10px;
      width: 250px;
      transition: 0.3s;
    }

    .leader-card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px #0ff;
    }

    .leader-card h3 {
      color: #0ff;
      font-size: 1.4rem;
    }

    .leader-card p {
      color: #ccc;
    }

    /* Başvuru Takip */
    #application-status {
      background-color: #111;
      padding: 20px;
      margin-top: 30px;
      border-radius: 10px;
      border: 1px solid #0ff;
    }

    footer {
      padding: 20px;
      text-align: center;
      font-size: 0.9rem;
      color: #888;
    }

  </style>
</head>
<body>

  <!-- Giriş Ekranı -->
  <div id="intro">
    <img src="logo.png" alt="ZZONE99 Logo" />
    <h1>ZZONE99</h1>
  </div>

  <header>
    <img src="logo.png" alt="Logo">
    <h2>ZZONE99</h2>
  </header>

  <section id="tanitim">
    <p>
      PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir. <br><br>
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </p>
  </section>

  <section id="buttons">
    <a href="#form" class="button">KLANA KATIL</a>
    <a href="#liderler" class="button">LİDERLER</a>
  </section>

  <section id="liderler">
    <h2>LİDERLER</h2>
    <div class="leaders">
      <div class="leader-card">
        <h3>mAzz99</h3>
        <p>ID: 516572604</p>
      </div>
      <div class="leader-card">
        <h3>yAzz99</h3>
        <p>ID: 520654025</p>
      </div>
    </div>
  </section>

  <section id="form">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="oyuncu_adi_uid" placeholder="Oyuncu Adı ve UID" required><br><br>
      <input type="text" name="isim" placeholder="İsminiz" required><br><br>
      <input type="number" name="yas" placeholder="Yaşınız" required><br><br>
      <input type="text" name="cihaz" placeholder="Kullandığınız Cihaz" required><br><br>
      <input type="text" name="aktiflik" placeholder="Aktiflik Durumunuz" required><br><br>
      <button type="submit" class="button">Gönder</button>
    </form>
  </section>

  <section id="application-status">
    <h3>Başvuru Durumu</h3>
    <p>Başvurunuz alındıktan sonra en kısa sürede size dönüş yapılacaktır.</p>
    <p>Durum: Onaylandı / Onaylanmadı olarak iletilecek.</p>
  </section>

  <footer>
    <p>Für die Famillia | SINCE 2018</p>
  </footer>

</body>
