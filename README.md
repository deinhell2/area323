
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZZONE99 - Klan Sitesi</title>
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }body {
  font-family: 'Orbitron', sans-serif;
  background: linear-gradient(270deg, #e0f7fa, #fff);
  background-size: 400% 400%;
  animation: gradientBG 15s ease infinite;
  color: #333;
  overflow-x: hidden;
}

@keyframes gradientBG {
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
  text-align: center;
  padding: 2rem;
}

.logo {
  width: 160px;
  height: auto;
  animation: pulse 2s infinite ease-in-out;
}

@keyframes pulse {
  0% { transform: scale(1); opacity: 1; }
  50% { transform: scale(1.05); opacity: 0.9; }
  100% { transform: scale(1); opacity: 1; }
}

h1 {
  font-size: 2.5rem;
  margin: 1.5rem 0 1rem;
  color: #222;
}

.button {
  background: #00bcd4;
  color: white;
  padding: 1rem 2rem;
  border: none;
  border-radius: 8px;
  margin: 1rem;
  cursor: pointer;
  font-size: 1rem;
  transition: background 0.3s ease;
  text-decoration: none;
}

.button:hover {
  background: #008c9e;
}

.content {
  max-width: 800px;
  padding: 2rem;
}

.leaders {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  margin-top: 2rem;
}

@media(min-width: 600px) {
  .leaders {
    flex-direction: row;
    justify-content: center;
  }
}

.card {
  background: #ffffffcc;
  padding: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}

.card h3 {
  margin-bottom: 0.5rem;
  color: #00bcd4;
}

form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 500px;
  margin: 2rem auto;
}

input, textarea {
  padding: 0.8rem;
  border-radius: 8px;
  border: 1px solid #ccc;
  font-size: 1rem;
}

footer {
  background: #f0f0f0;
  padding: 2rem;
  text-align: center;
}

.socials a {
  display: block;
  color: #00bcd4;
  text-decoration: none;
  margin: 0.5rem 0;
}

.hidden {
  display: none;
}

  </style>
  <script>
    function showSection(id) {
      document.querySelectorAll('section').forEach(s => s.classList.add('hidden'));
      document.getElementById(id).classList.remove('hidden');
    }
    window.onload = () => showSection('giris');
  </script>
</head>
<body>
  <!-- Giriş Bölümü -->
  <section id="giris">
    <img src="logo.png" alt="ZZONE99 Logo" class="logo">
    <h1>ZZONE99</h1>
    <button class="button" onclick="showSection('tanitim')">Tanıtım</button>
    <button class="button" onclick="showSection('liderler')">Liderler</button>
    <button class="button" onclick="showSection('basvuru')">Başvuru Yap</button>
    <button class="button" onclick="showSection('iletisim')">İletişim</button>
  </section>  <!-- Tanıtım -->  <section id="tanitim" class="hidden">
    <div class="content">
      <h1>Tanıtım</h1>
      <p>Since 2018 - Klanın ilk çıkış ismi <strong>Für die GANG</strong>, sonrasında <strong>AREA323</strong> ve yeni bir vizyon ile <strong>ZZONE99</strong> olarak devam edecektir.</p>
      <button class="button" onclick="showSection('giris')">Geri Dön</button>
    </div>
  </section>  <!-- Lider Kartları -->  <section id="liderler" class="hidden">
    <h1>Klan Liderleri</h1>
    <div class="leaders">
      <div class="card">
        <h3>mAzz99</h3>
        <p>TikTok: <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">@mAzz99theboss</a></p>
      </div>
      <div class="card">
        <h3>yAzz99</h3>
        <p>TikTok: <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a></p>
      </div>
    </div>
    <button class="button" onclick="showSection('giris')">Geri Dön</button>
  </section>  <!-- Başvuru Formu -->  <section id="basvuru" class="hidden">
    <h1>Başvuru Formu</h1>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="oyuncu_id" placeholder="Oyuncu ID" required>
      <input type="text" name="oyun_suresi" placeholder="Ne zamandır oynuyorsun?" required>
      <input type="text" name="eski_klanlar" placeholder="Eski Clan'ların" required>
      <input type="text" name="cihaz" placeholder="Kullandığın cihaz" required>
      <button class="button" type="submit">Başvuru Gönder</button>
    </form>
    <button class="button" onclick="showSection('giris')">Geri Dön</button>
  </section>  <!-- Sosyal Medya -->  <section id="iletisim" class="hidden">
    <h1>İletişim</h1>
    <div class="socials">
      <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">@mAzz99theboss</a>
      <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a>
    </div>
    <button class="button" onclick="showSection('giris')">Geri Dön</button>
  </section>  <footer>
    <p>&copy; 2025 ZZONE99. Tüm hakları saklıdır.</p>
  </footer>
</body>
</html>
