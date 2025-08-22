
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AREA323</title>
<meta name="description" content="AREA323 PUBG Mobile Klanı - Strateji, disiplin ve dostluğu birleştiren elit ekip.">
<link rel="icon" type="image/png" href="logo.png">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Segoe UI',sans-serif;background:#0a0a0a;color:#fff;line-height:1.6;overflow-x:hidden;}
a{color:inherit;text-decoration:none;}
img{display:block;}

/* Particle Background */
#particles{position:fixed;top:0;left:0;width:100%;height:100%;z-index:0;pointer-events:none;}

/* Preloader */
#preloader{
  position:fixed;width:100%;height:100%;background:#0a0a0a;display:flex;justify-content:center;align-items:center;
  z-index:2000;animation:fadeOut 2s ease 3s forwards;
}
#preloader img{width:150px;animation:logoPulse 2s infinite alternate;}
@keyframes logoPulse{0%{transform:scale(1);}50%{transform:scale(1.15);}100%{transform:scale(1);}}
@keyframes fadeOut{to{opacity:0;visibility:hidden;}}

/* Navbar */
nav{position:sticky;top:0;z-index:1000;display:flex;justify-content:space-between;align-items:center;padding:1rem 2rem;background:rgba(10,10,10,0.85);backdrop-filter:blur(8px);transition:box-shadow 0.3s;}
nav.scrolled{box-shadow:0 4px 15px rgba(0,255,255,0.3);}
nav .logo{font-size:1.6rem;font-weight:bold;color:#00ffff;text-shadow:0 0 10px #00ffff;}
nav ul{list-style:none;display:flex;gap:1.5rem;}
nav ul li a{position:relative;font-weight:600;transition:color 0.3s;}
nav ul li a::after{content:'';position:absolute;bottom:-5px;left:0;width:0%;height:2px;background:#00ffff;transition:width 0.3s;}
nav ul li a:hover{color:#00ffff;}
nav ul li a:hover::after{width:100%;}

/* Burger Menü */
.burger{display:none;cursor:pointer;flex-direction:column;gap:5px;}
.burger div{width:25px;height:3px;background:#00ffff;}
@media(max-width:768px){nav ul{display:none;flex-direction:column;background:#141414;position:absolute;top:60px;right:20px;width:200px;border-radius:8px;padding:1rem;}nav ul.active{display:flex;}.burger{display:flex;}}

/* Bölümler */
section{padding:5rem 2rem;text-align:center;display:none;opacity:0;transform:translateY(50px);transition:all 0.6s ease;}
section.active{display:block;opacity:1;transform:translateY(0);}
section h2{font-size:2.2rem;margin-bottom:1rem;color:#00ffff;text-shadow:0 0 10px #00ffff;}
section p{max-width:700px;margin:auto;font-size:1.1rem;color:#ccc;}

/* Butonlar */
button,input[type=submit]{padding:12px 25px;border:none;border-radius:25px;background:linear-gradient(90deg,#00ffff,#0077ff);color:#0a0a0a;font-size:1rem;font-weight:bold;cursor:pointer;transition:all 0.4s ease;}
button:hover,input[type=submit]:hover{transform:scale(1.08);box-shadow:0 0 15px rgba(0,255,255,0.6);}

/* Form */
form{max-width:500px;margin:auto;display:flex;flex-direction:column;gap:1rem;}
input,textarea{padding:12px;border:2px solid #333;border-radius:8px;font-size:1rem;background:#141414;color:#fff;transition:all 0.3s ease;}
input:focus,textarea:focus{border-color:#00ffff;box-shadow:0 0 10px rgba(0,255,255,0.4);outline:none;}

/* Onay Mesajı */
#formMessage{display:none;margin-top:1rem;color:#00ffdd;font-weight:bold;animation:fadeIn 0.5s ease forwards;}
@keyframes fadeIn{from{opacity:0;}to{opacity:1;}}

/* İletişim */
.socials{display:flex;justify-content:center;gap:2rem;margin-top:1rem;}
.socials a{display:flex;align-items:center;gap:0.5rem;font-weight:bold;color:#ccc;transition:all 0.4s ease;}
.socials a:hover{transform:rotate(-5deg) scale(1.1);color:#00ffff;text-shadow:0 0 10px #00ffff;}
.socials img{width:28px;height:28px;}

/* Footer */
footer{background:#111;color:#00ffff;text-align:center;padding:1.5rem;margin-top:2rem;font-weight:bold;letter-spacing:1px;text-shadow:0 0 10px #00ffff,0 0 20px #0077ff;}

/* Smooth Scroll */
html{scroll-behavior:smooth;}
</style>
</head>
<body>

<!-- Particle Background -->
<canvas id="particles"></canvas>

<!-- Preloader -->
<div id="preloader">
  <img src="logo.png" alt="AREA323 Logo">
</div>

<!-- Navbar -->
<nav>
  <div class="logo">AREA323</div>
  <ul>
    <li><a href="#" data-section="tanitim">Klan Tanıtımı</a></li>
    <li><a href="#" data-section="basvuru">Klana Katıl</a></li>
    <li><a href="#" data-section="iletisim">İletişim</a></li>
  </ul>
  <div class="burger"><div></div><div></div><div></div></div>
</nav>

<!-- Klan Tanıtımı -->
<section id="tanitim">
  <h2>Klan Tanıtımı</h2>
  <p>AREA323, sadece bir klan değil bir aile. Strateji, disiplin ve dostluğu birleştirerek sahada fark yaratan elit PUBG Mobile ekibiyiz. Bizimle olan herkes bu hikayenin bir parçasıdır.</p>
</section>

<!-- Klana Katıl -->
<section id="basvuru">
  <h2>Klana Katıl</h2>
  <form id="applyForm" action="https://formspree.io/f/xqalrayd" method="POST">
    <input type="text" name="ad" placeholder="Adınız" required>
    <input type="text" name="nick" placeholder="Oyun Nickiniz" required>
    <input type="number" name="yas" placeholder="Yaşınız" required>
    <input type="text" name="uid" placeholder="UID" required>
    <input type="text" name="cihaz" placeholder="Cihazınız" required>
    <input type="text" name="aktiflik" placeholder="Aktiflik Durumunuz" required>
    <input type="submit" value="Başvur">
  </form>
  <div id="formMessage">Başvurunuz alındı! ✅</div>
</section>

<!-- İletişim -->
<section id="iletisim">
  <h2>İletişim</h2>
  <div class="socials">
    <a href="https://www.tiktok.com/@exile323" target="_blank">
      <img src="tictoc-icon.png" alt="TikTok"> @exile323
    </a>
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">
      <img src="tictoc-icon.png" alt="TikTok"> @babavizyondapm
    </a>
  </div>
</section>

<!-- Footer -->
<footer>AREA323 – Since 2018</footer>

<script>
// Burger Menü
const burger=document.querySelector('.burger');
const navLinks=document.querySelector('nav ul');
burger.addEventListener('click',()=>{navLinks.classList.toggle('active');});

// Navbar scroll efekti
window.addEventListener("scroll",()=>{document.querySelector("nav").classList.toggle("scrolled",window.scrollY>50);});

// Bölümleri gösterme
const links=document.querySelectorAll('nav ul li a');
links.forEach(link=>{
  link.addEventListener('click',e=>{
    e.preventDefault();
    const sectionId=link.dataset.section;
    document.querySelectorAll('section').forEach(sec=>sec.classList.remove('active'));
    const sec=document.getElementById(sectionId);
    sec.classList.add('active');
    sec.scrollIntoView({behavior:"smooth"});});
});

/q/ Form onay mesajı
const form=document.getElementById('applyForm');
const message=document.getElementById('formMessage');
form.addEventListener('submit',e=>{
  e.preventDefault();
  fetch(form.action,{method:'POST',body:new FormData(form)})
    .then(()=>{
      message.style.display='block';
      form.reset();
      setTimeout(()=>{message.style.display='none';},4000);
    })
    .catch(()=>{alert('Başvuru gönderilemedi, tekrar deneyin');});
});

// Particle Arka Plan
const canvas=document.getElementById('particles');
const ctx=canvas.getContext('2d');
let w=canvas.width=window.innerWidth;
let h=canvas.height=window.innerHeight;
window.addEventListener('resize',()=>{w=canvas.width=window.innerWidth; h=canvas.height=window.innerHeight;});
let particlesArray=[];
class Particle{
  constructor(){
    this.x=Math.random()*w;
    this.y=Math.random()*h;
    this.size=Math.random()*3+1;
    this.speedX=(Math.random()-0.5)*0.5;
    this.speedY=(Math.random()-0.5)*0.5;
  }
  update(){
    this.x+=this.speedX; this.y+=this.speedY;
    if(this.x>w)this.x=0; if(this.x<0)this.x=w;
    if(this.y>h)this.y=0; if(this.y<0)this.y=h;
  }
  draw(){
    ctx.fillStyle='rgba(0,255,255,0.6)';
    ctx.beginPath();
    ctx.arc(this.x,this.y,this.size,0,Math.PI*2);
    ctx.fill();
  }
}
function init(){particlesArray=[];for(let i=0;i<120;i++){particlesArray.push(new Particle());}}
function animate(){ctx.clearRect(0,0,w,h);particlesArray.forEach(p=>{p.update();p.draw();});requestAnimationFrame(animate);}
init();animate();
</script>
</body>
