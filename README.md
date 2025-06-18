<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ZZONE99</title>
  <style>
    /* Reset ve temel */
    * {
      box-sizing: border-box;
      margin: 0; padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      color: #00fff7;
      user-select: none;
    }
    body {
      background: linear-gradient(135deg, #001f3f, #004d66);
      overflow-x: hidden;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 0 15px 50px;
    }
    a {
      color: #00fff7;
      text-decoration: none;
    }
    a:hover {
      color: #66fff7;
    }

    /* Loading Screen */
    #loading-screen {
      position: fixed;
      top: 0; left: 0; width: 100vw; height: 100vh;
      background-color: #001a33;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      user-select: none;
      transition: opacity 0.5s ease;
    }
    #loading-logo {
      width: 140px;
      animation: glow 2s infinite alternate;
    }
    #loading-text {
      font-size: 3.5rem;
      font-weight: 900;
      margin-top: 15px;
      text-shadow: 0 0 10px #00fff7;
      animation: glow 2s infinite alternate;
    }
    @keyframes glow {
      0% {
        filter: drop-shadow(0 0 5px #00fff7);
      }
      100% {
        filter: drop-shadow(0 0 20px #00fff7);
      }
    }

    /* Başlık ve açıklama */
    header {
      margin-top: 100px;
      text-align: center;
      max-width: 900px;
      user-select: text;
    }
    header h1 {
      font-size: 3.5rem;
      letter-spacing: 5px;
      font-weight: 900;
      text-shadow: 0 0 15px #00fff7;
      margin-bottom: 10px;
    }
    header p {
      font-size: 1.3rem;
      line-height: 1.6;
      color: #a0e9f8cc;
      font-weight: 600;
      user-select: text;
    }

    /* Liderler Bölümü */
    section.liderler {
      margin: 60px 0;
      width: 100%;
      max-width: 900px;
      text-align: center;
    }
    section.liderler h2 {
      font-size: 2.8rem;
      margin-bottom: 40px;
      text-shadow: 0 0 8px #00fff7;
      user-select: none;
    }
    .lider-container {
      display: flex;
      justify-content: center;
      gap: 60px;
      flex-wrap: wrap;
    }
    .lider {
      background: rgba(0, 255, 247, 0.1);
      border-radius: 15px;
      padding: 15px;
      width: 180px;
      box-shadow: 0 0 15px #00fff7cc;
      transition: transform 0.3s ease;
      cursor: default;
    }
    .lider:hover {
      transform: translateY(-10px);
      box-shadow: 0 0 30px #00fff7ff;
    }
    .lider img {
      width: 150px;
      height: auto;
      display: block;
      margin: 0 auto 10px;
      filter: drop-shadow(0 0 6px #00fff7);
      background: transparent;
      border-radius: 15px;
    }
    .lider .nick {
      font-size: 1.6rem;
      font-weight: 900;
      color: #00fff7;
      margin-bottom: 5px;
      text-shadow: 0 0 5px #00fff7;
    }
    .lider .id {
      font-size: 1.1rem;
      font-weight: 600;
      color: #66f7f7aa;
      user-select: text;
    }

    /* TikTok Linkler */
    .tiktok-links {
      margin-top: 25px;
      display: flex;
      justify-content: center;
      gap: 35px;
      user-select: none;
    }
    .tiktok-links a {
      display: inline-block;
      width: 45px;
      height: 45px;
      transition: transform 0.3s ease;
    }
    .tiktok-links a:hover {
      transform: scale(1.2);
    }
    .tiktok-links img {
      width: 100%;
      height: 100%;
      filter: drop-shadow(0 0 6px #00fff7);
    }

    /* Butonlar */
    .button-container {
      margin: 40px 0 30px;
      display: flex;
      justify-content: center;
      gap: 50px;
      user-select: none;
    }
    button {
      background: linear-gradient(135deg, #00f2ff, #00a6ff);
      border: none;
      padding: 15px 35px;
      border-radius: 50px;
      font-weight: 900;
      font-size: 1.3rem;
      color: #001f3f;
      cursor: pointer;
      box-shadow: 0 0 15px #00fff7;
      transition: all 0.3s ease;
      user-select: none;
    }
    button:hover {
      background: linear-gradient(135deg, #00a6ff, #00f2ff);
      box-shadow: 0 0 25px #00fff7;
      transform: scale(1.05);
    }
    button:focus {
      outline: none;
    }

    /* Başvuru Formu Popup */
    #popup-form {
      position: fixed;
      top: 50%; left: 50%;
      transform: translate(-50%, -50%) scale(0);
      background: #001f3fcc;
      padding: 30px 40px;
      border-radius: 20px;
      box-shadow: 0 0 40px #00fff7cc;
      z-index: 10000;
      transition: transform 0.4s ease;
      width: 90%;
      max-width: 420px;
    }
    #popup-form.active {
      transform: translate(-50%, -50%) scale(1);
    }
    #popup-form h3 {
      color: #00fff7;
      margin-bottom: 25px;
      text-align: center;
      font-weight: 900;
      text-shadow: 0 0 10px #00fff7;
    }
    #popup-form form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    #popup-form input, #popup-form select {
      padding: 12px 15px;
      border-radius: 10px;
      border: none;
      font-size: 1rem;
      font-weight: 600;
      user-select: text;
    }
    #popup-form input:focus, #popup-form select:focus {
      outline: none;
      box-shadow: 0 0 10px #00fff7;
    }
    #popup-form button {
      margin-top: 15px;
      background: #00fff7;
      color: #001f3f;
      font-weight: 900;
      font-size: 1.2rem;
      cursor: pointer;
      transition: background 0.3s ease;
      box-shadow: none;
      border-radius: 10px;
      padding: 12px 0;
      user-select: none;
    }
    #popup-form button:hover {
      background: #00b9c7;
    }

    /* Mesajlar */
    #form-message {
      margin-top: 15px;
      text-align: center;
      font-weight: 700;
      font-size: 1.1rem;
      color: #00fff7;
      text-shadow: 0 0 10px #00fff7;
      user-select: none;
    }
    #form-message.error {
      color: #ff4c4c;
      text-shadow: 0 0 10px #ff4c4c;
    }

    /* Ziyaretçi sayacı */
    #visitor-bar {
      position: fixed;
      bottom: 10px;
      left: 10px;
      width: 180px;
      height: 25px;
      border-radius: 50px;
      background: #00294d;
      box-shadow: 0 0 10px #00fff7cc inset;
      overflow: hidden;
      user-select: none;
      z-index: 999;
    }
    #visitor-bar-fill {
      height: 100%;
      width: 0%;
      background: #00fff7;
      border-radius: 50px;
      transition: width 0.5s ease;
    }
    #visitor-count {
      position: absolute;
      top: 2px;
      left: 50%;
      transform: translateX(-50%);
      font-weight: 900;
      font-size: 1rem;
      color: #001f3f;
      text-shadow: none;
      user-select: none;
    }

    /* Sayfa geçiş animasyonu */
    body.fade-out {
      opacity: 0;
      transition: opacity 0.5s ease;
    }

    /* Responsive */
    @media (max-width: 600px) {
      header h1 {
        font-size: 2.4rem;
      }
      header p {
        font-size: 1rem;
      }
      .lider-container {
        gap: 30px;
      }
      .lider {
        width: 140px;
        padding: 10px;
      }
      .lider img {
        width: 120px;
      }
      .button-container {
        flex-direction: column;
        gap: 25px;
      }
      button {
        width: 100%;
        max-width: 300px;
      }
      .tiktok-links {
        gap: 25px;
      }
    }
  </style>
