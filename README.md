<html lang="tr">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="ZZONE99 PUBG Mobile Klan Tanıtım ve Alım Sitesi" />
    <meta name="keywords" content="PUBG Mobile, Klan, ZZONE99, Başvuru" />
    <meta name="author" content="ZZONE99" />
    <title>ZZONE99</title>
    <link rel="stylesheet" href="style.css" />
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>
    <div id="loader">
        <h1 class="rgb-text">ZZONE99</h1>
    </div>

    <main class="hidden">
        <header>
            <img src="logo.png" alt="ZZONE99 Logo" class="logo" />
            <h1 class="rgb-text">ZZONE99</h1>
            <p class="subtitle">Since 2018</p>
        </header>

        <section class="intro-section">
            <h2>TANITIM</h2>
            <p>
                PUBG Mobile sahnesinde 2018 yılından beri aktif olan bir klan topluluğudur.<br />
                İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,<br />
                bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.<br />
                Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmak.
            </p>
        </section>

        <section class="characters">
            <div class="char-card">
                <img src="mazz.png" alt="mAzz99" />
                <p>mAzz99</p>
            </div>
            <div class="char-card">
                <img src="yazz.png" alt="yAzz99" />
                <p>yAzz99</p>
            </div>
        </section>

        <section class="form-section">
            <h2>KLANA KATIL</h2>
            <form action="https://formspree.io/f/xldnljve" method="POST">
                <input type="text" name="UID" placeholder="Oyuncu UID" required />
                <input type="text" name="username" placeholder="Oyun İsmi" required />
                <input type="text" name="realname" placeholder="İsim" required />
                <input type="number" name="age" placeholder="Yaş" required />
                <input type="text" name="device" placeholder="Kullandığı Cihaz" required />
                <input type="text" name="activity" placeholder="Aktiflik Durumu" required />
                <button type="submit">Başvur</button>
                <p id="form-response"></p>
            </form>
        </section>

        <section class="contact-section">
            <h2>İLETİŞİM</h2>
            <div class="tiktok-links">
                <a href="https://www.tiktok.com/@mazz99theboss" target="_blank"><i class="fab fa-tiktok"></i> @mazz99theboss</a>
                <a href="https://www.tiktok.com/@babavizyondapm" target="_blank"><i class="fab fa-tiktok"></i> @babavizyondapm</a>
            </div>
        </section>

        <footer>
            <p>Für die Famiilla - SINCE 2018</p>
            <p id="visitor-counter">Ziyaretçi Sayısı: 0</p>
        </footer>
    </main>
    <script src="script.js"></script>
</body>
