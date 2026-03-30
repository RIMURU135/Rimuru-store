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

<section id="contact" style="background-color: var(--section-bg);"><div class="container"><div class="section-title"><h2>Hubungi Kami</h2></div><div class="contact-info"><div class="contact-card"><i class="fas fa-user fa-2x"></i><h3>Admin</h3><p>Irwan Ariel</p></div><div class="contact-card"><i class="fab fa-whatsapp fa-2x"></i><h3>WhatsApp</h3><p><a href="https://wa.me/6283140427092" style="color:var(--primary)">0831-4042-7092</a></p></div><div class="contact-card"><i class="fas fa-envelope fa-2x"></i><h3>Email</h3><p>irwanaril798@gmail.com</p></div><div class="contact-card"><i class="fas fa-map-marker-alt fa-2x"></i><h3>Lokasi</h3><p>Riau, Indonesia</p></div></div></div></section>

<footer><div class="container"><div class="footer-content"><div><h3>Rimuru Store</h3><p>Topup gaming terpercaya & layanan digital</p></div><div><h3>Menu</h3><ul style="list-style:none"><li><a href="#home" style="color:white">Beranda</a></li><li><a href="#products" style="color:white">Produk</a></li></ul></div><div><h3>Sosial</h3><div class="social-links"><a href="https://wa.me/6283140427092"><i class="fab fa-whatsapp"></i></a><a href="https://www.instagram.com/zainala_keyzi"><i class="fab fa-instagram"></i></a><a href="#"><i class="fab fa-facebook"></i></a></div></div></div><div class="copyright"><p>© 2025 Rimuru Store - All rights reserved.</p></div></div></footer>

