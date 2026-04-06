
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>NarajiRawcrylics | Soft Rainbow Nail Studio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Great+Vibes&family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --soft-pink: #FFB7B2;
            --soft-lavender: #E8D1FF;
            --soft-mint: #B5F0E6;
            --soft-peach: #FFD6A5;
            --soft-blue: #A0C4FF;
            --soft-butter: #FDFFB0;
            
            /* Light mode (default) */
            --bg-primary: #f5f0eb;
            --bg-glass: rgba(255, 255, 255, 0.88);
            --bg-glass-solid: rgba(255, 255, 255, 0.95);
            --text-primary: #2C2C2C;
            --text-secondary: #5a5a5a;
            --border-color: rgba(255, 183, 178, 0.3);
            --marble-bg: url('https://i.imgur.com/a/SX7nG5v');
            --card-bg: rgba(255, 255, 255, 0.88);
            --price-item-bg: rgba(255, 255, 255, 0.7);
            
            --heading-font: 'Playfair Display', serif;
            --accent-font: 'Great Vibes', cursive;
            --body-font: 'Inter', sans-serif;
            --header-height-desktop: 80px;
            --header-height-mobile: 70px;
            --border-radius: 24px;
            --border-radius-small: 16px;
        }
        
        /* DARK MODE - TRUE BLACK BACKGROUND */
        body.dark-mode {
            --bg-primary: #000000;
            --bg-glass: rgba(15, 15, 15, 0.92);
            --bg-glass-solid: rgba(10, 10, 10, 0.96);
            --text-primary: #f0f0f0;
            --text-secondary: #b0b0b0;
            --border-color: rgba(255, 183, 178, 0.2);
            --marble-bg: none;
            --card-bg: rgba(20, 20, 20, 0.92);
            --price-item-bg: rgba(30, 30, 30, 0.7);
            background: #000000;
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: var(--body-font);
            background-color: var(--bg-primary);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: var(--marble-bg);
            background-size: cover;
            background-attachment: fixed;
            background-position: center;
            position: relative;
            transition: background-color 0.3s ease, color 0.3s ease;
        }
        body.dark-mode .falling-dots .dot { background: rgba(255,255,255,0.2); }
        
        .falling-dots { position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 1; overflow: hidden; }
        .dot { position: absolute; background: rgba(255,255,255,0.4); border-radius: 50%; animation: fall linear infinite; }
        @keyframes fall { 0% { transform: translateY(-10vh) rotate(0deg); opacity: 0; } 10% { opacity: 0.5; } 90% { opacity: 0.5; } 100% { transform: translateY(110vh) rotate(360deg); opacity: 0; } }
        .container { width: 100%; max-width: 1200px; margin: 0 auto; padding: 0 24px; position: relative; z-index: 2; }
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0);
            background-size: 300% 300%;
            color: #1a1a1a;
            font-weight: 600;
            padding: 12px 28px;
            border-radius: 40px;
            transition: all 0.4s ease;
            border: none;
            cursor: pointer;
            animation: softShift 8s ease infinite;
        }
        body.dark-mode .btn { color: #000000; }
        @keyframes softShift { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
        .section-title {
            font-family: var(--accent-font);
            font-size: 3rem;
            text-align: center;
            margin-bottom: 2rem;
            position: relative;
            color: var(--text-primary);
        }
        .section-title span { display: block; font-family: var(--body-font); font-size: 0.85rem; color: var(--text-secondary); letter-spacing: 2px; text-transform: uppercase; margin-top: 5px; }
        .page { display: none; animation: fadeIn 0.5s ease; }
        .page.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        
        /* LOCKED HEADER */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: var(--bg-glass-solid);
            backdrop-filter: blur(12px);
            height: var(--header-height-desktop);
            border-bottom: 1px solid var(--border-color);
            transition: all 0.3s ease;
        }
        .header-transparent { background: rgba(255,255,255,0.85) !important; }
        body.dark-mode .header-transparent { background: rgba(10,10,10,0.9) !important; }
        .header-container { display: flex; justify-content: space-between; align-items: center; height: 100%; padding: 0 24px; max-width: 1200px; margin: 0 auto; }
        .logo {
            font-family: var(--accent-font);
            font-size: 1.8rem;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            cursor: pointer;
        }
        @media (min-width:768px) { .logo { font-size: 2.2rem; } }
        .nav-desktop { display: flex; align-items: center; gap: 20px; }
        .nav-center { display: flex; align-items: center; gap: 20px; padding: 6px 16px; background: rgba(255,255,255,0.6); border-radius: 40px; }
        body.dark-mode .nav-center { background: rgba(255,255,255,0.08); }
        .nav-links { display: flex; gap: 20px; list-style: none; }
        .nav-links a { font-weight: 500; color: var(--text-primary); font-size: 0.9rem; cursor: pointer; }
        .nav-links a.active-page { color: #FF9B8A; }
        .divider { width: 1px; height: 20px; background: linear-gradient(to bottom, transparent, var(--soft-pink), transparent); }
        .hamburger { display: none; flex-direction: column; gap: 5px; background: rgba(255,255,255,0.9); border: 1px solid var(--border-color); padding: 10px; border-radius: 12px; cursor: pointer; width: 44px; height: 44px; }
        body.dark-mode .hamburger { background: rgba(255,255,255,0.1); }
        .hamburger span { width: 22px; height: 2px; background: var(--text-primary); transition: 0.3s; border-radius: 2px; }
        .mobile-menu { position: fixed; top: var(--header-height-mobile); left: 0; width: 100%; height: calc(100vh - var(--header-height-mobile)); background: var(--bg-glass-solid); backdrop-filter: blur(10px); transform: translateX(100%); opacity: 0; transition: 0.3s cubic-bezier(0.4,0,0.2,1); z-index: 999; pointer-events: none; overflow-y: auto; visibility: hidden; }
        .mobile-menu.active { transform: translateX(0); opacity: 1; pointer-events: all; visibility: visible; }
        .mobile-links { padding: 30px 20px; display: flex; flex-direction: column; gap: 15px; text-align: center; }
        .mobile-links li { background: rgba(255,255,255,0.08); border-radius: 16px; border: 1px solid var(--border-color); }
        .mobile-links a { display: block; padding: 14px 20px; font-size: 1.2rem; font-weight: 500; color: var(--text-primary); }
        .mobile-menu-btn { padding: 25px 20px 35px; text-align: center; border-top: 1px solid var(--border-color); }
        
        /* Dark Mode Toggle Button */
        .dark-mode-toggle {
            background: rgba(255,255,255,0.2);
            border: 1px solid var(--border-color);
            border-radius: 50%;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-left: 10px;
        }
        .dark-mode-toggle i { font-size: 1.2rem; color: var(--text-primary); }
        .dark-mode-toggle:hover { transform: scale(1.05); background: rgba(255,183,178,0.3); }
        .header-actions { display: flex; align-items: center; gap: 10px; }
        
        .hero {
            min-height: 90vh;
            background-image: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), url('https://i.postimg.cc/gjPtGJJG/Screenshot_2026_03_24_094423.png');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: 0;
            padding-top: calc(var(--header-height-desktop) + 40px);
            padding-bottom: 80px;
            text-align: center;
        }
        .hero-title { font-family: var(--accent-font); font-size: clamp(2.5rem,8vw,5rem); background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0); background-clip: text; -webkit-background-clip: text; color: transparent; animation: softShift 8s ease infinite; }
        .hero-subtitle { font-family: var(--accent-font); font-size: clamp(1.2rem,4vw,2.2rem); margin-bottom: 30px; color: var(--text-secondary); }
        
        .two-column { display: flex; flex-wrap: wrap; gap: 40px; align-items: center; }
        .two-column > div { flex: 1; min-width: 250px; }
        .side-image { border-radius: var(--border-radius); overflow: hidden; box-shadow: 0 8px 20px rgba(0,0,0,0.2); width: 100%; height: auto; }
        .side-image img { width: 100%; height: auto; display: block; object-fit: cover; }
        
        .hero-slideshow { width: 100%; overflow: hidden; margin: 40px 0 20px; border-radius: var(--border-radius); box-shadow: 0 10px 30px rgba(0,0,0,0.2); }
        .slideshow-container { position: relative; width: 100%; overflow: hidden; }
        .slideshow-track { display: flex; animation: scrollAll 60s linear infinite; width: fit-content; }
        .slideshow-track:hover { animation-play-state: paused; }
        .slide-item { flex: 0 0 auto; width: 280px; height: 280px; margin-right: 20px; border-radius: 20px; overflow: hidden; box-shadow: 0 5px 15px rgba(0,0,0,0.2); }
        .slide-item img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.4s; }
        .slide-item:hover img { transform: scale(1.05); }
        @keyframes scrollAll { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-300px * 12)); } }
        .view-gallery-btn { text-align: center; margin: 30px 0 20px; }
        
        .shea-callout {
            background: linear-gradient(135deg, rgba(255,183,178,0.2), rgba(232,209,255,0.2), rgba(181,240,230,0.2));
            border-radius: var(--border-radius);
            padding: 20px 30px;
            text-align: center;
            margin: 30px 0;
            border: 2px solid var(--soft-pink);
            backdrop-filter: blur(4px);
        }
        .shea-callout p {
            font-family: var(--accent-font);
            font-size: 2rem;
            color: var(--text-primary);
            margin: 0;
        }
        .shea-callout i {
            color: #FF9B8A;
            margin-right: 10px;
        }
        
        /* Shea Shop Section */
        .shea-shop {
            margin: 60px 0;
        }
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        .product-card {
            background: var(--card-bg);
            backdrop-filter: blur(4px);
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            border: 1px solid var(--border-color);
            transition: transform 0.3s ease;
        }
        .product-card:hover {
            transform: translateY(-8px);
        }
        .product-image {
            width: 100%;
            max-width: 250px;
            margin: 0 auto 20px;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }
        .product-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        .product-title {
            font-family: var(--heading-font);
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 10px;
            color: var(--text-primary);
        }
        .product-price {
            font-size: 1.3rem;
            color: #FF9B8A;
            font-weight: 600;
            margin-bottom: 15px;
        }
        .product-description {
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin-bottom: 15px;
        }
        .special-offer {
            background: rgba(255,183,178,0.2);
            padding: 10px;
            border-radius: 12px;
            margin: 15px 0;
            font-weight: bold;
            color: #FF9B8A;
        }
        .order-form-section {
            background: var(--card-bg);
            backdrop-filter: blur(4px);
            border-radius: var(--border-radius);
            padding: 35px;
            border: 1px solid var(--border-color);
            margin-top: 30px;
        }
        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 20px;
        }
        .form-group {
            flex: 1;
            min-width: 200px;
        }
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--text-primary);
        }
        .form-control {
            width: 100%;
            padding: 12px 16px;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            background: var(--bg-glass);
            color: var(--text-primary);
            font-family: var(--body-font);
        }
        .form-control:focus {
            outline: none;
            border-color: var(--soft-pink);
        }
        .quantity-select {
            display: flex;
            align-items: center;
            gap: 15px;
            flex-wrap: wrap;
        }
        .quantity-select select {
            width: auto;
            min-width: 100px;
        }
        
        .brand-card, .service-card, .hour-card, .price-category, .policy-item, .tech-content, .booking-form-container { background: var(--card-bg); backdrop-filter: blur(4px); border-radius: var(--border-radius); padding: 30px; border: 1px solid var(--border-color); transition: background 0.3s ease; }
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px,1fr)); gap: 30px; margin-top: 40px; }
        .price-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px,1fr)); gap: 15px; }
        .price-item { background: var(--price-item-bg); padding: 12px 18px; border-radius: var(--border-radius-small); display: flex; justify-content: space-between; align-items: center; transition: background 0.3s ease; }
        .price-amount { color: #FF9B8A; font-weight: 600; }
        .gallery-slider-container { overflow: hidden; padding: 15px 0; }
        .gallery-slider { display: flex; gap: 20px; animation: scrollSoft 45s linear infinite; }
        .gallery-slider:hover { animation-play-state: paused; }
        .gallery-slide { flex: 0 0 auto; width: 260px; height: 260px; border-radius: var(--border-radius); overflow: hidden; box-shadow: 0 8px 20px rgba(0,0,0,0.15); }
        .gallery-slide img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.4s; }
        .gallery-slide:hover img { transform: scale(1.08); }
        @keyframes scrollSoft { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-280px * 6)); } }
        .category-title { font-family: var(--heading-font); font-size: 2rem; font-weight: 600; text-align: center; margin-bottom: 25px; color: var(--text-primary); }
        .submit-btn { background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF); background-size: 300% 300%; color: #1a1a1a; font-weight: 600; padding: 14px 45px; border-radius: 40px; border: none; cursor: pointer; animation: softShift 8s ease infinite; transition: transform 0.2s; }
        .submit-btn:hover { transform: scale(1.02); }
        body.dark-mode .submit-btn { color: #000000; }
        footer { background: var(--bg-glass-solid); backdrop-filter: blur(8px); padding: 50px 0 30px; margin-top: 60px; border-top: 1px solid var(--border-color); }
        .footer-container { display: flex; flex-wrap: wrap; justify-content: space-between; gap: 40px; }
        .scroll-top { position: fixed; bottom: 30px; right: 30px; width: 45px; height: 45px; background: linear-gradient(135deg, #FFB7B2, #E8D1FF); border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; opacity: 0; visibility: hidden; transition: 0.3s; z-index: 100; box-shadow: 0 4px 12px rgba(0,0,0,0.2); }
        .scroll-top.visible { opacity: 1; visibility: visible; }
        .scroll-top i { color: #1a1a1a; }
        .modal-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.8); backdrop-filter: blur(4px); display: flex; align-items: center; justify-content: center; z-index: 1100; opacity: 0; visibility: hidden; transition: 0.3s; }
        .modal-overlay.active { opacity: 1; visibility: visible; }
        .modal-content { background: var(--bg-glass-solid); border-radius: var(--border-radius); padding: 40px; max-width: 500px; width: 90%; text-align: center; border: 1px solid var(--border-color); }
        
        @media (max-width: 768px) {
            .nav-desktop { display: none; }
            .hamburger { display: flex; }
            .hero { padding-top: calc(var(--header-height-mobile) + 30px); }
            .two-column { flex-direction: column; }
            .category-title { font-size: 1.6rem; }
            .slide-item { width: 200px; height: 200px; margin-right: 15px; }
            @keyframes scrollAll { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-215px * 12)); } }
            .gallery-slide { width: 200px; height: 200px; }
            @keyframes scrollSoft { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-220px * 6)); } }
            .product-grid { grid-template-columns: 1fr; }
        }
        @media (max-width: 480px) {
            .slide-item { width: 160px; height: 160px; margin-right: 12px; }
            @keyframes scrollAll { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-172px * 12)); } }
            .gallery-slide { width: 160px; height: 160px; }
            @keyframes scrollSoft { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-180px * 6)); } }
            .shea-callout p { font-size: 1.5rem; }
        }
    </style>
