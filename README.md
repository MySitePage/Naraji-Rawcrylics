
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NarajiRawcrylics | Soft Rainbow Nail Studio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Great+Vibes&family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            /* SOFT PASTEL RAINBOW COLORS - fluffy, not neon */
            --soft-pink: #FFB7B2;
            --soft-lavender: #E8D1FF;
            --soft-mint: #B5F0E6;
            --soft-peach: #FFD6A5;
            --soft-blue: #A0C4FF;
            --soft-butter: #FDFFB0;
            --soft-rose: #F7C6C6;
            
            /* Gradients */
            --rainbow-soft: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0, #FFB7B2);
            --rainbow-soft-horizontal: linear-gradient(90deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0, #FFB7B2);
            
            /* Background */
            --marble-bg: url('https://i.imgur.com/a/SX7nG5v');
            
            --dark-text: #2C2C2C;
            --medium-text: #5a5a5a;
            --light-text: #ffffff;
            --glass-white: rgba(255, 255, 255, 0.88);
            --glass-white-blur: rgba(255, 255, 255, 0.7);
            
            /* Fonts */
            --heading-font: 'Playfair Display', serif;
            --accent-font: 'Great Vibes', cursive;
            --body-font: 'Inter', sans-serif;
            
            /* Spacing */
            --header-height-desktop: 85px;
            --header-height-mobile: 70px;
            --border-radius: 24px;
            --border-radius-small: 16px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
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
        
        /* FALLING WHITE DOTS ANIMATION */
        .falling-dots {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
            overflow: hidden;
        }
        
        .dot {
            position: absolute;
            background: rgba(255, 255, 255, 0.6);
            border-radius: 50%;
            pointer-events: none;
            animation: fall linear infinite;
        }
        
        @keyframes fall {
            0% {
                transform: translateY(-10vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.6;
            }
            90% {
                opacity: 0.6;
            }
            100% {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Glass/Frosted Panel Effect */
        .glass-panel {
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(2px);
            border-radius: var(--border-radius);
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.05);
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
            position: relative;
            z-index: 2;
        }
        
        /* Soft Rainbow Text Effect */
        .rainbow-text {
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0);
            background-size: 300% 300%;
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            animation: softShift 8s ease infinite;
        }
        
        @keyframes softShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Soft Rainbow Button */
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0);
            background-size: 300% 300%;
            color: var(--dark-text);
            font-family: var(--body-font);
            font-weight: 600;
            padding: 12px 28px;
            border-radius: 40px;
            transition: all 0.4s ease;
            border: none;
            cursor: pointer;
            font-size: 15px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
            position: relative;
            overflow: hidden;
            animation: softShift 8s ease infinite;
        }
        
        .btn:hover {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
        }
        
        /* Section Titles */
        .section-title {
            font-family: var(--accent-font);
            font-weight: 400;
            font-size: 3rem;
            text-align: center;
            margin-bottom: 2rem;
            position: relative;
            color: var(--dark-text);
        }
        
        .section-title::before,
        .section-title::after {
            content: '🌸';
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            font-size: 1.5rem;
            opacity: 0.6;
        }
        
        .section-title::before {
            left: -40px;
        }
        
        .section-title::after {
            right: -40px;
        }
        
        .section-title span {
            display: block;
            font-family: var(--body-font);
            font-size: 0.85rem;
            font-weight: 400;
            color: var(--medium-text);
            margin-top: 5px;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
        
        /* Page Transitions */
        .page {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .page.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Header */
        header {
            position: sticky;
            top: 0;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            height: var(--header-height-desktop);
            border-bottom: 1px solid rgba(255, 183, 178, 0.3);
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.03);
            transition: all 0.4s ease;
            width: 100%;
        }
        
        .header-transparent {
            background: rgba(255, 255, 255, 0.85) !important;
            backdrop-filter: blur(12px);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            padding: 0 30px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Logo */
        .logo {
            font-family: var(--accent-font);
            font-weight: 400;
            font-size: 2.2rem;
            color: var(--dark-text);
            transition: all 0.3s ease;
            cursor: pointer;
            white-space: nowrap;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6);
            background-size: 200% 200%;
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        
        .logo:hover {
            transform: scale(1.02);
        }
        
        /* Desktop Navigation */
        .nav-desktop {
            display: flex;
            align-items: center;
            gap: 30px;
        }
        
        .nav-center {
            display: flex;
            align-items: center;
            gap: 30px;
            padding: 6px 20px;
            background: rgba(255, 255, 255, 0.6);
            border-radius: 40px;
            backdrop-filter: blur(4px);
        }
        
        .divider {
            width: 1px;
            height: 20px;
            background: linear-gradient(to bottom, transparent, var(--soft-pink), transparent);
        }
        
        .nav-links {
            display: flex;
            gap: 25px;
            list-style: none;
        }
        
        .nav-links a {
            font-family: var(--body-font);
            font-weight: 500;
            color: var(--dark-text);
            position: relative;
            transition: all 0.3s ease;
            cursor: pointer;
            font-size: 0.95rem;
        }
        
        .nav-links a.active-page {
            color: #FF9B8A;
            font-weight: 600;
        }
        
        .nav-links a:hover {
            color: #FF9B8A;
        }
        
        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -4px;
            left: 0;
            background: linear-gradient(90deg, var(--soft-pink), var(--soft-lavender));
            border-radius: 2px;
            transition: width 0.3s ease;
        }
        
        .nav-links a:hover:after,
        .nav-links a.active-page:after {
            width: 100%;
        }
        
        /* Mobile Navigation */
        .hamburger {
            display: none;
            flex-direction: column;
            gap: 5px;
            background: rgba(255, 255, 255, 0.8);
            border: none;
            cursor: pointer;
            padding: 10px;
            border-radius: 12px;
        }
        
        .hamburger span {
            display: block;
            width: 22px;
            height: 2px;
            background-color: var(--dark-text);
            transition: all 0.3s ease;
            border-radius: 2px;
        }
        
        .mobile-menu {
            position: fixed;
            top: var(--header-height-mobile);
            left: 0;
            width: 100%;
            height: calc(100vh - var(--header-height-mobile));
            background: rgba(255, 255, 255, 0.98);
            transform: translateY(-100%);
            opacity: 0;
            transition: all 0.4s ease;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            z-index: 999;
            pointer-events: none;
            overflow-y: auto;
        }
        
        .mobile-menu.active {
            transform: translateY(0);
            opacity: 1;
            pointer-events: all;
        }
        
        .mobile-links {
            list-style: none;
            padding: 40px 20px;
            display: flex;
            flex-direction: column;
            gap: 20px;
            text-align: center;
        }
        
        .mobile-links a {
            font-family: var(--body-font);
            font-size: 1.3rem;
            color: var(--dark-text);
            display: block;
            padding: 12px;
        }
        
        .mobile-links a.active-page {
            color: #FF9B8A;
            font-weight: 600;
        }
        
        .mobile-menu-btn {
            padding: 30px 20px;
            text-align: center;
            border-top: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        /* Hero Section with your image */
        .hero {
            min-height: 90vh;
            background-image: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), url('https://i.postimg.cc/gjPtGJJG/Screenshot_2026_03_24_094423.png');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            margin-top: calc(-1 * var(--header-height-desktop));
            padding: 100px 0;
            text-align: center;
        }
        
        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: 0 20px;
        }
        
        .hero-title {
            font-family: var(--accent-font);
            font-size: clamp(3rem, 8vw, 5rem);
            margin-bottom: 15px;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF, #FDFFB0);
            background-size: 300% 300%;
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            animation: softShift 8s ease infinite;
        }
        
        .hero-subtitle {
            font-family: var(--accent-font);
            font-size: clamp(1.5rem, 4vw, 2.2rem);
            margin-bottom: 30px;
            color: var(--medium-text);
        }
        
        /* Brand Description Card */
        .brand-description {
            padding: 60px 0;
        }
        
        .brand-card {
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(4px);
            border-radius: var(--border-radius);
            padding: 40px;
            text-align: center;
            border: 1px solid rgba(255, 183, 178, 0.3);
        }
        
        .brand-title {
            font-family: var(--accent-font);
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--dark-text);
        }
        
        .brand-text {
            font-size: 1rem;
            line-height: 1.7;
            color: var(--medium-text);
            max-width: 800px;
            margin: 0 auto;
        }
        
        /* Services Grid */
        .services {
            padding: 60px 0;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .service-card {
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(4px);
            border-radius: var(--border-radius);
            padding: 35px 25px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 183, 178, 0.2);
        }
        
        .service-card:hover {
            transform: translateY(-8px);
            border-color: var(--soft-pink);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.05);
        }
        
        .service-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            display: inline-block;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        
        .service-title {
            font-family: var(--heading-font);
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--dark-text);
        }
        
        .service-description {
            font-size: 0.9rem;
            color: var(--medium-text);
            line-height: 1.6;
        }
        
        /* After Hours */
        .after-hours {
            padding: 60px 0;
            background: rgba(255, 248, 245, 0.7);
            backdrop-filter: blur(4px);
        }
        
        .hours-grid {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            margin-top: 30px;
        }
        
        .hour-card {
            background: rgba(255, 255, 255, 0.9);
            padding: 25px 35px;
            border-radius: var(--border-radius);
            text-align: center;
            border: 1px solid rgba(255, 183, 178, 0.3);
        }
        
        .hour-time {
            font-family: var(--heading-font);
            font-size: 1.4rem;
            font-weight: 600;
            color: var(--dark-text);
        }
        
        .hour-price {
            font-size: 1.1rem;
            color: #FF9B8A;
            margin-top: 8px;
            font-weight: 500;
        }
        
        /* Price List */
        .price-list {
            padding: 60px 0;
        }
        
        .price-category {
            margin-bottom: 50px;
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(4px);
            border-radius: var(--border-radius);
            padding: 30px;
        }
        
        .price-category-title {
            font-family: var(--accent-font);
            font-size: 2rem;
            margin-bottom: 25px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--soft-pink);
            display: inline-block;
            color: var(--dark-text);
        }
        
        .price-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 15px;
        }
        
        .price-item {
            background: rgba(255, 255, 255, 0.7);
            padding: 12px 18px;
            border-radius: var(--border-radius-small);
            display: flex;
            justify-content: space-between;
            align-items: center;
            border: 1px solid rgba(0, 0, 0, 0.03);
        }
        
        .price-name {
            font-weight: 500;
            color: var(--dark-text);
        }
        
        .price-amount {
            color: #FF9B8A;
            font-weight: 600;
        }
        
        /* Gallery Section */
        .gallery-section {
            padding: 60px 0;
        }
        
        .gallery-category {
            margin-bottom: 60px;
        }
        
        /* CHANGED: Gallery category titles to Playfair Display (clean serif font) */
        .category-title {
            font-family: var(--heading-font);
            font-size: 2rem;
            font-weight: 600;
            text-align: center;
            margin-bottom: 25px;
            color: var(--dark-text);
            letter-spacing: 1px;
        }
        
        .gallery-slider-container {
            position: relative;
            width: 100%;
            overflow: hidden;
            padding: 15px 0;
        }
        
        .gallery-slider {
            display: flex;
            gap: 20px;
            animation: scrollSoft 45s linear infinite;
        }
        
        .gallery-slider:hover {
            animation-play-state: paused;
        }
        
        .gallery-slide {
            flex: 0 0 auto;
            width: 260px;
            height: 260px;
            border-radius: var(--border-radius);
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
        }
        
        .gallery-slide:hover {
            transform: scale(1.03);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.12);
        }
        
        .gallery-slide img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s ease;
        }
        
        .gallery-slide:hover img {
            transform: scale(1.08);
        }
        
        @keyframes scrollSoft {
            0% { transform: translateX(0); }
            100% { transform: translateX(calc(-280px * 6)); }
        }
        
        /* Meet the Tech */
        .meet-tech {
            padding: 60px 0;
            background: rgba(255, 248, 245, 0.6);
            backdrop-filter: blur(4px);
        }
        
        .tech-container {
            display: flex;
            flex-wrap: wrap;
            gap: 50px;
            align-items: flex-start;
        }
        
        .tech-content {
            flex: 1;
            background: rgba(255, 255, 255, 0.85);
            padding: 40px;
            border-radius: var(--border-radius);
        }
        
        .tech-name {
            font-family: var(--accent-font);
            font-size: 2.5rem;
            margin-bottom: 20px;
            color: var(--dark-text);
        }
        
        .tech-bio {
            font-size: 0.95rem;
            line-height: 1.7;
            color: var(--medium-text);
        }
        
        .tech-quote {
            font-family: var(--accent-font);
            font-size: 1.5rem;
            color: #FF9B8A;
            margin-top: 30px;
            padding: 20px;
            background: rgba(255, 183, 178, 0.15);
            border-radius: var(--border-radius);
            text-align: center;
        }
        
        /* Policies */
        .policies {
            padding: 60px 0;
        }
        
        .policies-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .policy-item {
            background: rgba(255, 255, 255, 0.88);
            backdrop-filter: blur(4px);
            border-radius: var(--border-radius);
            padding: 25px;
            margin-bottom: 20px;
            border-left: 4px solid var(--soft-pink);
            transition: all 0.3s ease;
        }
        
        .policy-item:hover {
            transform: translateX(8px);
            background: rgba(255, 255, 255, 0.95);
        }
        
        .policy-title {
            font-family: var(--heading-font);
            font-size: 1.3rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 12px;
            color: var(--dark-text);
        }
        
        .policy-title i {
            color: #FF9B8A;
            font-size: 1.3rem;
        }
        
        .policy-text {
            font-size: 0.9rem;
            color: var(--medium-text);
            line-height: 1.6;
        }
        
        /* Booking Page */
        .booking-hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-top: calc(-1 * var(--header-height-desktop));
            padding: 100px 0;
        }
        
        .booking-content {
            max-width: 900px;
            width: 100%;
            padding: 0 20px;
        }
        
        .booking-title {
            font-family: var(--accent-font);
            font-size: clamp(2rem, 6vw, 3.5rem);
            text-align: center;
            margin-bottom: 40px;
            color: var(--dark-text);
        }
        
        .booking-form-container {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(8px);
            border-radius: var(--border-radius);
            padding: 40px;
            border: 1px solid rgba(255, 183, 178, 0.3);
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-label {
            display: block;
            font-weight: 500;
            margin-bottom: 8px;
            color: var(--dark-text);
        }
        
        .form-control {
            width: 100%;
            padding: 14px 18px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            border-radius: 12px;
            background: white;
            font-family: var(--body-font);
            font-size: 0.95rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--soft-pink);
            box-shadow: 0 0 0 3px rgba(255, 183, 178, 0.2);
        }
        
        select.form-control {
            appearance: none;
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='14' height='14' viewBox='0 0 24 24' fill='none' stroke='%23FF9B8A' stroke-width='2'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");
            background-repeat: no-repeat;
            background-position: right 18px center;
        }
        
        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .form-row .form-group {
            flex: 1 1 250px;
        }
        
        .form-submit {
            text-align: center;
            margin-top: 35px;
        }
        
        .submit-btn {
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6, #FFD6A5, #A0C4FF);
            background-size: 300% 300%;
            color: var(--dark-text);
            font-family: var(--body-font);
            font-size: 1.1rem;
            font-weight: 600;
            padding: 14px 45px;
            border-radius: 40px;
            border: none;
            cursor: pointer;
            animation: softShift 8s ease infinite;
            transition: all 0.3s ease;
        }
        
        .submit-btn:hover {
            transform: scale(1.02);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
        }
        
        /* Footer */
        footer {
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(8px);
            padding: 50px 0 30px;
            margin-top: 60px;
            border-top: 1px solid rgba(255, 183, 178, 0.3);
        }
        
        .footer-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 40px;
        }
        
        .footer-brand, .footer-contact, .footer-social {
            flex: 1 1 250px;
        }
        
        .footer-logo {
            font-family: var(--accent-font);
            font-size: 1.8rem;
            margin-bottom: 15px;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF, #B5F0E6);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            display: inline-block;
        }
        
        .footer-brand p {
            font-size: 0.85rem;
            color: var(--medium-text);
        }
        
        .footer-contact h3, .footer-social h3 {
            font-family: var(--heading-font);
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: var(--dark-text);
        }
        
        .contact-info {
            list-style: none;
        }
        
        .contact-info li {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 12px;
            font-size: 0.9rem;
            color: var(--medium-text);
        }
        
        .contact-info i {
            color: #FF9B8A;
            width: 22px;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 183, 178, 0.2);
            border-radius: 50%;
            transition: all 0.3s ease;
            color: var(--dark-text);
        }
        
        .social-icons a:hover {
            background: var(--soft-pink);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(0, 0, 0, 0.05);
            font-size: 0.8rem;
            color: var(--medium-text);
        }
        
        /* Scroll Top Button */
        .scroll-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 45px;
            height: 45px;
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }
        
        .scroll-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        .scroll-top:hover {
            transform: translateY(-5px);
        }
        
        .scroll-top i {
            color: var(--dark-text);
            font-size: 1rem;
        }
        
        /* Modal */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(4px);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1100;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }
        
        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }
        
        .modal-content {
            background: white;
            border-radius: var(--border-radius);
            padding: 40px;
            max-width: 500px;
            width: 90%;
            text-align: center;
        }
        
        .modal-icon {
            font-size: 3rem;
            color: var(--soft-pink);
            margin-bottom: 20px;
        }
        
        .modal-title {
            font-family: var(--accent-font);
            font-size: 2rem;
            margin-bottom: 15px;
        }
        
        .modal-message {
            color: var(--medium-text);
            margin-bottom: 25px;
            white-space: pre-line;
            font-size: 0.9rem;
        }
        
        .modal-btn {
            background: linear-gradient(135deg, #FFB7B2, #E8D1FF);
            border: none;
            padding: 12px 30px;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 500;
        }
        
        /* Responsive */
        @media screen and (max-width: 1024px) {
            .section-title::before,
            .section-title::after {
                display: none;
            }
            .container {
                padding: 0 20px;
            }
        }
        
        @media screen and (max-width: 768px) {
            .nav-desktop { display: none; }
            .hamburger { display: flex; }
            .logo { font-size: 1.6rem; }
            .section-title { font-size: 2.2rem; }
            .price-grid { grid-template-columns: 1fr; }
            .gallery-slide { width: 200px; height: 200px; }
            @keyframes scrollSoft {
                0% { transform: translateX(0); }
                100% { transform: translateX(calc(-220px * 6)); }
            }
            .tech-container { flex-direction: column; }
            .footer-container { flex-direction: column; text-align: center; }
            .contact-info li { justify-content: center; }
            .social-icons { justify-content: center; }
            .category-title { font-size: 1.6rem; }
        }
        
        @media screen and (max-width: 480px) {
            .hero-title { font-size: 2.5rem; }
            .hero-subtitle { font-size: 1.3rem; }
            .brand-title { font-size: 1.8rem; }
            .tech-name { font-size: 1.8rem; }
            .gallery-slide { width: 160px; height: 160px; }
            @keyframes scrollSoft {
                0% { transform: translateX(0); }
                100% { transform: translateX(calc(-180px * 6)); }
            }
            .booking-form-container { padding: 25px; }
            .category-title { font-size: 1.4rem; }
        }
        
        @media (prefers-reduced-motion: reduce) {
            * { animation-duration: 0.01ms !important; }
            .gallery-slider { animation: none; }
            .falling-dots { display: none; }
        }
    </style>
</head>
<body>
    <!-- FALLING WHITE DOTS -->
    <div class="falling-dots" id="fallingDots"></div>
    
    <div class="scroll-top" id="scrollTop">
        <i class="fas fa-chevron-up"></i>
    </div>
    
    <header id="main-header">
        <div class="header-container">
            <div class="logo" data-page="home">NarajiRawcrylics</div>
            
            <div class="nav-desktop">
                <div class="nav-center">
                    <nav>
                        <ul class="nav-links">
                            <li><a href="#" class="nav-link active-page" data-page="home">Home</a></li>
                            <li><a href="#" class="nav-link" data-page="gallery">Gallery</a></li>
                            <li><a href="#" class="nav-link" data-page="booking">Booking</a></li>
                        </ul>
                    </nav>
                    <div class="divider"></div>
                    <a href="#" class="btn" data-page="booking">Book Now</a>
                </div>
            </div>
            
            <button class="hamburger" id="hamburger">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
        
        <div class="mobile-menu" id="mobile-menu">
            <ul class="mobile-links">
                <li><a href="#" class="nav-link active-page" data-page="home">Home</a></li>
                <li><a href="#" class="nav-link" data-page="gallery">Gallery</a></li>
                <li><a href="#" class="nav-link" data-page="booking">Booking</a></li>
            </ul>
            <div class="mobile-menu-btn">
                <a href="#" class="btn" data-page="booking">Book Now</a>
            </div>
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
            <!-- Brand Description -->
            <section class="brand-description">
                <div class="brand-card">
                    <h2 class="brand-title">✨ Creativity. Precision. Detail. ✨</h2>
                    <p class="brand-text">NarajiRawcrylics is a nail brand built on creativity, precision, and detail. I specialize in acrylic sets, Gel X extensions, and custom press-on nails designed to elevate each client's personal style.<br><br>
                    Every set is crafted with intention, focusing on structure, longevity, and a flawless finish. My goal is to provide not just nails, but a luxury experience where clients feel confident, comfortable, and taken care of.<br><br>
                    As the brand grows, NarajiRawcrylics is expanding into natural beauty, including herbs and skincare products that promote self-care from the inside out. 💐💕</p>
                </div>
            </section>
            
            <!-- Services -->
            <section class="services">
                <h2 class="section-title">My Services<span>Luxury Nail Experiences</span></h2>
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon"><i class="fas fa-hand-fist"></i></div>
                        <h3 class="service-title">Acrylic Sets</h3>
                        <p class="service-description">Traditional acrylic with strong structure and flawless finish. Perfect for bold, long-lasting looks.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon"><i class="fas fa-spa"></i></div>
                        <h3 class="service-title">Gel X Extensions</h3>
                        <p class="service-description">Lightweight, flexible gel extensions with natural feel and high-shine finish.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon"><i class="fas fa-box"></i></div>
                        <h3 class="service-title">Custom Press-Ons</h3>
                        <p class="service-description">Handcrafted press-on sets designed for perfect fit using your custom sizing kit.</p>
                    </div>
                </div>
            </section>
        </div>
        
        <!-- After Hours Luxury -->
        <section class="after-hours">
            <div class="container">
                <h2 class="section-title">After Hours Luxury<span>Private Late Night Experience</span></h2>
                <div class="hours-grid">
                    <div class="hour-card">
                        <div class="hour-time">9PM - 11PM</div>
                        <div class="hour-price">+$40</div>
                    </div>
                    <div class="hour-card">
                        <div class="hour-time">12AM - 2AM</div>
                        <div class="hour-price">+$60</div>
                    </div>
                    <div class="hour-card">
                        <div class="hour-time">2AM - 4AM</div>
                        <div class="hour-price">+$80</div>
                    </div>
                </div>
                <p style="text-align: center; margin-top: 20px; color: var(--medium-text);">✨ Exclusively available Tuesday-Thursday nights ✨</p>
            </div>
        </section>
        
        <div class="container">
            <!-- Meet Your Nail Tech -->
            <section class="meet-tech">
                <div class="tech-container">
                    <div class="tech-content">
                        <h2 class="tech-name">Meet Your Nail Tech - NARAJI</h2>
                        <p class="tech-bio">Hi, I'm the nail tech behind the nail drill. NarajiRawcrylics is the brand but you can call me Raw. With a true passion for art, creativity, and self-expression, I've been helping clients feel confident through beautifully crafted nails.<br><br>
                        I specialize in acrylic sets, Gel X extensions, and custom press-on nails designed to match each client's personal style. Every set is created with care, precision, and attention to detail.<br><br>
                        My goal is to provide quality work and a comfortable, luxury experience so every client leaves feeling confident, happy, and in love with their nails.<br><br>
                        Beyond nails, I am also growing NarajiRawOrganics - a natural beauty extension of my brand focused on herbs and skincare that support self-care and overall wellness. This allows me to care for my clients not only through beauty, but from the inside out. 💐💕</p>
                        <div class="tech-quote">"Freestyle sets may include nail art, stones, and custom designs. Each set is one of one ✨"</div>
                    </div>
                </div>
            </section>
            
            <!-- Price List -->
            <section class="price-list">
                <h2 class="section-title">Price List<span>Investment in Beauty</span></h2>
                
                <div class="price-category">
                    <h3 class="price-category-title">✨ Signature Freestyle</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">Freestyle Full Set</span><span class="price-amount">$100</span></div>
                    </div>
                    <p style="color: var(--medium-text); margin-top: 10px; font-size: 0.85rem;">*All lengths included except XL. Full creative control - trust the artist's vision*</p>
                </div>
                
                <div class="price-category">
                    <h3 class="price-category-title">💅 Full Sets</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">Super Short</span><span class="price-amount">$50</span></div>
                        <div class="price-item"><span class="price-name">Short</span><span class="price-amount">$60</span></div>
                        <div class="price-item"><span class="price-name">Medium</span><span class="price-amount">$70</span></div>
                        <div class="price-item"><span class="price-name">Long</span><span class="price-amount">$80</span></div>
                        <div class="price-item"><span class="price-name">XL</span><span class="price-amount">$90</span></div>
                        <div class="price-item"><span class="price-name">XXL</span><span class="price-amount">$100</span></div>
                        <div class="price-item"><span class="price-name">Multi-shape (per nail)</span><span class="price-amount">+$3</span></div>
                    </div>
                </div>
                
                <div class="price-category">
                    <h3 class="price-category-title">🌈 Ombre Full Sets</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">Super Short</span><span class="price-amount">$60</span></div>
                        <div class="price-item"><span class="price-name">Short</span><span class="price-amount">$70</span></div>
                        <div class="price-item"><span class="price-name">Medium</span><span class="price-amount">$80</span></div>
                        <div class="price-item"><span class="price-name">Long</span><span class="price-amount">$90</span></div>
                        <div class="price-item"><span class="price-name">XL</span><span class="price-amount">$110</span></div>
                        <div class="price-item"><span class="price-name">XXL</span><span class="price-amount">$125</span></div>
                    </div>
                </div>
                
                <div class="price-category">
                    <h3 class="price-category-title">💖 Gel Services</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">Gel Manicure</span><span class="price-amount">$50</span></div>
                        <div class="price-item"><span class="price-name">Gel Polish Change</span><span class="price-amount">$30</span></div>
                    </div>
                </div>
                
                <div class="price-category">
                    <h3 class="price-category-title">🦶 Toe Services</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">Acrylic Big Toe</span><span class="price-amount">$10</span></div>
                        <div class="price-item"><span class="price-name">Full Set Acrylic Toes</span><span class="price-amount">$45-60</span></div>
                        <div class="price-item"><span class="price-name">Polygel Big Toe</span><span class="price-amount">$15</span></div>
                        <div class="price-item"><span class="price-name">Full Set Polygel Toes</span><span class="price-amount">$55-65</span></div>
                    </div>
                </div>
                
                <div class="price-category">
                    <h3 class="price-category-title">📦 Press-On Sets</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">Sizing Kit</span><span class="price-amount">$10</span></div>
                        <div class="price-item"><span class="price-name">Toes + Hands Sizing Kit</span><span class="price-amount">$16</span></div>
                        <div class="price-item"><span class="price-name">Freestyle Press-Ons</span><span class="price-amount">$110</span></div>
                        <div class="price-item"><span class="price-name">Freestyle Press-Ons (Luxury)</span><span class="price-amount">$130</span></div>
                    </div>
                </div>
                
                <div class="price-category">
                    <h3 class="price-category-title">🎨 Add-Ons</h3>
                    <div class="price-grid">
                        <div class="price-item"><span class="price-name">French (per nail)</span><span class="price-amount">+$5</span></div>
                        <div class="price-item"><span class="price-name">Gel French (Full Set)</span><span class="price-amount">+$25</span></div>
                        <div class="price-item"><span class="price-name">Encapsulation (per nail)</span><span class="price-amount">+$7</span></div>
                        <div class="price-item"><span class="price-name">Cuticle Stones (per nail)</span><span class="price-amount">+$3</span></div>
                        <div class="price-item"><span class="price-name">Cluster Stones (per nail)</span><span class="price-amount">+$10</span></div>
                        <div class="price-item"><span class="price-name">3D Art (per nail)</span><span class="price-amount">+$12</span></div>
                        <div class="price-item"><span class="price-name">Basic Nail Art</span><span class="price-amount">+$8</span></div>
                        <div class="price-item"><span class="price-name">Nail Piercing (per nail)</span><span class="price-amount">+$3</span></div>
                        <div class="price-item"><span class="price-name">Marble (10 fingers)</span><span class="price-amount">+$15</span></div>
                        <div class="price-item"><span class="price-name">Soak Off</span><span class="price-amount">$25</span></div>
                        <div class="price-item"><span class="price-name">Soak Off (Not My Work)</span><span class="price-amount">$30</span></div>
                    </div>
                </div>
            </section>
            
            <!-- Policies -->
            <section class="policies">
                <div class="policies-container">
                    <h2 class="section-title">Booking Policies<span>Important Information</span></h2>
                    
                    <div class="policy-item">
                        <h3 class="policy-title"><i class="fas fa-money-bill-wave"></i> Deposit Required</h3>
                        <p class="policy-text">A $25 deposit is required to secure all appointments. Deposits go toward the total cost of the service and are non-refundable.</p>
                    </div>
                    
                    <div class="policy-item">
                        <h3 class="policy-title"><i class="fas fa-clock"></i> Late Policy</h3>
                        <p class="policy-text">Please arrive on time for your appointment. Clients arriving more than 10 minutes late may need to reschedule depending on availability.</p>
                    </div>
                    
                    <div class="policy-item">
                        <h3 class="policy-title"><i class="fas fa-calendar-times"></i> No Call, No Show</h3>
                        <p class="policy-text">No call and no show appointments will require a new deposit before booking again.</p>
                    </div>
                    
                    <div class="policy-item">
                        <h3 class="policy-title"><i class="fas fa-calendar-alt"></i> Rescheduling</h3>
                        <p class="policy-text">If you need to reschedule, please notify at least 24 hours before your appointment time. Deposits may be transferred one time when rescheduling within this timeframe.</p>
                    </div>
                    
                    <div class="policy-item">
                        <h3 class="policy-title"><i class="fas fa-hand-peace"></i> Preparation</h3>
                        <p class="policy-text">Please arrive with bare nails unless a removal service was booked. No extra guests allowed unless approved. Addressing will be provided 24 hours before service.</p>
                    </div>
                    
                    <div class="policy-item">
                        <h3 class="policy-title"><i class="fas fa-credit-card"></i> Payment</h3>
                        <p class="policy-text">Cash only preferred. If cash not on hand, payment of Zelle or Cash App must be provided beforehand (BEFORE SERVICE OR NO SERVICE).</p>
                    </div>
                </div>
            </section>
        </div>
    </div>
    
    <!-- GALLERY PAGE -->
    <div class="page" id="gallery-page">
        <div class="container">
            <section class="gallery-section">
                <h2 class="section-title">Nail Gallery<span>✨ My Latest Creations ✨</span></h2>
                
                <div class="gallery-category">
                    <h3 class="category-title">🎂 BIRTHDAY NAILS</h3>
                    <div class="gallery-slider-container">
                        <div class="gallery-slider" id="birthday-slider"></div>
                    </div>
                </div>
                
                <div class="gallery-category">
                    <h3 class="category-title">💕 SIMPLE SETS</h3>
                    <div class="gallery-slider-container">
                        <div class="gallery-slider" id="simple-slider"></div>
                    </div>
                </div>
                
                <div class="gallery-category">
                    <h3 class="category-title">🌸 SEASONAL SETS</h3>
                    <div class="gallery-slider-container">
                        <div class="gallery-slider" id="seasonal-slider"></div>
                    </div>
                </div>
                
                <div class="gallery-category">
                    <h3 class="category-title">🦶 HANDS + TOES</h3>
                    <div class="gallery-slider-container">
                        <div class="gallery-slider" id="handstoes-slider"></div>
                    </div>
                </div>
                
                <div class="gallery-category">
                    <h3 class="category-title">📦 PRESS-ONS</h3>
                    <div class="gallery-slider-container">
                        <div class="gallery-slider" id="presson-slider"></div>
                    </div>
                </div>
            </section>
        </div>
    </div>
    
    <!-- BOOKING PAGE -->
    <div class="page" id="booking-page">
        <section class="booking-hero">
            <div class="booking-content">
                <h1 class="booking-title">Book Your Appointment</h1>
                
                <div class="booking-form-container">
                    <form id="bookingForm">
                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label">First Name</label>
                                <input type="text" id="firstName" class="form-control" placeholder="Your first name" required>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Last Name</label>
                                <input type="text" id="lastName" class="form-control" placeholder="Your last name" required>
                            </div>
                        </div>
                        
                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label">Phone Number</label>
                                <input type="tel" id="phone" class="form-control" placeholder="(786) 251-4782" required>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Email Address</label>
                                <input type="email" id="email" class="form-control" placeholder="narajilove@gmail.com" required>
                            </div>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label">Select Service</label>
                            <select id="service" class="form-control" required>
                                <option value="" disabled selected>Choose a service</option>
                                <option value="freestyle">Freestyle Full Set - $100</option>
                                <option value="acrylic-short">Acrylic Full Set - Short - $60</option>
                                <option value="acrylic-medium">Acrylic Full Set - Medium - $70</option>
                                <option value="acrylic-long">Acrylic Full Set - Long - $80</option>
                                <option value="gel-x">Gel X Extensions - $80+</option>
                                <option value="ombre">Ombre Full Set - $60-125</option>
                                <option value="gel-manicure">Gel Manicure - $50</option>
                                <option value="toes">Toe Service - $45-65</option>
                                <option value="presson">Custom Press-Ons - $110+</option>
                                <option value="afterhours-9">After Hours 9PM-11PM (+$40)</option>
                                <option value="afterhours-12">After Hours 12AM-2AM (+$60)</option>
                                <option value="afterhours-2">After Hours 2AM-4AM (+$80)</option>
                                <option value="soakoff">Soak Off Removal - $25</option>
                            </select>
                        </div>
                        
                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label">Preferred Date</label>
                                <input type="date" id="date" class="form-control" required>
                            </div>
                            <div class="form-group">
                                <label class="form-label">Preferred Time</label>
                                <select id="time" class="form-control" required>
                                    <option value="" disabled selected>Select time</option>
                                    <option value="9am">9:00 AM</option>
                                    <option value="10am">10:00 AM</option>
                                    <option value="11am">11:00 AM</option>
                                    <option value="12pm">12:00 PM</option>
                                    <option value="1pm">1:00 PM</option>
                                    <option value="2pm">2:00 PM</option>
                                    <option value="3pm">3:00 PM</option>
                                    <option value="4pm">4:00 PM</option>
                                    <option value="5pm">5:00 PM</option>
                                    <option value="6pm">6:00 PM</option>
                                    <option value="7pm">7:00 PM</option>
                                    <option value="8pm">8:00 PM</option>
                                    <option value="9pm">9:00 PM (After Hours +$40)</option>
                                    <option value="12am">12:00 AM (After Hours +$60)</option>
                                    <option value="2am">2:00 AM (After Hours +$80)</option>
                                </select>
                            </div>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label">Additional Notes or Inspiration</label>
                            <textarea id="notes" class="form-control" rows="4" placeholder="Share your nail inspo, design ideas, or any questions..."></textarea>
                        </div>
                        
                        <div class="form-submit">
                            <button type="submit" class="submit-btn">Submit Booking Request</button>
                        </div>
                    </form>
                    
                    <div style="margin-top: 30px; text-align: center; color: var(--medium-text); font-size: 0.85rem;">
                        <p><strong>📌 Important Information:</strong></p>
                        <p>A $25 deposit is required to secure your appointment. You will receive confirmation within 24 hours.</p>
                        <p>Cash only preferred • Zelle or Cash App accepted beforehand</p>
                    </div>
                </div>
            </div>
        </section>
    </div>
    
    <!-- FOOTER -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-brand">
                    <div class="footer-logo">NarajiRawcrylics</div>
                    <p>Luxury Beauty • Self-Care</p>
                </div>
                
                <div class="footer-contact">
                    <h3>Contact Info</h3>
                    <ul class="contact-info">
                        <li><i class="fas fa-envelope"></i> narajilove@gmail.com</li>
                        <li><i class="fas fa-phone"></i> (786) 251-4782</li>
                        <li><i class="fab fa-instagram"></i> @narajirawcrylics</li>
                    </ul>
                </div>
                
                <div class="footer-social">
                    <h3>Follow Me</h3>
                    <div class="social-icons">
                        <a href="https://instagram.com/narajirawcrylics" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="mailto:narajilove@gmail.com"><i class="fas fa-envelope"></i></a>
                        <a href="tel:7862514782"><i class="fas fa-phone"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2024 NarajiRawcrylics. All rights reserved.
            </div>
        </div>
    </footer>
    
    <div class="modal-overlay" id="confirmationModal">
        <div class="modal-content">
            <div class="modal-icon"><i class="fas fa-check-circle"></i></div>
            <h2 class="modal-title">Booking Request Sent!</h2>
            <div class="modal-message" id="modalMessage"></div>
            <button class="modal-btn" id="modalCloseBtn">Okay</button>
        </div>
    </div>
    
    <script>
        // CREATE FALLING WHITE DOTS
        function createFallingDots() {
            const container = document.getElementById('fallingDots');
            if (!container) return;
            
            const dotCount = window.innerWidth < 768 ? 50 : 100;
            
            for (let i = 0; i < dotCount; i++) {
                const dot = document.createElement('div');
                dot.className = 'dot';
                
                const size = Math.random() * 4 + 2;
                const posX = Math.random() * 100;
                const delay = Math.random() * 20;
                const duration = Math.random() * 8 + 6;
                
                dot.style.width = `${size}px`;
                dot.style.height = `${size}px`;
                dot.style.left = `${posX}%`;
                dot.style.animationDelay = `${delay}s`;
                dot.style.animationDuration = `${duration}s`;
                
                container.appendChild(dot);
            }
        }
        
        // Gallery Images
        const birthdayImages = [
            'https://i.postimg.cc/J7SvLG8F/Screenshot-2026-03-30-105319.png',
            'https://i.postimg.cc/tCPfCpRf/Screenshot-2026-03-30-105341.png',
            'https://i.postimg.cc/02m32P5H/Screenshot-2026-03-30-105415.png',
            'https://i.postimg.cc/8PW3PNkY/Screenshot-2026-03-30-105424.png',
            'https://i.postimg.cc/wTJPTgx4/Screenshot-2026-03-30-105433.png',
            'https://i.postimg.cc/3Jp6JYJT/Screenshot-2026-03-30-105446.png',
            'https://i.postimg.cc/bNbMNpNf/Screenshot-2026-03-30-105501.png',
            'https://i.postimg.cc/3Jp6JYJH/Screenshot-2026-03-30-105516.png',
            'https://i.postimg.cc/nc75cpcp/Screenshot-2026-03-30-105530.png',
            'https://i.postimg.cc/bNbMNpNr/Screenshot-2026-03-30-105547.png',
            'https://i.postimg.cc/3Jp6JYJR/Screenshot-2026-03-30-105602.png',
            'https://i.postimg.cc/dVYfhpLJ/Screenshot-2026-03-30-105616.png',
            'https://i.postimg.cc/Vk8hJpdY/Screenshot-2026-03-30-105632.png',
            'https://i.postimg.cc/fRNPVpJk/Screenshot-2026-03-30-105648.png',
            'https://i.postimg.cc/bwh5ZWss/Screenshot-2026-03-30-105706.png',
            'https://i.postimg.cc/xTMfrwwQ/Screenshot-2026-03-30-110251.png',
            'https://i.postimg.cc/CLkhy334/Screenshot-2026-03-30-110304.png',
            'https://i.postimg.cc/tCWq0KKW/Screenshot-2026-03-30-110319.png',
            'https://i.postimg.cc/02DkgTT0/Screenshot-2026-03-30-110330.png'
        ];
        
        const simpleImages = [
            'https://i.postimg.cc/brGv2dVZ/Screenshot-2026-03-30-110702.png',
            'https://i.postimg.cc/sxB2Z1HH/Screenshot-2026-03-30-110717.png',
            'https://i.postimg.cc/Bb8v1t7M/Screenshot-2026-03-30-110739.png',
            'https://i.postimg.cc/T1yPWhNk/Screenshot-2026-03-30-110756.png',
            'https://i.postimg.cc/5yHtFjKR/Screenshot-2026-03-30-110812.png',
            'https://i.postimg.cc/NFWj8YZz/Screenshot-2026-03-30-110841.png',
            'https://i.postimg.cc/Bbdn5sRw/Screenshot-2026-03-30-110857.png',
            'https://i.postimg.cc/RhjZ192Y/Screenshot-2026-03-30-110913.png'
        ];
        
        const seasonalImages = [
            'https://i.postimg.cc/mDnHnv07/Screenshot-2026-03-30-111152.png',
            'https://i.postimg.cc/F15JrjFr/Screenshot-2026-03-30-111208.png',
            'https://i.postimg.cc/fy09QHs0/Screenshot-2026-03-30-111223.png',
            'https://i.postimg.cc/J0BkCT8t/Screenshot-2026-03-30-111238.png',
            'https://i.postimg.cc/6qGvxHK4/Screenshot-2026-03-30-111253.png',
            'https://i.postimg.cc/c6y8xQ1D/Screenshot-2026-03-30-111315.png',
            'https://i.postimg.cc/sfB62sDy/Screenshot-2026-03-30-111329.png',
            'https://i.postimg.cc/c1K9J04x/Screenshot-2026-03-30-111345.png',
            'https://i.postimg.cc/QNB4MhxC/Screenshot-2026-03-30-111402.png',
            'https://i.postimg.cc/1RgCzs58/Screenshot-2026-03-30-111420.png',
            'https://i.postimg.cc/kMV15qX8/Screenshot-2026-03-30-111434.png',
            'https://i.postimg.cc/1RgCzs5w/Screenshot-2026-03-30-111448.png'
        ];
        
        const handstoeImages = [
            'https://i.postimg.cc/QM3GQVCP/Screenshot-2026-03-30-111941.png',
            'https://i.postimg.cc/6QfsYwGX/Screenshot-2026-03-30-111954.png',
            'https://i.postimg.cc/q7xfj069/Screenshot-2026-03-30-112012.png',
            'https://i.postimg.cc/1zrxJPNS/Screenshot-2026-03-30-112028.png'
        ];
        
        const pressonImages = [
            'https://i.postimg.cc/D0dBKyn2/Screenshot-2026-03-30-112309.png',
            'https://i.postimg.cc/8khyvwWm/Screenshot-2026-03-30-112324.png',
            'https://i.postimg.cc/mkN8G2BH/Screenshot-2026-03-30-112340.png',
            'https://i.postimg.cc/sfpnWKSK/Screenshot-2026-03-30-112351.png',
            'https://i.postimg.cc/T2rkbQm7/Screenshot-2026-03-30-112405.png',
            'https://i.postimg.cc/tRhr6DPf/Screenshot-2026-03-30-112421.png'
        ];
        
        function createSlider(containerId, images) {
            const container = document.getElementById(containerId);
            if (!container) return;
            container.innerHTML = '';
            const allImages = [...images, ...images];
            for (let i = 0; i < allImages.length; i++) {
                const slide = document.createElement('div');
                slide.className = 'gallery-slide';
                const img = document.createElement('img');
                img.src = allImages[i];
                img.alt = `Nail design ${i+1}`;
                img.loading = 'lazy';
                slide.appendChild(img);
                container.appendChild(slide);
            }
        }
        
        createSlider('birthday-slider', birthdayImages);
        createSlider('simple-slider', simpleImages);
        createSlider('seasonal-slider', seasonalImages);
        createSlider('handstoes-slider', handstoeImages);
        createSlider('presson-slider', pressonImages);
        
        // Page Navigation
        const pages = {
            'home': document.getElementById('home-page'),
            'gallery': document.getElementById('gallery-page'),
            'booking': document.getElementById('booking-page')
        };
        
        const navLinks = document.querySelectorAll('.nav-link');
        const logo = document.querySelector('.logo');
        const header = document.getElementById('main-header');
        const scrollTopBtn = document.getElementById('scrollTop');
        const modal = document.getElementById('confirmationModal');
        const modalMessage = document.getElementById('modalMessage');
        const modalClose = document.getElementById('modalCloseBtn');
        
        function switchPage(pageId) {
            Object.values(pages).forEach(page => page.classList.remove('active'));
            pages[pageId].classList.add('active');
            navLinks.forEach(link => {
                if (link.dataset.page === pageId) link.classList.add('active-page');
                else link.classList.remove('active-page');
            });
            window.scrollTo({ top: 0, behavior: 'smooth' });
            if (pageId === 'booking') {
                const today = new Date().toISOString().split('T')[0];
                document.getElementById('date').min = today;
                const tomorrow = new Date();
                tomorrow.setDate(tomorrow.getDate() + 1);
                document.getElementById('date').value = tomorrow.toISOString().split('T')[0];
            }
            history.pushState(null, '', `#${pageId}`);
        }
        
        navLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                switchPage(link.dataset.page);
                mobileMenu.classList.remove('active');
                hamburger.classList.remove('active');
                document.body.style.overflow = 'auto';
            });
        });
        
        logo.addEventListener('click', () => switchPage('home'));
        
        document.querySelectorAll('.btn[data-page]').forEach(btn => {
            btn.addEventListener('click', (e) => {
                e.preventDefault();
                switchPage(btn.dataset.page);
                mobileMenu.classList.remove('active');
                hamburger.classList.remove('active');
            });
        });
        
        const hamburger = document.getElementById('hamburger');
        const mobileMenu = document.getElementById('mobile-menu');
        
        hamburger.addEventListener('click', () => {
            mobileMenu.classList.toggle('active');
            hamburger.classList.toggle('active');
            document.body.style.overflow = mobileMenu.classList.contains('active') ? 'hidden' : 'auto';
        });
        
        document.querySelectorAll('.mobile-links a, .mobile-menu-btn a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
                hamburger.classList.remove('active');
                document.body.style.overflow = 'auto';
            });
        });
        
        modalClose.addEventListener('click', () => {
            modal.classList.remove('active');
            document.body.style.overflow = 'auto';
        });
        
        document.getElementById('bookingForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const firstName = document.getElementById('firstName').value;
            const lastName = document.getElementById('lastName').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            const serviceSelect = document.getElementById('service');
            const service = serviceSelect.options[serviceSelect.selectedIndex]?.text || '';
            const date = document.getElementById('date').value;
            const timeSelect = document.getElementById('time');
            const time = timeSelect.options[timeSelect.selectedIndex]?.text || '';
            const notes = document.getElementById('notes').value;
            
            const message = `✨ Thank you, ${firstName} ${lastName}! ✨\n\n✅ Your booking request has been received.\n\n📋 Appointment Details:\n• Service: ${service}\n• Date: ${new Date(date).toLocaleDateString()}\n• Time: ${time}\n• Contact: ${phone}, ${email}\n\n📝 Notes: ${notes || 'None provided'}\n\n📍 Location info will be sent 24hrs before appointment\n\n💸 A $25 deposit is required to secure your appointment.\n\nFor questions, contact:\n📱 (786) 251-4782\n📧 narajilove@gmail.com\n📸 @narajirawcrylics`;
            
            modalMessage.textContent = message;
            modal.classList.add('active');
            document.body.style.overflow = 'hidden';
            this.reset();
            const today = new Date().toISOString().split('T')[0];
            document.getElementById('date').min = today;
            const tomorrow = new Date();
            tomorrow.setDate(tomorrow.getDate() + 1);
            document.getElementById('date').value = tomorrow.toISOString().split('T')[0];
        });
        
        scrollTopBtn.addEventListener('click', () => window.scrollTo({ top: 0, behavior: 'smooth' }));
        
        function updateScrollTop() {
            if (window.scrollY > 500) scrollTopBtn.classList.add('visible');
            else scrollTopBtn.classList.remove('visible');
        }
        
        window.addEventListener('scroll', updateScrollTop);
        window.addEventListener('resize', () => {
            createSlider('birthday-slider', birthdayImages);
            createSlider('simple-slider', simpleImages);
            createSlider('seasonal-slider', seasonalImages);
            createSlider('handstoes-slider', handstoeImages);
            createSlider('presson-slider', pressonImages);
            const dotsContainer = document.getElementById('fallingDots');
            if (dotsContainer) {
                dotsContainer.innerHTML = '';
                createFallingDots();
            }
        });
        
        window.addEventListener('DOMContentLoaded', () => {
            createFallingDots();
            const hash = window.location.hash.substring(1);
            if (hash && pages[hash]) switchPage(hash);
            const today = new Date().toISOString().split('T')[0];
            document.getElementById('date').min = today;
        });
        
        window.addEventListener('popstate', () => {
            const hash = window.location.hash.substring(1);
            if (hash && pages[hash]) switchPage(hash);
        });
    </script>
</body>
</html>
