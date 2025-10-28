<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Samuel Tegar - Portofolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Raleway:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
            --warning: #f39c12;
            --gradient: linear-gradient(135deg, var(--primary), var(--secondary));
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5 {
            font-family: 'Raleway', sans-serif;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1rem;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            display: inline-block;
            position: relative;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: var(--gradient);
            border-radius: 2px;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--gradient);
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            font-weight: 500;
            text-decoration: none;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: var(--shadow);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary);
            color: var(--secondary);
        }

        .btn-outline:hover {
            background: var(--secondary);
            color: white;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
        }

        header.scrolled {
            background: rgba(255, 255, 255, 0.98);
            padding: 10px 0;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--secondary);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .hamburger {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: var(--primary);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: var(--gradient);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800" opacity="0.1"><polygon fill="white" points="0,100 150,200 300,160 450,220 600,180 750,240 900,200 1050,260 1200,220 1200,800 0,800"/></svg>');
            background-size: cover;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 600px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            line-height: 1.1;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .hero-btns {
            display: flex;
            gap: 15px;
        }

        .hero-btns .btn {
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .hero-btns .btn:hover {
            background: white;
            color: var(--primary);
        }

        .scroll-down {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            color: white;
            font-size: 1.5rem;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0) translateX(-50%);
            }
            40% {
                transform: translateY(-10px) translateX(-50%);
            }
            60% {
                transform: translateY(-5px) translateX(-50%);
            }
        }

        /* About Section */
        .about {
            background: white;
        }

        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }

        .about-img {
            flex: 1;
            position: relative;
        }

        .about-img::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            width: 100%;
            height: 100%;
            border: 5px solid var(--secondary);
            border-radius: 10px;
            z-index: -1;
        }

        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .about-text {
            flex: 1;
        }

        .about-text h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .about-text p {
            margin-bottom: 1.5rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 2rem;
        }

        .skill {
            background: var(--light);
            padding: 8px 15px;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        /* Portfolio Section */
        .portfolio {
            background: var(--light);
        }

        .portfolio-filters {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 40px;
        }

        .filter-btn {
            padding: 8px 20px;
            background: white;
            border: none;
            border-radius: 30px;
            font-weight: 500;
            cursor: pointer;
            transition: var(--transition);
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--secondary);
            color: white;
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 30px;
        }

        .portfolio-item {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .portfolio-item:hover {
            transform: translateY(-10px);
        }

        .portfolio-img {
            height: 250px;
            overflow: hidden;
        }

        .portfolio-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .portfolio-item:hover .portfolio-img img {
            transform: scale(1.1);
        }

        .portfolio-info {
            padding: 20px;
        }

        .portfolio-info h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }

        .portfolio-info p {
            color: #666;
            margin-bottom: 15px;
        }

        .portfolio-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
        }

        .portfolio-tag {
            background: var(--light);
            padding: 5px 10px;
            border-radius: 3px;
            font-size: 0.8rem;
        }

        /* Games Section */
        .games {
            background: white;
        }

        .games-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .game-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .game-card:hover {
            transform: translateY(-5px);
        }

        .game-header {
            padding: 20px;
            background: var(--gradient);
            color: white;
        }

        .game-header h3 {
            margin-bottom: 0;
        }

        .game-body {
            padding: 20px;
        }

        /* Tic Tac Toe Game */
        .tic-tac-toe {
            text-align: center;
        }

        .game-info {
            margin-bottom: 15px;
            font-weight: 500;
        }

        .game-board {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 5px;
            margin: 0 auto 15px;
            max-width: 300px;
        }

        .cell {
            aspect-ratio: 1;
            background: var(--light);
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2rem;
            font-weight: bold;
            cursor: pointer;
            transition: var(--transition);
        }

        .cell:hover {
            background: #e0e0e0;
        }

        .cell.x {
            color: var(--accent);
        }

        .cell.o {
            color: var(--secondary);
        }

        /* Memory Game */
        .memory-game {
            text-align: center;
        }

        .memory-info {
            margin-bottom: 15px;
            font-weight: 500;
        }

        .memory-board {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 5px;
            margin: 0 auto 15px;
            max-width: 300px;
        }

        .memory-card {
            aspect-ratio: 1;
            background: var(--secondary);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            cursor: pointer;
            transition: var(--transition);
            transform-style: preserve-3d;
        }

        .memory-card.flipped {
            background: white;
            color: var(--secondary);
            transform: rotateY(180deg);
        }

        .memory-card.matched {
            background: var(--success);
            transform: rotateY(180deg);
        }

        /* Contact Section */
        .contact {
            background: var(--light);
        }

        .contact-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.2rem;
        }

        .contact-form {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Poppins', sans-serif;
            transition: var(--transition);
        }

        .form-control:focus {
            border-color: var(--secondary);
            outline: none;
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .footer-logo span {
            color: var(--secondary);
        }

        .footer-about p {
            margin-bottom: 20px;
            opacity: 0.8;
        }

        .footer-links h3, .footer-social h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
        }

        .footer-links h3::after, .footer-social h3::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 40px;
            height: 3px;
            background: var(--secondary);
        }

        .footer-links ul {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.8);
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: var(--secondary);
            padding-left: 5px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            text-decoration: none;
            transition: var(--transition);
        }

        .social-icon:hover {
            background: var(--secondary);
            transform: translateY(-3px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero-content h1 {
                font-size: 2.8rem;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: white;
                flex-direction: column;
                align-items: center;
                justify-content: flex-start;
                padding-top: 50px;
                transition: var(--transition);
                box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            }

            .nav-links.active {
                left: 0;
            }

            .nav-links li {
                margin: 15px 0;
            }

            .hamburger {
                display: block;
            }

            .hero-content h1 {
                font-size: 2.3rem;
            }

            .section-title h2 {
                font-size: 2rem;
            }
        }

        @media (max-width: 576px) {
            .hero-btns {
                flex-direction: column;
                width: 100%;
            }

            .hero-btns .btn {
                width: 100%;
                text-align: center;
            }

            .portfolio-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header id="header">
        <div class="container nav-container">
            <div class="logo">Samuel<span>Tegar</span></div>
            <div class="hamburger" id="hamburger">
                <i class="fas fa-bars"></i>
            </div>
            <ul class="nav-links" id="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">Tentang</a></li>
                <li><a href="#portfolio">Portofolio</a></li>
                <li><a href="#games">Games</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Samuel Tegar</h1>
                <p>Full Stack Developer & UI/UX Designer dengan pengalaman lebih dari 5 tahun dalam menciptakan solusi digital yang inovatif dan user-friendly.</p>
                <div class="hero-btns">
                    <a href="#portfolio" class="btn">Lihat Portofolio</a>
                    <a href="#contact" class="btn btn-outline">Hubungi Saya</a>
                </div>
            </div>
        </div>
        <a href="#about" class="scroll-down">
            <i class="fas fa-chevron-down"></i>
        </a>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>Tentang Saya</h2>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=774&q=80" alt="Samuel Tegar">
                </div>
                <div class="about-text">
                    <h3>Halo! Saya Samuel Tegar</h3>
                    <p>Saya adalah seorang Full Stack Developer dengan passion dalam menciptakan pengalaman digital yang menarik dan fungsional. Dengan latar belakang di bidang Computer Science, saya telah mengembangkan berbagai aplikasi web dan mobile untuk klien dari berbagai industri.</p>
                    <p>Saya memiliki keahlian dalam berbagai teknologi termasuk React, Node.js, Python, dan MongoDB. Saya selalu berusaha untuk tetap update dengan tren teknologi terbaru dan menerapkan best practices dalam setiap proyek yang saya kerjakan.</p>
                    <p>Selain coding, saya juga menikmati desain UI/UX dan percaya bahwa antarmuka yang baik adalah kunci keberhasilan produk digital.</p>
                    <div class="skills">
                        <span class="skill">JavaScript</span>
                        <span class="skill">React</span>
                        <span class="skill">Node.js</span>
                        <span class="skill">Python</span>
                        <span class="skill">MongoDB</span>
                        <span class="skill">UI/UX Design</span>
                        <span class="skill">Responsive Web</span>
                        <span class="skill">API Development</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>Portofolio</h2>
            </div>
            <div class="portfolio-filters">
                <button class="filter-btn active" data-filter="all">Semua</button>
                <button class="filter-btn" data-filter="web">Web Development</button>
                <button class="filter-btn" data-filter="mobile">Mobile Apps</button>
                <button class="filter-btn" data-filter="design">UI/UX Design</button>
            </div>
            <div class="portfolio-grid" id="portfolio-grid">
                <!-- Portfolio items will be dynamically added here -->
            </div>
        </div>
    </section>

    <!-- Games Section -->
    <section class="games" id="games">
        <div class="container">
            <div class="section-title">
                <h2>Games Interaktif</h2>
            </div>
            <div class="games-container">
                <!-- Tic Tac Toe Game -->
                <div class="game-card">
                    <div class="game-header">
                        <h3>Tic Tac Toe</h3>
                    </div>
                    <div class="game-body">
                        <div class="tic-tac-toe">
                            <div class="game-info" id="tic-tac-toe-info">Giliran: X</div>
                            <div class="game-board" id="tic-tac-toe-board">
                                <!-- Cells will be dynamically added -->
                            </div>
                            <button class="btn" id="tic-tac-toe-reset">Reset Game</button>
                        </div>
                    </div>
                </div>

                <!-- Memory Game -->
                <div class="game-card">
                    <div class="game-header">
                        <h3>Memory Game</h3>
                    </div>
                    <div class="game-body">
                        <div class="memory-game">
                            <div class="memory-info" id="memory-info">Temukan pasangan yang sama!</div>
                            <div class="memory-board" id="memory-board">
                                <!-- Cards will be dynamically added -->
                            </div>
                            <button class="btn" id="memory-reset">Reset Game</button>
                        </div>
                    </div>
                </div>

                <!-- Typing Game -->
                <div class="game-card">
                    <div class="game-header">
                        <h3>Typing Speed Test</h3>
                    </div>
                    <div class="game-body">
                        <div class="typing-game">
                            <div class="typing-info" id="typing-info">Ketik teks di bawah ini secepat mungkin!</div>
                            <div class="typing-text" id="typing-text">JavaScript adalah bahasa pemrograman yang powerful untuk pengembangan web.</div>
                            <textarea class="form-control" id="typing-input" placeholder="Ketik teks di sini..."></textarea>
                            <div class="typing-stats">
                                <div>Waktu: <span id="typing-time">0</span>s</div>
                                <div>Kecepatan: <span id="typing-speed">0</span> WPM</div>
                                <div>Akurasi: <span id="typing-accuracy">0</span>%</div>
                            </div>
                            <button class="btn" id="typing-reset">Mulai Ulang</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Kontak Saya</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div>
                            <h3>Lokasi</h3>
                            <p>Jakarta, Indonesia</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div>
                            <h3>Email</h3>
                            <p>samuel.tegar@example.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div>
                            <h3>Telepon</h3>
                            <p>+62 812 3456 7890</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-globe"></i>
                        </div>
                        <div>
                            <h3>Website</h3>
                            <p>www.samueltegar.com</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Nama Lengkap</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subjek</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Pesan</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="btn">Kirim Pesan</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-about">
                    <div class="footer-logo">Samuel<span>Tegar</span></div>
                    <p>Full Stack Developer dengan passion untuk menciptakan solusi digital yang inovatif dan user-friendly.</p>
                    <div class="social-icons">
                        <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h3>Link Cepat</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">Tentang</a></li>
                        <li><a href="#portfolio">Portofolio</a></li>
                        <li><a href="#games">Games</a></li>
                        <li><a href="#contact">Kontak</a></li>
                    </ul>
                </div>
                <div class="footer-social">
                    <h3>Media Sosial</h3>
                    <ul>
                        <li><a href="#"><i class="fab fa-facebook-f"></i> Facebook</a></li>
                        <li><a href="#"><i class="fab fa-twitter"></i> Twitter</a></li>
                        <li><a href="#"><i class="fab fa-instagram"></i> Instagram</a></li>
                        <li><a href="#"><i class="fab fa-linkedin-in"></i> LinkedIn</a></li>
                        <li><a href="#"><i class="fab fa-github"></i> GitHub</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 Samuel Tegar. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Portfolio Data
        const portfolioItems = [
            {
                id: 1,
                title: "E-commerce Platform",
                category: "web",
                image: "https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                description: "Platform e-commerce lengkap dengan sistem pembayaran terintegrasi dan manajemen inventaris.",
                tags: ["React", "Node.js", "MongoDB", "Stripe API"]
            },
            {
                id: 2,
                title: "Task Management App",
                category: "mobile",
                image: "https://images.unsplash.com/photo-1611224923853-80b023f02d71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1039&q=80",
                description: "Aplikasi mobile untuk manajemen tugas dengan fitur kolaborasi tim dan notifikasi.",
                tags: ["React Native", "Firebase", "Redux"]
            },
            {
                id: 3,
                title: "Travel Booking UI",
                category: "design",
                image: "https://images.unsplash.com/photo-1488646953014-85cb44e25828?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1035&q=80",
                description: "Desain UI/UX untuk aplikasi pemesanan travel dengan fokus pada pengalaman pengguna.",
                tags: ["Figma", "UI Design", "UX Research"]
            },
            {
                id: 4,
                title: "Social Media Dashboard",
                category: "web",
                image: "https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                description: "Dashboard analytics untuk media sosial dengan visualisasi data yang interaktif.",
                tags: ["Vue.js", "D3.js", "Express.js", "MySQL"]
            },
            {
                id: 5,
                title: "Fitness Tracking App",
                category: "mobile",
                image: "https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                description: "Aplikasi pelacak kebugaran dengan integrasi wearable devices dan analisis data kesehatan.",
                tags: ["Flutter", "Firebase", "HealthKit", "Google Fit"]
            },
            {
                id: 6,
                title: "Banking App Redesign",
                category: "design",
                image: "https://images.unsplash.com/photo-1563013544-824ae1b704d3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80",
                description: "Redesign UI/UX untuk aplikasi mobile banking dengan fokus pada keamanan dan kemudahan penggunaan.",
                tags: ["Sketch", "Prototyping", "User Testing"]
            }
        ];

        // DOM Elements
        const portfolioGrid = document.getElementById('portfolio-grid');
        const filterBtns = document.querySelectorAll('.filter-btn');
        const navLinks = document.getElementById('nav-links');
        const hamburger = document.getElementById('hamburger');
        const header = document.getElementById('header');
        const contactForm = document.getElementById('contactForm');

        // Initialize Portfolio
        function initPortfolio() {
            displayPortfolioItems('all');
            
            filterBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    // Remove active class from all buttons
                    filterBtns.forEach(b => b.classList.remove('active'));
                    // Add active class to clicked button
                    btn.classList.add('active');
                    // Filter portfolio items
                    displayPortfolioItems(btn.dataset.filter);
                });
            });
        }

        // Display Portfolio Items
        function displayPortfolioItems(category) {
            portfolioGrid.innerHTML = '';
            
            const filteredItems = category === 'all' 
                ? portfolioItems 
                : portfolioItems.filter(item => item.category === category);
            
            filteredItems.forEach(item => {
                const portfolioItem = document.createElement('div');
                portfolioItem.className = 'portfolio-item';
                portfolioItem.innerHTML = `
                    <div class="portfolio-img">
                        <img src="${item.image}" alt="${item.title}">
                    </div>
                    <div class="portfolio-info">
                        <h3>${item.title}</h3>
                        <p>${item.description}</p>
                        <div class="portfolio-tags">
                            ${item.tags.map(tag => `<span class="portfolio-tag">${tag}</span>`).join('')}
                        </div>
                    </div>
                `;
                portfolioGrid.appendChild(portfolioItem);
            });
        }

        // Mobile Navigation Toggle
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            hamburger.innerHTML = navLinks.classList.contains('active') 
                ? '<i class="fas fa-times"></i>' 
                : '<i class="fas fa-bars"></i>';
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                hamburger.innerHTML = '<i class="fas fa-bars"></i>';
            });
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Contact Form Submission
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Terima kasih! Pesan Anda telah dikirim. Saya akan menghubungi Anda segera.');
            contactForm.reset();
        });

        // Tic Tac Toe Game
        const ticTacToeBoard = document.getElementById('tic-tac-toe-board');
        const ticTacToeInfo = document.getElementById('tic-tac-toe-info');
        const ticTacToeReset = document.getElementById('tic-tac-toe-reset');

        let currentPlayer = 'X';
        let gameBoard = ['', '', '', '', '', '', '', '', ''];
        let gameActive = true;

        function initTicTacToe() {
            // Create board cells
            for (let i = 0; i < 9; i++) {
                const cell = document.createElement('div');
                cell.className = 'cell';
                cell.setAttribute('data-index', i);
                cell.addEventListener('click', handleCellClick);
                ticTacToeBoard.appendChild(cell);
            }
            
            // Reset game
            ticTacToeReset.addEventListener('click', resetTicTacToe);
        }

        function handleCellClick(e) {
            const index = e.target.getAttribute('data-index');
            
            if (gameBoard[index] !== '' || !gameActive) {
                return;
            }
            
            gameBoard[index] = currentPlayer;
            e.target.textContent = currentPlayer;
            e.target.classList.add(currentPlayer.toLowerCase());
            
            if (checkWinner()) {
                ticTacToeInfo.textContent = `Pemenang: ${currentPlayer}!`;
                gameActive = false;
                return;
            }
            
            if (checkDraw()) {
                ticTacToeInfo.textContent = 'Permainan Seri!';
                gameActive = false;
                return;
            }
            
            currentPlayer = currentPlayer === 'X' ? 'O' : 'X';
            ticTacToeInfo.textContent = `Giliran: ${currentPlayer}`;
        }

        function checkWinner() {
            const winPatterns = [
                [0, 1, 2], [3, 4, 5], [6, 7, 8], // Rows
                [0, 3, 6], [1, 4, 7], [2, 5, 8], // Columns
                [0, 4, 8], [2, 4, 6]             // Diagonals
            ];
            
            return winPatterns.some(pattern => {
                const [a, b, c] = pattern;
                return gameBoard[a] && gameBoard[a] === gameBoard[b] && gameBoard[a] === gameBoard[c];
            });
        }

        function checkDraw() {
            return gameBoard.every(cell => cell !== '');
        }

        function resetTicTacToe() {
            currentPlayer = 'X';
            gameBoard = ['', '', '', '', '', '', '', '', ''];
            gameActive = true;
            ticTacToeInfo.textContent = `Giliran: ${currentPlayer}`;
            
            document.querySelectorAll('.tic-tac-toe .cell').forEach(cell => {
                cell.textContent = '';
                cell.classList.remove('x', 'o');
            });
        }

        // Memory Game
        const memoryBoard = document.getElementById('memory-board');
        const memoryInfo = document.getElementById('memory-info');
        const memoryReset = document.getElementById('memory-reset');

        let memoryCards = [];
        let flippedCards = [];
        let matchedPairs = 0;
        let canFlip = true;

        const symbols = ['🍎', '🍌', '🍒', '🍇', '🍊', '🍓', '🥝', '🍉'];

        function initMemoryGame() {
            // Create pairs of symbols
            const cardValues = [...symbols, ...symbols];
            
            // Shuffle the cards
            shuffleArray(cardValues);
            
            // Create card elements
            cardValues.forEach((value, index) => {
                const card = document.createElement('div');
                card.className = 'memory-card';
                card.setAttribute('data-index', index);
                card.setAttribute('data-value', value);
                card.textContent = '?';
                card.addEventListener('click', flipCard);
                memoryBoard.appendChild(card);
                memoryCards.push(card);
            });
            
            // Reset game
            memoryReset.addEventListener('click', resetMemoryGame);
        }

        function shuffleArray(array) {
            for (let i = array.length - 1; i > 0; i--) {
                const j = Math.floor(Math.random() * (i + 1));
                [array[i], array[j]] = [array[j], array[i]];
            }
        }

        function flipCard(e) {
            if (!canFlip) return;
            
            const card = e.target;
            
            // Don't flip if card is already flipped or matched
            if (card.classList.contains('flipped') || card.classList.contains('matched')) {
                return;
            }
            
            // Flip the card
            card.textContent = card.getAttribute('data-value');
            card.classList.add('flipped');
            flippedCards.push(card);
            
            // Check for match when two cards are flipped
            if (flippedCards.length === 2) {
                canFlip = false;
                checkForMatch();
            }
        }

        function checkForMatch() {
            const [card1, card2] = flippedCards;
            const isMatch = card1.getAttribute('data-value') === card2.getAttribute('data-value');
            
            if (isMatch) {
                card1.classList.add('matched');
                card2.classList.add('matched');
                matchedPairs++;
                
                if (matchedPairs === symbols.length) {
                    memoryInfo.textContent = 'Selamat! Anda menang!';
                }
                
                flippedCards = [];
                canFlip = true;
            } else {
                setTimeout(() => {
                    card1.textContent = '?';
                    card2.textContent = '?';
                    card1.classList.remove('flipped');
                    card2.classList.remove('flipped');
                    flippedCards = [];
                    canFlip = true;
                }, 1000);
            }
        }

        function resetMemoryGame() {
            // Reset game state
            flippedCards = [];
            matchedPairs = 0;
            canFlip = true;
            memoryInfo.textContent = 'Temukan pasangan yang sama!';
            
            // Reset cards
            memoryCards.forEach(card => {
                card.textContent = '?';
                card.classList.remove('flipped', 'matched');
            });
            
            // Reshuffle cards
            setTimeout(() => {
                const cardValues = [...symbols, ...symbols];
                shuffleArray(cardValues);
                
                memoryCards.forEach((card, index) => {
                    card.setAttribute('data-value', cardValues[index]);
                });
            }, 500);
        }

        // Typing Game
        const typingText = document.getElementById('typing-text');
        const typingInput = document.getElementById('typing-input');
        const typingTime = document.getElementById('typing-time');
        const typingSpeed = document.getElementById('typing-speed');
        const typingAccuracy = document.getElementById('typing-accuracy');
        const typingReset = document.getElementById('typing-reset');

        let startTime;
        let timerInterval;
        let isTyping = false;

        const sampleTexts = [
            "JavaScript adalah bahasa pemrograman yang powerful untuk pengembangan web.",
            "React adalah library JavaScript yang populer untuk membangun antarmuka pengguna.",
            "Node.js memungkinkan JavaScript dijalankan di sisi server untuk aplikasi web.",
            "HTML dan CSS adalah fondasi dari setiap halaman web modern.",
            "Python dikenal dengan sintaks yang mudah dipahami dan banyak digunakan dalam data science."
        ];

        function initTypingGame() {
            // Set random text
            const randomIndex = Math.floor(Math.random() * sampleTexts.length);
            typingText.textContent = sampleTexts[randomIndex];
            
            // Start timer when user starts typing
            typingInput.addEventListener('input', () => {
                if (!isTyping) {
                    startTimer();
                    isTyping = true;
                }
                
                checkTypingProgress();
            });
            
            // Reset game
            typingReset.addEventListener('click', resetTypingGame);
        }

        function startTimer() {
            startTime = new Date();
            timerInterval = setInterval(updateTimer, 1000);
        }

        function updateTimer() {
            const currentTime = new Date();
            const elapsedTime = Math.floor((currentTime - startTime) / 1000);
            typingTime.textContent = elapsedTime;
        }

        function checkTypingProgress() {
            const typedText = typingInput.value;
            const originalText = typingText.textContent;
            
            // Calculate accuracy
            let correctChars = 0;
            for (let i = 0; i < typedText.length; i++) {
                if (typedText[i] === originalText[i]) {
                    correctChars++;
                }
            }
            
            const accuracy = typedText.length > 0 ? Math.floor((correctChars / typedText.length) * 100) : 0;
            typingAccuracy.textContent = accuracy;
            
            // Calculate speed (words per minute)
            const words = typedText.split(' ').length;
            const elapsedTimeInMinutes = (new Date() - startTime) / 60000;
            const wpm = elapsedTimeInMinutes > 0 ? Math.floor(words / elapsedTimeInMinutes) : 0;
            typingSpeed.textContent = wpm;
            
            // Check if text is completed
            if (typedText === originalText) {
                clearInterval(timerInterval);
                typingInput.disabled = true;
                typingInfo.textContent = 'Selesai! Tekan "Mulai Ulang" untuk mencoba lagi.';
            }
        }

        function resetTypingGame() {
            clearInterval(timerInterval);
            
            // Reset UI
            typingInput.value = '';
            typingInput.disabled = false;
            typingTime.textContent = '0';
            typingSpeed.textContent = '0';
            typingAccuracy.textContent = '0';
            isTyping = false;
            
            // Set new random text
            const randomIndex = Math.floor(Math.random() * sampleTexts.length);
            typingText.textContent = sampleTexts[randomIndex];
            typingInfo.textContent = 'Ketik teks di bawah ini secepat mungkin!';
        }

        // Initialize everything when DOM is loaded
        document.addEventListener('DOMContentLoaded', () => {
            initPortfolio();
            initTicTacToe();
            initMemoryGame();
            initTypingGame();
        });
    </script>
</body>
</html>
