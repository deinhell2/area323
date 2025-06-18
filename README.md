<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>zzone99</title>
<meta name="description" content="ZZONE99 PUBG Mobile Klan Sitesi - Since 2018" />
<meta name="keywords" content="PUBG, ZZONE99, Klan, Oyun, Başvuru" />
<meta name="author" content="ZZONE99 Klan" />
<link rel="icon" href="logo.png" type="image/png" />
<style>
  /* Reset & base */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #1e2a38, #16232f);
    color: #eee;
    overflow-x: hidden;
  }
  a {
    color: #00d8ff;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }

  /* Animasyonlu arkaplan */
  body::before {
    content: '';
    position: fixed;
    top: 0; left: 0; right:0; bottom: 0;
    background: radial-gradient(circle at center, #00405f, #0a1e2d);
    z-index: -3;
    animation: bgPulse 20s ease-in-out infinite alternate;
  }
  @keyframes bgPulse {
    0% { filter: brightness(1); }
    50% { filter: brightness(1.3); }
    100% { filter: brightness(1); }
  }

  /* Logo Animasyonu */
  #logo-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 8vh;
    animation: logoPopIn 2s ease forwards;
    opacity: 0;
  }
  @keyframes logoPopIn {
    to { opacity: 1; transform: scale(1); }
    from { opacity: 0; transform: scale(0.5); }
  }
  #logo-container img {
    width: 150px;
    height: 150px;
    object-fit: contain;
    filter: drop-shadow(0 0 6px #00d8ffaa);
  }
  #logo-container h1 {
    font-size: 3rem;
    margin-top: 10px;
    color: #00d8ff;
    letter-spacing: 0.15em;
    text-shadow: 0 0 8px #00d8ffaa;
  }

  /* Giriş animasyonu ekranı */
  #intro {
    position: fixed;
    inset: 0;
    background: #0c1621;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    z-index: 9999;
    animation: fadeOut 0.8s ease forwards;
    animation-delay: 2.2s;
  }
  #intro img {
    width: 130px;
    filter: drop-shadow(0 0 10px #00d8ff);
  }
  #intro h1 {
    margin-top: 15px;
    font-size: 2.5rem;
    color: #00d8ff;
    letter-spacing: 0.2em;
    font-weight: 700;
  }
  @keyframes fadeOut {
    to { opacity: 0; visibility: hidden; }
  }

  /* Ana container ve sayfa bölümleri */
  #main {
    opacity: 0;
    animation: fadeInMain 1s ease forwards;
    animation-delay: 2.7s;
    padding: 20px;
    max-width: 960px;
    margin: 0 auto;
  }
  @keyframes fadeInMain {
    to { opacity: 1; }
  }

  /* Butonlar */
  .btn {
    display: inline-block;
    padding: 12px 28px;
    margin: 12px 8px 20px 8px;
    border-radius: 30px;
    border: 2px solid #00d8ff;
    background: transparent;
    color: #00d8ff;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 0 8px #00d8ff44;
    user-select: none;
  }
  .btn:hover {
    background: #00d8ff;
    color: #0c1621;
    box-shadow: 0 0 15px #00d8ffdd;
  }

  /* Sayfa bölümleri */
  section {
    margin-bottom: 40px;
    border-radius: 12px;
    background: rgba(0,0,0,0.3);
    padding: 20px;
    box-shadow: 0 0 15px #00d8ff44;
  }
  section h2 {
    margin-bottom: 16px;
    font-size: 2rem;
    color: #00d8ff;
    border-bottom: 2px solid #00d8ff;
    padding-bottom: 6px;
    user-select: none;
  }
  section p, section li {
    font-size: 1.1rem;
    line-height: 1.4;
  }
  ul {
    list-style-type: disc;
    margin-left: 20px;
  }

  /* Başvuru formu */
  form {
    display: flex;
    flex-direction: column;
    gap: 14px;
    max-width: 500px;
  }
  input, select, textarea {
    padding: 10px 14px;
    font-size: 1rem;
    border-radius: 8px;
    border: none;
    outline: none;
    background: #001f35;
    color: #ccc;
    box-shadow: inset 0 0 5px #00d8ff55;
    transition: box-shadow 0.3s ease;
  }
  input:focus, select:focus, textarea:focus {
    box-shadow: 0 0 10px #00d8ffbb;
  }
  button[type="submit"] {
    max-width: 200px;
    margin-top: 8px;
    align-self: flex-start;
  }

  /* Üyeler listesi */
  #uyeler ul {
    list-style: none;
    padding-left: 0;
  }
  #uyeler li {
    margin-bottom: 10px;
    font-weight: 600;
    color: #a0f0ff;
  }

  /* TikTok embed container */
  .tiktok-container {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    justify-content: center;
  }

  /* Burger Menü */
  #burger {
    position: fixed;
    top: 20px; right: 20px;
    width: 35px; height: 28px;
    cursor: pointer;
    z-index: 10001;
    display: none;
    flex-direction: column;
    justify-content: space-between;
  }
  #burger div {
    width: 100%;
    height: 4px;
    background-color: #00d8ff;
    border-radius: 3px;
    transition: all 0.3s ease;
  }
  #burger.active div:nth-child(1) {
    transform: translateY(12px) rotate(45deg);
  }
  #burger.active div:nth-child(2) {
    opacity: 0;
  }
  #burger.active div:nth-child(3) {
    transform: translateY(-12px) rotate(-45deg);
  }

  nav {
    position: fixed;
    top: 0; right: 0;
    height: 100vh;
    width: 240px;
    background: rgba(0, 216, 255, 0.15);
    backdrop-filter: blur(12px);
    box-shadow: -4px 0 16px #00d8ff44;
    transform: translateX(100%);
    transition: transform 0.35s ease;
    padding-top: 60px;
    z-index: 10000;
  }
  nav.active {
    transform: translateX(0);
  }
  nav ul {
    list-style: none;
    padding-left: 24px;
  }
  nav ul li {
    margin-bottom: 28px;
  }
  nav ul li a {
    font-weight: 600;
    font-size: 1.3rem;
    color: #00d8ff;
  }
  nav ul li a:hover {
    color: #a0f0ff;
  }

  /* Responsive */
  @media (max-width: 768px) {
    #burger {
      display: flex;
    }
    #main {
      padding: 20px 12px;
    }
  }
