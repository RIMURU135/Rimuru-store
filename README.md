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
        <div class="cart-actions"><button class="btn-clear" id="clearCart">Kosongkan</button><button class="btn-checkout" id="checkoutBtn"><i class="fab fa-whatsa
