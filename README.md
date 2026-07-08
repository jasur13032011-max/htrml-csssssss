# htrml-csssssss
1. HTML (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Card va ID/Class Amaliyoti</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header id="header">
        <h1>Bizning Maxsus Kartalarimiz</h1>
        <p>HTML va CSS yordamida mantiqiy tuzilma</p>
    </header>

    <main class="container">
        <div class="card">
            <div class="card-title">Oddiy Karta 1</div>
            <div class="card-body">Bu standart uslubga ega bo'lgan birinchi kartaning asosiy matn qismidir.</div>
            <div class="card-footer">08.07.2026</div>
        </div>

        <div class="card primary">
            <div class="card-title">Asosiy Karta (Primary)</div>
            <div class="card-body">Bu ko'k rangli variant bo'lib, odatda muhim ma'lumotlarni ajratib ko'rsatish uchun ishlatiladi.</div>
            <div class="card-footer"><a href="#">Batafsil...</a></div>
        </div>

        <div class="card danger">
            <div class="card-title">Xavfli Karta (Danger)</div>
            <div class="card-body">Bu qizil rangli variant bo'lib, ogohlantirish yoki o'chirish kabi harakatlarga ishora qiladi.</div>
            <div class="card-footer">Diqqat qiling!</div>
        </div>

        <div class="card success">
            <div class="card-title">Muvaffaqiyatli Karta (Success)</div>
            <div class="card-body">Yashil rangli variant, muvaffaqiyatli bajarilgan ishlar yoki ijobiy yangiliklar uchun.</div>
            <div class="card-footer">Bajarildi</div>
        </div>

        <div class="card">
            <div class="card-title">Oddiy Karta 2</div>
            <div class="card-body">Yana bir standart karta. Class-lar bir nechta elementda takrorlanishi mumkinligiga misol.</div>
            <div class="card-footer">Aktiv</div>
        </div>

        <div class="card primary">
            <div class="card-title">Yana bir Primary Karta</div>
            <div class="card-body">Kamida 6 ta element bo'lishi sharti uchun yaratilgan oltinchi karta.</div>
            <div class="card-footer">Yakuniy qism</div>
        </div>
    </main>

    <section class="action-zone">
        <button id="cta">Hozir ro'yxatdan o'ting</button>
    </section>

</body>
</html>
2. CSS (style.css)
CSS
/* Umumiy sozlamalar */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f4f6f9;
    margin: 0;
    padding: 0;
    color: #333;
}

.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 20px;
    padding: 40px 20px;
    max-width: 1200px;
    margin: 0 auto;
}

/* --- ID SELECTORS (Faqat 1 marta qo'llaniladi) --- */
#header {
    background-color: #2c3e50;
    color: #ffffff;
    text-align: center;
    padding: 30px 10px;
}

#header h1 {
    margin: 0;
    font-size: 2.5rem;
}

#header p {
    margin: 5px 0 0 0;
    opacity: 0.8;
}

#cta {
    display: block;
    margin: 30px auto;
    padding: 15px 40px;
    font-size: 1.2rem;
    font-weight: bold;
    color: #fff;
    background-color: #e67e22;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    box-shadow: 0 4px 15px rgba(230, 126, 34, 0.4);
    transition: transform 0.2s, background-color 0.2s;
}

#cta:hover {
    background-color: #d35400;
    transform: translateY(-2px);
}

/* --- CLASS SELECTORS (Qayta ishlatiladigan qismlar) --- */
.card {
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
    border-left: 5px solid #bdc3c7; /* Default chet rangi */
    display: flex;
    flex-direction: column;
    overflow: hidden;
}

/* Sub-selectors (Karta ichidagi qismlar) */
.card .card-title {
    font-size: 1.3rem;
    font-weight: bold;
    padding: 15px;
    background-color: #fafbfc;
    border-bottom: 1px solid #eee;
}

.card .card-body {
    padding: 20px;
    font-size: 1rem;
    line-height: 1.5;
    flex-grow: 1; /* Matn kam bo'lsa ham footerni pastga suradi */
}

.card .card-footer {
    padding: 12px 20px;
    background-color: #fdfefe;
    border-top: 1px solid #eee;
    font-size: 0.85rem;
    color: #7f8c8d;
}

/* --- CARD VARIANTS (Turli rang variantlari) --- */
.card.primary {
    border-left-color: #3498db;
}
.card.primary .card-title {
    color: #2980b9;
    background-color: #eaf2f8;
}

.card.danger {
    border-left-color: #e74c3c;
}
.card.danger .card-title {
    color: #c0392b;
    background-color: #fdedec;
}

.card.success {
    border-left-color: #2ecc71;
}
.card.success .card-title {
    color: #27ae60;
    background-color: #e8f8f5;
}

.action-zone {
    text-align: center;
    padding-bottom: 50px;
}
3. README (README.md)
Markdown
# ID va Class Selectors: Farqi va Qo'llanilishi

Veb-sahifani loyihalashda elementlarga uslub (CSS) berish yoki ularni JavaScript-da boshqarish uchun `id` va `class` atributlaridan foydalaniladi. Ularning har birining o'z o'rni va qoidalari bor.

## 1. Class (`.classname`) — Qachon va nima uchun kerak?
* **Ko'p marta ishlatilishi:** Bir xil CSS uslubini sahifadagi bir nechta elementga bir vaqtda qo'llash kerak bo'lganda `class` ishlatiladi.
* **Guruhlash:** Masalan, bizda 6 ta karta (`.card`) bor. Ularning shakli, ichki bo'shliqlari (padding) va soyalari bir xil. Har biriga alohida kod yozmaslik uchun ularga umumiy bitta klass beriladi.
* **Kombinatsiya:** Bitta elementga bir nechta klassni qo'shib yozish mumkin (masalan: `class="card primary"`). Bu kodni qayta ishlatish (reusability) samaradorligini oshiradi.

## 2. ID (`#idname`) — Qachon va nima uchun kerak?
* **Unikallik (Yagonalik):** `id` sahifada faqat va faqat **bitta** elementga berilishi shart. Bitta sahifada bir xil nomli ikki yoki undan ortiq `id` bo'lishi mumkin emas (HTML bunga ruxsat bersa ham, bu qoidabuzarlik hisoblanadi va JS/CSS-da xatolarga olib keladi).
* **Maxsus elementlar:** Sahifada takrorlanmaydigan yagona qismlar uchun ishlatiladi. Masalan:
  * `#header` — Saytning eng yuqori bosh qismi.
  * `#cta` — Foydalanuvchini asosiy harakatga chaqiruvchi yagona tugma (Call to Action).
  * `#main-nav` — Asosiy menyu.
* **Anchor Link (Ssilka bilan sakrash):** ID yordamida sahifaning ma'lum bir qismiga ssilka orqali o'tish (sakrash) mumkin (`<a href="#header">`).

## Xulosa
* Agar uslub yoki element **takrorlansa** -> **Class** ishlating.
* Agar element butun sahifada **yagona va unikal** bo'lsa -> **ID** ishlating.
