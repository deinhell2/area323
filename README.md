<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ZZONE99 - PUBG Mobile Klan</title>
  <meta name="description" content="ZZONE99 PUBG Mobile Klan - Since 2018. Kaliteli topluluk, güçlü vizyon." />
  <meta name="keywords" content="PUBG Mobile, Klan, ZZONE99, mAzz99, yAzz99" />
  <meta name="author" content="ZZONE99" />
  <style>
    /* Reset */
    * {
      margin: 0; padding: 0; box-sizing: border-box;
    }
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0b0e14, #051219);
      color: #a3f7f9;
      min-height: 100vh;
      overflow-x: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      transition: background 0.7s ease;
    }

    /* Giriş banner */
    #banner {
      margin-top: 50px;
      text-align: center;
      animation: fadeInDown 1.8s ease forwards;
      opacity: 0;
    }
    #banner img {
      width: 140px;
      height: auto;
      animation: pulse 3s infinite ease-in-out;
      filter: drop-shadow(0 0 10px #00fff3);
      display: block;
      margin: 0 auto;
    }
    #banner h1 {
      font-size: 3.2rem;
      margin-top: 20px;
      background: linear-gradient(90deg, #00f2ff, #00ffe0, #00f2ff);
      background-size: 300% 300%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: rgbFlow 5s infinite;
      font-weight: 900;
    }

    /* Tanıtım kısmı */
    #tanitim {
      max-width: 720px;
      margin: 40px 20px 20px 20px;
      font-size: 1.1rem;
      line-height: 1.6;
      color: #a3f7f9cc;
      text-align: center;
      animation: fadeInUp 2s ease forwards;
      opacity: 0;
    }

    /* Karakter logoları ve nickler */
    #uyeler {
      margin-top: 35px;
      display: flex;
      justify-content: center;
      gap: 50px;
      animation: fadeInUp 2.5s ease forwards;
      opacity: 0;
    }
    .uye-kart {
      text-align: center;
      color: #00f0ff;
      user-select: none;
    }
    .uye-kart img {
      width: 130px;
      height: auto;
      border-radius: 12px;
      filter: drop-shadow(0 0 10px #00fff3);
      transition: transform 0.3s ease;
      cursor: default;
    }
    .uye-kart:hover img {
      transform: scale(1.07);
      filter: drop-shadow(0 0 20px #00fff3);
    }
    .uye-kart .nick {
      margin-top: 10px;
      font-weight: 700;
      font-size: 1.3rem;
      letter-spacing: 1.5px;
      background: linear-gradient(90deg, #00eaff, #00ffc8);
      background-clip: text;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      user-select: text;
    }

    /* Butonlar */
    button {
      cursor: pointer;
      border: none;
      padding: 14px 28px;
      font-size: 1.1rem;
      font-weight: 700;
      border-radius: 30px;
      background: linear-gradient(90deg, #00eaff, #00ffc8);
      color: #051219;
      margin: 30px 15px 15px 15px;
      transition: background 0.4s ease, transform 0.3s ease;
      box-shadow: 0 4px 10px rgba(0, 255, 255, 0.35);
      user-select: none;
    }
    button:hover {
      background: linear-gradient(90deg, #00ffc8, #00eaff);
      transform: scale(1.05);
      box-shadow: 0 8px 18px rgba(0, 255, 255, 0.65);
    }

    /* Form Popup */
    #popupForm {
      position: fixed;
      top: 50%; left: 50%;
      transform: translate(-50%, -50%) scale(0);
      background: #051219cc;
      border-radius: 15px;
      padding: 30px 35px;
      box-shadow: 0 0 30px #00ffe0aa;
      max-width: 400px;
      width: 90%;
      transition: transform 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
      z-index: 1500;
      color: #a3f7f9;
    }
    #popupForm.active {
      transform: translate(-50%, -50%) scale(1);
    }
    #popupForm h2 {
      text-align: center;
      margin-bottom: 20px;
      font-weight: 900;
      letter-spacing: 1.2px;
      color: #00fff3;
    }
    #popupForm label {
      display: block;
      margin: 10px 0 6px 0;
      font-weight: 700;
    }
    #popupForm input, #popupForm select {
      width: 100%;
      padding: 10px;
      border-radius: 10px;
      border: none;
      outline: none;
      font-size: 1rem;
      margin-bottom: 15px;
      background-color: #051219;
      color: #a3f7f9;
      box-shadow: inset 0 0 10px #00ffe0cc;
      transition: box-shadow 0.3s ease;
    }
    #popupForm input:focus, #popupForm select:focus {
      box-shadow: 0 0 15px #00fff3;
    }
    #popupForm button {
      width: 100%;
      background: #00f2ff;
      color: #051219;
      font-weight: 900;
      font-size: 1.2rem;
      padding: 14px;
      margin-top: 10px;
      box-shadow: 0 0 20px #00f2ff;
    }
    #popupForm button:hover {
      background: #00d2cc;
      box-shadow: 0 0 30px #00d2cc;
    }
    #closeBtn {
      position: absolute;
      top: 10px; right: 15px;
      font-size: 1.5rem;
      font-weight: 900;
      color: #00f2ff;
      cursor: pointer;
      user-select: none;
    }
    #formStatus {
      text-align: center;
      margin-top: 15px;
      font-weight: 700;
      min-height: 24px;
    }

    /* İletişim TikTok */
    #iletisim {
      margin: 40px 0 25px 0;
      text-align: center;
    }
    #iletisim h3 {
      color: #00eaff;
      font-weight: 800;
      margin-bottom: 20px;
    }
    .tiktok-links {
      display: inline-flex;
      gap: 24px;
      justify-content: center;
      cursor: pointer;
    }
    .tiktok-links div {
      background: #00f2ff;
      width: 48px; height: 48px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 0 10px #00fff3;
      transition: box-shadow 0.3s ease;
      position: relative;
    }
    .tiktok-links div:hover {
      box-shadow: 0 0 20px #00fff3;
    }
    .tiktok-links svg {
      fill: #051219;
      width: 26px; height: 26px;
    }
    /* Tooltip */
    .tooltip {
      position: absolute;
      bottom: 60px;
      background: #00f2ffdd;
      color: #051219;
      padding: 6px 12px;
      border-radius: 12px;
      font-weight: 700;
      font-size: 0.85rem;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s ease;
      white-space: nowrap;
      user-select: none;
    }
    .tiktok-links div:hover .tooltip {
      opacity: 1;
      pointer-events: auto;
    }

    /* Ziyaretçi sayacı */
    #ziyaretciSayaci {
      width: 90%;
      max-width: 720px;
      height: 18px;
      background: #051219;
      border-radius: 10px;
      box-shadow: inset 0 0 10px #00eaff77;
      margin-bottom: 30px;
      position: relative;
      overflow: hidden;
      user-select: none;
    }
    #ziyaretciBar {
      background: linear-gradient(90deg, #00f2ff, #00d8ff);
      height: 100%;
      width: 0%;
      border-radius: 10px;
      transition: width 0.8s ease;
      box-shadow: 0 0 8px #00f2ffcc;
    }
    #ziyaretciText {
      position: absolute;
      width: 100%;
      text-align: center;
      font-weight: 700;
      font-size: 0.85rem;
      color: #a3f7f9cc;
      user-select: none;
      line-height: 18px;
    }

    /* Kapanış */
    footer {
      margin: 50px 0 30px 0;
      text-align: center;
      font-size: 0.95rem;
      font-weight: 700;
      color: #008ba3cc;
      letter-spacing: 1.3px;
      user-select: none;
    }
    footer span {
      display: block;
      margin-top: 6px;
      font-weight: 600;
      font-size: 0.75rem;
      color: #00505a99;
    }

    /* Animasyonlar */
    @keyframes rgbFlow {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }
    @keyframes pulse {
      0%, 100% {
        transform: scale(1);
        filter: drop-shadow(0 0 10px #00f0ffaa);
      }
      50% {
        transform: scale(1.05);
        filter: drop-shadow(0 0 22px #00f0ffcc);
      }
    }
    @keyframes fadeInDown {
      0% {
        opacity: 0;
        transform: translateY(-60px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(30px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }
  </style>
</head>
<body>

  <!-- Açılış Banner -->
  <section id="banner" aria-label="Site Açılış Bannerı">
    <img src="logo.png" alt="ZZONE99 Logo" />
    <h1>ZZONE99</h1>
  </section>

  <!-- Tanıtım -->
  <section id="tanitim" aria-label="Klan Tanıtımı">
    <p>
      TANITIM : PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.<br />
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,<br />
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.<br />
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </p>
  </section>

  <!-- Üyeler Bölümü -->
  <section id="uyeler" aria-label="Klan Üyeleri">
    <div class="uye-kart">
      <img src="mazz.png" alt="mAzz99 Logo" />
      <div class="nick">mAzz99</div>
    </div>
    <div class="uye-kart">
      <img src="yazz.png" alt="yAzz99 Logo" />
      <div class="nick">yAzz99</div>
    </div>
  </section>

  <!-- Butonlar -->
  <div>
    <button id="btnBasvuru" aria-haspopup="dialog" aria-controls="popupForm" aria-expanded="false">
      KLANA KATIL
    </button>
    <button id="btnIletisim">
      İLETİŞİM
    </button>
  </div>

  <!-- Başvuru Popup -->
  <section id="popupForm" role="dialog" aria-modal="true" aria-labelledby="popupTitle" aria-describedby="popupDesc">
    <span id="closeBtn" tabindex="0" role="button" aria-label="Formu Kapat">&times;</span>
    <h2 id="popupTitle">Klan Başvuru Formu</h2>
    <form id="basvuruForm" action="https://formspree.io/f/xldnljve" method="POST">
      <label for="uid">UID - Oyun İsmi</label>
      <input type="text" id="uid" name="UID-OYUN-ISMI" placeholder="UID ve Oyun İsminiz" required />

      <label for="isim">İsim - Yaş</label>
      <input type="text" id="isim" name="ISIM-YAS" placeholder="Adınız ve Yaşınız" required />

      <label for="cihaz">Kullandığı Cihaz</label>
      <select id="cihaz" name="CIHAZ" required>
        <option value="" disabled selected>Cihaz Seçiniz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="Diğer">Diğer</option>
      </select>

      <label for="aktiflik">Aktiflik Durumu</label>
      <select id="aktiflik" name="AKTIFLIK" required>
        <option value="" disabled selected>Aktiflik Durumu</option>
        <option value="Haftada 1-2 Gün">Haftada 1-2 Gün</option>
        <option value="Haftada 3-5 Gün">Haftada 3-5 Gün</option>
        <option value="Her Gün">Her Gün</option>
        <option value="Nadir">Nadir</option>
      </select>

      <button type="submit">Başvuruyu Gönder</button>
      <div id="formStatus" aria-live="polite" role="status"></div>
    </form>
  </section>

  <!-- İletişim Bölümü -->
  <section id="iletisim" aria-label="İletişim Bilgileri">
    <h3>İletişim</h3>
    <div class="tiktok-links" aria-label="TikTok Linkleri">
      <div tabindex="0" role="button" aria-describedby="tipMazz" onclick="window.open('https://www.tiktok.com/@mazz99theboss', '_blank')">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <path d="M9.578 7.95v8.748c0 2.99-2.427 5.418-5.42 5.418S-1.263 19.688-1.263 16.698s2.427-5.418 5.42-5.418c.94 0 1.813.326 2.487.87v-3.6l2.176.04z"/>
        </svg>
        <span class="tooltip" id="tipMazz">@mazz99theboss</span>
      </div>
      <div tabindex="0" role="button" aria-describedby="tipYazz" onclick="window.open('https://www.tiktok.com/@babavizyondapm', '_blank')">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <path d="M9.578 7.95v8.748c0 2.99-2.427 5.418-5.42 5.418S-1.263 19.688-1.263 16.698s2.427-5.418 5.42-5.418c.94 0 1.813.326 2.487.87v-3.6l2.176.04z"/>
        </svg>
        <span class="tooltip" id="tipYazz">@babavizyondapm</span>
      </div>
    </div>
  </section>

  <!-- Ziyaretçi Sayacı -->
  <div id="ziyaretciSayaci" aria-label="Bugünkü ziyaretçi sayacı">
    <div id="ziyaretciBar"></div>
    <div id="ziyaretciText">Bugün: 0 ziyaretçi</div>
  </div>

  <!-- Footer -->
  <footer>
    Für die Famiilla <span>SINCE 2018</span>
  </footer>

  <script>
    // Sayfa geçiş animasyonu (basit fade in/out)
    document.body.style.opacity = 0;
    window.addEventListener('DOMContentLoaded', () => {
      let body = document.body;
      body.style.transition = "opacity 0.7s ease";
      body.style.opacity = 1;
    });

    // Başvuru popup kontrolü
    const btnBasvuru = document.getElementById('btnBasvuru');
    const popupForm = document.getElementById('popupForm');
    const closeBtn = document.getElementById('closeBtn');
    btnBasvuru.addEventListener('click', () => {
      popupForm.classList.add('active');
      btnBasvuru.setAttribute('aria-expanded', 'true');
      // Focus formun ilk inputuna
      document.getElementById('uid').focus();
    });
    closeBtn.addEventListener('click', () => {
      popupForm.classList.remove('active');
      btnBasvuru.setAttribute('aria-expanded', 'false');
      btnBasvuru.focus();
      resetFormStatus();
    });

    // ESC ile popup kapatma
    window.addEventListener('keydown', (e) => {
      if(e.key === "Escape" && popupForm.classList.contains('active')) {
        popupForm.classList.remove('active');
        btnBasvuru.setAttribute('aria-expanded', 'false');
        btnBasvuru.focus();
        resetFormStatus();
      }
    });

    // Başvuru form gönderimi ve durum bildirimi
    const basvuruForm = document.getElementById('basvuruForm');
    const formStatus = document.getElementById('formStatus');

    function resetFormStatus(){
      formStatus.textContent = '';
    }

    basvuruForm.addEventListener('submit', (e) => {
      e.preventDefault();

      formStatus.textContent = "Başvurunuz gönderiliyor...";
      const formData = new FormData(basvuruForm);

      fetch(basvuruForm.action, {
        method: 'POST',
        body: formData,
        headers: {
          'Accept': 'application/json'
        }
      }).then(response => {
        if (response.ok) {
          formStatus.style.color = '#00ffcc';
          formStatus.textContent = "Başvurunuz başarıyla alındı! Onaylandı veya reddedildiğinde bilgilendirileceksiniz.";
          basvuruForm.reset();
        } else {
          throw new Error('Bir hata oluştu');
        }
      }).catch(() => {
        formStatus.style.color = '#ff004c';
        formStatus.textContent = "Başvuru gönderilemedi. Lütfen tekrar deneyin.";
      });
    });

    // Ziyaretçi sayacı simülasyonu (örnek, gerçek backend yok)
    const ziyaretciBar = document.getElementById('ziyaretciBar');
    const ziyaretciText = document.getElementById('ziyaretciText');
    // Rastgele sayı 30-120 arası günlük ziyaretçi sayısı simüle edilir
    function simulateVisitorCount() {
      let ziyaretciSayisi = Math.floor(Math.random() * 90) + 30;
      let widthPercent = Math.min(100, (ziyaretciSayisi / 150) * 100); // max 150 kişi baz alınır
      ziyaretciBar.style.width = widthPercent + '%';
      ziyaretciText.textContent = `Bugün: ${ziyaretciSayisi} ziyaretçi`;
    }
    simulateVisitorCount();

    // İletişim butonu TikTok pop-up toggle (basit)
    const btnIletisim = document.getElementById('btnIletisim');
    btnIletisim.addEventListener('click', () => {
      alert('TikTok hesapları:\n@mazz99theboss\n@babavizyondapm');
    });
  </script>

</body>
