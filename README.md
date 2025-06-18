<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99 PUBG Mobile Klanı</title>
<meta name="description" content="PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğu. İlk olarak Für die GANG adıyla kurulan ekip, AREA323 ile yükseldi, şimdi ZZONE99 olarak devam ediyor." />
<style>
  /* Temel Reset */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #001f3f, #0074D9);
    color: #e0f7fa;
    min-height: 100vh;
    overflow-x: hidden;
  }
  a {
    color: #00bcd4;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }
  header, main, footer {
    max-width: 960px;
    margin: auto;
    padding: 1rem;
  }
  /* Açılış ekranı */
  #splash {
    position: fixed;
    inset: 0;
    background: #001f3f;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #00bcd4;
    z-index: 1000;
    animation: fadeOutSplash 1s ease 2s forwards;
  }
  #splash img {
    width: 120px;
    height: auto;
    animation: logoGlow 2s infinite alternate;
    margin-bottom: 0.8rem;
  }
  #splash h1 {
    font-size: 3rem;
    letter-spacing: 0.3rem;
    font-weight: 900;
    text-shadow: 0 0 15px #00bcd4;
    animation: textGlow 2s infinite alternate;
  }
  @keyframes fadeOutSplash {
    to {opacity: 0; visibility: hidden;}
  }
  @keyframes logoGlow {
    from {filter: drop-shadow(0 0 10px #00bcd4);}
    to {filter: drop-shadow(0 0 25px #00bcd4);}
  }
  @keyframes textGlow {
    from {text-shadow: 0 0 15px #00bcd4;}
    to {text-shadow: 0 0 35px #00e5ff;}
  }

  /* Navbar */
  nav {
    background: rgba(0, 28, 58, 0.8);
    border-radius: 10px;
    padding: 0.5rem 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
  }
  nav .logo {
    display: flex;
    align-items: center;
    gap: 0.8rem;
  }
  nav .logo img {
    width: 50px;
    height: auto;
    filter: drop-shadow(0 0 5px #00bcd4);
    transition: transform 0.3s ease;
  }
  nav .logo img:hover {
    transform: scale(1.1);
  }
  nav .logo h2 {
    font-size: 1.8rem;
    color: #00bcd4;
    font-weight: 700;
    letter-spacing: 0.15rem;
    user-select: none;
  }

  /* Hamburger Menu */
  .menu-toggle {
    display: none;
    flex-direction: column;
    cursor: pointer;
  }
  .menu-toggle span {
    width: 28px;
    height: 3px;
    background: #00bcd4;
    margin-bottom: 5px;
    border-radius: 2px;
    transition: 0.3s;
  }

  ul.nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
  ul.nav-links li {
    cursor: pointer;
    position: relative;
  }
  ul.nav-links li a {
    font-size: 1.1rem;
    font-weight: 600;
    color: #00bcd4;
    padding: 0.3rem 0;
    transition: color 0.3s ease;
  }
  ul.nav-links li a:hover {
    color: #00e5ff;
  }
  /* Hover underline animation */
  ul.nav-links li a::after {
    content: "";
    position: absolute;
    width: 0%;
    height: 2px;
    background: #00e5ff;
    bottom: 0;
    left: 0;
    transition: width 0.3s ease;
  }
  ul.nav-links li a:hover::after {
    width: 100%;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .menu-toggle {
      display: flex;
    }
    ul.nav-links {
      position: fixed;
      top: 65px;
      right: 0;
      background: rgba(0, 28, 58, 0.95);
      height: calc(100vh - 65px);
      width: 200px;
      flex-direction: column;
      padding-top: 1rem;
      transform: translateX(100%);
      transition: transform 0.3s ease-in-out;
      border-radius: 0 0 0 10px;
      gap: 1.5rem;
    }
    ul.nav-links.active {
      transform: translateX(0);
    }
    ul.nav-links li a {
      font-size: 1.3rem;
      padding: 0.5rem 1rem;
    }
  }

  /* İçerik Bölümleri */
  section {
    margin-bottom: 3rem;
  }
  section h3 {
    font-size: 1.8rem;
    color: #00e5ff;
    text-shadow: 0 0 6px #00bcd4;
    margin-bottom: 1rem;
  }
  section p {
    font-size: 1.1rem;
    line-height: 1.5;
    color: #caf9ff;
    max-width: 800px;
  }

  /* Tanıtım açıklaması */
  #description {
    margin: auto;
    max-width: 800px;
  }

  /* Karakter kartları */
  #members {
    display: flex;
    justify-content: center;
    gap: 3rem;
    flex-wrap: wrap;
  }
  .member-card {
    background: rgba(0, 28, 58, 0.6);
    border-radius: 15px;
    padding: 1rem;
    width: 180px;
    text-align: center;
    box-shadow: 0 0 15px #00bcd4;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .member-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 0 30px #00e5ff;
  }
  .member-card img {
    width: 130px;
    height: auto;
    border-radius: 50%;
    margin-bottom: 0.7rem;
    filter: drop-shadow(0 0 5px #00bcd4);
  }
  .member-card h4 {
    color: #00e5ff;
    font-size: 1.4rem;
    font-weight: 700;
    text-shadow: 0 0 8px #00bcd4;
  }

  /* Başvuru butonu */
  .btn {
    display: inline-block;
    background: linear-gradient(45deg, #00bcd4, #0074D9);
    color: white;
    font-weight: 700;
    padding: 0.7rem 1.5rem;
    border-radius: 30px;
    cursor: pointer;
    transition: background 0.4s ease, box-shadow 0.4s ease;
    user-select: none;
  }
  .btn:hover {
    background: linear-gradient(45deg, #00e5ff, #005f8d);
    box-shadow: 0 0 20px #00e5ff;
  }
  .btn:active {
    transform: scale(0.95);
  }
  .btn-container {
    text-align: center;
    margin-bottom: 3rem;
  }

  /* Başvuru popup */
  #popupForm {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%) scale(0);
    background: #001f3f;
    padding: 2rem;
    border-radius: 20px;
    box-shadow: 0 0 25px #00bcd4;
    width: 90%;
    max-width: 450px;
    color: #caf9ff;
    transition: transform 0.3s ease;
    z-index: 1100;
  }
  #popupForm.active {
    transform: translate(-50%, -50%) scale(1);
  }
  #popupForm h3 {
    margin-bottom: 1rem;
    color: #00e5ff;
    text-align: center;
    text-shadow: 0 0 10px #00bcd4;
  }
  #popupForm label {
    display: block;
    margin: 0.8rem 0 0.3rem;
    font-weight: 600;
  }
  #popupForm input, #popupForm select {
    width: 100%;
    padding: 0.6rem;
    border-radius: 8px;
    border: none;
    font-size: 1rem;
  }
  #popupForm button.submit-btn {
    margin-top: 1.3rem;
    background: linear-gradient(45deg, #00bcd4, #0074D9);
    border: none;
    color: white;
    font-weight: 700;
    padding: 0.8rem;
    width: 100%;
    border-radius: 30px;
    cursor: pointer;
    transition: background 0.4s ease;
  }
  #popupForm button.submit-btn:hover {
    background: linear-gradient(45deg, #00e5ff, #005f8d);
  }
  #popupForm .close-btn {
    position: absolute;
    top: 12px;
    right: 16px;
    font-size: 1.6rem;
    font-weight: 700;
    cursor: pointer;
    color: #00e5ff;
  }

  /* Başvuru geri bildirim */
  #formFeedback {
    position: fixed;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    background: #004d73;
    padding: 1rem 2rem;
    border-radius: 30px;
    color: #caf9ff;
    font-weight: 600;
    box-shadow: 0 0 15px #00bcd4;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.5s ease;
    z-index: 1200;
  }
  #formFeedback.show {
    opacity: 1;
    pointer-events: auto;
  }
