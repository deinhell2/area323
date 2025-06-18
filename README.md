<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ZZONE99 PUBG Mobile Klanı</title>
  <meta name="description" content="PUBG Mobile sahnesinde 2018 yılından beri aktif olan ZZONE99 klanı. Kaliteli bir topluluk ve oyun başarısı için buradayız." />
  <meta property="og:title" content="ZZONE99 PUBG Mobile Klanı" />
  <meta property="og:description" content="PUBG Mobile sahnesinde 2018 yılından beri aktif olan ZZONE99 klanı. Kaliteli bir topluluk ve oyun başarısı için buradayız." />
  <meta property="og:image" content="logo.png" />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#007FFF" />

  <style>
    /* --- GENEL STİLLER --- */
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }
    body, html {
      margin: 0; padding: 0;
      font-family: 'Montserrat', sans-serif;
      background: linear-gradient(135deg, #00111f, #004080);
      color: #e0f7ff;
      min-height: 100vh;
      overflow-x: hidden;
    }
    a {
      color: #00cfff;
      text-decoration: none;
      transition: color 0.3s ease;
    }
    a:hover {
      color: #72e0ff;
    }

    /* --- LOADING SCREEN --- */
    #loadingScreen {
      position: fixed;
      inset: 0;
      background: linear-gradient(135deg, #00111f, #004080);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      animation: fadeOut 1s ease forwards;
      animation-delay: 2s;
    }
    #loadingScreen.fadeOut {
      opacity: 0;
      visibility: hidden;
      pointer-events: none;
    }
    #loadingScreen img {
      width: 120px;
      animation: logoPulse 2s ease-in-out infinite;
    }
    #loadingScreen h1 {
      font-size: 3rem;
      color: #00d4ff;
      text-shadow: 0 0 8px #00d4ff;
      margin: 1rem 0 0 0;
      letter-spacing: 6px;
      font-weight: 900;
      animation: textGlow 2s ease-in-out infinite;
    }
    @keyframes logoPulse {
      0%, 100% { transform: scale(1); filter: drop-shadow(0 0 10px #00d4ff);}
      50% { transform: scale(1.1); filter: drop-shadow(0 0 20px #00f0ff);}
    }
    @keyframes textGlow {
      0%, 100% { text-shadow: 0 0 5px #00cfff, 0 0 15px #00f0ff; }
      50% { text-shadow: 0 0 15px #00e5ff, 0 0 25px #00f0ff; }
    }
    @keyframes fadeOut {
      to {
        opacity: 0;
        visibility: hidden;
      }
    }

    /* --- FLOATING NAV --- */
    #floatingMenu {
      position: fixed;
      top: 20px;
      right: 20px;
      background: rgba(0, 132, 255, 0.8);
      border-radius: 50px;
      padding: 10px 20px;
      box-shadow: 0 0 15px #00cfff;
      z-index: 1000;
      display: flex;
      gap: 20px;
      font-weight: 700;
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s ease;
      user-select: none;
    }
    #floatingMenu a {
      color: #e0f7ff;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      cursor: pointer;
    }
    #floatingMenu a:hover {
      color: #00f7ff;
      text-shadow: 0 0 8px #00f7ff;
    }

    /* --- ANA KUTU --- */
    .container {
      max-width: 1080px;
      margin: 0 auto;
      padding: 2rem 1rem 4rem;
      text-align: center;
    }

    /* --- BANNER --- */
    #banner {
      margin-top: 1rem;
      margin-bottom: 3rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
    }
    #banner img {
      max-width: 140px;
      filter: drop-shadow(0 0 10px #00d4ff);
      animation: logoGlow 3s ease-in-out infinite alternate;
    }
    #banner h2 {
      font-size: 2.5rem;
      font-weight: 900;
      color: #00d4ff;
      text-shadow: 0 0 10px #00d4ff;
      letter-spacing: 0.2em;
      margin: 0;
      animation: textPulse 3s ease-in-out infinite alternate;
    }
    @keyframes logoGlow {
      from { filter: drop-shadow(0 0 10px #00d4ff);}
      to { filter: drop-shadow(0 0 25px #00ffff);}
    }
    @keyframes textPulse {
      from { text-shadow: 0 0 10px #00d4ff;}
      to { text-shadow: 0 0 20px #00ffff;}
    }

    /* --- TANITIM --- */
    #intro {
      font-size: 1.2rem;
      line-height: 1.5;
      color: #caf0f8;
      max-width: 900px;
      margin: 0 auto 4rem auto;
      text-align: center;
      font-weight: 500;
      opacity: 0;
      transform: translateY(40px);
      animation: fadeUp 1s ease forwards;
      animation-delay: 2.3s;
    }
    @keyframes fadeUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* --- LİDERLER --- */
    #leaders {
      display: flex;
      justify-content: center;
      gap: 4rem;
      margin-bottom: 4rem;
      opacity: 0;
      animation: fadeUp 1s ease forwards;
      animation-delay: 2.7s;
      flex-wrap: wrap;
    }
    .leader-card {
      background: rgba(0, 132, 255, 0.2);
      border-radius: 15px;
      padding: 1rem;
      width: 180px;
      color: #e0f7ff;
      box-shadow: 0 0 15px #00bfff;
      transition: transform 0.3s ease;
      cursor: default;
      user-select: none;
      text-align: center;
    }
    .leader-card:hover {
      transform: scale(1.07);
      box-shadow: 0 0 25px #00eaff;
    }
    .leader-card img {
      width: 130px;
      border-radius: 15px;
      margin-bottom: 1rem;
      filter: drop-shadow(0 0 8px #00d4ff);
      transition: filter 0.3s ease;
    }
    .leader-card img:hover {
      filter: drop-shadow(0 0 20px #00ffff);
    }
    .leader-card h3 {
      margin: 0 0 0.3rem;
      font-weight: 700;
      font-size: 1.3rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: #00cfff;
      text-shadow: 0 0 10px #00cfff;
    }
    .leader-card p {
      margin: 0;
      font-weight: 500;
      font-size: 0.9rem;
      letter-spacing: 0.05em;
      color: #b0e0ff;
    }

    /* --- BAŞVURU BUTONU --- */
    #applyBtn {
      background: #00cfff;
      color: #00111f;
      border: none;
      padding: 12px 25px;
      border-radius: 40px;
      font-weight: 700;
      font-size: 1.1rem;
      letter-spacing: 0.1em;
      cursor: pointer;
      box-shadow: 0 0 10px #00cfff;
      transition: background-color 0.3s ease, transform 0.2s ease;
      margin: 2rem auto 4rem;
      display: block;
    }
    #applyBtn:hover {
      background: #00e6ff;
      transform: scale(1.05);
      box-shadow: 0 0 20px #00e6ff;
    }

    /* --- BAŞVURU MODAL --- */
    #applyModal {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.8);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 10000;
    }
    #applyModal.active {
      display: flex;
    }
    #applyModal .modal-content {
      background: #002640;
      border-radius: 15px;
      padding: 2rem;
      width: 90%;
      max-width: 420px;
      box-shadow: 0 0 25px #00cfff;
      color: #caf0f8;
      position: relative;
    }
    #applyModal .modal-content h2 {
      margin-top: 0;
      margin-bottom: 1rem;
      text-align: center;
      color: #00d4ff;
      letter-spacing: 0.15em;
    }
    #applyModal label {
      display: block;
      margin-top: 1rem;
      font-weight: 600;
      color: #b0e0ff;
    }
    #applyModal input, #applyModal select {
      width: 100%;
      padding: 0.5rem;
      border-radius: 8px;
      border: none;
      margin-top: 0.3rem;
      font-size: 1rem;
      font-weight: 500;
      color: #00111f;
    }
    #applyModal button {
      margin-top: 1.5rem;
      width: 100%;
      padding: 12px 0;
      background: #00cfff;
      border: none;
      border-radius: 50px;
      font-weight: 700;
      font-size: 1.2rem;
      cursor: pointer;
      color: #00111f;
      transition: background-color 0.3s ease;
    }
    #applyModal button:hover {
      background: #00e6ff;
    }
    #applyModal .close-btn {
      position: absolute;
      top: 12px;
      right: 16px;
      font-size: 1.8rem;
      color: #00d4ff;
      cursor: pointer;
      font-weight: 700;
    }

    /* --- GERİ BİLDİRİM MESAJI --- */
    #feedbackMsg {
      margin-top: 1rem;
      text-align: center;
      font-weight: 700;
      font-size: 1.1rem;
      color: #00ffcc;
    }
    #feedbackMsg.error {
      color: #ff5555;
    }

    /* --- FOOTER --- */
    footer {
      text-align: center;
      color: #00aaff;
      padding: 1rem 1rem 2rem;
      font-weight: 600;
      letter-spacing: 0.15em;
      user-select: none;
      border-top: 1px solid #00cfff55;
    }
    footer span {
      display: block;
      margin-top: 0.3rem;
      font-size: 0.9rem;
      color: #0099ccaa;
      font-weight: 400;
      font-style: italic;
    }

    /* --- SCROLL ANİMASYONLARI --- */
    .fade-in {
      opacity: 0;
      transform: translateY(30px);
      transition: opacity 1s ease, transform 1s ease;
    }
    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* --- RESPONSIVE --- */
    @media (max-width: 768px) {
      #leaders {
        flex-direction: column;
        align-items: center;
        gap: 2rem;
      }
      #floatingMenu {
        flex-direction: column;
        padding: 10px;
        right: 10px;
        top: 10px;
        gap: 10px;
      }
      #applyBtn {
        width: 80%;
        font-size: 1rem;
        padding: 10px 15px;
      }
    }
  </style>
