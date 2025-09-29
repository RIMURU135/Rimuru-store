<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rimuru Store - Topup Game & Layanan Digital Terpercaya</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #3498db;
            --secondary: #2c3e50;
            --accent: #e74c3c;
            --dark: #2c3e50;
            
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
        
        /* Hero Section dengan Video Background */
        .hero {
            position: relative;
            height: 60vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            overflow: hidden;
        }
        
        .video-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            z-index: 0;
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
        
        /* Filter dan Pencarian */
        .product-filters {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            gap: 1rem;
        }
        
        .search-box {
            flex: 1;
            min-width: 250px;
            position: relative;
        }
        
        .search-box input {
            width: 100%;
            padding: 0.8rem 1rem 0.8rem 2.5rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            background-color: var(--card-bg);
            color: var(--text-color);
        }
        
        .search-box i {
            position: absolute;
            left: 0.8rem;
            top: 50%;
            transform: translateY(-50%);
            color: #777;
        }
        
        .category-filters {
            display: flex;
            gap: 0.5rem;
            flex-wrap: wrap;
        }
        
        .category-btn {
            padding: 0.5rem 1rem;
            background-color: var(--card-bg);
            border: 1px solid #ddd;
            border-radius: 4px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .category-btn.active {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
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
            max-height: 400px;
            overflow-y: auto;
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
        
        .add-to-cart {
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 4px;
            padding: 0.3rem 0.7rem;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        .add-to-cart:hover {
            background-color: #2980b9;
        }
        
        .cart-container {
            position: fixed;
            bottom: 20px;
            left: 20px;
            z-index: 1000;
        }
        
        .cart-btn {
            background-color: var(--accent);
            color: white;
            border: none;
            border-radius: 50%;
            width: 60px;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
        }
        
        .cart-btn:hover {
            transform: scale(1.1);
        }
        
        .cart-badge {
            position: absolute;
            top: -5px;
            right: -5px;
            background-color: #e74c3c;
            color: white;
            border-radius: 50%;
            width: 25px;
            height: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .cart-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1001;
            align-items: center;
            justify-content: center;
        }
        
        .cart-content {
            background-color: var(--card-bg);
            border-radius: 8px;
            width: 90%;
            max-width: 500px;
            max-height: 80vh;
            overflow-y: auto;
            padding: 2rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #eee;
        }
        
        .cart-items {
            margin-bottom: 1.5rem;
        }
        
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.8rem 0;
            border-bottom: 1px solid #eee;
        }
        
        .cart-item-info {
            flex: 1;
        }
        
        .cart-item-actions {
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .cart-item-actions button {
            background: none;
            border: none;
            cursor: pointer;
            color: var(--primary);
            font-size: 1.2rem;
        }
        
        .cart-total {
            display: flex;
            justify-content: space-between;
            font-weight: bold;
            font-size: 1.2rem;
            padding-top: 1rem;
            border-top: 2px solid #eee;
        }
        
        .cart-actions {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }
        
        .cart-actions button {
            flex: 1;
            padding: 0.8rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
        }
        
        .btn-clear {
            background-color: #e0e0e0;
            color: #333;
        }
        
        .btn-checkout {
            background-color: var(--primary);
            color: white;
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
        
        /* Video Controls */
        .video-controls {
            position: absolute;
            bottom: 20px;
            left: 20px;
            z-index: 2;
            display: flex;
            gap: 10px;
        }
        
        .video-controls button {
            background: rgba(255, 255, 255, 0.2);
            border: none;
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .video-controls button:hover {
            background: rgba(255, 255, 255, 0.3);
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
        
        /* Loading indicator */
        .loading {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 9999;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            color: white;
        }
        
        .loading-spinner {
            width: 50px;
            height: 50px;
            border: 5px solid rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            border-top-color: white;
            animation: spin 1s linear infinite;
            margin-bottom: 1rem;
        }
        
        @keyframes spin {
            to {
                transform: rotate(360deg);
            }
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
            
            .video-controls {
                bottom: 10px;
                left: 10px;
            }
            
            .product-filters {
                flex-direction: column;
                align-items: stretch;
            }
            
            .cart-container {
                bottom: 80px;
            }
        }
    </style>
</head>
<body>
    <!-- Loading Indicator -->
    <div class="loading" id="loading">
        <div class="loading-spinner"></div>
        <p>Memuat...</p>
    </div>

    <!-- Audio Background -->
    <audio id="bgMusic" loop>
        <source src="https://assets.mixkit.co/music/preview/mixkit-game-show-suspense-waiting-667.mp3" type="audio/mp3">
        Browser Anda tidak mendukung audio HTML5.
    </audio>

    <div class="music-player" id="musicToggle">
        <i class="fas fa-music"></i>
    </div>

    <!-- Cart Button -->
    <div class="cart-container">
        <button class="cart-btn" id="cartBtn">
            <i class="fas fa-shopping-cart"></i>
            <span class="cart-badge" id="cartBadge">0</span>
        </button>
    </div>

    <!-- Cart Modal -->
    <div class="cart-modal" id="cartModal">
        <div class="cart-content">
            <div class="cart-header">
                <h2>Keranjang Belanja</h2>
                <button id="closeCart">&times;</button>
            </div>
            <div class="cart-items" id="cartItems">
                <!-- Cart items will be added here dynamically -->
            </div>
            <div class="cart-total">
                <span>Total:</span>
                <span id="cartTotal">Rp 0</span>
            </div>
            <div class="cart-actions">
                <button class="btn-clear" id="clearCart">Kosongkan</button>
                <button class="btn-checkout" id="checkoutBtn">Checkout via WhatsApp</button>
            </div>
        </div>
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
        <!-- Video Background -->
        <video class="video-background" id="backgroundVideo" autoplay muted loop>
            <source src="https://files.catbox.moe/027sir.mp4" type="video/mp4">
            Browser Anda tidak mendukung video HTML5.
        </video>
        
        <!-- Video Controls -->
        <div class="video-controls">
            <button id="playPauseVideo">
                <i class="fas fa-pause"></i>
            </button>
            <button id="muteUnmuteVideo">
                <i class="fas fa-volume-up"></i>
            </button>
        </div>
        
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
            
            <!-- Filter dan Pencarian -->
            <div class="product-filters">
                <div class="search-box">
                    <i class="fas fa-search"></i>
                    <input type="text" id="searchInput" placeholder="Cari produk...">
                </div>
                <div class="category-filters">
                    <button class="category-btn active" data-category="all">Semua</button>
                    <button class="category-btn" data-category="freefire">Free Fire</button>
                    <button class="category-btn" data-category="mobilelegends">Mobile Legends</button>
                    <button class="category-btn" data-category="roblox">Roblox</button>
                    <button class="category-btn" data-category="cod">Call of Duty</button>
                    <button class="category-btn" data-category="pubg">PUBG</button>
                    <button class="category-btn" data-category="lainnya">Lainnya</button>
                </div>
            </div>
            
            <div class="products" id="productsContainer">
                <!-- Free Fire -->
                <div class="product-card" data-category="freefire">
                    <div class="product-header">
                        <h3>Free Fire</h3>
                        <p>FF | Epep | FREE FIRE💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>12💎 = 2.500</span>
                            <button class="add-to-cart" data-name="Free Fire 12💎" data-price="2500">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>25💎 = 4.999</span>
                            <button class="add-to-cart" data-name="Free Fire 25💎" data-price="4999">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>50💎 = 7.300</span>
                            <button class="add-to-cart" data-name="Free Fire 50💎" data-price="7300">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>75💎 = 10.000</span>
                            <button class="add-to-cart" data-name="Free Fire 75💎" data-price="10000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>90💎 = 12.999</span>
                            <button class="add-to-cart" data-name="Free Fire 90💎" data-price="12999">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>100💎 = 14.000</span>
                            <button class="add-to-cart" data-name="Free Fire 100💎" data-price="14000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>120💎 = 16.000</span>
                            <button class="add-to-cart" data-name="Free Fire 120💎" data-price="16000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>130💎 = 18.000</span>
                            <button class="add-to-cart" data-name="Free Fire 130💎" data-price="18000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>150💎 = 19.900</span>
                            <button class="add-to-cart" data-name="Free Fire 150💎" data-price="19900">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>160💎 = 21.000</span>
                            <button class="add-to-cart" data-name="Free Fire 160💎" data-price="21000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>180💎 = 23.999</span>
                            <button class="add-to-cart" data-name="Free Fire 180💎" data-price="23999">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>190💎 = 25.000</span>
                            <button class="add-to-cart" data-name="Free Fire 190💎" data-price="25000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>200💎 = 26.000</span>
                            <button class="add-to-cart" data-name="Free Fire 200💎" data-price="26000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>210💎 = 27.000</span>
                            <button class="add-to-cart" data-name="Free Fire 210💎" data-price="27000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>Membership Mingguan = 28.000</span>
                            <button class="add-to-cart" data-name="Free Fire Membership Mingguan" data-price="28000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>250💎 = 32.000</span>
                            <button class="add-to-cart" data-name="Free Fire 250💎" data-price="32000">+ Keranjang</button>
                        </div>
                    </div>
                </div>

                <!-- Mobile Legends -->
                <div class="product-card" data-category="mobilelegends">
                    <div class="product-header">
                        <h3>Mobile Legends</h3>
                        <p>mlbb | ꭑⱺᑲ𝗂ᥣ𝖾 ᥣ𝖾𝗀𝖾𐓣ᑯ𝗌💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>14💎 = 4.500</span>
                            <button class="add-to-cart" data-name="Mobile Legends 14💎" data-price="4500">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>19💎 = 6.400</span>
                            <button class="add-to-cart" data-name="Mobile Legends 19💎" data-price="6400">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>36💎 = 10.500</span>
                            <button class="add-to-cart" data-name="Mobile Legends 36💎" data-price="10500">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>44💎 = 13.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 44💎" data-price="13000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>50💎 = 14.500</span>
                            <button class="add-to-cart" data-name="Mobile Legends 50💎" data-price="14500">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>59💎 = 16.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 59💎" data-price="16000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>65💎 = 18.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 65💎" data-price="18000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>74💎 = 20.300</span>
                            <button class="add-to-cart" data-name="Mobile Legends 74💎" data-price="20300">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>85💎 = 23.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 85💎" data-price="23000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>112💎 = 31.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 112💎" data-price="31000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>172💎 = 36.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 172💎" data-price="36000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>185💎 = 50.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 185💎" data-price="50000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>257💎 = 55.500</span>
                            <button class="add-to-cart" data-name="Mobile Legends 257💎" data-price="55500">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>284💎 = 75.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 284💎" data-price="75000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>296💎 = 78.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 296💎" data-price="78000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>344💎 = 92.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 344💎" data-price="92000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>370💎 = 97.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 370💎" data-price="97000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>429💎 = 111.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 429💎" data-price="111000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>514💎 = 135.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 514💎" data-price="135000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>568💎 = 143.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 568💎" data-price="143000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>600💎 = 154.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 600💎" data-price="154000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>716💎 = 184.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 716💎" data-price="184000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>792💎 = 206.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 792💎" data-price="206000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>878💎 = 222.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 878💎" data-price="222000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>963💎 = 242.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 963💎" data-price="242000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>1050💎 = 265.000</span>
                            <button class="add-to-cart" data-name="Mobile Legends 1050💎" data-price="265000">+ Keranjang</button>
                        </div>
                    </div>
                </div>

                <!-- Roblox -->
                <div class="product-card" data-category="roblox">
                    <div class="product-header">
                        <h3>Roblox</h3>
                        <p>Roblox | Roblox𝗌💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>100rbx = 18.000</span>
                            <button class="add-to-cart" data-name="Roblox 100rbx" data-price="18000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>400RBX = 77.000</span>
                            <button class="add-to-cart" data-name="Roblox 400RBX" data-price="77000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>Roblox Gift Card = 102.000</span>
                            <button class="add-to-cart" data-name="Roblox Gift Card 102rb" data-price="102000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>Roblox Gift Card = 203.000</span>
                            <button class="add-to-cart" data-name="Roblox Gift Card 203rb" data-price="203000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>Roblox Gift Card = 505.000</span>
                            <button class="add-to-cart" data-name="Roblox Gift Card 505rb" data-price="505000">+ Keranjang</button>
                        </div>
                    </div>
                </div>

                <!-- Call of Duty Mobile -->
                <div class="product-card" data-category="cod">
                    <div class="product-header">
                        <h3>Call of Duty Mobile</h3>
                        <p>COD | CODM | Call of Duty MOBILE 💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>26CP = 5.500</span>
                            <button class="add-to-cart" data-name="COD 26CP" data-price="5500">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>62CP = 9.800</span>
                            <button class="add-to-cart" data-name="COD 62CP" data-price="9800">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>127CP = 18.800</span>
                            <button class="add-to-cart" data-name="COD 127CP" data-price="18800">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>320CP = 49.000</span>
                            <button class="add-to-cart" data-name="COD 320CP" data-price="49000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>528CP = 96.000</span>
                            <button class="add-to-cart" data-name="COD 528CP" data-price="96000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>1056CP = 185.000</span>
                            <button class="add-to-cart" data-name="COD 1056CP" data-price="185000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>1584CP = 290.000</span>
                            <button class="add-to-cart" data-name="COD 1584CP" data-price="290000">+ Keranjang</button>
                        </div>
                    </div>
                </div>

                <!-- PUBG -->
                <div class="product-card" data-category="pubg">
                    <div class="product-header">
                        <h3>PUBG Mobile</h3>
                        <p>Pubg | UC💸💸</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>52UC = 16.000</span>
                            <button class="add-to-cart" data-name="PUBG 52UC" data-price="16000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>62UC = 18.000</span>
                            <button class="add-to-cart" data-name="PUBG 62UC" data-price="18000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>263UC = 74.000</span>
                            <button class="add-to-cart" data-name="PUBG 263UC" data-price="74000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>500UC = 112.000</span>
                            <button class="add-to-cart" data-name="PUBG 500UC" data-price="112000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>700UC = 164.000</span>
                            <button class="add-to-cart" data-name="PUBG 700UC" data-price="164000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>788UC = 193.000</span>
                            <button class="add-to-cart" data-name="PUBG 788UC" data-price="193000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>1000UC = 242.000</span>
                            <button class="add-to-cart" data-name="PUBG 1000UC" data-price="242000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>1100UC = 250.000</span>
                            <button class="add-to-cart" data-name="PUBG 1100UC" data-price="250000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>2425UC = 517.000</span>
                            <button class="add-to-cart" data-name="PUBG 2425UC" data-price="517000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>2875UC = 625.000</span>
                            <button class="add-to-cart" data-name="PUBG 2875UC" data-price="625000">+ Keranjang</button>
                        </div>
                    </div>
                </div>

                <!-- Layanan Lain -->
                <div class="product-card" data-category="lainnya">
                    <div class="product-header">
                        <h3>Sewa Bot WhatsApp</h3>
                        <p>Bot WhatsApp Premium</p>
                    </div>
                    <div class="product-body">
                        <div class="price-item">
                            <span>1 bulan = 5.000</span>
                            <button class="add-to-cart" data-name="Sewa Bot WA 1 bulan" data-price="5000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>2 bulan = 10.000</span>
                            <button class="add-to-cart" data-name="Sewa Bot WA 2 bulan" data-price="10000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>3 bulan = 15.000</span>
                            <button class="add-to-cart" data-name="Sewa Bot WA 3 bulan" data-price="15000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>4 bulan = 20.000</span>
                            <button class="add-to-cart" data-name="Sewa Bot WA 4 bulan" data-price="20000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>1 tahun = 25.000</span>
                            <button class="add-to-cart" data-name="Sewa Bot WA 1 tahun" data-price="25000">+ Keranjang</button>
                        </div>
                    </div>
                </div>

                <!-- Suntik Sosmed -->
                <div class="product-card" data-category="lainnya">
                    <div class="product-header">
                        <h3>Suntik Sosmed</h3>
                        <p>Tiktok & Instagram</p>
                    </div>
                    <div class="product-body">
                        <h4>Tiktok:</h4>
                        <div class="price-item">
                            <span>500 Like = 1.000</span>
                            <button class="add-to-cart" data-name="Suntik Tiktok 500 Like" data-price="1000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>500 View = 900</span>
                            <button class="add-to-cart" data-name="Suntik Tiktok 500 View" data-price="900">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>100 Follow = 3.000</span>
                            <button class="add-to-cart" data-name="Suntik Tiktok 100 Follow" data-price="3000">+ Keranjang</button>
                        </div>
                        <h4 style="margin-top: 1rem;">Instagram:</h4>
                        <div class="price-item">
                            <span>500 Like = 2.000</span>
                            <button class="add-to-cart" data-name="Suntik IG 500 Like" data-price="2000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>500 View = 1.000</span>
                            <button class="add-to-cart" data-name="Suntik IG 500 View" data-price="1000">+ Keranjang</button>
                        </div>
                        <div class="price-item">
                            <span>100 Follow = 3.000</span>
                            <button class="add-to-cart" data-name="Suntik IG 100 Follow" data-price="3000">+ Keranjang</button>
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
                        <p style="margin-top: 1rem; font-style: italic;"> Note: Nominal lain tanyakan admin, no rush, send id - pay - done </p>
                    </div>
                </div>
                <div class="about-image">
                    <img src="https://file.idnet.my.id/api/preview.php?file=ikhk9tu8.jpg" alt="Tentang Rimuru Store">
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
        // Cart functionality
        let cart = [];
        const cartBtn = document.getElementById('cartBtn');
        const cartModal = document.getElementById('cartModal');
        const closeCart = document.getElementById('closeCart');
        const cartItems = document.getElementById('cartItems');
        const cartTotal = document.getElementById('cartTotal');
        const cartBadge = document.getElementById('cartBadge');
        const clearCart = document.getElementById('clearCart');
        const checkoutBtn = document.getElementById('checkoutBtn');
        const addToCartButtons = document.querySelectorAll('.add-to-cart');
        
        // Open cart modal
        cartBtn.addEventListener('click', () => {
            cartModal.style.display = 'flex';
        });
        
        // Close cart modal
        closeCart.addEventListener('click', () => {
            cartModal.style.display = 'none';
        });
        
        // Close modal when clicking outside
        window.addEventListener('click', (e) => {
            if (e.target === cartModal) {
                cartModal.style.display = 'none';
            }
        });
        
        // Add to cart functionality
        addToCartButtons.forEach(button => {
            button.addEventListener('click', () => {
                const name = button.getAttribute('data-name');
                const price = parseInt(button.getAttribute('data-price'));
                
                // Check if item already in cart
                const existingItem = cart.find(item => item.name === name);
                
                if (existingItem) {
                    existingItem.quantity += 1;
                } else {
                    cart.push({
                        name: name,
                        price: price,
                        quantity: 1
                    });
                }
                
                updateCart();
                showNotification(`${name} ditambahkan ke keranjang`);
            });
        });
        
        // Update cart display
        function updateCart() {
            cartItems.innerHTML = '';
            let total = 0;
            let itemCount = 0;
            
            cart.forEach((item, index) => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                itemCount += item.quantity;
                
                const cartItem = document.createElement('div');
                cartItem.className = 'cart-item';
                cartItem.innerHTML = `
                    <div class="cart-item-info">
                        <div>${item.name}</div>
                        <div>Rp ${item.price.toLocaleString('id-ID')} x ${item.quantity}</div>
                    </div>
                    <div class="cart-item-actions">
                        <button class="decrease-quantity" data-index="${index}">-</button>
                        <span>${item.quantity}</span>
                        <button class="increase-quantity" data-index="${index}">+</button>
                        <button class="remove-item" data-index="${index}"><i class="fas fa-trash"></i></button>
                    </div>
                `;
                
                cartItems.appendChild(cartItem);
            });
            
            cartTotal.textContent = `Rp ${total.toLocaleString('id-ID')}`;
            cartBadge.textContent = itemCount;
            
            // Add event listeners to cart item buttons
            document.querySelectorAll('.decrease-quantity').forEach(button => {
                button.addEventListener('click', (e) => {
                    const index = e.target.getAttribute('data-index');
                    if (cart[index].quantity > 1) {
                        cart[index].quantity -= 1;
                    } else {
                        cart.splice(index, 1);
                    }
                    updateCart();
                });
            });
            
            document.querySelectorAll('.increase-quantity').forEach(button => {
                button.addEventListener('click', (e) => {
                    const index = e.target.getAttribute('data-index');
                    cart[index].quantity += 1;
                    updateCart();
                });
            });
            
            document.querySelectorAll('.remove-item').forEach(button => {
                button.addEventListener('click', (e) => {
                    const index = e.target.closest('button').getAttribute('data-index');
                    cart.splice(index, 1);
                    updateCart();
                });
            });
        }
        
        // Clear cart
        clearCart.addEventListener('click', () => {
            if (cart.length > 0) {
                if (confirm('Apakah Anda yakin ingin mengosongkan keranjang?')) {
                    cart = [];
                    updateCart();
                    showNotification('Keranjang berhasil dikosongkan');
                }
            }
        });
        
        // Checkout via WhatsApp
        checkoutBtn.addEventListener('click', () => {
            if (cart.length === 0) {
                alert('Keranjang belanja Anda kosong!');
                return;
            }
            
            let message = "Halo Rimuru Store, saya ingin memesan:\n\n";
            let total = 0;
            
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                message += `- ${item.name} (${item.quantity}x) = Rp ${itemTotal.toLocaleString('id-ID')}\n`;
            });
            
            message += `\nTotal: Rp ${total.toLocaleString('id-ID')}\n\n`;
            message += "Apakah produk tersedia?";
            
            const encodedMessage = encodeURIComponent(message);
            const whatsappUrl = `https://wa.me/6289506222871?text=${encodedMessage}`;
            
            window.open(whatsappUrl, '_blank');
        });
        
        // Show notification
        function showNotification(message) {
            // Create notification element
            const notification = document.createElement('div');
            notification.style.cssText = `
                position: fixed;
                top: 20px;
                right: 20px;
                background-color: var(--primary);
                color: white;
                padding: 1rem 1.5rem;
                border-radius: 4px;
                box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
                z-index: 1000;
                transform: translateX(100%);
                transition: transform 0.3s ease;
            `;
            notification.textContent = message;
            
            document.body.appendChild(notification);
            
            // Animate in
            setTimeout(() => {
                notification.style.transform = 'translateX(0)';
            }, 100);
            
            // Animate out and remove
            setTimeout(() => {
                notification.style.transform = 'translateX(100%)';
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 300);
            }, 3000);
        }
        
        // Product filtering and search
        const searchInput = document.getElementById('searchInput');
        const categoryButtons = document.querySelectorAll('.category-btn');
        const productCards = document.querySelectorAll('.product-card');
        
        // Search functionality
        searchInput.addEventListener('input', () => {
            const searchTerm = searchInput.value.toLowerCase();
            
            productCards.forEach(card => {
                const productName = card.querySelector('.product-header h3').textContent.toLowerCase();
                const productDesc = card.querySelector('.product-header p').textContent.toLowerCase();
                
                if (productName.includes(searchTerm) || productDesc.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });
        
        // Category filtering
        categoryButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove active class from all buttons
                categoryButtons.forEach(btn => btn.classList.remove('active'));
                // Add active class to clicked button
                button.classList.add('active');
                
                const category = button.getAttribute('data-category');
                
                productCards.forEach(card => {
                    if (category === 'all' || card.getAttribute('data-category') === category) {
                        card.style.display = 'block';
                    } else {
                        card.style.display = 'none';
                    }
                });
            });
        });
        
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

        // Video Background Controls
        const backgroundVideo = document.getElementById('backgroundVideo');
        const playPauseVideoBtn = document.getElementById('playPauseVideo');
        const muteUnmuteVideoBtn = document.getElementById('muteUnmuteVideo');
        const playPauseVideoIcon = playPauseVideoBtn.querySelector('i');
        const muteUnmuteVideoIcon = muteUnmuteVideoBtn.querySelector('i');

        playPauseVideoBtn.addEventListener('click', () => {
            if (backgroundVideo.paused) {
                backgroundVideo.play();
                playPauseVideoIcon.classList.remove('fa-play');
                playPauseVideoIcon.classList.add('fa-pause');
            } else {
                backgroundVideo.pause();
                playPauseVideoIcon.classList.remove('fa-pause');
                playPauseVideoIcon.classList.add('fa-play');
            }
        });

        muteUnmuteVideoBtn.addEventListener('click', () => {
            backgroundVideo.muted = !backgroundVideo.muted;
            if (backgroundVideo.muted) {
                muteUnmuteVideoIcon.classList.remove('fa-volume-up');
                muteUnmuteVideoIcon.classList.add('fa-volume-mute');
            } else {
                muteUnmuteVideoIcon.classList.remove('fa-volume-mute');
                muteUnmuteVideoIcon.classList.add('fa-volume-up');
            }
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

        // Loading indicator for video
        const loadingIndicator = document.getElementById('loading');
        const video = document.getElementById('backgroundVideo');
        
        video.addEventListener('loadstart', () => {
            loadingIndicator.style.display = 'flex';
        });
        
        video.addEventListener('canplay', () => {
            loadingIndicator.style.display = 'none';
        });
        
        video.addEventListener('error', () => {
            loadingIndicator.style.display = 'none';
            console.error('Error loading video');
        });
    </script>
</body>
</html>
