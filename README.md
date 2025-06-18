<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="ZZONE99 PUBG Mobile klanı için başvuru ve tanıtım sitesi. Since 2018."/>
  <meta name="keywords" content="ZZONE99, PUBG Mobile, Clan Başvuru, Fur die Gang, AREA323"/>
  <meta name="author" content="ZZONE99"/>
  <title>ZZONE99</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&family=Montserrat&display=swap" rel="stylesheet"/>
  <style>
    * {
      margin: 0; padding: 0; box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
    }
    body {
      background: linear-gradient(135deg, #111, #1f1f1f);
      color: #fff;
      overflow-x: hidden;
    }
    header, section, footer {
      padding: 2rem;
      text-align: center;
    }

    /* Loading */
    #loading {
      position: fixed;
      top: 0; left: 0;
      width: 100vw; height: 100vh;
      background: #000;
      color: #fff;
      display: flex; align-items: center; justify-content: center;
      font-size: 2rem;
      z-index: 9999;
      transition: 1s;
    }

    /* Giriş ekranı */
    #giris {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: radial-gradient(circle, #222, #000);
      animation: fadeIn 2s ease forwards;
    }
    #giris img {
      width: 120px;
      margin-bottom: 1rem;
      animation: pulse 2s infinite;
    }
    #giris h1 {
      font-size: 2.5rem;
      letter-spacing: 5px;
      font-family: 'Orbitron', sans-serif;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes pulse {
      0% { transform: scale(1); opacity: 0.8; }
      50% { transform: scale(1.1); opacity: 1; }
      100% { transform: scale(1); opacity: 0.8; }
    }

    .buton {
      margin: 1rem auto;
      display: inline-block;
      padding: 0.8rem 1.5rem;
      background: #0f0f0f;
      border: 1px solid #444;
      border-radius: 5px;
      color: #fff;
      text-decoration: none;
      transition: 0.3s ease;
    }
    .buton:hover {
      background: #fff;
      color: #000;
    }

    #aciklama {
      max-width: 700px;
      margin: auto;
      font-size: 1.1rem;
      line-height: 1.7;
    }

    .uyeler {
      display: flex;
      justify-content: center;
      gap: 2rem;
      flex-wrap: wrap;
      margin-top: 2rem;
    }
    .uye {
      background: #222;
      padding: 1rem 2rem;
      border-radius: 10px;
      font-size: 1.2rem;
      font-weight: bold;
    }

    form {
      max-width: 500px;
      margin: auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      background: #1b1b1b;
      padding: 2rem;
      border-radius: 10px;
    }
    input, textarea {
      padding: 0.8rem;
      background: #333;
      border: 1px solid #555;
      color: #fff;
      border-radius: 5px;
    }
    .tiktok {
      margin-top: 2rem;
    }
    .tiktok a {
      display: inline-block;
      margin: 0.5rem;
      text-decoration: none;
      color: #1DA1F2;
    }

    footer {
      margin-top: 4rem;
      font-size: 0.9rem;
      color: #aaa;
    }

    #onlineCount {
      font-size: 1.2rem;
      margin-top: 1rem;
      color: #0f0;
    }

    @media(max-width: 600px) {
      #giris h1 { font-size: 1.8rem; }
      .uyeler { flex-direction: column; }
    }
  </style>
  <script>
    // Simüle edilmiş online kişi sayısı
    function updateOnlineCount() {
      const count = Math.floor(Math.random() * 20) + 3;
      document.getElementById("onlineCount").innerText = "Online Üyeler: " + count;
    }
    window.onload = () => {
      document.getElementById("loading").style.display = "none";
      updateOnlineCount();
      setInterval(updateOnlineCount, 7000);
    };
  </script>
</head>
<body>

  <div id="loading">Yükleniyor...</div>

  <!-- Giriş -->
  <div id="giris">
    <img src="logo.png" alt="Logo">
    <h1>ZZONE99</h1>
    <a href="#tanitim" class="buton">Giriş Yap</a>
  </div>

  <!-- Tanıtım -->
  <section id="tanitim">
    <h2>Tanıtım</h2>
    <div id="aciklama">
      <p>
        ZZONE99, PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.
        İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,
        bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.
        Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmak.
      </p>
      <p id="onlineCount"></p>
    </div>
  </section>
  <!-- Başvuru -->
  <section id="basvuru">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="Oyuncu Adı ve UID" placeholder="Oyuncu Adı ve UID" required>
      <input type="text" name="Yaş" placeholder="Yaşınız" required>
      <input type="text" name="Aktiflik" placeholder="Günde kaç saat oynuyorsunuz?" required>
      <input type="text" name="Kullandığı cihaz" placeholder="Kullandığınız cihaz" required>
      <button type="submit" class="buton">Başvuruyu Gönder</button>
    </form>
  </section>

  <!-- TikTok ve İletişim -->
  <section class="tiktok">
    <h2>İletişim</h2>
    <p><a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">📱 @mAzz99theboss</a></p>
    <p><a href="https://www.tiktok.com/@babavizyondapm" target="_blank">📱 @babavizyondapm</a></p>
  </section>

  <!-- Footer -->
  <footer>
    Für die Famillia • Since 2018
  </footer>

</body>
