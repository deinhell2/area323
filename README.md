
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AREA323</title>
  <style>
    /* Reset */
    * {margin:0; padding:0; box-sizing:border-box;}
    body {
      font-family: 'Poppins', sans-serif;
      color: #fff;
      overflow-x: hidden;
      background: linear-gradient(135deg, #0a0a1a, #1a1a3a, #0a0a1a);
      background-size: 400% 400%;
      animation: bgMove 20s ease infinite;
    }
    @keyframes bgMove {
      0%{background-position:0% 50%}
      50%{background-position:100% 50%}
      100%{background-position:0% 50%}
    }
    a{text-decoration:none;color:inherit}
    h1,h2,h3{margin-bottom:10px}
    section{padding:60px 20px;text-align:center}

    /* Preloader */
    #preloader {
      position:fixed;top:0;left:0;width:100%;height:100%;
      display:flex;align-items:center;justify-content:center;
      background:#000;z-index:1000;
    }
    #preloader img {width:120px; animation:spin 3s infinite linear;}
    @keyframes spin {100%{transform:rotate(360deg)}}

    /* Navbar */
    nav {
      position:fixed;top:0;left:0;width:100%;
      display:flex;justify-content:space-between;align-items:center;
      padding:15px 30px;background:rgba(0,0,0,0.6);
      z-index:999;
    }
    nav .logo {font-size:24px;font-weight:bold;color:#0ff;}
    nav ul {display:flex;gap:20px;list-style:none;}
    nav ul li a {transition:0.3s;}
    nav ul li a:hover {color:#0ff;}
    .burger {display:none;flex-direction:column;cursor:pointer;}
    .burger div {width:25px;height:3px;background:#fff;margin:4px;}

    @media(max-width:768px){
      nav ul {
        position:absolute;top:60px;right:-100%;
        flex-direction:column;background:#111;width:200px;padding:20px;
        transition:0.5s;
      }
      nav ul.active{right:0;}
      .burger{display:flex;}
    }

    /* Hero */
    #hero {height:100vh;display:flex;flex-direction:column;
      align-items:center;justify-content:center;}
    #slogan {font-size:40px;color:#0ff;text-shadow:0 0 20px #0ff;}
    .btn {
      margin-top:20px;padding:10px 20px;border:2px solid #0ff;
      color:#0ff;border-radius:8px;transition:0.3s;
    }
    .btn:hover {background:#0ff;color:#000;box-shadow:0 0 20px #0ff;}

    /* About */
    #about {background:rgba(255,255,255,0.05);border-radius:12px;margin:20px;}
    #about p{max-width:600px;margin:0 auto;line-height:1.6;}

    /* Leaders */
    .leader {margin:20px auto;padding:20px;max-width:400px;
      background:rgba(0,0,0,0.4);border-radius:12px;box-shadow:0 0 15px #0ff;}
    .leader h3{color:#0ff;}

    /* Form */
    form {max-width:400px;margin:0 auto;display:flex;flex-direction:column;gap:10px;}
    input,textarea {padding:10px;border:none;border-radius:6px;}
    button {padding:10px;border:none;border-radius:6px;background:#0ff;color:#000;cursor:pointer;transition:0.3s;}
    button:hover {background:#0cc;}

    /* TikTok */
    #tiktok a {font-size:20px;color:#fff;background:#ff0050;
      padding:10px 20px;border-radius:8px;transition:0.3s;}
    #tiktok a:hover {background:#fff;color:#ff0050;}

    /* Footer */
    footer {padding:20px;text-align:center;background:#000;color:#888;margin-top:40px;}

    /* Particles (background dots) */
    #particles {
      position:fixed;top:0;left:0;width:100%;height:100%;
      z-index:-1;overflow:hidden;
    }
    .dot {
      position:absolute;width:3px;height:3px;background:#0ff;border-radius:50%;
      animation:float 20s linear infinite;
    }
    @keyframes float {
      0% {transform:translateY(0);}
      100% {transform:translateY(-100vh);}
    }
  </style>
</head>
<body>
  <!-- Preloader -->
  <div id="preloader">
    <img src="logo.png" alt="logo">
  </div>

  <!-- Particles -->
  <div id="particles"></div>

  <!-- Navbar -->
  <nav>
    <div class="logo">AREA323</div>
    <ul>
      <li><a href="#hero">Ana Sayfa</a></li>
      <li><a href="#about">Hakkımızda</a></li>
      <li><a href="#leaders">Liderler</a></li>
      <li><a href="#apply">Başvuru</a></li>
      <li><a href="#tiktok">TikTok</a></li>
    </ul>
    <div class="burger">
      <div></div><div></div><div></div>
    </div>
  </nav>

  <!-- Hero -->
  <section id="hero">
    <h1 id="slogan">Für die Famillia</h1>
    <a href="#apply" class="btn">Klana Katıl</a>
  </section>

  <!-- About -->
  <section id="about">
    <h2>Hakkımızda</h2>
    <p>AREA323, 2018’den beri sahalarda olan, dayanışmayı ve aile ruhunu ön planda tutan bir PUBG Mobile klanıdır. 
    Amacımız hem rekabetçi alanda başarı göstermek hem de samimi bir topluluk oluşturmaktır.</p>
  </section>

  <!-- Leaders -->
  <section id="leaders">
    <h2>Liderler</h2>
    <div class="leader">
      <h3>EXILE323</h3>
      <p>ID: 516572604</p>
    </div>
  </section>

  <!-- Apply -->
  <section id="apply">
    <h2>Başvuru Formu</h2>
    <form action="https://formspree.io/f/xqalrayd" method="POST">
      <input type="text" name="uid" placeholder="Oyun UID" required>
      <input type="text" name="nick" placeholder="Oyun Nicki" required>
      <input type="text" name="isim" placeholder="İsim" required>
      <input type="number" name="yas" placeholder="Yaş" required>
      <input type="text" name="cihaz" placeholder="Cihaz" required>
      <input type="text" name="aktiflik" placeholder="Aktiflik (gün/saat)" required>
      <button type="submit">Gönder</button>
    </form>
  </section>

  <!-- TikTok -->
  <section id="tiktok">
    <h2>Bizi Takip Et</h2>
    <a href="https://www.tiktok.com/@exile323" target="_blank">@exile323</a>
  </section>

  <!-- Footer -->
  <footer>
    <p>Für die Famillia | SINCE 2018</p>
  </footer>

  <script>
    // Preloader
    window.addEventListener("load", ()=>{
      document.getElementById("preloader").style.display="none";
    });

    // Burger Menu
    const burger=document.querySelector('.burger');
    const navUL=document.querySelector('nav ul');
    burger.addEventListener('click', ()=> navUL.classList.toggle('active'));

    // Dynamic slogan
    const slogans=["Für die Famillia","SINCE 2018","AREA323"];
    let i=0;
    setInterval(()=>{
      document.getElementById("slogan").textContent=slogans[i];
      i=(i+1)%slogans.length;
    },4000);

    // Particles
    const particles=document.getElementById("particles");
    for(let i=0;i<50;i++){
      let dot=document.createElement("div");
      dot.className="dot";
      dot.style.left=Math.random()*100+"%";
      dot.style.top=Math.random()*100+"%";
      dot.style.animationDuration=(10+Math.random()*20)+"s";
      particles.appendChild(dot);
    }
  </script>
</body>
