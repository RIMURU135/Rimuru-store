<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>Rimuru Store - Topup Game & Layanan Digital Terpercaya</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, system-ui, sans-serif;
            transition: background-color 0.2s ease, color 0.2s, border-color 0.2s;
        }

        :root {
            --primary: #3498db;
            --primary-dark: #2980b9;
            --secondary: #2c3e50;
            --accent: #e74c3c;
            --accent-dark: #c0392b;
            --bg-color: #f8fafc;
            --text-color: #1e293b;
            --card-bg: #ffffff;
            --header-bg: linear-gradient(135deg, #2c3e50, #1a2632);
            --footer-bg: #0f172a;
            --section-bg: #f1f5f9;
            --border-light: #e2e8f0;
            --shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.05);
        }

        .dark-mode {
            --primary: #3b82f6;
            --primary-dark: #2563eb;
            --secondary: #1e293b;
            --accent: #f97316;
            --accent-dark: #ea580c;
            --bg-color: #0f172a;
            --text-color: #e2e8f0;
            --card-bg: #1e293b;
            --header-bg: linear-gradient(135deg, #0f172a, #020617);
            --footer-bg: #020617;
            --section-bg: #111827;
            --border-light: #334155;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.5;
        }

        .container {
            width: 90%;
            max-width: 1280px;
            margin: 0 auto;
        }

        header {
            background: var(--header-bg);
            color: white;
            padding: 0.8rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(2px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo img {
            height: 48px;
            width: auto;
            border-radius: 12px;
        }

        .logo h1 {
            font-size: 1.6rem;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        nav ul {
            display: flex;
            list-style: none;
            align-items: center;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 1rem;
            border-radius: 40px;
            transition: 0.2s;
        }

        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        .theme-toggle {
            background: rgba(255,255,255,0.15);
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .hero {
            position: relative;
            width: 100%;
            height: 100vh;
            min-height: 560px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            overflow: hidden;
            background-color: #000;
        }

        .video-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: contain;
            object-position: center center;
            background-color: #000;
            z-index: 0;
        }

        .hero-video-fallback {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
            z-index: 0;
            display: none;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            z-index: 1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 820px;
            padding: 2rem;
            animation: fadeUp 0.8s ease;
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(30px);}
            to { opacity: 1; transform: translateY(0);}
        }

        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 12px rgba(0,0,0,0.5);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            text-shadow: 1px 1px 6px rgba(0,0,0,0.4);
        }

        .video-controls {
            position: absolute;
            bottom: 20px;
            left: 20px;
            z-index: 3;
            display: flex;
            gap: 12px;
        }

        .video-controls button {
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(6px);
            border: none;
            color: white;
            width: 44px;
            height: 44px;
            border-radius: 60px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: 0.2s;
        }

        .video-controls button:hover {
            background: var(--primary);
            transform: scale(1.05);
        }

        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.8rem 2rem;
            border-radius: 60px;
            font-weight: 600;
            text-decoration: none;
            transition: 0.2s;
            box-shadow: 0 6px 14px rgba(0,0,0,0.2);
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background: var(--accent-dark);
            transform: translateY(-3px);
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
            display: inline-block;
            padding-bottom: 0.5rem;
            border-bottom: 4px solid var(--primary);
        }

        .product-filters {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1.2rem;
            margin-bottom: 2rem;
        }

        .search-box {
            flex: 2;
            min-width: 240px;
            position: relative;
        }

        .search-box input {
            width: 100%;
            padding: 0.8rem 1rem 0.8rem 2.6rem;
            border: 1px solid var(--border-light);
            border-radius: 60px;
            background: var(--card-bg);
            color: var(--text-color);
        }

        .search-box i {
            position: absolute;
            left: 1rem;
            top: 50%;
            transform: translateY(-50%);
            color: #7f8c8d;
        }

        .category-filters {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
        }

        .category-btn {
            padding: 0.5rem 1.2rem;
            background: var(--card-bg);
            border: 1px solid var(--border-light);
            border-radius: 40px;
            cursor: pointer;
            font-weight: 500;
            transition: 0.2s;
            color: var(--text-color);
        }

        .category-btn.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: var(--card-bg);
            border-radius: 28px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.25s;
            border: 1px solid var(--border-light);
        }

        .product-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 20px 30px -12px rgba(0,0,0,0.2);
        }

        .product-header {
            background: var(--primary);
            color: white;
            padding: 1.2rem;
            text-align: center;
        }

        .product-header h3 {
            font-size: 1.6rem;
        }

        .product-body {
            padding: 1.2rem;
            max-height: 420px;
            overflow-y: auto;
        }

        .price-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.65rem 0;
            border-bottom: 1px dashed var(--border-light);
        }

        .add-to-cart {
            background: var(--primary);
            border: none;
            color: white;
            padding: 0.3rem 0.9rem;
            border-radius: 30px;
            cursor: pointer;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .add-to-cart:hover {
            background: var(--primary-dark);
        }

        .cart-container {
            position: fixed;
            bottom: 24px;
            left: 24px;
            z-index: 1000;
        }
        .cart-btn {
            background: var(--accent);
            width: 64px;
            height: 64px;
            border-radius: 50%;
            border: none;
            font-size: 1.8rem;
            color: white;
            cursor: pointer;
            box-shadow: 0 10px 20px rgba(0,0,0,0.25);
        }
        .cart-badge {
            position: absolute;
            top: -6px;
            right: -6px;
            background: #f1c40f;
            color: #1e293b;
            font-weight: bold;
            border-radius: 40px;
            width: 26px;
            height: 26px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
        }
        .cart-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            z-index: 1100;
            align-items: center;
            justify-content: center;
        }
        .cart-content {
            background: var(--card-bg);
            width: 90%;
            max-width: 520px;
            max-height: 85vh;
            border-radius: 32px;
            padding: 1.8rem;
            overflow-y: auto;
        }
        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        #closeCart {
            background: none;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            color: var(--text-color);
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.8rem 0;
            border-bottom: 1px solid var(--border-light);
        }
        .cart-total {
            font-weight: bold;
            font-size: 1.3rem;
            margin: 1rem 0;
            text-align: right;
        }
        .cart-actions {
            display: flex;
            gap: 1rem;
            justify-content: flex-end;
        }
        .btn-clear, .btn-checkout {
            padding: 0.6rem 1.2rem;
            border-radius: 40px;
            border: none;
            cursor: pointer;
            font-weight: 600;
        }
        .btn-clear { background: #94a3b8; color: white; }
        .btn-checkout { background: #25D366; color: white; }

        .testimonials {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }
        .testimonial-card {
            background: var(--card-bg);
            padding: 1.5rem;
            border-radius: 28px;
            width: 280px;
            box-shadow: var(--shadow);
        }
        .testimonial-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }
        .testimonial-header img {
            width: 55px;
            height: 55px;
            border-radius: 50%;
            object-fit: cover;
        }
        .testimonial-rating { color: #fbbf24; margin: 0.5rem 0; }

        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem;
            justify-content: center;
        }
        .contact-card {
            background: var(--card-bg);
            padding: 1.5rem;
            border-radius: 28px;
            text-align: center;
            width: 220px;
        }
        .social-links a {
            color: white;
            background: #2c3e50;
            display: inline-block;
            margin: 0 6px;
            width: 38px;
            height: 38px;
            border-radius: 50%;
            line-height: 38px;
            text-align: center;
        }

        footer {
            background: var(--footer-bg);
            color: #cbd5e1;
            padding: 2.5rem 0 1rem;
        }
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 2rem;
        }
        .copyright {
            text-align: center;
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #334155;
        }

        .loading {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.85);
            z-index: 9999;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            color: white;
        }
        @keyframes spin { to { transform: rotate(360deg); } }
        @media (max-width: 780px) {
            .hero h2 { font-size: 2rem; }
            .hero p { font-size: 1rem; }
            .header-content { flex-direction: column; }
            .category-filters { justify-content: center; }
        }
        @media (orientation: landscape) and (max-width: 900px) {
            .hero { min-height: 100vh; }
            .hero h2 { font-size: 1.8rem; }
        }
    </style>
