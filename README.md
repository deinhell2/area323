<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');
  * {
    margin:0; padding:0; box-sizing: border-box;
  }
  body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #cce7ff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px 20px 80px;
    text-align: center;
    position: relative;
  }
  #logo {
    width: 140px;
    margin-bottom: 20px;
    filter: drop-shadow(0 0 6px #40e0d0);
    animation: glow 3s ease-in-out infinite alternate;
  }
  @keyframes glow {
    from { filter: drop-shadow(0 0 4px #40e0d0); }
    to { filter: drop-shadow(0 0 12px #40e0d0); }
  }
  h1 {
    font-size: 3.5rem;
    font-weight: 700;
    margin-bottom: 30px;
    color: #55d8e7;
    text-shadow:
      0 0 5px #33c2d9,
      0 0 10px #00fff7,
      0 0 20px #00fff7,
      0 0 30px #00fff7,
      0 0 40px #00fff7;
  }
  #intro {
    max-width: 600px;
    font-weight: 400;
    font-size: 1.25rem;
    line-height: 1.6;
    color: #a0cde7cc;
    margin-bottom: 50px;
  }
  #contact {
    width: 100%;
    max-width: 600px;
    background: rgba(8, 34, 44, 0.75);
    padding: 25px 30px;
    border-radius: 15px;
    box-shadow: 0 0 12px #00fff7aa;
    color: #d6f5ff;
    text-align: center;
  }
  #contact h2 {
    margin-bottom: 25px;
    font-size: 2rem;
    color: #00d9f7;
    text-shadow: 0 0 8px #00d9f7;
  }
  #contact .members {
    display: flex;
    justify-content: center;
    gap: 40px;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .member {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 130px;
  }
  .member img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    box-shadow: 0 0 8px #00fff7bb;
    margin-bottom: 12px;
    transition: transform 0.3s ease;
  }
  .member img:hover {
    transform: scale(1.1) rotate(3deg);
    box-shadow: 0 0 20px #00fff7ff;
  }
  .member .nickname {
    font-weight: 700;
    font-size: 1.1rem;
    margin-bottom: 8px;
    color: #75e0ff;
    text-shadow: 0 0 4px #00c4da;
  }
  .member a {
    color: #0ff6ff;
    text-decoration: none;
    font-weight: 600;
    transition: color 0.3s ease;
  }
  .member a:hover {
    color: #00a7bb;
    text-shadow: 0 0 8px #00a7bb;
  }
  footer {
    margin-top: 50px;
    color: #0093a0dd;
    font-weight: 600;
    font-size: 1rem;
    letter-spacing: 1.5px;
    text-shadow: 0 0 4px #005f6b;
  }

  /* Popup Button */
  #applyBtn {
    position: fixed;
    top: 15px;
    left: 50%;
    transform: translateX(-50%);
    background: #00fff7;
    color: #00373d;
    font-weight: 700;
    font-size: 1.1rem;
    padding: 12px 30px;
    border: none;
    border-radius: 40px;
    cursor: pointer;
    box-shadow: 0 0 15px #00fff7cc;
    transition: background 0.3s ease, box-shadow 0.3s ease;
    z-index: 9999;
  }
  #applyBtn:hover {
    background: #00c4bb;
    box-shadow: 0 0 25px #00c4bb;
  }

  /* Popup Overlay */
  #popupOverlay {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.85);
    backdrop-filter: blur(4px);
    z-index: 9998;
    justify-content: center;
    align-items: center;
  }
  #popupOverlay.active {
    display: flex;
  }

  /* Popup Content */
  #popupForm {
    background: linear-gradient(135deg, #0f2027, #203a43);
    padding: 30px 40px;
    border-radius: 20px;
    box-shadow: 0 0 25px #00fff7cc;
    max-width: 420px;
    width: 90%;
    color: #cce7ff;
    position: relative;
  }
  #popupForm h2 {
    margin-bottom: 20px;
    font-size: 2rem;
    color: #00d9f7;
    text-align: center;
    text-shadow: 0 0 10px #00d9f7;
  }
  #popupForm label {
    display: block;
    font-weight: 600;
    margin-bottom: 8px;
    margin-top: 15px;
    font-size: 1rem;
  }
  #popupForm input, #popupForm select {
    width: 100%;
    padding: 10px 14px;
    border-radius: 8px;
    border: none;
    font-size: 1rem;
    outline: none;
  }
  #popupForm button[type="submit"] {
    margin-top: 25px;
    width: 100%;
    padding: 12px;
    font-weight: 700;
    font-size: 1.2rem;
    background: #00fff7;
    border: none;
    border-radius: 40px;
    cursor: pointer;
    color: #00373d;
    box-shadow: 0 0 15px #00fff7cc;
    transition: background 0.3s ease, box-shadow 0.3s ease;
  }
  #popupForm button[type="submit"]:hover {
    background: #00c4bb;
    box-shadow: 0 0 25px #00c4bb;
  }
  #popupForm .closeBtn {
    position: absolute;
    top: 15px;
    right: 15px;
    background: transparent;
    border: none;
    font-size: 1.5rem;
    color: #00d9f7;
    cursor: pointer;
    font-weight: 700;
    transition: color 0.3s ease;
  }
  #popupForm .closeBtn:hover {
    color: #00939f;
  }
  #formMessage {
    margin-top: 20px;
    font-weight: 600;
    font-size: 1.1rem;
    text-align: center;
    min-height: 1.4em;
    color: #00ffcc;
    text-shadow: 0 0 6px #00ffcc;
  }
  #formMessage.error {
    color: #ff6b6b;
    text-shadow: 0 0 6px #ff6b6b;
  }

  @media (max-width: 600px) {
    #contact .members {
      gap: 25px;
    }
    .member {
      max-width: 90px;
    }
    .member img {
      width: 80px;
      height: 80px;
    }
    #intro {
      font-size: 1.1rem;
      margin-bottom: 30px;
    }
    h1 {
      font-size: 2.7rem;
      margin-bottom: 25px;
    }
    #applyBtn {
      font-size: 1rem;
      padding: 10px 25px;
      top: 10px;
    }
  }
