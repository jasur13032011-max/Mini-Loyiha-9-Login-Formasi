# Mini-Loyiha-9-Login-Formasi
Mana, siz aytgan barcha talablarga javob beradigan, zamonaviy va chiroyli stillashtirilgan HTML va CSS kodlari majmuasi.

Siz bu kodlarni to'g'ridan-to'g'ri loyihangizga ko'chirib o'tkazib ishlatishingiz mumkin:

HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Stillashtirilgan Forma</title>
    <style>
        /* Umumiy stillar */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f7f6;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .form-container {
            background-color: #ffffff;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 450px;
        }

        /* 1. Forma sarlavhasi stillashtirish */
        .form-title {
            font-size: 24px;
            font-weight: 700;
            color: #333;
            margin-bottom: 25px;
            text-align: center;
            position: relative;
            padding-bottom: 8px;
        }

        .form-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 2px;
        }

        /* 2. Label + Input juftligi */
        .form-group {
            margin-bottom: 20px;
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-size: 14px;
            font-weight: 600;
            color: #555;
            margin-bottom: 8px;
        }

        .form-group input[type="text"],
        .form-group input[type="email"],
        /* 3. Select elementi */
        .form-group select {
            padding: 12px;
            border: 1.5px solid #e0e0e0;
            border-radius: 8px;
            font-size: 15px;
            outline: none;
            transition: border-color 0.3s ease;
            background-color: #fafafa;
        }

        .form-group input:focus,
        .form-group select:focus {
            border-color: #667eea;
            background-color: #fff;
        }

        /* 5. Accent-color bilan Checkbox va Radio */
        .choice-group {
            margin-bottom: 20px;
        }

        .choice-title {
            font-size: 14px;
            font-weight: 600;
            color: #555;
            margin-bottom: 10px;
        }

        .checkbox-label, .radio-label {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 15px;
            color: #444;
            margin-bottom: 8px;
            cursor: pointer;
        }

        .checkbox-label input, .radio-label input {
            width: 18px;
            height: 18px;
            accent-color: #667eea; /* Checkbox/Radio rangi */
            cursor: pointer;
        }

        /* 6. Xato holati */
        .error {
            border-color: #ff4d4d !important;
            background-color: #fff8f8 !important;
        }

        .error-message {
            color: #ff4d4d;
            font-size: 12px;
            margin-top: 5px;
            font-weight: 500;
        }

        /* 4. Tugma: to'liq kenglikda va hover gradient */
        .btn-submit {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 8px;
            color: white;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            background-size: 200% auto;
            transition: 0.5s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.4);
        }

        .btn-submit:hover {
            background-position: right center; /* Gradient siljishi */
            box-shadow: 0 6px 20px rgba(118, 75, 162, 0.4);
        }
    </style>
</head>
<body>

<div class="form-container">
    <h2 class="form-title">Ro'yxatdan o'tish</h2>

    <form>
        <div class="form-group">
            <label for="username">Foydalanuvchi nomi</label>
            <input type="text" id="username" placeholder="Masalan: templates_uz">
        </div>

        <div class="form-group">
            <label for="email">Elektron pochta</label>
            <input type="email" id="email" class="error" value="notogri-elektron-pochta@" placeholder="example@mail.com">
            <span class="error-message">Iltimos, to'g'ri elektron pochta kiriting.</span>
        </div>

        <div class="form-group">
            <label for="country">Viloyatni tanlang</label>
            <select id="country">
                <option value="toshkent">Toshkent</option>
                <option value="samarqand">Samarqand</option>
                <option value="fargona">Farg'ona</option>
            </select>
        </div>

        <div class="choice-group">
            <div class="choice-title">Jinsingiz</div>
            <label class="radio-label">
                <input type="radio" name="gender" value="male" checked> Erkak
            </label>
            <label class="radio-label">
                <input type="radio" name="gender" value="female"> Ayol
            </label>
        </div>

        <div class="choice-group">
            <div class="choice-title">Shartlar</div>
            <label class="checkbox-label">
                <input type="checkbox" id="terms" checked> Shartlarga roziman
            </label>
        </div>

        <button type="submit" class="btn-submit">Yuborish</button>
    </form>
</div>

</body>
</html>
Kodning asosiy xususiyatlari:
Sarlavha: Chiroyli gradient chiziqcha bilan bezatilgan.

Accent-color: Checkbox va Radio tugmalari brauzerning standart ko'k rangida emas, dizaynga mos accent-color: #667eea; rangi orqali stillashtirilgan.

Hover Gradient: btn-submit tugmasi ustiga sichqoncha olib borilganda (hover), gradient rangi silliq siljiydi (background-position).

Xato holati (.error): email inputida xato holati qizil chegara (border-color: red) va och qizil fon bilan ko'rsatilgan.
