# Mini-Loyiha-9-Login-Formasi
Mana, siz aytgan barcha talablarni (kamida 2 ta @keyframes, animation qisqartmasi, transition bilan hover, transform effektlari, animation-delay ketma-ketligi va animation-direction: alternate) o'z ichiga olgan zamonaviy animatsion elementlar to'plami.

Siz buni to'g'ridan-to'g'ri HTML va CSS faylingizga qo'shib tekshirib ko'rishingiz mumkin:

HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Animatsiyalar</title>
    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            background-color: #0f172a;
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            margin: 0;
            gap: 40px;
        }

        .container {
            display: flex;
            gap: 20px;
        }

        /* =======================================================
           1-ANIMATSIYA: @keyframes pulse-glow va Ketma-ketlik (Delay)
           ======================================================= */
        @keyframes pulse-glow {
            0% {
                transform: scale(1);
                box-shadow: 0 0 10px rgba(99, 102, 241, 0.5);
            }
            100% {
                /* transform: scale ishlatildi */
                transform: scale(1.1); 
                box-shadow: 0 0 25px rgba(99, 102, 241, 0.9);
            }
        }

        .box {
            width: 100px;
            height: 100px;
            background: linear-gradient(135deg, #6366f1, #4f46e5);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            
            /* animation: name duration timing-function iteration-count; */
            /* animation-direction: alternate qo'shildi */
            animation: pulse-glow 1.5s ease-in-out infinite alternate;
        }

        /* animation-delay yordamida ketma-ket (staggered) effekt yaratish */
        .box:nth-child(2) {
            animation-delay: 0.3s;
            background: linear-gradient(135deg, #ec4899, #d946ef);
        }

        .box:nth-child(3) {
            animation-delay: 0.6s;
            background: linear-gradient(135deg, #14b8a6, #0d9488);
        }


        /* =======================================================
           2-ANIMATSIYA: @keyframes float-move
           ======================================================= */
        @keyframes float-move {
            0% {
                /* transform: translateX va rotate ishlatildi */
                transform: translateX(0) rotate(0deg);
            }
            100% {
                transform: translateX(30px) rotate(10deg);
            }
        }

        .badge {
            padding: 15px 30px;
            background-color: #1e293b;
            border: 2px solid #38bdf8;
            border-radius: 50px;
            cursor: pointer;
            font-size: 18px;
            color: #38bdf8;
            
            /* animation qisqartmasi va alternate */
            animation: float-move 2s ease-in-out infinite alternate;
            
            /* Transition hover animatsiyasi uchun tayyorlanadi */
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        /* Transition bilan hover animatsiyasi */
        .badge:hover {
            /* Hover bo'lganda animatsiya to'xtaydi va transform o'zgaradi */
            animation-play-state: paused; 
            background-color: #38bdf8;
            color: #1e293b;
            transform: scale(1.2) rotate(-5deg);
            box-shadow: 0 10px 20px rgba(56, 189, 248, 0.4);
        }
    </style>
</head>
<body>

    <div class="container">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
    </div>

    <div class="badge">Hover & Animatsiya</div>

</body>
</html>
Kod qanday ishlamoqda:
@keyframes (Kamida 2 ta): Kodda pulse-glow va float-move nomli ikkita alohida animatsiya bloki yaratildi.

animation qisqartmasi: .box ichida animation: pulse-glow 1.5s ease-in-out infinite alternate; ko'rinishida yozildi.

animation-direction: alternate: Bu xususiyat tufayli animatsiya tugagach, orqaga qarab (0% dan 100% ga, keyin esa 100% dan 0% ga) silliq qaytadi.

transform turlari:

scale(1.1) — .box elementlarini kattalashtirish uchun.

translateX(30px) rotate(10deg) — .badge elementini yonga surish va burish uchun.

animation-delay: .box:nth-child(2) va (3) elementlariga mos ravishda 0.3s va 0.6s kechikish berildi. Bu ularning to'lqinsimon, ketma-ket harakatlanishini ta'minlaydi.

transition bilan hover: .badge elementiga sichqoncha olib borilganda, transition: all 0.4s tufayli uning rangi, o'lchami (scale) va burilishi judayam silliq o'zgaradi.
