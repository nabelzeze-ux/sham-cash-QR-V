# sham-cash-QR-V
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QR Code - Sham Cash</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            background: #0b0b0b;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            font-family: 'Arial', sans-serif;
        }
        .qr-container {
            text-align: center;
            padding: 20px;
        }
        .qr-container h2 {
            color: #ffd700;
            margin-bottom: 20px;
            font-size: 24px;
            text-shadow: 0 0 10px #ffd700;
        }
        .qr-container img {
            max-width: 300px;
            width: 90vw;
            border-radius: 15px;
            border: 3px solid #ffd700;
            box-shadow: 0 0 30px rgba(255,215,0,0.3);
        }
    </style>
</head>
<body>
    <div class="qr-container">
        <h2>📷 Sham Cash QR Code</h2>
        <img id="qrImage" src="" alt="QR Code">
    </div>

    <script>
        // الحصول على رابط الصورة من URL parameter
        const urlParams = new URLSearchParams(window.location.search);
        const imgUrl = urlParams.get('img');
        
        if (imgUrl) {
            document.getElementById('qrImage').src = decodeURIComponent(imgUrl);
        } else {
            document.getElementById('qrImage').src = 'https://via.placeholder.com/300x300/1a1a2e/ffd700?text=QR+Code';
        }
    </script>
</body>
</html>
