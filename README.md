<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>เว็บจราจร ร้อยเอ็ด</title>
  <style>
    body {
      background: linear-gradient(to bottom right, #1e3a8a, #000);
      color: white;
      font-family: sans-serif;
      text-align: center;
      padding: 2rem;
    }
    .card {
      background: #111;
      border: 1px solid gold;
      border-radius: 16px;
      padding: 1.5rem;
      max-width: 400px;
      margin: 0 auto;
      box-shadow: 0 0 20px rgba(255, 215, 0, 0.4);
    }
    iframe {
      border-radius: 12px;
      margin-top: 1rem;
    }
    audio {
      margin-top: 1rem;
      width: 100%;
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>ระบบจราจร ร้อยเอ็ด</h1>

    <h2>แผนที่</h2>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3875.286586404378!2d103.65336541483136!3d16.053372788879364!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31234d8ea2cbe9b7%3A0x882f9c0b0fa7f4e3!2z4LiK4Li14LmI4LiX4Li04LiH4LmA4LiI4Liy4LiB4Lil4LmM!5e0!3m2!1sth!2sth!4v1700000000000"
      width="100%" height="250" allowfullscreen="" loading="lazy"
      referrerpolicy="no-referrer-when-downgrade">
    </iframe>

    <h2>ข่าวจราจร</h2>
    <ul style="text-align: left; padding-left: 1.5rem;">
      <li>หลีกเลี่ยงถนนแจ้งสนิทช่วงเย็น – รถติด</li>
      <li>แนะนำเส้นทางผ่านบ้านป่าไม้</li>
    </ul>

    <h2>ฟังวิทยุจราจร</h2>
    <audio controls>
      <source src="https://radio.streaming.in.th:8443/fm91.mp3" type="audio/mpeg">
      เบราว์เซอร์ของคุณไม่รองรับการเล่นเสียง
    </audio>
  </div>
</body>
</html>
