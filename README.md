<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, user-scalable=yes">
  <title>Naraji Rawcrylics | Artisan Nail Sets</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #fff;
      font-family: 'Playfair Display', serif;
    }

    /* Header - extremely mobile friendly, touch-friendly */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      width: 100%;
      background: rgba(255, 255, 255, 0.92);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      z-index: 1000;
      padding: 0.75rem 1.25rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      transition: background 0.2s ease;
      box-shadow: 0 1px 8px rgba(0,0,0,0.05);
    }

    .header-left .logo-img {
      height: 44px;
      width: auto;
      display: block;
      max-width: 100%;
    }

    .header-center {
      display: flex;
      gap: 2rem;
      align-items: center;
    }

    .header-center a {
      font-family: 'Playfair Display', serif;
      font-weight: 700;
      font-size: 1.1rem;
      text-decoration: none;
      color: #1a1a1a;
      transition: opacity 0.2s;
      padding: 0.5rem 0;
      letter-spacing: 0.3px;
      -webkit-tap-highlight-color: transparent;
    }

    .header-center a:active {
      opacity: 0.6;
    }

    .header-right {
      width: 44px;
    }

    /* Full width hero image */
    .hero-image {
      width: 100%;
      display: block;
      margin-top: 68px; /* Space for fixed header */
    }

    /* Full width image wall - VERTICAL LAYOUT, EDGE TO EDGE */
    .image-wall {
      width: 100%;
      display: flex;
      flex-direction: column;
    }

    .wall-img {
      width: 100%;
      display: block;
      height: auto;
      /* No margins, touches the walls perfectly */
    }

    /* Gallery page background */
    body.gallery-active {
      background-image: url('https://i.postimg.cc/8cRzGJng/Untitled-design.png');
      background-size: cover;
      background-attachment: fixed;
      background-position: center;
      background-repeat: no-repeat;
    }

    .gallery-container {
      margin-top: 80px;
      padding: 1.5rem;
      max-width: 1400px;
      margin-left: auto;
      margin-right: auto;
      background: rgba(255, 255, 245, 0.88);
      border-radius: 28px;
      backdrop-filter: blur(3px);
      -webkit-backdrop-filter: blur(3px);
    }

    .gallery-title {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
      font-size: 2.2rem;
      text-align: center;
      margin-bottom: 1.75rem;
      color: #000;
      letter-spacing: -0.3px;
    }

    .category-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
      gap: 1.5rem;
      margin-top: 0.5rem;
    }

    .category-card {
      background: rgba(255, 255, 245, 0.96);
      border-radius: 20px;
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.25s, box-shadow 0.25s;
      box-shadow: 0 4px 12px rgba(0,0,0,0.08);
      -webkit-tap-highlight-color: transparent;
    }

    .category-card:active {
      transform: scale(0.98);
    }

    .category-thumb {
      width: 100%;
      aspect-ratio: 1 / 1;
      object-fit: cover;
      display: block;
    }

    .category-name {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
      font-size: 1.2rem;
      text-align: center;
      padding: 1rem;
      color: #000;
    }

    /* Category detail page */
    .detail-container {
      margin-top: 80px;
      padding: 1.5rem;
      max-width: 1400px;
      margin-left: auto;
      margin-right: auto;
      background: rgba(255, 255, 245, 0.92);
      border-radius: 28px;
      backdrop-filter: blur(3px);
      -webkit-backdrop-filter: blur(3px);
    }

    .back-btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-family: 'Playfair Display', serif;
      font-weight: 700;
      background: rgba(0,0,0,0.75);
      color: white;
      padding: 0.7rem 1.6rem;
      border-radius: 40px;
      text-decoration: none;
      margin-bottom: 1.8rem;
      cursor: pointer;
      border: none;
      font-size: 0.95rem;
      transition: background 0.2s;
      -webkit-tap-highlight-color: transparent;
    }

    .back-btn:active {
      background: black;
      transform: scale(0.97);
    }

    .detail-title {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
      font-size: 1.9rem;
      margin-bottom: 1.8rem;
      color: #000;
    }

    .photos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 1.2rem;
    }

    .photo-card {
      aspect-ratio: 1 / 1;
      background: rgba(245, 245, 240, 0.8);
      border-radius: 18px;
      overflow: hidden;
      box-shadow: 0 2px 8px rgba(0,0,0,0.08);
    }

    .photo-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    /* Footer */
    .footer {
      text-align: center;
      padding: 2rem 1.5rem;
      background: rgba(255, 250, 240, 0.96);
      margin-top: 2rem;
      font-family: 'Playfair Display', serif;
      border-top: 1px solid rgba(0,0,0,0.05);
    }

    .footer p {
      margin: 0.4rem 0;
    }

    .footer a {
      color: #000;
      text-decoration: none;
      font-weight: 700;
      border-bottom: 1px solid #000;
      transition: opacity 0.2s;
      -webkit-tap-highlight-color: transparent;
    }

    .footer a:active {
      opacity: 0.7;
    }

    .footer .phone {
      font-weight: 500;
      letter-spacing: 0.3px;
    }

    /* Mobile first optimizations */
    @media (max-width: 768px) {
      .header {
        padding: 0.6rem 1rem;
      }
      .header-left .logo-img {
        height: 38px;
      }
      .header-center {
        gap: 1.6rem;
      }
      .header-center a {
        font-size: 1rem;
      }
      .hero-image {
        margin-top: 60px;
      }
      .gallery-title {
        font-size: 1.8rem;
      }
      .category-grid {
        gap: 1.2rem;
        grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      }
      .photos-grid {
        gap: 1rem;
        grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
      }
      .gallery-container, .detail-container {
        padding: 1.2rem;
        margin-top: 70px;
        border-radius: 20px;
      }
      .detail-title {
        font-size: 1.7rem;
      }
      .back-btn {
        padding: 0.6rem 1.3rem;
        font-size: 0.9rem;
      }
    }

    @media (max-width: 480px) {
      .header-center {
        gap: 1.2rem;
      }
      .header-center a {
        font-size: 0.9rem;
      }
      .category-grid {
        grid-template-columns: 1fr 1fr;
        gap: 0.9rem;
      }
      .category-name {
        font-size: 1rem;
        padding: 0.8rem;
      }
      .photos-grid {
        grid-template-columns: 1fr 1fr;
        gap: 0.8rem;
      }
      .gallery-title {
        font-size: 1.6rem;
      }
    }

    /* Ensure everything touches edges properly */
    body, #app, .image-wall, .hero-image {
      width: 100%;
      max-width: 100%;
      overflow-x: hidden;
    }

    img {
      max-width: 100%;
      height: auto;
    }
  </style>
