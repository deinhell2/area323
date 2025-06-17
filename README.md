<!DOCTYPE html><html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZZONE99 Clan</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@700&display=swap');* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Orbitron', sans-serif;
  color: #fff;
  background: linear-gradient(-45deg, #000000, #222222, #111111, #333333);
  background-size: 400% 400%;
  animation: backgroundFlow 15s ease infinite;
}

@keyframes backgroundFlow {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

header {
  text-align: center;
  padding: 40px 20px 20px 20px;
}

header img {
  width: 120px;
  margin-bottom: 20px;
}

header h1 {
  font-size: 52px;
  color: #FF003C;
  text-shadow: 2px 2px 15px #ff0059;
  letter-spacing: 3px;
}

.slogan {
  margin: 20px 0;
  font-size: 22px;
  color: #ffffffcc;
  text-transform: uppercase;
  font-style: italic;
  text-shadow: 1px 1px 4px #000;
}

section.members, section.form-section {
  padding: 30px 25px;
  max-width: 700px;
  margin: 40px auto;
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 16px;
  box-shadow: 0 0 20px #ff005977;
  backdrop-filter: blur(6px);
}

section.members h2, section.form-section h2 {
  text-align: center;
  font-size: 28px;
  margin-bottom: 20px;
  color: #FF0059;
}

ul.member-list {
  list-style: none;
  font-size: 20px;
  padding: 0;
}

ul.member-list li {
  margin: 12px 0;
  text-align: center;
}

.social {
  text-align: center;
  margin: 30px 0;
}

.social a {
  display: inline-block;
  margin: 0 15px;
  font-size: 18px;
  color: #FF0059;
  text-decoration: none;
  transition: color 0.3s ease;
}

.social a:hover {
  color: #ff66a5;
}

footer {
  text-align: center;
  font-size: 14px;
  padding: 20px;
  color: #999;
}

form {
  display: flex;
  flex-direction: column;
}

form input, form textarea, form button {
  margin-bottom: 15px;
  padding: 12px;
  font-size: 16px;
  border-radius: 8px;
  border: none;
}

form input, form textarea {
  background-color: rgba(255, 255, 255, 0.1);
  color: #fff;
}

form button {
  background-color: #FF0059;
  color: white;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

form button:hover {
  background-color: #e6004d;
}

  </style>
</head>
<body>
  <header>
    <img src="Logo.png" alt="ZZONE99 Logo">
    <h1>ZZONE99</h1>
    <p class="slogan">ZAFER BİZİM ZONEMİZDE YAZILIR!</p>
  </header>  <section class="members">
    <h2>Üyeler</h2>
    <ul class="member-list">
      <li><strong>mAzz99</strong> - Lider</li>
      <li><strong>yAzz99</strong> - Lider</li>
      <li><strong>iSzz99</strong> - Yönetici</li>
    </ul>
  </section>  <section class="form-section">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xkgbzjqp" method="POST">
      <input type="text" name="name" placeholder="İsmin" required />
      <input type="text" name="uid" placeholder="PUBG UID" required />
      <textarea name="reason" placeholder="Neden katılmak istiyorsun?" required></textarea>
      <button type="submit">Başvur</button>
    </form>
  </section>  <div class="social">
    <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">@mAzz99theboss</a>
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a>
  </div>  <footer>
    &copy; 2025 ZZONE99 Klanı. Tüm hakları saklıdır.
  </footer>
</body>
</html>
