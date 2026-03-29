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
        
        /* Hero Section dengan Video Background - DIPERBAIKI */
        .hero {
            position: relative;
            height: 60vh;
            min-height: 500px; /* tambahan agar tidak terlalu pendek di mobile */
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            overflow: hidden;
        }
        
        .video-background {
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100%;
            height: 100%;
            transform: translate(-50%, -50%);
            object-fit: cover;           /* memastikan full cover tanpa stretch */
            object-position: center;     /* center agar tidak terpotong bagian penting */
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
        <!-- Video Background - DIPERBAIKI -->
        <video class="video-background" id="backgroundVideo" autoplay muted loop playsinline>
            <source src="https://assets.mixkit.co/videos/preview/12345/12345-large.mp4" type="video/mp4"> <!-- Ganti dengan link video landscape Anda yang bagus -->
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

    <!-- Bagian lain dari website tetap sama (products, about, testimonials, contact, footer, script) -->
    <!-- ... (semua kode dari section id="products" sampai akhir script tetap persis seperti kode asli Anda) ... -->

    <!-- Untuk menjaga agar kode tidak terlalu panjang di respons ini, saya sarankan copy-paste seluruh bagian dari <section id="products"> sampai akhir </html> dari kode asli Anda. -->

    <!-- Script tetap sama seperti asli -->
    <script>
        // (Paste seluruh script JavaScript dari kode asli Anda di sini - tidak ada perubahan)
        // Cart functionality, music, video controls, dark mode, dll. tetap sama.
    </script>
</body>
</html>