</style>
</head>
<body>

<!-- Giriş animasyonu -->
<div id="intro">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
</div>

<!-- Burger Menü -->
<div id="burger" aria-label="Toggle menu" role="button" tabindex="0">
  <div></div><div></div><div></div>
</div>

<!-- Menü -->
<nav id="menu">
  <ul>
    <li><a href="#tanitim" onclick="closeMenu()">Tanıtım</a></li>
    <li><a href="#basvuru" onclick="closeMenu()">Başvuru</a></li>
    <li><a href="#iletisim" onclick="closeMenu()">İletişim</a></li>
    <li><a href="#uyeler" onclick="closeMenu()">Üyeler</a></li>
  </ul>
</nav>

<!-- Ana içerik -->
<main id="main" role="main" aria-label="ZZONE99 Klan sitesi">

  <!-- Tanıtım -->
  <section id="tanitim" tabindex="0">
    <div id="logo-container">
      <img src="logo.png" alt="ZZONE99 Logo" />
      <h1>ZZONE99</h1>
    </div>
    <p style="margin-top:20px; font-size:1.2rem; line-height:1.5; max-width:720px;">
      Since 2018, klanımız <strong>Für die GANG</strong> ve <strong>AREA323</strong> olarak
      başlayan yolculuğuna, yeni bir vizyon ile <strong>ZZONE99</strong> olarak devam etmektedir.
    </p>
  </section>

  <!-- Başvuru -->
  <section id="basvuru" tabindex="0">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xldnljve" method="POST">
      <label for="oyuncu">Oyuncu Adı ve UID</label>
      <input type="text" name="oyuncu" id="oyuncu" placeholder="Örn: mAzz99 #123456" required />

      <label for="yas">Yaş</label>
      <input type="number" name="yas" id="yas" placeholder="Yaşınızı yazın" min="12" max="99" required />

      <label for="aktiflik">Aktiflik</label>
      <select name="aktiflik" id="aktiflik" required>
        <option value="" disabled selected>Seçiniz</option>
        <option value="Günlük">Günlük</option>
        <option value="Haftalık">Haftalık</option>
        <option value="Ara sıra">Ara sıra</option>
      </select>

      <label for="cihaz">Kullandığı cihaz</label>
      <input type="text" name="cihaz" id="cihaz" placeholder="Örn: Android, iPhone" required />

      <label for="iletisim_oyun">Oyun İçi İletişim (mAzz99 516572604)</label>
      <input type="text" name="iletisim_oyun" id="iletisim_oyun" value="mAzz99 516572604" readonly />
      
      <button type="submit" class="btn">Başvur</button>
    </form>
  </section>

  <!-- İletişim -->
  <section id="iletisim" tabindex="0">
    <h2>İletişim</h2>
    <p>Bizimle TikTok üzerinden iletişime geçebilirsiniz:</p>
    <ul>
      <li><a href="https://www.tiktok.com/@mAzz99theboss" target="_blank" rel="noopener">@mAzz99theboss</a></li>
      <li><a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener">@babavizyondapm</a></li>
    </ul>
    <div class="tiktok-container">
      <blockquote class="tiktok-embed" cite="https://www.tiktok.com/@mAzz99theboss" data-video-id="" style="max-width: 325px; min-width: 325px;" > </blockquote>
      <blockquote class="tiktok-embed" cite="https://www.tiktok.com/@babavizyondapm" data-video-id="" style="max-width: 325px; min-width: 325px;" > </blockquote>
    </div>
  </section>

  <!-- Üyeler -->
  <section id="uyeler" tabindex="0">
    <h2>Üyeler</h2>
    <ul>
      <li><strong>Lider Kadrosu:</strong> mAzz99, yAzz99</li>
      <li><strong>Yönetici Kadrosu:</strong> iSzz99</li>
    </ul>
  </section>

  <footer style="text-align:center; margin-top:40px; padding: 20px 0; color:#00405f; font-weight: 600;">
    Für die Famillia
  </footer>
