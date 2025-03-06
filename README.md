
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Поздравление</title>
    <style>
        body {
            background-color: #0a0a3d;
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
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 100px;
            opacity: 0;
            animation: heartsFlow 4s 2s forwards;
        }
        @keyframes heartsFlow {
            0% { opacity: 0; transform: translateY(20px); }
            100% { opacity: 1; transform: translateY(-50px); }
        }
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: red;
            transform: rotate(-45deg);
            top: 0;
            left: 50%;
            animation: floatUp 4s infinite ease-in-out;
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
        .text {
            margin-top: 20px;
            font-size: 22px;
            opacity: 0;
            animation: fadeIn 3s 3s forwards;
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
            <div class="heart" style="animation-delay: 0s;"></div>
            <div class="heart" style="left: 60%; animation-delay: 0.5s;"></div>
            <div class="heart" style="left: 40%; animation-delay: 1s;"></div>
        </div>
        <div class="text">
            <p>Дорогие девушки! С 8 Марта! Пусть счастье, улыбки и любовь наполняют вашу жизнь!</p>
        </div>
        <div class="signature">
            <p>От Арнура</p>
        </div>
    </div>
</body>
</html> 
