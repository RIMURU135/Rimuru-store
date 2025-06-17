<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rimuru Store - Game Topup Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #00b4d8;
            --secondary: #90e0ef;
            --accent: #ff9e00;
            --dark: #03045e;
            --ff-color: #f5a623;
            --ml-color: #ff2d55;
            --roblox-color: #e7325a;
            --cod-color: #5cb3ff;
            --pubg-color: #ffcc00;
            --bot-color: #25d366;
            --sosmed-color: #c13584;
        }
        
        body {
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
            color: white;
            overflow-x: hidden;
            background-color: #000;
        }
        
        #video-background {
            position: fixed;
            right: 0;
            bottom: 0;
            min-width: 100%;
            min-height: 100%;
            z-index: -1;
            filter: brightness(0.3);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 30px;
            background-color: rgba(0, 0, 0, 0.7);
            border-radius: 20px;
            margin-top: 40px;
            margin-bottom: 50px;
            box-shadow: 0 0 40px rgba(0, 180, 216, 0.6);
            border: 2px solid var(--primary);
            backdrop-filter: blur(10px);
            animation: glow 4s infinite alternate;
        }
        
        @keyframes glow {
            0% {
                box-shadow: 0 0 30px rgba(0, 180, 216, 0.6);
                border-color: var(--primary);
            }
            50% {
                box-shadow: 0 0 40px rgba(144, 224, 239, 0.8);
                border-color: var(--secondary);
            }
            100% {
                box-shadow: 0 0 30px rgba(255, 158, 0, 0.6);
                border-color: var(--accent);
            }
        }
        
        header {
            text-align: center;
            margin-bottom: 40px;
            padding: 40px 20px;
            background: linear-gradient(90deg, rgba(0,0,0,0) 0%, rgba(0,180,216,0.2) 50%, rgba(0,0,0,0) 100%);
            border-radius: 15px;
            position: relative;
            overflow: hidden;
        }
        
        header::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 25%;
            width: 50%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
        }
        
        h1 {
            font-size: 4.5em;
            margin: 15px 0;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(0, 180, 216, 0.3);
            font-weight: 800;
            letter-spacing: 3px;
        }
        
        .subtitle {
            font-size: 1.8em;
            margin-bottom: 10px;
            color: var(--secondary);
            font-weight: 300;
        }
        
        .game-tabs {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }
        
        .tab-btn {
            padding: 12px 25px;
            background: rgba(3, 4, 94, 0.5);
            border: 2px solid var(--primary);
            color: white;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
            font-size: 1.1em;
            position: relative;
            overflow: hidden;
        }
        
        .tab-btn::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                transparent,
                rgba(0, 180, 216, 0.2),
                transparent
            );
            transform: rotate(45deg);
            transition: all 0.5s ease;
        }
        
        .tab-btn.active {
            transform: translateY(-5px);
            box-shadow: 0 0 20px rgba(0, 180, 216, 0.5);
            border-color: var(--secondary);
        }
        
        .tab-btn:hover {
            background: rgba(0, 150, 199, 0.5);
        }
        
        .tab-btn:hover::before {
            left: 100%;
        }
        
        /* Game-specific tab colors */
        .tab-btn.ff {
            border-color: var(--ff-color);
        }
        .tab-btn.ff.active {
            background: linear-gradient(45deg, var(--ff-color), var(--dark));
            box-shadow: 0 0 20px rgba(245, 166, 35, 0.5);
        }
        
        .tab-btn.ml {
            border-color: var(--ml-color);
        }
        .tab-btn.ml.active {
            background: linear-gradient(45deg, var(--ml-color), var(--dark));
            box-shadow: 0 0 20px rgba(255, 45, 85, 0.5);
        }
        
        .tab-btn.roblox {
            border-color: var(--roblox-color);
        }
        .tab-btn.roblox.active {
            background: linear-gradient(45deg, var(--roblox-color), var(--dark));
            box-shadow: 0 0 20px rgba(231, 50, 90, 0.5);
        }
        
        .tab-btn.cod {
            border-color: var(--cod-color);
        }
        .tab-btn.cod.active {
            background: linear-gradient(45deg, var(--cod-color), var(--dark));
            box-shadow: 0 0 20px rgba(92, 179, 255, 0.5);
        }
        
        .tab-btn.pubg {
            border-color: var(--pubg-color);
        }
        .tab-btn.pubg.active {
            background: linear-gradient(45deg, var(--pubg-color), var(--dark));
            box-shadow: 0 0 20px rgba(255, 204, 0, 0.5);
        }
        
        .tab-btn.bot {
            border-color: var(--bot-color);
        }
        .tab-btn.bot.active {
            background: linear-gradient(45deg, var(--bot-color), var(--dark));
            box-shadow: 0 0 20px rgba(37, 211, 102, 0.5);
        }
        
        .tab-btn.sosmed {
            border-color: var(--sosmed-color);
        }
        .tab-btn.sosmed.active {
            background: linear-gradient(45deg, var(--sosmed-color), var(--dark));
            box-shadow: 0 0 20px rgba(193, 53, 132, 0.5);
        }
        
        .game-section {
            display: none;
            margin-bottom: 40px;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .game-section.active {
            display: block;
        }
        
        .game-title {
            font-size: 2.5em;
            margin-bottom: 25px;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
        }
        
        .game-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 35%;
            width: 30%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
        }
        
        .game-subtitle {
            font-size: 1.5em;
            text-align: center;
            margin-bottom: 30px;
            color: var(--secondary);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .product-card {
            background: linear-gradient(135deg, rgba(3, 4, 94, 0.6), rgba(0, 0, 50, 0.8));
            border: 1px solid rgba(0, 180, 216, 0.3);
            padding: 20px;
            border-radius: 15px;
            color: white;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
            text-align: center;
            backdrop-filter: blur(5px);
        }
        
        .product-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(
                45deg,
                transparent,
                rgba(0, 180, 216, 0.1),
                transparent
            );
            transition: all 0.5s ease;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 180, 216, 0.3);
        }
        
        .product-card:hover::before {
            transform: translateX(100%);
        }
        
        .product-name {
            font-size: 1.3em;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .product-price {
            font-size: 1.5em;
            color: var(--accent);
            font-weight: bold;
        }
        
        .payment-info {
            background: linear-gradient(135deg, rgba(3, 4, 94, 0.6), rgba(0, 0, 80, 0.8));
            padding: 30px;
            border-radius: 15px;
            margin-top: 50px;
            backdrop-filter: blur(5px);
            border: 1px solid var(--secondary);
        }
        
        .payment-title {
            font-size: 2em;
            color: var(--primary);
            margin-bottom: 25px;
            text-align: center;
            text-shadow: 0 0 15px rgba(0, 180, 216, 0.3);
        }
        
        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 20px;
        }
        
        .payment-method {
            background: rgba(0, 0, 0, 0.4);
            padding: 15px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            gap: 15px;
            border-left: 3px solid var(--primary);
            transition: all 0.3s ease;
        }
        
        .payment-method:hover {
            transform: translateX(5px);
            background: rgba(0, 0, 0, 0.6);
        }
        
        .payment-method i {
            color: var(--secondary);
            font-size: 1.5em;
            min-width: 30px;
        }
        
        .note {
            font-style: italic;
            color: #ff9999;
            margin-top: 40px;
            padding: 25px;
            background-color: rgba(255, 0, 0, 0.1);
            border-radius: 15px;
            border-left: 4px solid #ff5555;
        }
        
        .note strong {
            color: #ff5555;
            font-size: 1.2em;
        }
        
        .divider {
            border-top: 2px dashed var(--primary);
            margin: 40px 0;
            opacity: 0.5;
        }
        
        .music-control {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background-color: rgba(3, 4, 94, 0.8);
            padding: 15px;
            border-radius: 50%;
            cursor: pointer;
            z-index: 100;
            border: 2px solid var(--primary);
            box-shadow: 0 0 20px rgba(0, 180, 216, 0.4);
            transition: all 0.3s ease;
        }
        
        .music-control:hover {
            transform: scale(1.1);
            background-color: rgba(0, 119, 182, 0.8);
        }
        
        .music-control i {
            font-size: 28px;
            color: var(--secondary);
        }
        
        .whatsapp-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            background: linear-gradient(45deg, #25D366, #128C7E);
            color: white;
            text-align: center;
            padding: 18px 30px;
            border-radius: 50px;
            margin-top: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            width: 100%;
            font-size: 1.2em;
            box-shadow: 0 5px 20px rgba(37, 211, 102, 0.4);
        }
        
        .whatsapp-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(37, 211, 102, 0.6);
            background: linear-gradient(45deg, #128C7E, #25D366);
        }
        
        .whatsapp-btn i {
            font-size: 1.6em;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .container {
                margin: 20px;
                padding: 20px;
            }
            
            h1 {
                font-size: 2.8em;
            }
            
            .product-grid {
                grid-template-columns: 1fr;
            }
            
            .tab-btn {
                padding: 10px 15px;
                font-size: 0.9em;
            }
            
            .game-title {
                font-size: 1.8em;
            }
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Background Video -->
    <video autoplay muted loop id="video-background">
        <source src="https://file.idnet.my.id/api/preview.php?file=d5xgc1q1.mp4" type="video/mp4">
        <!-- Replace with your actual video URL -->
    </video>
    
    <!-- Background Music (hidden) -->
    <audio id="bg-music" loop>
        <source src="https://file.idnet.my.id/api/preview.php?file=lr6ishvw.opus" type="audio/mpeg">
        <!-- Replace with your actual music file -->
    </audio>
    
    <!-- Music Control Button -->
    <div class="music-control" onclick="toggleMusic()">
        <i id="music-icon" class="fas fa-music"></i>
    </div>
    
    <div class="container">
        <header>
            <h1>RIMURU STORE</h1>
            <div class="subtitle">Premium Game Topup & Digital Services</div>
        </header>
        
        <div class="game-tabs">
            <button class="tab-btn ff active" onclick="showGame('freefire')">FREE FIRE</button>
            <button class="tab-btn ml" onclick="showGame('mobilelegends')">MOBILE LEGENDS</button>
            <button class="tab-btn roblox" onclick="showGame('roblox')">ROBLOX</button>
            <button class="tab-btn cod" onclick="showGame('codm')">CALL OF DUTY</button>
            <button class="tab-btn pubg" onclick="showGame('pubg')">PUBG</button>
            <button class="tab-btn bot" onclick="showGame('bot')">WHATSAPP BOT</button>
            <button class="tab-btn sosmed" onclick="showGame('sosmed')">SOSMED</button>
        </div>
        
        <!-- Free Fire Section -->
        <div class="game-section active" id="freefire">
            <h2 class="game-title" style="color: var(--ff-color);">FREE FIRE TOPUP</h2>
            <div class="game-subtitle">*DM FF INDO🍥*</div>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('Free Fire', '12💎', '2.500')">
                    <div class="product-name">12💎</div>
                    <div class="product-price">Rp 2.500</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '25💎', '4.999')">
                    <div class="product-name">25💎</div>
                    <div class="product-price">Rp 4.999</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '50💎', '7.300')">
                    <div class="product-name">50💎</div>
                    <div class="product-price">Rp 7.300</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '75💎', '10.000')">
                    <div class="product-name">75💎</div>
                    <div class="product-price">Rp 10.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '90💎', '12.999')">
                    <div class="product-name">90💎</div>
                    <div class="product-price">Rp 12.999</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '100💎', '14.000')">
                    <div class="product-name">100💎</div>
                    <div class="product-price">Rp 14.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '120💎', '16.000')">
                    <div class="product-name">120💎</div>
                    <div class="product-price">Rp 16.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '130💎', '18.000')">
                    <div class="product-name">130💎</div>
                    <div class="product-price">Rp 18.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '150💎', '19.900')">
                    <div class="product-name">150💎</div>
                    <div class="product-price">Rp 19.900</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '160💎', '21.000')">
                    <div class="product-name">160💎</div>
                    <div class="product-price">Rp 21.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '180💎', '23.999')">
                    <div class="product-name">180💎</div>
                    <div class="product-price">Rp 23.999</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '190💎', '25.000')">
                    <div class="product-name">190💎</div>
                    <div class="product-price">Rp 25.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '200💎', '26.000')">
                    <div class="product-name">200💎</div>
                    <div class="product-price">Rp 26.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '210💎', '27.000')">
                    <div class="product-name">210💎</div>
                    <div class="product-price">Rp 27.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', 'Weekly Membership', '28.000')">
                    <div class="product-name">Weekly Membership</div>
                    <div class="product-price">Rp 28.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Free Fire', '250💎', '32.000')">
                    <div class="product-name">250💎</div>
                    <div class="product-price">Rp 32.000</div>
                </div>
            </div>
        </div>
        
        <!-- Mobile Legends Section -->
        <div class="game-section" id="mobilelegends">
            <h2 class="game-title" style="color: var(--ml-color);">MOBILE LEGENDS TOPUP</h2>
            <div class="game-subtitle">*DM ML INDO🍥*</div>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('Mobile Legends', '14💎', '4.500')">
                    <div class="product-name">14💎</div>
                    <div class="product-price">Rp 4.500</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '19💎', '6.400')">
                    <div class="product-name">19💎</div>
                    <div class="product-price">Rp 6.400</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '36💎', '10.500')">
                    <div class="product-name">36💎</div>
                    <div class="product-price">Rp 10.500</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '44💎', '13.000')">
                    <div class="product-name">44💎</div>
                    <div class="product-price">Rp 13.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '50💎', '14.500')">
                    <div class="product-name">50💎</div>
                    <div class="product-price">Rp 14.500</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '59💎', '16.000')">
                    <div class="product-name">59💎</div>
                    <div class="product-price">Rp 16.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '65💎', '18.000')">
                    <div class="product-name">65💎</div>
                    <div class="product-price">Rp 18.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '74💎', '20.300')">
                    <div class="product-name">74💎</div>
                    <div class="product-price">Rp 20.300</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '85💎', '23.000')">
                    <div class="product-name">85💎</div>
                    <div class="product-price">Rp 23.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '112💎', '31.000')">
                    <div class="product-name">112💎</div>
                    <div class="product-price">Rp 31.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '172💎', '36.000')">
                    <div class="product-name">172💎</div>
                    <div class="product-price">Rp 36.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '185💎', '50.000')">
                    <div class="product-name">185💎</div>
                    <div class="product-price">Rp 50.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '257💎', '55.500')">
                    <div class="product-name">257💎</div>
                    <div class="product-price">Rp 55.500</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '284💎', '75.000')">
                    <div class="product-name">284💎</div>
                    <div class="product-price">Rp 75.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '296💎', '78.000')">
                    <div class="product-name">296💎</div>
                    <div class="product-price">Rp 78.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '344💎', '92.000')">
                    <div class="product-name">344💎</div>
                    <div class="product-price">Rp 92.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '370💎', '97.000')">
                    <div class="product-name">370💎</div>
                    <div class="product-price">Rp 97.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '429💎', '111.000')">
                    <div class="product-name">429💎</div>
                    <div class="product-price">Rp 111.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '514💎', '135.000')">
                    <div class="product-name">514💎</div>
                    <div class="product-price">Rp 135.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '568💎', '143.000')">
                    <div class="product-name">568💎</div>
                    <div class="product-price">Rp 143.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '600💎', '154.000')">
                    <div class="product-name">600💎</div>
                    <div class="product-price">Rp 154.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '716💎', '184.000')">
                    <div class="product-name">716💎</div>
                    <div class="product-price">Rp 184.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '792💎', '206.000')">
                    <div class="product-name">792💎</div>
                    <div class="product-price">Rp 206.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '878💎', '222.000')">
                    <div class="product-name">878💎</div>
                    <div class="product-price">Rp 222.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '963💎', '242.000')">
                    <div class="product-name">963💎</div>
                    <div class="product-price">Rp 242.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Mobile Legends', '1050💎', '265.000')">
                    <div class="product-name">1050💎</div>
                    <div class="product-price">Rp 265.000</div>
                </div>
            </div>
        </div>
        
        <!-- Roblox Section -->
        <div class="game-section" id="roblox">
            <h2 class="game-title" style="color: var(--roblox-color);">ROBLOX TOPUP</h2>
            <div class="game-subtitle">*Price Roblox 🍥*</div>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('Roblox', '100 Robux', '18.000')">
                    <div class="product-name">100 Robux</div>
                    <div class="product-price">Rp 18.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Roblox', '400 Robux', '77.000')">
                    <div class="product-name">400 Robux</div>
                    <div class="product-price">Rp 77.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Roblox', 'Roblox Gift Card', '102.000')">
                    <div class="product-name">Roblox Gift Card</div>
                    <div class="product-price">Rp 102.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Roblox', 'Roblox Gift Card', '203.000')">
                    <div class="product-name">Roblox Gift Card</div>
                    <div class="product-price">Rp 203.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Roblox', 'Roblox Gift Card', '505.000')">
                    <div class="product-name">Roblox Gift Card</div>
                    <div class="product-price">Rp 505.000</div>
                </div>
            </div>
        </div>
        
        <!-- Call of Duty Section -->
        <div class="game-section" id="codm">
            <h2 class="game-title" style="color: var(--cod-color);">CALL OF DUTY TOPUP</h2>
            <div class="game-subtitle">*CP Call of Duty MOBILE🍥*</div>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('Call of Duty', '26 CP', '5.500')">
                    <div class="product-name">26 CP</div>
                    <div class="product-price">Rp 5.500</div>
                </div>
                <div class="product-card" onclick="orderProduct('Call of Duty', '62 CP', '9.800')">
                    <div class="product-name">62 CP</div>
                    <div class="product-price">Rp 9.800</div>
                </div>
                <div class="product-card" onclick="orderProduct('Call of Duty', '127 CP', '18.800')">
                    <div class="product-name">127 CP</div>
                    <div class="product-price">Rp 18.800</div>
                </div>
                <div class="product-card" onclick="orderProduct('Call of Duty', '320 CP', '49.000')">
                    <div class="product-name">320 CP</div>
                    <div class="product-price">Rp 49.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Call of Duty', '528 CP', '96.000')">
                    <div class="product-name">528 CP</div>
                    <div class="product-price">Rp 96.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Call of Duty', '1056 CP', '185.000')">
                    <div class="product-name">1056 CP</div>
                    <div class="product-price">Rp 185.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Call of Duty', '1584 CP', '290.000')">
                    <div class="product-name">1584 CP</div>
                    <div class="product-price">Rp 290.000</div>
                </div>
            </div>
        </div>
        
        <!-- PUBG Section -->
        <div class="game-section" id="pubg">
            <h2 class="game-title" style="color: var(--pubg-color);">PUBG TOPUP</h2>
            <div class="game-subtitle">*UC PUBG INDO🍥*</div>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('PUBG', '52 UC', '16.000')">
                    <div class="product-name">52 UC</div>
                    <div class="product-price">Rp 16.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '62 UC', '18.000')">
                    <div class="product-name">62 UC</div>
                    <div class="product-price">Rp 18.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '263 UC', '74.000')">
                    <div class="product-name">263 UC</div>
                    <div class="product-price">Rp 74.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '500 UC', '112.000')">
                    <div class="product-name">500 UC</div>
                    <div class="product-price">Rp 112.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '700 UC', '164.000')">
                    <div class="product-name">700 UC</div>
                    <div class="product-price">Rp 164.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '788 UC', '193.000')">
                    <div class="product-name">788 UC</div>
                    <div class="product-price">Rp 193.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '1000 UC', '242.000')">
                    <div class="product-name">1000 UC</div>
                    <div class="product-price">Rp 242.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '1100 UC', '250.000')">
                    <div class="product-name">1100 UC</div>
                    <div class="product-price">Rp 250.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '2425 UC', '517.000')">
                    <div class="product-name">2425 UC</div>
                    <div class="product-price">Rp 517.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('PUBG', '2875 UC', '625.000')">
                    <div class="product-name">2875 UC</div>
                    <div class="product-price">Rp 625.000</div>
                </div>
            </div>
        </div>
        
        <!-- WhatsApp Bot Section -->
        <div class="game-section" id="bot">
            <h2 class="game-title" style="color: var(--bot-color);">WHATSAPP BOT RENTAL</h2>
            <div class="game-subtitle">Premium WhatsApp Bot Services</div>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('WhatsApp Bot', '1 Month', '5.000')">
                    <div class="product-name">1 Month</div>
                    <div class="product-price">Rp 5.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('WhatsApp Bot', '2 Months', '10.000')">
                    <div class="product-name">2 Months</div>
                    <div class="product-price">Rp 10.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('WhatsApp Bot', '3 Months', '15.000')">
                    <div class="product-name">3 Months</div>
                    <div class="product-price">Rp 15.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('WhatsApp Bot', '4 Months', '20.000')">
                    <div class="product-name">4 Months</div>
                    <div class="product-price">Rp 20.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('WhatsApp Bot', '1 Year', '25.000')">
                    <div class="product-name">1 Year</div>
                    <div class="product-price">Rp 25.000</div>
                </div>
            </div>
        </div>
        
        <!-- Social Media Section -->
        <div class="game-section" id="sosmed">
            <h2 class="game-title" style="color: var(--sosmed-color);">SOCIAL MEDIA SERVICES</h2>
            <div class="game-subtitle">Boost your social media presence</div>
            
            <h3 style="color: var(--sosmed-color); text-align: center; margin-top: 30px;">TikTok</h3>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('TikTok', '500 Likes', '1.000')">
                    <div class="product-name">500 Likes</div>
                    <div class="product-price">Rp 1.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('TikTok', '500 Views', '900')">
                    <div class="product-name">500 Views</div>
                    <div class="product-price">Rp 900</div>
                </div>
                <div class="product-card" onclick="orderProduct('TikTok', '100 Followers', '3.000')">
                    <div class="product-name">100 Followers</div>
                    <div class="product-price">Rp 3.000</div>
                </div>
            </div>
            
            <h3 style="color: var(--sosmed-color); text-align: center; margin-top: 30px;">Instagram</h3>
            <div class="product-grid">
                <div class="product-card" onclick="orderProduct('Instagram', '500 Likes', '2.000')">
                    <div class="product-name">500 Likes</div>
                    <div class="product-price">Rp 2.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Instagram', '500 Views', '1.000')">
                    <div class="product-name">500 Views</div>
                    <div class="product-price">Rp 1.000</div>
                </div>
                <div class="product-card" onclick="orderProduct('Instagram', '100 Followers', '3.000')">
                    <div class="product-name">100 Followers</div>
                    <div class="product-price">Rp 3.000</div>
                </div>
            </div>
        </div>
        
        <div class="divider"></div>
        
        <div class="payment-info">
            <h3 class="payment-title">PAYMENT METHODS</h3>
            <div class="payment-methods">
                <div class="payment-method">
                    <i class="fas fa-phone-alt"></i>
                    <span>Admin: 089506222871</span>
                </div>
                <div class="payment-method">
                    <i class="fas fa-wallet"></i>
                    <span>Dana: 083140427092</span>
                </div>
                <div class="payment-method">
                    <i class="fab fa-google-pay"></i>
                    <span>GOPAY: 083140427092</span>
                </div>
                <div class="payment-method">
                    <i class="fas fa-mobile-alt"></i>
                    <span>SPAY: 083140427092</span>
                </div>
                <div class="payment-method">
                    <i class="fas fa-credit-card"></i>
                    <span>OVO: 083140427092</span>
                </div>
                <div class="payment-method">
                    <i class="fas fa-money-bill-wave"></i>
                    <span>SEABAK: 083140427092</span>
                </div>
                <div class="payment-method">
                    <i class="fas fa-qrcode"></i>
                    <span>QRIS: Contact Admin</span>
                </div>
            </div>
            
            <a href="https://wa.me/6289506222871" class="whatsapp-btn">
                <i class="fab fa-whatsapp"></i>
                CONTACT US VIA WHATSAPP
            </a>
        </div>
        
        <div class="note">
            <p><strong>NOTE 🦢</strong></p>
            <p>- Other denominations please ask admin</p>
            <p>- No rush orders</p>
            <p>- Process: Send ID → Make Payment → Order Completed</p>
        </div>
    </div>

    <script>
        // Music control functionality
        const music = document.getElementById('bg-music');
        const musicIcon = document.getElementById('music-icon');
        let isMusicPlaying = false;
        
        // Try to autoplay music (may be blocked by browser)
        document.addEventListener('DOMContentLoaded', function() {
            music.volume = 0.3; // Set volume to 30%
            const playPromise = music.play();
            
            if (playPromise !== undefined) {
                playPromise.then(_ => {
                    isMusicPlaying = true;
                    musicIcon.classList.add('fa-volume-up');
                    musicIcon.classList.remove('fa-music');
                })
                .catch(error => {
                    isMusicPlaying = false;
                    musicIcon.classList.add('fa-music');
                    musicIcon.classList.remove('fa-volume-up');
                });
            }
        });
        
        function toggleMusic() {
            if (isMusicPlaying) {
                music.pause();
                musicIcon.classList.remove('fa-volume-up');
                musicIcon.classList.add('fa-music');
            } else {
                music.play();
                musicIcon.classList.add('fa-volume-up');
                musicIcon.classList.remove('fa-music');
            }
            isMusicPlaying = !isMusicPlaying;
        }
        
        // Game section switching
        function showGame(gameId) {
            // Hide all game sections
            document.querySelectorAll('.game-section').forEach(section => {
                section.classList.remove('active');
            });
            
            // Show selected game section
            document.getElementById(gameId).classList.add('active');
            
            // Update active tab
            document.querySelectorAll('.tab-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            event.target.classList.add('active');
        }
        
        // Product ordering function
        function orderProduct(game, product, price) {
            const message = `Hello Rimuru Store, I want to order:\nGame: ${game}\nProduct: ${product}\nPrice: Rp ${price}\n\nPlease help me complete this order.`;
            const whatsappUrl = `https://wa.me/6289506222871?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
        }
        
        // Animate product cards on load
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.product-card');
            cards.forEach((card, index) => {
                setTimeout(() => {
                    card.style.opacity = '1';
                    card.style.transform = 'translateY(0)';
                }, index * 50);
            });
        });
    </script>
</body>
</html>
