
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
            --dark-text: #2C2C2C;
            --medium-text: #5a5a5a;
            --heading-font: 'Playfair Display', serif;
            --accent-font: 'Great Vibes', cursive;
            --body-font: 'Inter', sans-serif;
            --header-height-desktop: 80px;
            --header-height-mobile: 70px;
            --border-radius: 24px;
            --border-radius-small: 16px;
        }
        
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: var(--body-font);
            background-color: #f5f0eb;
            color: var(--dark-text);
            line-height: 1.6;
            overflow-x: hidden;
            background-image: url('https://i.imgur.com/a/SX7nG5v');
            background-size: cover;
            background-attachment: fixed;
            background-position: center;
            position: relative;
        }
        .falling-dots { position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; z-index: 1; overflow: hidden; }
        .dot { position: absolute; background: rgba(255,255,255,0.6); border-radius: 50%; animation: fall linear infinite; }
        @keyframes fall { 0% { transform: translateY(-10vh) rotate(0deg); opacity: 0; } 10% { opacity: 0.6; } 90% { opacity: 0.6; } 100% { transform: translateY(110vh) rotate(360deg); opacity: 0; } }
        .container { width: 100%; max-width: 1200px; margin: 0 auto; padding: 0 24px; position: relative; z-index: 2; }
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0);
            background-size: 300% 300%;
            color: var(--dark-text);
            font-weight: 600;
            padding: 12px 28px;
            border-radius: 40px;
            transition: all 0.4s ease;
            border: none;
            cursor: pointer;
            animation: softShift 8s ease infinite;
        }
        @keyframes softShift { 0% { background-position: 0% 50%; } 50% { background-position: 100% 50%; } 100% { background-position: 0% 50%; } }
        .section-title {
            font-family: var(--accent-font);
            font-size: 3rem;
            text-align: center;
            margin-bottom: 2rem;
            position: relative;
            color: var(--dark-text);
        }
        .section-title span { display: block; font-family: var(--body-font); font-size: 0.85rem; color: var(--medium-text); letter-spacing: 2px; text-transform: uppercase; margin-top: 5px; }
        .page { display: none; animation: fadeIn 0.5s ease; }
        .page.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
        
        /* ========== LOCKED HEADER ========== */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255,255,255,0.98);
            backdrop-filter: blur(12px);
            height: var(--header-height-desktop);
            border-bottom: 1px solid rgba(255,183,178,0.3);
            transition: all 0.3s ease;
        }
        .header-transparent { background: rgba(255,255,255,0.85) !important; }
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
        .nav-links { display: flex; gap: 20px; list-style: none; }
        .nav-links a { font-weight: 500; color: var(--dark-text); font-size: 0.9rem; cursor: pointer; }
        .nav-links a.active-page { color: #FF9B8A; }
        .divider { width: 1px; height: 20px; background: linear-gradient(to bottom, transparent, var(--soft-pink), transparent); }
        .hamburger { display: none; flex-direction: column; gap: 5px; background: rgba(255,255,255,0.9); border: 1px solid rgba(255,183,178,0.3); padding: 10px; border-radius: 12px; cursor: pointer; width: 44px; height: 44px; }
        .hamburger span { width: 22px; height: 2px; background: var(--dark-text); transition: 0.3s; border-radius: 2px; }
        .mobile-menu { position: fixed; top: var(--header-height-mobile); left: 0; width: 100%; height: calc(100vh - var(--header-height-mobile)); background: rgba(255,255,255,0.98); backdrop-filter: blur(10px); transform: translateX(100%); opacity: 0; transition: 0.3s cubic-bezier(0.4,0,0.2,1); z-index: 999; pointer-events: none; overflow-y: auto; visibility: hidden; }
        .mobile-menu.active { transform: translateX(0); opacity: 1; pointer-events: all; visibility: visible; }
        .mobile-links { padding: 30px 20px; display: flex; flex-direction: column; gap: 15px; text-align: center; }
        .mobile-links li { background: rgba(255,255,255,0.6); border-radius: 16px; border: 1px solid rgba(255,183,178,0.2); }
        .mobile-links a { display: block; padding: 14px 20px; font-size: 1.2rem; font-weight: 500; color: var(--dark-text); }
        .mobile-menu-btn { padding: 25px 20px 35px; text-align: center; border-top: 1px solid rgba(0,0,0,0.05); }
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
        .hero-subtitle { font-family: var(--accent-font); font-size: clamp(1.2rem,4vw,2.2rem); margin-bottom: 30px; color: var(--medium-text); }
        
        /* Two-column layout helpers */
        .two-column { display: flex; flex-wrap: wrap; gap: 40px; align-items: center; }
        .two-column > div { flex: 1; min-width: 250px; }
        .side-image { border-radius: var(--border-radius); overflow: hidden; box-shadow: 0 8px 20px rgba(0,0,0,0.08); width: 100%; height: auto; }
        .side-image img { width: 100%; height: auto; display: block; object-fit: cover; }
        
        /* Existing component styles (kept intact) */
        .brand-card, .service-card, .hour-card, .price-category, .policy-item, .tech-content, .booking-form-container { background: rgba(255,255,255,0.88); backdrop-filter: blur(4px); border-radius: var(--border-radius); padding: 30px; border: 1px solid rgba(255,183,178,0.3); }
        .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px,1fr)); gap: 30px; margin-top: 40px; }
        .price-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px,1fr)); gap: 15px; }
        .price-item { background: rgba(255,255,255,0.7); padding: 12px 18px; border-radius: var(--border-radius-small); display: flex; justify-content: space-between; align-items: center; }
        .price-amount { color: #FF9B8A; font-weight: 600; }
        .gallery-slider-container { overflow: hidden; padding: 15px 0; }
        .gallery-slider { display: flex; gap: 20px; animation: scrollSoft 45s linear infinite; }
        .gallery-slider:hover { animation-play-state: paused; }
        .gallery-slide { flex: 0 0 auto; width: 260px; height: 260px; border-radius: var(--border-radius); overflow: hidden; box-shadow: 0 8px 20px rgba(0,0,0,0.08); }
        .gallery-slide img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.4s; }
        .gallery-slide:hover img { transform: scale(1.08); }
        @keyframes scrollSoft { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-280px * 6)); } }
        .category-title { font-family: var(--heading-font); font-size: 2rem; font-weight: 600; text-align: center; margin-bottom: 25px; }
        .form-control { width: 100%; padding: 14px 18px; border: 1px solid rgba(0,0,0,0.1); border-radius: 12px; background: white; }
        .submit-btn { background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF); background-size: 300% 300%; color: var(--dark-text); font-weight: 600; padding: 14px 45px; border-radius: 40px; border: none; cursor: pointer; animation: softShift 8s ease infinite; }
        footer { background: rgba(255,255,255,0.92); backdrop-filter: blur(8px); padding: 50px 0 30px; margin-top: 60px; border-top: 1px solid rgba(255,183,178,0.3); }
        .footer-container { display: flex; flex-wrap: wrap; justify-content: space-between; gap: 40px; }
        .scroll-top { position: fixed; bottom: 30px; right: 30px; width: 45px; height: 45px; background: linear-gradient(135deg, #FFB7B2, #E8D1FF); border-radius: 50%; display: flex; align-items: center; justify-content: center; cursor: pointer; opacity: 0; visibility: hidden; transition: 0.3s; z-index: 100; }
        .scroll-top.visible { opacity: 1; visibility: visible; }
        .modal-overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.5); backdrop-filter: blur(4px); display: flex; align-items: center; justify-content: center; z-index: 1100; opacity: 0; visibility: hidden; transition: 0.3s; }
        .modal-overlay.active { opacity: 1; visibility: visible; }
        .modal-content { background: white; border-radius: var(--border-radius); padding: 40px; max-width: 500px; width: 90%; text-align: center; }
        
        @media (max-width: 768px) {
            .nav-desktop { display: none; }
            .hamburger { display: flex; }
            .hero { padding-top: calc(var(--header-height-mobile) + 30px); }
            .two-column { flex-direction: column; }
            .category-title { font-size: 1.6rem; }
            .gallery-slide { width: 200px; height: 200px; }
            @keyframes scrollSoft { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-220px * 6)); } }
        }
        @media (max-width: 480px) {
            .gallery-slide { width: 160px; height: 160px; }
            @keyframes scrollSoft { 0% { transform: translateX(0); } 100% { transform: translateX(calc(-180px * 6)); } }
        }
    </style>
