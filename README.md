<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99 - PUBG Mobile Klanı</title>
<meta name="description" content="ZZONE99, 2018’den beri PUBG Mobile arenasında dostluk ve başarıyla yoluna devam eden köklü bir klan." />
<style>
  /* --- Temel Reset & Font --- */
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');
  * {
    margin:0; padding:0; box-sizing:border-box;
    font-family: 'Poppins', sans-serif;
  }
  body {
    background: #0a111f;
    color: #a0f0f8;
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
  }
  a {
    color: #5bf0e0;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  a:hover {
    color: #00fff7;
  }

  /* --- RGB Arkaplan animasyonu --- */
  #rgbGlow {
    position: fixed;
    top:0; left:0; width:100%; height:100%;
    pointer-events:none;
    background:
      radial-gradient(circle at 30% 30%, rgba(0,255,255,0.25), transparent 40%),
      radial-gradient(circle at 70% 70%, rgba(0,191,255,0.25), transparent 40%);
    animation: glowPulse 5s ease-in-out infinite;
    z-index: -1;
  }
  @keyframes glowPulse {
    0%,100% {opacity:0.15;}
    50% {opacity:0.05;}
  }

  /* --- Container --- */
  .container {
    max-width: 900px;
    margin: auto;
    padding: 30px 20px;
  }

  /* --- Giriş Ekranı (Overlay) --- */
  #entryScreen {
    position: fixed;
    top:0; left:0; width:100%; height:100vh;
    background: #05111f;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 9999;
    animation: fadeInOut 4s forwards;
  }
  #entryScreen img {
    width: 120px;
    height: auto;
    filter: drop-shadow(0 0 8px #00fff7);
    animation: logoPulse 4s ease-in-out infinite;
  }
  #entryScreen h1 {
    margin-top: 20px;
    font-size: 3rem;
    font-weight: 900;
    color: #00fff7;
    text-shadow:
      0 0 10px #00fff7,
      0 0 20px #00fff7,
      0 0 30px #00fff7;
    animation: glowText 4s ease-in-out infinite;
  }

  @keyframes fadeInOut {
    0% {opacity:0;}
    10% {opacity:1;}
    90% {opacity:1;}
    100% {opacity:0; pointer-events:none;}
  }
  @keyframes logoPulse {
    0%, 100% {filter: drop-shadow(0 0 8px #00fff7);}
    50% {filter: drop-shadow(0 0 18px #00fff7);}
  }
  @keyframes glowText {
    0%, 100% {
      text-shadow:
        0 0 10px #00fff7,
        0 0 20px #00fff7,
        0 0 30px #00fff7;
    }
    50% {
      text-shadow:
        0 0 15px #00fff7,
        0 0 30px #00fff7,
        0 0 40px #00fff7;
    }
  }

  /* --- Başlık & Açıklama --- */
  header {
    text-align: center;
    margin-bottom: 40px;
  }
  header img.logo-main {
    width: 100px;
    filter: drop-shadow(0 0 5px #00fff7);
    margin-bottom: 15px;
  }
  header h2 {
    font-size: 2.2rem;
    font-weight: 700;
    color: #00f0ff;
    margin-bottom: 15px;
    text-shadow: 0 0 8px #00fff7;
  }
  header p.description {
    max-width: 600px;
    margin: 0 auto;
    font-size: 1.05rem;
    line-height: 1.5;
    color: #c4f6fa;
  }

  /* --- Nick & Logo Bölümü --- */
  .members {
    display: flex;
    justify-content: center;
    gap: 60px;
    margin: 50px 0 70px 0;
    flex-wrap: wrap;
  }
  .member-card {
    background: rgba(0,255,255,0.07);
    border-radius: 16px;
    padding: 20px 25px;
    width: 140px;
    text-align: center;
    box-shadow:
      0 0 10px #00fff7,
      inset 0 0 6px #00fff7;
    transition: box-shadow 0.3s ease;
  }
  .member-card:hover {
    box-shadow:
      0 0 20px #00fff7,
      inset 0 0 12px #00fff7;
  }
  .member-card img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: contain;
    filter: drop-shadow(0 0 5px #00fff7);
  }
  .member-nick {
    margin-top: 12px;
    font-weight: 900;
    font-size: 1.3rem;
    color: #00fff7;
    text-shadow:
      0 0 6px #00fff7,
      0 0 12px #00fff7;
  }

  /* --- Klan'a Katıl Buton ve Popup Form --- */
  #btnBasvuru {
    display: block;
    margin: 0 auto 50px auto;
    padding: 15px 40px;
    font-size: 1.3rem;
    background: #00d5ff;
    color: #01131a;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    font-weight: 700;
    box-shadow: 0 0 15px #00d5ff;
    transition: background 0.3s ease, box-shadow 0.3s ease;
  }
  #btnBasvuru:hover {
    background: #00fff7;
    box-shadow: 0 0 30px #00fff7;
  }

  /* Popup form kaplama */
  #popupFormWrapper {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    background: rgba(0, 0, 0, 0.7);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 10000;
  }
  #popupFormWrapper.active {
    display: flex;
  }

  /* Popup form kutusu */
  #popupForm {
    background: #01131a;
    padding: 30px 35px;
    border-radius: 20px;
    width: 90%;
    max-width: 420px;
    box-shadow: 0 0 30px #00fff7;
    position: relative;
  }
  #popupForm h3 {
    margin-bottom: 20px;
    color: #00fff7;
    text-align: center;
    font-weight: 700;
  }
  #popupForm label {
    display: block;
    font-weight: 600;
    margin-bottom: 6px;
    color: #8ef2ff;
  }
  #popupForm input,
  #popupForm select,
  #popupForm textarea {
    width: 100%;
    padding: 10px 12px;
    margin-bottom: 18px;
    border-radius: 10px;
    border: none;
    font-size: 1rem;
    font-family: 'Poppins', sans-serif;
  }
  #popupForm textarea {
    resize: vertical;
  }
  #popupForm button[type="submit"] {
    width: 100%;
    padding: 15px;
    background: #00fff7;
    color: #01131a;
    font-weight: 800;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    font-size: 1.1rem;
    transition: background 0.3s ease;
  }
  #popupForm button[type="submit"]:hover {
    background: #00d5ff;
  }
  /* Kapat butonu */
  #closePopup {
    position: absolute;
    top: 12px;
    right: 15px;
    font-size: 1.8rem;
    color: #00fff7;
    cursor: pointer;
    user-select: none;
  }

  /* Form durum mesajı */
  #formStatus {
    text-align: center;
    margin-top: 15px;
    font-weight: 700;
  }
  #formStatus.success {
    color: #32d632;
  }
  #formStatus.error {
    color: #f54343;
  }

  /* --- Tiktok Pop-up --- */
  #tiktokPopup {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: #01131a;
    padding: 12px 20px;
    border-radius: 40px;
    box-shadow: 0 0 20px #00fff7;
    display: flex;
    gap: 12px;
    align-items: center;
    cursor: pointer;
    color: #00fff7;
    font-weight: 700;
    user-select: none;
    z-index: 9999;
  }
  #tiktokPopup:hover {
    background: #00fff7;
    color: #01131a;
    box-shadow: 0 0 40px #00fff7;
  }
  #tiktokPopup svg {
    width: 24px;
    height: 24px;
    fill: currentColor;
  }

  /* --- Tanıtım bölümü (açıklama) --- */
  #tanitim {
    max-width: 700px;
    margin: 0 auto 60px auto;
    font-size: 1.1rem;
    line-height: 1.5;
    color: #aafcff;
  }

  /* --- Sayfa Geçiş Animasyonu --- */
  main {
    opacity: 0;
    animation: fadeInPage 1.2s forwards;
  }
  @keyframes fadeInPage {
    to {opacity: 1;}
  }

  /* --- Responsive --- */
  @media(max-width:600px) {
    header h2 {
      font-size: 1.8rem;
    }
    .members {
      gap: 30px;
    }
    .member-card {
      width: 120px;
      padding: 15px 18px;
    }
    .member-card img {
      width: 80px;
      height: 80px;
    }
    #btnBasvuru {
      width: 90%;
      font-size: 1.1rem;
      padding: 12px 0;
    }
  }
