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
        
        /* BACKGROUND VIDEO - FULL UKURAN & TIDAK TERPOTONG (Landscape + Portrait) */
        .hero {
            position: relative;
            height: 100vh;
            min-height: 500px;
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
            min-width: 100%;
            min-height: 100%;
            transform: translate(-50%, -50%);
            object-fit: cover;
            object-position: center center;
            z-index: -1;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.65);
            z-index: 0;
        }
        
        @media (orientation: portrait) {
            .hero { height: 100vh; }
            .video-background { object-position: center top; }
        }
        
        @media (orientation: landscape) {
            .hero { height: 100vh; }
            .video-background { object-position: center center; }
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            padding: 2rem;
        }
        
        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.3rem;
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
        
        section { padding: 4rem 0; }
        .section-title { text-align: center; margin-bottom: 3rem; }
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
        
        .product-filters { display: flex; justify-content: space-between; align-items: center; margin-bottom: 2rem; flex-wrap: wrap; gap: 1rem; }
        .search-box { flex: 1; min-width: 250px; position: relative; }
        .search-box input { width: 100%; padding: 0.8rem 1rem 0.8rem 2.5rem; border: 1px solid #ddd; border-radius: 4px; background-color: var(--card-bg); color: var(--text-color); }
        .search-box i { position: absolute; left: 0.8rem; top: 50%; transform: translateY(-50%); color: #777; }
        .category-filters { display: flex; gap: 0.5rem; flex-wrap: wrap; }
        .category-btn { padding: 0.5rem 1rem; background-color: var(--card-bg); border: 1px solid #ddd; border-radius: 4px; cursor: pointer; transition: all 0.3s ease; }
        .category-btn.active { background-color: var(--primary); color: white; border-color: var(--primary); }
        .products { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 2rem; }
        .product-card { background-color: var(--card-bg); border-radius: 8px; overflow: hidden; box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1); transition: transform 0.3s ease, box-shadow 0.3s ease; }
        .product-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15); }
        .product-header { background-color: var(--primary); color: white; padding: 1rem; text-align: center; }
        .product-header h3 { font-size: 1.4rem; margin-bottom: 0.5rem; }
        .product-body { padding: 1.5rem; max-height: 400px; overflow-y: auto; }
        .price-item { display: flex; justify-content: space-between; align-items: center; padding: 0.5rem 0; border-bottom: 1px dashed rgba(0, 0, 0, 0.1); }
        .price-item:last-child { border-bottom: none; }
        .add-to-cart { background-color: var(--primary); color: white; border: none; border-radius: 4px; padding: 0.3rem 0.7rem; cursor: pointer; transition: background-color 0.3s; }
        .add-to-cart:hover { background-color: #2980b9; }
        
        .cart-container { position: fixed; bottom: 20px; left: 20px; z-index: 1000; }
        .cart-btn { background-color: var(--accent); color: white; border: none; border-radius: 50%; width: 60px; height: 60px; display: flex; align-items: center; justify-content: center; font-size: 1.5rem; cursor: pointer; box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2); }
        .cart-badge { position: absolute; top: -5px; right: -5px; background-color: #e74c3c; color: white; border-radius: 50%; width: 25px; height: 25px; display: flex; align-items: center; justify-content: center; font-size: 0.8rem; font-weight: bold; }
        .cart-modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background-color: rgba(0, 0, 0, 0.5); z-index: 1001; align-items: center; justify-content: center; }
        .cart-content { background-color: var(--card-bg); border-radius: 8px; width: 90%; max-width: 500px; max-height: 80vh; overflow-y: auto; padding: 2rem; box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2); }
        .music-player { position: fixed; bottom: 20px; right: 20px; background-color: var(--card-bg); border-radius: 50%; width: 60px; height: 60px; display: flex; align-items: center; justify-content: center; box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2); cursor: pointer; z-index: 99; }
        .video-controls { position: absolute; bottom: 20px; left: 20px; z-index: 2; display: flex; gap: 10px; }
        .video-controls button { background: rgba(255, 255, 255, 0.2); border: none; color: white; width: 40px; height: 40px; border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; transition: all 0.3s ease; }
        .loading { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background-color: rgba(0, 0, 0, 0.7); z-index: 9999; align-items: center; justify-content: center; flex-direction: column; color: white; }
        .loading-spinner { width: 50px; height: 50px; border: 5px solid rgba(255, 255, 255, 0.3); border-radius: 50%; border-top-color: white; animation: spin 1s linear infinite; margin-bottom: 1rem; }
        @keyframes spin { to { transform: rotate(360deg); } }
        
        @media (max-width: 768px) {
            .hero h2 { font-size: 2.2rem; }
            .video-controls { bottom: 10px; left: 10px; }
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
            <div class="cart-items" id="cartItems"></div>
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
        <!-- Video Background Full Ukuran -->
        <video class="video-background" id="backgroundVideo" autoplay muted loop playsinline>
            <source src="https://image2url.com/r2/default/videos/1774790761304-592aeffb-1a5b-4038-872b-48cc9d92b619.mp4" type="video/mp4">
            Browser Anda tidak mendukung video HTML5.
        </video>
        
        <div class="video-controls">
            <button id="playPauseVideo"><i class="fas fa-pause"></i></button>
            <button id="muteUnmuteVideo"><i class="fas fa-volume-up"></i></button>
        </div>
        
        <div class="hero-content">
            <h2>Topup Game & Layanan Digital Terpercaya</h2>
            <p>Proses cepat, harga terjangkau, dan pelayanan ramah 24/7</p>
            <a href="#products" class="btn">Lihat Produk</a>
        </div>
    </section>

    <section id="products">
        <div class="container">
            <div class="section-title"><h2>Produk Kami</h2></div>
            
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
                    <div class="product-header"><h3>Free Fire</h3><p>FF | Epep | FREE FIRE 💎💸</p></div>
                    <div class="product-body">
                        <div class="price-item"><span>12 💎 = 2.500</span><button class="add-to-cart" data-name="Free Fire 12 💎" data-price="2500">+ Keranjang</button></div>
                        <div class="price-item"><span>25 💎 = 4.999</span><button class="add-to-cart" data-name="Free Fire 25 💎" data-price="4999">+ Keranjang</button></div>
                        <div class="price-item"><span>50 💎 = 7.300</span><button class="add-to-cart" data-name="Free Fire 50 💎" data-price="7300">+ Keranjang</button></div>
                        <div class="price-item"><span>75 💎 = 10.000</span><button class="add-to-cart" data-name="Free Fire 75 💎" data-price="10000">+ Keranjang</button></div>
                        <div class="price-item"><span>90 💎 = 12.999</span><button class="add-to-cart" data-name="Free Fire 90 💎" data-price="12999">+ Keranjang</button></div>
                        <div class="price-item"><span>100 💎 = 14.000</span><button class="add-to-cart" data-name="Free Fire 100 💎" data-price="14000">+ Keranjang</button></div>
                        <div class="price-item"><span>120 💎 = 16.000</span><button class="add-to-cart" data-name="Free Fire 120 💎" data-price="16000">+ Keranjang</button></div>
                        <div class="price-item"><span>130 💎 = 18.000</span><button class="add-to-cart" data-name="Free Fire 130 💎" data-price="18000">+ Keranjang</button></div>
                        <div class="price-item"><span>150 💎 = 19.900</span><button class="add-to-cart" data-name="Free Fire 150 💎" data-price="19900">+ Keranjang</button></div>
                        <div class="price-item"><span>160 💎 = 21.000</span><button class="add-to-cart" data-name="Free Fire 160 💎" data-price="21000">+ Keranjang</button></div>
                        <div class="price-item"><span>180 💎 = 23.999</span><button class="add-to-cart" data-name="Free Fire 180 💎" data-price="23999">+ Keranjang</button></div>
                        <div class="price-item"><span>190 💎 = 25.000</span><button class="add-to-cart" data-name="Free Fire 190 💎" data-price="25000">+ Keranjang</button></div>
                        <div class="price-item"><span>200 💎 = 26.000</span><button class="add-to-cart" data-name="Free Fire 200 💎" data-price="26000">+ Keranjang</button></div>
                        <div class="price-item"><span>210 💎 = 27.000</span><button class="add-to-cart" data-name="Free Fire 210 💎" data-price="27000">+ Keranjang</button></div>
                        <div class="price-item"><span>Membership Mingguan = 28.000</span><button class="add-to-cart" data-name="Free Fire Membership Mingguan" data-price="28000">+ Keranjang</button></div>
                        <div class="price-item"><span>250 💎 = 32.000</span><button class="add-to-cart" data-name="Free Fire 250 💎" data-price="32000">+ Keranjang</button></div>
                    </div>
                </div>

                <!-- Mobile Legends -->
                <div class="product-card" data-category="mobilelegends">
                    <div class="product-header"><h3>Mobile Legends</h3><p>MLBB | Diamonds 💎💸</p></div>
                    <div class="product-body">
                        <div class="price-item"><span>14 💎 = 4.500</span><button class="add-to-cart" data-name="Mobile Legends 14 💎" data-price="4500">+ Keranjang</button></div>
                        <div class="price-item"><span>19 💎 = 6.400</span><button class="add-to-cart" data-name="Mobile Legends 19 💎" data-price="6400">+ Keranjang</button></div>
                        <div class="price-item"><span>36 💎 = 10.500</span><button class="add-to-cart" data-name="Mobile Legends 36 💎" data-price="10500">+ Keranjang</button></div>
                        <div class="price-item"><span>44 💎 = 13.000</span><button class="add-to-cart" data-name="Mobile Legends 44 💎" data-price="13000">+ Keranjang</button></div>
                        <div class="price-item"><span>50 💎 = 14.500</span><button class="add-to-cart" data-name="Mobile Legends 50 💎" data-price="14500">+ Keranjang</button></div>
                        <div class="price-item"><span>59 💎 = 16.000</span><button class="add-to-cart" data-name="Mobile Legends 59 💎" data-price="16000">+ Keranjang</button></div>
                        <div class="price-item"><span>65 💎 = 18.000</span><button class="add-to-cart" data-name="Mobile Legends 65 💎" data-price="18000">+ Keranjang</button></div>
                        <div class="price-item"><span>74 💎 = 20.300</span><button class="add-to-cart" data-name="Mobile Legends 74 💎" data-price="20300">+ Keranjang</button></div>
                        <div class="price-item"><span>85 💎 = 23.000</span><button class="add-to-cart" data-name="Mobile Legends 85 💎" data-price="23000">+ Keranjang</button></div>
                        <div class="price-item"><span>112 💎 = 31.000</span><button class="add-to-cart" data-name="Mobile Legends 112 💎" data-price="31000">+ Keranjang</button></div>
                        <div class="price-item"><span>172 💎 = 36.000</span><button class="add-to-cart" data-name="Mobile Legends 172 💎" data-price="36000">+ Keranjang</button></div>
                        <div class="price-item"><span>185 💎 = 50.000</span><button class="add-to-cart" data-name="Mobile Legends 185 💎" data-price="50000">+ Keranjang</button></div>
                        <div class="price-item"><span>257 💎 = 55.500</span><button class="add-to-cart" data-name="Mobile Legends 257 💎" data-price="55500">+ Keranjang</button></div>
                        <div class="price-item"><span>284 💎 = 75.000</span><button class="add-to-cart" data-name="Mobile Legends 284 💎" data-price="75000">+ Keranjang</button></div>
                        <div class="price-item"><span>296 💎 = 78.000</span><button class="add-to-cart" data-name="Mobile Legends 296 💎" data-price="78000">+ Keranjang</button></div>
                        <div class="price-item"><span>344 💎 = 92.000</span><button class="add-to-cart" data-name="Mobile Legends 344 💎" data-price="92000">+ Keranjang</button></div>
                        <div class="price-item"><span>370 💎 = 97.000</span><button class="add-to-cart" data-name="Mobile Legends 370 💎" data-price="97000">+ Keranjang</button></div>
                        <div class="price-item"><span>429 💎 = 111.000</span><button class="add-to-cart" data-name="Mobile Legends 429 💎" data-price="111000">+ Keranjang</button></div>
                        <div class="price-item"><span>514 💎 = 135.000</span><button class="add-to-cart" data-name="Mobile Legends 514 💎" data-price="135000">+ Keranjang</button></div>
                        <div class="price-item"><span>568 💎 = 143.000</span><button class="add-to-cart" data-name="Mobile Legends 568 💎" data-price="143000">+ Keranjang</button></div>
                        <div class="price-item"><span>600 💎 = 154.000</span><button class="add-to-cart" data-name="Mobile Legends 600 💎" data-price="154000">+ Keranjang</button></div>
                        <div class="price-item"><span>716 💎 = 184.000</span><button class="add-to-cart" data-name="Mobile Legends 716 💎" data-price="184000">+ Keranjang</button></div>
                        <div class="price-item"><span>792 💎 = 206.000</span><button class="add-to-cart" data-name="Mobile Legends 792 💎" data-price="206000">+ Keranjang</button></div>
                        <div class="price-item"><span>878 💎 = 222.000</span><button class="add-to-cart" data-name="Mobile Legends 878 💎" data-price="222000">+ Keranjang</button></div>
                        <div class="price-item"><span>963 💎 = 242.000</span><button class="add-to-cart" data-name="Mobile Legends 963 💎" data-price="242000">+ Keranjang</button></div>
                        <div class="price-item"><span>1050 💎 = 265.000</span><button class="add-to-cart" data-name="Mobile Legends 1050 💎" data-price="265000">+ Keranjang</button></div>
                    </div>
                </div>

                <!-- Roblox -->
                <div class="product-card" data-category="roblox">
                    <div class="product-header"><h3>Roblox</h3><p>Roblox | Robux 💸</p></div>
                    <div class="product-body">
                        <div class="price-item"><span>100 Robux = 18.000</span><button class="add-to-cart" data-name="Roblox 100 Robux" data-price="18000">+ Keranjang</button></div>
                        <div class="price-item"><span>400 Robux = 77.000</span><button class="add-to-cart" data-name="Roblox 400 Robux" data-price="77000">+ Keranjang</button></div>
                        <div class="price-item"><span>Roblox Gift Card = 102.000</span><button class="add-to-cart" data-name="Roblox Gift Card" data-price="102000">+ Keranjang</button></div>
                        <div class="price-item"><span>Roblox Gift Card = 203.000</span><button class="add-to-cart" data-name="Roblox Gift Card" data-price="203000">+ Keranjang</button></div>
                        <div class="price-item"><span>Roblox Gift Card = 505.000</span><button class="add-to-cart" data-name="Roblox Gift Card" data-price="505000">+ Keranjang</button></div>
                    </div>
                </div>

                <!-- Call of Duty Mobile -->
                <div class="product-card" data-category="cod">
                    <div class="product-header"><h3>Call of Duty Mobile</h3><p>CODM | CP 💎</p></div>
                    <div class="product-body">
                        <div class="price-item"><span>26 CP = 5.500</span><button class="add-to-cart" data-name="COD 26 CP" data-price="5500">+ Keranjang</button></div>
                        <div class="price-item"><span>62 CP = 9.800</span><button class="add-to-cart" data-name="COD 62 CP" data-price="9800">+ Keranjang</button></div>
                        <div class="price-item"><span>127 CP = 18.800</span><button class="add-to-cart" data-name="COD 127 CP" data-price="18800">+ Keranjang</button></div>
                        <div class="price-item"><span>320 CP = 49.000</span><button class="add-to-cart" data-name="COD 320 CP" data-price="49000">+ Keranjang</button></div>
                        <div class="price-item"><span>528 CP = 96.000</span><button class="add-to-cart" data-name="COD 528 CP" data-price="96000">+ Keranjang</button></div>
                        <div class="price-item"><span>1056 CP = 185.000</span><button class="add-to-cart" data-name="COD 1056 CP" data-price="185000">+ Keranjang</button></div>
                        <div class="price-item"><span>1584 CP = 290.000</span><button class="add-to-cart" data-name="COD 1584 CP" data-price="290000">+ Keranjang</button></div>
                    </div>
                </div>

                <!-- PUBG -->
                <div class="product-card" data-category="pubg">
                    <div class="product-header"><h3>PUBG Mobile</h3><p>PUBG | UC 💎</p></div>
                    <div class="product-body">
                        <div class="price-item"><span>52 UC = 16.000</span><button class="add-to-cart" data-name="PUBG 52 UC" data-price="16000">+ Keranjang</button></div>
                        <div class="price-item"><span>62 UC = 18.000</span><button class="add-to-cart" data-name="PUBG 62 UC" data-price="18000">+ Keranjang</button></div>
                        <div class="price-item"><span>263 UC = 74.000</span><button class="add-to-cart" data-name="PUBG 263 UC" data-price="74000">+ Keranjang</button></div>
                        <div class="price-item"><span>500 UC = 112.000</span><button class="add-to-cart" data-name="PUBG 500 UC" data-price="112000">+ Keranjang</button></div>
                        <div class="price-item"><span>700 UC = 164.000</span><button class="add-to-cart" data-name="PUBG 700 UC" data-price="164000">+ Keranjang</button></div>
                        <div class="price-item"><span>788 UC = 193.000</span><button class="add-to-cart" data-name="PUBG 788 UC" data-price="193000">+ Keranjang</button></div>
                        <div class="price-item"><span>1000 UC = 242.000</span><button class="add-to-cart" data-name="PUBG 1000 UC" data-price="242000">+ Keranjang</button></div>
                        <div class="price-item"><span>1100 UC = 250.000</span><button class="add-to-cart" data-name="PUBG 1100 UC" data-price="250000">+ Keranjang</button></div>
                        <div class="price-item"><span>2425 UC = 517.000</span><button class="add-to-cart" data-name="PUBG 2425 UC" data-price="517000">+ Keranjang</button></div>
                        <div class="price-item"><span>2875 UC = 625.000</span><button class="add-to-cart" data-name="PUBG 2875 UC" data-price="625000">+ Keranjang</button></div>
                    </div>
                </div>

                <!-- Sewa Bot WhatsApp -->
                <div class="product-card" data-category="lainnya">
                    <div class="product-header"><h3>Sewa Bot WhatsApp</h3><p>Bot WhatsApp Premium</p></div>
                    <div class="product-body">
                        <div class="price-item"><span>1 bulan = 5.000</span><button class="add-to-cart" data-name="Sewa Bot WA 1 bulan" data-price="5000">+ Keranjang</button></div>
                        <div class="price-item"><span>2 bulan = 10.000</span><button class="add-to-cart" data-name="Sewa Bot WA 2 bulan" data-price="10000">+ Keranjang</button></div>
                        <div class="price-item"><span>3 bulan = 15.000</span><button class="add-to-cart" data-name="Sewa Bot WA 3 bulan" data-price="15000">+ Keranjang</button></div>
                        <div class="price-item"><span>4 bulan = 20.000</span><button class="add-to-cart" data-name="Sewa Bot WA 4 bulan" data-price="20000">+ Keranjang</button></div>
                        <div class="price-item"><span>1 tahun = 25.000</span><button class="add-to-cart" data-name="Sewa Bot WA 1 tahun" data-price="25000">+ Keranjang</button></div>
                    </div>
                </div>

                <!-- Suntik Sosmed -->
                <div class="product-card" data-category="lainnya">
                    <div class="product-header"><h3>Suntik Sosmed</h3><p>Tiktok & Instagram</p></div>
                    <div class="product-body">
                        <h4>Tiktok:</h4>
                        <div class="price-item"><span>500 Like = 1.000</span><button class="add-to-cart" data-name="Suntik Tiktok 500 Like" data-price="1000">+ Keranjang</button></div>
                        <div class="price-item"><span>500 View = 900</span><button class="add-to-cart" data-name="Suntik Tiktok 500 View" data-price="900">+ Keranjang</button></div>
                        <div class="price-item"><span>100 Follow = 3.000</span><button class="add-to-cart" data-name="Suntik Tiktok 100 Follow" data-price="3000">+ Keranjang</button></div>
                        <h4 style="margin-top: 1rem;">Instagram:</h4>
                        <div class="price-item"><span>500 Like = 2.000</span><button class="add-to-cart" data-name="Suntik IG 500 Like" data-price="2000">+ Keranjang</button></div>
                        <div class="price-item"><span>500 View = 1.000</span><button class="add-to-cart" data-name="Suntik IG 500 View" data-price="1000">+ Keranjang</button></div>
                        <div class="price-item"><span>100 Follow = 3.000</span><button class="add-to-cart" data-name="Suntik IG 100 Follow" data-price="3000">+ Keranjang</button></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="about" style="background-color: var(--section-bg);">
        <div class="container">
            <div class="section-title"><h2>Tentang Kami</h2></div>
            <div class="about-content">
                <div class="about-text">
                    <p>Rimuru Store adalah penyedia layanan topup game dan layanan digital terpercaya yang telah beroperasi sejak 2020. Kami berkomitmen untuk memberikan pelayanan terbaik dengan harga kompetitif dan proses yang cepat.</p>
                    <p style="margin-top: 1rem;">Tim kami terdiri dari para gamer berpengalaman yang memahami kebutuhan pelanggan. Kami selalu berusaha memberikan pengalaman berbelanja yang menyenangkan dan memuaskan.</p>
                    <div style="margin-top: 2rem;">
                        <h3>Metode Pembayaran:</h3>
                        <ul style="margin-top: 0.5rem; margin-left: 1.5rem;">
                            <li>Dana: 0831-4042-7092</li>
                            <li>GOPAY: 0831-4042-7092</li>
                            <li>SPAY: 0831-4042-7092</li>
                            <li>OVO: 0831-4042-7092</li>
                            <li>SEABAK: 901428220963</li>
                            <li>QRIS: CHAT ADMIN</li>
                        </ul>
                        <p style="margin-top: 1rem; font-style: italic;">Note: Nominal lain tanyakan admin, no rush, send id - pay - done</p>
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
            <div class="section-title"><h2>Testimoni Pelanggan</h2></div>
            <div class="testimonials">
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Pelanggan 1">
                        <div><h4>Rizky Pratama</h4><p>Pelanggan Free Fire</p></div>
                    </div>
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p>"Prosesnya cepat banget, ga sampe 5 menit diamond langsung masuk. Adminnya ramah dan helpful. Recommended banget!"</p>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Pelanggan 2">
                        <div><h4>Sarah Wijaya</h4><p>Pelanggan Mobile Legends</p></div>
                    </div>
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p>"Pertama kali beli disini dan ga mengecewakan. Harganya murah dibanding tempat lain. Bakal langganan disini terus."</p>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-header">
                        <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Pelanggan 3">
                        <div><h4>Andi Setiawan</h4><p>Pelanggan Sewa Bot WA</p></div>
                    </div>
                    <div class="testimonial-rating"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star-half-alt"></i></div>
                    <p>"Bot WA-nya bekerja dengan baik. Ada kendala sedikit tapi admin langsung bantu selesaikan. Good service!"</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" style="background-color: var(--section-bg);">
        <div class="container">
            <div class="section-title"><h2>Kontak Kami</h2></div>
            <div class="contact-info">
                <div class="contact-card"><i class="fas fa-user"></i><h3>Nama Admin</h3><p>Irwan Ariel</p></div>
                <div class="contact-card"><i class="fas fa-phone-alt"></i><h3>WhatsApp</h3><p><a href="https://wa.me/6283140427092" style="color: var(--primary); text-decoration: none;">0831-4042-7092</a></p></div>
                <div class="contact-card"><i class="fas fa-envelope"></i><h3>Email</h3><p><a href="mailto:irwanaril798@gmail.com" style="color: var(--primary); text-decoration: none;">irwanaril798@gmail.com</a></p></div>
                <div class="contact-card"><i class="fas fa-map-marker-alt"></i><h3>Alamat</h3><p>Riau, Indonesia</p></div>
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
                    <p><i class="fas fa-phone-alt"></i> 0831-4042-7092</p>
                    <p><i class="fas fa-envelope"></i> irwanaril798@gmail.com</p>
                    <div class="social-links">
                        <a href="https://wa.me/6283140427092"><i class="fab fa-whatsapp"></i></a>
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
        
        cartBtn.addEventListener('click', () => cartModal.style.display = 'flex');
        closeCart.addEventListener('click', () => cartModal.style.display = 'none');
        window.addEventListener('click', (e) => { if (e.target === cartModal) cartModal.style.display = 'none'; });
        
        addToCartButtons.forEach(button => {
            button.addEventListener('click', () => {
                const name = button.getAttribute('data-name');
                const price = parseInt(button.getAttribute('data-price'));
                const existing = cart.find(item => item.name === name);
                if (existing) existing.quantity += 1;
                else cart.push({name, price, quantity: 1});
                updateCart();
                showNotification(`${name} ditambahkan ke keranjang`);
            });
        });
        
        function updateCart() {
            cartItems.innerHTML = '';
            let total = 0, itemCount = 0;
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
            
            document.querySelectorAll('.decrease-quantity').forEach(btn => btn.addEventListener('click', e => {
                const i = e.target.getAttribute('data-index');
                if (cart[i].quantity > 1) cart[i].quantity -= 1; else cart.splice(i, 1);
                updateCart();
            }));
            document.querySelectorAll('.increase-quantity').forEach(btn => btn.addEventListener('click', e => {
                const i = e.target.getAttribute('data-index');
                cart[i].quantity += 1;
                updateCart();
            }));
            document.querySelectorAll('.remove-item').forEach(btn => btn.addEventListener('click', e => {
                const i = e.target.closest('button').getAttribute('data-index');
                cart.splice(i, 1);
                updateCart();
            }));
        }
        
        clearCart.addEventListener('click', () => {
            if (cart.length > 0 && confirm('Kosongkan keranjang?')) {
                cart = [];
                updateCart();
                showNotification('Keranjang dikosongkan');
            }
        });
        
        checkoutBtn.addEventListener('click', () => {
            if (cart.length === 0) return alert('Keranjang kosong!');
            let msg = "Halo Rimuru Store, saya ingin memesan:\n\n";
            let total = 0;
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                total += itemTotal;
                msg += `- ${item.name} (${item.quantity}x) = Rp ${itemTotal.toLocaleString('id-ID')}\n`;
            });
            msg += `\nTotal: Rp ${total.toLocaleString('id-ID')}\n\nApakah produk tersedia?`;
            window.open(`https://wa.me/6283140427092?text=${encodeURIComponent(msg)}`, '_blank');
        });
        
        function showNotification(message) {
            const n = document.createElement('div');
            n.style.cssText = `position:fixed;top:20px;right:20px;background:var(--primary);color:white;padding:1rem 1.5rem;border-radius:4px;box-shadow:0 4px 12px rgba(0,0,0,0.2);z-index:1000;transform:translateX(100%);transition:transform 0.3s ease;`;
            n.textContent = message;
            document.body.appendChild(n);
            setTimeout(() => n.style.transform = 'translateX(0)', 100);
            setTimeout(() => { n.style.transform = 'translateX(100%)'; setTimeout(() => n.remove(), 300); }, 3000);
        }
        
        // Search & Filter
        const searchInput = document.getElementById('searchInput');
        const categoryButtons = document.querySelectorAll('.category-btn');
        const productCards = document.querySelectorAll('.product-card');
        
        searchInput.addEventListener('input', () => {
            const term = searchInput.value.toLowerCase();
            productCards.forEach(card => {
                const h3 = card.querySelector('.product-header h3').textContent.toLowerCase();
                const p = card.querySelector('.product-header p').textContent.toLowerCase();
                card.style.display = (h3.includes(term) || p.includes(term)) ? 'block' : 'none';
            });
        });
        
        categoryButtons.forEach(btn => {
            btn.addEventListener('click', () => {
                categoryButtons.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
                const cat = btn.dataset.category;
                productCards.forEach(card => {
                    card.style.display = (cat === 'all' || card.dataset.category === cat) ? 'block' : 'none';
                });
            });
        });
        
        // Music toggle
        const musicToggle = document.getElementById('musicToggle');
        const bgMusic = document.getElementById('bgMusic');
        let isPlaying = false;
        musicToggle.addEventListener('click', () => {
            if (isPlaying) { bgMusic.pause(); musicToggle.innerHTML = '<i class="fas fa-music"></i>'; }
            else { bgMusic.play(); musicToggle.innerHTML = '<i class="fas fa-pause"></i>'; }
            isPlaying = !isPlaying;
        });
        
        // Video Controls
        const backgroundVideo = document.getElementById('backgroundVideo');
        const playPauseVideoBtn = document.getElementById('playPauseVideo');
        const muteUnmuteVideoBtn = document.getElementById('muteUnmuteVideo');
        
        playPauseVideoBtn.addEventListener('click', () => {
            if (backgroundVideo.paused) {
                backgroundVideo.play();
                playPauseVideoBtn.querySelector('i').classList.replace('fa-play', 'fa-pause');
            } else {
                backgroundVideo.pause();
                playPauseVideoBtn.querySelector('i').classList.replace('fa-pause', 'fa-play');
            }
        });
        
        muteUnmuteVideoBtn.addEventListener('click', () => {
            backgroundVideo.muted = !backgroundVideo.muted;
            const icon = muteUnmuteVideoBtn.querySelector('i');
            if (backgroundVideo.muted) icon.classList.replace('fa-volume-up', 'fa-volume-mute');
            else icon.classList.replace('fa-volume-mute', 'fa-volume-up');
        });
        
        // Dark Mode
        const themeToggle = document.getElementById('themeToggle');
        const body = document.body;
        const currentTheme = localStorage.getItem('theme');
        if (currentTheme) { body.classList.add(currentTheme); updateThemeIcon(currentTheme); }
        themeToggle.addEventListener('click', () => {
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
            themeToggle.innerHTML = theme === 'dark-mode' ? '<i class="fas fa-sun"></i>' : '<i class="fas fa-moon"></i>';
        }
        
        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', e => {
                e.preventDefault();
                document.querySelector(anchor.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
            });
        });
        
        // Loading video
        const loading = document.getElementById('loading');
        backgroundVideo.addEventListener('loadstart', () => loading.style.display = 'flex');
        backgroundVideo.addEventListener('canplay', () => loading.style.display = 'none');
    </script>
</body>
</html>