</head>
<body>
<div class="loading" id="loading">
    <div style="width:50px;height:50px;border:5px solid rgba(255,255,255,0.3);border-top:5px solid white;border-radius:50%;animation:spin 1s linear infinite;margin-bottom:1rem;"></div>
    <p>Memuat pengalaman terbaik...</p>
</div>

<div class="cart-container">
    <button class="cart-btn" id="cartBtn"><i class="fas fa-shopping-cart"></i><span class="cart-badge" id="cartBadge">0</span></button>
</div>
<div class="cart-modal" id="cartModal">
    <div class="cart-content">
        <div class="cart-header"><h2>🛒 Keranjang Belanja</h2><button id="closeCart">&times;</button></div>
        <div id="cartItems"></div>
        <div class="cart-total"><span>Total : </span><span id="cartTotal">Rp 0</span></div>
        <div class="cart-actions"><button class="btn-clear" id="clearCart">Kosongkan</button><button class="btn-checkout" id="checkoutBtn">Checkout WA</button></div>
    </div>
</div>

<header>
    <div class="container header-content">
        <div class="logo">
            <img src="https://www.image2url.com/r2/default/files/1777688423905-b001353d-1314-4be4-8fd1-d9d6ef69bc51.jpg" alt="Rimuru Store Logo" style="height:48px; width:48px; object-fit:cover; border-radius:50%;">
            <h1>Rimuru Store</h1>
        </div>
        <nav><ul><li><a href="#home">Beranda</a></li><li><a href="#products">Produk</a></li><li><a href="#about">Tentang</a></li><li><a href="#testimonials">Testimoni</a></li><li><a href="#contact">Kontak</a></li><li><button class="theme-toggle" id="themeToggle"><i class="fas fa-moon"></i></button></li></ul></nav>
    </div>
