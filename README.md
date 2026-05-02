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
            --header-bg: #0f0b1a;
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
            --header-bg: #ffffff;
            --footer-bg: #ede7f6;
            --section-bg: #f3e5f5;
            --border-light: #d1c4e9;
            --shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
            --neon-glow: 0 0 12px rgba(106, 27, 154, 0.3);
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
            color: var(--text-color);
            padding: 0.8rem 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            border-bottom: 2px solid var(--accent);
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.4);
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
            display: flex;
            align-items: center;
            gap: 0.4rem;
            font-size: 0.9rem;
            background: transparent;
            border: 1.5px solid transparent;
        }

        nav ul li a:hover {
            background: rgba(155, 48, 249, 0.15);
            border-color: var(--accent);
            color: #fff;
            box-shadow: 0 0 10px rgba(255, 94, 156, 0.3);
        }

        #darkModeToggle {
            background: var(--card-bg);
            border: 1.5px solid var(--border-light);
            color: var(--text-color);
            font-size: 1.1rem;
            cursor: pointer;
            padding: 0.5rem 0.9rem;
            border-radius: 50%;
            margin-left: 0.3rem;
        }

        #darkModeToggle:hover {
            background: var(--accent);
            color: #fff;
            border-color: var(--accent);
        }

        .hero {
            background: linear-gradient(135deg, #1a0a2e 0%, #0d0b1a 60%, #1a0a2e 100%);
            padding: 7rem 0 4rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 2px solid var(--accent);
        }

        .light-mode .hero {
            background: linear-gradient(135deg, #e8def8 0%, #f5f0fa 60%, #e8def8 100%);
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at 30% 50%, rgba(155, 48, 249, 0.08) 0%, transparent 60%);
            animation: rotateGlow 20s linear infinite;
            pointer-events: none;
        }

        @keyframes rotateGlow {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }

        .hero h2 {
            font-family: var(--font-display);
            font-size: 2.8rem;
            margin-bottom: 1rem;
            background: linear-gradient(to right, #e9d5ff, #fbcfe8, #c084fc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            position: relative;
            z-index: 1;
        }

        .hero p {
            font-size: 1.2rem;
            opacity: 0.85;
            max-width: 650px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        .btn-cta {
            display: inline-block;
            margin-top: 2rem;
            background: var(--accent);
            color: #fff;
            font-weight: 800;
            padding: 0.9rem 2.5rem;
            border-radius: 40px;
            text-decoration: none;
            font-size: 1.1rem;
            letter-spacing: 0.5px;
            box-shadow: 0 0 25px rgba(255, 94, 156, 0.5);
            position: relative;
            z-index: 1;
            border: none;
            cursor: pointer;
        }

        .btn-cta:hover {
            background: var(--accent-dark);
            box-shadow: 0 0 35px rgba(255, 94, 156, 0.7);
            transform: translateY(-2px);
        }

        section {
            padding: 3.5rem 0;
        }

        .section-title {
            font-family: var(--font-display);
            text-align: center;
            font-size: 2rem;
            margin-bottom: 2.5rem;
            color: var(--text-color);
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 70px;
            height: 3px;
            background: var(--accent);
            margin: 0.6rem auto 0;
            border-radius: 4px;
            box-shadow: 0 0 12px var(--accent);
        }

        .game-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(170px, 1fr));
            gap: 1.8rem;
        }

        .game-card {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 1.5rem 1rem;
            text-align: center;
            cursor: pointer;
            border: 2px solid var(--border-light);
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .game-card:hover {
            border-color: var(--accent);
            box-shadow: var(--neon-glow);
            transform: translateY(-6px);
        }

        .game-card img {
            width: 80px;
            height: 80px;
            object-fit: contain;
            margin-bottom: 0.8rem;
            border-radius: 16px;
            background: rgba(255, 255, 255, 0.04);
            padding: 8px;
        }

        .game-card h3 {
            font-weight: 700;
            font-size: 1rem;
            color: var(--text-color);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            gap: 1.5rem;
        }

        .product-card {
            background: var(--card-bg);
            border-radius: 18px;
            padding: 1.4rem;
            border: 1.5px solid var(--border-light);
            box-shadow: var(--shadow);
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }

        .product-card h4 {
            font-size: 1.1rem;
            color: var(--accent);
            font-weight: 700;
        }

        .product-card .price {
            font-size: 1.5rem;
            font-weight: 800;
            color: var(--text-color);
        }

        .btn-buy {
            background: var(--primary);
            color: #fff;
            border: none;
            border-radius: 30px;
            padding: 0.6rem 1.2rem;
            font-weight: 700;
            cursor: pointer;
            letter-spacing: 0.4px;
            box-shadow: 0 0 14px rgba(155, 48, 249, 0.4);
            margin-top: auto;
        }

        .btn-buy:hover {
            background: var(--primary-dark);
            box-shadow: 0 0 22px rgba(155, 48, 249, 0.7);
        }

        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            backdrop-filter: blur(6px);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 2000;
            padding: 1rem;
        }

        .modal {
            background: var(--card-bg);
            border-radius: 24px;
            max-width: 480px;
            width: 100%;
            padding: 2rem;
            border: 2px solid var(--accent);
            box-shadow: 0 0 40px rgba(255, 94, 156, 0.3);
            color: var(--text-color);
        }

        .modal h3 {
            font-family: var(--font-display);
            margin-bottom: 1.2rem;
            font-size: 1.5rem;
            text-align: center;
        }

        .modal input,
        .modal select {
            width: 100%;
            padding: 0.8rem 1rem;
            border-radius: 30px;
            border: 1.5px solid var(--border-light);
            background: var(--bg-color);
            color: var(--text-color);
            font-weight: 500;
            margin-bottom: 1rem;
            outline: none;
        }

        .modal input:focus,
        .modal select:focus {
            border-color: var(--accent);
            box-shadow: 0 0 10px var(--accent);
        }

        .payment-methods {
            display: flex;
            flex-wrap: wrap;
            gap: 0.7rem;
            margin: 0.8rem 0 1.2rem;
        }

        .payment-btn {
            flex: 1 1 auto;
            min-width: 80px;
            background: var(--bg-color);
            border: 1.5px solid var(--border-light);
            border-radius: 30px;
            padding: 0.65rem 0.8rem;
            font-weight: 700;
            cursor: pointer;
            color: var(--text-color);
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.4rem;
            font-size: 0.85rem;
        }

        .payment-btn.active {
            background: var(--accent);
            color: #fff;
            border-color: var(--accent);
            box-shadow: 0 0 15px var(--accent);
        }

        .modal .btn-confirm {
            background: var(--accent);
            color: #fff;
            font-weight: 800;
            padding: 0.8rem;
            border-radius: 30px;
            border: none;
            width: 100%;
            cursor: pointer;
            font-size: 1rem;
            margin-top: 0.6rem;
            box-shadow: 0 0 18px rgba(255, 94, 156, 0.4);
        }

        .btn-close-modal {
            background: transparent;
            border: 1px solid var(--border-light);
            color: var(--text-color);
            padding: 0.5rem 1.2rem;
            border-radius: 30px;
            cursor: pointer;
            margin-top: 0.6rem;
            width: 100%;
        }

        .qris-container {
            display: none;
            text-align: center;
            margin: 1rem 0;
            padding: 1rem;
            background: #fff;
            border-radius: 16px;
            border: 2px solid var(--accent);
        }
        .qris-container.active {
            display: block;
        }
        .qris-container img {
            max-width: 220px;
            height: auto;
            border-radius: 12px;
        }
        .qris-container p {
            margin-top: 0.5rem;
            font-weight: 700;
            color: #1a0a2e;
            font-size: 0.9rem;
        }

        footer {
            background: var(--footer-bg);
            padding: 2rem 0;
            text-align: center;
            border-top: 2px solid var(--accent);
            color: var(--text-color);
            font-size: 0.9rem;
        }

        .hidden {
            display: none !important;
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 0.5rem;
            }
            nav ul {
                justify-content: center;
            }
            .hero h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <div class="logo">
                <img src="https://i.imgur.com/8hVqK4y.png" alt="Rimuru Logo" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22%3E%3Ccircle cx=%2250%22 cy=%2250%22 r=%2245%22 fill=%22%239b30f9%22/%3E%3Ctext x=%2250%22 y=%2255%22 text-anchor=%22middle%22 fill=%22white%22 font-size=%2222%22 font-weight=%22bold%22%3ER%3C/text%3E%3C/svg%3E';">
                <h1>Rimuru Store</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home"><i class="fas fa-home"></i> Beranda</a></li>
                    <li><a href="#games"><i class="fas fa-gamepad"></i> Game</a></li>
                    <li><a href="#products"><i class="fas fa-cubes"></i> Produk</a></li>
                    <li><button id="darkModeToggle"><i class="fas fa-moon"></i></button></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <h2>Topup Game & Layanan Digital</h2>
            <p>Cepat, murah, dan terpercaya sejak 2024. Dapatkan diamond, voucher, dan layanan digital favoritmu dalam hitungan detik.</p>
            <button class="btn-cta" onclick="document.getElementById('games').scrollIntoView({behavior:'smooth'})">
                <i class="fas fa-bolt"></i> Mulai Topup Sekarang
            </button>
        </div>
    </section>

    <section id="games">
        <div class="container">
            <h2 class="section-title">🎮 Pilih Game</h2>
            <div class="game-grid" id="gameGrid">
                <!-- Game cards rendered by JS -->
            </div>
        </div>
    </section>

    <section id="products">
        <div class="container">
            <h2 class="section-title" id="productSectionTitle">📦 Pilih Nominal Topup</h2>
            <div class="products-grid" id="productsContainer">
                <p style="text-align:center;grid-column:1/-1;opacity:0.7;">Silakan pilih game terlebih dahulu.</p>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Rimuru Store. Seluruh transaksi aman & terenkripsi.</p>
            <p style="margin-top:0.4rem;"><i class="fab fa-whatsapp"></i> CS: 0812-3456-7890 | <i class="fab fa-instagram"></i> @rimurustore</p>
        </div>
    </footer>

    <!-- Modal Order -->
    <div class="modal-overlay hidden" id="orderModal">
        <div class="modal">
            <h3>🧾 Konfirmasi Pesanan</h3>
            <div style="margin-bottom:0.8rem;">
                <strong id="orderGameName">-</strong>
            </div>
            <div style="margin-bottom:0.8rem;">
                <span id="orderProductName">-</span> · <strong id="orderPrice">Rp 0</strong>
            </div>
            <input type="text" id="playerId" placeholder="Masukkan ID / Server (contoh: 12345678 (1200))" required>
            <label style="font-weight:600;display:block;margin-bottom:0.3rem;">Metode Pembayaran:</label>
            <div class="payment-methods" id="paymentMethods">
                <button class="payment-btn active" data-method="dana"><i class="fas fa-wallet"></i> DANA</button>
                <button class="payment-btn" data-method="gopay"><i class="fas fa-mobile-alt"></i> GoPay</button>
                <button class="payment-btn" data-method="ovo"><i class="fas fa-credit-card"></i> OVO</button>
                <button class="payment-btn" data-method="qris"><i class="fas fa-qrcode"></i> QRIS</button>
            </div>
            <div class="qris-container" id="qrisContainer">
                <img src="https://www.image2url.com/r2/default/files/1777684205267-2fa2694c-ba5a-4e46-8a96-f17da2fb7fa2.png"
                alt="QRIS Code" onerror="this.style.display='none'; this.nextElementSibling.style.display='block';">
                <p style="display:none;">⚠️ Gambar QRIS gagal dimuat. Silakan refresh halaman.</p>
                <p><i class="fas fa-camera"></i> Scan QR Code di atas melalui aplikasi e-wallet / mobile banking kamu</p>
                <p style="font-size:0.8rem;color:#555;">Total: <strong id="qrisAmount">Rp 0</strong></p>
            </div>
            <button class="btn-confirm" id="btnConfirmOrder"><i class="fas fa-check-circle"></i> Bayar Sekarang</button>
            <button class="btn-close-modal" id="btnCloseModal">Batal</button>
        </div>
    </div>

    <script>
        (function() {
            // --- DATA GAME & PRODUK ---
            const gameData = [{
                id: 'mlbb',
                name: 'Mobile Legends',
                icon: 'https://i.imgur.com/YWDUh1C.png',
                products: [
                    { id: 'mlbb1', name: '86 Diamonds', price: 28000 },
                    { id: 'mlbb2', name: '172 Diamonds', price: 55000 },
                    { id: 'mlbb3', name: '344 Diamonds', price: 105000 },
                    { id: 'mlbb4', name: '706 Diamonds', price: 210000 },
                ]
            }, {
                id: 'ff',
                name: 'Free Fire',
                icon: 'https://i.imgur.com/4oNS5lA.png',
                products: [
                    { id: 'ff1', name: '70 Diamonds', price: 10000 },
                    { id: 'ff2', name: '140 Diamonds', price: 20000 },
                    { id: 'ff3', name: '355 Diamonds', price: 50000 },
                    { id: 'ff4', name: '720 Diamonds', price: 98000 },
                ]
            }, {
                id: 'pubg',
                name: 'PUBG Mobile',
                icon: 'https://i.imgur.com/L3Yq9tM.png',
                products: [
                    { id: 'pubg1', name: '60 UC', price: 15000 },
                    { id: 'pubg2', name: '180 UC', price: 45000 },
                    { id: 'pubg3', name: '600 UC', price: 140000 },
                ]
            }];

            // --- STATE ---
            let selectedGame = null;
            let selectedProduct = null;
            let selectedPayment = 'dana';
            let darkMode = localStorage.getItem('rimuruDarkMode') === 'true';

            // --- DOM REFS ---
            const gameGrid = document.getElementById('gameGrid');
            const productsContainer = document.getElementById('productsContainer');
            const productSectionTitle = document.getElementById('productSectionTitle');
            const orderModal = document.getElementById('orderModal');
            const orderGameName = document.getElementById('orderGameName');
            const orderProductName = document.getElementById('orderProductName');
            const orderPrice = document.getElementById('orderPrice');
            const playerIdInput = document.getElementById('playerId');
            const paymentBtns = document.querySelectorAll('.payment-btn');
            const btnConfirm = document.getElementById('btnConfirmOrder');
            const btnCloseModal = document.getElementById('btnCloseModal');
            const darkModeToggle = document.getElementById('darkModeToggle');
            const qrisContainer = document.getElementById('qrisContainer');
            const qrisAmount = document.getElementById('qrisAmount');

            // --- FUNCTIONS ---
            function applyDarkMode() {
                document.body.classList.toggle('light-mode', !darkMode);
                const icon = darkModeToggle.querySelector('i');
                if (darkMode) {
                    icon.className = 'fas fa-sun';
                } else {
                    icon.className = 'fas fa-moon';
                }
                localStorage.setItem('rimuruDarkMode', darkMode);
            }

            function renderGameGrid() {
                gameGrid.innerHTML = gameData.map(game => `
                    <div class="game-card" data-game-id="${game.id}">
                        <img src="${game.icon}" alt="${game.name}" loading="lazy" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 80 80%22%3E%3Crect width=%2280%22 height=%2280%22 rx=%2216%22 fill=%22%233a2a50%22/%3E%3Ctext x=%2240%22 y=%2245%22 text-anchor=%22middle%22 fill=%22white%22 font-size=%2212%22%3E${game.name.substring(0,4)}%3C/text%3E%3C/svg%3E';">
                        <h3>${game.name}</h3>
                    </div>
                `).join('');

                document.querySelectorAll('.game-card').forEach(card => {
                    card.addEventListener('click', () => {
                        const gameId = card.dataset.gameId;
                        selectedGame = gameData.find(g => g.id === gameId);
                        selectedProduct = null;
                        renderProducts(selectedGame);
                        productSectionTitle.textContent = `📦 ${selectedGame.name} - Pilih Nominal`;
                        document.getElementById('products').scrollIntoView({ behavior: 'smooth' });
                    });
                });
            }

            function renderProducts(game) {
                if (!game) {
                    productsContainer.innerHTML =
                        '<p style="text-align:center;grid-column:1/-1;opacity:0.7;">Silakan pilih game terlebih dahulu.</p>';
                    return;
                }
                productsContainer.innerHTML = game.products.map(prod => `
                    <div class="product-card" data-product-id="${prod.id}">
                        <h4>${prod.name}</h4>
                        <div class="price">Rp ${prod.price.toLocaleString('id-ID')}</div>
                        <button class="btn-buy" data-product-id="${prod.id}">Beli Sekarang</button>
                    </div>
                `).join('');

                document.querySelectorAll('.btn-buy').forEach(btn => {
                    btn.addEventListener('click', (e) => {
                        const prodId = btn.dataset.productId;
                        selectedProduct = game.products.find(p => p.id === prodId);
                        openOrderModal();
                    });
                });
            }

            function openOrderModal() {
                if (!selectedGame || !selectedProduct) return;
                orderGameName.textContent = `🎮 ${selectedGame.name}`;
                orderProductName.textContent = selectedProduct.name;
                orderPrice.textContent = `Rp ${selectedProduct.price.toLocaleString('id-ID')}`;
                playerIdInput.value = '';
                // reset payment ke dana & tampilkan QRIS hanya jika QRIS aktif
                setPaymentMethod('dana');
                orderModal.classList.remove('hidden');
            }

            function closeOrderModal() {
                orderModal.classList.add('hidden');
                qrisContainer.classList.remove('active');
            }

            function setPaymentMethod(method) {
                selectedPayment = method;
                paymentBtns.forEach(btn => {
                    const isActive = btn.dataset.method === method;
                    btn.classList.toggle('active', isActive);
                });
                // Tampilkan QRIS container hanya jika metode qris dipilih
                if (method === 'qris') {
                    qrisContainer.classList.add('active');
                    if (selectedProduct) {
                        qrisAmount.textContent = `Rp ${selectedProduct.price.toLocaleString('id-ID')}`;
                    }
                } else {
                    qrisContainer.classList.remove('active');
                }
            }

            function processPayment() {
                const playerId = playerIdInput.value.trim();
                if (!playerId) {
                    alert('⚠️ Harap masukkan ID / Server kamu terlebih dahulu.');
                    return;
                }
                if (!selectedProduct) {
                    alert('Produk tidak ditemukan.');
                    return;
                }

                // Jika QRIS dipilih, pastikan QRIS container sudah aktif (sudah)
                const methodNames = { dana: 'DANA', gopay: 'GoPay', ovo: 'OVO', qris: 'QRIS' };
                const methodDisplay = methodNames[selectedPayment] || selectedPayment.toUpperCase();

                if (selectedPayment === 'qris') {
                    alert(
                        `✅ Pesanan berhasil dibuat!\n\nGame: ${selectedGame.name}\nProduk: ${selectedProduct.name}\nHarga: Rp ${selectedProduct.price.toLocaleString('id-ID')}\nID: ${playerId}\nMetode: QRIS\n\nSilakan scan QR Code yang muncul untuk menyelesaikan pembayaran. Setelah pembayaran berhasil, saldo akan otomatis masuk.`
                        );
                } else {
                    alert(
                        `✅ Pesanan berhasil dibuat!\n\nGame: ${selectedGame.name}\nProduk: ${selectedProduct.name}\nHarga: Rp ${selectedProduct.price.toLocaleString('id-ID')}\nID: ${playerId}\nMetode: ${methodDisplay}\n\nSilakan lanjutkan pembayaran melalui aplikasi ${methodDisplay}.`
                        );
                }
                closeOrderModal();
            }

            // --- EVENT LISTENERS ---
            paymentBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    setPaymentMethod(btn.dataset.method);
                });
            });

            btnConfirm.addEventListener('click', processPayment);
            btnCloseModal.addEventListener('click', closeOrderModal);
            orderModal.addEventListener('click', (e) => {
                if (e.target === orderModal) closeOrderModal();
            });

            darkModeToggle.addEventListener('click', () => {
                darkMode = !darkMode;
                applyDarkMode();
            });

            // --- INIT ---
            applyDarkMode();
            renderGameGrid();
            renderProducts(null);

            // Set default payment tampilan
            setPaymentMethod('dana');
        })();
    </script>
</body>
</html>