</head>
<body>
  <div class="header">
    <div class="header-left">
      <img src="https://i.postimg.cc/Nfj3B2nM/Screenshot-2026-03-30-103801-removebg-preview.png" alt="Naraji Rawcrylics Logo" class="logo-img">
    </div>
    <div class="header-center">
      <a href="#" onclick="showHome(); return false;">HOME</a>
      <a href="#" onclick="showGallery(); return false;">GALLERY</a>
    </div>
    <div class="header-right"></div>
  </div>

  <div id="app"></div>

  <script>
    // ========== HERO IMAGE (only one at top) ==========
    const heroImageUrl = "https://i.postimg.cc/QxTn0X27/Yoyo.jpg";
    
    // ========== EXACT WALL IMAGES IN YOUR ORDER ==========
    const wallImages = [
      "https://i.postimg.cc/QxTn0X27/Yoyo.jpg",  // Hero image also first under hero? Actually you said "under the hero image add this Yoyo.jpg then this..."
      "https://i.postimg.cc/Wz2VcWRj/file_00000000e5f071f7bc8461a0f509ccd4_(1).jpg",
      "https://i.postimg.cc/rpRw7BMR/file_00000000fa6871f5ac8a5602760fe7df_(1).jpg",
      "https://i.postimg.cc/N0Sd1SNq/file-0000000009dc71f5bbedb109a903d6ec.png",
      "https://i.postimg.cc/0y5XxpMP/file_00000000b85c71fd87d30f2674b04c57.png",
      "https://i.postimg.cc/QtnSVKvz/file_000000004190722f9caa8c85702884dc_(2).jpg",
      "https://i.postimg.cc/gjwB9dn2/file_00000000a10c71fd9de893dd575156d6.png",
      "https://i.postimg.cc/HkHNqXmc/file-00000000061c71fd83ac214e21c2343c-(1).jpg"
    ];

    // ========== CATEGORY DATA (GALLERY REMAINS 100% UNCHANGED) ==========
    const categories = {
      "Birthday Sets": {
        thumbnail: "https://i.postimg.cc/J7SvLG8F/Screenshot_2026_03_30_105319.png",
        images: [
          "https://i.postimg.cc/J7SvLG8F/Screenshot_2026_03_30_105319.png",
          "https://i.postimg.cc/tCPfCpRf/Screenshot_2026_03_30_105341.png",
          "https://i.postimg.cc/02m32P5H/Screenshot_2026_03_30_105415.png",
          "https://i.postimg.cc/8PW3PNkY/Screenshot_2026_03_30_105424.png",
          "https://i.postimg.cc/wTJPTgx4/Screenshot_2026_03_30_105433.png",
          "https://i.postimg.cc/3Jp6JYJT/Screenshot_2026_03_30_105446.png",
          "https://i.postimg.cc/bNbMNpNf/Screenshot_2026_03_30_105501.png",
          "https://i.postimg.cc/3Jp6JYJH/Screenshot_2026_03_30_105516.png",
          "https://i.postimg.cc/nc75cpcp/Screenshot_2026_03_30_105530.png",
          "https://i.postimg.cc/bNbMNpNr/Screenshot_2026_03_30_105547.png",
          "https://i.postimg.cc/3Jp6JYJR/Screenshot_2026_03_30_105602.png",
          "https://i.postimg.cc/dVYfhpLJ/Screenshot_2026_03_30_105616.png",
          "https://i.postimg.cc/Vk8hJpdY/Screenshot_2026_03_30_105632.png",
          "https://i.postimg.cc/fRNPVpJk/Screenshot_2026_03_30_105648.png",
          "https://i.postimg.cc/bwh5ZWss/Screenshot_2026_03_30_105706.png",
          "https://i.postimg.cc/xTMfrwwQ/Screenshot_2026_03_30_110251.png",
          "https://i.postimg.cc/CLkhy334/Screenshot_2026_03_30_110304.png",
          "https://i.postimg.cc/tCWq0KKW/Screenshot_2026_03_30_110319.png",
          "https://i.postimg.cc/02DkgTT0/Screenshot_2026_03_30_110330.png"
        ]
      },
      "Simple Sets": {
        thumbnail: "https://i.postimg.cc/brGv2dVZ/Screenshot_2026_03_30_110702.png",
        images: [
          "https://i.postimg.cc/brGv2dVZ/Screenshot_2026_03_30_110702.png",
          "https://i.postimg.cc/sxB2Z1HH/Screenshot_2026_03_30_110717.png",
          "https://i.postimg.cc/Bb8v1t7M/Screenshot_2026_03_30_110739.png",
          "https://i.postimg.cc/T1yPWhNk/Screenshot_2026_03_30_110756.png",
          "https://i.postimg.cc/5yHtFjKR/Screenshot_2026_03_30_110812.png",
          "https://i.postimg.cc/NFWj8YZz/Screenshot_2026_03_30_110841.png",
          "https://i.postimg.cc/Bbdn5sRw/Screenshot_2026_03_30_110857.png",
          "https://i.postimg.cc/RhjZ192Y/Screenshot_2026_03_30_110913.png"
        ]
      },
      "Seasonal Sets": {
        thumbnail: "https://i.postimg.cc/mDnHnv07/Screenshot_2026_03_30_111152.png",
        images: [
          "https://i.postimg.cc/mDnHnv07/Screenshot_2026_03_30_111152.png",
          "https://i.postimg.cc/F15JrjFr/Screenshot_2026_03_30_111208.png",
          "https://i.postimg.cc/fy09QHs0/Screenshot_2026_03_30_111223.png",
          "https://i.postimg.cc/J0BkCT8t/Screenshot_2026_03_30_111238.png",
          "https://i.postimg.cc/6qGvxHK4/Screenshot_2026_03_30_111253.png",
          "https://i.postimg.cc/c6y8xQ1D/Screenshot_2026_03_30_111315.png",
          "https://i.postimg.cc/sfB62sDy/Screenshot_2026_03_30_111329.png",
          "https://i.postimg.cc/c1K9J04x/Screenshot_2026_03_30_111345.png",
          "https://i.postimg.cc/QNB4MhxC/Screenshot_2026_03_30_111402.png",
          "https://i.postimg.cc/1RgCzs58/Screenshot_2026_03_30_111420.png",
          "https://i.postimg.cc/kMV15qX8/Screenshot_2026_03_30_111434.png",
          "https://i.postimg.cc/1RgCzs5w/Screenshot_2026_03_30_111448.png"
        ]
      },
      "Hands + Toes Sets": {
        thumbnail: "https://i.postimg.cc/QM3GQVCP/Screenshot_2026_03_30_111941.png",
        images: [
          "https://i.postimg.cc/QM3GQVCP/Screenshot_2026_03_30_111941.png",
          "https://i.postimg.cc/6QfsYwGX/Screenshot_2026_03_30_111954.png",
          "https://i.postimg.cc/q7xfj069/Screenshot_2026_03_30_112012.png",
          "https://i.postimg.cc/1zrxJPNS/Screenshot_2026_03_30_112028.png"
        ]
      },
      "Press-On Sets": {
        thumbnail: "https://i.postimg.cc/D0dBKyn2/Screenshot_2026_03_30_112309.png",
        images: [
          "https://i.postimg.cc/D0dBKyn2/Screenshot_2026_03_30_112309.png",
          "https://i.postimg.cc/8khyvwWm/Screenshot_2026_03_30_112324.png",
          "https://i.postimg.cc/mkN8G2BH/Screenshot_2026_03_30_112340.png",
          "https://i.postimg.cc/sfpnWKSK/Screenshot_2026_03_30_112351.png",
          "https://i.postimg.cc/T2rkbQm7/Screenshot_2026_03_30_112405.png",
          "https://i.postimg.cc/tRhr6DPf/Screenshot_2026_03_30_112421.png"
        ]
      }
    };

    function setBodyBackground(isGallery) {
      if (isGallery) {
        document.body.classList.add('gallery-active');
      } else {
        document.body.classList.remove('gallery-active');
      }
    }

    // HOME PAGE: Hero image (Yoyo.jpg) at top, then exact wall images underneath, edge-to-edge
    function showHome() {
      setBodyBackground(false);
      const app = document.getElementById('app');
      app.innerHTML = '';
      
      // Create container that holds hero + image wall (vertical stack)
      const mainContainer = document.createElement('div');
      mainContainer.style.width = '100%';
      
      // Hero image (first image, Yoyo.jpg)
      const heroImg = document.createElement('img');
      heroImg.src = heroImageUrl;
      heroImg.className = 'hero-image';
      heroImg.alt = 'Hero banner';
      heroImg.style.display = 'block';
      heroImg.style.width = '100%';
      heroImg.style.height = 'auto';
      
      // Image wall div (vertical stack of the exact images)
      const imageWall = document.createElement('div');
      imageWall.className = 'image-wall';
      
      // Add each wall image in the exact order you provided (wallImages array already includes Yoyo? No, but you said "under hero image add this Yoyo.jpg then this..." 
      // According to your instruction: remove all images except hero image, then UNDER hero image add Yoyo.jpg, then the rest.
      // That means hero image is standalone at top, then the wall starts with Yoyo.jpg again? Or did you mean hero image = Yoyo.jpg and then under it add the others?
      // To be precise: You said "remove all images on the home page except for the hero image and under the hero image add this Yoyo.jpg then this (second link) etc"
      // I interpret as: Hero image is Yoyo.jpg, and THEN the first image under hero is also Yoyo.jpg (duplicate) or just start the wall with the second link?
      // Based on typical request, I'll make the hero image Yoyo.jpg, and the wall images start with the SECOND link you provided (the e5f071f7...)
      // But to match your literal "add this Yoyo.jpg then this (second link)" — I will add Yoyo.jpg as the FIRST wall image below hero, then the rest.
      // That creates hero + duplicate Yoyo.jpg at top of wall. If you meant hero = Yoyo and wall starts from second link, let me know — but I'll follow your exact wording.
      
      // Create wall images array as per your sequence: Yoyo.jpg first, then the others
      const exactWallSequence = [
        "https://i.postimg.cc/QxTn0X27/Yoyo.jpg",  // first under hero
        "https://i.postimg.cc/Wz2VcWRj/file_00000000e5f071f7bc8461a0f509ccd4_(1).jpg",
        "https://i.postimg.cc/rpRw7BMR/file_00000000fa6871f5ac8a5602760fe7df_(1).jpg",
        "https://i.postimg.cc/N0Sd1SNq/file-0000000009dc71f5bbedb109a903d6ec.png",
        "https://i.postimg.cc/0y5XxpMP/file_00000000b85c71fd87d30f2674b04c57.png",
        "https://i.postimg.cc/QtnSVKvz/file_000000004190722f9caa8c85702884dc_(2).jpg",
        "https://i.postimg.cc/gjwB9dn2/file_00000000a10c71fd9de893dd575156d6.png",
        "https://i.postimg.cc/HkHNqXmc/file-00000000061c71fd83ac214e21c2343c-(1).jpg"
      ];
      
      exactWallSequence.forEach(imgUrl => {
        const img = document.createElement('img');
        img.src = imgUrl;
        img.className = 'wall-img';
        img.alt = 'Nail art display';
        img.style.width = '100%';
        img.style.display = 'block';
        imageWall.appendChild(img);
      });
      
      mainContainer.appendChild(heroImg);
      mainContainer.appendChild(imageWall);
      app.appendChild(mainContainer);
      addFooter();
    }
    
    function showGallery() {
      setBodyBackground(true);
      const app = document.getElementById('app');
      app.innerHTML = '';
      
      const container = document.createElement('div');
      container.className = 'gallery-container';
      
      const title = document.createElement('h1');
      title.className = 'gallery-title';
      title.innerText = 'Collections';
      container.appendChild(title);
      
      const grid = document.createElement('div');
      grid.className = 'category-grid';
      
      for (const [catName, catData] of Object.entries(categories)) {
        const card = document.createElement('div');
        card.className = 'category-card';
        card.onclick = () => showCategoryDetail(catName);
        
        const thumb = document.createElement('img');
        thumb.src = catData.thumbnail;
        thumb.className = 'category-thumb';
        thumb.alt = catName;
        
        const name = document.createElement('div');
        name.className = 'category-name';
        name.innerText = catName;
        
        card.appendChild(thumb);
        card.appendChild(name);
        grid.appendChild(card);
      }
      
      container.appendChild(grid);
      app.appendChild(container);
      addFooter();
    }
    
    function showCategoryDetail(categoryName) {
      setBodyBackground(true);
      const category = categories[categoryName];
      if (!category) return;
      
      const app = document.getElementById('app');
      app.innerHTML = '';
      
      const container = document.createElement('div');
      container.className = 'detail-container';
      
      const backBtn = document.createElement('button');
      backBtn.className = 'back-btn';
      backBtn.innerText = '← Back to Galleries';
      backBtn.onclick = showGallery;
      
      const title = document.createElement('h1');
      title.className = 'detail-title';
      title.innerText = categoryName;
      
      const photosGrid = document.createElement('div');
      photosGrid.className = 'photos-grid';
      
      category.images.forEach(imgUrl => {
        const photoCard = document.createElement('div');
        photoCard.className = 'photo-card';
        const img = document.createElement('img');
        img.src = imgUrl;
        img.alt = categoryName;
        photoCard.appendChild(img);
        photosGrid.appendChild(photoCard);
      });
      
      container.appendChild(backBtn);
      container.appendChild(title);
      container.appendChild(photosGrid);
      app.appendChild(container);
      addFooter();
    }
    
    function addFooter() {
      const existingFooter = document.querySelector('.footer');
      if (existingFooter) existingFooter.remove()