</header>

<section class="hero" id="home">
    <video class="video-background" id="backgroundVideo" autoplay muted loop playsinline poster="https://picsum.photos/id/104/1920/1080">
        <source src="https://image2url.com/r2/default/videos/1774790761304-592aeffb-1a5b-4038-872b-48cc9d92b619.mp4" type="video/mp4">
    </video>
    <div class="hero-video-fallback" id="videoFallback"></div>
    <div class="video-controls"><button id="playPauseVideo"><i class="fas fa-pause"></i></button><button id="muteUnmuteVideo"><i class="fas fa-volume-up"></i></button></div>
    <div class="hero-content"><h2>Topup Game & Layanan Digital Terpercaya</h2><p>Proses cepat, harga terjangkau, pelayanan 24/7</p><a href="#products" class="btn">Lihat Produk</a></div>
</section>

<section id="products"><div class="container"><div class="section-title"><h2>🔥 Produk Kami</h2></div>
<div class="product-filters"><div class="search-box"><i class="fas fa-search"></i><input type="text" id="searchInput" placeholder="Cari diamond, robux, UC..."></div>
<div class="category-filters"><button class="category-btn active" data-category="all">Semua</button><button class="category-btn" data-category="freefire">Free Fire</button><button class="category-btn" data-category="mobilelegends">Mobile Legends</button><button class="category-btn" data-category="roblox">Roblox</button><button class="category-btn" data-category="cod">Call of Duty</button><button class="category-btn" data-category="pubg">PUBG</button><button class="category-btn" data-category="lainnya">Lainnya</button></div></div>
<div class="products" id="productsContainer"></div></div></section>

<section id="about" style="background-color: var(--section-bg);"><div class="container"><div class="section-title"><h2>Tentang Kami</h2></div><div class="about-content"><p>Rimuru Store adalah penyedia topup game & layanan digital terpercaya sejak 2020. Proses super cepat, harga miring, dan dukungan ramah. Metode pembayaran: DANA, GOPAY, OVO, SPAY, SEA BANK, QRIS. CS 24 jam siap membantu.</p><div style="margin-top:1rem"><strong>💳 Metode Pembayaran:</strong> 0831-4042-7092 (Semua e-Wallet) / BANK JAGO : 901428220963</div>
        <div style="margin-top:2rem; text-align:center;">
            <p><strong>📱 Scan QRIS untuk Pembayaran</strong></p>
            <img src="https://www.image2url.com/r2/default/files/1777684205267-2fa2694c-ba5a-4e46-8a96-f17da2fb7fa2.png" alt="QRIS Rimuru Store" style="max-width:280px; width:100%; height:auto; border-radius:20px; box-shadow:0 8px 20px rgba(0,0,0,0.1); margin-top:0.5rem;">
        </div>
    </div></div></section>

<section id="testimonials"><div class="container"><div class="section-title"><h2>⭐ Testimoni</h2></div><div class="testimonials"><div class="testimonial-card"><div class="testimonial-header"><img src="https://randomuser.me/api/portraits/men/32.jpg"><div><h4>Rizky P.</h4><p>FF Player</p></div></div><div class="testimonial-rating">★★★★★</div><p>"Diamond masuk dalam 2 menit, admin baik, jadi langganan!"</p></div><div class="testimonial-card"><div class="testimonial-header"><img src="https://randomuser.me/api/portraits/women/44.jpg"><div><h4>Sarah W.</h4><p>MLBB</p></div></div><div class="testimonial-rating">★★★★★</div><p>"Murah meriah, proses cepet. Rekomended!"</p></div><div class="testimonial-card"><div class="testimonial-header"><img src="https://randomuser.me/api/portraits/men/75.jpg"><div><h4>Andi S.</h4><p>Bot WA</p></div></div><div class="testimonial-rating">★★★★½</div><p>"Sewa bot stabil, respon admin sigap. Mantap!"</p></div></div></div></section>