</style>
</head>
<body>

<!-- Açılış ekranı -->
<div id="splash">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
</div>

<!-- Navbar -->
<nav>
  <div class="logo">
    <img src="logo.png" alt="ZZONE99 Logo" />
    <h2>ZZONE99</h2>
  </div>
  <div class="menu-toggle" id="menuToggle">
    <span></span>
    <span></span>
    <span></span>
  </div>
  <ul class="nav-links" id="navLinks">
    <li><a href="#tanitim">Tanıtım</a></li>
    <li><a href="#basvuru">Klana Katıl</a></li>
    <li><a href="#iletisim">İletişim</a></li>
  </ul>
</nav>

<main>
  <!-- Tanıtım -->
  <section id="tanitim">
    <h3>TANITIM</h3>
    <p>
      PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </p>
  </section>

  <!-- Üyeler -->
  <section id="members">
    <div class="member-card">
      <img src="mazz.png" alt="mAzz99" />
      <h4>mAzz99</h4>
      <p><a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">@mAzz99theboss</a></p>
    </div>
    <div class="member-card">
      <img src="yazz.png" alt="yAzz99" />
      <h4>yAzz99</h4>
      <p><a href="https://www.tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a></p>
    </div>
  </section>

  <!-- Başvuru Butonu -->
  <div class="btn-container">
    <button class="btn" id="openFormBtn">KLANA KATIL</button>
  </div>

  <!-- İletişim -->
  <section id="iletisim">
    <h3>İletişim</h3>
    <p>TikTok Profilleri:</p>
    <ul>
      <li><a href="https://www.tiktok.com/@mAzz99theboss" target="_blank">mAzz99 (@mAzz99theboss)</a></li>
      <li><a href="https://www.tiktok.com/@babavizyondapm" target="_blank">yAzz99 (@babavizyondapm)</a></li>
    </ul>
  </section>
