<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZZONE99 - PUBG MOBILE</title>
  <style>
    body {
      margin: 0;
      background-color: #0a0a0a;
      color: #feda6a;
      font-family: Arial, sans-serif;
    }
    header {
      text-align: center;
      padding: 40px 20px 20px;
    }
    header img {
      max-width: 300px;
    }
    section {
      max-width: 800px;
      margin: 20px auto;
      padding: 20px;
      background: #111;
      border-radius: 10px;
      border: 2px solid #feda6a;
    }
    h2 {
      border-bottom: 1px solid #feda6a;
      padding-bottom: 10px;
      margin-bottom: 20px;
    }
    .members, .uyeler {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      justify-content: center;
    }
    .card, .card-nofoto {
      background: #1a1a1a;
      padding: 15px;
      border: 1px solid #feda6a;
      border-radius: 8px;
      width: 140px;
      text-align: center;
      color: #fff;
    }
    .card img {
      width: 80px;
      height: 80px;
      border-radius: 50%;
      margin-bottom: 10px;
    }
    a {
      color: #feda6a;
      text-decoration: none;
      font-size: 14px;
    }
    form input, form textarea {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      background: #1a1a1a;
      color: white;
      border: 1px solid #feda6a;
      border-radius: 5px;
    }
    form button {
      background: #feda6a;
      color: black;
      border: none;
      padding: 10px 20px;
      border-radius: 5px;
      font-weight: bold;
      cursor: pointer;
    }
    footer {
      text-align: center;
      color: #888;
      padding: 30px 10px;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <header>
    <img src="logo.png" alt="ZZONE99 Logo">
  </header>

  <section>
    <h2>Hakkımızda</h2>
    <p>ZZONE99, PUBG MOBILE evreninde 2018'den beri aktif, agresif ve disiplinli bir klan grubudur. Amacımız sadece savaşmak değil, iz bırakmak!</p>
  </section>

  <section>
    <h2>Kadro</h2>
    <div class="members">
      <div class="card">
        <img src="https://robohash.org/mazz99?set=set2" alt="mAzz99">
        <strong>mAzz99</strong><br>
        <a href="https://tiktok.com/@mazz99theboss" target="_blank">TikTok</a>
      </div>
      <div class="card">
        <img src="https://robohash.org/yazz99?set=set2" alt="yAzz99">
        <strong>yAzz99</strong><br>
        <a href="https://tiktok.com/@yazz99" target="_blank">TikTok</a>
      </div>
      <div class="card">
        <img src="https://robohash.org/iszz99?set=set2" alt="iSzz99">
        <strong>iSzz99</strong>
      </div>
    </div>
  </section>

  <section>
    <h2>Üyelerimiz</h2>
    <div class="uyeler">
      <div class="card-nofoto">Üye1</div>
      <div class="card-nofoto">Üye2</div>
      <div class="card-nofoto">Üye3</div>
    </div>
  </section>

  <section>
    <h2>Klan Başvurusu</h2>
    <form action="mailto:tayf.pm@gmail.com" method="POST" enctype="text/plain">
      <input type="text" name="oyuncuAdi" placeholder="Oyuncu Adın" required>
      <input type="text" name="yas" placeholder="Yaş" required>
      <textarea name="neden" rows="4" placeholder="Neden katılmak istiyorsun?" required></textarea>
      <button type="submit">Gönder</button>
    </form>
  </section>

  <footer>
    ZZONE99 © 2018 - PUBG MOBILE TAKIMI
  </footer>

</body>
</html>
