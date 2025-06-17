<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rimuru Store</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #00d9ff;
            --secondary: #00ffaa;
            --accent: #ff55a5;
        }
        
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
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
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.75);
            border-radius: 20px;
            margin-top: 30px;
            margin-bottom: 50px;
            box-shadow: 0 0 30px rgba(0, 217, 255, 0.7);
            border: 2px solid var(--primary);
            backdrop-filter: blur(8px);
            animation: glow 3s infinite alternate;
        }
        
        @keyframes glow {
            0% {
                box-shadow: 0 0 25px rgba(0, 217, 255, 0.6);
                border-color: var(--primary);
            }
            50% {
                box-shadow: 0 0 35px rgba(0, 255, 242, 0.8);
                border-color: var(--secondary);
            }
            100% {
                box-shadow: 0 0 25px rgba(214, 0, 255, 0.6);
                border-color: var(--accent);
            }
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding: 30px 20px;
            background: linear-gradient(90deg, rgba(0,0,0,0) 0%, rgba(0,217,255,0.15) 50%, rgba(0,0,0,0) 100%);
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
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
        }
        
        h1 {
            font-size: 4em;
            margin: 10px 0;
            background: linear-gradient(to right, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 20px rgba(0, 217, 255, 0.3);
            font-weight: 800;
            letter-spacing: 2px;
        }
        
        .subtitle {
            font-size: 1.5em;
            margin-bottom: 5px;
            color: var(--secondary);
            font-weight: 300;
        }
        
        .category-tabs {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }
        
        .tab-btn {
            padding: 12px 25px;
            background: rgba(0, 100, 150, 0.3);
            border: 1px solid var(--primary);
            color: white;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
            backdrop-filter: blur(5px);
        }
        
        .tab-btn.active {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: #111;
            box-shadow: 0 0 15px rgba(0, 217, 255, 0.5);
            transform: translateY(-3px);
        }
        
        .tab-btn:hover {
            background: rgba(0, 150, 200, 0.5);
        }
        
        .product-section {
            margin-bottom: 40px;
        }
        
        .product-title {
            font-size: 2.2em;
            color: var(--primary);
            margin-bottom: 25px;
            text-align: center;
            position: relative;
        }
        
        .product-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 35%;
            width: 30%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent), transparent);
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .product-btn {
            background: linear-gradient(135deg, rgba(0, 50, 80, 0.5), rgba(0, 0, 50, 0.7));
            border: none;
            padding: 15px;
            border-radius: 10px;
            color: white;
            font-size: 1.1em;
            cursor: pointer;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(0, 217, 255, 0.3);
            text-align: center;
            backdrop-filter: blur(5px);
        }
        
        .product-btn::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                transparent,
                rgba(0, 217, 255, 0.1),
                transparent
            );
            transform: rotate(45deg);
            transition: all 0.5s ease;
        }
        
        .product-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 217, 255, 0.3);
            border-color: var(--primary);
        }
        
        .product-btn:hover::before {
            left: 100%;
        }
        
        .product-btn .diamond {
            color: var(--secondary);
            font-weight: bold;
        }
        
        .product-btn .price {
            display: block;
            margin-top: 8px;
            font-size: 1.2em;
            color: var(--accent);
            font-weight: bold;
        }
        
        .payment-info {
            background: linear-gradient(135deg, rgba(0, 80, 120, 0.5), rgba(0, 0, 80, 0.7));
            padding: 25px;
            border-radius: 15px;
            margin-top: 40px;
            backdrop-filter: blur(5px);
            border: 1px solid var(--secondary);
        }
        
        .payment-title {
            font-size: 1.8em;
            color: var(--primary);
            margin-bottom: 20px;
            text-align: center;
            text-shadow: 0 0 10px rgba(0, 217, 255, 0.3);
        }
        
        .payment-methods {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
        }
        
        .payment-method {
            background: rgba(0, 0, 0, 0.3);
            padding: 12px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
            border-left: 3px solid var(--primary);
        }
        
        .payment-method i {
            color: var(--secondary);
            font-size: 1.3em;
        }
        
        .note {
            font-style: italic;
            color: #ff9999;
            margin-top: 30px;
            padding: 20px;
            background-color: rgba(255, 0, 0, 0.1);
            border-radius: 10px;
            border-left: 4px solid #ff5555;
        }
        
        .note strong {
            color: #ff5555;
        }
        
        .divider {
            border-top: 1px dashed var(--primary);
            margin: 30px 0;
            opacity: 0.5;
        }
        
        .music-control {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: rgba(0, 0, 0, 0.7);
            padding: 12px;
            border-radius: 50%;
            cursor: pointer;
            z-index: 100;
            border: 1px solid var(--primary);
            box-shadow: 0 0 15px rgba(0, 217, 255, 0.3);
            transition: all 0.3s ease;
        }
        
        .music-control:hover {
            transform: scale(1.1);
            background-color: rgba(0, 50, 80, 0.7);
        }
        
        .music-control i {
            font-size: 24px;
            color: var(--primary);
        }
        
        .whatsapp-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            background-color: #25D366;
            color: white;
            text-align: center;
            padding: 15px 25px;
            border-radius: 50px;
            margin-top: 25px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            width: 100%;
            font-size: 1.1em;
            box-shadow: 0 5px 15px rgba(37, 211, 102, 0.3);
        }
        
        .whatsapp-btn:hover {
            background-color: #128C7E;
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(37, 211, 102, 0.4);
        }
        
        .whatsapp-btn i {
            font-size: 1.4em;
        }
        
        /* Animation for product buttons */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .product-btn {
            animation: fadeInUp 0.5s ease forwards;
            opacity: 0;
        }
        
        /* Responsive adjustments */
        @media (max-width: 768px) {
            .container {
                margin: 15px;
                padding: 15px;
            }
            
            h1 {
                font-size: 2.5em;
            }
            
            .product-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
            
            .payment-methods {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Background Video -->
    <video autoplay muted loop id="video-background">
        <source src="https://file.idnet.my.id/api/preview.php?file=2rl4hdtl.mp4" type="video/mp4">
        <!-- Replace with your actual video URL -->
    </video>
    
    <!-- Background Music (hidden) -->
    <audio id="bg-music" loop>
        <source src="https://file.idnet.my.id/api/preview.php?file=si1sc8p7.opus" type="audio/mpeg">
        <!-- Replace with your actual music file -->
    </audio>
    
    <!-- Music Control Button -->
    <div class="music-control" onclick="toggleMusic()">
        <i id="music-icon" class="fas fa-music"></i>
    </div>
    
    <div class="container">
        <header>
            <h1>RIMURU STORE</h1>
            <div class="subtitle">Premium In-Game Items & Currency</div>
        </header>
        
        <div class="category-tabs">
            <button class="tab-btn active">FREE FIRE</button>
            <button class="tab-btn">EPEP</button>
            <button class="tab-btn">OTHER GAMES</button>
        </div>
        
        <div class="product-section">
            <h2 class="product-title">*DM FF INDO🍥*</h2>
            <div class="product-grid">
                <button class="product-btn">
                    <span class="diamond">12💎</span>
                    <span class="price">Rp 2.500</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">25💎</span>
                    <span class="price">Rp 4.999</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">50💎</span>
                    <span class="price">Rp 7.300</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">75💎</span>
                    <span class="price">Rp 10.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">90💎</span>
                    <span class="price">Rp 12.999</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">100💎</span>
                    <span class="price">Rp 14.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">120💎</span>
                    <span class="price">Rp 16.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">130💎</span>
                    <span class="price">Rp 18.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">150💎</span>
                    <span class="price">Rp 19.900</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">160💎</span>
                    <span class="price">Rp 21.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">180💎</span>
                    <span class="price">Rp 23.999</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">190💎</span>
                    <span class="price">Rp 25.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">200💎</span>
                    <span class="price">Rp 26.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">210💎</span>
                    <span class="price">Rp 27.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">Weekly Membership</span>
                    <span class="price">Rp 28.000</span>
                </button>
                <button class="product-btn">
                    <span class="diamond">250💎</span>
                    <span class="price">Rp 32.000</span>
                </button>
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
                ORDER VIA WHATSAPP
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
        
        // Animate product buttons on load
        document.addEventListener('DOMContentLoaded', function() {
            const buttons = document.querySelectorAll('.product-btn');
            buttons.forEach((btn, index) => {
                setTimeout(() => {
                    btn.style.animationDelay = `${index * 0.1}s`;
                    btn.style.opacity = 1;
                }, 100);
            });
            
            // Tab functionality
            const tabs = document.querySelectorAll('.tab-btn');
            tabs.forEach(tab => {
                tab.addEventListener('click', () => {
                    tabs.forEach(t => t.classList.remove('active'));
                    tab.classList.add('active');
                    // Here you would add code to switch between different product categories
                });
            });
            
            // Make product buttons clickable (would link to order process)
            const productBtns = document.querySelectorAll('.product-btn');
            productBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    const product = btn.querySelector('.diamond').textContent;
                    const price = btn.querySelector('.price').textContent;
                    alert(`You selected: ${product} for ${price}\nYou will be redirected to WhatsApp to complete your order.`);
                    // window.location.href = 'https://wa.me/6289506222871';
                });
            });
        });
    </script>
</body>
</html>
