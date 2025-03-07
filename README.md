
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құттықтау</title>
    <style>
        body {
            background-color: #1a1a1a;
            color: white;
            text-align: center;
            font-family: Arial, sans-serif;
        }
        .container {
            position: relative;
            margin-top: 50px;
        }
        .envelope {
            display: inline-block;
            padding: 20px;
            background-color: red;
            color: white;
            font-size: 20px;
            font-weight: bold;
            cursor: pointer;
            border-radius: 5px;
        }
        .message {
            display: none;
            margin-top: 20px;
            font-size: 18px;
        }
        .hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            overflow: hidden;
            top: 0;
            left: 0;
            pointer-events: none;
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: fall 3s linear infinite;
        }
        @keyframes fall {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }
    </style>
</head>
<body>

<h1>🌸 8 НАУРЫЗ ҚҰТТЫҚТАУ 🌸</h1>
<p>Нажми на конверт, чтобы открыть!</p>

<div class="container">
    <div class="hearts"></div>
    <div class="envelope" onclick="openMessage()">Ізгі тілекпен М-23-9-1</div>
    <div class="message" id="message">
        <p>Құрметті Ақмаржан, Ақниет, Ақсезім, Аиназым, Аружан, Аяжан, Береке, Памбух Ұлдана, Гүлназ, Закия, Жанерке, Жаннұр, Жансая, Жібек, Сұлухан, Сабина!</p>
        <p>Сіздерді көктемнің ең ерекше, ең жарқын мерекесі – 8 Наурызбен құттықтаймын! 🌹</p>
        <p>Сіздерге шексіз бақыт, зор денсаулық, қуаныш пен махаббат тілеймін. Әр күніңіз гүлдей жайнап, жүректеріңіз шаттыққа толы болсын!</p>
        <p>Сондай-ақ, қасиетті Рамазан айында Алла сіздерге жеңілдік берсін, жүректеріңіз нұрға толсын. Бұл ай өзіңіздің ең жақсы нұсқаңызға айналуыңызға мүмкіндік болсын!</p>
        <p>💖🌙 Ізгі тілекпен, М-23-9-1!</p>
    </div>
</div>

<script>
    function openMessage() {
        document.getElementById("message").style.display = "block";
        createHearts();
    }

    function createHearts() {
        const heartContainer = document.querySelector(".hearts");
        for (let i = 0; i < 20; i++) {
            let heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = (Math.random() * 2 + 2) + "s";
            heart.style.animationDelay = Math.random() + "s";
            heartContainer.appendChild(heart);
        }
    }
</script>

</body>
</html>
