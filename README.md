
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құттықтау</title>
    <style>
        body {
            background-color: #1e1e1e;
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
            margin: 0;
            padding: 0;
        }

        .container {
            position: relative;
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .envelope {
            width: 150px;
            height: 100px;
            background-color: #d62828;
            position: relative;
            cursor: pointer;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.3s ease;
        }

        .envelope:hover {
            transform: scale(1.1);
        }

        .envelope::before {
            content: "От Арнура";
            color: white;
            font-weight: bold;
            position: absolute;
            top: -30px;
        }

        .hint {
            font-size: 14px;
            color: #fff;
            position: absolute;
            top: -50px;
            animation: blink 1.5s infinite;
        }

        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .hearts-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: red;
            clip-path: polygon(50% 0%, 100% 40%, 80% 100%, 50% 80%, 20% 100%, 0% 40%);
            opacity: 0;
            animation: fall 4s linear forwards;
        }

        @keyframes fall {
            0% { opacity: 1; transform: translateY(0); }
            100% { opacity: 0; transform: translateY(100vh); }
        }

        .message {
            display: none;
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
            width: 80%;
            max-width: 500px;
            font-size: 18px;
            line-height: 1.5;
        }

        .names {
            color: #ffcc00;
            font-weight: bold;
        }
    </style>
</head>
<body>

<div class="container">
    <div class="hint">Нажми, чтобы открыть</div>
    <div class="envelope" onclick="openEnvelope()"></div>
    <div class="hearts-container"></div>
    <div class="message" id="message">
        <p><span class="names">Ақмаржан, Ақниет, Ақсезім, Аиназым, Аружан, Аяжан, Береке, Памбух Ұлдана, Гүлназ, Закия, Жанерке, Жаннұр, Жансая, Жібек, Сұлухан, Сабина</span>!</p>
        <p>Сіздерді 8 Наурыз Халықаралық әйелдер күнімен шын жүректен құттықтаймын! Сіздердің сұлулықтарыңыз бен мейірімділіктеріңіз әлемді жарқын етеді. Денсаулық, бақыт, табыс және жүректеріңізде мәңгілік көктем болсын!</p>
        <p>Алдағы Рамазан айында сабыр, ізгілік және рухани жетілу тілеймін. Жүректеріңіз тыныштық пен жылулыққа толсын!</p>
        <p>✨ Ізгі тілекпен, Арнұр ✨</p>
    </div>
</div>

<script>
    function openEnvelope() {
        document.querySelector(".envelope").style.display = "none";
        document.querySelector(".hint").style.display = "none";

        const heartsContainer = document.querySelector(".hearts-container");
        for (let i = 0; i < 50; i++) {
            let heart = document.createElement("div");
            heart.classList.add("heart");
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = (2 + Math.random() * 3) + "s";
            heartsContainer.appendChild(heart);
        }

        setTimeout(() => {
            document.getElementById("message").style.display = "block";
        }, 2000);
    }
</script>

</body>
</html>
