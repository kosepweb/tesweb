
<html lang="id">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Perusahaan - Ghaisan Utama Indomedia</title>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }

        nav {
            background-color: #1d1d1d;
            color: #fff;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        nav .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #ff6f61;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 15px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }

        header {
            background: url('your-image.jpg') no-repeat center center/cover;
            height: 70vh;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 20px;
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        header p {
            font-size: 1.2rem;
            margin-top: 20px;
        }

        .container {
            max-width: 1100px;
            margin: auto;
            padding: 20px;
        }

        .about, .services, .contact {
            padding: 40px 20px;
            background-color: #fff;
            margin-bottom: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .about h2, .services h2, .contact h2 {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 20px;
            color: #ff6f61;
        }

        .about p, .services p {
            text-align: justify;
        }

        .services .service-cards {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .services .service-card {
            background-color: #f9f9f9;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .services .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }

        .services .service-card p {
            font-size: 1rem;
        }

        footer {
            background-color: #1d1d1d;
            color: #fff;
            text-align: center;
            padding: 10px 0;
        }

        .footer-socials {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 10px;
        }

        .footer-socials a {
            color: #fff;
            text-decoration: none;
            font-size: 1.2rem;
        }

        @media (min-width: 768px) {
            header h1 {
                font-size: 3rem;
            }

            header p {
                font-size: 1.5rem;
            }

            .services .service-cards {
                flex-direction: row;
                flex-wrap: wrap;
                gap: 20px;
            }

            .services .service-card {
                flex: 1 1 calc(33% - 40px);
            }
        }
    </style>
</head>

<body>
    <nav>
        <div class="logo">Ghaisan Utama Indomedia</div>
        <ul>
            <li><a href="#about">Tentang Kami</a></li>
            <li><a href="#services">Layanan</a></li>
            <li><a href="#contact">Kontak</a></li>
        </ul>
    </nav>

    <header>
        <div>
            <h1>Selamat Datang di Ghaisan Utama Indomedia</h1>
            <p>Kreativitas tanpa batas, Solusi yang tepat</p>
        </div>
    </header>

    <div class="container">
        <section id="about" class="about">
            <h2>Tentang Kami</h2>
            <p>Ghaisan Utama Indomedia adalah perusahaan yang bergerak di bidang industri kreatif, menyediakan layanan terbaik di bidang event organizing, konstruksi, dan multimedia. Dengan pengalaman lebih dari satu dekade, kami berkomitmen untuk memberikan hasil terbaik bagi klien kami.</p>
        </section>

        <section id="services" class="services">
            <h2>Layanan Kami</h2>
            <div class="service-cards">
                <div class="service-card">
                    <h3>Event Organizer</h3>
                    <p>Mengelola berbagai acara formal maupun non-formal dengan sentuhan profesionalisme yang tinggi.</p>
                </div>
                <div class="service-card">
                    <h3>Konstruksi</h3>
                    <p>Menyediakan solusi konstruksi dari perencanaan hingga pelaksanaan dengan standar kualitas terbaik.</p>
                </div>
                <div class="service-card">
                    <h3>Multimedia</h3>
                    <p>Menyajikan layanan multimedia yang meliputi fotografi, videografi, dan desain grafis dengan hasil yang memukau.</p>
                </div>
            </div>
        </section>

        <section id="contact" class="contact">
            <h2>Kontak Kami</h2>
            <p>Hubungi kami untuk informasi lebih lanjut atau konsultasi:</p>
            <p>Email: <a href="mailto:info@ghaisanindomedia.com">info@ghaisanindomedia.com</a></p>
            <p>Telepon: <a href="tel:+621234567890">+62 123-4567-890</a></p>
            <p>Alamat: Jl. Bakti Komp Ruko Bakti Soho Center, Kota Makassar, Sulawesi Selatan</p>
        </section>
    </div>

    <footer>
        <p>&copy; 2009-2024 Ghaisan Utama Indomedia. All rights reserved.</p>
        <div class="footer-socials">
            <a href="#">Instagram</a>
            <a href="#">Facebook</a>
            <a href="https://wa.me/621234567890" target="_blank">WhatsApp</a>
        </div>
    </footer>
</body>

</html>