</head>
<body>
    <div class="falling-dots" id="fallingDots"></div>
    <div class="scroll-top" id="scrollTop"><i class="fas fa-chevron-up"></i></div>
    
    <header id="main-header">
        <div class="header-container">
            <div class="logo" data-page="home">NarajiRawcrylics</div>
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
            <button class="hamburger" id="hamburger" aria-label="Menu"><span></span><span></span><span></span></button>
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

    <!-- HOME PAGE -->
    <div class="page active" id="home-page">
        <section class="hero">
            <div class="hero-content">
                <h1 class="hero-title">NarajiRawcrylics</h1>
                <p class="hero-subtitle">Soft Rainbow Nail Studio</p>
                <a href="#" class="btn hero-btn" data-page="booking">Book Your Appointment</a>
            </div>
        </section>
        
        <div class="container">
            <!-- BRAND DESCRIPTION + IMAGE (two-column) -->
            <section class="brand-description">
                <div class="two-column">
                    <div>
                        <div class="brand-card">
                            <h2 class="brand-title" style="font-family: var(--accent-font); font-size: 2.5rem;">✨ Creativity. Precision. Detail. ✨</h2>
                            <p class="brand-text">NarajiRawcrylics is a nail brand built on creativity, precision, and detail. I specialize in acrylic sets, Gel X extensions, and custom press-on nails designed to elevate each client's personal style.<br><br>
                            Every set is crafted with intention, focusing on structure, longevity, and a flawless finish. My goal is to provide not just nails, but a luxury experience where clients feel confident, comfortable, and taken care of.<br><br>
                            As the brand grows, NarajiRawcrylics is expanding into natural beauty, including herbs and skincare products that promote self-care from the inside out. 💐💕</p>
                        </div>
                    </div>
                    <div class="side-image">
                        <img src="https://i.postimg.cc/fLHMqhg7/Screenshot-20260403-163502-Docs-2.jpg" alt="Brand inspiration">
                    </div>
                </div>
            </section>
            
            <!-- SERVICES SECTION (no changes) -->
            <section class="services">
                <h2 class="section-title">My Services<span>Luxury Nail Experiences</span></h2>
                <div class="services-grid">
                    <div class="service-card"><div class="service-icon"><i class="fas fa-hand-fist"></i></div><h3 class="service-title">Acrylic Sets</h3><p class="service-description">Traditional acrylic with strong structure and flawless finish.</p></div>
                    <div class="service-card"><div class="service-icon"><i class="fas fa-spa"></i></div><h3 class="service-title">Gel X Extensions</h3><p class="service-description">Lightweight, flexible gel extensions with natural feel and high shine.</p></div>
                    <div class="service-card"><div class="service-icon"><i class="fas fa-box"></i></div><h3 class="service-title">Custom Press-Ons</h3><p class="service-description">Handcrafted press‑ons using your custom sizing kit. <strong>Available any day!</strong> Order whenever you're ready.</p></div>
                </div>
            </section>
        </div>
        
        <!-- AFTER HOURS (unchanged) -->
        <section class="after-hours"><div class="container"><h2 class="section-title">After Hours Luxury<span>Private Late Night Experience</span></h2><div class="hours-grid"><div class="hour-card"><div class="hour-time">9PM - 11PM</div><div class="hour-price">+$40</div></div><div class="hour-card"><div class="hour-time">12AM - 2AM</div><div class="hour-price">+$60</div></div><div class="hour-card"><div class="hour-time">2AM - 4AM</div><div class="hour-price">+$80</div></div></div><p style="text-align:center; margin-top:20px;">✨ Exclusively available Tuesday-Thursday nights ✨</p></div></section>
        
        <div class="container">
            <!-- MEET YOUR NAIL TECH + IMAGE (two-column) -->
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
                            Beyond nails, I am also growing NarajiRawOrganics - a natural beauty extension of my brand focused on herbs and skincare that support self-care and overall wellness. 💐💕</p>
                            <div class="tech-quote" style="font-family: var(--accent-font); font-size: 1.5rem; color: #FF9B8A; margin-top: 30px; padding: 20px; background: rgba(255,183,178,0.15); border-radius: var(--border-radius); text-align: center;">"Freestyle sets may include nail art, stones, and custom designs. Each set is one of one ✨"</div>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- PRICE LIST (updated with French tip offer) -->
            <section class="price-list">
                <h2 class="section-title">Price List<span>Investment in Beauty</span></h2>
                <div class="price-category"><h3 class="price-category-title">✨ Signature Freestyle</h3><div class="price-grid"><div class="price-item"><span>Freestyle Full Set</span><span class="price-amount">$100</span></div></div><p style="font-size:0.85rem;">*All lengths except XL. Full creative control – trust the artist's vision*</p></div>
                <div class="price-category"><h3 class="price-category-title">💅 Full Sets</h3><div class="price-grid"><div class="price-item"><span>Super Short</span><span class="price-amount">$50</span></div><div class="price-item"><span>Short</span><span class="price-amount">$60</span