<script>
    // ========= DATA PRODUK LENGKAP =========
    const productsData = [
        { category: "freefire", name: "Free Fire 12 💎", price: 2500, display: "12 💎 = 2.500" },
        { category: "freefire", name: "Free Fire 25 💎", price: 4999, display: "25 💎 = 4.999" },
        { category: "freefire", name: "Free Fire 50 💎", price: 7300, display: "50 💎 = 7.300" }, { category: "freefire", name: "Free Fire 75 💎", price: 10000, display: "75 💎 = 10.000" },
        { category: "freefire", name: "Free Fire 100 💎", price: 14000, display: "100 💎 = 14.000" }, { category: "freefire", name: "Free Fire 150 💎", price: 19900, display: "150 💎 = 19.900" },
        { category: "freefire", name: "Free Fire 200 💎", price: 26000, display: "200 💎 = 26.000" }, { category: "freefire", name: "Free Fire Membership Mingguan", price: 28000, display: "Membership Mingguan = 28.000" },
        { category: "mobilelegends", name: "Mobile Legends 14 💎", price: 4500, display: "14 💎 = 4.500" }, { category: "mobilelegends", name: "Mobile Legends 36 💎", price: 10500, display: "36 💎 = 10.500" },
        { category: "mobilelegends", name: "Mobile Legends 50 💎", price: 14500, display: "50 💎 = 14.500" }, { category: "mobilelegends", name: "Mobile Legends 85 💎", price: 23000, display: "85 💎 = 23.000" },
        { category: "mobilelegends", name: "Mobile Legends 112 💎", price: 31000, display: "112 💎 = 31.000" }, { category: "mobilelegends", name: "Mobile Legends 185 💎", price: 50000, display: "185 💎 = 50.000" },
        { category: "mobilelegends", name: "Mobile Legends 284 💎", price: 75000, display: "284 💎 = 75.000" }, { category: "mobilelegends", name: "Mobile Legends 429 💎", price: 111000, display: "429 💎 = 111.000" },
        { category: "mobilelegends", name: "Mobile Legends 600 💎", price: 154000, display: "600 💎 = 154.000" }, { category: "mobilelegends", name: "Mobile Legends 792 💎", price: 206000, display: "792 💎 = 206.000" },
        { category: "mobilelegends", name: "Mobile Legends 1050 💎", price: 265000, display: "1050 💎 = 265.000" },
        { category: "roblox", name: "Roblox 100 Robux", price: 18000, display: "100 Robux = 18.000" }, { category: "roblox", name: "Roblox 400 Robux", price: 77000, display: "400 Robux = 77.000" }, { category: "roblox", name: "Roblox Gift Card 200rb", price: 203000, display: "Gift Card = 203.000" },
        { category: "cod", name: "COD 26 CP", price: 5500, display: "26 CP = 5.500" }, { category: "cod", name: "COD 127 CP", price: 18800, display: "127 CP = 18.800" }, { category: "cod", name: "COD 528 CP", price: 96000, display: "528 CP = 96.000" }, { category: "cod", name: "COD 1056 CP", price: 185000, display: "1056 CP = 185.000" },
        { category: "pubg", name: "PUBG 52 UC", price: 16000, display: "52 UC = 16.000" }, { category: "pubg", name: "PUBG 263 UC", price: 74000, display: "263 UC = 74.000" }, { category: "pubg", name: "PUBG 500 UC", price: 112000, display: "500 UC = 112.000" }, { category: "pubg", name: "PUBG 1000 UC", price: 242000, display: "1000 UC = 242.000" },
        { category: "lainnya", name: "Sewa Bot WA 1 bulan", price: 5000, display: "Bot WA 1 bulan = 5.000" }, { category: "lainnya", name: "Sewa Bot WA 1 tahun", price: 25000, display: "Bot WA 1 tahun = 25.000" },
        { category: "lainnya", name: "Suntik Tiktok 500 Like", price: 1000, display: "TikTok 500 Like = 1.000" }, { category: "lainnya", name: "Suntik IG 100 Follow", price: 3000, display: "IG 100 Follow = 3.000" }
    ];

    function buildProductsHTML() {
        const container = document.getElementById('productsContainer');
        const grouped = {};
        productsData.forEach(p => { if (!grouped[p.category]) grouped[p.category] = []; grouped[p.category].push(p); });
        let html = '';
        for (let cat in grouped) {
            let catName = cat === 'freefire' ? 'Free Fire' : cat === 'mobilelegends' ? 'Mobile Legends' : cat === 'roblox' ? 'Roblox' : cat === 'cod' ? 'Call of Duty' : cat === 'pubg' ? 'PUBG' : 'Layanan Digital';
            html += `<div class="product-card" data-category="${cat}"><div class="product-header"><h3>${catName}</h3><p>💎 Topup murah</p></div><div class="product-body">`;
            grouped[cat].forEach(item => { html += `<div class="price-item"><span>${item.display}</span><button class="add-to-cart" data-name="${item.name}" data-price="${item.price}">+ Keranjang</button></div>`; });
            html += `</div></div>`;
        }
        container.innerHTML = html;
        attachCartEvents();
    }

    function attachCartEvents() { document.querySelectorAll('.add-to-cart').forEach(btn => btn.addEventListener('click', addToCartHandler)); }
    let cart = [];
    function addToCartHandler(e) { const name = e.currentTarget.getAttribute('data-name'); const price = parseInt(e.currentTarget.getAttribute('data-price')); const exist = cart.find(i => i.name === name); if(exist) exist.quantity++; else cart.push({name, price, quantity: 1}); updateCartUI(); showNotif(`✅ ${name} ditambahkan`); }
    function updateCartUI() { let total = 0, count = 0; const container = document.getElementById('cartItems'); container.innerHTML = ''; cart.forEach((item, idx) => { const itemTot = item.price * item.quantity; total += itemTot; count += item.quantity; const div = document.createElement('div'); div.className = 'cart-item'; div.innerHTML = `<div><b>${item.name}</b><br>Rp${item.price.toLocaleString()} x ${item.quantity}</div><div><button class="decr" data-idx="${idx}">-</button> <span>${item.quantity}</span> <button class="incr" data-idx="${idx}">+</button> <button class="rem" data-idx="${idx}"><i class="fas fa-trash"></i></button></div>`; container.appendChild(div); });
        document.querySelectorAll('.decr').forEach(btn => btn.addEventListener('click', e => { let i = btn.getAttribute('data-idx'); if(cart[i].quantity > 1) cart[i].quantity--; else cart.splice(i,1); updateCartUI(); }));
        document.querySelectorAll('.incr').forEach(btn => btn.addEventListener('click', e => { let i = btn.getAttribute('data-idx'); cart[i].quantity++; updateCartUI(); }));
        document.querySelectorAll('.rem').forEach(btn => btn.addEventListener('click', e => { let i = btn.getAttribute('data-idx'); cart.splice(i,1); updateCartUI(); }));
        document.getElementById('cartTotal').innerText = `Rp ${total.toLocaleString('id-ID')}`; document.getElementById('cartBadge').innerText = count;
    }
    function showNotif(msg) { const n = document.createElement('div'); n.innerText = msg; n.style.cssText = 'position:fixed;top:20px;right:20px;background:var(--primary);color:white;padding:12px 20px;border-radius:40px;z-index:9999'; document.body.appendChild(n); setTimeout(()=>n.remove(),2500); }

    // Filter & search
    let activeCategory = 'all'; let searchTerm = '';
    function filterProducts() {
        const cards = document.querySelectorAll('.product-card');
        cards.forEach(card => { const cat = card.getAttribute('data-category'); const title = card.querySelector('.product-header h3')?.innerText.toLowerCase() || ''; const matchCat = activeCategory === 'all' || cat === activeCategory; const matchSearch = title.includes(searchTerm.toLowerCase()) || card.innerText.toLowerCase().includes(searchTerm.toLowerCase()); card.style.display = (matchCat && matchSearch) ? 'block' : 'none'; });
    }
    document.getElementById('searchInput').addEventListener('input', e => { searchTerm = e.target.value; filterProducts(); });
    document.querySelectorAll('.category-btn').forEach(btn => { btn.addEventListener('click', () => { document.querySelectorAll('.category-btn').forEach(b=>b.classList.remove('active')); btn.classList.add('active'); activeCategory = btn.getAttribute('data-category'); filterProducts(); }); });

    // Cart Modal
    document.getElementById('cartBtn').onclick = () => document.getElementById('cartModal').style.display = 'flex';
    document.getElementById('closeCart').onclick = () => document.getElementById('cartModal').style.display = 'none';
    window.onclick = e => { if(e.target === document.getElementById('cartModal')) document.getElementById('cartModal').style.display = 'none'; };
    document.getElementById('clearCart').onclick = () => { if(cart.length && confirm('Kosongkan keranjang?')) { cart = []; updateCartUI(); showNotif('Keranjang dikosongkan'); } };
    document.getElementById('checkoutBtn').onclick = () => { if(!cart.length) return alert('Keranjang kosong!'); let msg = 'Halo Rimuru Store, saya ingin order:\n'; let total=0; cart.forEach(i=>{ let sub=i.price*i.quantity; total+=sub; msg+=`- ${i.name} (${i.quantity}x) = Rp${sub.toLocaleString()}\n`; }); msg+=`\nTotal: Rp${total.toLocaleString()}\nApakah ready?`; window.open(`https://wa.me/6283140427092?text=${encodeURIComponent(msg)}`,'_blank'); };

    // Video: object-fit contain (tidak terpotong), kontrol play/mute
    const video = document.getElementById('backgroundVideo');
    const fallbackDiv = document.getElementById('videoFallback');
    video.onerror = () => { video.style.display = 'none'; fallbackDiv.style.display = 'block'; fallbackDiv.style.background = "linear-gradient(135deg, #0f2027, #2c5364)"; document.getElementById('loading').style.display = 'none'; };
    video.addEventListener('canplay', () => document.getElementById('loading').style.display = 'none');
    video.addEventListener('loadstart', () => document.getElementById('loading').style.display = 'flex');
    document.getElementById('playPauseVideo').addEventListener('click', () => { if(video.paused) video.play(); else video.pause(); });
    document.getElementById('muteUnmuteVideo').addEventListener('click', () => { video.muted = !video.muted; const icon = document.querySelector('#muteUnmuteVideo i'); icon.className = video.muted ? 'fas fa-volume-mute' : 'fas fa-volume-up'; });
    video.addEventListener('play', () => { document.querySelector('#playPauseVideo i').className = 'fas fa-pause'; });
    video.addEventListener('pause', () => { document.querySelector('#playPauseVideo i').className = 'fas fa-play'; });

    // Dark Mode (tanpa musik)
    const themeToggle = document.getElementById('themeToggle'); const body = document.body;
    if(localStorage.getItem('theme') === 'dark-mode') body.classList.add('dark-mode'), themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
    themeToggle.onclick = () => { body.classList.toggle('dark-mode'); const isDark = body.classList.contains('dark-mode'); localStorage.setItem('theme', isDark ? 'dark-mode' : ''); themeToggle.innerHTML = isDark ? '<i class="fas fa-sun"></i>' : '<i class="fas fa-moon"></i>'; };
    
    buildProductsHTML(); updateCartUI(); filterProducts();
    document.querySelectorAll('a[href^="#"]').forEach(anchor => anchor.addEventListener('click', function(e){ e.preventDefault(); document.querySelector(this.getAttribute('href')).scrollIntoView({behavior:'smooth'}); }));
    setTimeout(() => { if(video.readyState === 0) { video.style.display = 'none'; fallbackDiv.style.display = 'block'; fallbackDiv.style.background = "#1e293b"; document.getElementById('loading').style.display = 'none'; } }, 3000);
</script>
</body>
</html>
