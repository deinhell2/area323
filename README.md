<!DOCTYPE html><html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Klan Alım - 2018'den Beri</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }body {
  margin: 0;
  font-family: 'Orbitron', sans-serif;
  color: white;
  background: linear-gradient(270deg, #0f0f0f, #1a1a1a);
  background-size: 400% 400%;
  animation: backgroundShift 10s ease infinite;
}

@keyframes backgroundShift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

header {
  text-align: center;
  padding: 2rem 1rem;
}

header img {
  width: 40vw;
  max-width: 200px;
  margin-bottom: 1rem;
}

h1 {
  font-size: 1.5rem;
  margin: 0.5rem 0;
}

p {
  max-width: 90%;
  margin: 1rem auto;
  font-size: 1rem;
}

.buttons {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  margin-top: 2rem;
}

@media (min-width: 600px) {
  .buttons {
    flex-direction: row;
  }
}

.button {
  padding: 1rem 2rem;
  background-color: #e50914;
  border: none;
  border-radius: 8px;
  color: white;
  font-size: 1rem;
  cursor: pointer;
  text-decoration: none;
  transition: background 0.3s ease;
  text-align: center;
  width: 200px;
}

.button:hover {
  background-color: #ff2a2a;
}

.leader-section {
  max-width: 900px;
  margin: 4rem auto;
  padding: 0 1rem;
  text-align: center;
}

.leader-cards {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

@media (min-width: 600px) {
  .leader-cards {
    flex-direction: row;
    justify-content: center;
  }
}

.card {
  background: #222;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(255, 0, 0, 0.3);
  flex: 1;
}

.card h3 {
  margin-top: 0;
  font-size: 1.2rem;
}

.card a {
  display: inline-block;
  margin-top: 0.5rem;
  color: #ff5959;
  text-decoration: none;
  font-size: 0.95rem;
}

.card a:hover {
  text-decoration: underline;
}

footer {
  margin-top: 4rem;
  text-align: center;
  padding: 2rem 1rem;
  border-top: 1px solid #333;
}

.socials a {
  display: block;
  color: #ccc;
  margin: 0.5rem 0;
  font-size: 1rem;
  text-decoration: none;
}

@media (min-width: 600px) {
  .socials a {
    display: inline-block;
    margin: 0 1rem;
  }
}

  </style>
</head>
<body>
  <header>
    <img src="logo.png" alt="Klan Logosu">
    <h1>2018'den Beri Sahada: Önce Fur die GANG, Sonra AREA323. Şimdi Yepyeni Bir Güç!</h1>
    <p>Klanımız 2018 yılından bu yana sahalarda! Taktik, takım oyunu ve zafer için buradayız. PUBG arenasında bizimle oynamaya hazır mısın?</p>
    <div class="buttons">
      <a href="https://formspree.io/f/xkgbzjqp" class="button">Başvuru Yap</a>
      <a href="#iletisim" class="button">İletişim</a>
    </div>
  </header>  <section class="leader-section">
    <h2>Klan Liderleri</h2>
    <div class="leader-cards">
      <div class="card">
        <h3>mAzz99</h3>
        <p>Taktiksel lider, kurucu. Ekibin beyni!</p>
        <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">TikTok: @mAzz99theboss</a>
      </div>
      <div class="card">
        <h3>yAzz99</h3>
        <p>Vizyoner stratejist. Sahada ve planlamada öncü.</p>
        <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">TikTok: @babavizyondapm</a>
      </div>
    </div>
  </section>  <footer id="iletisim">
    <h2>İletişim</h2>
    <div class="socials">
      <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">mAzz99 (@mAzz99theboss)</a>
      <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">yAzz99 (@babavizyondapm)</a>
    </div>
  </footer>
</body>
</html>
