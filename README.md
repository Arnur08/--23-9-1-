
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құттықтау</title>
    <style>
        body {
            background-color: #1a1a1a; /* Темно-серый фон */
            color: white;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
        }
        .container {
            position: relative;
            width: 100%;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
        .envelope {
            position: relative;
            width: 200px;
            height: 150px;
            background: #ffcc66;
            border-radius: 10px;
            box-shadow: 0px 5px 10px rgba(0,0,0,0.2);
        }
        .flap {
            position: absolute;
            top: 0;
            width: 0;
            height: 0;
            border-left: 100px solid transparent;
            border-right: 100px solid transparent;
            border-bottom: 75px solid #ffb347;
            transform-origin: top;
            animation: openFlap 2s forwards;
        }
        @keyframes openFlap {
            0% { transform: rotate(0deg); }
            100% { transform: rotateX(180deg); }
        }
        .hearts {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            height: 100vh;
            pointer-events: none;
        }
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: red;
            transform: rotate(-45deg);
            animation: floatDown 5s linear infinite;
        }
        .heart:before, .heart:after {
            content: "";
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: red;
            border-radius: 50%;
        }
        .heart:before { top: -10px; left: 0; }
        .heart:after { left: -10px; top: 0; }
        @keyframes floatDown {
            0% { transform: translateY(-50px) rotate(-45deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(-45deg); opacity: 0; }
        }
        .text {
            margin-top: 20px;
            font-size: 22px;
            opacity: 0;
            animation: fadeIn 3s 3s forwards;
            width: 80%;
        }
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        .signature {
            margin-top: 40px;
            font-size: 18px;
            opacity: 0;
            animation: fadeIn 3s 4s forwards;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="envelope">
            <div class="flap"></div>
        </div>
        <div class="hearts">
            <script>
                for (let i = 0; i < 20; i++) {
                    let heart = document.createElement("div");
                    heart.classList.add("heart");
                    heart.style.left = `${Math.random() * 100}%`;
                    heart.style.animationDuration = `${4 + Math.random() * 3}s`;
                    heart.style.animationDelay = `${Math.random() * 5}s`;
                    document.querySelector(".hearts").appendChild(heart);
                }
            </script>
        </div>
        <div class="text">
            <p>Құрметті Аксезім, Акниет, Аружан, Ақмаржан, Аяулым, Аиназым, Береке, Жібек, Жанерке, Жансая, Жаннұр, Памбук, Ұлдана, Іңкәр, Закия!</p>
            <p>Сіздерді 8 Наурыз – Халықаралық әйелдер күнімен шын жүректен құттықтаймын! Сіздерге бақыт, махаббат пен шексіз қуаныш тілеймін!</p>
            <p>Әр күніңіз шаттық пен нұрға толы болсын! Барлық армандарыңыз орындалсын, жүректеріңіз махаббат пен жылылыққа бөленсін!</p>
            <p>Сіздер біздің шабыт көзі, отбасының жүрегі, әлемнің сұлулығысыздар! Осы күн сіздерге тек қуаныш пен бақыт әкелсін!</p>
            <p><b>Рамазан айында сіздерге тек жақсылық, рухани өсу және жеңілдік тілеймін! Өзіңіздің ең жақсы нұсқаңыз болыңыз!</b></p>
        </div>
        <div class="signature">
            <p>Махаббатпен, Арнур</p>
        </div>
    </div>
</body>
</html>
