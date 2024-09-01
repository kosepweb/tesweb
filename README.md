
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ghaisan Utama Indomedia</title>
  <link rel="stylesheet" href="styles.css" />
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link
    href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap"
    rel="stylesheet"
  />
  <style>
    /* General Styles */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        scroll-behavior: smooth;
    }
    
    body {
        font-family: 'Poppins', sans-serif;
        line-height: 1.6;
        color: #333;
    }
    
    .container {
        width: 90%;
        max-width: 1200px;
        margin: auto;
        padding: 40px 0;
    }
    
    h1, h2, h3, h4 {
        margin-bottom: 20px;
        font-weight: 600;
    }
    
    /* Header */
    header {
        background: #fff;
        padding: px 0;
        position: center;
        width: 100%;
        top: 0;
        z-index: 100;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    }
    
    .logo {
        height: 50px;
    }
    
    nav {
        float: right;
    }
    
    nav ul {
        list-style: none;
        display: flex;
        gap: 20px;
    }
    
    nav a {
        text-decoration: none;
        color: #333;
        font-weight: 500;
        transition: color 0.3s;
    }
    
    nav a:hover {
        color: #007bff;
    }
    
    /* Hero Section */
    .hero {
        background: url('images/hero-bg.jpg') no-repeat center center/cover;
        height: 100vh;
        display: flex;
        align-items: center;
        color: #fff;
        text-align: center;
        position: relative;
        padding-top: 80px;
    }
    
    .hero::after {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
    }
    
    .hero .container {
        position: relative;
        z-index: 1;
    }
    
    .hero h1 {
        font-size: 2.5rem;
        margin-bottom: 20px;
        animation: fadeInDown 1s ease-in-out;
    }
    
    .hero h1 span {
        color: #007bff;
    }
    
    .hero p {
        font-size: 1.2rem;
        margin-bottom: 30px;
        animation: fadeInUp 1s ease-in-out;
    }
    
    .btn {
        display: inline-block;
        padding: 12px 30px;
        background-color: #007bff;
        color: #fff;
        border-radius: 50px;
        text-decoration: none;
        font-weight: 500;
        transition: background-color 0.3s;
    }
    
    .btn:hover {
        background-color: #0056b3;
    }
    
    /* About Section */
    .about {
        background-color: #f9f9f9;
        padding: 80px 0;
    }
    
    .about-content {
        text-align: center;
        animation: fadeIn 1s ease-in-out;
    }
    
    .about p {
        margin-bottom: 20px;
        color: #666;
    }
    
    /* Services Section */
    .services {
        padding: 80px 0;
        text-align: center;
    }
    
    .services-wrapper {
        display: flex;
        flex-wrap: wrap;
        gap: 40px;
        justify-content: center;
        margin-top: 40px;
    }
    
    .service-item {
        background-color: #fff;
        padding: 30px;
        border-radius: 10px;
        width: 300px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s;
        animation: fadeInUp 1s ease-in-out;
    }
    
    .service-item:hover {
        transform: translateY(-10px);
    }
    
    .service-item img {
        height: 80px;
        margin-bottom: 20px;
    }
    
    .service-item h3 {
        margin-bottom: 15px;
        font-size: 1.5rem;
    }
    
    .service-item p {
        color: #666;
    }
    
    /* Portfolio Section */
    .portfolio {
        padding: 80px 0;
        text-align: center;
    }
    
    .portfolio-wrapper {
        display: flex;
        flex-wrap: wrap;
        gap: 40px;
        justify-content: center;
    }
    
    .portfolio-item {
        background-color: #fff;
        padding: 20px;
        border-radius: 10px;
        width: 300px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        cursor: pointer;
        transition: transform 0.3s;
    }
    
    .portfolio-item:hover {
        transform: translateY(-10px);
    }
    
    .portfolio-item img {
        width: 100%;
        height: auto;
        border-radius: 10px;
    }
    
    /* Modal Container */
    .modal {
        display: none; /* Hide by default */
        position: fixed;
        z-index: 1000;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        overflow: auto;
        background-color: rgba(0, 0, 0, 0.8); /* Background overlay */
        justify-content: center;
        align-items: center;
    }
    
    /* Modal Content */
    .modal-content {
        background-color: #fff;
        margin: 15px;
        padding: 20px;
        border-radius: 10px;
        max-width: 90%;
        max-height: 80%;
        overflow: hidden; /* Hide overflow if needed */
        display: flex;
        flex-direction: column;
        align-items: center;
        position: relative;
    }
    
    /* Image inside Modal */
    .modal-content img {
        max-width: 100%;
        max-height: 100%;
        object-fit: contain; /* Maintain aspect ratio */
        display: none;
    }
    
    /* Show the current image */
    .modal-content img.active {
        display: block;
    }
    
    /* Close Button */
    .modal-close {
        color: #aaa;
        float: right;
        font-size: 28px;
        font-weight: bold;
        cursor: pointer;
    }
    
    .modal-close:hover,
    .modal-close:focus {
        color: black;
        text-decoration: none;
        cursor: pointer;
    }
    
    /* Navigation Buttons */
    .modal-prev, .modal-next {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        background-color: rgba(0, 0, 0, 0.5);
        color: #fff;
        border: none;
        padding: 10px;
        cursor: pointer;
        font-size: 24px;
        border-radius: 50%;
        z-index: 1001;
    }
    
    .modal-prev {
        left: 10px;
    }
    
    .modal-next {
        right: 10px;
    }
    
    /* Responsiveness */
    @media (max-width: 768px) {
        .modal-content {
            max-width: 95%;
            max-height: 90%;
        }
    }
    
    /* Animations */
    @keyframes fadeInDown {
        from {
            opacity: 0;
            transform: translateY(-30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    @keyframes fadeInUp {
        from {
            opacity: 0;
            transform: translateY(30px);
        }
        to {
            opacity: 1;
            transform: translateY(0);
        }
    }
    
    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="container" style="display: flex; align-items: center;">
      <img src="logo-gui.png" alt="Logo Perusahaan" class="logo" />
      <div class="company-name" style="margin-left: 15px;">
        <h1></h1>
      </div>
      <nav style="margin-left: auto;">
        <ul>
          <li><a href="#home">Beranda</a></li>
          <li><a href="#about">Tentang Kami</a></li>
          <li><a href="#services">Layanan</a></li>
          <li><a href="#portfolio">Portofolio</a></li>
          <li><a href="#contact">Kontak</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section id="home" class="hero" style="background: url('foto1.jpg') no-repeat center center/cover;">
    <div class="container">
        <h1> <span></span></h1>
        <p>
        </p>
        <a href="#contact" class="btn">Hubungi Kami</a>
    </div>
</section>
  
  <!-- About Section -->
  <section id="about" class="about">
    <div class="container about-content">
      <h2>Tentang Kami</h2>
      <p>
        Kami adalah perusahaan yang berkomitmen untuk memberikan layanan
        terbaik dan solusi inovatif untuk kebutuhan bisnis Anda. Tim kami
        terdiri dari para ahli di berbagai bidang yang siap membantu Anda.
      </p>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="services">
    <div class="container">
      <h2>Services</h2>
      <div class="services-wrapper">
        <div class="service-item">
          <img src="icon2.png" alt="Layanan 1" />
          <h3>Event Organizer Services</h3>
          <p>
            DIdirikan tahun 2009, dan sampai sekarang telah menjadi partner terpercaya oleh banyak perusahaan dan pribadi, untuk keperluan event organizing. Mulai dari acara formal ataupun non-formal yang selalu berhasil meninggalkan kesan tersendiri bagi client
          </p>
        </div>
        <div class="service-item">
          <img src="icon23.png" alt="Layanan 2" />
          <h3>Construction Serice</h3>
          <p>
            Didirikan ditahun 2012 sampai sekarang, didukung tim teknis dan arsitek berpengalaman, menjadi Konsultan Perencanaan serta Pelaksanaan Konstruksi Perumahaan, Pengelolaan Real Estate, Renovasi Rumah dan Kantor Eksterior/Interior
          </p>
        </div>
        <div class="service-item">
          <img src="icon3.png" alt="Layanan 3" />
          <h3>Cinematography Service</h3>
          <p>
            Didirikan ditahun 2015, dan sampai sekarang telah membuat beberapa film layar lebar dengan jumlah penoton yang lebih dari lima ratus ribu orang. Disamping itu Finisia, juga telah memproduksi beberapa video, berupa compay profile, comercial dan lain-lain.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Portfolio Section -->
  <section id="portfolio" class="portfolio">
    <div class="container">
      <h2>Portofolio Kami</h2>
      <div class="portfolio-wrapper">
        <div class="portfolio-item" onclick="openModal('portfolio1')">
          <img src="LOGO ALPRO.png" alt="Portofolio 1" />
        </div>
        <div class="portfolio-item" onclick="openModal('portfolio2')">
          <img src="LOGO dR.jpg" alt="Portofolio 2" />
        </div>
        <div class="portfolio-item" onclick="openModal('portfolio3')">
          <img src="finisia.png" alt="Portofolio 3" />
        </div>
      </div>
    </div>
  </section>

  <!-- Modal for Portfolio 1 -->
  <div id="portfolio1" class="modal">
    <div class="modal-content">
      <span class="modal-close" onclick="closeModal('portfolio1')">&times;</span>
      <button class="modal-prev" onclick="prevImage('portfolio1')">&#10094;</button>
      <button class="modal-next" onclick="nextImage('portfolio1')">&#10095;</button>
      <img src="giias15.jpg" alt="Portofolio 1" class="active" />
      <img src="giias16.jpg" alt="Portofolio 1" />
      <img src="giias17.jpg" alt="Portofolio 1" />
      <img src="GIIAS18.jpg" alt="Portofolio 1" />
      <img src="rei.jpg" alt="Portofolio 1" />
      <img src="karangtaruna.jpg" alt="Portofolio 1" />
      <img src="FEED BMO 1 copy.jpg" alt="Portofolio 1" />
    </div>
  </div>

  <!-- Modal for Portfolio 2 -->
  <div id="portfolio2" class="modal">
    <div class="modal-content">
      <span class="modal-close" onclick="closeModal('portfolio2')">&times;</span>
      <button class="modal-prev" onclick="prevImage('portfolio2')">&#10094;</button>
      <button class="modal-next" onclick="nextImage('portfolio2')">&#10095;</button>
      <img src="dr1.jpg" alt="Portofolio 2" class="active" />
      <img src="dr2.jpg" alt="Portofolio 2" />
      <img src="dr3.jpg" alt="Portofolio 2" />
      <img src="dr4.jpg" alt="Portofolio 2" />
      <img src="dr5.jpg" alt="Portofolio 2" />
      <img src="dr6.jpg" alt="Portofolio 2" />
    </div>
  </div>

  <!-- Modal for Portfolio 3 -->
  <div id="portfolio3" class="modal">
    <div class="modal-content">
      <span class="modal-close" onclick="closeModal('portfolio3')">&times;</span>
      <button class="modal-prev" onclick="prevImage('portfolio3')">&#10094;</button>
      <button class="modal-next" onclick="nextImage('portfolio3')">&#10095;</button>
      <img src="up1.jpg" alt="Portofolio 3" class="active" />
      <img src="halomakassar.jpg" alt="Portofolio 3" />
      <img src="anakmudapalsu.jpg" alt="Portofolio 3" />
      <img src="keluarmain.jpg" alt="Portofolio 3" />
      <img src="up2.jpg" alt="Portofolio 3" />
    </div>
  </div>

  <!-- Contact Section -->
  <section id="contact">
    <div class="container">
      <h2>Kontak Kami</h2>
      <p>
        Hubungi kami untuk informasi lebih lanjut atau jika Anda memiliki
        pertanyaan tentang layanan kami.
      </p>
      <!-- Form Kontak atau informasi kontak -->
    </div>
  </section>

  <!-- JavaScript -->
  <script>
    // Fungsi untuk membuka modal
    function openModal(modalId) {
        document.getElementById(modalId).style.display = 'flex';
    }

    // Fungsi untuk menutup modal
    function closeModal(modalId) {
        document.getElementById(modalId).style.display = 'none';
    }

    // Fungsi untuk navigasi gambar
    function showImage(modalId, index) {
        var modal = document.getElementById(modalId);
        var images = modal.querySelectorAll('.modal-content img');
        if (index >= images.length) index = 0;
        if (index < 0) index = images.length - 1;
        images.forEach((img, i) => img.classList.toggle('active', i === index));
        modal.currentIndex = index;
    }

    function prevImage(modalId) {
        var modal = document.getElementById(modalId);
        showImage(modalId, (modal.currentIndex || 0) - 1);
    }

    function nextImage(modalId) {
        var modal = document.getElementById(modalId);
        showImage(modalId, (modal.currentIndex || 0) + 1);
    }

    // Event listener untuk menutup modal ketika klik di luar konten modal
    window.onclick = function(event) {
        if (event.target.classList.contains('modal')) {
            event.target.style.display = 'none';
        }
    }
  </script>
</body>
</html>
