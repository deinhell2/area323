<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>zzone99 - PUBG Mobile Klan</title>
<meta name="description" content="ZZONE99 PUBG Mobile Klan Sitesi - Rekabetçi, Dost Canlısı ve Aktif" />
<meta name="keywords" content="PUBG, ZZONE99, Klan, PUBG Mobile, Başvuru, Türkiye" />
<meta name="author" content="ZZONE99 Klan" />
<link rel="icon" href="logo.png" type="image/png" />

<style>
  /* Reset & Base */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
  }
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: var(--bg);
    color: var(--text-color);
    overflow-x: hidden;
    transition: background 0.5s ease, color 0.5s ease;
  }
  a {
    color: var(--accent);
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }

  /* Tema renkleri */
  :root {
    --accent: #00d8ff;
    --bg: linear-gradient(135deg, #1e2a38, #16232f);
    --bg-alt: rgba(0, 216, 255, 0.15);
    --text-color: #eee;
    --box-bg: rgba(0,0,0,0.3);
    --shadow: #00d8ff44;
    --popup-bg: #001f35;
  }
  body.dark {
    --accent: #00d8ff;
    --bg: linear-gradient(135deg, #16232f, #0d151f);
    --bg-alt: rgba(0, 216, 255, 0.25);
    --text-color: #ccc;
    --box-bg: rgba(5,5,5,0.6);
    --shadow: #00d8ff66;
    --popup-bg: #000a12;
  }
  body.light {
    --accent: #0077cc;
    --bg: linear-gradient(135deg, #f5f7fa, #e9eff5);
    --bg-alt: rgba(0, 119, 204, 0.12);
    --text-color: #202020;
    --box-bg: rgba(255,255,255,0.8);
    --shadow: #0077cc44;
    --popup-bg: #f0f5fa;
  }

  /* Animasyonlu arkaplan */
  body::before {
    content: '';
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background: radial-gradient(circle at center, var(--accent), #0a1e2d);
    z-index: -3;
    animation: bgPulse 20s ease-in-out infinite alternate;
    filter: brightness(0.7);
  }
  @keyframes bgPulse {
    0% { filter: brightness(0.7); }
    50% { filter: brightness(1.2); }
    100% { filter: brightness(0.7); }
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
    width: 160px;
    height: 160px;
    object-fit: contain;
    filter: drop-shadow(0 0 8px var(--accent));
    border-radius: 50%;
  }
  #logo-container h1 {
    font-size: 3rem;
    margin-top: 12px;
    color: var(--accent);
    letter-spacing: 0.15em;
    text-shadow: 0 0 10px var(--accent);
  }

  /* Giriş animasyonu ekranı */
  #intro {
    position: fixed;
    inset: 0;
    background: var(--bg);
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    z-index: 9999;
    animation: fadeOut 0.8s ease forwards;
    animation-delay: 2.5s;
  }
  #intro img {
    width: 140px;
    filter: drop-shadow(0 0 12px var(--accent));
    border-radius: 50%;
  }
  #intro h1 {
    margin-top: 20px;
    font-size: 2.8rem;
    color: var(--accent);
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
    animation-delay: 3s;
    padding: 24px 20px 60px;
    max-width: 960px;
    margin: 0 auto;
  }
  @keyframes fadeInMain {
    to { opacity: 1; }
  }

  /* Butonlar */
  .btn {
    display: inline-block;
    padding: 14px 32px;
    margin: 12px 8px 20px 8px;
    border-radius: 30px;
    border: 2px solid var(--accent);
    background: transparent;
    color: var(--accent);
    font-weight: 700;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 0 10px var(--accent);
    user-select: none;
  }
  .btn:hover {
    background: var(--accent);
    color: var(--bg);
    box-shadow: 0 0 20px var(--accent);
  }

  /* Sayfa bölümleri */
  section {
    margin-bottom: 48px;
    border-radius: 14px;
    background: var(--box-bg);
    padding: 28px 32px;
    box-shadow: 0 0 18px var(--shadow);
    transition: background 0.4s ease;
  }
  section h2 {
    margin-bottom: 22px;
    font-size: 2.4rem;
    color: var(--accent);
    border-bottom: 3px solid var(--accent);
    padding-bottom: 8px;
    user-select: none;
  }
  section p, section li {
    font-size: 1.2rem;
    line-height: 1.6;
  }
  ul {
    list-style-type: disc;
    margin-left: 26px;
  }

  /* Başvuru formu */
  form {
    display: flex;
    flex-direction: column;
    gap: 16px;
    max-width: 540px;
  }
  input, select, textarea {
    padding: 12px 18px;
    font-size: 1.1rem;
    border-radius: 10px;
    border: none;
    outline: none;
    background: var(--popup-bg);
    color: var(--text-color);
    box-shadow: inset 0 0 8px var(--accent);
    transition: box-shadow 0.3s ease;
  }
  input:focus, select:focus, textarea:focus {
    box-shadow: 0 0 14px var(--accent);
  }
  button[type="submit"] {
    max-width: 220px;
    margin-top: 10px;
    align-self: flex-start;
  }

  /* Üyeler listesi */
  #uyeler ul {
    list-style: none;
    padding-left: 0;
  }
  #uyeler li {
    margin-bottom: 14px;
    font-weight: 700;
    color: var(--accent);
  }

  /* TikTok embed container */
  .tiktok-container {
    display: flex;
    gap: 24px;
    flex-wrap: wrap;
    justify-content: center;
  }

  /* İletişim linklerine ikon ve pop-up */
  .contact-link {
    position: relative;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    color: var(--accent);
    font-weight: 600;
  }
  .contact-link img {
    width: 28px;
    height: 28px;
    filter: drop-shadow(0 0 5px var(--accent));
    transition: transform 0.3s ease;
  }
  .contact-link:hover img {
    transform: scale(1.1);
  }
  .popup-tooltip {
    position: absolute;
    bottom: 130%;
    left: 50%;
    transform: translateX(-50%);
    background: var(--popup-bg);
    padding: 6px 14px;
    border-radius: 8px;
    font-size: 0.95rem;
    color: var(--accent);
    box-shadow: 0 0 12px var(--accent);
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s ease;
    white-space: nowrap;
    user-select: none;
    z-index: 10;
  }
  .contact-link:hover .popup-tooltip {
    opacity: 1;
    pointer-events: auto;
  }

  /* Burger Menü */
  #burger {
    position: fixed;
    top: 20px; right: 20px;
    width: 38px; height: 30px;
    cursor: pointer;
    z-index: 10001;
    display: none;
    flex-direction: column;
    justify-content: space-between;
  }
  #burger div {
    width: 100%;
    height: 4px;
    background-color: var(--accent);
    border-radius: 4px;
    transition: all 0.3s ease;
  }
  #burger.active div:nth-child(1) {
    transform: translateY(13px) rotate(45deg);
  }
  #burger.active div:nth-child(2) {
    opacity: 0;
  }
  #burger.active div:nth-child(3) {
    transform: translateY(-13px) rotate(-45deg);
  }

  nav {
    position: fixed;
    top: 0; right: 0;
    height: 100vh;
    width: 260px;
    background: var(--bg-alt);
    backdrop-filter: blur(14px);
    box-shadow: -4px 0 22px var(--shadow);
    transform: translateX(100%);
    transition: transform 0.35s ease;
    padding-top: 70px;
    z-index: 10000;
  }
  nav.active {
    transform: translateX(0);
  }
  nav ul {
    list-style: none;
    padding-left: 28px;
  }
  nav ul li {
    margin-bottom: 32px;
  }
  nav ul li a {
    font-weight: 700;
    font-size: 1.4rem;
    color: var(--accent);
  }
  nav ul li a:hover {
    color: #a0f0ff;
  }

  /* Footer */
  footer {
    text-align: center;
    margin-top: 60px;
    padding: 24px 20px;
    color: var(--accent);
    font-weight: 700;
    font-size: 1rem;
    letter-spacing: 0.15em;
  }

  /* Ziyaretçi Sayacı */
  #visitorCounter {
    position: fixed;
    bottom: 18px;
    left: 18px;
    color: var(--accent);
    font-weight: 700;
    user-select:none;
    font-family: monospace;
    font-size: 15px;
    z-index: 10000;
    text-shadow: 0 0 10px var(--accent);
  }

  /* Tema Seçici */
  #theme-toggle {
    position: fixed;
    top: 20px;
    left: 20px;
    background: var(--bg-alt);
    border-radius: 50%;
    padding: 10px;
    box-shadow: 0 0 15px var(--accent);
    cursor: pointer;
    z-index: 10002;
    transition: background 0.4s ease;
  }
  #theme-toggle:hover {
    background: var(--accent);
  }
  #theme-toggle img {
    width: 28px;
    height: 28px;
    filter: drop-shadow(0 0 6px var(--accent));
  }

  /* Responsive */
  @media (max-width: 768px) {
    #burger {
      display: flex;
    }
    #main {
      padding: 18px 14px 60px;
    }
    .tiktok-container {
      flex-direction: column;
      align-items: center;
    }
  }
