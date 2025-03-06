<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құтты Болсын!</title>
    <style>
        body {
            background-color: #121212;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
            position: relative;
        }
        .envelope {
            width: 220px;
            height: 160px;
            background: #ff4d4d;
            position: absolute;
            top: 60%;
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
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }
        .message {
            display: none;
            position: absolute;
            top: 30%;
            left: 50%;
            transform: translate(-50%, -30%);
            font-size: 22px;
            background: rgba(0, 0, 0, 0.7);
            padding: 25px;
            border-radius: 10px;
        }
        .confetti div {
            position: absolute;
            width: 10px;
            height: 10px;
            background: yellow;
            opacity: 0.7;
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
        <h2>8 НАУРЫЗ ҚҰТТЫ БОЛСЫН!</h2>
        <p>Құрметті арулар: Айдана, Жанерке, Мадина, Фариза, Әсел, Фатима!</p>
        <p>Сіздерді көктемнің шуақты мерекесімен шын жүректен құттықтаймын! Әр күніңіз бақыт пен махаббатқа толы болсын! 😊</p>
        <p>Бұл қасиетті Рамазан айында жүректеріңіз тыныштыққа бөленіп, ең жақсы нұсқаңыз болуды тілеймін!</p>
        <p>💖 Құрметпен, Арнұр 💖</p>
    </div>

    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.animationDuration = Math.random() * 2 + 4 + "s";
            document.querySelector(".hearts").appendChild(heart);
            setTimeout(() => heart.remove(), 6000);
        }
        setInterval(createHeart, 150);

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
            for (let i = 0; i < 50; i++) {
                setTimeout(createConfetti, i * 100);
            }
        }
    </script>

</body>
</html>
