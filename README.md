<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>З Днем Валентина, Софійка!</title>
    <style>
        body {
            background-color: #ffcccc;
            text-align: center;
            font-family: 'Arial', sans-serif;
            color: #ff4d4d;
            overflow: hidden;
        }
        h1 {
            font-size: 3em;
            margin-top: 50px;
            animation: fadeIn 2s ease-in-out;
        }
        p {
            font-size: 1.5em;
            margin: 20px;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .heart {
            position: absolute;
            width: 50px;
            height: 50px;
            background-color: red;
            transform: rotate(-45deg);
            animation: float 5s infinite ease-in-out;
        }
        .heart::before, .heart::after {
            content: '';
            position: absolute;
            width: 50px;
            height: 50px;
            background-color: red;
            border-radius: 50%;
        }
        .heart::before {
            top: -25px;
            left: 0;
        }
        .heart::after {
            left: 25px;
            top: 0;
        }
        @keyframes float {
            0% { transform: translateY(0) rotate(-45deg); }
            50% { transform: translateY(-20px) rotate(-45deg); }
            100% { transform: translateY(0) rotate(-45deg); }
        }
    </style>
</head>
<body>
    <audio autoplay loop>
        <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mp3">
        Ваш браузер не підтримує аудіо.
    </audio>
    <h1>З Днем Святого Валентина, Софійка! 💖</h1>
    <p>Дорога Софійка, ти найкраща, наймиліша і найдорожча для мене! Нехай цей день принесе тобі радість і усмішку. 😘</p>
    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.top = Math.random() * window.innerHeight + "px";
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHeart, 500);
    </script>
</body>
</html>
