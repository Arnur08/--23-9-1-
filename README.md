
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құтты Болсын!</title>
    <style>
        body {
            background-color: #1a1a1a;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
            position: relative;
        }
        .envelope {
            width: 250px;
            height: 180px;
            background: #ff4d4d;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 22px;
            font-weight: bold;
            cursor: pointer;
            animation: float 2s infinite alternate;
        }
        @keyframes float {
            0% { transform: translate(-50%, -50%) translateY(-10px); }
            100% { transform: translate(-50%, -50%) translateY(10px); }
        }
        .hearts, .confetti {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }
        .heart {
            position: absolute;
            bottom: -10px;
            color: red;
            font-size: 28px;
            animation: fall linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(100vh) scale(0.5); opacity: 0; }
        }
        .message {
            display: none;
            position: absolute;
            top: 25%;
            left: 50%;
            transform: translate(-50%, -30%);
            font-size: 24px;
            background: rgba(0, 0, 0, 0.8);
            padding: 30px;
            border-radius: 10px;
            max-width: 500px;
        }
        .confetti div {
            position: absolute;
            width: 12px;
            height: 12px;
            opacity: 0.8;
            animation: confetti-fall linear infinite;
        }
        @keyframes confetti-fall {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <div class="hearts"></div>
    <div class="confetti"></div>

    <div class="envelope" onclick="openMessage()">📩 Аш!</div>

    <div class="message">
        <h2>✨ 8 НАУРЫЗ ҚҰТТЫ БОЛСЫН! ✨</h2>
        <p>Құрметті арулар: Айдана, Жанерке, Мадина, Фариза, Әсел, Фатима!</p>
        <p>Сіздерді көктемнің ең тамаша мерекесімен шын жүректен құттықтаймын!  
           Бұл күн тек әйелдер үшін ғана емес, бүкіл әлемді жылулық пен мейірімділікке бөлейтін күн!  
           Әр күніңіз қуаныш пен махаббатқа толы болсын! 💖</p>
        <p>Бұл қасиетті Рамазан айында сіздерге жүрек тыныштығы, жақсылық және ең мықты нұсқаңыз болуды тілеймін!</p>
        <p>💐 Сіздер ең әдемі, ең мейірімді жандарсыздар! Қуаныш пен шаттық сізбен бірге болсын! 💐</p>
        <p>💖 Құрметпен, Арнұр 💖</p>
    </div>

    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.animationDuration = Math.random() * 3 + 3 + "s";
            document.querySelector(".hearts").appendChild(heart);
            setTimeout(() => heart.remove(), 6000);
        }
        setInterval(createHeart, 200);

        function createConfetti() {
            const confetti = document.createElement("div");
            confetti.style.left = Math.random() * window.innerWidth + "px";
            confetti.style.animationDuration = Math.random() * 3 + 3 + "s";
            confetti.style.background = `hsl(${Math.random() * 360}, 100%, 50%)`;
            confetti.classList.add("confetti");
            document.querySelector(".confetti").appendChild(confetti);
            setTimeout(() => confetti.remove(), 5000);
        }

        function openMessage() {
            document.querySelector(".envelope").style.display = "none";
            document.querySelector(".message").style.display = "block";
            for (let i = 0; i < 70; i++) {
                setTimeout(createConfetti, i * 50);
            }
        }
    </script>

</body>
</html>