<section id="contact" style="background-color: var(--section-bg);"><div class="container"><div class="section-title"><h2>📞 Hubungi Kami</h2></div>
<div class="contact-info">
    <div class="contact-card"><i class="fab fa-whatsapp fa-3x" style="color:#25D366"></i><h3>WhatsApp</h3><p>0812-3456-7890</p></div>
    <div class="contact-card"><i class="fab fa-instagram fa-3x" style="color:#E1306C"></i><h3>Instagram</h3><p>@ZAINALA_KEYΖΙ</p></div>
    <div class="contact-card"><i class="fas fa-envelope fa-3x" style="color:#EA4335"></i><h3>Email</h3><p>irwanaril798@gmail.com</p></div>
    <div class="contact-card"><i class="fas fa-user fa-3x" style="color:#3498db"></i><h3>Admin</h3><p>Irwan Aril</p></div>
</div>
<div style="text-align:center; margin-top:2rem" class="social-links">
    <a href="#"><i class="fab fa-whatsapp"></i></a>
    <a href="#"><i class="fab fa-instagram"></i></a>
    <a href="#"><i class="fab fa-tiktok"></i></a>
</div></div></section>

<footer>
    <div class="container footer-content">
        <div><h3>Rimuru Store</h3><p>Topup Game & Layanan Digital #1</p></div>
        <div><h4>Navigasi</h4><p><a href="#home" style="color:#cbd5e1">Beranda</a> | <a href="#products" style="color:#cbd5e1">Produk</a> | <a href="#contact" style="color:#cbd5e1">Kontak</a></p></div>
        <div><p>Jam Operasional: 24/7</p><p>Metode: DANA, GOPAY, OVO, QRIS, Bank Transfer</p></div>
    </div>
    <div class="copyright"><p>&copy; 2026 Rimuru Store. All rights reserved.</p></div>
</footer>