</main>

<!-- Ziyaretçi Sayacı -->
<div style="position: fixed; bottom: 15px; left: 15px; color: #00d8ff; font-weight: 600; user-select:none; font-family: monospace; font-size: 14px; z-index: 10000;">
  Ziyaretçi Sayısı: <span id="visitorCount">0</span>
</div>

<!-- Tawk.to Canlı Sohbet -->
<script type="text/javascript">
var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/68526ad5a39e6f190afdd004/1iu0v2kel';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();
</script>

<script async src="https://www.tiktok.com/embed.js"></script>

<script>
  // Intro ekranını 2 saniye sonra gizle
  window.addEventListener('load', () => {
    setTimeout(() => {
      document.getElementById('intro').style.display = 'none';
      document.getElementById('main').style.opacity = '1';
    }, 2200);
  });

  // Burger menü açma/kapatma
  const burger = document.getElementById('burger');
  const menu = document.getElementById('menu');

  burger.addEventListener('click', () => {
    burger.classList.toggle('active');
    menu.classList.toggle('active');
  });
  function closeMenu() {
    burger.classList.remove('active');
    menu.classList.remove('active');
  }

  // Basit ziyaretçi sayacı (localStorage tabanlı)
  const countEl = document.getElementById('visitorCount');
  let count = localStorage.getItem('visitorCount');
  if(!count) count = 0;
  count = parseInt(count) + 1;
  localStorage.setItem('visitorCount', count);
  countEl.textContent = count;

  // Smooth scroll navigation for anchor links
  document.querySelectorAll('nav ul li a').forEach(anchor => {
    anchor.addEventListener('click', e => {
      e.preventDefault();
      const targetID = anchor.getAttribute('href').substring(1);
      const targetSection = document.getElementById(targetID);
      if(targetSection){
        targetSection.scrollIntoView({behavior: 'smooth'});
        closeMenu();
        // Update URL without reloading page
        history.pushState(null, null, `#${targetID}`);
      }
    });
  });

  // Accessibility: allow burger menu toggle with keyboard
  burger.addEventListener('keydown', e => {
    if(e.key === 'Enter' || e.key === ' ') {
      e.preventDefault();
      burger.click();
    }
  });
</script>
</body>
