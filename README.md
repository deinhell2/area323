<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99</title>
<meta name="description" content="PUBG Mobile klanı ZZONE99 - 2018’den beri aktif, kaliteli topluluk. Katılmak için başvuru yap!" />
<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');

  * {
    box-sizing: border-box;
  }
  body {
    margin: 0; padding: 0;
    font-family: 'Montserrat', sans-serif;
    background: linear-gradient(135deg, #001f3f, #0074D9);
    color: #e0f7ff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
  header {
    text-align: center;
    padding: 40px 20px 20px;
  }
  header img.logo {
    width: 160px;
    animation: glow 3s ease-in-out infinite alternate;
    margin-bottom: 10px;
  }
  @keyframes glow {
    0% {filter: drop-shadow(0 0 4px #00ffff);}
    100% {filter: drop-shadow(0 0 15px #00e6ff);}
  }
  header h1 {
    font-size: 3rem;
    font-weight: 900;
    letter-spacing: 0.15em;
    margin: 0;
    color: #00e6ff;
    text-shadow:
      0 0 5px #00e6ff,
      0 0 10px #00e6ff,
      0 0 20px #00ffff,
      0 0 30px #00ffff;
  }
  main {
    flex-grow: 1;
    max-width: 900px;
    margin: 0 auto;
    padding: 0 15px 40px;
  }
  section {
    background: rgba(0, 36, 70, 0.65);
    border-radius: 12px;
    margin-bottom: 30px;
    padding: 25px 30px;
    box-shadow: 0 0 15px rgba(0, 230, 255, 0.25);
    transition: background 0.3s ease;
  }
  section:hover {
    background: rgba(0, 36, 70, 0.85);
  }
  section h2 {
    margin-top: 0;
    font-size: 1.9rem;
    border-bottom: 2px solid #00e6ff;
    padding-bottom: 8px;
    margin-bottom: 20px;
  }
  /* Tanıtım metni */
  #tanitim p {
    line-height: 1.5;
    font-size: 1.15rem;
  }

  /* Karakter logosu bölümü */
  #uyeler .member-list {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
  }
  #uyeler .member {
    text-align: center;
    max-width: 140px;
  }
  #uyeler .member img {
    width: 140px;
    height: auto;
    border-radius: 15px;
    box-shadow: 0 0 10px #00e6ff;
    transition: transform 0.3s ease;
  }
  #uyeler .member img:hover {
    transform: scale(1.05) rotate(3deg);
    filter: drop-shadow(0 0 6px #00ffff);
  }
  #uyeler .member .nick {
    margin-top: 10px;
    font-size: 1.3rem;
    font-weight: 700;
    color: #00e6ff;
    text-shadow: 0 0 7px #00b8d9;
  }

  /* Başvuru formu */
  #basvuru form {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }
  #basvuru label {
    font-weight: 600;
    margin-bottom: 4px;
  }
  #basvuru input, #basvuru select, #basvuru textarea {
    padding: 10px 12px;
    font-size: 1rem;
    border-radius: 8px;
    border: none;
    outline: none;
    box-shadow: 0 0 6px #00e6ff inset;
    background: #003050;
    color: #d0f0ff;
    transition: box-shadow 0.3s ease;
  }
  #basvuru input:focus, #basvuru select:focus, #basvuru textarea:focus {
    box-shadow: 0 0 12px #00ffff;
  }
  #basvuru button {
    background: #00d8ff;
    border: none;
    color: #003050;
    font-weight: 700;
    font-size: 1.2rem;
    border-radius: 10px;
    padding: 12px;
    cursor: pointer;
    box-shadow: 0 0 15px #00b4cc;
    transition: background 0.3s ease, box-shadow 0.3s ease;
  }
  #basvuru button:hover {
    background: #00a9cc;
    box-shadow: 0 0 25px #00ffff;
  }
  #basvuru .feedback {
    margin-top: 15px;
    font-weight: 700;
    font-size: 1.1rem;
    text-align: center;
  }
  #basvuru .feedback.success {
    color: #7fffd4;
  }
  #basvuru .feedback.error {
    color: #ff6b6b;
  }

  /* İletişim bölümü */
  #iletisim {
    text-align: center;
    padding: 0;
    margin-bottom: 40px;
  }
  #iletisim .contacts {
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
  }
  #iletisim .contact {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 130px;
  }
  #iletisim .contact img {
    width: 90px;
    border-radius: 50%;
    box-shadow: 0 0 10px #00e6ff;
    transition: box-shadow 0.3s ease;
  }
  #iletisim .contact img:hover {
    box-shadow: 0 0 18px #00ffff;
  }
  #iletisim .contact a {
    margin-top: 8px;
    font-weight: 600;
    font-size: 1.1rem;
    color: #00c8ff;
    text-decoration: none;
    transition: color 0.3s ease;
  }
  #iletisim .contact a:hover {
    color: #00ffff;
  }
  #iletisim .contact .tiktok-icon {
    vertical-align: middle;
    width: 20px;
    height: 20px;
    margin-right: 5px;
    filter: drop-shadow(0 0 1px #00b8d9);
  }

  /* Footer */
  footer {
    text-align: center;
    padding: 15px 20px;
    background: #002140;
    color: #0099cc;
    font-weight: 600;
    letter-spacing: 0.1em;
    box-shadow: inset 0 2px 5px #003355;
    user-select: none;
  }

  /* Responsive */
  @media (max-width: 600px) {
    header h1 {
      font-size: 2.5rem;
    }
    #uyeler .member-list {
      gap: 30px;
    }
    #uyeler .member {
      max-width: 120px;
    }
    #uyeler .member img {
      width: 120px;
    }
    #iletisim .contacts {
      gap: 25px;
    }
    #iletisim .contact {
      max-width: 100px;
    }
    #iletisim .contact img {
      width: 70px;
    }
    #iletisim .contact a {
      font-size: 1rem;
    }
  }
