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

        /* Header */
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

        /* HERO + VIDEO - TIDAK TERPOTONG, LANDSCAPE UTUH */
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

        /* Filter & Produk */
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

        /* Cart */
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

        /* Testimoni */
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

        /* Kontak */
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
        <div class="logo"><img src="https://file.idnet.my.id/api/preview.php?file=ymggle9h.png" alt="Rimuru Store"><h1>Rimuru Store</h1></div>
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

<section id="about" style="background-color: var(--section-bg);"><div class="container"><div class="section-title"><h2>Tentang Kami</h2></div><div class="about-content"><p>Rimuru Store adalah penyedia topup game & layanan digital terpercaya sejak 2020. Proses super cepat, harga miring, dan dukungan ramah. Metode pembayaran: DANA, GOPAY, OVO, SPAY, SEA BANK, QRIS. CS 24 jam siap membantu.</p><div style="margin-top:1rem"><strong>💳 Metode Pembayaran:</strong> 0831-4042-7092 (Semua e-Wallet) / BANK JAGO : 901428220963</div></div></div></section>

<section id="testimonials"><div class="container"><div class="section-title"><h2>⭐ Testimoni</h2></div><div class="testimonials"><div class="testimonial-card"><div class="testimonial-header"><img src="https://randomuser.me/api/portraits/men/32.jpg"><div><h4>Rizky P.</h4><p>FF Player</p></div></div><div class="testimonial-rating">★★★★★</div><p>"Diamond masuk dalam 2 menit, admin baik, jadi langganan!"</p></div><div class="testimonial-card"><div class="testimonial-header"><img src="https://randomuser.me/api/portraits/women/44.jpg"><div><h4>Sarah W.</h4><p>MLBB</p></div></div><div class="testimonial-rating">★★★★★</div><p>"Murah meriah, proses cepet. Rekomended!"</p></div><div class="testimonial-card"><div class="testimonial-header"><img src="https://randomuser.me/api/portraits/men/75.jpg"><div><h4>Andi S.</h4><p>Bot WA</p></div></div><div class="testimonial-rating">★★★★½</div><p>"Sewa bot stabil, respon admin sigap. Mantap!"</p></div></div></div></section>

<section id="contact" style="background-color: var(--section-bg);"><div class="container"><div class
