<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99</title>
<style>
  /* Genel body */
  body {
    margin: 0; padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #0a1f2f, #003346);
    color: #e0f7fa;
    overflow-x: hidden;
  }

  /* Giriş animasyonu fadeIn 2 saniye */
  header {
    text-align: center;
    padding: 50px 20px;
    animation: fadeIn 2s ease forwards;
    opacity: 0;
  }

  @keyframes fadeIn {
    to { opacity: 1; }
  }

  /* Logo */
  header img {
    width: 140px;
    height: auto;
    margin-bottom: 10px;
    filter: drop-shadow(0 0 10px #00fff7);
    animation: glow 3s ease-in-out infinite alternate;
  }

  @keyframes glow {
    0% { filter: drop-shadow(0 0 5px #00fff7);}
    100% { filter: drop-shadow(0 0 20px #00fff7);}
  }

  /* Başlık */
  header h1 {
    font-size: 3.5rem;
    margin: 0;
    color: #00fff7;
    text-shadow: 0 0 10px #00fff7;
  }

  /* Butonlar container */
  .buttons {
    display: flex;
    justify-content: center;
    gap: 40px;
    margin-top: 30px;
    flex-wrap: wrap;
  }

  /* Butonlar stili */
  button {
    background: #00fff7;
    border: none;
    padding: 15px 45px;
    font-size: 1.25rem;
    font-weight: 600;
    border-radius: 8px;
    cursor: pointer;
    color: #002b33;
    transition: all 0.3s ease;
    box-shadow: 0 0 15px #00fff7aa;
  }
  button:hover {
    background: #00c6b8;
    box-shadow: 0 0 25px #00fff7ff;
  }

  /* TikTok profilleri */
  .tiktok-profiles {
    margin: 35px auto 0;
    max-width: 360px;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 20px;
  }
  .tiktok-profile {
    background: #004d66;
    padding: 12px 18px;
    border-radius: 15px;
    box-shadow: 0 0 12px #00fff7aa;
    flex: 1 1 140px;
    text-align: center;
  }
  .tiktok-profile a {
    color: #00fff7;
    font-weight: 700;
    font-size: 1.1rem;
    text-decoration: none;
  }
  .tiktok-profile a:hover {
    text-decoration: underline;
  }

  /* Başvuru durumu sorgulama */
  .application-status {
    margin: 50px auto 70px;
    text-align: center;
    max-width: 320px;
  }
  .application-status h2 {
    font-size: 1.8rem;
    margin-bottom: 20px;
    color: #00fff7;
    text-shadow: 0 0 8px #00fff7bb;
  }
  .application-status input {
    width: 90%;
    padding: 12px 15px;
    font-size: 1rem;
    border-radius: 10px;
    border: none;
    outline: none;
    margin-bottom: 15px;
    box-shadow: inset 0 0 10px #00fff7aa;
    color: #004d66;
    font-weight: 600;
  }
  .application-status button {
    width: 94%;
  }

  /* Responsive */
  @media (max-width: 600px) {
    header h1 {
      font-size: 2.8rem;
    }
    .buttons {
      flex-direction: column;
      gap: 20px;
    }
    button {
      width: 80%;
      padding: 14px;
    }
    .tiktok-profiles {
      max-width: 90vw;
      gap: 15px;
    }
  }
</style>
</head>
<body>

<header>
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
</header>

<div class="buttons">
  <button onclick="document.getElementById('popup').style.display='flex'">Klana Katıl</button>
  <button onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">İletişim</button>
</div>

<div class="tiktok-profiles">
  <div class="tiktok-profile"><a href="https://www.tiktok.com/@mazz99theboss" target="_blank" rel="noopener">@mazz99theboss</a></div>
  <div class="tiktok-profile"><a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener">@babavizyondapm</a></div>
</div>

<section class="application-status" id="application-status">
  <h2>Başvuru Durumu Sorgula</h2>
  <input id="uidInput" type="text" placeholder="Oyun UID'nizi girin" />
  <br />
  <button onclick="checkApplicationStatus()">Durumu Sorgula</button>
</section>

<section id="contact" style="max-width:400px;margin:50px auto; text-align:center;">
  <h2 style="color:#00fff7;">İletişim</h2>
  <p>
    TikTok Profilleri:<br />
    <a href="https://www.tiktok.com/@mazz99theboss" target="_blank" rel="noopener" style="color:#00fff7; font-weight:bold;">@mazz99theboss</a><br />
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener" style="color:#00fff7; font-weight:bold;">@babavizyondapm</a>
  </p>
</section>

<!-- Klana Katıl Pop-up -->
<div id="popup" style="
  display:none;
  position:fixed;
  top:0; left:0; right:0; bottom:0;
  background: rgba(0,0,0,0.85);
  justify-content:center;
  align-items:center;
  z-index:9999;
">
  <div style="
    background:#002b33;
    padding:30px;
    border-radius:20px;
    width:90%;
    max-width:400px;
    box-shadow: 0 0 20px #00fff7aa;
    color:#e0f7fa;
    position: relative;
  ">
    <h2 style="text-align:center; color:#00fff7;">Klana Katıl</h2>
    <form id="joinForm">
      <input name="uid" placeholder="UID - Oyun İsmi" required style="width:100%; padding:12px; margin-bottom:15px; border-radius:10px; border:none;"/>
      <input name="name" placeholder="İsim" required style="width:100%; padding:12px; margin-bottom:15px; border-radius:10px; border:none;"/>
      <input name="age" type="number" placeholder="Yaş" required style="width:100%; padding:12px; margin-bottom:15px; border-radius:10px; border:none;"/>
      <input name="device" placeholder="Kullandığı Cihaz" required style="width:100%; padding:12px; margin-bottom:15px; border-radius:10px; border:none;"/>
      <input name="activity" placeholder="Aktiflik" required style="width:100%; padding:12px; margin-bottom:25px; border-radius:10px; border:none;"/>
      <button type="submit" style="width:100%; background:#00fff7; border:none; padding:15px; border-radius:10px; font-weight:700; color:#002b33; cursor:pointer; transition: background 0.3s;">
        Başvur
      </button>
    </form>
    <button onclick="document.getElementById('popup').style.display='none'" style="position:absolute; top:10px; right:15px; background:none; border:none; font-size:1.5rem; color:#00fff7; cursor:pointer;">&times;</button>
    <p id="formResponse" style="margin-top:15px; text-align:center;"></p>
  </div>
</div>

<script>
  // Başvuru formu gönderimi
  document.getElementById('joinForm').addEventListener('submit', async function(e) {
    e.preventDefault();
    const form = e.target;
    const formData = new FormData(form);

    // Formspree endpoint
    const url = 'https://formspree.io/f/xldnljve';

    try {
      const response = await fetch(url, {
        method: 'POST',
        body: formData,
        headers: { 'Accept': 'application/json' }
      });
      if (response.ok) {
        document.getElementById('formResponse').textContent = 'Başvurunuz başarıyla alındı!';
        form.reset();
      } else {
        document.getElementById('formResponse').textContent = 'Başvuru gönderilirken hata oluştu. Lütfen tekrar deneyin.';
      }
    } catch (error) {
      document.getElementById('formResponse').textContent = 'Başvuru gönderilirken hata oluştu. Lütfen internet bağlantınızı kontrol edin.';
    }
  });

  // Başvuru durum sorgulama (örnek statik)
  function checkApplicationStatus() {
    const uid = document.getElementById('uidInput').value.trim();
    if (!uid) {
      alert('Lütfen UID girin!');
      return;
    }
    // Gerçek sorgu API bağlanabilir burada, şimdilik örnek alert:
    alert(`Başvuru durumu: Onay Bekliyor (UID: ${uid})`);
  }
</script>

</body>