</style>
</head>
<body>

  <!-- Logo and Title -->
  <img id="logo" src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>

  <!-- Tanıtım -->
  <div id="intro">
    İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,<br />
    bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.<br />
    Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmak.
  </div>

  <!-- İletişim -->
  <section id="contact">
    <h2>İletişim ve Üyeler</h2>
    <div class="members">
      <div class="member">
        <img src="mazz.png" alt="mAzz99" />
        <div class="nickname">mAzz99</div>
        <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank" rel="noopener noreferrer">TikTok: @mAzz99theboss</a>
      </div>
      <div class="member">
        <img src="yazz.png" alt="yAzz99" />
        <div class="nickname">yAzz99</div>
        <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener noreferrer">TikTok: @babavizyondapm</a>
      </div>
    </div>
  </section>

  <footer>Für die Famillia &nbsp;&nbsp;|&nbsp;&nbsp; SINCE 2018</footer>

  <!-- Klana Katıl Butonu -->
  <button id="applyBtn" aria-haspopup="dialog" aria-controls="popupOverlay" aria-expanded="false">Klana Katıl</button>

  <!-- Popup Form -->
  <div id="popupOverlay" role="dialog" aria-modal="true" aria-labelledby="popupTitle" tabindex="-1">
    <form id="popupForm" action="https://formspree.io/f/xldnljve" method="POST" novalidate>
      <button type="button" class="closeBtn" aria-label="Kapat">&times;</button>
      <h2 id="popupTitle">Klana Katıl Başvuru Formu</h2>

      <label for="uid">UID (Oyuncu ID):</label>
      <input type="text" id="uid" name="UID" required placeholder="Ör: 123456789" />

      <label for="gameName">Oyun İsmi:</label>
      <input type="text" id="gameName" name="Oyun_Ismi" required placeholder="Oyundaki nickiniz" />

      <label for="name">İsim:</label>
      <input type="text" id="name" name="İsim" required placeholder="Gerçek isminiz" />

      <label for="age">Yaş:</label>
      <input type="number" id="age" name="Yaş" required min="10" max="99" placeholder="Yaşınız" />

      <label for="device">Cihaz:</label>
      <select id="device" name="Cihaz" required>
        <option value="" disabled selected>Seçiniz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="Diğer">Diğer</option>
      </select>

      <label for="activity">Aktiflik Durumu:</label>
      <select id="activity" name="Aktiflik" required>
        <option value="" disabled selected>Seçiniz</option>
        <option value="Her Gün">Her Gün</option>
        <option value="Haftada birkaç kez">Haftada birkaç kez</option>
        <option value="Ara sıra">Ara sıra</option>
      </select>

      <button type="submit">Başvuruyu Gönder</button>
      <div id="formMessage" role="alert" aria-live="polite"></div>
    </form>
  </div>

<script>
  const applyBtn = document.getElementById('applyBtn');
  const popupOverlay = document.getElementById('popupOverlay');
  const closeBtn = document.querySelector('#popupForm .closeBtn');
  const popupForm = document.getElementById('popupForm');
  const formMessage = document.getElementById('formMessage');

  function openPopup() {
    popupOverlay.classList.add('active');
    applyBtn.setAttribute('aria-expanded', 'true');
    popupOverlay.focus();
  }
  function closePopup() {
    popupOverlay.classList.remove('active');
    applyBtn.setAttribute('aria-expanded', 'false');
    formMessage.textContent = '';
    formMessage.className = '';
    popupForm.reset();
    applyBtn.focus();
  }

  applyBtn.addEventListener('click', openPopup);
  closeBtn.addEventListener('click', closePopup);

  popupOverlay.addEventListener('click', (e) => {
    if(e.target === popupOverlay) closePopup();
  });

  // Form submit with Formspree and feedback
  popupForm.addEventListener('submit', async (e) => {
    e.preventDefault();

    formMessage.textContent = '';
    formMessage.className = '';

    const formData = new FormData(popupForm);
    try {
      const response = await fetch(popupForm.action, {
        method: 'POST',
        headers: { 'Accept': 'application/json' },
        body: formData
      });

      if (response.ok) {
        formMessage.textContent = 'Başvurunuz başarıyla gönderildi!';
        formMessage.className = 'success';
        popupForm.reset();
        setTimeout(() => {
          closePopup();
        }, 3000);
      } else {
        const data = await response.json();
        if (data.errors) {
          formMessage.textContent = data.errors.map(e => e.message).join(', ');
        } else {
          formMessage.textContent = 'Başvuru gönderilirken hata oluştu.';
        }
        formMessage.className = 'error';
      }
    } catch {
      formMessage.textContent = 'Başvuru gönderilirken bir hata oluştu. İnternet bağlantınızı kontrol edin.';
      formMessage.className = 'error';
    }
  });
</script>

</body>
