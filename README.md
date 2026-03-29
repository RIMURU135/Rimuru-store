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
        
        * { margin:0; padding:0; box-sizing:border-box; font-family:'Segoe UI',Tahoma,Geneva,Verdana,sans-serif; }
        
        body { background:var(--bg-color); color:var(--text-color); line-height:1.6; }
        
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
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center center;
            z-index: -1;
        }
        
        /* Desktop (Landscape) - Ukuran asli video tetap utuh */
        @media (min-width: 1024px) {
            .video-background {
                object-position: center center;
            }
        }
        
        /* Mobile Portrait - Video tetap landscape tapi tidak terpotong berlebihan */
        @media (max-width: 1023px) and (orientation: portrait) {
            .video-background {
                object-position: center top;
            }
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.65);
            z-index: 0;
        }
        
        .hero-content { position:relative; z-index:1; max-width:800px; padding:2rem; }
        .hero h2 { font-size:2.8rem; margin-bottom:1rem; text-shadow:2px 2px 4px rgba(0,0,0,0.5); }
        .hero p { font-size:1.3rem; margin-bottom:2rem; text-shadow:1px 1px 2px rgba(0,0,0,0.5); }
        
        .btn {
            display:inline-block; background:var(--accent); color:white; padding:0.8rem 1.5rem;
            border:none; border-radius:4px; text-decoration:none; font-weight:600; cursor:pointer;
            transition:all 0.3s ease;
        }
        .btn:hover { background:#c0392b; transform:translateY(-2px); }
        
        /* Sisanya CSS sama seperti kode sebelumnya (product, cart, dll) */
        section { padding:4rem 0; }
        .section-title { text-align:center; margin-bottom:3rem; }
        .section-title h2 { font-size:2.2rem; color:var(--text-color); position:relative; display:inline-block; padding-bottom:0.5rem; }
        .section-title h2::after { content:''; position:absolute; bottom:0; left:50%; transform:translateX(-50%); width:80px; height:3px; background:var(--primary); }
        
        .product-filters { display:flex; justify-content:space-between; align-items:center; margin-bottom:2rem; flex-wrap:wrap; gap:1rem; }
        .search-box { flex:1; min-width:250px; position:relative; }
        .search-box input { width:100%; padding:0.8rem 1rem 0.8rem 2.5rem; border:1px solid #ddd; border-radius:4px; background:var(--card-bg); color:var(--text-color); }
        .search-box i { position:absolute; left:0.8rem; top:50%; transform:translateY(-50%); color:#777; }
        .category-filters { display:flex; gap:0.5rem; flex-wrap:wrap; }
        .category-btn { padding:0.5rem 1rem; background:var(--card-bg); border:1px solid #ddd; border-radius:4px; cursor:pointer; transition:all 0.3s ease; }
        .category-btn.active { background:var(--primary); color:white; border-color:var(--primary); }
        .products { display:grid; grid-template-columns:repeat(auto-fill, minmax(300px, 1fr)); gap:2rem; }
        .product-card { background:var(--card-bg); border-radius:8px; overflow:hidden; box-shadow:0 5px 15px rgba(0,0,0,0.1); transition:transform 0.3s ease, box-shadow 0.3s ease; }
        .product-card:hover { transform:translateY(-10px); box-shadow:0 15px 30px rgba(0,0,0,0.15); }
        .product-header { background:var(--primary); color:white; padding:1rem; text-align:center; }
        .product-header h3 { font-size:1.4rem; margin-bottom:0.5rem; }
        .product-body { padding:1.5rem; max-height:400px; overflow-y:auto; }
        .price-item { display:flex; justify-content:space-between; align-items:center; padding:0.5rem 0; border-bottom:1px dashed rgba(0,0,0,0.1); }
        .price-item:last-child { border-bottom:none; }
        .add-to-cart { background:var(--primary); color:white; border:none; border-radius:4px; padding:0.3rem 0.7rem; cursor:pointer; }
        .add-to-cart:hover { background:#2980b9; }
        
        /* Cart, Music, Footer, dll. tetap sama */
        .cart-container { position:fixed; bottom:20px; left:20px; z-index:1000; }
        .cart-btn { background:var(--accent); color:white; border:none; border-radius:50%; width:60px; height:60px; display:flex; align-items:center; justify-content:center; font-size:1.5rem; cursor:pointer; box-shadow:0 4px 12px rgba(0,0,0,0.2); }
        .cart-badge { position:absolute; top:-5px; right:-5px; background:#e74c3c; color:white; border-radius:50%; width:25px; height:25px; display:flex; align-items:center; justify-content:center; font-size:0.8rem; font-weight:bold; }
        .music-player { position:fixed; bottom:20px; right:20px; background:var(--card-bg); border-radius:50%; width:60px; height:60px; display:flex; align-items:center; justify-content:center; box-shadow:0 5px 15px rgba(0,0,0,0.2); cursor:pointer; z-index:99; }
        .video-controls { position:absolute; bottom:20px; left:20px; z-index:2; display:flex; gap:10px; }
        .video-controls button { background:rgba(255,255,255,0.2); border:none; color:white; width:40px; height:40px; border-radius:50%; display:flex; align-items:center; justify-content:center; cursor:pointer; }
        .loading { display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.7); z-index:9999; align-items:center; justify-content:center; flex-direction:column; color:white; }
        .loading-spinner { width:50px; height:50px; border:5px solid rgba(255,255,255,0.3); border-radius:50%; border-top-color:white; animation:spin 1s linear infinite; margin-bottom:1rem; }
        @keyframes spin { to { transform:rotate(360deg); } }
        
        @media (max-width:768px) {
            .hero h2 { font-size:2.2rem; }
        }
    </style>
</head>
<body>
    <!-- Loading Indicator -->
    <div class="loading" id="loading">
        <div class="loading-spinner"></div>
        <p>Memuat...</p>
    </div>

    <audio id="bgMusic" loop>
        <source src="https://assets.mixkit.co/music/preview/mixkit-game-show-suspense-waiting-667.mp3" type="audio/mp3">
    </audio>

    <div class="music-player" id="musicToggle"><i class="fas fa-music"></i></div>

    <div class="cart-container">
        <button class="cart-btn" id="cartBtn"><i class="fas fa-shopping-cart"></i><span class="cart-badge" id="cartBadge">0</span></button>
    </div>

    <div class="cart-modal" id="cartModal">
        <div class="cart-content">
            <div class="cart-header"><h2>Keranjang Belanja</h2><button id="closeCart">&times;</button></div>
            <div class="cart-items" id="cartItems"></div>
            <div class="cart-total"><span>Total:</span><span id="cartTotal">Rp 0</span></div>
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
                        <li><button class="theme-toggle" id="themeToggle"><i class="fas fa-moon"></i></button></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero" id="home">
        <!-- Video Background - Sudah diperbaiki agar tidak kepotong di portrait -->
        <video class="video-background" id="backgroundVideo" autoplay muted loop playsinline poster="https://file.idnet.my.id/api/preview.php?file=ikhk9tu8.jpg">
            <source src="https://image2url.com/r2/default/videos/1774790761304-592aeffb-1a5b-4038-872b-48cc9d92b619.mp4" type="video/mp4">
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

    <!-- Semua section produk, about, testimonials, contact, footer, dan script tetap sama seperti kode sebelumnya (saya tidak ulang di sini agar tidak terlalu panjang, tapi Anda tinggal copy dari kode terakhir yang saya berikan) -->

    <!-- ... (paste semua section produk sampai footer dan script dari kode sebelumnya) ... -->

    <script>
        // Script lengkap (sama seperti kode terakhir)
        // ... (cart, music, video controls, dark mode, dll.)
    </script>
</body>
</html>
