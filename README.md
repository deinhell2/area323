
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AREA323</title>
<link rel="icon" type="image/png" href="logo.png">
<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Segoe UI',sans-serif;background:#0a0a0a;color:#fff;overflow-x:hidden;position:relative;}
a{text-decoration:none;color:inherit;}
#particles{position:fixed;top:0;left:0;width:100%;height:100%;z-index:0;pointer-events:none;}
#progressBar{position:fixed;top:0;left:0;height:4px;background:#00ffff;width:0%;z-index:1500;box-shadow:0 0 10px #00ffff;}
#hero{width:100vw;height:100vh;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;position:relative;z-index:1;}
#hero img{width:200px;animation:pulse 2s infinite alternate;}
@keyframes pulse{0%{transform:scale(1);}50%{transform:scale(1.15);}100%{transform:scale(1);}}
#hero .buttons{margin-top:3rem;display:flex;flex-direction:column;gap:1.5rem;}
#hero .buttons button{padding:15px 40px;border:none;border-radius:30px;background:linear-gradient(90deg,#00ffff,#0077ff);color:#0a0a0a;font-size:1.2rem;font-weight:bold;cursor:pointer;transition:all 0.4s ease;}
#hero .buttons button:hover{transform:scale(1.08);box-shadow:0 0 20px rgba(0,255,255,0.6);}
section{padding:5rem 2rem;text-align:center;display:none;opacity:0;transform:translateY(50px);transition:all 0.6s ease;z-index:1;position:relative;}
section.active{display:block;opacity:1;transform:translateY(0);}
section h2{font-size:2.2rem;margin-bottom:1rem;color:#00ffff;text-shadow:0 0 10px #00ffff;}
section p{max-width:700px;margin:auto;font-size:1.1rem;color:#ccc;}
form{max-width:500px;margin:auto;display:flex;flex-direction:column;gap:1rem;}
input,textarea{padding:12px;border:2px solid #333;border-radius:8px;font-size:1rem;background:#141414;color:#fff;transition:all 0.3s ease;}
input:focus,textarea:focus{border-color:#00ffff;box-shadow:0 0 10px rgba(0,255,255,0.4);outline:none;}
input[type=submit]{background:linear-gradient(90deg,#00ffff,#0077ff);color:#0a0a0a;font-weight:bold;cursor:pointer;transition:all 0.4s ease;}
input[type=submit]:hover{transform:scale(1.08);box-shadow:0 0 15px rgba(0,255,255,0.6);}
#formMessage{display:none;margin-top:1rem;color:#00ffdd;font-weight:bold;animation:fadeIn 0.5s ease forwards;}
@keyframes fadeIn{from{opacity:0;}to{opacity:1;}}
.socials{display:flex;justify-content:center;gap:2rem;margin-top:1rem;}
.socials a{display:flex;align-items:center;gap:0.5rem;font-weight:bold;color:#ccc;transition:all 0.4s ease;position:relative;}
.socials a:hover{transform:rotate(-5deg) scale(1.1);color:#00ffff;text-shadow:0 0 10px #00ffff;}
.socials a span{position:absolute;bottom:150%;left:50%;transform:translateX(-50%);background:#00ffff;color:#0a0a0a;padding:3px 7px;border-radius:4px;font-size:0.75rem;opacity:0;pointer-events:none;transition:opacity 0.3s;}
.socials a:hover span{opacity:1;}
.socials img{width:28px;height:28px;}
footer{background:#111;color:#00ffff;text-align:center;padding:1.5rem;margin-top:2rem;font-weight:bold;letter-spacing:1px;text-shadow:0 0 10px #00ffff,0 0 20px #0077ff;}
#backTop{position:fixed;bottom:30px;right:30px;padding:10px 15px;background:#00ffff;color:#0a0a0a;border:none;border-radius:50%;cursor:pointer;display:none;box-shadow:0 0 15px #00ffff;transition:all 0.3s;}
#backTop:hover{transform:scale(1.1);}
</style>
</head>
<body>

<canvas id="particles"></canvas>
<div id="progressBar"></div>

<div id="hero">
  <img src="logo.png" alt="AREA323 Logo">
  <div class="buttons">
    <button data-section="tanitim">Klan Hakkında</button>
    <button data-section="basvuru">Klana Katıl</button>
    <button data-section="iletisim">İletişim</button>
  </div>
</div>

<section id="tanitim">
  <h2>Klan Tanıtımı</h2>
  <p>AREA323, sadece bir klan değil bir aile. Strateji, disiplin ve dostluğu birleştirerek sahada fark yaratan elit PUBG Mobile ekibiyiz. Bizimle olan herkes bu hikayenin bir parçasıdır.</p>
</section>

<section id="basvuru">
  <h2>Klana Katıl</h2>
  <form id="applyForm" action="https://formspree.io/f/xqalrayd" method="POST" target="_blank">
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

<section id="iletisim">
  <h2>İletişim</h2>
  <div class="socials">
    <a href="https://www.tiktok.com/@exile323" target="_blank">
      <img src="tictoc-icon.png" alt="TikTok"> @exile323
      <span>TikTok Profili Aç</span>
    </a>
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">
      <img src="tictoc-icon.png" alt="TikTok"> @babavizyondapm
      <span>TikTok Profili Aç</span>
    </a>
  </div>
</section>

<footer>AREA323 – Since 2018</footer>
<button id="backTop">&#8679;</button>

<script>
// Particle Arka Plan
const canvas=document.getElementById('particles'); const ctx=canvas.getContext('2d');
let w=canvas.width=window.innerWidth; let h=canvas.height=window.innerHeight;
window.addEventListener('resize',()=>{w=canvas.width=window.innerWidth; h=canvas.height=window.innerHeight;});
let particlesArray=[];
class Particle{constructor(){this.x=Math.random()*w;this.y=Math.random()*h;this.size=Math.random()*3+1;this.speedX=(Math.random()-0.5)*0.5;this.speedY=(Math.random()-0.5)*0.5;}
update(){this.x+=this.speedX;this.y+=this.speedY;if(this.x>w)this.x=0;if(this.x<0)this.x=w;if(this.y>h)this.y=0;if(this.y<0)this.y=h;}
draw(){ctx.fillStyle='rgba(0,255,255,0.6)';ctx.beginPath();ctx.arc(this.x,this.y,this.size,0,Math.PI*2);ctx.fill();}}
function init(){particlesArray=[];for(let i=0;i<120;i++){particlesArray.push(new Particle());}}
function animate(){ctx.clearRect(0,0,w,h);particlesArray.forEach(p=>{p.update();p.draw();});requestAnimationFrame(animate);}
init();animate();

// Scroll Progress
window.addEventListener('scroll',()=>{const winScroll=document.body.scrollTop||document.documentElement.scrollTop;
const height=document.documentElement.scrollHeight-document.documentElement.clientHeight;
document.getElementById('progressBar').style.width=((winScroll/height)*100)+'%';});

// Back to Top
const backTop=document.getElementById('backTop');
window.addEventListener('scroll',()=>{backTop.style.display=(window.scrollY>500)?'block':'none';});
backTop.addEventListener('click',()=>{window.scrollTo({top:0,behavior:'smooth'});});

// Bölümlere tıklayınca açma
const buttons=document.querySelectorAll('#hero .buttons button');
buttons.forEach(btn=>{btn.addEventListener('click',()=>{
  const secId=btn.dataset.section;
  document.querySelectorAll('section').forEach(s=>s.classList.remove('active'));
  document.getElementById(secId).classList.add('active');
  document.getElementById(secId).scrollIntoView({behavior:"smooth"});
});});

// Form onay mesajı
const form=document.getElementById('applyForm');
const message=document.getElementById('formMessage');
form.addEventListener('submit', e=>{
  e.preventDefault();
  form.submit();
  message.style.display='block';
  setTimeout(()=>{message.style.display='none';},5000);
});
</script>

</body>
