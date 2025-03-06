# M-23-9-1
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құттықтау</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #ffccdd; /* Розовый фон */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            flex-direction: column;
            overflow: hidden;
            font-family: Arial, sans-serif;
            text-align: center;
        }

        .heart {
            position: absolute;
            width: 15px;
            height: 15px;
            background-color: red;
            transform: rotate(-45deg);
            position: absolute;
            animation: fall linear infinite;
        }

        .heart::before,
        .heart::after {
            content: '';
            width: 15px;
            height: 15px;
            background-color: red;
            border-radius: 50%;
            position: absolute;
        }

        .heart::before {
            top: -7px;
            left: 0;
        }

        .heart::after {
            top: 0;
            left: 7px;
        }

        @keyframes fall {
            0% { transform: translateY(-10vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }

        .message-box {
            display: none;
            padding: 15px;
            background-color: #ff69b4;
            color: white;
            text-align: center;
            font-size: 1.2em;
            border-radius: 10px;
            box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.2);
            width: 90%;
            max-width: 400px;
        }

        .nurse-box {
            display: none;
            position: absolute;
            top: 10px;
            width: 100%;
            text-align: center;
            font-size: 2em;
            color: #ff1493;
        }

        .name-list {
            font-size: 1em;
            margin-top: 10px;
        }

        .fatima {
            font-weight: bold;
            color: #ff0000;
            font-size: 1.2em;
        }
    </style>
</head>
<body>

    <h1>Құрметті ханымдар!</h1>

    <script>
        function createHearts() {
            for (let i = 0; i < 80; i++) {
                let heart = document.createElement("div");
                heart.className = "heart";
                heart.style.left = Math.random() * 100 + "vw";
                heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
                document.body.appendChild(heart);

                setTimeout(() => {
                    heart.remove();
                }, 5000);
            }
        }

        function showNurses() {
            let nurseBox = document.createElement("div");
            nurseBox.className = "nurse-box";
            nurseBox.innerHTML = "👩‍⚕️ 👩‍⚕️ 👩‍⚕️";
            document.body.appendChild(nurseBox);
            nurseBox.style.display = "block";
        }

        function showMessage() {
            let messageBox = document.createElement("div");
            messageBox.className = "message-box";
            messageBox.innerHTML = `
                <p><b>Құрметті арулар!</b></p>
                <p>Сіздерді 8 Наурыз - Халықаралық әйелдер күнімен шын жүректен құттықтаймыз!</p>
                <p>Сіздерге мықты денсаулық, шексіз бақыт және өмірлеріңіз жарқын болуын тілейміз!</p>
                <p class="name-list">Ақсәйім, Ақниет, Арухан, Ақмаржан, Аяулым, Айназым, Береке, Жібек, Жанерке, Жансая, Жаннур, Памбук, Улдана, Іңкәр, Заки</p>
                <p class="fatima">Және ерекше Фатима!</p>
            `;
            document.body.appendChild(messageBox);
            messageBox.style.display = "block";
        }

        setTimeout(createHearts, 500);
        setTimeout(showNurses, 3000);
        setTimeout(showMessage, 5000);
    </script>

</body>
</html>
