# Mini-Loyiha-9-Login-Formasi

Conversation with Gemini
✅ Forma sahifa markazida (flexbox)

✅ Input: border, padding, border-radius

✅ input:focus { border-color: ...; outline: none; }

✅ Tugma hover da rang o'zgarsin

✅ box-shadow bilan forma kartochkasi

✅ ::placeholder rangini o'zgartiring\

Mana yuqoridagi barcha talablarga javob beradigan to'liq HTML va CSS kodi. Bu kod orqali forma aniq sahifa markaziga joylashadi va chiroyli zamonaviy dizaynga ega bo'ladi.

HTML partiyasi (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chiroyli Forma</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="form-container">
        <h2>Tizimga kirish</h2>
        <form>
            <div class="input-group">
                <input type="email" placeholder="Elektron pochta manzili" required>
            </div>
            <div class="input-group">
                <input type="password" placeholder="Parol" required>
            </div>
            <button type="submit" class="submit-btn">Yuborish</button>
        </form>
    </div>

</body>
</html>
CSS partiyasi (style.css)
CSS
/* Sahifani to'liq tozalash va flexbox orqali markazlashtirish */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-color: #f4f7f6;
}

/* Box-shadow bilan forma kartochkasi */
.form-container {
    background-color: #ffffff;
    padding: 30px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1); /* Chiroyli soya */
    width: 100%;
    max-width: 400px;
}

.form-container h2 {
    margin-bottom: 20px;
    color: #333;
    text-align: center;
}

.input-group {
    margin-bottom: 20px;
}

/* Input: border, padding, border-radius */
.input-group input {
    width: 100%;
    padding: 12px 15px;
    border: 2px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    color: #333;
    transition: border-color 0.3s ease;
}

/* input:focus { border-color: ...; outline: none; } */
.input-group input:focus {
    border-color: #4a90e2; /* Fokus bo'lgandagi rang */
    outline: none; /* Standart ko'k chiziqni yo'qotish */
}

/* ::placeholder rangini o'zgartirish */
.input-group input::placeholder {
    color: #999999;
    font-style: italic;
}

/* Tugma uslubi */
.submit-btn {
    width: 100%;
    padding: 12px;
    background-color: #4a90e2;
    color: white;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

/* Tugma hover da rang o'zgarsin */
.submit-btn:hover {
    background-color: #357abd; /* To'qroq ko'k rang */
}
Nimalar bajarildi?
Flexbox markazlashtirish: body qismiga display: flex, justify-content: center va align-items: center berilib, forma ekranning roppa-rosa o'rtasiga keltirildi.

Chiroyli soya: .form-containerga mayin va zamonaviy box-shadow berildi.

Inputlar: Padding, border va chetlari yumaloq (border-radius) holatga keltirildi. Fokus bo'lganda (:focus) tashqi chiziq yo'qolib, border rangi ko'kka o'zgaradi.

Placeholder: ::placeholder selektori yordamida ichidagi matn rangi och kulrang va kursiv qilindi.

Hover effekti: Tugma ustiga sichqoncha olib borilganda (:hover) rangi silliq o'zgarishi uchun transition ishlatildi.




Gemini isn’t human. It can make mistakes, so double-check it.