</head>
<body>
    <div class="falling-dots" id="fallingDots"></div>
    <div class="scroll-top" id="scrollTop"><i class="fas fa-chevron-up"></i></div>
    
    <header id="main-header">
        <div class="header-container">
            <div class="logo" data-page="home">NarajiRawcrylics</div>
            <div class="header-actions">
                <div class="nav-desktop">
                    <div class="nav-center">
                        <ul class="nav-links">
                            <li><a href="#" class="nav-link active-page" data-page="home">Home</a></li>
                            <li><a href="#" class="nav-link" data-page="gallery">Gallery</a></li>
                            <li><a href="#" class="nav-link" data-page="booking">Booking</a></li>
                        </ul>
                        <div class="divider"></div>
                        <a href="#" class="btn" data-page="booking">Book Now</a>
                    </div>
                </div>
                <div class="dark-mode-toggle" id="darkModeToggle">
                    <i class="fas fa-moon"></i>
                </div>
                <button class="hamburger" id="hamburger" aria-label="Menu"><span></span><span></span><span></span></button>
            </div>
        </div>
        <div class="mobile-menu" id="mobile-menu">
            <ul class="mobile-links">
                <li><a href="#" class="nav-link active-page" data-page="home">Home</a></li>
                <li><a href="#" class="nav-link" data-page="gallery">Gallery</a></li>
                <li><a href="#" class="nav-link" data-page="booking">Booking</a></li>
            </ul>
            <div class="mobile-menu-btn"><a href="#" class="btn" data-page="booking">Book Now</a></div>
        </div>
    </header>

    <!-- HOME PAGE (existing nail content remains unchanged) -->
    <div class="page active" id="home-page">
        <section class="hero">
            <div class="hero-content">
                <h1 class="hero-title">NarajiRawcrylics</h1>
                <p class="hero-subtitle">Soft Rainbow Nail Studio</p>
                <a href="#" class="btn hero-btn" data-page="booking">Book Your Appointment</a>
            </div>
        </section>
        
        <div class="container">
            <div class="hero-slideshow">
                <div class="slideshow-container">
                    <div class="slideshow-track" id="homeSlideshow"></div>
                </div>
                <div class="view-gallery-btn">
                    <a href="#" class="btn" data-page="gallery">✨ View Full Gallery ✨</a>
                </div>
            </div>
            
            <section class="brand-description">
                <div class="two-column">
                    <div>
                        <div class="brand-card">
                            <h2 class="brand-title" style="font-family: var(--accent-font); font-size: 2.5rem;">✨ Creativity. Precision. Detail. ✨</h2>
                            <p class="brand-text">NarajiRawcrylics is a nail brand built on creativity, precision, and detail. I specialize in acrylic sets, Gel X extensions, and custom press-on nails designed to elevate each client's personal style.<br><br>
                            Every set is crafted with intention, focusing on structure, longevity, and a flawless finish. My goal is to provide not just nails, but a luxury experience where clients feel confident, comfortable, and taken care of.<br><br>
                            As the brand grows, NarajiRawcrylics is expanding into natural beauty, including <strong>whipped Shea butter, herbs, and skincare products</strong> that promote self-care from the inside out. 💐💕<br>
                            🌿 <em>Coming soon: NarajiRawOrganics – pure, handcrafted Shea butter and herbal body care.</em></p>
                        </div>
                    </div>
                    <div class="side-image">
                        <img src="https://i.postimg.cc/fLHMqhg7/Screenshot-20260403-163502-Docs-2.jpg" alt="Brand inspiration">
                    </div>
                </div>
            </section>
            
            <div class="shea-callout">
                <p><i class="fas fa-hand-peace"></i> Go check out my handmade shea butter!! <i class="fas fa-heart" style="color: #FF9B8A;"></i></p>
            </div>
            
            <section class="services">
                <h2 class="section-title">My Services<span>Luxury Nail Experiences</span></h2>
                <div class="services-grid">
                    <div class="service-card"><div class="service-icon"><i class="fas fa-hand-fist"></i></div><h3 class="service-title">Acrylic Sets</h3><p class="service-description">Traditional acrylic with strong structure and flawless finish.</p></div>
                    <div class="service-card"><div class="service-icon"><i class="fas fa-spa"></i></div><h3 class="service-title">Gel X Extensions</h3><p class="service-description">Lightweight, flexible gel extensions with natural feel and high shine.</p></div>
                    <div class="service-card"><div class="service-icon"><i class="fas fa-box"></i></div><h3 class="service-title">Custom Press-Ons</h3><p class="service-description">Handcrafted press‑ons using your custom sizing kit. <strong>Available any day!</strong> Order whenever you're ready.</p></div>
                </div>
            </section>
        </div>
        
        <section class="after-hours"><div class="container"><h2 class="section-title">After Hours Luxury<span>Private Late Night Experience</span></h2><div class="hours-grid"><div class="hour-card"><div class="hour-time">9PM - 11PM</div><div class="hour-price">+$40</div></div><div class="hour-card"><div class="hour-time">12AM - 2AM</div><div class="hour-price">+$60</div></div><div class="hour-card"><div class="hour-time">2AM - 4AM</div><div class="hour-price">+$80</div></div></div><p style="text-align:center; margin-top:20px;">✨ Exclusively available Tuesday-Thursday nights ✨</p></div></section>
        
        <div class="container">
            <section class="meet-tech">
                <div class="two-column">
                    <div class="side-image">
                        <img src="https://i.postimg.cc/k5zV1K6P/Screenshot-20260403-161537-Docs-2.jpg" alt="Nail tech portrait">
                    </div>
                    <div>
                        <div class="tech-content">
                            <h2 class="tech-name" style="font-family: var(--accent-font); font-size: 2.5rem;">Meet Your Nail Tech - NARAJI</h2>
                            <p class="tech-bio">Hi, I'm the nail tech behind the nail drill. NarajiRawcrylics is the brand but you can call me Raw. With a true passion for art, creativity, and self-expression, I've been helping clients feel confident through beautifully crafted nails.<br><br>
                            I specialize in acrylic sets, Gel X extensions, and custom press-on nails designed to match each client's personal style. Every set is created with care, precision, and attention to detail.<br><br>
                            My goal is to provide quality work and a comfortable, luxury experience so every client leaves feeling confident, happy, and in love with their nails.<br><br>
                            Beyond nails, I am also growing <strong>NarajiRawOrganics</strong> – a natural beauty line featuring whipped Shea butter, herbal infusions, and skincare that support self-care and overall wellness. 💐💕</p>
                            <div class="tech-quote" style="font-family: var(--accent-font); font-size: 1.5rem; color: #FF9B8A; margin-top: 30px; padding: 20px; background: rgba(255,183,178,0.12); border-radius: var(--border-radius); text-align: center;">"Freestyle sets may include nail art, stones, and custom designs. Each set is one of one ✨"</div>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="price-list">
                <h2 class="section-title">Price List<span>Investment in Beauty</span></h2>
                <div class="price-category"><h3 class="price-category-title">✨ Signature Freestyle</h3><div class="price-grid"><div class="price-item"><span>Freestyle Full Set</span><span class="price-amount">$100</span></div></div><p style="font-size:0.85rem;">*All lengths except XL. Full creative control – trust the artist's vision*</p></div>
                <div class="price-category"><h3 class="price-category-title">💅 Full Sets</h3><div class="price-grid"><div class="price-item"><span>Super Short</span><span class="price-amount">$50</span></div><div class="price-item"><span>Short</span><span class="price-amount">$60</span></div><div class="price-item"><span>Medium</span><span class="price-amount">$70</span></div><div class="price-item"><span>Long</span><span class="price-amount">$80</span></div><div class="price-item"><span>XL</span><span class="price-amount">$90</span></div><div class="price-item"><span>XXL</span><span class="price-amount">$100</span></div><div class="price-item"><span>Multi-shape (per nail)</span><span class="price-amount">+$3</span></div></div></div>
                <div class="price-category"><h3 class="price-category-title">🌈 Ombre Full Sets</h3><div class="price-grid"><div class="price-item"><span>Super Short</span><span class="price-amount">$60</span></div><div class="price-item"><span>Short</span><span class="price-amount">$70</span></div><div class="price-item"><span>Medium</span><span class="price-amount">$80</span></div><div class="price-item"><span>Long</span><span class="price-amount">$90</span></div><div class="price-item"><span>XL</span><span class="price-amount">$110</span></div><div class="price-item"><span>XXL</span><span class="price-amount">$125</span></div></div></div>
                <div class="price-category"><h3 class="price-category-title">💖 Gel Services</h3><div class="price-grid"><div class="price-item"><span>Gel Manicure</span><span class="price-amount">$50</span></div><div class="price-item"><span>Gel Polish Change</span><span class="price-amount">$30</span></div></div></div>
                <div class="price-category"><h3 class="price-category-title">🦶 Toe Services</h3><div class="price-grid"><div class="price-item"><span>Acrylic Big Toe</span><span class="price-amount">$10</span></div><div class="price-item"><span>Full Set Acrylic Toes</span><span class="price-amount">$45-60</span></div><div class="price-item"><span>Polygel Big Toe</span><span class="price-amount">$15</span></div><div class="price-item"><span>Full Set Polygel Toes</span><span class="price-amount">$55-65</span></div></div></div>
                
                <div class="price-category">
                    <div class="two-column" style="gap: 30px;">
                        <div style="flex:1">
                            <h3 class="price-category-title">📦 Press-On Sets</h3>
                            <div class="price-grid">
                                <div class="price-item"><span>Sizing Kit</span><span class="price-amount">$10</span></div>
                                <div class="price-item"><span>Toes + Hands Sizing Kit</span><span class="price-amount">$16</span></div>
                                <div class="price-item"><span>Freestyle Press-Ons</span><span class="price-amount">$110</span></div>
                                <div class="price-item"><span>Freestyle Press-Ons (Luxury)</span><span class="price-amount">$130</span></div>
                            </div>
                            <p style="margin-top: 15px; background: rgba(255,183,178,0.15); padding: 10px; border-radius: 12px; text-align: center;"><strong>✨ Press-ons can be purchased ANY DAY ✨</strong><br>Order your sizing kit, then your custom set – no appointment needed!</p>
                            <p style="margin-top: 10px; background: rgba(255,100,100,0.15); padding: 8px; border-radius: 12px; text-align: center; font-weight: bold; color: #FF9B8A;">⚠️ ALL SALES ARE FINAL on custom press-ons and products.</p>
                        </div>
                        <div class="side-image" style="flex:1">
                            <img src="https://i.postimg.cc/85CS60Pk/Screenshot-20260403-163445-Docs-2.jpg" alt="Press-on nails example">
                        </div>
                    </div>
                </div>
                
                <div class="price-category"><h3 class="price-category-title">🎨 Add-Ons</h3>
                    <div class="price-grid">
                        <div class="price-item"><span>French (per nail)</span><span class="price-amount">+$5</span></div>
                        <div class="price-item"><span><strong>🔥 French Tip (All 10 fingers)</strong></span><span class="price-amount"><strong>+$10</strong></span></div>
                        <div class="price-item"><span>Gel French (Full Set)</span><span class="price-amount">+$25</span></div>
                        <div class="price-item"><span>Encapsulation (per nail)</span><span class="price-amount">+$7</span></div>
                        <div class="price-item"><span>Cuticle Stones (per nail)</span><span class="price-amount">+$3</span></div>
                        <div class="price-item"><span>Cluster Stones (per nail)</span><span class="price-amount">+$10</span></div>
                        <div class="price-item"><span>3D Art (per nail)</span><span class="price-amount">+$12</span></div>
                        <div class="price-item"><span>Basic Nail Art</span><span class="price-amount">+$8</span></div>
                        <div class="price-item"><span>Nail Piercing (per nail)</span><span class="price-amount">+$3</span></div>
                        <div class="price-item"><span>Marble (10 fingers)</span><span class="price-amount">+$15</span></div>
                        <div class="price-item"><span>Soak Off</span><span class="price-amount">$25</span></div>
                        <div class="price-item"><span>Soak Off (Not My Work)</span><span class="price-amount">$30</span></div>
                    </div>
                </div>
            </section>
            
            <section class="policies"><div class="policies-container"><h2 class="section-title">Booking Policies<span>Important Information</span></h2>
                <div class="policy-item"><h3 class="policy-title"><i class="fas fa-money-bill-wave"></i> Deposit Required</h3><p class="policy-text">A $25 deposit is required to secure all appointments. Non-refundable.</p></div>
                <div class="policy-item"><h3 class="policy-title"><i class="fas fa-clock"></i> Late Policy</h3><p class="policy-text">Please arrive on time. More than 10 minutes late may need to reschedule.</p></div>
                <div class="policy-item"><h3 class="policy-title"><i class="fas fa-calendar-times"></i> No Call, No Show</h3><p class="policy-text">Will require a new deposit before booking again.</p></div>
                <div class="policy-item"><h3 class="policy-title"><i class="fas fa-calendar-alt"></i> Rescheduling</h3><p class="policy-text">Notify at least 24 hours in advance. Deposit may be transferred once.</p></div>
                <div class="policy-item"><h3 class="policy-title"><i class="fas fa-hand-peace"></i> Preparation</h3><p class="policy-text">Arrive with bare nails unless removal booked. No extra guests without approval. Address sent 24h before.</p></div>
                <div class="policy-item"><h3 class="policy-title"><i class="fas fa-credit-card"></i> Payment</h3><p class="policy-text">Cash preferred. Zelle or Cash App accepted before service.</p></div>
            </div></section>
            
            <!-- NEW SHEA BUTTER SHOP SECTION (separate from nail services) -->
            <section class="shea-shop">
                <h2 class="section-title">Whipped Shea Butters<span>Handmade • Natural • Luxurious</span></h2>
                <div class="product-grid">
                    <!-- 4 oz product -->
                    <div class="product-card">
                        <div class="product-image">
                            <img src="https://i.postimg.cc/MKqK9Hrb/Screenshot_20260405_201239_Docs_2.jpg" alt="4 oz Coconut Vanilla Body Butter">
                        </div>
                        <h3 class="product-title">Coconut Vanilla Body Butter</h3>
                        <div class="product-price">4 oz (Glass Jar) – $15</div>
                        <p class="product-description">Pamper yourself with our luxurious, all-natural body butter. Carefully handcrafted, each batch is piped by hand into a beautiful glass jar, making every jar unique. Infused with the warm, soothing scents of coconut and vanilla, it melts effortlessly into your skin, leaving it soft, nourished, and delicately scented. Made with 100% natural ingredients.</p>
                    </div>
                    <!-- 1 oz product -->
                    <div class="product-card">
                        <div class="product-image">
                            <img src="https://i.postimg.cc/yYsYLxrh/Screenshot_20260405_201153_Docs-2.jpg" alt="1 oz Coconut Vanilla Body Butter">
                        </div>
                        <h3 class="product-title">Coconut Vanilla Body Butter</h3>
                        <div class="product-price">1 oz – $5</div>
                        <p class="product-description">Same luxurious formula in a convenient travel size. Perfect for on-the-go hydration or to try before committing to the full size. Hand-piped and made with love.</p>
                    </div>
                </div>
                
                <!-- Special offer & shipping info -->
                <div style="text-align: center; margin: 20px 0;">
                    <div class="special-offer" style="display: inline-block; padding: 12px 25px;">
                        🎁 Special: Two for $25 (mix & match sizes) 🎁
                    </div>
                    <p style="margin-top: 15px; font-size: 0.9rem; color: var(--text-secondary);">
                        <i class="fas fa-shipping-fast"></i> Shipping: Each jar is carefully packaged and shipped within 1 business day. Delivery typically takes 2–3 business days via USPS First Class, or 1–2 days with Priority Mail.
                    </p>
                </div>
                
                <!-- SEPARATE ORDER FORM FOR SHEA BUTTER (includes address) -->
                <div class="order-form-section">
                    <h3 style="font-family: var(--accent-font); font-size: 2rem; text-align: center; margin-bottom: 25px;">Order Shea Butter</h3>
                    <form id="sheaOrderForm">
                        <div class="form-row">
                            <div class="form-group">
                                <label>Full Name</label>
                                <input type="text" id="sheaName" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label>Email Address</label>
                                <input type="email" id="sheaEmail" class="form-control" required>
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label>Phone Number</label>
                                <input type="tel" id="sheaPhone" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label>Shipping Address</label>
                                <input type="text" id="sheaAddress" class="form-control" placeholder="Street address, city, state, ZIP" required>
                            </div>
                        </div>
                        <div class="form-row">
                            <div class="form-group">
                                <label>Select Size</label>
                                <select id="sheaSize" class="form-control" required>
                                    <option value="">Choose size</option>
                                    <option value="1oz">1 oz - $5</option>
                                    <option value="4oz">4 oz (Glass Jar) - $15</option>
                                    <option value="two-for-25">Two for $25 (mix & match - specify in notes)</option>
                                </select>
                            </div>
                            <div class="form-group">
                                <label>Quantity</label>
                                <input type="number" id="sheaQuantity" class="form-control" value="1" min="1" required>
                            </div>
                        </div>
                        <div class="form-group">
                            <label>Special Instructions or Notes</label>
                            <textarea id="sheaNotes" class="form-control" rows="3" placeholder="e.g., mix & match sizes, scent preferences, etc."></textarea>
                        </div>
                        <div style="text-align: center; margin-top: 25px;">
                            <button type="submit" class="submit-btn">Place Order Request</button>
                        </div>
                    </form>
                </div>
            </section>
        </div>
    </div>
    
    <!-- GALLERY PAGE (unchanged) -->
    <div class="page" id="gallery-page"><div class="container"><section class="gallery-section"><h2 class="section-title">Nail Gallery<span>✨ My Latest Creations ✨</span></h2>
        <div class="gallery-category"><h3 class="category-title">🎂 BIRTHDAY NAILS</h3><div class="gallery-slider-container"><div class="gallery-slider" id="birthday-slider"></div></div></div>
        <div class="gallery-category"><h3 class="category-title">💕 SIMPLE SETS</h3><div class="gallery-slider-container"><div class="gallery-slider" id="simple-slider"></div></div></div>
        <div class="gallery-category"><h3 class="category-title">🌸 SEASONAL SETS</h3><div class="gallery-slider-container"><div class="gallery-slider" id="seasonal-slider"></div></div></div>
        <div class="gallery-category"><h3 class="category-title">🦶 HANDS + TOES</h3><div class="gallery-slider-container"><div class="gallery-slider" id="handstoes-slider"></div></div></div>
        <div class="gallery-category"><h3 class="category-title">📦 PRESS-ONS</h3><div class="gallery-slider-container"><div class="gallery-slider" id="presson-slider"></div></div></div>
    </section></div></div>
    
    <!-- BOOKING PAGE (original nail booking form, untouched) -->
    <div class="page" id="booking-page"><section class="booking-hero"><div class="booking-content"><h1 class="booking-title">Book Your Appointment</h1><div class="booking-form-container"><form id="bookingForm"><div class="form-row"><div class="form-group"><label>First Name</label><input type="text" id="firstName" class="form-control" required></div><div class="form-group"><label>Last Name</label><input type="text" id="lastName" class="form-control" required></div></div><div class="form-row"><div class="form-group"><label>Phone</label><input type="tel" id="phone" class="form-control" placeholder="(786) 251-4782" required></div><div class="form-group"><label>Email</label><input type="email" id="email" class="form-control" placeholder="narajilove@gmail.com" required></div></div><div class="form-group"><label>Select Service</label><select id="service" class="form-control" required><option value="" disabled selected>Choose a service</option><option>Freestyle Full Set - $100</option><option>Acrylic Full Set - Short - $60</option><option>Acrylic Full Set - Medium - $70</option><option>Acrylic Full Set - Long - $80</option><option>Gel X Extensions - $80+</option><option>Ombre Full Set - $60-125</option><option>Gel Manicure - $50</option><option>Toe Service - $45-65</option><option>Custom Press-Ons - $110+</option><option>After Hours 9PM-11PM (+$40)</option><option>After Hours 12AM-2AM (+$60)</option><option>After Hours 2AM-4AM (+$80)</option><option>Soak Off Removal - $25</option></select></div><div class="form-row"><div class="form-group"><label>Preferred Date</label><input type="date" id="date" class="form-control" required></div><div class="form-group"><label>Preferred Time</label><select id="time" class="form-control" required><option value="" disabled selected>Select time</option><option>9:00 AM</option><option>10:00 AM</option><option>11:00 AM</option><option>12:00 PM</option><option>1:00 PM</option><option>2:00 PM</option><option>3:00 PM</option><option>4:00 PM</option><option>5:00 PM</option><option>6:00 PM</option><option>7:00 PM</option><option>8:00 PM</option><option>9:00 PM (After Hours +$40)</option><option>12:00 AM (After Hours +$60)</option><option>2:00 AM (After Hours +$80)</option></select></div></div><div class="form-group"><label>Notes / Inspiration</label><textarea id="notes" class="form-control" rows="4"></textarea></div><div class="form-submit"><button type="submit" class="submit-btn">Submit Booking Request</button></div></form><div style="margin-top:30px; text-align:center;"><p><strong>📌 Important:</strong> $25 deposit required. Confirmation within 24h. Cash/Zelle/CashApp accepted.</p></div></div></div></section></div>
    
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-brand">
                    <div class="footer-logo">NarajiRawcrylics</div>
                    <p>Luxury Beauty • Self-Care • Shea Butter</p>
                </div>
                <div class="footer-contact">
                    <h3>Contact</h3>
                    <ul class="contact-info">
                        <li><i class="fas fa-envelope"></i> narajilove@gmail.com</li>
                        <li><i class="fas fa-phone"></i> <span id="phoneNumberPlaceholder">(786) 251-4782</span></li>
                        <li><i class="fab fa-instagram"></i> @NarajiRawcrylics</li>
                        <li><i class="fab fa-instagram"></i> @NarajiRaworganic</li>
                    </ul>
                </div>
                <div class="footer-social">
                    <h3>Follow</h3>
                    <div class="social-icons">
                        <a href="https://instagram.com/narajirawcrylics" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="https://instagram.com/narajiraworganic" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="mailto:narajilove@gmail.com"><i class="fas fa-envelope"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">&copy; 2024 NarajiRawcrylics. All rights reserved. | Handcrafted with Shea butter love.</div>
        </div>
    </footer>
    
    <!-- Modal for both forms (reused) -->
    <div class="modal-overlay" id="confirmationModal"><div class="modal-content"><div class="modal-icon"><i class="fas fa-check-circle"></i></div><h2 class="modal-title" id="modalTitle">Request Sent!</h2><div class="modal-message" id="modalMessage"></div><button class="modal-btn" id="modalCloseBtn">Okay</button></div></div>

    <script>
        // All gallery images (same as before)
        const birthdayImages = [ 'https://i.postimg.cc/J7SvLG8F/Screenshot-2026-03-30-105319.png', 'https://i.postimg.cc/tCPfCpRf/Screenshot-2026-03-30-105341.png', 'https://i.postimg.cc/02m32P5H/Screenshot-2026-03-30-105415.png', 'https://i.postimg.cc/8PW3PNkY/Screenshot-2026-03-30-105424.png', 'https://i.postimg.cc/wTJPTgx4/Screenshot-2026-03-30-105433.png', 'https://i.postimg.cc/3Jp6JYJT/Screenshot-2026-03-30-105446.png', 'https://i.postimg.cc/bNbMNpNf/Screenshot-2026-03-30-105501.png', 'https://i.postimg.cc/3Jp6JYJH/Screenshot-2026-03-30-105516.png', 'https://i.postimg.cc/nc75cpcp/Screenshot-2026-03-30-105530.png', 'https://i.postimg.cc/bNbMNpNr/Screenshot-2026-03-30-105547.png', 'https://i.postimg.cc/3Jp6JYJR/Screenshot-2026-03-30-105602.png', 'https://i.postimg.cc/dVYfhpLJ/Screenshot-2026-03-30-105616.png', 'https://i.postimg.cc/Vk8hJpdY/Screenshot-2026-03-30-105632.png', 'https://i.postimg.cc/fRNPVpJk/Screenshot-2026-03-30-105648.png', 'https://i.postimg.cc/bwh5ZWss/Screenshot-2026-03-30-105706.png', 'https://i.postimg.cc/xTMfrwwQ/Screenshot-2026-03-30-110251.png', 'https://i.postimg.cc/CLkhy334/Screenshot-2026-03-30-110304.png', 'https://i.postimg.cc/tCWq0KKW/Screenshot-2026-03-30-110319.png', 'https://i.postimg.cc/02DkgTT0/Screenshot-2026-03-30-110330.png' ];
        const simpleImages = [ 'https://i.postimg.cc/brGv2dVZ/Screenshot-2026-03-30-110702.png', 'https://i.postimg.cc/sxB2Z1HH/Screenshot-2026-03-30-110717.png', 'https://i.postimg.cc/Bb8v1t7M/Screenshot-2026-03-30-110739.png', 'https://i.postimg.cc/T1yPWhNk/Screenshot-2026-03-30-110756.png', 'https://i.postimg.cc/5yHtFjKR/Screenshot-2026-03-30-110812.png', 'https://i.postimg.cc/NFWj8YZz/Screenshot-2026-03-30-110841.png', 'https://i.postimg.cc/Bbdn5sRw/Screenshot-2026-03-30-110857.png', 'https://i.postimg.cc/RhjZ192Y/Screenshot-2026-03-30-110913.png' ];
        const seasonalImages = [ 'https://i.postimg.cc/mDnHnv07/Screenshot-2026-03-30-111152.png', 'https://i.postimg.cc/F15JrjFr/Screenshot-2026-03-30-111208.png', 'https://i.postimg.cc/fy09QHs0/Screenshot-2026-03-30-111223.png', 'https://i.postimg.cc/J0BkCT8t/Screenshot-2026-03-30-111238.png', 'https://i.postimg.cc/6qGvxHK4/Screenshot-2026-03-30-111253.png', 'https://i.postimg.cc/c6y8xQ1D/Screenshot-2026-03-30-111315.png', 'https://i.postimg.cc/sfB62sDy/Screenshot-2026-03-30-111329.png', 'https://i.postimg.cc/c1K9J04x/Screenshot-2026-03-30-111345.png', 'https://i.postimg.cc/QNB4MhxC/Screenshot-2026-03-30-111402.png', 'https://i.postimg.cc/1RgCzs58/Screenshot-2026-03-30-111420.png', 'https://i.postimg.cc/kMV15qX8/Screenshot-2026-03-30-111434.png', 'https://i.postimg.cc/1RgCzs5w/Screenshot-2026-03-30-111448.png' ];
        const handstoeImages = [ 'https://i.postimg.cc/QM3GQVCP/Screenshot-2026-03-30-111941.png', 'https://i.postimg.cc/6QfsYwGX/Screenshot-2026-03-30-111954.png', 'https://i.postimg.cc/q7xfj069/Screenshot-2026-03-30-112012.png', 'https://i.postimg.cc/1zrxJPNS/Screenshot-2026-03-30-112028.png' ];
        const pressonImages = [ 'https://i.postimg.cc/D0dBKyn2/Screenshot-2026-03-30-112309.png', 'https://i.postimg.cc/8khyvwWm/Screenshot-2026-03-30-112324.png', 'https://i.postimg.cc/mkN8G2BH/Screenshot-2026-03-30-112340.png', 'https://i.postimg.cc/sfpnWKSK/Screenshot-2026-03-30-112351.png', 'https://i.postimg.cc/T2rkbQm7/Screenshot-2026-03-30-112405.png', 'https://i.postimg.cc/tRhr6DPf/Screenshot-2026-03-30-112421.png' ];
        
        const allImages = [...birthdayImages, ...simpleImages, ...seasonalImages, ...handstoeImages, ...pressonImages];
        
        function buildHomeSlideshow() {
            const track = document.getElementById('homeSlideshow');
            if (!track) return;
            track.innerHTML = '';
            const slides = [...allImages, ...allImages, ...allImages];
            slides.forEach((src, idx) => {
                const slideDiv = document.createElement('div');
                slideDiv.className = 'slide-item';
                const img = document.createElement('img');
                img.src = src;
                img.alt = `Nail art ${idx}`;
                img.loading = 'lazy';
                slideDiv.appendChild(img);
                track.appendChild(slideDiv);
            });
        }
        buildHomeSlideshow();
        
        function createSlider(id, arr) { const c = document.getElementById(id); if(!c) return; c.innerHTML=''; [...arr,...arr].forEach((src,i)=>{ let s=document.createElement('div'); s.className='gallery-slide'; let img=document.createElement('img'); img.src=src; img.alt='Nail art'; s.appendChild(img); c.appendChild(s); }); }
        createSlider('birthday-slider', birthdayImages); createSlider('simple-slider', simpleImages); createSlider('seasonal-slider', seasonalImages); createSlider('handstoes-slider', handstoeImages); createSlider('presson-slider', pressonImages);
        
        function createFallingDots(){ let cont=document.getElementById('fallingDots'); if(!cont) return; cont.innerHTML=''; let count=window.innerWidth<768?50:100; for(let i=0;i<count;i++){ let d=document.createElement('div'); d.className='dot'; let s=Math.random()*4+2; d.style.width=s+'px'; d.style.height=s+'px'; d.style.left=Math.random()*100+'%'; d.style.animationDelay=Math.random()*20+'s'; d.style.animationDuration=Math.random()*8+6+'s'; cont.appendChild(d); } }
        createFallingDots();
        
        // Dark mode toggle
        const darkModeToggle = document.getElementById('darkModeToggle');
        const darkModeIcon = darkModeToggle.querySelector('i');
        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
            const isDark = document.body.classList.contains('dark-mode');
            localStorage.setItem('narajiDarkMode', isDark);
            darkModeIcon.className = isDark ? 'fas fa-sun' : 'fas fa-moon';
        }
        const savedDarkMode = localStorage.getItem('narajiDarkMode');
        if (savedDarkMode === 'true') {
            document.body.classList.add('dark-mode');
            darkModeIcon.className = 'fas fa-sun';
        }
        darkModeToggle.addEventListener('click', toggleDarkMode);
        
        // Navigation (unchanged)
        const pages = { home: document.getElementById('home-page'), gallery: document.getElementById('gallery-page'), booking: document.getElementById('booking-page') };
        const navLinks = document.querySelectorAll('.nav-link');
        const logo = document.querySelector('.logo');
        const header = document.getElementById('main-header');
        const scrollTopBtn = document.getElementById('scrollTop');
        const modal = document.getElementById('confirmationModal');
        const modalMessage = document.getElementById('modalMessage');
        const modalTitle = document.getElementById('modalTitle');
        const modalClose = document.getElementById('modalCloseBtn');
        
        function switchPage(id){ Object.values(pages).forEach(p=>p.classList.remove('active')); pages[id].classList.add('active'); navLinks.forEach(l=>{ if(l.dataset.page===id) l.classList.add('active-page'); else l.classList.remove('active-page'); }); window.scrollTo(0,0); if(id==='booking'){ let today=new Date().toISOString().split('T')[0]; document.getElementById('date').min=today; let tom=new Date(); tom.setDate(tom.getDate()+1); document.getElementById('date').value=tom.toISOString().split('T')[0]; } history.pushState(null,'','#'+id); }
        navLinks.forEach(l=>l.addEventListener('click',(e)=>{ e.preventDefault(); switchPage(l.dataset.page); mobileMenu.classList.remove('active'); hamburger.classList.remove('active'); document.body.style.overflow='auto'; }));
        logo.addEventListener('click',()=>switchPage('home'));
        document.querySelectorAll('.btn[data-page]').forEach(b=>b.addEventListener('click',(e)=>{ e.preventDefault(); switchPage(b.dataset.page); mobileMenu.classList.remove('active'); hamburger.classList.remove('active'); }));
        
        const hamburger = document.getElementById('hamburger');
        const mobileMenu = document.getElementById('mobile-menu');
        hamburger.addEventListener('click',()=>{ mobileMenu.classList.toggle('active'); hamburger.classList.toggle('active'); document.body.style.overflow=mobileMenu.classList.contains('active')?'hidden':'auto'; });
        document.querySelectorAll('.mobile-links a, .mobile-menu-btn a').forEach(l=>l.addEventListener('click',()=>{ mobileMenu.classList.remove('active'); hamburger.classList.remove('active'); document.body.style.overflow='auto'; }));
        
        modalClose.addEventListener('click',()=>{ modal.classList.remove('active'); document.body.style.overflow='auto'; });
        
        // NAIL BOOKING FORM (original, unchanged)
        document.getElementById('bookingForm').addEventListener('submit',function(e){ e.preventDefault(); let fname=document.getElementById('firstName').value; let lname=document.getElementById('lastName').value; let phone=document.getElementById('phone').value; let email=document.getElementById('email').value; let svc=document.getElementById('service').options[document.getElementById('service').selectedIndex]?.text||''; let date=document.getElementById('date').value; let tm=document.getElementById('time').options[document.getElementById('time').selectedIndex]?.text||''; let notes=document.getElementById('notes').value; modalTitle.innerText = 'Booking Request Sent!'; modalMessage.innerText=`✨ Thank you, ${fname} ${lname}! ✨\n\n✅ Booking request received.\n\n📋 Details:\n• Service: ${svc}\n• Date: ${new Date(date).toLocaleDateString()}\n• Time: ${tm}\n• Contact: ${phone}, ${email}\n\n📝 Notes: ${notes||'None'}\n\n📍 Address sent 24h before\n\n💸 A $25 deposit secures your appointment.\n\nQuestions? (786) 251-4782 / narajilove@gmail.com`; modal.classList.add('active'); document.body.style.overflow='hidden'; this.reset(); let td=new Date().toISOString().split('T')[0]; document.getElementById('date').min=td; let tom=new Date(); tom.setDate(tom.getDate()+1); document.getElementById('date').value=tom.toISOString().split('T')[0]; });
        
        // SHEA BUTTER ORDER FORM (separate)
        document.getElementById('sheaOrderForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('sheaName').value;
            const email = document.getElementById('sheaEmail').value;
            const phone = document.getElementById('sheaPhone').value;
            const address = document.getElementById('sheaAddress').value;
            const sizeSelect = document.getElementById('sheaSize');
            const size = sizeSelect.options[sizeSelect.selectedIndex]?.text || '';
            const quantity = document.getElementById('sheaQuantity').value;
            const notes = document.getElementById('sheaNotes').value;
            
            let total = 0;
            if (size.includes('1 oz')) total = 5 * quantity;
            else if (size.includes('4 oz')) total = 15 * quantity;
            else if (size.includes('Two for $25')) total = 25 * Math.ceil(quantity/2);
            
            modalTitle.innerText = 'Shea Butter Order Received!';
            modalMessage.innerText = `🧈 Thank you, ${name}! 🧈\n\n✅ Your order request has been received.\n\n📦 Order Details:\n• Product: Coconut Vanilla Body Butter\n• Size: ${size}\n• Quantity: ${quantity}\n• Total: $${total}\n\n📍 Shipping to:\n${address}\n\n📞 Contact: ${phone}, ${email}\n📝 Notes: ${notes || 'None'}\n\n🚚 Shipping within 1 business day via USPS.\n\nYou will receive a confirmation email with payment instructions. For questions: narajilove@gmail.com or (786) 251-4782`;
            modal.classList.add('active');
            document.body.style.overflow = 'hidden';
            this.reset();
        });
        
        scrollTopBtn.addEventListener('click',()=>window.scrollTo(0,0));
        window.addEventListener('scroll',()=>{ if(window.scrollY>500) scrollTopBtn.classList.add('visible'); else scrollTopBtn.classList.remove('visible'); if(window.scrollY<50) header.classList.add('header-transparent'); else header.classList.remove('header-transparent'); });
        window.addEventListener('resize',()=>{ createSlider('birthday-slider', birthdayImages); createSlider('simple-slider', simpleImages); createSlider('seasonal-slider', seasonalImages); createSlider('handstoes-slider', handstoeImages); createSlider('presson-slider', pressonImages); buildHomeSlideshow(); let dots=document.getElementById('fallingDots'); if(dots){ dots.innerHTML=''; createFallingDots(); } });
        window.addEventListener('DOMContentLoaded',()=>{ createFallingDots(); buildHomeSlideshow(); let hash=location.hash.substring(1); if(hash&&pages[hash]) switchPage(hash); let td=new Date().toISOString().split('T')[0]; document.getElementById('date').min=td; header.classList.add('header-transparent'); });
        window.addEventListener('popstate',()=>{ let hash=location.hash.substring(1); if(hash&&pages[hash]) switchPage(hash); });
    </script>
</body>
</html>
