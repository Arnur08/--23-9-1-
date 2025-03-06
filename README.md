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
        }

        .truck {
            width: 200px;
            position: absolute;
            left: -250px;
            bottom: 50px;
            animation: drive 3s ease-out forwards;
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

        .men {
            display: flex;
            justify-content: center;
            gap: 15px;
            position: absolute;
            bottom: -200px;
            left: 50%;
            transform: translateX(-50%);
            animation: appear 2s ease-out 3s forwards;
        }

        .man {
            width: 50px;
            height: 100px;
            background-color: navy;
            border-radius: 10px;
            position: relative;
        }

        .flower {
            width: 20px;
            height: 20px;
            background-color: red;
            border-radius: 50%;
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
        }

        @keyframes appear {
            to {
                bottom: 50px;
            }
        }

        .message {
            opacity: 0;
            font-size: 24px;
            color: white;
            background: rgba(0, 0, 0, 0.5);
            display: inline-block;
            padding: 15px;
            border-radius: 10px;
            margin-top: 300px;
            animation: fadeIn 2s ease-in 5s forwards;
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
    
    <div class="men">
        <div class="man"><div class="flower"></div></div>
        <div class="man"><div class="flower"></div></div>
        <div class="man"><div class="flower"></div></div>
        <div class="man"><div class="flower"></div></div>
        <div class="man"><div class="flower"></div></div>
        <div class="man"><div class="flower"></div></div>
    </div>

    <div class="message">
        <p>Құрметті Ақсезім, Ақниет, Аружан, Ақмаржан, Аяулым, Аиназым, Береке, Жібек, Жанерке, Жансая, Жаннұр, Памбух, Ұлдана, Іңкәр, Закия!</p>
        <p>Сіздерді 8 Наурыз - Халықаралық әйелдер күнімен шын жүректен құттықтаймыз!</p>
        <p>Сіздерге мықты денсаулық, шексіз бақыт және өмірлеріңіз жарқын болуын тілейміз!</p>
        <p><b>Ал біздің сүйікті кураторымыз Фатима</b> – сіздің еңбегіңізге үлкен рақмет! Біз сізді жоғары бағалаймыз!</p>
    </div>

</body>
</html>
