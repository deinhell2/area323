<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>zzone99</title>
<style>
  /* Temel koyu tema */
  body {
    margin:0; padding:0;
    background: #121212;
    color: #eee;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  nav {
    background: #181818;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    position: sticky;
    top: 0;
    z-index: 1000;
    border-bottom: 1px solid #222;
  }
  nav .logo {
    font-weight: bold;
    font-size: 22px;
    color: #1db954;
  }
  nav .menu {
    display: flex;
    gap: 20px;
  }
  nav button.menu-btn {
    background: none;
    border: none;
    color: #eee;
    font-size: 16px;
    cursor: pointer;
    font-weight: 500;
  }
  nav button.menu-btn.active {
    color: #1db954;
    font-weight: 700;
  }
  nav select {
    background: #222;
    border: none;
    color: #eee;
    border-radius: 4px;
    padding: 4px 8px;
    cursor: pointer;
  }
  /* Burger menu gizli */
  nav button.burger {
    display: none;
    background: none;
    border: none;
    font-size: 28px;
    color: #eee;
    cursor: pointer;
  }
  /* Mobilde burger göster */
  @media (max-width:700px) {
    nav .menu {
      display: none;
    }
    nav button.burger {
      display: block;
    }
    nav .mobile-menu {
      position: absolute;
      top: 60px;
      right: 20px;
      background: #222;
      border-radius: 8px;
      padding: 10px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      z-index: 1100;
      width: 150px;
    }
    nav .mobile-menu button {
      color: #eee;
      background: none;
      border: none;
      font-size: 16px;
      cursor: pointer;
      text-align: left;
    }
    nav .mobile-menu button.active {
      color: #1db954;
      font-weight: 700;
    }
    nav .mobile-menu select {
      margin-top: 10px;
      background: #333;
    }
  }
  main {
    padding: 20px;
    min-height: 80vh;
  }
  /* Sayfa geçiş animasyon */
  .page {
    opacity: 0;
    transform: translateY(10px);
    transition: opacity 0.3s ease, transform 0.3s ease;
    position: absolute;
    width: 100%;
  }
  .page.active {
    opacity: 1;
    transform: translateY(0);
    position: relative;
  }
  /* Başvuru form */
  form {
    max-width: 400px;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  form label {
    display: flex;
    flex-direction: column;
    color: #eee;
    font-weight: 600;
  }
  form input {
    padding: 8px;
    margin-top: 6px;
    border-radius: 6px;
    border: 1px solid #555;
    background: #222;
    color: #eee;
  }
  form button[type="submit"] {
    background: #1db954;
    border: none;
    padding: 10px;
    color: white;
    font-weight: 700;
    cursor: pointer;
    border-radius: 6px;
    font-size: 16px;
  }
  form button[type="submit"]:disabled {
    background: #555;
    cursor: wait;
  }
  /* Toast mesaj */
  #toast {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: #4caf50;
    color: white;
    padding: 12px 20px;
    border-radius: 5px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.4);
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s ease;
    z-index: 1200;
  }
  #toast.error {
    background: #f44336;
  }
  #toast.show {
    opacity: 1;
    pointer-events: auto;
  }
  /* TikTok popup */
  #tiktokPopup {
    position: fixed;
    top:0; left:0;
    width: 100vw; height: 100vh;
    background: rgba(0,0,0,0.85);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 1300;
  }
  #tiktokPopup.active {
    display: flex;
  }
  #tiktokPopup iframe {
    width: 90vw;
    max-width: 480px;
    height: 80vw;
    max-height: 600px;
    border: none;
    border-radius: 10px;
  }
  #tiktokPopup button.closeBtn {
    position: absolute;
    top: 20px;
    right: 30px;
    font-size: 36px;
    background: transparent;
    border: none;
    color: white;
    cursor: pointer;
    user-select: none;
  }
</style>
</head>
<body>

<nav>
  <div class="logo">zzone99</div>
  <div class="menu" role="menubar" aria-label="Main navigation">
    <button class="menu-btn active" data-page="home" role="menuitem">Anasayfa</button>
    <button class="menu-btn" data-page="application" role="menuitem">Başvuru</button>
    <select id="langSelect" aria-label="Dil Seçimi">
      <option value="tr">TR</option>
      <option value="en">EN</option>
    </select>
  </div>
  <button class="burger" aria-label="Menüyü aç">☰</button>
