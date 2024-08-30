<!DOCTYPE html>
<html lang="id">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ghaisan Utama Indomedia</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #eaeaea;
            color: #333;
            line-height: 1.6;
        }

        nav {
            background-color: #1d1d1d;
            color: #fff;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: background-color 0.3s;
        }

        nav.scrolled {
            background-color: #333;
        }

        nav .logo {
            font-size: 2rem;
            font-weight: bold;
            letter-spacing: 1px;
            color: #ff6f61;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.3s, transform 0.3s;
        }

        nav ul li a:hover {
            color: #ff6f61;
            transform: scale(1.05);
        }

        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
                url('foto1.jpg') no-repeat center center/cover;
            height: 100vh;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 20px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin: 0;
            padding: 0;
            line-height: 1.2;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        .hero-content p {
            font-size: 1.4rem;
            margin-top: 20px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
        }

        .section {
            padding: 80px 20px;
            position: relative;
        }

        .section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #fff;
            transform: skewY(-4deg);
            transform-origin: top left;
            z-index: -1;
            clip-path: polygon(0 0, 100% 0, 100% 100%, 0 95%);
        }

        h2 {
            text-align: center;
            font-size: 2.8rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
            color: #ff6f61;
        }

        h2::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: #ff6f61;
            margin: 10px auto 0;
            border-radius: 2px;
        }

        .timeline {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .timeline-item {
            position: relative;
            padding: 20px;
            border-left: 4px solid #ff6f61;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .timeline-item h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: #333;
        }

        .timeline-item p {
            margin: 0;
            color: #666;
        }

        .services-cards {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
        }

        .card {
            background-color: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            flex: 1 1 calc(33% - 40px);
            margin: 20px;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .card:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }

        .card h3 {
            margin-bottom: 15px;
            font-size: 1.6rem;
            color: #333;
        }

        .portfolio-gallery {
            display: flex;
            gap: 20px;
            justify-content: center;
            flex-wrap: nowrap;
            overflow-x: auto;
        }

        .gallery-item {
            flex: 0 0 auto;
            text-align: center;
            margin: 0;
        }

        .gallery-item img {
            width: 150px;
            height: 150px;
            object-fit: contain;
            border-radius: 10px;
            transition: transform 0.3s;
        }

        .gallery-item img:hover {
            transform: scale(1.05);
        }

        footer {
            background-color: #1d1d1d;
            color: #fff;
            text-align: center;
            padding: 20px 0;
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
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .footer-socials a:hover {
            color: #ff6f61;
        }

        iframe {
            border: 0;
        }

        /* Modal styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1001;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.9);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            max-width: 90%;
            margin: auto;
        }

        .modal-content img {
            max-width: 45%;
            border-radius: 10px;
            margin: 10px;
            transition: transform 0.3s;
        }

        .modal-content img:hover {
            transform: scale(1.05);
        }

        .close {
            position: absolute;
            top: 20px;
            right: 35px;
            color: #fff;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: #ff6f61;
            text-decoration: none;
            cursor: pointer;
        }

        @media only screen and (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .hero-content p {
                font-size: 1.2rem;
            }

            h2 {
                font-size: 2.2rem;
            }

            .card {
                flex: 1 1 calc(100% - 40px);
            }

            .services-cards,
            .portfolio-gallery {
                flex-direction: column;
                gap: 10px;
            }

            .portfolio-gallery {
                overflow-x: scroll;
            }

            .modal-content img {
                max-width: 80%;
                margin: 5px;
            }
        }
    </style>
</head>

<body>
    <!-- Navigation -->
    <nav id="navbar">
        <div class="logo">Ghaisan Utama Indomedia</div>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#portfolio">Portfolio</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Welcome to Ghaisan Utama Indomedia</h1>
            <p>Your Solution for Innovative Media and Design</p>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section">
        <div class="container">
            <h2>About Us</h2>
            <p>Ghaisan Utama Indomedia adalah perusahaan yang bergerak di bidang media dan desain yang inovatif. Kami
                menyediakan solusi terbaik untuk kebutuhan media Anda.</p>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="section">
        <div class="container">
            <h2>Experience</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <h3>2023 - Launch of Innovative Media Platform</h3>
                    <p>Kami meluncurkan platform media inovatif yang telah digunakan oleh berbagai perusahaan besar
                        untuk
                        meningkatkan
                        efisiensi
                        komunikasi mereka.</p>
                </div>
                <div class="timeline-item">
                    <h3>2022 - Expansion into International Markets</h3>
                    <p>Kami memperluas layanan kami ke pasar internasional, dengan fokus pada kualitas dan keandalan.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section">
        <div class="container">
            <h2>Our Services</h2>
            <div class="services-cards">
                <div class="card">
                    <h3>Web Development</h3>
                    <p>Kami membangun situs web yang responsif dan dinamis untuk bisnis Anda.</p>
                </div>
                <div class="card">
                    <h3>Graphic Design</h3>
                    <p>Desain grafis yang menarik dan profesional untuk kebutuhan pemasaran Anda.</p>
                </div>
                <div class="card">
                    <h3>Media Strategy</h3>
                    <p>Strategi media yang efektif untuk mencapai audiens yang tepat.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio" class="section">
        <div class="container">
            <h2>Our Portfolio</h2>
            <div class="portfolio-gallery">
                <div class="gallery-item">
                    <img src="portfolio1.jpg" alt="Project 1">
                </div>
                <div class="gallery-item">
                    <img src="portfolio2.jpg" alt="Project 2">
                </div>
                <div class="gallery-item">
                    <img src="portfolio3.jpg" alt="Project 3">
                </div>
                <div class="gallery-item">
                    <img src="portfolio4.jpg" alt="Project 4">
                </div>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer id="contact">
        <div>
            <p>&copy; 2024 Ghaisan Utama Indomedia. All Rights Reserved.</p>
            <div class="footer-socials">
                <a href="#"><img src="whatsapp-icon.png" alt="WhatsApp"></a>
                <a href="#"><img src="instagram-icon.png" alt="Instagram"></a>
                <a href="#"><img src="email-icon.png" alt="Email"></a>
            </div>
            <p>
                <iframe src="https://open.spotify.com/embed/track/yourtrackid" width="300" height="80" frameborder="0"
                    allowtransparency="true" allow="encrypted-media"></iframe>
            </p>
        </div>
    </footer>

    <!-- Modal -->
    <div id="modal" class="modal">
        <span class="close">&times;</span>
        <div class="modal-content">
            <img src="portfolio1.jpg" alt="Project 1">
            <img src="portfolio2.jpg" alt="Project 2">
            <img src="portfolio3.jpg" alt="Project 3">
            <img src="portfolio4.jpg" alt="Project 4">
        </div>
    </div>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', function () {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 100) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Modal functionality
        const modal = document.getElementById('modal');
        const closeBtn = document.querySelector('.close');
        const galleryItems = document.querySelectorAll('.gallery-item img');

        galleryItems.forEach(item => {
            item.addEventListener('click', function () {
                modal.style.display = 'flex';
                const modalContent = document.querySelector('.modal-content');
                modalContent.innerHTML = `<img src="${this.src}" alt="${this.alt}">`;
            });
        });

        closeBtn.addEventListener('click', function () {
            modal.style.display = 'none';
        });

        window.addEventListener('click', function (e) {
            if (e.target === modal) {
                modal.style.display = 'none';
            }
        });
    </script>
</body>

</html>
