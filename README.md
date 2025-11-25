<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seasonal Supply Co. — Lithophane Ornaments</title>
    <meta name="description" content="Custom 3D-printed lithophane Christmas ornaments that glow with your most cherished memories.">
    <link href="https://fonts.googleapis.com/css2?family=Helvetica+Neue:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --green: #1e3932;
            --red: #c41e3a;
            --light: #fafafa;
            --dark: #111;
        }
        * { margin:0; padding:0; box-sizing:border-box; }
        html { scroll-behavior:smooth; }
        body {
            font-family:'Helvetica Neue', -apple-system, BlinkMacSystemFont, sans-serif;
            background:var(--light);
            color:var(--dark);
            line-height:1.5;
        }
        nav {
            position:fixed;
            top:0; left:0; width:100%;
            padding:1.5rem 4%;
            display:flex;
            justify-content:space-between;
            align-items:center;
            z-index:1000;
            background:rgba(255,255,255,0.95);
            backdrop-filter:blur(10px);
            transition:all 0.4s;
        }
        nav.scrolled { padding:1rem 4%; box-shadow:0 4px 20px rgba(0,0,0,0.08); }
        .logo img { height:48px; width:auto; }
        .nav-links { display:flex; gap:3rem; }
        .nav-links a { text-decoration:none; color:var(--dark); font-weight:500; font-size:1rem; }
        .nav-links a:hover { color:var(--red); }
        /* Hero */
        .hero {
            height:100vh;
            background: linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.65)),
                        url('Images/Dark.jpg.jpg') center/cover no-repeat;
            display:flex;
            flex-direction:column;
            justify-content:center;
            align-items:center;
            text-align:center;
            color:white;
        }
        .hero h1 { font-size:5.5rem; font-weight:700; letter-spacing:-2px; margin-bottom:1rem; }
        .hero .subtitle { font-size:1.8rem; font-weight:300; margin-bottom:3rem; opacity:0.9; }
        .btn { padding:0.9rem 3rem; font-size:1.1rem; font-weight:500; border-radius:4px; text-decoration:none; transition:all 0.3s; min-width:220px; display:inline-block; text-align:center; }
        .btn-primary { background:var(--red); color:white; }
        .btn-primary:hover { background:#a01729; transform:translateY(-3px); }
        .btn-secondary { background:transparent; color:white; border:2px solid white; }
        .btn-secondary:hover { background:rgba(255,255,255,0.15); }
        /* Product Section */
        .product-section {
            padding:10rem 8%;
            display:grid;
            grid-template-columns:1fr 1fr;
            gap:8rem;
            align-items:center;
            max-width:1400px;
            margin:0 auto;
            background:white;
        }
        .product-image, .about-image {
            width:100%;
            aspect-ratio:1/1;
            border-radius:12px;
            overflow:hidden;
            box-shadow:0 20px 60px rgba(0,0,0,0.15);
        }
        .product-image img, .about-image img {
            width:100%;
            height:100%;
            object-fit:cover;
            display:block;
        }
        .about-image { aspect-ratio:4/3; box-shadow:0 20px 60px rgba(0,0,0,0.1); }
        .product-info h2 { font-size:4rem; font-weight:700; color:var(--green); margin-bottom:1.5rem; }
        .product-info .price { font-size:3rem; color:var(--red); font-weight:600; margin:2rem 0; }
        .product-info p { font-size:1.3rem; color:#444; line-height:1.8; margin-bottom:2rem; }
        .features { list-style:none; margin:3rem 0; }
        .features li { font-size:1.2rem; padding:0.8rem 0; border-bottom:1px solid #eee; }
        .features li::before { content:"Checkmark "; color:var(--green); font-weight:bold; }
        /* About Section */
        .about-section {
            padding:10rem 8%;
            background:var(--light);
            text-align:center;
        }
        .about-section h2 {
            font-size:4rem;
            font-weight:700;
            color:var(--green);
            margin-bottom:2rem;
        }
        .about-grid {
            display:grid;
            grid-template-columns:1fr 1fr;
            gap:6rem;
            max-width:1200px;
            margin:4rem auto 0;
            align-items:center;
        }
        .about-text {
            font-size:1.4rem;
            color:#333;
            line-height:1.9;
            text-align:left;
        }
        .about-text p { margin-bottom:1.5rem; }
        footer { background:var(--dark); color:#aaa; text-align:center; padding:4rem 2rem; }
        footer a { color:#fff; text-decoration:none; }
        @media (max-width:968px) {
            .hero h1 { font-size:4rem; }
            .product-section, .about-grid { grid-template-columns:1fr; padding:8rem 5%; text-align:center; }
            .about-text { text-align:center; }
        }
    </style>
</head>
<body>
    <nav id="navbar">
        <div class="logo">
            <img src="Images/logo.jpg" alt="Seasonal Supply Co.">
        </div>
        <div class="nav-links">
            <a href="#home">Home</a>
            <a href="#product">The Ornament</a>
            <a href="#about">About</a>
            <a href="#order">Order</a>
        </div>
    </nav>
    <!-- Hero -->
    <section id="home" class="hero">
        <h1>Lithophane Ornament</h1>
        <p class="subtitle">The Savior of the world, glowing on your Chirtmas tree</p>
        <div style="display:flex; gap:1.5rem; flex-wrap:wrap; justify-content:center;">
            <a href="#order" class="btn btn-primary">Order Now – $14.99</a>
            <a href="#product" class="btn btn-secondary">Learn More</a>
        </div>
    </section>
    <!-- Product Section - IMAGE NOW WORKS -->
    <section id="product" class="product-section">
        <div class="product-image">
            <img src="Images/cover.jpg.jpg" alt="Glowing Lithophane Ornament on Christmas Tree">
        </div>
        <div class="product-info">
            <h2>The Lithophane Ornament</h2>
            <div class="price">$14.99</div>
            <p>A one-of-a-kind Christmas ornament.</p>
            <p>Limited batch • Handcrafted in North America • Ships in 5–12 days</p>
            <ul class="features">
                <li>Premium Oak Hardwood and durable plastic</li>
                <li>Backlit effect creates stunning glowing portrait</li>
                <li>2.5-inch diameter – perfect orniment size</li>
            </ul>
            <a href="#order" class="btn btn-primary" style="margin-top:2rem;">Order Your Custom Ornament</a>
        </div>
    </section>
    <!-- About Section - IMAGE NOW WORKS -->
    <section id="about" class="about-section">
        <h2>About Seasonal Supply Co.</h2>
        <div class="about-grid">
            <div class="about-image">
                <img src="Images/logo.jpg" alt="Seasonal Supply Co. Workshop">
            </div>
            <div class="about-text">
                <p>We started Seasonal Supply Co. in 2025 knowing that we could make better Christmas ornaments that put Christ in Christmas.</p>
                <p>These decorations will light up your home and holiday season.</p>
                <p>Each ornament is designed and printed by hand in our small studio. No mass production. No middlemen. Just real people making something magical for your family.</p>
                <p>This Christmas, give a decoration that tells the story of Christmas.</p>
            </div>
        </div>
    </section>
    <footer>
        <p>© 2025 Seasonal Supply Co. — Handcrafted with care.</p>
        <p><a href="mailto:sscinquries@gmail.com">sscinquries@gmail.com</a></p>
    </footer>

    <script>
        window.addEventListener('scroll', () => {
            document.getElementById('navbar').classList.toggle('scrolled', window.scrollY > 100);
        });
    </script>
</body>
</html>
