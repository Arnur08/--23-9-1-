<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Құттықтау</title>
    <style>
        body {
            background-color: black;
            color: white;
            text-align: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
        }

        #envelope {
            position: relative;
            width: 100px;
            height: 80px;
            background-color: red;
            margin: 150px auto;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            cursor: pointer;
            border-radius: 10px;
            transition: transform 0.5s ease-in-out;
        }

        .heart {
            position: absolute;
            color: red;
            font-size: 24px;
            animation: fall 2s linear forwards;
        }

        @keyframes fall {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(100vh); opacity: 0; }
        }

        #openBtn {
            display: none;
            padding: 10px 20px;
            font-size: 18px;
            background-color: red;
            color: white;
            border: none;
            cursor: pointer;
            margin-top: 20px;
            border-radius: 5px;
        }

        #message {
            display: none;
            font-size: 20px;
            padding: 20px;
        }
    </style>
</head>
<body>

    <div id="envelope" onclick="openEnvelope()">📩</div>
    <button id="openBtn" onclick="showMessage()">Открыть</button>
    <div id="message">
        <p>Құрметті Ақмаржан, Ақниет, Ақсезім, Аиназым, Аружан, Аяжан, Береке, Памбух Ұлдана, Гүлназ, Закия, Жанерке, Жаннұр, Жансая, Жібек, Сұлухан, Сабина!</p>
        <p>Сіздерді көктемнің ең ерекше, ең жарқын мерекесімен құттықтаймын! 🌹</p>
        <p>Сіздерге шексіз бақыт, зор денсаулық, қуаныш пен махаббат тілеймін. Әр күніңіз гүлдей жайнап, жүректеріңіз шаттыққа толы болсын! ❤️</p>
        <p>Сондай-ақ, қасиетті Рамазан айында Алла сіздерге жеңілдік берсін, жүректеріңіз нұрға толсын. Бұл ай өзіңіздің ең жақсы нұсқаңызға айналуыңызға мүмкіндік болсын! ❤️</p>
        <p>💖🌙 Ізгі тілекпен, M-23-9-1!</p>
    </div>

    <script>
        function openEnvelope() {
            let envelope = document.getElementById("envelope");
            envelope.style.display = "none";

            for (let i = 0; i < 20; i++) {
                let heart = document.createElement("div");
                heart.classList.add("heart");
                heart.innerHTML = "❤️";
                heart.style.left = Math.random() * window.innerWidth + "px";
                heart.style.top = "-20px";
                heart.style.fontSize = Math.random() * 20 + 20 + "px";
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 2000);
            }

            setTimeout(() => {
                document.getElementById("openBtn").style.display = "block";
            }, 2000);
        }

        function showMessage() {
            document.getElementById("openBtn").style.display = "none";
            document.getElementById("message").style.display = "block";

            for (let i = 0; i < 20; i++) {
                let heart = document.createElement("div");
                heart.classList.add("heart");
                heart.innerHTML = "❤️";
                heart.style.left = Math.random() * window.innerWidth + "px";
                heart.style.top = "-20px";
                heart.style.fontSize = Math.random() * 20 + 20 + "px";
                document.body.appendChild(heart);
                setTimeout(() => heart.remove(), 2000);
            }
        }
    </script>

</body>
</html>
