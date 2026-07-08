# htrml-csssssss
Mana, topshiriq shartlariga to'liq javob beradigan, har bir element turi alohida bo'limlarga ajratilgan va vizual ko'rinishga ega HTML va CSS kodi:

HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Elementlar Turlari</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            background-color: #f4f6f9;
        }
        .section {
            background-color: #ffffff;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            padding: 20px;
            margin-bottom: 25px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }
        h3 {
            color: #2c3e50;
            margin-top: 0;
            border-bottom: 2px solid #3498db;
            padding-bottom: 5px;
        }
        p.description {
            color: #7f8c8d;
            font-style: italic;
            margin-bottom: 15px;
        }
        /* Block elementlar uchun stillar */
        .block-element {
            background-color: #3498db;
            color: white;
            padding: 10px;
            margin: 10px 0;
            border-radius: 4px;
        }
        /* Inline elementlar uchun stillar */
        .inline-element {
            background-color: #2ecc71;
            color: white;
            padding: 5px 10px;
            margin: 0 5px;
            border-radius: 4px;
        }
        /* Inline-block elementlar uchun stillar */
        .inline-block-element {
            display: inline-block;
            width: 120px;
            height: 60px;
            background-color: #e67e22;
            color: white;
            text-align: center;
            line-height: 60px; /* Matnni vertikal markazlash */
            margin: 5px;
            border-radius: 4px;
            font-weight: bold;
        }
    </style>
</head>
<body>

    <div class="section">
        <h3>1. Block Elementlar (div)</h3>
        <p class="description">Block elementlar har doim yangi qatordan boshlanadi va mavjud bo'lgan butun kenglikni egallaydi.</p>
        
        <div class="block-element">1-kodli blok (Birinchi div)</div>
        <div class="block-element">2-kodli blok (Ikkinchi div)</div>
        <div class="block-element">3-kodli blok (Uchinchi div)</div>
    </div>

    <div class="section">
        <h3>2. Inline Elementlar (span)</h3>
        <p class="description">Inline elementlar yangi qatordan boshlanmaydi va faqat o'ziga kerakli bo'lgan kenglikni egallab, bir qatorda joylashadi.</p>
        
        <span class="inline-element">Span 1</span>
        <span class="inline-element">Span 2</span>
        <span class="inline-element">Span 3</span>
        <span class="inline-element">Span 4</span>
        <span class="inline-element">Span 5</span>
    </div>

    <div class="section">
        <h3>3. Inline-Block Elementlar</h3>
        <p class="description">Inline-block elementlar xuddi inline kabi bir qatorda joylashadi, lekin ularga blok elementlari kabi width (kenglik) va height (balandlik) berish imkoniyati mavjud.</p>
        
        <div class="inline-block-element">Blok 1</div>
        <div class="inline-block-element">Blok 2</div>
        <div class="inline-block-element">Blok 3</div>
    </div>

</body>
</html>
Kodning asosiy xususiyatlari:
Struktura: Har bir bo'lim alohida h3 sarlavhasi va izohli p (paragraph) bilan boshlanadi.

Vizual ajratish: Har bir bo'lim oq fonda, atrofi kulrang chegara (border) va soya (box-shadow) bilan chiroyli ramkaga olingan.

Ranglar yordamida farqlash: * div (block) elementlari ko'k rangda va har biri yangi qatorda.

span (inline) elementlari yashil rangda va yonma-yon joylashgan.

inline-block elementlari to'q sariq rangda, yonma-yon joylashgan hamda ularga maxsus width: 120px va height: 60px o'lchamlari berilgan.