</style>
</head>
<body>

<header>
  <img src="logo.png" alt="ZZONE99 Logo" class="logo" />
  <h1>ZZONE99</h1>
</header>

<main>

  <section id="tanitim" aria-label="Klan Tanıtımı">
    <h2>TANITIM</h2>
    <p>
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,<br />
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.<br />
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </p>
  </section>

  <section id="uyeler" aria-label="Klan Üyeleri">
    <h2>ÜYELER</h2>
    <div class="member-list">
      <div class="member" role="group" aria-label="mAzz99">
        <img src="mazz.png" alt="mAzz99 Logo" />
        <div class="nick">mAzz99</div>
      </div>
      <div class="member" role="group" aria-label="yAzz99">
        <img src="yazz.png" alt="yAzz99 Logo" />
        <div class="nick">yAzz99</div>
      </div>
    </div>
  </section>

  <section id="basvuru" aria-label="Klan Başvuru Formu">
    <h2>KLANA KATIL</h2>
    <form id="applyForm" action="https://formspree.io/f/xldnljve" method="POST" novalidate>
      <label for="uid">UID - Oyun İsmi</label>
      <input type="text" id="uid" name="UID_OyunIsmi" required placeholder="Örnek: 12345678 - PlayerName" />
      
      <label for="isim">İsim - Yaş</label>
      <input type="text" id="isim" name="Isim_Yas" required placeholder="Örnek: Muhammet - 20" />
      
      <label for="cihaz">Kullandığı Cihaz</label>
      <select id="cihaz" name="Cihaz" required>
        <option value="" disabled selected>Seçiniz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="PC Emulator">PC Emulator</option>
        <option value="Diğer">Diğer</option>
      </select>

      <label for="aktiflik">Aktiflik</label>
      <textarea id="aktiflik" name="Aktiflik" rows="3" placeholder="Ne kadar süredir oynuyorsunuz?" required></textarea>

      <button type="submit">Başvuruyu Gönder</button>
      <div class="feedback" id="feedbackMsg" role="alert" aria-live="polite"></div>
    </form>
  </section>

  <section id="iletisim" aria-label="İletişim Bilgileri">
    <h2>İLETİŞİM</h2>
    <div class="contacts">
      <div class="contact" role="group" aria-label="mAzz99 TikTok">
        <img src="mazz.png" alt="mAzz99 Logo" />
        <a href="https://www.tiktok.com/@mAzz99theboss" target="_blank" rel="noopener noreferrer" tabindex="0">
          <img src="https://cdn-icons-png.flaticon.com/512/3046/3046120.png" alt="TikTok Icon" class="tiktok-icon" /> @mAzz99theboss
        </a>
      </div>
      <div class="contact" role="group" aria-label="yAzz99 TikTok">
        <img src="yazz.png" alt="yAzz99 Logo" />
        <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener noreferrer" tabindex="0">
          <img src="https://cdn-icons-png.flaticon.com/512/3046/3046120.png" alt="TikTok Icon" class="tiktok-icon" /> @babavizyondapm
        </a>
      </div>
    </div>
  </section>

</main>

<footer>
  Für die Famillia &nbsp;|&nbsp; SINCE 2018
</footer>

<script>
  // Başvuru formu gönderimi ve geri bildirim
  const form = document.getElementById('applyForm');
  const feedback = document.getElementById('feedbackMsg');

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    feedback.textContent = 'Gönderiliyor...';
    feedback.className = 'feedback';

    const data = new FormData(form);

    fetch(form.action, {
      method: 'POST',
      body: data,
      headers: { 'Accept': 'application/json' }
    }).then(response => {
      if (response.ok) {
        feedback.textContent = 'Başvurunuz alındı, teşekkürler!';
        feedback.classList.add('success');
        form.reset();
      } else {
        response.json().then(data => {
          if (data.errors) {
            feedback.textContent = data.errors.map(error => error.message).join(', ');
          } else {
            feedback.textContent = 'Bir hata oluştu, lütfen tekrar deneyin.';
          }
          feedback.classList.add('error');
        });
      }
    }).catch(() => {
      feedback.textContent = 'Gönderim sırasında bir hata oluştu.';
      feedback.classList.add('error');
    });
  });
</script>

</body>