</main>

<!-- Başvuru Popup Form -->
<div id="popupForm">
  <span class="close-btn" id="closeFormBtn">&times;</span>
  <h3>Başvuru Formu</h3>
  <form id="applicationForm" method="POST" action="https://formspree.io/f/xldnljve">
    <label for="uid">UID - Oyun İsmi</label>
    <input type="text" id="uid" name="uid" required placeholder="Ör: 12345678 - PlayerName" />

    <label for="nameAge">İsim - Yaş</label>
    <input type="text" id="nameAge" name="nameAge" required placeholder="Ör: Ali - 22" />

    <label for="device">Kullandığı Cihaz</label>
    <select id="device" name="device" required>
      <option value="" disabled selected>Seçiniz</option>
      <option value="Android">Android</option>
      <option value="iOS">iOS</option>
      <option value="PC Emulator">PC Emulator</option>
      <option value="Diğer">Diğer</option>
    </select>

    <label for="activity">Aktiflik</label>
    <select id="activity" name="activity" required>
      <option value="" disabled selected>Seçiniz</option>
      <option value="Günlük">Günlük</option>
      <option value="Haftalık">Haftalık</option>
      <option value="Ara sıra">Ara sıra</option>
    </select>

    <button type="submit" class="submit-btn">Başvuruyu Gönder</button>
  </form>
</div>

<!-- Geri Bildirim -->
<div id="formFeedback"></div>

<script>
  // Splash Screen Kapanışı
  window.addEventListener('load', () => {
    setTimeout(() => {
      const splash = document.getElementById('splash');
      splash.style.opacity = '0';
      splash.style.pointerEvents = 'none';
    }, 2000);
  });

  // Menü Toggle (Mobil)
  const menuToggle = document.getElementById('menuToggle');
  const navLinks = document.getElementById('navLinks');
  menuToggle.addEventListener('click', () => {
    navLinks.classList.toggle('active');
  });

  // Popup Form Aç/Kapat
  const openFormBtn = document.getElementById('openFormBtn');
  const closeFormBtn = document.getElementById('closeFormBtn');
  const popupForm = document.getElementById('popupForm');

  openFormBtn.addEventListener('click', () => {
    popupForm.classList.add('active');
  });
  closeFormBtn.addEventListener('click', () => {
    popupForm.classList.remove('active');
  });

  // Form Gönderim İşlemi ve Geri Bildirim
  const applicationForm = document.getElementById('applicationForm');
  const formFeedback = document.getElementById('formFeedback');

  applicationForm.addEventListener('submit', (e) => {
    e.preventDefault();

    // Basit doğrulama (tüm required inputlar kontrolü)
    if(!applicationForm.checkValidity()) {
      applicationForm.reportValidity();
      return;
    }

    // Form verileri
    const formData = new FormData(applicationForm);

    // Formspree POST isteği (Fetch API)
    fetch(applicationForm.action, {
      method: 'POST',
      headers: { 'Accept': 'application/json' },
      body: formData
    }).then(response => {
      if (response.ok) {
        formFeedback.textContent = "Başvurunuz başarıyla alındı!";
        applicationForm.reset();
        popupForm.classList.remove('active');
      } else {
        formFeedback.textContent = "Bir hata oluştu, lütfen tekrar deneyiniz.";
      }
      formFeedback.classList.add('show');
      setTimeout(() => formFeedback.classList.remove('show'), 4000);
    }).catch(() => {
      formFeedback.textContent = "Bağlantı hatası. İnternet bağlantınızı kontrol edin.";
      formFeedback.classList.add('show');
      setTimeout(() => formFeedback.classList.remove('show'), 4000);
    });
  });

  // Sayfa Geçiş Animasyonu (smooth scroll)
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if(target) {
        target.scrollIntoView({ behavior: 'smooth' });
      }
      if(navLinks.classList.contains('active')) {
        navLinks.classList.remove('active');
      }
    });
  });
</script>

<footer style="text-align:center; padding:1rem; color:#00bcd4; font-weight:600;">
  <p>Für die Famiilla &nbsp; | &nbsp; SINCE 2018</p>
</footer>

</body>
