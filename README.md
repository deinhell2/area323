<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AREA323</title>
  <style>
    /* Genel Reset */
    * {margin: 0; padding: 0; box-sizing: border-box; font-family: 'Arial Black', sans-serif;}

    body {
      background: black;
      color: white;
      overflow-x: hidden;
      text-align: center;
    }

    /* Hareketli Neon Grid */
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: url('logo.png') center/30% no-repeat, 
                  repeating-linear-gradient(90deg, rgba(0,255,255,0.1) 0 2px, transparent 2px 40px),
                  repeating-linear-gradient(0deg, rgba(255,0,255,0.1) 0 2px, transparent 2px 40px);
      z-index: -1;
      animation: moveGrid 10s linear infinite;
    }
    @keyframes moveGrid {
      0% {background-position: 0 0, 0 0, 0 0;}
      100% {background-position: 100px 100px, 40px 0, 0 40px;}
    }

    /* Loading Screen */
    #loading {
      position: fixed;
      top:0; left:0; right:0; bottom:0;
      background:black;
      display:flex; justify-content:center; align-items:center;
      z-index:9999;
    }
    #loading img {width: 200px; animation: pulse 1.5s infinite;}
    @keyframes pulse {0%,100%{opacity:0.3;}50%{opacity:1;}}

    /* Navbar */
    nav {
      width:100%;
      padding:15px 30px;
      display:flex;
      justify-content:space-between;
      align-items:center;
      background:rgba(0,0,0,0.7);
      position:fixed;
      top:0;
      z-index:1000;
    }
    nav h1 {font-size: 1.5rem; color: cyan;}
    nav ul {display:flex; gap:20px; list-style:none;}
    nav ul li a {color:white; text-decoration:none; transition:0.3s;}
    nav ul li a:hover {color:cyan; text-shadow:0 0 10px cyan;}

    /* Burger Menü */
    .burger {display:none; flex-direction:column; cursor:pointer;}
    .burger div {width:25px; height:3px; background:white; margin:5px; transition:0.3s;}
    @media (max-width:768px) {
      nav ul {display:none; flex-direction:column; background:black; position:absolute; top:60px; right:0; width:200px; text-align:right; padding:10px;}
      nav ul.active {display:flex;}
      .burger {display:flex;}
    }

    /* Hero */
    .hero {
      height:100vh;
      display:flex;
      flex-direction:column;
      justify-content:center;
      align-items:center;
      gap:20px;
    }
    .hero img {width:220px;}
    .glitch-btn {
      font-size:1.2rem;
      padding:15px 30px;
      border:none;
      color:white;
      background:black;
      border:2px solid cyan;
      cursor:pointer;
      position:relative;
      overflow:hidden;
    }
    .glitch-btn::before, .glitch-btn::after {
      content:"KLANA KATIL";
      position:absolute;
      left:0; top:0;
      width:100%; height:100%;
      background:black;
      color:magenta;
      overflow:hidden;
      clip:rect(0,900px,0,0);
    }
    .glitch-btn:hover::before {
      animation:glitchTop 1s infinite;
    }
    .glitch-btn:hover::after {
      color:cyan;
      animation:glitchBot 1s infinite;
    }
    @keyframes glitchTop {
      0%{clip:rect(0,900px,0,0);}
      50%{clip:rect(0,900px,60px,0);}
      100%{clip:rect(0,900px,0,0);}
    }
    @keyframes glitchBot {
      0%{clip:rect(0,900px,0,0);}
      50%{clip:rect(60px,900px,900px,0);}
      100%{clip:rect(0,900px,0,0);}
    }

    /* Slogan */
    #slogan {font-size:1.5rem; color:magenta; text-shadow:0 0 10px cyan;}

    /* Popup */
    .popup {
      position:fixed;
      top:50%; left:50%;
      transform:translate(-50%,-50%);
      background:black;
      border:2px solid cyan;
      padding:20px;
      display:none;
      flex-direction:column;
      gap:15px;
      z-index:2000;
      width:300px;
      border-radius:10px;
    }
    .popup h2 {color:cyan; font-size:1.3rem;}
    .popup .leader {display:flex; align-items:center; gap:10px;}
    .popup img {width:50px; border-radius:50%;}
    .close {cursor:pointer; color:red;}

    /* Footer */
    footer {
      background:black;
      padding:20px;
      border-top:2px solid cyan;
      margin-top:50px;
    }
    footer p {color:gray; font-size:0.9rem;}
  </style>
</head>
<body>
  <!-- Loading -->
  <div id="loading"><img src="logo.png" alt="logo"></div>

  <!-- Navbar -->
  <nav>
    <h1>AREA323</h1>
    <ul>
      <li><a href="#hero">Ana Sayfa</a></li>
      <li><a href="#" onclick="togglePopup()">Liderler</a></li>
      <li><a href="https://formspree.io/f/xqalrayd" target="_blank">Başvuru</a></li>
    </ul>
    <div class="burger" onclick="toggleMenu()">
      <div></div><div></div><div></div>
    </div>
  </nav>

  <!-- Hero -->
  <section class="hero" id="hero">
    <img src="logo.png" alt="AREA323 Logo">
    <button class="glitch-btn" onclick="location.href='https://formspree.io/f/xqalrayd'">KLANA KATIL</button>
    <p id="slogan">Für die Famillia</p>
  </section>

  <!-- Popup Liderler -->
  <div class="popup" id="popup">
    <span class="close" onclick="togglePopup()">Kapat ✖</span>
    <h2>Liderler</h2>
    <div class="leader">
      <img src="exile.png" alt="EXILE323">
      <div>
        <p>EXILE323</p>
        <p>ID: 516572604</p>
        <p>TikTok: exile323</p>
      </div>
    </div>
    <div class="leader">
      <img src="exile.png" alt="BABAVIZYONDA">
      <div>
        <p>BABAVIZYONDA</p>
        <p>TikTok: babavizyondapm</p>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer>
    <p>Für die Famillia | SINCE 2018</p>
  </footer>

  <script>
    // Loading
    window.onload = () => {
      setTimeout(()=>{document.getElementById('loading').style.display='none';},1500);
    };

    // Burger Menü
    function toggleMenu(){
      document.querySelector('nav ul').classList.toggle('active');
    }

    // Popup
    function togglePopup(){
      const p = document.getElementById('popup');
      p.style.display = p.style.display === 'flex' ? 'none' : 'flex';
    }

    // Dinamik slogan
    const slogans = ["Für die Famillia","Zafer Bizim","AREA323 Her Yerde"];
    let i=0;
    setInterval(()=>{
      i=(i+1)%slogans.length;
      document.getElementById("slogan").innerText=slogans[i];
    },3000);
  </script>
</body>
</html>
