<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ZZONE99 PUBG MOBILE KLANI</title>
  <style>
    /* Reset & Temel */
    * { margin:0; padding:0; box-sizing:border-box; font-family:'Segoe UI',sans-serif; }
    body {
      position: relative;
      background: #0e1217;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }
    body::before {
      content:"";
      position:fixed;
      top:-50%; left:-50%;
      width:200%; height:200%;
      background:radial-gradient(circle at center,#264b6c,transparent 70%);
      filter:blur(150px);
      z-index:0;
    }
    img { max-width:100%; display:block; }

    /* Preloader (Giriş Animasyonu) */
    #preloader {
      position:fixed;
      inset:0;
      background:#0e1217;
      z-index:9999;
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      text-align:center;
    }
    #preloader img {
      width:140px;
      filter:drop-shadow(0 0 20px #00fffa);
      animation:grow-logo 2s ease forwards;
    }
    #preloader h1 {
      margin-top:15px;
      font-size:3rem;
      color:#00fffa;
      text-shadow:0 0 15px #00fffa;
      animation:fadeText 2s ease forwards;
    }
    #preloader p {
      margin-top: 8px;
      font-size:1.1rem;
      color:#9ae7fa;
      text-shadow:0 0 8px #0099aa;
      opacity:0;
      animation:fadeText 2s ease forwards 0.5s;
    }
    @keyframes grow-logo {
      from { transform:scale(0.5); opacity:0; }
      to { transform:scale(1); opacity:1; }
    }
    @keyframes fadeText {
      from { opacity:0; }
      to { opacity:1; }
    }
    .fade-away {
      animation:fade-out 1s ease forwards;
    }
    @keyframes fade-out { to { opacity:0; visibility:hidden; } }

    /* Header */
    header {
      position:relative;
      z-index:1;
      padding:20px 0;
      text-align:center;
    }
    header img {
      width:80px;
      filter:drop-shadow(0 0 10px #00fffa);
    }
    header h2 {
      margin-top:12px;
      font-size:2.5rem;
      color:#00fffa;
      text-shadow:0 0 10px #00fffa;
    }

    /* Ana Bölümler */
    main {
      position:relative; z-index:1;
      max-width:900px;
      margin:50px auto 60px;
      padding:0 20px;
    }
    section { margin-bottom:60px; }
    h3.section-title {
      font-size:2rem;
      color:#00fffa;
      margin-bottom:25px;
      text-align:center;
      text-shadow:0 0 10px #00fffa;
    }

    #description { 
      background:rgba(0,116,217,0.15);
      border-radius:10px;
      padding:20px;
      color:#d0e9ff;
      line-height:1.6;
      text-align:justify;
      box-shadow:0 0 12px #0074D9;
    }

    #leaders {
      display:flex;
      justify-content:center;
      flex-wrap:wrap;
      gap:40px;
    }
    .leader-card {
      width:180px;
      background:rgba(0,116,217,0.2);
      border-radius:12px;
      padding:15px;
      box-shadow:0 0 15px #00fffa;
      text-align:center;
      transition:transform 0.3s ease;
    }
    .leader-card:hover {
      transform:scale(1.05);
      box-shadow:0 0 25px #00fffa;
    }
    .leader-card img {
      width:100px;
      height:100px;
      margin-bottom:12px;
      border-radius:50%;
      filter:drop-shadow(0 0 5px #00fffa);
    }
    .leader-card .nick {
      font-size:1.3rem;
      color:#00fffa;
      font-weight:bold;
      text-shadow:0 0 8px #00fffa;
    }
    .leader-card .id {
      font-size:0.9rem;
      color:#9ae7fa;
      margin-top:5px;
    }

    /* Buton */
    .btn-katil {
      display:block;
      margin:30px auto;
      padding:12px 30px;
      font-size:1.2rem;
      font-weight:700;
      background:#00fffa;
      color:#001522;
      border:none;
      border-radius:40px;
      cursor:pointer;
      box-shadow:0 0 15px #00fffa;
      transition:background 0.3s ease,transform .2s ease;
    }
    .btn-katil:hover {
      background:#00ccdd;
      transform:scale(1.05);
    }

    /* İletişim */
    .tiktok-links {
      display:flex;
      justify-content:center;
      gap:30px;
      flex-wrap:wrap;
    }
    .tiktok-links a {
      display:flex;
      align-items:center;
      gap:8px;
      color:#00fffa;
      font-size:1.1rem;
      font-weight:600;
      text-decoration:none;
      transition:color 0.3s ease;
    }
    .tiktok-links a:hover { color:#9ae7fa; }
    .tiktok-links img {
      width:28px;
      filter:drop-shadow(0 0 5px #00fffa);
    }

    /* Başvuru Formu */
    .form-wrapper {
      max-width:400px;
      margin:0 auto;
      text-align:center;
    }
    .form-wrapper form {
      display:flex;
      flex-direction:column;
      gap:12px;
    }
    .form-wrapper input, .form-wrapper select {
      padding:10px;
      font-size:1rem;
      border:none;
      border-radius:6px;
      outline:none;
    }
    .form-wrapper button[type=submit] {
      margin-top:10px;
      padding:12px;
      font-size:1.1rem;
      font-weight:700;
      background:#00fffa;
      color:#001522;
      border:none;
      border-radius:30px;
      cursor:pointer;
      box-shadow:0 0 10px #00fffa;
      transition:background 0.3s ease;
    }
    .form-wrapper button[type=submit]:hover {
      background:#00ccdd;
    }
    .message {
      margin-top:10px;
      font-size:1rem;
      font-weight:600;
      color:#9ae7fa;
    }

    /* Footer Marquee */
    footer {
      position:fixed;
      bottom:0; left:0;
      width:100%;
      background:#001522;
      overflow:hidden;
      z-index:1;
      box-shadow:0 -2px 10px #00fffa;
    }
    .marquee {
      display:flex;
      gap:50px;
      animation:marquee 15s linear infinite;
      align-items:center;
      white-space:nowrap;
      padding:10px 0;
    }
    .marquee img {
      width:30px;
      filter:drop-shadow(0 0 5px #00fffa);
    }
    .marquee span {
      font-size:1.2rem;
      font-weight:bold;
      color:#00fffa;
      text-shadow:0 0 10px #00fffa;
    }
    @keyframes marquee {
      from { transform:translateX(100%); }
      to { transform:translateX(-100%); }
    }

    /* Responsive */
    @media(max-width:600px){
      #leaders { gap:20px; }
      .leader-card { width:140px; padding:12px; }
      .leader-card img { width:80px; height:80px; }
      .btn-katil { font-size:1rem; padding:10px 25px; }
    }
  </style>
</head>
<body>

<!-- Preloader -->
<div id="preloader">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
  <p>NE DENGEMİZ NE DENGİMİZ VAR ZZONE99 MARKA</p>
</div>

<header>
  <img src="logo.png" alt="logo" />
  <h2>ZZONE99</h2>
</header>

<main>
  <section id="description">
    <h3 class="section-title">Klan Hakkında</h3>
    <p>İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında...
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam ediyoruz. Hedefimiz sadece oyun kazanmak değil, kaliteli ve kalıcı bir topluluk oluşturmak.</p>
  </section>

  <section id="leaders">
    <h3 class="section-title">Liderler</h3>
    <div class="leader-card"><img src="mazz.png" alt="mAzz99" /><div class="nick">mAzz99</div><div class="id">ID: 516572604</div></div>
    <div class="leader-card"><img src="yazz.png" alt="yAzz99" /><div class="nick">yAzz99</div><div class="id">ID: 520654025</div></div>
  </section>

  <button class="btn-katil" onclick="document.getElementById('basvuru').scrollIntoView()">KLANA KATIL</button>

  <section id="contact">
    <h3 class="section-title">İletişim</h3>
    <div class="tiktok-links">
      <a href="https://www.tiktok.com/@mazz99theboss" target="_blank"><img src="tiktok-icon.png" alt="" />@mazz99theboss</a>
      <a href="https://www.tiktok.com/@babavizyondapm" target="_blank"><img src="tiktok-icon.png" alt="" />@babavizyondapm</a>
    </div>
  </section>

  <section id="basvuru" class="form-wrapper">
    <h3 class="section-title">Başvuru Formu</h3>
    <form id="frm" action="https://formspree.io/f/xldnljve" method="POST">
      <input type="text" name="UID" placeholder="UID" required />
      <input type="text" name="Oyun_Ismi" placeholder="Oyun İsmi" required />
      <input type="text" name="İsim" placeholder="İsim" required />
      <input type="number" name="Yaş" placeholder="Yaş" required min="10" max="99" />
      <select name="Cihaz" required>
        <option value="">Cihaz</option>
        <option>Android</option>
        <option>iOS</option>
      </select>
      <select name="Aktiflik" required>
        <option value="">Aktiflik</option>
        <option>Günlük</option>
        <option>Haftalık</option>
        <option>Aylık</option>
      </select>
      <button type="submit">Gönder</button>
    </form>
    <div class="message" id="msg"></div>
  </section>
</main>

<footer>
  <div class="marquee">
    <img src="logo.png" alt="" /><span>NE DENGEMİZ NE DENGİMİZ VAR ZZONE99 MARKA</span>
    <img src="logo.png" alt="" /><span>NE DENGEMİZ NE DENGİMİZ VAR ZZONE99 MARKA</span>
  </div>
</footer>

<script>
  window.addEventListener('load',()=>{
    setTimeout(()=>{
      document.getElementById('preloader').classList.add('fade-away');
    },2000);
  });

  // Formspree AJAX
  const form=document.getElementById('frm'),
        msg=document.getElementById('msg');
  form.addEventListener('submit',e=>{
    e.preventDefault();
    const data=new FormData(form);
    fetch(form.action,{method:'POST',body:data,headers:{Accept:'application/json'}})
    .then(res=>{
      if(res.ok){
        msg.textContent='Başvurunuz alınmıştır, teşekkürler!';
        form.reset();
      } else res.json().then(d=>{
        msg.textContent=(d.errors||[]).map(er=>er.message).join(', ')||'Hata!';
      });
    }).catch(()=>msg.textContent='Bağlantı hatası!');
  });
</script>
</body>

