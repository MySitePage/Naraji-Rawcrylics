
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Naraji Rawcrylics</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&display=swap" rel="stylesheet">
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

    /* Header - low opacity white with logo only */
    .header {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(255, 255, 255, 0.55);
      backdrop-filter: blur(8px);
      z-index: 100;
      padding: 0.6rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      transition: background 0.3s ease;
    }

    .header-left .logo-img {
      height: 50px;
      width: auto;
      display: block;
    }

    .header-center {
      display: flex;
      gap: 2.5rem;
      align-items: center;
    }

    .header-center a {
      font-family: 'Playfair Display', serif;
      font-weight: 700;
      font-size: 1.2rem;
      text-decoration: none;
      color: #000;
      transition: opacity 0.3s;
    }

    .header-center a:hover {
      opacity: 0.7;
    }

    .header-right {
      width: 50px;
    }

    /* Full width image wall - vertical layout */
    .image-wall {
      width: 100%;
      margin-top: 0;
    }

    .wall-img {
      width: 100%;
      display: block;
    }

    /* Gallery page with background image */
    body.gallery-active {
      background-image: url('https://i.postimg.cc/8cRzGJng/Untitled-design.png');
      background-size: cover;
      background-attachment: fixed;
      background-position: center;
      background-repeat: no-repeat;
    }

    .gallery-container {
      margin-top: 80px;
      padding: 2rem;
      max-width: 1400px;
      margin-left: auto;
      margin-right: auto;
      background: rgba(255, 255, 245, 0.85);
      border-radius: 24px;
      backdrop-filter: blur(2px);
    }

    .gallery-title {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
      font-size: 2.5rem;
      text-align: center;
      margin-bottom: 2rem;
      color: #000;
    }

    .category-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 2rem;
      margin-top: 1rem;
    }

    .category-card {
      background: rgba(255, 255, 245, 0.95);
      border-radius: 20px;
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    }

    .category-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 25px rgba(0,0,0,0.15);
    }

    .category-thumb {
      width: 100%;
      aspect-ratio: 1 / 1;
      object-fit: cover;
    }

    .category-name {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
      font-size: 1.3rem;
      text-align: center;
      padding: 1rem;
      color: #000;
    }

    /* Category detail page */
    .detail-container {
      margin-top: 80px;
      padding: 2rem;
      max-width: 1400px;
      margin-left: auto;
      margin-right: auto;
      background: rgba(255, 255, 245, 0.9);
      border-radius: 24px;
      backdrop-filter: blur(2px);
    }

    .back-btn {
      display: inline-block;
      font-family: 'Playfair Display', serif;
      font-weight: 700;
      background: rgba(0,0,0,0.7);
      color: white;
      padding: 0.6rem 1.5rem;
      border-radius: 30px;
      text-decoration: none;
      margin-bottom: 2rem;
      cursor: pointer;
      border: none;
      font-size: 1rem;
    }

    .back-btn:hover {
      background: black;
    }

    .detail-title {
      font-family: 'Playfair Display', serif;
      font-weight: 900;
      font-size: 2.2rem;
      margin-bottom: 2rem;
      color: #000;
    }

    .photos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
      gap: 1.5rem;
    }

    .photo-card {
      aspect-ratio: 1 / 1;
      background: rgba(245, 245, 245, 0.8);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    }

    .photo-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    /* Footer */
    .footer {
      text-align: center;
      padding: 2rem;
      background: rgba(255, 250, 240, 0.95);
      margin-top: 3rem;
      font-family: 'Playfair Display', serif;
    }

    .footer p {
      margin: 0.3rem 0;
    }

    .footer a {
      color: #000;
      text-decoration: none;
      font-weight: 700;
      border-bottom: 1px solid #000;
    }

    .footer a:hover {
      opacity: 0.7;
    }

    .footer .phone {
      font-weight: 500;
      letter-spacing: 0.5px;
    }

    @media (max-width: 768px) {
      .header {
        padding: 0.5rem 1rem;
      }
      .header-left .logo-img {
        height: 40px;
      }
      .header-center {
        gap: 1.5rem;
      }
      .header-center a {
        font-size: 1rem;
      }
      .gallery-title {
        font-size: 1.8rem;
      }
      .category-grid {
        gap: 1rem;
      }
      .photos-grid {
        gap: 1rem;
      }
      .gallery-container, .detail-container {
        padding: 1rem;
        margin-top: 75px;
      }
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
    // All image URLs for the homepage wall (vertical layout)
    const homepageImages = [
      "https://i.postimg.cc/28ZsXNL8/Screenshot-2026-03-30-104747.png",
      "https://i.postimg.cc/C5Y8TgLM/file_00000000ecb471f5a73def0af0ab6b81_(1).jpg",
      "https://i.postimg.cc/NF4HQz5j/file_00000000e5f071f7bc8461a0f509ccd4_(1).jpg",
      "https://i.postimg.cc/C5Y8TgLM/file_00000000ecb471f5a73def0af0ab6b81_(1).jpg",
      "https://i.postimg.cc/2ymWRD8m/file_00000000fa6871f5ac8a5602760fe7df_(1).jpg",
      "https://i.postimg.cc/Hn2yThVn/file_000000004190722f9caa8c85702884dc_(2).jpg",
      "https://i.postimg.cc/ZnZNtSKT/file_00000000b85c71fd87d30f2674b04c57_(1).jpg",
      "https://i.postimg.cc/T19DT4pP/file_00000000bf4c71f5a35b775ca168cd5d_(1).jpg",
      "https://i.postimg.cc/4yZckgNT/file_00000000061c71fd83ac214e21c2343c_(1).jpg"
    ];

    // Category data
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

    function showHome() {
      setBodyBackground(false);
      const app = document.getElementById('app');
      app.innerHTML = '';
      
      const imageWall = document.createElement('div');
      imageWall.className = 'image-wall';
      
      homepageImages.forEach(imgUrl => {
        const img = document.createElement('img');
        img.src = imgUrl;
        img.className = 'wall-img';
        img.alt = 'Nail art';
        imageWall.appendChild(img);
      });
      
      app.appendChild(imageWall);
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
      if (existingFooter) existingFooter.remove();
      
      const footer = document.createElement('div');
      footer.className = 'footer';
      footer.innerHTML = `
        <p>© 2026 naraji rawcrylics</p>
        <p class="phone">📞 <a href="tel:+17862514782">(786) 251-4782</a></p>
        <p><a href="https://www.instagram.com/narajirawcrylics" target="_blank">@narajirawcrylics</a></p>
      `;
      document.body.appendChild(footer);
    }
    
    showHome();
  </script>
</body>
</html>
