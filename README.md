<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقع مبيعات فرع الإسكندرية</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #0056b3;
            padding: 10px 0;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
        }
        nav a:hover {
            text-decoration: underline;
        }
        section {
            padding: 20px;
        }
        .products {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }
        .product {
            background: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 15px;
            text-align: center;
            width: 200px;
        }
        .product img {
            width: 100%;
            height: auto;
            border-radius: 5px;
        }
        .product h3 {
            margin: 10px 0;
        }
        .product p {
            margin: 5px 0;
            color: #007bff;
            font-weight: bold;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            margin-top: 20px;
        }
        .language-switch {
            text-align: center;
            margin-top: 10px;
        }
        .language-switch button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 0 5px;
            cursor: pointer;
            border-radius: 5px;
        }
        .language-switch button:hover {
            background-color: #0056b3;
        }
        .contact-info {
            margin-top: 20px;
            background: #fff;
            padding: 15px;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        .contact-info p {
            margin: 5px 0;
        }
    </style>
    <script>
        const content = {
            ar: {
                title: "موقع مبيعات فرع الإسكندرية",
                home: "الرئيسية",
                products: "المنتجات",
                contact: "اتصل بنا",
                about: "نحن متخصصون في تقديم أفضل غرسات الأسنان السويسرية بأعلى جودة تحت علامة Roott.",
                productsSection: "المنتجات",
                contactSection: "اتصل بنا",
                send: "إرسال",
                footer: "جميع الحقوق محفوظة &copy; 2025",
                address: "العصافرة بحري، شارع سليمان الفارسي، بجوار جزارة الحمد",
                phone: "رقم الهاتف: 01099331401",
                implants: [
                    { name: "غرسة أسنان ROOTT R", price: "3700 جنيه" },
                    { name: "غرسة أسنان ROOTT C COMPRESSIVE", price: "3000 جنيه" },
                    { name: "غرسة أسنان ROOTT M", price: "3300 جنيه" },
                    { name: "Healing abutment", price: "650 جنيه" }
                ]
            },
            en: {
                title: "Alexandria Branch Sales Website",
                home: "Home",
                products: "Products",
                contact: "Contact Us",
                about: "We specialize in providing the best Swiss dental implants with top quality under the Roott brand.",
                productsSection: "Products",
                contactSection: "Contact Us",
                send: "Send",
                footer: "All rights reserved &copy; 2025",
                address: "Al Asafra Bahri, Suleiman Al-Farsi Street, next to Al-Hamd Butchery",
                phone: "Phone: 01099331401",
                implants: [
                    { name: "ROOTT R Dental Implant", price: "3700 EGP" },
                    { name: "ROOTT C COMPRESSIVE Dental Implant", price: "3000 EGP" },
                    { name: "ROOTT M Dental Implant", price: "3300 EGP" },
                    { name: "Healing abutment", price: "650 EGP" }
                ]
            }
        };

        function switchLanguage(lang) {
            document.title = content[lang].title;
            document.getElementById("home-link").textContent = content[lang].home;
            document.getElementById("products-link").textContent = content[lang].products;
            document.getElementById("contact-link").textContent = content[lang].contact;
            document.getElementById("about").textContent = content[lang].about;
            document.getElementById("products-section-title").textContent = content[lang].productsSection;
            document.getElementById("contact-section-title").textContent = content[lang].contactSection;
            document.getElementById("footer").innerHTML = content[lang].footer;
            document.getElementById("address").textContent = content[lang].address;
            document.getElementById("phone").textContent = content[lang].phone;

            const productsContainer = document.getElementById("products-container");
            productsContainer.innerHTML = "";
            content[lang].implants.forEach(product => {
                const productDiv = document.createElement("div");
                productDiv.classList.add("product");
                productDiv.innerHTML = `
                    <img src="https://via.placeholder.com/200" alt="${product.name}">
                    <h3>${product.name}</h3>
                    <p>${product.price}</p>
                `;
                productsContainer.appendChild(productDiv);
            });
        }
    </script>
</head>
<body onload="switchLanguage('ar')">
    <header>
        <h1 id="title">موقع مبيعات فرع الإسكندرية</h1>
    </header>
    <nav>
        <a href="#home" id="home-link">الرئيسية</a>
        <a href="#products" id="products-link">المنتجات</a>
        <a href="#contact" id="contact-link">اتصل بنا</a>
    </nav>
    <section id="home">
        <h2>نبذة عن الفرع</h2>
        <p id="about">نحن متخصصون في تقديم أفضل غرسات الأسنان السويسرية بأعلى جودة تحت علامة Roott.</p>
    </section>
    <section id="products">
        <h2 id="products-section-title">المنتجات</h2>
        <div class="products" id="products-container"></div>
    </section>
    <section id="contact">
        <h2 id="contact-section-title">اتصل بنا</h2>
        <div class="contact-form">
            <input type="text" placeholder="الاسم" required>
            <input type="email" placeholder="البريد الإلكتروني" required>
            <textarea placeholder="رسالتك" rows="5" required></textarea>
            <button type="submit" id="send-button">إرسال</button>
        </div>
        <div class="contact-info">
            <p id="address">العصافرة بحري، شارع سليمان الفارسي، بجوار جزارة الحمد</p>
            <p id="phone">رقم الهاتف: 01099331401</p>
        </div>
    </section>
    <footer>
        <p id="footer">جميع الحقوق محفوظة &copy; 2025</p>
        <div class="language-switch">
            <button onclick="switchLanguage('ar')">العربية</button>
            <button onclick="switchLanguage('en')">English</button>
        </div>
    </footer>
</body>
</html>
