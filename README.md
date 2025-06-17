<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ZZONE99 - Klan Tanıtımı</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Orbitron', sans-serif;
      color: #f00;
      background-color: #000;
      background: url('https://i.gifer.com/3zDq.gif') no-repeat center center fixed;
      background-size: cover;
      overflow-x: hidden;
    }
    header {
      text-align: center;
      padding: 40px 20px 20px;
    }
    header img {
      width: 300px;
      max-width: 80vw;
      animation: pulse 2s infinite;
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
    }
    section {
      background-color: rgba(0, 0, 0, 0.8);
      padding: 30px;
      margin: 20px auto;
      width: 90%;
      max-width: 800px;
      border-radius: 10px;
      box-shadow: 0 0 15px #f00;
    }
    h2 {
      border-bottom: 1px solid #f00;
      padding-bottom: 10px;
      margin-bottom: 20px;
    }
    form input, form textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      background: #111;
      color: white;
      border: 1px solid #f00;
      border-radius: 5px;
    }
    form button {
      background: #f00;
      color: white;
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .members {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .card {
      background: #111;
      border: 1px solid #f00;
      padding: 15px;
      border-radius: 10px;
      width: 180px;
      text-align: center;
    }
    .card img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      margin-bottom: 10px;
    }
    .card a {
      color: #f00;
      text-decoration: none;
      font-size: 14px;
    }
    iframe {
      width: 100%;
      border: none;
      border-radius: 10px;
      height: 300px;
    }
    footer {
      text-align: center;
      padding: 30px;
      color: #777;
    }
    a {
      color: #f00;
    }
  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="ZZONE99 Logo" />
  </header>  <section>
    <h2>Klan Hakkında</h2>
    <p>ZZONE99, 2018 yılından beri aktif olan, kuralsız ama etkili bir takım ruhuyla ilerleyen agresif bir oyuncu topluluğudur. "Ne dengemiz ne dengimiz var" felsefesiyle sahaları domine eder.</p>
  </section>  <section>
    <h2>Yönetim Kadrosu</h2>
    <div class="members">
      <div class="card">
        <img src="https://robohash.org/mazz99?set=set2" alt="mAzz99" />
        <strong>mAzz99</strong><br>Lider<br>
        <a href="https://tiktok.com/@mazz99theboss" target="_blank">TikTok</a>
      </div>
      <div class="card">
        <img src="https://robohash.org/yazz99?set=set2" alt="yAzz99" />
        <strong>yAzz99</strong><br>Yönetici<br>
        <a href="https://tiktok.com/@yazz99" target="_blank">TikTok</a>
      </div>
      <div class="card">
        <img src="https://robohash.org/iszz99?set=set2" alt="iSzz99" />
        <strong>iSzz99</strong><br>Yönetici
      </div>
    </div>
  </section>  <section>
    <h2>Başvuru Formu</h2>
    <form action="mailto:tayf.pm@gmail.com" method="POST" enctype="text/plain">
      <input type="text" name="oyuncuAdi" placeholder="Oyuncu Adın" required />
      <input type="text" name="yas" placeholder="Yaş" required />
      <input type="text" name="oyun" placeholder="Oynadığın Oyun" required />
      <textarea name="neden" rows="4" placeholder="Neden klana katılmak istiyorsun?" required></textarea>
      <button type="submit">Başvur</button>
    </form>
  </section>  <footer>
    ZZONE99 © 2018 - Tüm hakları saklıdır.
  </footer>
</body>
