<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rimuru Store - Topup Game & Layanan Digital</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary: #3498db;
            --secondary: #2980b9;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
            
            /* Light mode colors */
            --bg-color: #f5f7fa;
            --text-color: #333;
            --card-bg: white;
            --header-bg: linear-gradient(135deg, var(--primary), var(--secondary));
            --footer-bg: var(--dark);
            --section-bg: #f0f8ff;
        }
        
        .dark-mode {
            --bg-color: #1a1a1a;
            --text-color: #f0f0f0;
            --card-bg: #2d2d2d;
            --header-bg: linear-gradient(135deg, #1e3c72, #2a5298);
            --footer-bg: #121212;
            --section-bg: #252525;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            transition: background-color 0.3s, color 0.3s;
        }
        
        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background: var(--header-bg);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo img {
            height: 50px;
            margin-right: 15px;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        nav ul {
            display: flex;
            list-style: none;
            align-items: center;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
        
        .theme-toggle {
            background: none;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
            padding: 0.5rem;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .theme-toggle:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
        
        .hero {
            background: url('https://file.idnet.my.id/api/preview.php?file=2aheqo7m.jpg') no-repeat center center/cover;
            height: 60vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .btn:hover {
            background-color: #c0392b;
            transform: translateY(-2px);
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.15);
        }
        
        .btn-whatsapp {
            background-color: #25D366;
        }
        
        .btn-whatsapp:hover {
            background-color: #128C7E;
        }
        
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            color: var(--text-color);
            position: relative;
            display: inline-block;
            padding-bottom: 0.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--primary);
        }
        
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: var(--card-bg);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .product-header {
            background-color: var(--primary);
            color: white;
            padding: 1rem;
            text-align: center;
        }
        
        .product-header h3 {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }
        
        .product-body {
            padding: 1.5rem;
        }
        
        .price-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.5rem 0;
            border-bottom: 1px dashed rgba(0, 0, 0, 0.1);
        }
        
        .price-item:last-child {
            border-bottom: none;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            text-align: center;
        }
        
        .about-image img {
            max-width: 100%;
            border-radius: 8px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .contact-card {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: transform 0.3s ease;
        }
        
        .contact-card:hover {
            transform: translateY(-5px);
        }
        
        .contact-card i {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .testimonials {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial-card {
            background-color: var(--card-bg);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-header {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .testimonial-header img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: 1rem;
        }
        
        .testimonial-rating {
            color: #f1c40f;
            margin-top: 0.5rem;
        }
        
        footer {
            background-color: var(--footer-bg);
            color: white;
            padding: 3rem 0 1rem;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 2rem;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
            margin-bottom: 1.5rem;
        }
        
        .footer-section h3 {
            margin-bottom: 1rem;
            position: relative;
            padding-bottom: 0.5rem;
        }
        
        .footer-section h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--primary);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white;
            background-color: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }
        
        .copyright {
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Music player */
        .music-player {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: var(--card-bg);
            border-radius: 50%;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            z-index: 99;
        }
        
        .music-player i {
            font-size: 1.5rem;
            color: var(--primary);
        }
        
        /* Dark mode toggle */
        .theme-toggle-container {
            display: flex;
            align-items: center;
            margin-left: 1.5rem;
        }
        
        .theme-toggle {
            background: rgba(255, 255, 255, 0.1);
            border: none;
            color: white;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .theme-toggle:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
                flex-wrap: wrap;
            }
            
            nav ul li {
                margin: 0.5rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .footer-content {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }
            
            .footer-section h3::after {
                left: 50%;
                transform: translateX(-50%);
            }
        }
    </style>
</head>
<body>
    <audio id="bgMusic" loop>
        <source src="https://files.catbox.moe/xbsqo2.opus" type="audio/mpeg">
    </audio>
    
    <div class="music-player" id="musicToggle">
        <i class="fas fa-music"></i>
    </div>
    
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <img src="https://file.idnet.my.id/api/preview.php?file=ymggle9h.png" alt="Rimuru Store Logo">
                    <h1>Rimuru Store</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">Beranda</a></li>
                        <li><a href="#products">Produk</a></li>
                        <li><a href="#about">Tentang Kami</a></li>
                        <li><a href="#testimonials">Testimoni</a></li>
                        <li><a href="#contact">Kontak</a></li>
                        <li class="theme-toggle-container">
                            <button class="theme-toggle" id="themeToggle">
                                <i class="fas fa-moon"></i>
                            </button>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
    
    <section class="hero" id="home">
        <div class="hero-content">
            <h2>Topup Game & Layanan Digital Terpercaya</h2>
            <p>Proses cepat, harga terjangkau, dan pelayanan ramah 24/7</p>
            <a href="#products" class="btn">Lihat Produk</a>
        </div>
    </section>
    
    <section id="products">
        <div class="container">
            <div class="section-title">
                <h2>Produk Kami</h2>
            </div>
            
            <div class="products">
                <!-- Free Fire -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>Free Fire</h3>
                        <p>FF | Epep | FREE FIRE💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>12💎 = 2.500</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%2012💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>25💎 = 4.999</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%2025💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>50💎 = 7.300</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%2050💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>75💎 = 10.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%2075💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>90💎 = 12.999</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%2090💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>100💎 = 14.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20100💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>120💎 = 16.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20120💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>130💎 = 18.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20130💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>150💎 = 19.900</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20150💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>160💎 = 21.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20160💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>180💎 = 23.999</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20180💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>190💎 = 25.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20190💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>200💎 = 26.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20200💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>210💎 = 27.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20210💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>Membership Mingguan = 28.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20Membership%20Mingguan" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>250💎 = 32.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20FF%20250💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
                
                <!-- Mobile Legends -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>Mobile Legends</h3>
                        <p>mlbb | ꭑⱺᑲ𝗂ᥣ𝖾 ᥣ𝖾𝗀𝖾𐓣ᑯ𝗌💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>14💎 = 4.500</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2014💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>19💎 = 6.400</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2019💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>36💎 = 10.500</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2036💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>44💎 = 13.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2044💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>50💎 = 14.500</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2050💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>59💎 = 16.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2059💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>65💎 = 18.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2065💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>74💎 = 20.300</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2074💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>85💎 = 23.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%2085💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>112💎 = 31.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20112💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>172💎 = 36.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20172💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>185💎 = 50.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20185💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>257💎 = 55.500</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20257💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>284💎 = 75.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20284💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>296💎 = 78.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20296💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>344💎 = 92.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20344💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>370💎 = 97.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20370💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>429💎 = 111.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20429💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>514💎 = 135.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20514💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>568💎 = 143.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20568💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>600💎 = 154.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20600💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>716💎 = 184.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20716💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>792💎 = 206.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20792💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>878💎 = 222.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20878💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>963💎 = 242.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%20963💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>1050💎 = 265.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20DM%20ML%201050💎" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
                
                <!-- Roblox -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>Roblox</h3>
                        <p>Roblox | Roblox𝗌💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>100rbx = 18.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20Roblox%20100rbx" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>400RBX = 77.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20Roblox%20400RBX" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>Roblox Gift Card = 102.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20Roblox%20Gift%20Card%20102rb" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>Roblox Gift Card = 203.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20Roblox%20Gift%20Card%20203rb" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>Roblox Gift Card = 505.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20Roblox%20Gift%20Card%20505rb" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
                
                <!-- Call of Duty Mobile -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>Call of Duty Mobile</h3>
                        <p>COD | CODM | Call of Duty MOBILE 💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>26CP = 5.500</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%2026CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>62CP = 9.800</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%2062CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>127CP = 18.800</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%20127CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>320CP = 49.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%20320CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>528CP = 96.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%20528CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>1056CP = 185.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%201056CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>1584CP = 290.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20COD%201584CP" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
                
                <!-- PUBG -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>PUBG Mobile</h3>
                        <p>Pubg | UC💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>52UC = 16.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%2052UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>62UC = 18.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%2062UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>263UC = 74.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%20263UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>500UC = 112.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%20500UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>700UC = 164.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%20700UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>788UC = 193.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%20788UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>1000UC = 242.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%201000UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>1100UC = 250.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%201100UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>2425UC = 517.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%202425UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>2875UC = 625.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20beli%20PUBG%202875UC" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
                
                <!-- Layanan Lain -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>Sewa Bot WhatsApp</h3>
                        <p>Bot WhatsApp Premium</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>1 bulan = 5.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20sewa%20Bot%20WA%201%20bulan" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>2 bulan = 10.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20sewa%20Bot%20WA%202%20bulan" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>3 bulan = 15.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20sewa%20Bot%20WA%203%20bulan" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>4 bulan = 20.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20sewa%20Bot%20WA%204%20bulan" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>1 tahun = 25.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20sewa%20Bot%20WA%201%20tahun" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
                
                <!-- Suntik Sosmed -->
                <div class="product-card">
                    <div class="product-header">
                        <h3>Suntik Sosmed</h3>
                        <p>Tiktok & Instagram</p>
                    </div>
                    <div class="product-body">
                        <h4>Tiktok:</h4>
                        <div class="price-item">
                            <span>500 Like = 1.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20suntik%20Tiktok%20500%20Like" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>500 View = 900</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20suntik%20Tiktok%20500%20View" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>100 Follow = 3.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20suntik%20Tiktok%20100%20Follow" class="btn btn-whatsapp">Beli</a>
                        </div>
                        
                        <h4 style="margin-top: 1rem;">Instagram:</h4>
                        <div class="price-item">
                            <span>500 Like = 2.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20suntik%20IG%20500%20Like" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>500 View = 1.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20suntik%20IG%20500%20View" class="btn btn-whatsapp">Beli</a>
                        </div>
                        <div class="price-item">
                            <span>100 Follow = 3.000</span>
                            <a href="https://wa.me/6289506222871?text=Halo%20Rimuru%20Store,%20saya%20mau%20suntik%20IG%20100%20Follow" class="btn btn-whatsapp">Beli</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <section id="about" style="background-color: var(--section-bg);">
        <div class="container">
            <div class="section-title">
                <h2>Tentang Kami</h2>
            </div>
            
            <div class="about-content">
                <div class="about-text">
                    <p>Rimuru Store adalah penyedia layanan topup game dan layanan digital terpercaya yang telah beroperasi sejak 2020. Kami berkomitmen untuk memberikan pelayanan terbaik dengan harga kompetitif dan proses yang cepat.</p>
                    <p style="margin-top: 1rem;">Tim kami terdiri dari para gamer berpengalaman yang memahami kebutuhan pelanggan. Kami selalu berusaha memberikan pengalaman berbelanja yang menyenangkan dan memuaskan.</p>
                    <div style="margin-top: 2rem;">
                        <h3>Metode Pembayaran:</h3>
                        <ul style="margin-top: 0.5rem; margin-left: 1.5rem;">
                            <li>Dana: 083140427092</li>
                            <li>GOPAY: 083140427092</li>
                            <li>SPAY: 083140427092</li>
                            <li>OVO: 083140427092</li>
                            <li>SEABAK: 083140427092</li>
                            <li>QRIS: CHAT ADMIN</li>
                        </ul>
                        <p style="margin-top: 1rem; font-style: italic;">
                            Note: Nominal lain tanyakan admin, no rush, send id - pay - done
                        </p>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://file.idnet.my.id/api/preview.php?file=ymggle9h.png" alt="Tentang Rimuru Store">
                </div>
            </div>
        </div>
    </section>
    
    <section id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Testimoni Pelanggan</h2>
            </div>
            
            <div class="testimonials">
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Pelanggan 1">
                        <div>
                            <h4>Rizky Pratama</h4>
                            <p>Pelanggan Free Fire</p>
                        </div>
                    </div>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p>"Prosesnya cepat banget, ga sampe 5 menit diamond langsung masuk. Adminnya ramah dan helpful. Recommended banget!"</p>
                </div>
                
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Pelanggan 2">
                        <div>
                            <h4>Sarah Wijaya</h4>
                            <p>Pelanggan Mobile Legends</p>
                        </div>
                    </div>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p>"Pertama kali beli disini dan ga mengecewakan. Harganya murah dibanding tempat lain. Bakal langganan disini terus."</p>
                </div>
                
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Pelanggan 3">
                        <div>
                            <h4>Andi Setiawan</h4>
                            <p>Pelanggan Sewa Bot WA</p>
                        </div>
                    </div>
                    <div class="testimonial-rating">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                    <p>"Bot WA-nya bekerja dengan baik. Ada kendala sedikit tapi admin langsung bantu selesaikan. Good service!"</p>
                </div>
            </div>
        </div>
    </section>
    
    <section id="contact" style="background-color: var(--section-bg);">
        <div class="container">
            <div class="section-title">
                <h2>Kontak Kami</h2>
            </div>
            
            <div class="contact-info">
                <div class="contact-card">
                    <i class="fas fa-user"></i>
                    <h3>Nama Admin</h3>
                    <p>Irwan Ariel</p>
                </div>
                
                <div class="contact-card">
                    <i class="fas fa-phone-alt"></i>
                    <h3>WhatsApp</h3>
                    <p><a href="https://wa.me/6289506222871" style="color: var(--primary); text-decoration: none;">089506222871</a></p>
                </div>
                
                <div class="contact-card">
                    <i class="fas fa-envelope"></i>
                    <h3>Email</h3>
                    <p><a href="mailto:irwanaril798@gmail.com" style="color: var(--primary); text-decoration: none;">irwanaril798@gmail.com</a></p>
                </div>
                
                <div class="contact-card">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Alamat</h3>
                    <p>Riau, Indonesia</p>
                </div>
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Tentang Rimuru Store</h3>
                    <p>Penyedia layanan topup game dan layanan digital terpercaya dengan harga kompetitif dan pelayanan terbaik.</p>
                </div>
                
                <div class="footer-section">
                    <h3>Link Cepat</h3>
                    <ul style="list-style: none;">
                        <li><a href="#home" style="color: white; text-decoration: none;">Beranda</a></li>
                        <li><a href="#products" style="color: white; text-decoration: none;">Produk</a></li>
                        <li><a href="#about" style="color: white; text-decoration: none;">Tentang Kami</a></li>
                        <li><a href="#testimonials" style="color: white; text-decoration: none;">Testimoni</a></li>
                        <li><a href="#contact" style="color: white; text-decoration: none;">Kontak</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>Hubungi Kami</h3>
                    <p><i class="fas fa-phone-alt"></i> 089506222871</p>
                    <p><i class="fas fa-envelope"></i> irwanaril798@gmail.com</p>
                    <div class="social-links">
                        <a href="https://wa.me/6289506222871"><i class="fab fa-whatsapp"></i></a>
                        <a href="https://www.instagram.com/zainala_keyzi?igsh=MTk1Zm10OXBlZjdzZA=="><i class="fab fa-instagram"></i></a>
                        <a href="https://www.facebook.com/share/16iKtXrYsy/"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Rimuru Store. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Music toggle
        const musicToggle = document.getElementById('musicToggle');
        const bgMusic = document.getElementById('bgMusic');
        let isPlaying = false;
        
        musicToggle.addEventListener('click', function() {
            if (isPlaying) {
                bgMusic.pause();
                musicToggle.innerHTML = '<i class="fas fa-music"></i>';
            } else {
                bgMusic.play();
                musicToggle.innerHTML = '<i class="fas fa-pause"></i>';
            }
            isPlaying = !isPlaying;
        });
        
        // Dark mode toggle
        const themeToggle = document.getElementById('themeToggle');
        const body = document.body;
        
        // Check for saved user preference
        const currentTheme = localStorage.getItem('theme');
        if (currentTheme) {
            body.classList.add(currentTheme);
            updateThemeIcon(currentTheme);
        }
        
        themeToggle.addEventListener('click', function() {
            if (body.classList.contains('dark-mode')) {
                body.classList.remove('dark-mode');
                localStorage.setItem('theme', '');
                updateThemeIcon('');
            } else {
                body.classList.add('dark-mode');
                localStorage.setItem('theme', 'dark-mode');
                updateThemeIcon('dark-mode');
            }
        });
        
        function updateThemeIcon(theme) {
            if (theme === 'dark-mode') {
                themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
            } else {
                themeToggle.innerHTML = '<i class="fas fa-moon"></i>';
            }
        }
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
