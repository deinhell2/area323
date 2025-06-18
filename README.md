<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZZONE99 | mAzz99</title>
  <style>
    body {
      margin: 0;
      background-color: #0d0d0d;
      font-family: 'Segoe UI', sans-serif;
      overflow-x: hidden;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    .logo-container {
      position: relative;
      animation: fadeIn 2s ease forwards;
      text-align: center;
    }

    .logo-container img {
      width: 220px; /* Boyutu büyüttük */
      height: auto;
      animation: pulse 3s infinite ease-in-out;
    }

    .nickname {
      margin-top: 20px;
      font-size: 28px;
      font-weight: bold;
      background: linear-gradient(90deg, #00f2ff, #00ffe0, #00f2ff);
      background-size: 300% 300%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: rgbFlow 5s infinite;
    }

    @keyframes rgbFlow {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    @keyframes fadeIn {
      0% {opacity: 0; transform: translateY(-50px);}
      100% {opacity: 1; transform: translateY(0);}
    }

    @keyframes pulse {
      0%, 100% {
        transform: scale(1);
        filter: drop-shadow(0 0 10px rgba(0, 255, 255, 0.5));
      }
      50% {
        transform: scale(1.05);
        filter: drop-shadow(0 0 20px rgba(0, 255, 255, 0.8));
      }
    }
  </style>
</head>
<body>
  <div class="logo-container">
    <img src="mazz.png" alt="mAzz99 Logo">
    <div class="nickname">mAzz99</div>
  </div>
</body>