</style>

</head>
<body>

<!-- Giriş animasyonu -->
<div id="intro" role="alert" aria-live="assertive">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
</div>

<!-- Tema Seçici -->
<button id="theme-toggle" aria-label="Tema değiştirme butonu" title="Tema değiştir">
  <img src="https://cdn-icons-png.flaticon.com/512/869/869869.png" alt="Tema değiştir ikonu" />
</button>

<!-- Burger Menü -->
<div id="burger" aria-label="Menüyü aç/kapat" role="button" tabindex="0" aria-expanded="false">
  <div></div><div></div><div></div>
</div>

<!-- Menü -->
<nav id="menu" role="navigation" aria-label="Ana menü">
  <ul>
    <li><a href="#tanitim" onclick="closeMenu()" aria-label="Tanıtım bölümüne git">Tanıtım</a></li>
    <li><a href="#basvuru" onclick="closeMenu()" aria-label="Başvuru formuna git">Başvuru</a></li>
    <li><a href="#iletisim" onclick="closeMenu()" aria-label="İletişim bölümüne git">İletişim</a></li>
    <li><a href="#uyeler" onclick="closeMenu()" aria-label="Üyeler bölümüne git">Üyeler</a></li>
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
    <p style="margin-top:22px; font-size:1.25rem; line-height:1.7; max-width:720px;">
      2018 yılında <strong>Für die GANG</strong> ve <strong>AREA323</strong> olarak başlayan yolculuğumuz,
      aktif ve disiplinli yapımızla, <strong>ZZONE99</strong> adı altında PUBG Mobile arenasında varlığını sürdürüyor.
      Klanımız; rekabetçi, dost canlısı, takım ruhuna önem veren ve Türkiye'nin dört bir yanından oyuncuları bir araya getiriyor.
    </p>
    <p style="max-width: 720px; font-style: italic; color: var(--accent); margin-top: 10px;">
      "Takım olarak güçlüyüz, birlikte daha iyiyiz." - ZZONE99
    </p>
  </section>

  <!-- Başvuru -->
  <section id="basvuru" tabindex="0">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xldnljve" method="POST" aria-label="Klan başvuru formu">
      <label for="oyuncu">Oyuncu Adı ve UID</label>
      <input type="text" name="oyuncu" id="oyuncu" placeholder="Örn: mAzz99 #123456" required aria-required="true" />

      <label for="yas">Yaş</label>
      <input type="number" name="yas" id="yas" placeholder="Yaşınızı yazın" min="12" max="99" required aria-required="true" />

      <label for="aktiflik">Aktiflik</label>
      <select name="aktiflik" id="aktiflik" required aria-required="true">
        <option value="" disabled selected>Seçiniz</option>
        <option value="Günlük">Günlük</option>
        <option value="Haftalık">Haftalık</option>
        <option value="Ara sıra">Ara sıra</option>
      </select>

      <label for="cihaz">Kullandığı cihaz</label>
      <input type="text" name="cihaz" id="cihaz" placeholder="Örn: Android, iPhone" required aria-required="true" />

      <label for="iletisim_oyun">Oyun İçi İletişim
