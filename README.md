<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>QR Code with Photos</title>
  <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 20px;
      background: #f4f4f4;
    }
    .box {
      background: white;
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      display: inline-block;
      max-width: 800px;
    }
    canvas {
      margin: 15px 0;
    }
    .photos {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 15px;
      margin-top: 20px;
    }
    .photos img {
      width: 100%;
      border-radius: 10px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
    }
    h2 {
      color: #333;
    }
  </style>
</head>
<body>
  <div class="box">
    <h2>Scan to Open Link</h2>
    <canvas id="qrcode"></canvas>
    <p>Google Drive File Link</p>

    <!-- Photos yaha dikhengi -->
    <div class="photos">
      <img src="images/pic1.jpg" alt="Photo 1">
      <img src="images/pic2.jpg" alt="Photo 2">
      <img src="images/pic3.jpg" alt="Photo 3">
      <img src="images/pic4.jpg" alt="Photo 4">
      <img src="images/pic5.jpg" alt="Photo 5">
      <img src="images/pic6.jpg" alt="Photo 6">
      <img src="images/pic7.jpg" alt="Photo 7">
      <img src="images/pic8.jpg" alt="Photo 8">
      <img src="images/pic9.jpg" alt="Photo 9">
      <img src="images/pic10.jpg" alt="Photo 10">
      <img src="images/pic11.jpg" alt="Photo 11">
    </div>
  </div>

  <script>
    // Yaha apna link daalo
    const link = "https://drive.google.com/file/d/1s8cRYhPS3NcU89xY-m-jcpRL56P76I-q/view?usp=sharing";
    
    QRCode.toCanvas(document.getElementById('qrcode'), link, { width: 200 }, function (error) {
      if (error) console.error(error);
      console.log('QR Code generated!');
    });
  </script>
</body>
</html>
# dhruvsgift
