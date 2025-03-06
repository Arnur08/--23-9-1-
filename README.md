
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
            width: 200px;
            height: 150px;
            background: #ff4d4d;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 20px;
            font-weight: bold;
            cursor: pointer;
            animation: float 2s infinite alternate;
        }
        @keyframes float {
            0% { transform: translate(-50%, -50%) translateY(-10px); }
            100% { transform: translate(-50%, -50%) translateY(10px); }
        }
        .hearts {
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
            font-size: 24px;
            animation: fall linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }
        .message {
            display: none;
            position: absolute;
            top: 20%;
            left: 50%;
            transform: translate(-50%, -20%);
            font-size: 22px;
            background: rgba(0, 0, 0, 0.7);
            padding: 20px;
            border-radius: 10px;
        }
    </style>
</head>
<body>

    <div class="hearts"></div>

    <div class="envelope" onclick="openMessage()">📩 Аш!</div>

    <div class="message">
        <h2>8 НАУРЫЗ ҚҰТТЫ БОЛСЫН!</h2>
        <p>Қымбатты ханымдар, сіздерді осы тамаша көктем мерекесімен шын жүректен құттықтаймын! Сіздерге тек бақыт, денсаулық және махаббат тілеймін!</p>
        <p>Рамазан айында жүректеріңіз тыныштыққа толы болсын, өздеріңіздің ең жақсы нұсқаларыңыз болуды тілеймін!</p>
        <p>💖 Құрметпен, Арнұр 💖</p>
    </div>

    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.animationDuration = Math.random() * 2 + 3 + "s";
            document.querySelector(".hearts").appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHeart, 200);

        function openMessage() {
            document.querySelector(".envelope").style.display = "none";
            document.querySelector(".message").style.display = "block";
        }
    </script>

</body>
</html>
