
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ZZONE99 - Klan Tanıtımı</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Orbitron', sans-serif;
      background-color: #0a0a0a;
      color: #f00;
      display: flex;
      flex-direction: column;
      align-items: center;
    }header {
  padding: 40px 20px 20px;
  text-align: center;
}

header img {
  width: 300px;
  max-width: 80vw;
}

section {
  max-width: 600px;
  width: 90%;
  margin: 30px 0;
  background-color: #111;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 15px #f00;
}

h2 {
  color: #f00;
  margin-top: 0;
  border-bottom: 1px solid #f00;
  padding-bottom: 10px;
}

form {
  display: flex;
  flex-direction: column;
}

input, textarea {
  background-color: #222;
  color: white;
  border: 1px solid #f00;
  padding: 10px;
  margin-bottom: 15px;
  border-radius: 5px;
}

button {
  background-color: #f00;
  color: white;
  border: none;
  padding: 10px;
  border-radius: 5px;
  cursor: pointer;
}

footer {
  padding: 30px 10px;
  text-align: center;
  font-size: 14px;
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
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/moqgjebz" method="POST">
      <input type="text" name="oyuncuAdi" placeholder="Oyuncu Adın" required />
      <input type="text" name="yas" placeholder="Yaş" required />
      <input type="text" name="oyun" placeholder="Oynadığın Oyun" required />
      <textarea name="neden" rows="4" placeholder="Neden klana katılmak istiyorsun?" required></textarea>
      <button type="submit">Başvur</button>
    </form>
  </section>  <section>
    <h2>İletişim</h2>
    <p>Bize ulaşmak için: <a href="tiktok.com/@mazz99theboss" target="_blank">@mazz99theboss</a></p>
  </section>  <footer>
    ZZONE99 © 2018 - Tüm hakları saklıdır.
  </footer>
</body>
