# M-23-9-1
<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>8 Наурыз Құтты Болсын!</title>
    <style>
        body {
            background-color: #ffb6c1;
            text-align: center;
            font-family: Arial, sans-serif;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            position: relative;
        }

        .truck {
            width: 250px;
            position: absolute;
            left: -300px;
            bottom: 50px;
            animation: drive 4s ease-out forwards;
        }

        @keyframes drive {
            50% {
                left: 50%;
                transform: translateX(-50%);
            }
            100% {
                left: 50%;
                transform: translateX(-50%);
            }
        }

        .men-container {
            position: absolute;
            bottom: -200px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 20px;
            animation: appearMen 2s ease-out 4s forwards;
        }

        @keyframes appearMen {
            to {
                bottom: 80px;
            }
        }

        .man {
            width: 60px;
            height: 150px;
            background-color: #6b4226;
            border-radius: 10px;
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .head {
            width: 40px;
            height: 40px;
            background-color: #f4c09c;
            border-radius: 50%;
            position: absolute;
            top: -40px;
        }

        .flower {
            width: 20px;
            height: 50px;
            background: linear-gradient(to top, green 50%, red 50%);
            border-radius: 10px;
            position: absolute;
            top: 30px;
            left: 50%;
            transform: translateX(-50%);
        }

        .message {
            opacity: 0;
            font-size: 20px;
            color: white;
            background: rgba(0, 0, 0, 0.5);
            padding: 20px;
            border-radius: 10px;
            margin-top: 250px;
            animation: fadeIn 2s ease-in 6s forwards;
        }

        @keyframes fadeIn {
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>

    <img src="https://i.imgur.com/F5oNnvO.png" alt="Truck" class="truck">

    <div class="men-container">
        <div class="man"><div class="head"></div><div class="flower"></div></div>
        <div class="man"><div class="head"></div><div class="flower"></div></div>
        <div class="man"><div class="head"></div><div class="flower"></div></div>
        <div class="man"><div class="head"></div><div class="flower"></div></div>
        <div class="man"><div class="head"></div><div class="flower"></div></div>
        <div class="man"><div class="head"></div><div class="flower"></div></div>
    </div>

    <div class="message">
        <p>Құрметті Ақсезім, Ақниет, Аружан, Ақмаржан, Аяулым, Аиназым, Береке, Жібек, Жанерке, Жансая, Жаннұр, Памбух, Ұлдана, Іңкәр, Закия!</p>
        <p>Сіздерді 8 Наурыз - Халықаралық әйелдер күнімен шын жүректен құттықтаймыз!</p>
        <p>Сіздерге мықты денсаулық, шексіз бақыт және өмірлеріңіз жарқын болуын тілейміз!</p>
        <p><b>Ал біздің сүйікті кураторымыз Фатима</b> – сіздің еңбегіңізге үлкен рақмет! Біз сізді жоғары бағалаймыз!</p>
    </div>

</body>
</html>
