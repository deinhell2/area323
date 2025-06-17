<!DOCTYPE html><html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ZZONE99 - PUBG MOBILE Klanı</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: 'Orbitron', sans-serif;
      color: #feda6a;
      background-color: #000;
      background: url('https://cdn.pixabay.com/photo/2021/04/25/19/35/war-6206675_1280.jpg') no-repeat center center fixed;
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
      animation: fadeIn 2s ease-in;
    }
    @keyframes fadeIn {
      0% { opacity: 0; transform: translateY(-20px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    section {
      background-color: rgba(0, 0, 0, 0.85);
      padding: 30px;
      margin: 20px auto;
      width: 90%;
      max-width: 800px;
      border-radius: 10px;
      border: 2px solid #feda6a;
    }
    h2 {
      border-bottom: 1px solid #feda6a;
      padding-bottom: 10px;
      margin-bottom: 20px;
    }
    p, li {
      font-size: 16px;
      line-height: 1.6;
    }
    form input, form textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      background: #1a1a1a;
      color: white;
      border: 1px solid #feda6a;
      border-radius: 5px;
    }
    form button {
      background: #feda6a;
      color: #000;
      padding: 10px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }
    .members, .uyeler {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }
    .card {
      background: #1a1a1a;
      border: 1px solid #feda6a;
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
      color: #feda6a;
      text-decoration: none;
      font-size: 14px;
    }
    .card-nofoto {
      background: #1a1a1a;
      border: 1px solid #feda6a;
      padding: 15px;
      border-radius: 10px;
      width: 150px;
      text-align: center;
      font-size: 16px;
      font-weight: bold;
    }
    footer {
      text-align: center;
      padding: 30px;
      color: #ccc;
    }
    a {
      color: #feda6a;
    }
  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="ZZONE99 Logo" />
  </header>  <section>
    <h2>Hakkımızda</h2>
    <p>ZZONE99, PUBG MOBILE arenasında 2018'den bu yana aktif olan elit bir klan grubudur. Agresif oyun tarzı, takım uyumu ve oyun zekasıyla rakiplerine korku salan bir ekip olarak bilinmektedir. Amacımız sadece kazanmak değil, korku yaymak!</p>
  </section>  <section>
    <h2>Kadro</h2>
    <div class="members">
      <div class="card">
        <img src="https://robohash.org/mazz99?set=set2" alt="mAzz99" />
        <strong>mAzz99</strong><br>
        <a href="https://tiktok.com/@mazz99theboss" target="_blank">TikTok</a>
      </div>
      <div class="card">
        <img src="https://robohash.org/yazz99?set=set2" alt="yAzz99" />
        <strong>yAzz99</strong><br>
        <a href="https://tiktok.com/@yazz99" target="_blank">TikTok</a>
      </div>
      <div class="card">
        <img src="https://robohash.org/iszz99?set=set2" alt="iSzz99" />
        <strong>iSzz99</strong>
      </div>
    </div>
  </section>  <section>
    <h2>Üyelerimiz</h2>
    <div class="uyeler">
      <div class="card-nofoto">Üye1</div>
      <div class="card-nofoto">Üye2</div>
      <div class="card-nofoto">Üye3</div>
      <div class="card-nofoto">Üye4</div>
    </div>
  </section>  <section>
    <h2>Klanımıza Katıl</h2>
    <form action="mailto:tayf.pm@gmail.com" method="POST" enctype="text/plain">
      <input type="text" name="oyuncuAdi" placeholder="Oyuncu Adın (PUBG Mobile)" required />
      <input type="text" name="yas" placeholder="Yaş" required />
      <input type="text" name="oyun" value="PUBG MOBILE" disabled />
      <textarea name="neden" rows="4" placeholder="Neden klana katılmak istiyorsun?" required></textarea>
      <button type="submit">Başvur</button>
    </form>
  </section>  <footer>
    ZZONE99 © 2018 - PUBG MOBILE TAKIMI
  </footer>
</body>
</html>
