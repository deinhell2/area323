
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AREA323</title>
  <style>
    /* Reset */
    * {margin:0;padding:0;box-sizing:border-box;}
    body {
      font-family: 'Poppins', sans-serif;
      color: #fff;
      background: #000;
      overflow-x: hidden;
    }

    /* Neon grid arkaplan */
    body::before {
      content:"";
      position:fixed;
      top:0;left:0;width:100%;height:100%;
      background:linear-gradient(45deg,rgba(0,255,255,.2) 25%,transparent 25%),
                 linear-gradient(-45deg,rgba(255,0,255,.2) 25%,transparent 25%);
      background-size:50px 50px;
      animation:movebg 10s linear infinite;
      z-index:-1;
    }
    @keyframes movebg {
      0%{background-position:0 0,0 0;}
      100%{background-position:100px 100px, -100px -100px;}
    }

    /* Giriş animasyonu */
    #loading {
      position:fixed;
      top:0;left:0;width:100%;height:100%;
      background:#000;
      display:flex;align-items:center;justify-content:center;
      flex-direction:column;
      z-index:9999;
    }
    #loading img {
      width:120px;
      animation:pop 1s ease forwards;
    }
    @keyframes pop {
      0%{opacity:0;transform:scale(0.5);}
      100%{opacity:1;transform:scale(1);}
    }

    /* Header */
    header {
      text-align:center;
      padding:30px 20px;
    }
    header h1 {
      font-size:2.5rem;
      letter-spacing:3px;
      color:#0ff;
      text-shadow:0 0 15px #0ff;
    }

    /* Orta logo + buton */
    .center {
      display:flex;
      flex-direction:column;
      align-items:center;
      margin-top:20px;
    }
    .center img {
      width:200px;
      margin-bottom:20px;
    }
    .glitch-btn {
      padding:15px 30px;
      font-size:1.2rem;
      color:#fff;
      background:transparent;
      border:2px solid #0ff;
      cursor:pointer;
      position:relative;
      overflow:hidden;
    }
    .glitch-btn::before {
      content:"";
      position:absolute;
      top:0;left:-100%;width:100%;height:100%;
      background:#0ff;
      transition:0.3s;
      z-index:-1;
    }
    .glitch-btn:hover::before {left:0;}
    .glitch-btn:hover {color:#000;}

    /* Liderler */
    section {
      padding:60px 20px;
      text-align:center;
    }
    .leaders {
      display:flex;
      justify-content:center;
      gap:40px;
      flex-wrap:wrap;
    }
    .leader {
      background:rgba(255,255,255,0.05);
      padding:20px;
      border-radius:15px;
      width:220px;
      box-shadow:0 0 20px rgba(0,255,255,0.3);
    }
    .leader img {width:100%;border-radius:15px;}
    .leader h3 {margin:10px 0 5px;font-size:1.3rem;}
    .leader p {font-size:0.9rem;color:#ccc;}
    .leader a img {width:25px;margin-top:10px;}

    /* Başvuru formu */
    form {
      max-width:500px;
      margin:0 auto;
      display:flex;
      flex-direction:column;
      gap:15px;
    }
    input, select {
      padding:12px;
      border:none;
      border-radius:8px;
      outline:none;
    }
    button[type=submit] {
      padding:12px;
      border:none;
      border-radius:8px;
      background:#0ff;
      font-weight:bold;
      cursor:pointer;
    }
    #success {
      display:none;
      text-align:center;
      margin-top:15px;
      color:#0f0;
      font-weight:bold;
      animation:fadein 1s;
    }
    @keyframes fadein {from{opacity:0;}to{opacity:1;}}

    /* Footer */
    footer {
      text-align:center;
      padding:20px;
      font-size:0.9rem;
      color:#888;
    }

    @media(max-width:768px){
      .leaders{flex-direction:column;align-items:center;}
    }
  </style>
</head>
<body>
  <!-- Loading -->
  <div id="loading">
    <img src="logo.png" alt="Logo">
  </div>

  <header>
    <h1>AREA323</h1>
  </header>

  <div class="center">
    <img src="logo.png" alt="Klan Logo">
    <a href="#form"><button class="glitch-btn">KLANA KATIL</button></a>
  </div>

  <!-- Liderler -->
  <section>
    <h2>Liderler</h2>
    <div class="leaders">
      <div class="leader">
        <img src="exile.png" alt="EXILE323">
        <h3>EXILE323</h3>
        <p>ID: 516572604</p>
        <a href="https://www.tiktok.com/@exile323" target="_blank">
          <img src="tiktok-logo.png" alt="TikTok">
        </a>
      </div>
      <div class="leader">
        <img src="exile.png" alt="BABAVIZYONDA">
        <h3>BABAVIZYONDA</h3>
        <p>@babavizyondapm</p>
        <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">
          <img src="tiktok-logo.png" alt="TikTok">
        </a>
      </div>
    </div>
  </section>

  <!-- Başvuru -->
  <section id="form">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xqalrayd" method="POST" id="applyForm">
      <input type="text" name="ad" placeholder="Adın" required>
      <input type="text" name="nick" placeholder="Oyun Nickin" required>
      <input type="number" name="fps" placeholder="FPS (örn. 90)" required>
      <input type="number" name="yas" placeholder="Yaşın" required>
      <input type="text" name="cihaz" placeholder="Cihazın" required>
      <input type="text" name="aktiflik" placeholder="Aktiflik (örn. Günlük)" required>
      <input type="text" name="tecrube" placeholder="PUBG Tecrüben" required>
      <button type="submit">Başvur</button>
    </form>
    <div id="success">✅ Başvurun başarıyla gönderildi!</div>
  </section>

  <footer>
    <p>Für die Famillia • SINCE 2018</p>
  </footer>

  <script>
    // Loading screen
    window.addEventListener("load", ()=>{
      setTimeout(()=>{
        document.getElementById("loading").style.display="none";
      },1500);
    });

    // Form başarı mesajı
    const form = document.getElementById("applyForm");
    form.addEventListener("submit", async function(e){
      e.preventDefault();
      const data = new FormData(form);
      const response = await fetch(form.action, {
        method: form.method,
        body: data,
        headers: {'Accept':'application/json'}
      });
      if (response.ok) {
        form.reset();
        document.getElementById("success").style.display="block";
      }
    });
  </script>
</body>
