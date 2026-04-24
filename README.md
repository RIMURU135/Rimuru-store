
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <title>Rimuru Store - Topup Game & Layanan Digital</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@400;600;700&family=M+PLUS+Rounded+1c:wght@400;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #9b30f9;
            --primary-dark: #7a1fd1;
            --secondary: #1a0a2e;
            --accent: #ff5e9c;
            --accent-dark: #e04880;
            --bg-color: #0d0b1a;
            --text-color: #f0e6ff;
            --card-bg: #1a1228;
            --header-bg: transparent;
            --footer-bg: #060311;
            --section-bg: #0f0c1e;
            --border-light: #3a2a50;
            --shadow: 0 10px 30px rgba(155, 48, 249, 0.2);
            --neon-glow: 0 0 15px rgba(155, 48, 249, 0.5);
            --font-display: 'Noto Serif JP', serif;
            --font-body: 'M PLUS Rounded 1c', 'Segoe UI', sans-serif;
        }

        .light-mode {
            --primary: #6a1b9a;
            --primary-dark: #4a148c;
            --secondary: #f3e5f5;
            --accent: #e91e63;
            --accent-dark: #c2185b;
            --bg-color: #f5f0fa;
            --text-color: #1e1a2b;
            --card-bg: #ffffff;
            --header-bg: rgba(255, 255, 255, 0.85);
            --footer-bg: #ede7f6;
            --section-bg: #f3e5f5;
            --border-light: #d1c4e9;
            --shadow: 0 10px 25px rgba(0,0,0,0.08);
            --neon-glow: 0 0 12px rgba(106,27,154,0.3);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: var(--font-body);
            transition: background-color 0.3s, color 0.3s, border-color 0.3s, box-shadow 0.3s;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1280px;
            margin: 0 auto;
        }

        header {
            background: var(--header-bg);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            color: var(--text-color);
            padding: 0.8rem 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.08);
            box-shadow: 0 2px 20px rgba(0,0,0,0.3);
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
            gap: 10px;
        }

        .logo img {
            height: 44px;
            width: auto;
            border-radius: 50%;
            border: 2px solid var(--accent);
            box-shadow: 0 0 12px var(--accent);
        }

        .logo h1 {
            font-family: var(--font-display);
            font-size: 1.6rem;
            font-weight: 700;
            letter-spacing: 1px;
            background: linear-gradient(135deg, #c084fc, #f472b6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        nav ul {
            display: flex;
            list-style: none;
            align-items: center;
            gap: 0.3rem;
            flex-wrap: wrap;
        }

        nav ul li a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 600;
            padding: 0.5rem 1.1rem;
            border-radius: 30px;
            transition: 0.2s;
            letter-spacing: 0.5px;
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 6px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s;
            border-radius: 2px;
        }

        nav ul li a:hover {
            color: white;
            text-shadow: 0 0 10px var(--accent);
        }

        nav ul li a:hover::after {
            width: 60%;
        }

        .theme-toggle {
            background: rgba(255,255,255,0.08);
            border: 1px solid var(--border-light);
            color: var(--text-color);
            font-size: 1.2rem;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            backdrop-filter: blur(4px);
        }

        .theme-toggle:hover {
            background: var(--primary);
            color: white;
            box-shadow: var(--neon-glow);
        }

        .hero {
            position: relative;
            width: 100%;
            height: 100vh;
            min-height: 600px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            overflow: hidden;
            background-color: #0a0418;
        }

        .video-background {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center center;
            z-index: 0;
            opacity: 0.9;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(30, 10, 60, 0.75), rgba(10, 5, 35, 0.8));
            z-index: 1;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 2rem;
            animation: fadeUp 1s ease;
        }

        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(40px);}
            to { opacity: 1; transform: translateY(0);}
        }

        .hero h2 {
            font-family: var(--font-display);
            font-size: 3.2rem;
            margin-bottom: 0.8rem;
            text-shadow: 0 0 30px rgba(200, 100, 255, 0.7);
            letter-spacing: 2px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
            text-shadow: 0 0 15px rgba(0,0,0,0.8);
            font-weight: 400;
            opacity: 0.9;
        }

        .video-controls {
            position: absolute;
            bottom: 25px;
            left: 25px;
            z-index: 3;
            display: flex;
            gap: 12px;
        }

        .video-controls button {
            background: rgba(20, 10, 40, 0.7);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.3);
            color: white;
            width: 44px;
            height: 44px;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            transition: 0.2s;
        }

        .video-controls button:hover {
            background: var(--accent);
            box-shadow: 0 0 20px var(--accent);
            transform: scale(1.1);
        }

        .btn {
            display: inline-block;
            background: transparent;
            color: white;
            padding: 0.8rem 2.4rem;
            border-radius: 50px;
            font-weight: 700;
            text-decoration: none;
            transition: 0.3s;
            border: 2px solid white;
            letter-spacing: 1px;
            backdrop-filter: blur(4px);
            background: rgba(255,255,255,0.1);
            box-shadow: 0 4px 15px rgba(255, 94, 156, 0.3);
        }

        .btn:hover {
            background: var(--accent);
            border-color: var(--accent);
            transform: translateY(-4px);
            box-shadow: 0 8px 25px var(--accent);
        }

        section {
            padding: 5rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3.5rem;
        }

        .section-title h2 {
            font-family: var(--font-display);
            font-size: 2.6rem;
            display: inline-block;
            padding-bottom: 0.5rem;
            position: relative;
            letter-spacing: 1px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 70px;
            height: 3px;
            background: var(--accent);
            box-shadow: 0 0 15px var(--accent);
            border-radius: 2px;
        }

        .product-filters {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin-bottom: 2.5rem;
        }

        .search-box {
            flex: 2;
            min-width: 250px;
            position: relative;
        }

        .search-box input {
            width: 100%;
            padding: 0.9rem 1.2rem 0.9rem 2.8rem;
            border: 1px solid var(--border-light);
            border-radius: 50px;
            background: var(--card-bg);
            color: var(--text-color);
            font-weight: 500;
            backdrop-filter: blur(4px);
        }

        .search-box i {
            position: absolute;
            left: 1.2rem;
            top: 50%;
            transform: translateY(-50%);
            color: var(--accent);
        }

        .category-filters {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
        }

        .category-btn {
            padding: 0.5rem 1.3rem;
            background: var(--card-bg);
            border: 1px solid var(--border-light);
            border-radius: 40px;
            cursor: pointer;
            font-weight: 600;
            transition: 0.2s;
            letter-spacing: 0.5px;
        }

        .category-btn.active {
            background: var(--primary);
            color: white;
            border-color: var(--primary);
            box-shadow: 0 0 15px var(--primary);
        }

        .products {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: var(--card-bg);
            border-radius: 24px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: all 0.3s;
            border: 1px solid var(--border-light);
            backdrop-filter: blur(4px);
        }

        .product-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(155, 48, 249, 0.3);
            border-color: var(--accent);
        }

        .product-header {
            background: linear-gradient(135deg, #3b1f6e, #1e0a3c);
            color: white;
            padding: 1.4rem;
            text-align: center;
            border-bottom: 2px solid var(--accent);
        }

        .product-header h3 {
            font-family: var(--font-display);
            font-size: 1.7rem;
            letter-spacing: 0.5px;
        }

        .product-body {
            padding: 1.3rem;
            max-height: 420px;
            overflow-y: auto;
            background: rgba(0,0,0,0.15);
        }

        .price-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0.7rem 0;
            border-bottom: 1px dashed var(--border-light);
        }

        .add-to-cart {
            background: var(--primary);
            border: none;
            color: white;
            padding: 0.4rem 1.1rem;
            border-radius: 30px;
            cursor: pointer;
            font-size: 0.8rem;
            font-weight: 700;
            transition: 0.2s;
        }

        .add-to-cart:hover {
            background: var(--accent);
            box-shadow: 0 0 12px var(--accent);
        }

        .cart-container {
            position: fixed;
            bottom: 28px;
            left: 28px;
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
            box-shadow: 0 8px 25px rgba(255, 94, 156, 0.6);
            transition: 0.3s;
        }
        .cart-btn:hover {
            transform: scale(1.1);
            box-shadow: 0 12px 30px var(--accent);
        }
        .cart-badge {
            position: absolute;
            top: -6px;
            right: -6px;
            background: #ffcc00;
            color: #1e1a2b;
            font-weight: bold;
            border-radius: 50px;
            width: 28px;
            height: 28px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.4);
        }
        .cart-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.85);
            backdrop-filter: blur(5px);
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
            border: 1px solid var(--border-light);
            box-shadow: 0 20px 50px rgba(155,48,249,0.4);
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
            flex-wrap: wrap;
        }
        .btn-clear, .btn-checkout {
            padding: 0.6rem 1.4rem;
            border-radius: 40px;
            border: none;
            cursor: pointer;
            font-weight: 700;
            letter-spacing: 0.5px;
        }
        .btn-clear { background: #475569; color: white; }
        .btn-checkout { background: #25D366; color: white; box-shadow: 0 0 15px rgba(37,211,102,0.5); }

        .testimonials {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }
        .testimonial-card {
            background: var(--card-bg);
            padding: 1.8rem;
            border-radius: 28px;
            width: 280px;
            box-shadow: var(--shadow);
            border: 1px solid var(--border-light);
            transition: 0.3s;
        }
        .testimonial-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
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
            border: 2px solid var(--accent);
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
            padding: 1.8rem;
            border-radius: 28px;
            text-align: center;
            width: 220px;
            border: 1px solid var(--border-light);
        }
        .social-links a {
            color: white;
            background: #2d1b4e;
            display: inline-block;
            margin: 0 6px;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            line-height: 40px;
            text-align: center;
            transition: 0.2s;
        }
        .social-links a:hover {
            background: var(--accent);
            box-shadow: 0 0 15px var(--accent);
        }

        footer {
            background: var(--footer-bg);
            color: #c4b5e5;
            padding: 2.5rem 0 1rem;
            border-top: 1px solid var(--border-light);
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
            border-top: 1px solid #2e1c44;
        }

        .loading {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(5,2,20,0.95);
            z-index: 9999;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            color: white;
            backdrop-filter: blur(10px);
        }
        @keyframes spin { to { transform: rotate(360deg); } }

        @media (max-width: 780px) {
            .hero h2 { font-size: 2.1rem; }
            .hero p { font-size: 0.95rem; }
            .header-content { flex-direction: column; }
            .category-filters { justify-content: center; }
            .section-title h2 { font-size: 2rem; }
        }

        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #1a1228; }
        ::-webkit-scrollbar-thumb { background: #9b30f9; border-radius: 10px; }
    </style>
</head>
<body>
<div class="loading" id="loading">
    <div style="width:50px;height:50px;border:5px solid rgba(255,255,255,0.2);border-top:5px solid var(--accent);border-radius:50%;animation:spin 1s linear infinite;margin-bottom:1rem;"></div>
    <p>Memuat dunia anime...</p>
</div>

<div class="cart-container">
    <button class="cart-btn" id="cartBtn"><i class="fas fa-shopping-cart"></i><span class="cart-badge" id="cartBadge">0</span></button>
</div>
<div class="cart-modal" id="cartModal">
    <div class="cart-content">
        <div class="cart-header"><h2>🛒 Keranjang</h2><button id="closeCart">&times;</button></div>
        <div id="cartItems"></div>
        <div class="cart-total"><span>Total : </span><span id="cartTotal">Rp 0</span></div>
        <div class="cart-actions"><button class="btn-clear" id="clearCart">Kosongkan</button><button class="btn-checkout" id="checkoutBtn"><i class="fab fa-whatsapp"></i> Checkout WA</button></div>
    </div>
</div>

<header>
    <div class="container header-content">
        <div class="logo">
            <img src="https://file.idnet.my.id/api/preview.php?file=ymggle9h.png" alt="Rimuru Store">
            <h1>Rimuru Store</h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Beranda</a></li>
                <li><a href="#products">Produk</a></li>
                <li><a href="#about">Tentang</a></li>
                <li><a href="#testimonials">Testimoni</a></li>
                <li><a href="#contact">Kontak</a></li>
                <li><button class="theme-toggle" id="themeToggle"><i class="fas fa-moon"></i></button></li>
            </ul>
        </nav>
    </div>
</header>

<section class="hero" id="home">
    <!-- VIDEO BACKGROUND DIGANTI -->
    <video class="video-background" id="backgroundVideo" autoplay muted loop playsinline poster="https://picsum.photos/id/104/1920/1080">
        <source src="https://www.image2url.com/r2/default/videos/1777021085438-4c5933f8-2d34-4fd4-b6b1-ea879e8ed302.mp4" type="video/mp4">
    </video>
    <div class="video-controls">
        <button id="playPauseVideo"><i class="fas fa-pause"></i></button>
        <button id="muteUnmuteVideo"><i class="fas fa-volume-up"></i></button>
    </div>
    <div class="hero-content">
        <h2>Topup Game & Layanan Digital</h2>
        <p>Proses kilat • Harga bersahabat • Pelayanan 24/7</p>
        <a href="#products" class="btn">Jelajahi Produk</a>
    </div>
</section>

<section id="products">
    <div class="container">
        <div class="section-title"><h2>🔥 Produk Kami</h2></div>
        <div class="product-filters">
            <div class="search-box">
                <i class="fas fa-search"></i>
                <input type="text" id="searchInput" placeholder="Cari diamond, robux, UC...">
            </div>
            <div class="category-filters">
                <button class="category-btn active" data-category="all">Semua</button>
                <button class="category-btn" data-category="freefire">Free Fire</button>
                <button class="category-btn" data-category="mobilelegends">Mobile Legends</button>
                <button class="category-btn" data-category="roblox">Roblox</button>
                <button class="category-btn" data-category="cod">Call of Duty</button>
                <button class="category-btn" data-category="pubg">PUBG</button>
                <button class="category-btn" data-category="genshin">Genshin Impact</button>
                <button class="category-btn" data-category="lainnya">Lainnya</button>
            </div>
        </div>
        <div class="products" id="productsContainer"></div>
    </div>
</section>

<section id="about" style="background-color: var(--section-bg);">
    <div class="container">
        <div class="section-title"><h2>Tentang Kami</h2></div>
        <div class="about-content">
            <p>Rimuru Store hadir sejak 2020 sebagai penyedia topup game & layanan digital terpercaya. Dengan semangat pelayanan ala dunia anime, kami menawarkan proses super cepat, harga kompetitif, dan dukungan ramah 24 jam.</p>
            <div style="margin-top:1.2rem"><strong>💳 Metode Pembayaran:</strong> DANA, GOPAY, OVO, SPAY, SEA BANK, QRIS</div>
            <div><strong>📞 Nomor Transaksi:</strong> 0831-4042-7092 | BANK JAGO: 901428220963</div>
        </div>
    </div>
</section>

<section id="testimonials">
    <div class="container">
        <div class="section-title"><h2>⭐ Testimoni Pelanggan</h2></div>
        <div class="testimonials">
            <div class="testimonial-card">
                <div class="testimonial-header">
                    <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Rizky">
                    <div><h4>Rizky P.</h4><p>Free Fire</p></div>
                </div>
                <div class="testimonial-rating">★★★★★</div>
                <p>"Diamond masuk 2 menit, admin ramah, jadi langganan!"</p>
            </div>
            <div class="testimonial-card">
                <div class="testimonial-header">
                    <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Sarah">
                    <div><h4>Sarah W.</h4><p>Mobile Legends</p></div>
                </div>
                <div class="testimonial-rating">★★★★★</div>
                <p>"Murah, cepat, recommended banget!"</p>
            </div>
            <div class="testimonial-card">
                <div class="testimonial-header">
                    <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Andi">
                    <div><h4>Andi S.</h4><p>Bot WA</p></div>
                </div>
                <div class="testimonial-rating">★★★★½</div>
                <p>"Sewa bot stabil, respon sigap. Mantap!"</p>
            </div>
        </div>
    </div>
</section>

<section id="contact" style="background-color: var(--section-bg);">
    <div class="container">
        <div class="section-title"><h2>📱 Hubungi Kami</h2></div>
        <div class="contact-info">
            <div class="contact-card">
                <i class="fab fa-whatsapp fa-2x" style="color:#25D366;"></i>
                <h4>WhatsApp</h4>
                <p>0831-4042-7092</p>
            </div>
            <div class="contact-card">
                <i class="fab fa-instagram fa-2x" style="color:#E1306C;"></i>
                <h4>Instagram</h4>
                <p>@ZAINALA_KEYΖΙ</p>
            </div>
        </div>
    </div>
</section>

<footer>
    <div class="container">
        <div class="footer-content">
            <div>
                <h3>Rimuru Store</h3>
                <p>Topup game & digital terpercaya sejak 2020.</p>
            </div>
            <div>
                <h4>Navigasi</h4>
                <a href="#home" style="color: #c4b5e5; display:block;">Beranda</a>
                <a href="#products" style="color: #c4b5e5; display:block;">Produk</a>
                <a href="#contact" style="color: #c4b5e5; display:block;">Kontak</a>
            </div>
            <div class="social-links">
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-whatsapp"></i></a>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2025 Rimuru Store. All rights reserved. | Tema terinspirasi oleh dunia anime.</p>
        </div>
    </div>
</footer>

<script>
    (function() {
        // TEMA GELAP/TERANG (default gelap)
        const body = document.body;
        const themeToggle = document.getElementById('themeToggle');
        const icon = themeToggle.querySelector('i');

        function updateThemeUI() {
            if (body.classList.contains('light-mode')) {
                icon.classList.remove('fa-moon');
                icon.classList.add('fa-sun');
            } else {
                icon.classList.remove('fa-sun');
                icon.classList.add('fa-moon');
            }
        }

        themeToggle.addEventListener('click', () => {
            body.classList.toggle('light-mode');
            updateThemeUI();
        });
        updateThemeUI();

        // VIDEO HERO CONTROLS
        const video = document.getElementById('backgroundVideo');
        const playPauseBtn = document.getElementById('playPauseVideo');
        const muteUnmuteBtn = document.getElementById('muteUnmuteVideo');
        if (video && playPauseBtn && muteUnmuteBtn) {
            playPauseBtn.addEventListener('click', () => {
                if (video.paused) {
                    video.play();
                    playPauseBtn.innerHTML = '<i class="fas fa-pause"></i>';
                } else {
                    video.pause();
                    playPauseBtn.innerHTML = '<i class="fas fa-play"></i>';
                }
            });
            muteUnmuteBtn.addEventListener('click', () => {
                video.muted = !video.muted;
                muteUnmuteBtn.innerHTML = video.muted ? '<i class="fas fa-volume-mute"></i>' : '<i class="fas fa-volume-up"></i>';
            });
        }

        // DATA PRODUK LENGKAP (Netflix, Disney+, Voucher Google Play dihapus)
        const productsData = [
            {
                category: "freefire",
                name: "Free Fire",
                prices: [
                    "5 Diamonds - Rp 1.000",
                    "12 Diamonds - Rp 2.000",
                    "20 Diamonds - Rp 3.000",
                    "35 Diamonds - Rp 5.000",
                    "50 Diamonds - Rp 7.000",
                    "70 Diamonds - Rp 10.000",
                    "100 Diamonds - Rp 14.000",
                    "140 Diamonds - Rp 20.000",
                    "200 Diamonds - Rp 28.000",
                    "355 Diamonds - Rp 50.000",
                    "500 Diamonds - Rp 70.000",
                    "1000 Diamonds - Rp 140.000"
                ]
            },
            {
                category: "mobilelegends",
                name: "Mobile Legends",
                prices: [
                    "11 Diamonds - Rp 3.000",
                    "22 Diamonds - Rp 6.000",
                    "30 Diamonds - Rp 8.000",
                    "56 Diamonds - Rp 15.000",
                    "86 Diamonds - Rp 22.000",
                    "172 Diamonds - Rp 44.000",
                    "257 Diamonds - Rp 66.000",
                    "344 Diamonds - Rp 88.000",
                    "514 Diamonds - Rp 132.000",
                    "600 Diamonds - Rp 154.000",
                    "706 Diamonds - Rp 180.000",
                    "1000 Diamonds - Rp 250.000"
                ]
            },
            {
                category: "roblox",
                name: "Roblox",
                prices: [
                    "40 Robux - Rp 6.000",
                    "80 Robux - Rp 12.000",
                    "160 Robux - Rp 24.000",
                    "240 Robux - Rp 36.000",
                    "320 Robux - Rp 48.000",
                    "450 Robux - Rp 67.000",
                    "800 Robux - Rp 120.000",
                    "1000 Robux - Rp 150.000",
                    "2000 Robux - Rp 300.000"
                ]
            },
            {
                category: "cod",
                name: "Call of Duty",
                prices: [
                    "31 CP - Rp 5.000",
                    "53 CP - Rp 8.000",
                    "62 CP - Rp 10.000",
                    "124 CP - Rp 20.000",
                    "155 CP - Rp 25.000",
                    "310 CP - Rp 50.000",
                    "620 CP - Rp 100.000",
                    "1260 CP - Rp 200.000"
                ]
            },
            {
                category: "pubg",
                name: "PUBG Mobile",
                prices: [
                    "30 UC - Rp 6.000",
                    "60 UC - Rp 12.000",
                    "120 UC - Rp 24.000",
                    "180 UC - Rp 36.000",
                    "300 UC - Rp 60.000",
                    "600 UC - Rp 120.000",
                    "1500 UC - Rp 300.000",
                    "3000 UC - Rp 600.000"
                ]
            },
            {
                category: "genshin",
                name: "Genshin Impact",
                prices: [
                    "60 Genesis Crystals - Rp 12.000",
                    "300+30 Genesis Crystals - Rp 60.000",
                    "980+110 Genesis Crystals - Rp 200.000",
                    "1980+260 Genesis Crystals - Rp 400.000",
                    "3280+600 Genesis Crystals - Rp 650.000",
                    "6480+1600 Genesis Crystals - Rp 1.300.000"
                ]
            },
            {
                category: "lainnya",
                name: "Layanan Digital",
                prices: [
                    "Spotify Premium 1 Bulan - Rp 55.000",
                    "YouTube Premium 1 Bulan - Rp 65.000",
                    "Bot WhatsApp 1 Bulan - Rp 15.000",
                    "Sewa Bot Discord 1 Bulan - Rp 20.000"
                ]
            }
        ];

        let cart = [];
        const productsContainer = document.getElementById('productsContainer');
        const cartBtn = document.getElementById('cartBtn');
        const cartModal = document.getElementById('cartModal');
        const closeCart = document.getElementById('closeCart');
        const cartItemsDiv = document.getElementById('cartItems');
        const cartTotalSpan = document.getElementById('cartTotal');
        const cartBadge = document.getElementById('cartBadge');
        const clearCartBtn = document.getElementById('clearCart');
        const checkoutBtn = document.getElementById('checkoutBtn');
        const searchInput = document.getElementById('searchInput');
        const categoryButtons = document.querySelectorAll('.category-btn');
        let activeCategory = 'all';

        function displayProducts(filter = 'all', searchTerm = '') {
            productsContainer.innerHTML = '';
            const filtered = productsData.filter(p => {
                const matchCat = filter === 'all' || p.category === filter;
                const matchSearch = p.name.toLowerCase().includes(searchTerm.toLowerCase()) ||
                    p.prices.some(pr => pr.toLowerCase().includes(searchTerm.toLowerCase()));
                return matchCat && matchSearch;
            });

            if (filtered.length === 0) {
                productsContainer.innerHTML = '<p style="grid-column:1/-1;text-align:center;">Tidak ada produk ditemukan.</p>';
                return;
            }

            filtered.forEach(product => {
                const card = document.createElement('div');
                card.className = 'product-card';
                card.innerHTML = `
                    <div class="product-header"><h3>${product.name}</h3></div>
                    <div class="product-body">
                        ${product.prices.map(price => `
                            <div class="price-item">
                                <span>${price}</span>
                                <button class="add-to-cart" data-product="${product.name}" data-price="${price}">+ Topup</button>
                            </div>
                        `).join('')}
                    </div>
                `;
                productsContainer.appendChild(card);
            });

            document.querySelectorAll('.add-to-cart').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const name = e.target.dataset.product;
                    const priceStr = e.target.dataset.price;
                    const priceNumber = parseInt(priceStr.replace(/[^0-9]/g, ''));
                    addToCart(name, priceStr, priceNumber);
                });
            });
        }

        function addToCart(name, priceStr, priceNumber) {
            cart.push({ name, priceStr, priceNumber });
            updateCartUI();
        }

        function updateCartUI() {
            cartBadge.textContent = cart.length;
            cartItemsDiv.innerHTML = '';
            let total = 0;
            cart.forEach((item, index) => {
                total += item.priceNumber;
                const div = document.createElement('div');
                div.className = 'cart-item';
                div.innerHTML = `<span>${item.name} - ${item.priceStr}</span>
                    <button class="remove-item" data-index="${index}" style="background:none;border:none;color:var(--accent);cursor:pointer;font-size:1.2rem;">&times;</button>`;
                cartItemsDiv.appendChild(div);
            });
            cartTotalSpan.textContent = 'Rp ' + total.toLocaleString('id-ID');

            document.querySelectorAll('.remove-item').forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const index = e.target.dataset.index;
                    cart.splice(index, 1);
                    updateCartUI();
                });
            });
        }

        cartBtn.addEventListener('click', () => cartModal.style.display = 'flex');
        closeCart.addEventListener('click', () => cartModal.style.display = 'none');
        window.addEventListener('click', (e) => { if (e.target === cartModal) cartModal.style.display = 'none'; });
        clearCartBtn.addEventListener('click', () => { cart = []; updateCartUI(); });
        checkoutBtn.addEventListener('click', () => {
            if (cart.length === 0) return alert('Keranjang kosong!');
            let message = 'Halo Rimuru Store, saya mau order:%0A';
            cart.forEach(item => message += `- ${item.name} : ${item.priceStr}%0A`);
            const total = cart.reduce((s, i) => s + i.priceNumber, 0);
            message += `%0ATotal: Rp ${total.toLocaleString('id-ID')}`;
            window.open(`https://wa.me/6283140427092?text=${message}`, '_blank');
        });

        searchInput.addEventListener('input', () => displayProducts(activeCategory, searchInput.value));
        categoryButtons.forEach(btn => {
            btn.addEventListener('click', () => {
                categoryButtons.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                activeCategory = btn.dataset.category;
                displayProducts(activeCategory, searchInput.value);
            });
        });

        window.addEventListener('load', () => {
            const loading = document.getElementById('loading');
            loading.style.display = 'flex';
            setTimeout(() => {
                loading.style.display = 'none';
                displayProducts();
            }, 1000);
        });
    })();
</script>
</body>
</html>