<script>
    (function() {
        // ========== DATA PRODUK ==========
        const productData = {
            freefire: {
                name: "Free Fire",
                items: [
                    { name: "70 Diamond", price: 8000 },
                    { name: "140 Diamond", price: 16000 },
                    { name: "355 Diamond", price: 40000 },
                    { name: "720 Diamond", price: 80000 },
                    { name: "1450 Diamond", price: 160000 },
                    { name: "2180 Diamond", price: 240000 },
                    { name: "3640 Diamond", price: 400000 },
                    { name: "Bundle Mingguan", price: 30000 },
                    { name: "Bundle Bulanan", price: 90000 },
                ]
            },
            mobilelegends: {
                name: "Mobile Legends",
                items: [
                    { name: "86 Diamonds", price: 20000 },
                    { name: "172 Diamonds", price: 40000 },
                    { name: "344 Diamonds", price: 80000 },
                    { name: "429 Diamonds", price: 100000 },
                    { name: "706 Diamonds", price: 160000 },
                    { name: "878 Diamonds", price: 200000 },
                    { name: "Starlight Member", price: 120000 },
                    { name: "Weekly Diamond Pass", price: 30000 },
                ]
            },
            roblox: {
                name: "Roblox",
                items: [
                    { name: "100 Robux", price: 16000 },
                    { name: "200 Robux", price: 32000 },
                    { name: "400 Robux", price: 64000 },
                    { name: "800 Robux", price: 120000 },
                    { name: "1000 Robux", price: 150000 },
                    { name: "2000 Robux", price: 300000 },
                ]
            },
            cod: {
                name: "Call of Duty",
                items: [
                    { name: "80 CP", price: 8000 },
                    { name: "160 CP", price: 16000 },
                    { name: "400 CP", price: 40000 },
                    { name: "800 CP", price: 80000 },
                    { name: "1600 CP", price: 160000 },
                    { name: "4000 CP", price: 400000 },
                ]
            },
            pubg: {
                name: "PUBG Mobile",
                items: [
                    { name: "60 UC", price: 8000 },
                    { name: "120 UC", price: 16000 },
                    { name: "300 UC", price: 40000 },
                    { name: "600 UC", price: 80000 },
                    { name: "1500 UC", price: 200000 },
                    { name: "3000 UC", price: 400000 },
                    { name: "Royale Pass", price: 120000 },
                ]
            },
            lainnya: {
                name: "Layanan Lainnya",
                items: [
                    { name: "Sewa Bot WA (1 bulan)", price: 35000 },
                    { name: "Sewa Bot WA (3 bulan)", price: 90000 },
                    { name: "Joki Rank ML (Epic-Legend)", price: 50000 },
                    { name: "Joki Rank ML (Mythic)", price: 100000 },
                    { name: "Google Play ID 50K", price: 52000 },
                    { name: "Google Play ID 100K", price: 102000 },
                    { name: "Voucher Steam 50K", price: 52000 },
                    { name: "Spotify Premium 1 Bulan", price: 25000 },
                    { name: "Netflix 1 Bulan", price: 45000 },
                ]
            }
        };

        // ========== STATE ==========
        let cart = [];
        let currentCategory = 'all';
        let searchTerm = '';

        // ========== DOM ELEMENTS ==========
        const productsContainer = document.getElementById('productsContainer');
        const searchInput = document.getElementById('searchInput');
        const categoryBtns = document.querySelectorAll('.category-btn');
        const cartBtn = document.getElementById('cartBtn');
        const cartModal = document.getElementById('cartModal');
        const closeCart = document.getElementById('closeCart');
        const cartItems = document.getElementById('cartItems');
        const cartTotal = document.getElementById('cartTotal');
        const cartBadge = document.getElementById('cartBadge');
        const clearCartBtn = document.getElementById('clearCart');
        const checkoutBtn = document.getElementById('checkoutBtn');
        const themeToggle = document.getElementById('themeToggle');
        const loadingEl = document.getElementById('loading');
        const backgroundVideo = document.getElementById('backgroundVideo');
        const videoFallback = document.getElementById('videoFallback');
        const playPauseVideo = document.getElementById('playPauseVideo');
        const muteUnmuteVideo = document.getElementById('muteUnmuteVideo');

        // ========== FUNCTIONS ==========
        function renderProducts() {
            if (!productsContainer) return;
            let html = '';
            const categories = Object.keys(productData);
            
            categories.forEach(cat => {
                if (currentCategory !== 'all' && currentCategory !== cat) return;
                const product = productData[cat];
                const filteredItems = product.items.filter(item => 
                    item.name.toLowerCase().includes(searchTerm.toLowerCase()) ||
                    product.name.toLowerCase().includes(searchTerm.toLowerCase())
                );
                
                if (filteredItems.length === 0) return;
                
                html += `
                    <div class="product-card" data-category="${cat}">
                        <div class="product-header"><h3>${product.name}</h3></div>
                        <div class="product-body">
                            ${filteredItems.map((item, index) => `
                                <div class="price-item">
                                    <span>${item.name}</span>
                                    <div style="display:flex;align-items:center;gap:0.5rem;">
                                        <span style="font-weight:600;">Rp ${item.price.toLocaleString('id-ID')}</span>
                                        <button class="add-to-cart" data-category="${cat}" data-index="${index}" data-name="${item.name}" data-price="${item.price}">+</button>
                                    </div>
                                </div>
                            `).join('')}
                        </div>
                    </div>
                `;
            });
            
            if (html === '') {
                html = '<div style="text-align:center;padding:3rem;grid-column:1/-1;">Produk tidak ditemukan. Coba kata kunci lain.</div>';
            }
            productsContainer.innerHTML = html;
            
            document.querySelectorAll('.add-to-cart').forEach(btn => {
                btn.addEventListener('click', function() {
                    const name = this.dataset.name;
                    const price = parseInt(this.dataset.price);
                    const category = this.dataset.category;
                    addToCart({ name, price, category });
                });
            });
        }

        function addToCart(item) {
            const existing = cart.find(i => i.name === item.name && i.category === item.category);
            if (existing) {
                existing.qty = (existing.qty || 1) + 1;
            } else {
                cart.push({ ...item, qty: 1 });
            }
            updateCart();
            cartBtn.style.transform = 'scale(1.1)';
            setTimeout(() => { cartBtn.style.transform = ''; }, 200);
        }

        function removeFromCart(index) {
            if (cart[index].qty > 1) {
                cart[index].qty -= 1;
            } else {
                cart.splice(index, 1);
            }
            updateCart();
        }

        function updateCart() {
            const total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
            const totalItems = cart.reduce((sum, item) => sum + item.qty, 0);
            
            cartBadge.textContent = totalItems;
            cartTotal.textContent = 'Rp ' + total.toLocaleString('id-ID');
            
            if (cart.length === 0) {
                cartItems.innerHTML = '<p style="text-align:center;padding:1rem;">Keranjang kosong</p>';
            } else {
                cartItems.innerHTML = cart.map((item, i) => `
                    <div class="cart-item">
                        <div>
                            <strong>${item.name}</strong>
                            <div style="font-size:0.8rem;color:#7f8c8d;">${item.qty}x Rp ${item.price.toLocaleString('id-ID')}</div>
                        </div>
                        <div style="display:flex;align-items:center;gap:0.5rem;">
                            <span>Rp ${(item.price * item.qty).toLocaleString('id-ID')}</span>
                            <button onclick="window._removeFromCart(${i})" style="background:#e74c3c;color:white;border:none;border-radius:50%;width:24px;height:24px;cursor:pointer;">-</button>
                        </div>
                    </div>
                `).join('');
            }
        }

        window._removeFromCart = function(index) {
            removeFromCart(index);
        };

        function checkout() {
            if (cart.length === 0) return alert('Keranjang masih kosong!');
            let message = 'Halo Rimuru Store, saya ingin memesan:%0A%0A';
            cart.forEach(item => {
                message += `- ${item.name} (${item.qty}x) : Rp ${(item.price * item.qty).toLocaleString('id-ID')}%0A`;
            });
            const total = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
            message += `%0ATotal: Rp ${total.toLocaleString('id-ID')}%0A%0AMohon info pembayaran.`;
            window.open(`https://wa.me/6281234567890?text=${message}`, '_blank');
        }

        function setActiveCategory(category) {
            currentCategory = category;
            categoryBtns.forEach(btn => {
                btn.classList.toggle('active', btn.dataset.category === category);
            });
            renderProducts();
        }

        // ========== EVENT LISTENERS ==========
        searchInput.addEventListener('input', function(e) {
            searchTerm = e.target.value;
            renderProducts();
        });

        categoryBtns.forEach(btn => {
            btn.addEventListener('click', function() {
                setActiveCategory(this.dataset.category);
            });
        });

        cartBtn.addEventListener('click', () => { cartModal.style.display = 'flex'; });
        closeCart.addEventListener('click', () => { cartModal.style.display = 'none'; });
        cartModal.addEventListener('click', function(e) {
            if (e.target === cartModal) cartModal.style.display = 'none';
        });
        clearCartBtn.addEventListener('click', () => { cart = []; updateCart(); });
        checkoutBtn.addEventListener('click', checkout);

        const darkPref = localStorage.getItem('darkMode');
        if (darkPref === 'enabled') {
            document.body.classList.add('dark-mode');
            themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
        }
        themeToggle.addEventListener('click', () => {
            document.body.classList.toggle('dark-mode');
            if (document.body.classList.contains('dark-mode')) {
                localStorage.setItem('darkMode', 'enabled');
                themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
            } else {
                localStorage.setItem('darkMode', 'disabled');
                themeToggle.innerHTML = '<i class="fas fa-moon"></i>';
            }
        });

        playPauseVideo.addEventListener('click', () => {
            if (backgroundVideo.paused) {
                backgroundVideo.play();
                playPauseVideo.innerHTML = '<i class="fas fa-pause"></i>';
            } else {
                backgroundVideo.pause();
                playPauseVideo.innerHTML = '<i class="fas fa-play"></i>';
            }
        });
        muteUnmuteVideo.addEventListener('click', () => {
            backgroundVideo.muted = !backgroundVideo.muted;
            muteUnmuteVideo.innerHTML = backgroundVideo.muted ? '<i class="fas fa-volume-mute"></i>' : '<i class="fas fa-volume-up"></i>';
        });

        backgroundVideo.addEventListener('error', () => {
            backgroundVideo.style.display = 'none';
            videoFallback.style.display = 'block';
        });

        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                const href = this.getAttribute('href');
                if (href === '#') return;
                e.preventDefault();
                const target = document.querySelector(href);
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });

        window.addEventListener('load', () => {
            loadingEl.style.display = 'none';
        });
        setTimeout(() => { loadingEl.style.display = 'none'; }, 3000);

        renderProducts();
        updateCart();
    })();
</script>
</body>
</html>