</nav>

<div class="mobile-menu" style="display:none;" role="menu" aria-label="Mobil Menü">
  <button class="menu-btn active" data-page="home" role="menuitem">Anasayfa</button>
  <button class="menu-btn" data-page="application" role="menuitem">Başvuru</button>
  <select id="langSelectMobile" aria-label="Dil Seçimi Mobil">
    <option value="tr">TR</option>
    <option value="en">EN</option>
  </select>
</div>

<main>
  <section id="home" class="page active" aria-label="Anasayfa">
    <h1>zzone99</h1>
    <p>
      PUBG Mobile klanımız zzone99'a hoş geldiniz! En iyi oyuncularla takım kurup birlikte kazanmanın tadını çıkarın.
    </p>
    <h2>TikTok Videoları</h2>
    <div>
      <button class="tiktokBtn" data-url="https://www.tiktok.com/embed/v2/7043990426214152198">TikTok Video #1</button>
      <button class="tiktokBtn" data-url="https://www.tiktok.com/embed/v2/6957034976603799298">TikTok Video #2</button>
    </div>
  </section>
  <section id="application" class="page" aria-label="Başvuru Formu" style="display:none;">
    <h1>Şimdi Başvur</h1>
    <form id="applicationForm" novalidate>
      <label for="nameInput">İsim
        <input type="text" id="nameInput" name="name" required />
      </label>
      <label for="emailInput">E-posta
        <input type="email" id="emailInput" name="email" required />
      </label>
      <button type="submit">Gönder</button>
    </form>
  </section>
</main>

<div id="toast" role="alert" aria-live="assertive"></div>

<div id="tiktokPopup" role="dialog" aria-modal="true" aria-label="TikTok Video Popup">
  <button class="closeBtn" aria-label="Popup kapat">×</button>
  <iframe src="" allow="autoplay; fullscreen" allowfullscreen></iframe>
</div>

