<!DOCTYPE html>
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
            margin: 0;
            padding: 20px;
            overflow: hidden;
        }
        h1 {
            font-size: 28px;
            margin-bottom: 10px;
        }
        p {
            font-size: 18px;
            line-height: 1.6;
            margin: 10px 0;
        }
        .container {
            position: relative;
            z-index: 1;
        }
        .hidden {
            display: none;
        }
        .button {
            background-color: red;
            color: white;
            border: none;
            padding: 15px 20px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 20px;
        }
        .hearts {
            position: fixed;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 0;
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

<div class="hearts"></div>

<div class="container">
    <h1>🌸 8 НАУРЫЗ ҚҰТТЫҚТАУ! 🌸</h1>
    <button class="button" onclick="showMessage()">Ізгі тілекпен M-23-9-1</button>
    
    <div id="message" class="hidden">
        <p>Құрметті Ақмаржан, Ақниет, Ақсезім, Аиназым, Аружан, Аяжан, Береке, Памбух Ұлдана, Гүлназ, Закия, Жанерке, Жаннұр, Жансая, Жібек, Сұлухан, Сабина!</p>
        <p>Сіздерді көктемнің ең ерекше, ең жарқын мерекесі – 8 Наурызбен шын жүректен құттықтаймын! 🌹</p>
        <p>Сіздерге шексіз бақыт, зор денсаулық, қуаныш пен махаббат тілеймін. Әр күніңіз гүлдей жайнап, жүректеріңіз шаттыққа толы болсын! ❤️</p>
        <p>Сондай-ақ, қасиетті Рамазан айында Алла сіздерге жеңілдік берсін, жүректеріңіз нұрға толсын. Бұл ай өзіңіздің ең жақсы нұсқаңызға айналуыңызға мүмкіндік болсын! ❤️🌙</p>
        <p>💖 Ізгі тілекпен, M-23-9-1!</p>
    </div>
</div>

<script>
    function showMessage() {
        document.getElementById("message").classList.remove("hidden");
        document.querySelector(".button").style.display = "none";
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
