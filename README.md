# egypt-tour-guide
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الدليل السياحي لمصر</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <nav>
            <h1>الدليل السياحي لمصر</h1>
            <ul>
                <li><a href="#home">الرئيسية</a></li>
                <li><a href="#destinations">الوجهات</a></li>
                <li><a href="#services">الخدمات</a></li>
                <li><a href="#contact">اتصل بنا</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="hero">
        <div class="hero-text">
            <h2>اكتشف جمال مصر</h2>
            <p>أهرامات الجيزة، نهر النيل، الإسكندرية، الأقصر وأسوان… كل هذا بانتظارك!</p>
            <a href="#destinations" class="btn">ابدأ رحلتك</a>
        </div>
    </section>

    <section id="destinations" class="section">
        <h2 class="section-title">أشهر الوجهات السياحية</h2>
        <div class="cards">

            <div class="card">
                <img src="https://upload.wikimedia.org/wikipedia/commons/e/e3/Kheops-Pyramid.jpg" alt="الأهرامات">
                <h3>الأهرامات – الجيزة</h3>
                <p>واحدة من عجائب الدنيا السبع وأشهر المعالم السياحية في العالم.</p>
            </div>

            <div class="card">
                <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Nile_River_in_Cairo.jpg" alt="نهر النيل">
                <h3>نهر النيل – القاهرة</h3>
                <p>أطول نهر في العالم، يحكي تاريخ حضارة تمتد لآلاف السنين.</p>
            </div>

            <div class="card">
                <img src="https://upload.wikimedia.org/wikipedia/commons/5/54/Luxor_Temple.jpg" alt="الأقصر">
                <h3>الأقصر</h3>
                <p>أكبر متحف مفتوح في العالم، معابد وتماثيل فرعونية مهيبة.</p>
            </div>

            <div class="card">
                <img src="https://upload.wikimedia.org/wikipedia/commons/3/39/Aswan_Egypt.jpg" alt="أسوان">
                <h3>أسوان</h3>
                <p>مدينة الهدوء والجمال، ملتقى التاريخ بالنوبة.</p>
            </div>

        </div>
    </section>

    <section id="services" class="section services">
        <h2 class="section-title">خدماتنا</h2>
        <ul>
            <li>حجز جولات سياحية في أنحاء مصر</li>
            <li>خدمة سيارات مع سائق</li>
            <li>حجز فنادق بأسعار خاصة</li>
            <li>مرشدين سياحيين محترفين</li>
        </ul>
    </section>

    <section id="contact" class="section contact">
        <h2 class="section-title">اتصل بنا</h2>
        <form id="contactForm">
            <input type="text" placeholder="الاسم" required>
            <input type="email" placeholder="البريد الإلكتروني" required>
            <textarea placeholder="رسالتك" required></textarea>
            <button type="submit">إرسال</button>
        </form>
        <p id="formMessage"></p>
    </section>

    <footer>
        <p>© 2025 الدليل السياحي لمصر. جميع الحقوق محفوظة.</p>
    </footer>

    <script src="script.js"></script>

</body>
</html>
body {
    margin: 0;
    font-family: "Cairo", sans-serif;
    background: #fafafa;
}

header {
    background: #a30000;
    color: white;
    padding: 10px 0;
}

nav {
    width: 90%;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 20px;
}

nav ul li a {
    text-decoration: none;
    color: white;
    font-weight: bold;
}

.hero {
    background: url('https://upload.wikimedia.org/wikipedia/commons/e/e3/Kheops-Pyramid.jpg') center/cover no-repeat;
    height: 80vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.hero-text {
    background: rgba(0,0,0,0.5);
    padding: 30px;
    text-align: center;
    color: white;
    border-radius: 10px;
}

.btn {
    background: #ffd700;
    color: black;
    padding: 10px 20px;
    margin-top: 15px;
    display: inline-block;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
}

.section {
    padding: 50px 0;
    width: 90%;
    margin: auto;
}

.section-title {
    text-align: center;
    margin-bottom: 30px;
    font-size: 30px;
    color: #a30000;
}

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

.card {
    background: white;
    padding: 15px;
    border-radius: 10px;
    box-shadow: 0 3px 10px rgba(0,0,0,0.1);
    text-align: center;
}

.card img {
    width: 100%;
    border-radius: 10px;
}

.services ul {
    list-style: none;
    line-height: 2;
    font-size: 18px;
}

.contact form {
    display: grid;
    gap: 15px;
    max-width: 400px;
    margin: auto;
}

.contact input, .contact textarea {
    padding: 10px;
    border-radius: 5px;
    border: 1px solid #aaa;
}

button {
    background: #a30000;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
}

footer {
    background: #333;
    color: white;
    text-align: center;
    padding: 10px;
}
document.getElementById("contactForm").addEventListener("submit", function(e) {
    e.preventDefault();
    document.getElementById("formMessage").textContent = "تم إرسال رسالتك بنجاح! سنعود إليك قريبًا.";
});