<script>
  (() => {
    const langData = {
      tr: {
        home: "Anasayfa",
        application: "Başvuru",
        applyNow: "Şimdi Başvur",
        name: "İsim",
        email: "E-posta",
        submit: "Gönder",
        success: "Başvurunuz başarıyla alındı!",
        error: "Lütfen tüm alanları doldurun!",
        tiktok: "TikTok Videoları",
        close: "Kapat",
        welcome: "PUBG Mobile klanımız zzone99'a hoş geldiniz! En iyi oyuncularla takım kurup birlikte kazanmanın tadını çıkarın."
      },
      en: {
        home: "Home",
        application: "Application",
        applyNow: "Apply Now",
        name: "Name",
        email: "Email",
        submit: "Submit",
        success: "Your application was successful!",
        error: "Please fill all fields!",
        tiktok: "TikTok Videos",
        close: "Close",
        welcome: "Welcome to our PUBG Mobile clan zzone99! Join the best players and enjoy winning together."
      },
    };

    const navBtns = document.querySelectorAll("nav .menu-btn");
    const mobileMenu = document.querySelector(".mobile-menu");
    const mobileNavBtns = mobileMenu.querySelectorAll("button.menu-btn");
    const burgerBtn = document.querySelector("nav button.burger");
    const langSelect = document.getElementById("langSelect");
    const langSelectMobile = document.getElementById("langSelectMobile");
    const pages = document.querySelectorAll("main section.page");
    const toast = document.getElementById("toast");
    const tiktokPopup = document.getElementById("tiktokPopup");
    const tiktokIframe = tiktokPopup.querySelector("iframe");
    const tiktokCloseBtn = tiktokPopup.querySelector(".closeBtn");

    let currentLang = "tr";
    let currentPage = "home";
    let toastTimeout = null;

    // Dil güncelle
    function updateLang(lang) {
      currentLang = lang;
      const d = langData[lang];
      // Nav butonları
      navBtns.forEach((btn) => {
        const page = btn.dataset.page;
        btn.textContent = d[page];
      });
      mobileNavBtns.forEach((btn) => {
        const page = btn.dataset.page;
        btn.textContent = d[page];
      });
      // Select labeller yok ama option var
      langSelect.value = lang;
      langSelectMobile.value = lang;
      // İçerikler
      document.querySelector("#home h1").textContent = "zzone99";
      document.querySelector("#home p").textContent = d.welcome;
      document.querySelector("#home h2").textContent = d.tiktok;
      document.querySelector("#application h1").textContent = d.applyNow;
      document.querySelector('label[for="nameInput"]').firstChild.textContent = d.name;
      document.querySelector('label[for="emailInput"]').firstChild.textContent = d.email;
      document.querySelector("#application button[type=submit]").textContent = d.submit;
    }

    // Sayfa geçişi
    function setPage(page) {
      if (page === currentPage) return;
      const oldPage = document.getElementById(currentPage);
      const newPage = document.getElementById(page);
      if (!newPage) return;
      // Menü aktif buton değiştir
      navBtns.forEach(btn => btn.classList.toggle("active", btn.dataset.page === page));
      mobileNavBtns.forEach(btn => btn.classList.toggle("active", btn.dataset.page === page));
      // Animasyonlu değişim:
      oldPage.classList.remove("active");
      oldPage.style.display = "none";
      newPage.style.display = "block";
      setTimeout(() => newPage.classList.add("active"), 10);
      currentPage = page;
      // Hash güncelle
      history.replaceState(null, null, `#${page}`);
      // Mobil menüyü kapat
      mobileMenu.style.display = "none";
    }

    // Toast göster
    function showToast(msg, success = true) {
      toast.textContent = msg;
      toast.className = "show" + (success ? "" : " error");
      if (toastTimeout) clearTimeout(toastTimeout);
      toastTimeout = setTimeout(() => {
        toast.className = "";
      }, 3000);
    }

    // Başvuru formu gönderim simülasyonu
    const form = document.getElementById("applicationForm");
    form.addEventListener("submit", e => {
      e.preventDefault();
      const name = form.name.value.trim();
      const email = form.email.value.trim();
      if (!name || !email) {
        showToast(langData[currentLang].error, false);
        return;
      }
      form.querySelector("button[type=submit]").disabled = true;
      showToast("...");
      setTimeout(() => {
        form.querySelector("button[type=submit]").disabled = false;
        if (Math.random() < 0.8) {
          showToast(langData[currentLang].success, true);
          form.reset();
        } else {
          showToast(langData[currentLang].error, false);
        }
      }, 1500);
    });

    // TikTok popup açma
    document.querySelectorAll(".tiktokBtn").forEach(btn => {
      btn.addEventListener("click", () => {
        const url = btn.dataset.url;
        tiktokIframe.src = url;
        tiktokPopup.classList.add("active");
      });
    });
    // TikTok popup kapatma
    tiktokCloseBtn.addEventListener("click", () => {
      tiktokPopup.classList.remove("active");
      tiktokIframe.src = "";
    });
    tiktokPopup.addEventListener("click", () => {
      tiktokPopup.classList.remove("active");
      tiktokIframe.src = "";
    });
    tiktokIframe.addEventListener("click", e => e.stopPropagation());

    // Menü butonları
    navBtns.forEach(btn => btn.addEventListener("click", () => setPage(btn.dataset.page)));
    mobileNavBtns.forEach(btn => btn.addEventListener("click", () => setPage(btn.dataset.page)));

    // Dil seçimi
    langSelect.addEventListener("change", e => updateLang(e.target.value));
    langSelectMobile.addEventListener("change", e => updateLang(e.target.value));

    // Burger menü toggle
    burgerBtn.addEventListener("click", () => {
      mobileMenu.style.display = mobileMenu.style.display === "flex" ? "none" : "flex";
    });

    // Hash varsa ona göre sayfa aç
    function loadFromHash() {
      const h = location.hash.replace("#", "");
      if (h === "home" || h === "application") setPage(h);
      else setPage("home");
    }
    window.addEventListener("hashchange", loadFromHash);
    loadFromHash();

    // Başlangıç dil ayarla
    updateLang(currentLang);
  })();
</script>

</body>