</style>
</head>
<body>

<div id="rgbGlow"></div>

<!-- Giriş Ekranı -->
<div id="entryScreen" aria-label="Giriş Ekranı">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
</div>

<div class="container" role="main">

  <!-- Başlık ve Açıklama -->
  <header>
    <img src="logo.png" alt="ZZONE99 Logo" class="logo-main" />
    <h2>ZZONE99 PUBG Mobile Klanı</h2>
  </header>

  <!-- Tanıtım Açıklaması -->
  <section id="tanitim" aria-label="Klan Tanıtımı">
    <p>
      PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş, 
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </p>
  </section>

  <!-- Üyeler Bölümü -->
  <section class="members" aria-label="Klan Üyeleri">
    <div class="member-card" tabindex="0">
      <img src="mazz.png" alt="mAzz99 Logo" />
      <div class="member-nick">mAzz99</div>
    </div>
    <div class="member-card" tabindex="0">
      <img src="yazz.png" alt="yAzz99 Logo" />
      <div class="member-nick">yAzz99</div>
    </div>
  </section>

  <!-- Klan'a Katıl Butonu -->
  <button id="btnBasvuru" aria-haspopup="dialog" aria-controls="popupFormWrapper" aria-expanded="false">KLANA KATIL</button>

  <!-- Başvuru Formu Popup -->
  <div id="popupFormWrapper" role="dialog" aria-modal="true" aria-labelledby="popupTitle" tabindex="-1">
    <form id="popupForm" action="https://formspree.io/f/xldnljve" method="POST" novalidate>
      <button id="closePopup" aria-label="Formu Kapat">&times;</button>
      <h3 id="popupTitle">Klan Başvuru Formu</h3>

      <label for="uid">UID (Oyuncu Kimliği):</label>
      <input type="text" id="uid" name="UID" required placeholder="Örn: 123456789" />

      <label for="oyunIsmi">Oyun İsim:</label>
      <input type="text" id="oyunIsmi" name="OyunIsmi" required placeholder="Oyundaki isminiz" />

      <label for="isim">Adınız:</label>
      <input type="text" id="isim" name="Isim" required placeholder="Gerçek adınız" />

      <label for="yas">Yaşınız:</label>
      <input type="number" id="yas" name="Yas" min="13" max="99" required />

      <label for="cihaz">Kullandığınız Cihaz:</label>
      <select id="cihaz" name="Cihaz" required>
        <option value="" disabled selected>Cihazınızı seçin</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="Emulator">Emulator</option>
        <option value="Diğer">Diğer</option>
      </select>

      <label for="aktiflik">Aktiflik Durumu:</label>
      <textarea id="aktiflik" name="Aktiflik" rows="3" placeholder="Klan için aktiflik durumunuz ve diğer bilgiler"></textarea>

      <button type="submit">Başvuruyu Gönder</button>

      <div id="formStatus" role="alert" aria-live="polite"></div>
    </form>
  </div>