</head>
<body>
  <!-- Loading Screen -->
  <div id="loading-screen">
    <img src="logo.png" alt="ZZONE99 Logo" id="loading-logo" />
    <h1 id="loading-text">ZZONE99</h1>
  </div>

  <!-- Header / Tanıtım -->
  <header>
    <h1>ZZONE99</h1>
    <p>İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,<br>
       bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.<br>
       Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmak.</p>
  </header>

  <!-- Liderler -->
  <section class="liderler">
    <h2>LİDERLER</h2>
    <div class="lider-container">
      <div class="lider">
        <img src="mazz.png" alt="mAzz99" />
        <div class="nick">mAzz99</div>
        <div class="id">516572604</div>
      </div>
      <div class="lider">
        <img src="yazz.png" alt="yAzz99" />
        <div class="nick">yAzz99</div>
        <div class="id">520654025</div>
      </div>
    </div>
    <div class="tiktok-links">
      <a href="https://www.tiktok.com/@mazz99theboss" target="_blank" rel="noopener noreferrer">
        <img src="tiktok-icon.png" alt="TikTok mAzz99" />
      </a>
      <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener noreferrer">
        <img src="tiktok-icon.png" alt="TikTok yAzz99" />
      </a>
    </div>
  </section>

  <!-- Butonlar -->
  <div class="button-container">
    <button id="openFormBtn">KLANA KATIL</button>
  </div>

  <!-- Başvuru Formu Popup -->
  <div id="popup-form">
    <h3>Klana Katıl Başvurusu</h3>
    <form id="application-form" action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="uid" placeholder="UID" required autocomplete="off" />
      <input type="text" name="oyun_ismi" placeholder="Oyun İsmi" required autocomplete="off" />
      <input type="text" name="isim" placeholder="İsim" required autocomplete="off" />
      <input type="number" name="yas" placeholder="Yaş" min="10" max="80" required autocomplete="off" />
      <select name="cihaz" required>
        <option value="" disabled selected>Cihaz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="Diğer">Diğer</option>
      </select>
      <select name="aktiflik" required>
        <option value="" disabled selected>Aktiflik</option>
        <option value="Haftada 7 Gün">Haftada 7 Gün</option>
        <option value="Haftada 4-6 Gün">Haftada 4-6 Gün</option>
        <option value="Haftada 1-3 Gün">Haftada 1-3 Gün</option>
      </select>
      <button type="submit">Başvuruyu Gönder</button>
    </form>
    <div id="form-message"></div>
  </div>

  <!-- Ziyaretçi sayacı -->
  <div id="visitor-bar">
    <div id="visitor-bar-fill"></div>
    <div id="visitor-count">0</div>
  </div>

  <script>
    // Loading ekranı 2 saniye sonra kaybolur
    window.addEventListener('load', () => {
      setTimeout(() => {
        const loadingScreen = document.getElementById('loading-screen');
        loadingScreen.style.opacity = '0';
        setTimeout(() => loadingScreen.style.display = 'none', 500);
      }, 2000);
    });

    // Pop-up form açma / kapama
    const openFormBtn = document.getElementById('openFormBtn');
    const popupForm = document.getElementById('popup-form');
    const formMessage = document.getElementById('form-message');

    openFormBtn.addEventListener('click', () => {
      popupForm.classList.add('active');
      formMessage.textContent = '';
      document.getElementById('application-form').reset();
    });

    // Form gönderimi (formspree)
    const applicationForm = document.getElementById('application-form');
    applicationForm.addEventListener('submit', (e) => {
      e.preventDefault();
      formMessage.textContent = 'Gönderiliyor...';

      const formData = new FormData(applicationForm);
      fetch(applicationForm.action, {
        method: 'POST',
        body: formData,
        headers: { 'Accept': 'application/json' }
      }).then(response => {
        if (response.ok) {
          formMessage.textContent = 'Başvurunuz alındı, teşekkürler!';
          applicationForm.reset();
          setTimeout(() => {
            popupForm.classList.remove('active');
            formMessage.textContent = '';
          }, 3000);
        } else {
          response.json().then(data => {
            formMessage.textContent = data.error || 'Başvuru gönderilirken hata oluştu.';
            formMessage.classList.add('error');
          });
        }
      }).catch(() => {
        formMessage.textContent = 'Başvuru gönderilirken hata oluştu.';
        formMessage.classList.add('error');
      });
    });

    // Basit ziyaretçi sayacı (localStorage ile)
    const visitorCountEl = document.getElementById('visitor-count');
    const visitorBarFill = document.getElementById('visitor-bar-fill');
    function updateVisitorCount() {
      let count = localStorage.getItem('zzone99_visitor_count');
      if (!count) {
        count = 1;
      } else {
        count = parseInt(count) + 1;
      }
      localStorage.setItem('zzone99_visitor_count', count);
      visitorCountEl.textContent = count;
      // Bar doluluk oranı max 1000 ziyaretçi varsayım
      let widthPercent = Math.min((count / 1000) * 100, 100);
      visitorBarFill.style.width = widthPercent + '%';
    }
    updateVisitorCount();

    // Sayfa geçiş animasyonu (basit fade)
    document.querySelectorAll('a').forEach(link => {
      if (link.href && link.target !== '_blank' && !link.href.includes('#')) {
        link.addEventListener('click', (e) => {
          e.preventDefault();
          document.body.classList.add('fade-out');
          setTimeout(() => {
            window.location.href = link.href;
          }, 500);
        });
      }
    });
  </script>
</body>

