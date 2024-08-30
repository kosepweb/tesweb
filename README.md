<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Contoh website responsif dan kreatif">
    <title>Website Kreatif dan Responsif</title>
    <style>
        /* Reset browser defaults */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f4f4f4;
        }

        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #333;
            color: white;
            padding: 10px 20px;
        }

        .logo h1 {
            margin: 0;
        }

        .navbar ul {
            list-style-type: none;
            display: flex;
        }

        .navbar ul li {
            margin: 0 10px;
        }

        .navbar ul li a {
            color: white;
            text-decoration: none;
        }

        .hamburger {
            display: none;
            flex-direction: column;
            cursor: pointer;
        }

        .hamburger span {
            width: 25px;
            height: 3px;
            background: white;
            margin: 4px;
        }

        .hero {
            text-align: center;
            padding: 100px 20px;
            background: #333;
            color: white;
        }

        .hero h2 {
            font-size: 2.5rem;
        }

        .hero p {
            margin: 20px 0;
        }

        .cta-button {
            display: inline-block;
            padding: 10px 20px;
            background: #f44336;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s;
        }

        .cta-button:hover {
            background: #e53935;
        }

        section {
            padding: 50px 20px;
            text-align: center;
        }

        footer {
            text-align: center;
            padding: 20px;
            background: #333;
            color: white;
        }

        @media (max-width: 768px) {
            .navbar ul {
                flex-direction: column;
                position: absolute;
                top: 60px;
                left: -100%;
                width: 100%;
                background: #333;
                transition: all 0.3s;
            }

            .navbar ul.active {
                left: 0;
            }

            .hamburger {
                display: flex;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <h1>Logo</h1>
        </div>
        <nav class="navbar">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <div class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </nav>
    </header>

    <section id="home">
        <div class="hero">
            <h2>Welcome to Our Creative Website</h2>
            <p>We design with passion and create with love.</p>
            <a href="#about" class="cta-button">Learn More</a>
        </div>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>This is a brief description about our company and what we do.</p>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <p>Details about the services we offer.</p>
    </section>

    <footer>
        <p>&copy; 2024 Website Kreatif. All rights reserved.</p>
    </footer>

    <script>
        const hamburger = document.getElementById('hamburger');
        const navUL = document.querySelector('.navbar ul');

        hamburger.addEventListener('click', () => {
            navUL.classList.toggle('active');
        });
    </script>
</body>
</html>