</div>

<!-- Tiktok Popup -->
<div id="tiktokPopup" tabindex="0" role="button" aria-label="TikTok Hesapları">
  <svg viewBox="0 0 24 24"><path d="M9 3a7.5 7.5 0 0 0 7.52 7.5v4.5a4.5 4.5 0 1 1-4.5-4.5V3Z"/></svg>
  <span>@mAzz99theboss</span>
  <span>|</span>
  <span>@babavizyondapm</span>
</div>

<!-- Footer -->
<footer style="text-align:center; margin: 50px 0 30px 0; color:#0097a7; font-weight:600; font-size:1rem; user-select:none;">
  Für die Famiilla &nbsp;&nbsp;|&nbsp;&nbsp; SINCE 2018
</footer>

<script>
  // Entry Screen gizleme (4 saniye sonra)
  window.addEventListener('load', () => {
    setTimeout(() => {
      const entry = document.getElementById('entryScreen');
      entry.style.display = 'none';
    }, 4000);
  });

  // Popup form aç/kapa
  const btnBasvuru = document.getElementById('btnBasvuru');
  const popupWrapper = document.getElementById('popupFormWrapper');
  const closePopupBtn = document.getElementById('closePopup');
  const formStatus = document.getElementById('formStatus');
  const popupForm = document.getElementById('popupForm');

  btnBasvuru.addEventListener('click', () => {
    popupWrapper.classList.add('active');
    btnBasvuru.setAttribute('aria-expanded', 'true');
    popupWrapper.focus();
  });

  closePopupBtn.addEventListener('click', () => {
    popupWrapper.classList.remove('active');
    btnBasvuru.setAttribute('aria-expanded', 'false');
  });

  // Form gönderimi - Formspree entegrasyonu ve geri bildirim
  popupForm.addEventListener('submit', async (e) => {
    e.preventDefault();
    formStatus.textContent = 'Başvurunuz gönderiliyor...';
    formStatus.className = '';

    const formData = new FormData(popupForm);
    try {
      const response = await fetch(popupForm.action, {
        method: 'POST',
        headers: { 'Accept': 'application/json' },
        body: formData,
      });
      if (response.ok) {
        formStatus.textContent = 'Başvurunuz başarıyla gönderildi. Teşekkürler!';
        formStatus.className = 'success';
        popupForm.reset();
      } else {
        throw new Error('Gönderim başarısız oldu.');
      }
    } catch (error) {
      formStatus.textContent = 'Başvuru gönderilirken hata oluştu, lütfen tekrar deneyin.';
      formStatus.className = 'error';
    }
  });

  // Tiktok Popup tıklama ile link açma
  const tiktokPopup = document.getElementById('tiktokPopup');
  tiktokPopup.addEventListener('click', () => {
    window.open('https://www.tiktok.com/@mazz99theboss', '_blank');
  });
  tiktokPopup.addEventListener('keypress', e => {
    if (e.key === 'Enter' || e.key === ' ') {
      window.open('https://www.tiktok.com/@mazz99theboss', '_blank');
    }
  });

  // Ziyaretçi sayacı - basit localStorage ile
  const visitorCountKey = 'zzone99_visitorCount';
  let count = localStorage.getItem(visitorCountKey);
  if (!count) {
    count = 1;
  } else {
    count = parseInt(count) + 1;
  }
  localStorage.setItem(visitorCountKey, count);
  // Footer altına göster
  const footer = document.querySelector('footer');
  const counterEl = document.createElement('div');
  counterEl.textContent = `Bugün Ziyaretçi: ${count}`;
  counterEl.style.color = '#00fff7';
  counterEl.style.marginTop = '8px';
  footer.appendChild(counterEl);
</script>

</body>
