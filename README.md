<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>AREA323</title>
  <meta name="theme-color" content="#0a0a0a" />
  <style>
    :root{
      --bg:#0a0a0a;--card:#111;--txt:#fff;--muted:#9aa1a6;--primary:#ff003c;--accent:#00e6ff;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;background:var(--bg);color:var(--txt);font-family:"Segoe UI",system-ui,Arial,sans-serif;scroll-behavior:smooth}
    a{color:var(--accent);text-decoration:none}/* === Loading (Preloader) === */
#loading{position:fixed;inset:0;background:#000;display:flex;align-items:center;justify-content:center;z-index:9999}
#loading .pulse{width:140px;height:140px;border-radius:20px;display:flex;align-items:center;justify-content:center;background:#0f0f0f;box-shadow:0 0 40px rgba(255,0,60,.3);animation:floaty 2.2s ease-in-out infinite}
#loading .pulse img{width:110px;filter:drop-shadow(0 0 18px var(--primary))}
@keyframes floaty{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}

/* === Navbar + Burger === */
nav{position:fixed;top:0;left:0;right:0;z-index:1000;background:rgba(0,0,0,.75);backdrop-filter:blur(6px);border-bottom:1px solid rgba(255,255,255,.06)}
.nav-inner{max-width:1100px;margin:auto;display:flex;align-items:center;justify-content:space-between;padding:12px 16px}
.brand{display:flex;align-items:center;gap:10px;font-weight:800;letter-spacing:.5px;color:var(--primary)}
.brand img{width:30px;height:30px;filter:drop-shadow(0 0 8px var(--primary))}
ul.menu{list-style:none;display:flex;gap:18px;margin:0;padding:0}
ul.menu a{color:#fff;opacity:.9}
ul.menu a:hover{color:var(--primary)}
.burger{display:none;flex-direction:column;gap:5px;cursor:pointer}
.burger span{width:26px;height:3px;background:#fff;transition:.3s}
@media(max-width:840px){ul.menu{display:none;position:absolute;right:12px;top:56px;background:#0d0d0d;border:1px solid rgba(255,255,255,.06);border-radius:12px;flex-direction:column;padding:10px;width:200px}
  ul.menu.open{display:flex}
  .burger{display:flex}
}

/* === Background subtle motion === */
.bg-animation{position:fixed;inset:0;z-index:-1;background:url('https://www.transparenttextures.com/patterns/dark-matter.png');animation:movebg 60s linear infinite}
@keyframes movebg{from{background-position:0 0}to{background-position:1000px 1000px}}

/* === Hero === */
.hero{min-height:100vh;display:grid;place-items:center;padding-top:80px;text-align:center;background:radial-gradient(60% 60% at 50% 30%,#1a1a1a 0%,#000 100%)}
.hero-inner{display:flex;flex-direction:column;align-items:center;gap:16px;animation:fadeIn 1s}
.hero-inner img{width:210px;filter:drop-shadow(0 0 20px var(--primary))}
.title{font-size:40px;text-shadow:0 0 10px var(--primary)}
.subtitle{opacity:.8}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}

/* === Sections / Page transition feel === */
main{opacity:0;transition:opacity .5s ease}
main.ready{opacity:1}
section{padding:80px 16px}
.container{max-width:1100px;margin:auto}
.card{background:var(--card);border:1px solid rgba(255,255,255,.06);border-radius:16px;padding:20px}

/* === Neon buttons === */
.btn{display:inline-block;padding:12px 18px;border:2px solid var(--primary);color:var(--primary);font-weight:700;text-transform:uppercase;border-radius:12px;transition:.25s;letter-spacing:.5px}
.btn:hover{background:var(--primary);color:#fff;box-shadow:0 0 16px var(--primary),0 0 36px var(--primary)}

/* === Grid helpers === */
.grid{display:grid;gap:16px}
.grid-2{grid-template-columns:1fr 1fr}
@media(max-width:840px){.grid-2{grid-template-columns:1fr}}

/* === Forms === */
form{display:flex;flex-direction:column;gap:12px}
input,textarea,select{padding:12px;border-radius:10px;border:1px solid rgba(255,255,255,.08);background:#0c0c0c;color:#fff}
label{font-size:14px;color:var(--muted)}

/* === Footer === */
footer{background:#0d0d0d;border-top:1px solid rgba(255,255,255,.06);padding:24px;text-align:center;color:#9aa1a6}

  </style>
</head>
<body>
  <!-- Preloader -->
  <div id="loading" aria-label="Loading">
    <div class="pulse"><img src="logo.png" alt="AREA323 Logo" /></div>
  </div>  <!-- BG effect -->  <div class="bg-animation" aria-hidden="true"></div>  <!-- Navbar -->  <nav>
    <div class="nav-inner">
      <div class="brand"><img src="logo.png" alt="A"/>AREA323</div>
      <div class="burger" id="burger" aria-label="Menüyü aç/kapat" aria-expanded="false"><span></span><span></span><span></span></div>
      <ul class="menu" id="menu">
        <li><a href="#hero">Ana Sayfa</a></li>
        <li><a href="#about">Hakkımızda</a></li>
        <li><a href="#leaders">Liderler</a></li>
        <li><a href="#apply">Başvuru</a></li>
        <li><a href="#tracker">Takip</a></li>
        <li><a href="#contact">İletişim</a></li>
      </ul>
    </div>
  </nav>  <!-- Hero -->  <header id="hero" class="hero">
    <div class="hero-inner">
      <img src="logo.png" alt="AREA323" />
      <h1 class="title">Für die Famillia</h1>
      <p class="subtitle">SINCE 2018 • Beyond Limits</p>
      <div>
        <a class="btn" href="#apply">Klan Başvurusu</a>
        <a class="btn" href="#tracker">Başvuru Takip</a>
      </div>
    </div>
  </header>  <main id="main">
    <!-- Hakkımızda -->
    <section id="about">
      <div class="container grid grid-2">
        <div class="card">
          <h2>Hakkımızda</h2>
          <p>AREA323, sadece bir klan değil bir aile. 2018’den beri PUBG Mobile sahnesinde aktif olan ekibimiz, disiplin, dostluk ve rekabeti aynı potada eritiyor. Amacımız birlikte büyümek, sahnede en iyiler arasında yer almak ve her maçta takım ruhunu hissettirmek.</p>
        </div>
        <div class="card">
          <h3>Değerlerimiz</h3>
          <ul>
            <li>Takım Ruhu ve Saygı</li>
            <li>Sürekli Gelişim</li>
            <li>Rekabet ve Eğlence Dengesi</li>
          </ul>
        </div>
      </div>
    </section><!-- Liderler -->
<section id="leaders">
  <div class="container">
    <div class="card">
      <h2>Liderler</h2>
      <div class="grid grid-2" style="margin-top:12px">
        <div class="card">
          <h3>EXILE323</h3>
          <p><strong>ID:</strong> 516572604</p>
        </div>
        <div class="card">
          <h3>Yakında</h3>
          <p>Yeni lider veya moderatör eklenecek.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Başvuru Formu (Formspree) -->
<section id="apply">
  <div class="container">
    <div class="card">
      <h2>Klan Başvurusu</h2>
      <form action="https://formspree.io/f/xqalrayd" method="POST">
        <label>UID
          <input name="uid" type="text" placeholder="Oyun UID" required />
        </label>
        <label>Oyun Nicki
          <input name="nick" type="text" placeholder="Nick" required />
        </label>
        <label>Yaş
          <input name="age" type="number" min="10" max="80" placeholder="18" required />
        </label>
        <label>Cihaz
          <input name="device" type="text" placeholder="iOS / Android / Model" />
        </label>
        <label>Aktiflik
          <select name="activity">
            <option value="gunluk">Günlük</option>
            <option value="haftalik">Haftalık</option>
            <option value="degisken">Değişken</option>
          </select>
        </label>
        <label>Not
          <textarea name="note" rows="3" placeholder="Eklemek istediğin bir şey var mı?"></textarea>
        </label>
        <button class="btn" type="submit">Gönder</button>
      </form>
    </div>
  </div>
</section>

<!-- Başvuru Takip Sistemi (Mock) -->
<section id="tracker">
  <div class="container">
    <div class="card">
      <h2>Başvuru Takip</h2>
      <p>Başvuru yaptıktan sonra aşağıya UID veya ID girerek durumunu kontrol edebilirsin.</p>
      <form id="trackForm" onsubmit="return false;">
        <label>UID / ID
          <input id="trackId" type="text" placeholder="Örn: 516572604" required />
        </label>
        <button class="btn" id="trackBtn">Durumu Sorgula</button>
      </form>
      <div id="trackResult" style="margin-top:12px;color:#cbd5e1"></div>
    </div>
  </div>
</section>

<!-- İletişim / Sosyal -->
<section id="contact">
  <div class="container grid grid-2">
    <div class="card">
      <h2>İletişim</h2>
      <p>İşbirliği ve takım başvuruları için bize sosyal medya üzerinden ulaşabilirsin.</p>
      <p><strong>TikTok:</strong> <a href="https://www.tiktok.com/@exile323" target="_blank" rel="noopener">@exile323</a></p>
    </div>
    <div class="card">
      <h3>Duyuru</h3>
      <p>Başvurular **açıktır**. Formu doldurduktan sonra Takip bölümünden durumunu sorgulayabilirsin.</p>
    </div>
  </div>
</section>

  </main>  <footer>
    Für die Famillia | SINCE 2018
  </footer>  <script>
    // Preloader -> hide when ready
    window.addEventListener('load',()=>{
      document.getElementById('loading').style.display='none';
      document.getElementById('main').classList.add('ready');
    });

    // Burger menu
    const burger=document.getElementById('burger');
    const menu=document.getElementById('menu');
    burger?.addEventListener('click',()=>{
      const isOpen=menu.classList.toggle('open');
      burger.setAttribute('aria-expanded',isOpen?'true':'false');
    });

    // Simple page-transition feel (fade on anchor click)
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click',()=>{
        const main=document.getElementById('main');
        main.classList.remove('ready');
        setTimeout(()=>main.classList.add('ready'),250);
      })
    });

    // Tracker mock logic
    const mockStatuses={
      '516572604':{status:'Onaylandı ✅',note:'Lider ID'},
      '123456789':{status:'Beklemede ⏳',note:'Değerlendirme sürecinde'},
      '987654321':{status:'Reddedildi ❌',note:'Kriterleri karşılamıyor'}
    };
    const trackBtn=document.getElementById('trackBtn');
    const trackId=document.getElementById('trackId');
    const trackResult=document.getElementById('trackResult');
    trackBtn?.addEventListener('click',()=>{
      const key=(trackId.value||'').trim();
      if(!key){trackResult.textContent='Lütfen bir UID/ID gir.';return}
      const data=mockStatuses[key];
      trackResult.innerHTML=data?`<strong>Durum:</strong> ${data.status}<br/><small>${data.note}</small>`:`<strong>Durum:</strong> Beklemede ⏳<br/><small>Kayıt bulunamadıysa başvurun yeni düşmüş olabilir.</small>`;
    });
  </script></body>