</head>
<body>

  <!-- LOADING SCREEN -->
  <div id="loadingScreen">
    <img src="logo.png" alt="ZZONE99 Logo" />
    <h1>ZZONE99</h1>
  </div>

  <!-- FLOATING MENU -->
  <div id="floatingMenu">
    <a href="#intro">Tanıtım</a>
    <a href="#leaders">Liderler</a>
    <a href="#" id="openApply">Klana Katıl</a>
  </div>

  <!-- ANA CONTAINER -->
  <div class="container">

    <!-- BANNER -->
    <section id="banner">
      <img src="logo.png" alt="ZZONE99 Logo" />
      <h2>ZZONE99</h2>
    </section>

    <!-- TANITIM -->
    <section id="intro" class="fade-in">
      PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </section>

    <!-- LIDERLER -->
    <section id="leaders" class="fade-in">
      <div class="leader-card">
        <img src="mazz.png" alt="mAzz99" />
        <h3>mAzz99</h3>
        <p>ID: 516572604</p>
      </div>
      <div class="leader-card">
        <img src="yazz.png" alt="yAzz99" />
        <h3>yAzz99</h3>
        <p>ID: 520654025</p>
      </div>
    </section>

    <!-- BASVURU BUTONU -->
    <button id="applyBtn">Klana Katıl</button>

  </div>

  <!-- BASVURU MODAL -->
  <div id="applyModal">
    <div class="modal-content">
      <span class="close-btn" id="closeApply">&times;</span>
      <h2>Başvuru Formu</h2>
      <form id="applyForm" action="https://formspree.io/f/xldnljve" method="POST" novalidate>
        <label for="uid">UID - Oyun İsmi</label>
        <input type="text" id="uid" name="UID-Oyun İsmi" placeholder="UID ve Oyun İsmi" required />
        <label for="name">İsim</label>
        <input type="text" id="name" name="İsim" placeholder="Adınız" required />
        <label for="age">Yaş</label>
        <input type="number" id="age" name="Yaş" min="12" max="99" placeholder="Yaşınız" required />
        <label for="device">Cihaz</label>
        <select id="device" name="Cihaz" required>
          <option value="" disabled selected>Cihaz Seçiniz</option>
          <option value="Android">Android</option>
          <option value="iOS">iOS</option>
          <option value="Emulator">Emülatör</option>
          <option value="Diğer">Diğer</option>
        </select>
        <label for="activity">Aktiflik (günlük saat)</label>
        <input type="number" id="activity" name="Aktiflik" min="0" max="24" placeholder="Günde kaç saat aktif?" required />
        <button type="submit">Başvur</button>
        <p id="feedbackMsg"></p>
      </form>
    </div>
  </div>

  <!-- FOOTER -->
  <footer>
    Für die Famiilla<br/>
    <span>SINCE 2018</span>
  </footer>

  <script>
    // LOADING SCREEN KAYBOLMASI
    window.addEventListener('load', () => {
      const loadingScreen = document.getElementById('loadingScreen');
      loadingScreen.classList.add('fadeOut');
      setTimeout(() => loadingScreen.style.display = 'none', 1000);
    });

    // APPLY MODAL AÇMA/KAPAMA
    const openApply = document.getElementById('openApply');
    const applyBtn = document.getElementById('applyBtn');
    const applyModal = document.getElementById('applyModal');
    const closeApply = document.getElementById('closeApply');

    function openModal() {
      applyModal.classList.add('active');
    }
    function closeModal() {
      applyModal.classList.remove('active');
      clearFeedback();
      applyForm.reset();
    }

    openApply.addEventListener('click', (e) => {
      e.preventDefault();
      openModal();
    });
    applyBtn.addEventListener('click', openModal);
    closeApply.addEventListener('click', closeModal);
    applyModal.addEventListener('click', (e) => {
      if (e.target === applyModal) closeModal();
    });

    // FORM VALIDATION VE FORM SUBMIT
    const applyForm = document.getElementById('applyForm');
    const feedbackMsg = document.getElementById('feedbackMsg');

    function clearFeedback() {
      feedbackMsg.textContent = '';
      feedbackMsg.classList.remove('error');
    }

    applyForm.addEventListener('submit', (e) => {
      e.preventDefault();
      clearFeedback();

      // Basit validasyon
      if (!applyForm.checkValidity()) {
        feedbackMsg.textContent = 'Lütfen tüm alanları doğru şekilde doldurunuz.';
        feedbackMsg.classList.add('error');
        return;
      }

      // Submit Formspree'e fetch ile
      fetch(applyForm.action, {
        method: 'POST',
        headers: { 'Accept': 'application/json' },
        body: new FormData(applyForm)
      }).then(response => {
        if (response.ok) {
          feedbackMsg.textContent = 'Başvurunuz başarıyla alındı, teşekkürler!';
          feedbackMsg.classList.remove('error');
          applyForm.reset();
          setTimeout(closeModal, 3000);
        } else {
          response.json().then(data => {
            if (Object.hasOwn(data, 'errors')) {
              feedbackMsg.textContent = data["errors"].map(error => error["message"]).join(", ");
            } else {
              feedbackMsg.textContent = 'Bir hata oluştu. Lütfen tekrar deneyiniz.';
            }
            feedbackMsg.classList.add('error');
          });
        }
      }).catch(() => {
        feedbackMsg.textContent = 'Sunucuya ulaşılamıyor. İnternet bağlantınızı kontrol edin.';
        feedbackMsg.classList.add('error');
      });
    });

    // SAYFA KAYDIRMA EFECTİ (fade-in)
    const faders = document.querySelectorAll('.fade-in');
    const appearOptions = { threshold: 0, rootMargin: "0px 0px -100px 0px" };
    const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll) {
      entries.forEach(entry => {
        if (!entry.isIntersecting) return;
        entry.target.classList.add('visible');
        appearOnScroll.unobserve(entry.target);
      });
    }, appearOptions);
    faders.forEach(fader => appearOnScroll.observe(fader));

  </script>

</body>
