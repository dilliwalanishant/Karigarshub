<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>KARIGAR's HUB | Empowering Weavers</title>
    
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#3D3B36">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&family=Playfair+Display:wght@700;800&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --background: #F9F5F0; 
            --text-dark: #3D3B36;   
            --primary-dark: #413F3D; 
            --accent-gold: #C0A172;  
            --accent-gold-darker: #a18258;
            --text-light: #F9F5F0;
            --border-light: #EAE0D3;

            --font-heading: 'Playfair Display', serif;
            --font-body: 'Montserrat', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-body);
            margin: 0;
            padding: 0;
            background-color: var(--background);
            color: var(--text-dark);
            overflow-x: hidden; /* Prevents horizontal scroll from animations */
        }

        /* --- NAVIGATION --- */
        .main-nav {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5em 3em;
            box-sizing: border-box;
            background: linear-gradient(to bottom, rgba(0,0,0,0.5), transparent);
        }
        .nav-logo-text {
            font-family: var(--font-heading);
            font-weight: 800;
            font-size: 1.5em;
            color: var(--text-light);
            text-decoration: none;
        }
        .nav-links a {
            font-family: var(--font-body);
            font-weight: 500;
            text-decoration: none;
            color: var(--text-light);
            padding: 0.5em 1em;
            margin: 0 0.5em;
            transition: color 0.3s;
        }
        .nav-links a:hover {
            color: var(--accent-gold);
        }

        /* --- HERO SECTION --- */
        .hero-section {
            height: 100vh;
            background-image: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('images/KH pic 1.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--text-light);
            padding: 2em;
        }
        .hero-section h1 {
            font-family: var(--font-heading);
            font-size: 4.5em;
            font-weight: 800;
            margin: 0;
            text-shadow: 2px 2px 10px rgba(0,0,0,0.5);
        }
        .hero-section p {
            font-size: 1.2em;
            max-width: 600px;
            margin: 1em 0 2em 0;
            text-shadow: 1px 1px 5px rgba(0,0,0,0.5);
        }

        /* --- GENERAL SECTION STYLING --- */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1em;
        }
        .feature-section {
            padding: 5em 2em;
        }
        .section-title {
            text-align: center;
            font-family: var(--font-heading);
            font-size: 3em;
            margin-bottom: 1em;
            color: var(--text-dark);
        }

        /* --- THE ART OF WEAVING SECTION --- */
        .craft-process-container {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 2em;
            text-align: center;
        }
        .craft-step {
            flex: 1;
            min-width: 280px;
            padding: 2em;
        }
        .craft-step .icon {
            font-size: 3em;
            color: var(--accent-gold);
            margin-bottom: 0.5em;
            display: inline-block;
            border: 2px solid var(--border-light);
            width: 100px;
            height: 100px;
            line-height: 100px;
            border-radius: 50%;
            transition: background-color 0.3s, color 0.3s;
        }
        .craft-step:hover .icon {
            background-color: var(--accent-gold);
            color: var(--primary-dark);
        }
        .craft-step h3 {
            font-family: var(--font-heading);
            font-size: 1.8em;
            margin-bottom: 0.5em;
        }

        /* --- OVERLAPPING LAYOUT SECTION --- */
        .overlapping-layout {
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            align-items: center;
            gap: 2em;
            margin: 4em 0;
        }
        .overlap-image {
            grid-column: 1 / span 7;
            grid-row: 1;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 10px 10px 40px rgba(0,0,0,0.1);
        }
        .overlap-image img {
            width: 100%;
            display: block;
        }
        .overlap-content {
            grid-column: 7 / span 6;
            grid-row: 1;
            background-color: #fff;
            padding: 3em;
            border-radius: 8px;
            border: 1px solid var(--border-light);
            box-shadow: 0 5px 25px rgba(0,0,0,0.05);
        }
        .overlap-content h3 {
            font-family: var(--font-heading);
            font-size: 2em;
            margin-top: 0;
        }

        /* --- FEATURE CARDS --- */
        .feature-grid {
            display: flex; flex-wrap: wrap; justify-content: center; width: 100%;
        }
        .feature {
            flex: 1 1 45%; margin: 1em; padding: 2em; background-color: #fff;
            border: 1px solid var(--border-light); border-radius: 8px; text-align: center;
            display: flex; flex-direction: column; justify-content: flex-start;
            box-shadow: 0 5px 25px rgba(0,0,0,0.05); transition: transform 0.3s, box-shadow 0.3s;
        }
        .feature:hover { transform: translateY(-5px); box-shadow: 0 10px 30px rgba(0,0,0,0.08); }
        .feature .icon { font-size: 2.5em; color: var(--accent-gold); margin-bottom: 0.5em; }
        .feature h3 { font-family: var(--font-heading); font-size: 1.8em; }
        .feature p { line-height: 1.7; margin-bottom: 1.5em; }

        /* --- BUTTONS --- */
        .btn {
            display: inline-block; font-family: var(--font-body); font-weight: 700;
            padding: 0.9em 2em; background-color: var(--accent-gold); color: var(--text-dark);
            text-decoration: none; border-radius: 50px; margin-top: auto; cursor: pointer;
            border: 2px solid var(--accent-gold); transition: all 0.3s;
        }
        .btn:hover { background-color: var(--accent-gold-darker); border-color: var(--accent-gold-darker); transform: translateY(-3px); box-shadow: 0 5px 15px rgba(0,0,0,0.1); }
        .btn-secondary { background-color: transparent; color: var(--accent-gold); }
        .btn-secondary:hover { background-color: var(--accent-gold); color: var(--text-dark); }
        
        /* --- OTHER STYLES (MODAL, FORM, ETC) --- */
        .styled-form input, .styled-form select {
            width: 100%; padding: 12px; margin-bottom: 10px; border-radius: 5px; border: 1px solid var(--border-light);
            font-family: var(--font-body); font-size: 1em; background: var(--background);
        }
        .product-gallery {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px;
            justify-content: center; margin-top: 1.5em;
        }
        .gallery-item { position: relative; overflow: hidden; border-radius: 8px; }
        .gallery-item img {
            width: 100%; height: 100%; aspect-ratio: 1 / 1; object-fit: cover;
            border: 1px solid var(--border-light); transition: transform 0.4s ease;
        }
        .gallery-item:hover img { transform: scale(1.1); }
        .gallery-overlay {
            position: absolute; top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(to top, rgba(0,0,0,0.7), transparent);
            display: flex; justify-content: center; align-items: flex-end;
            padding: 1em; color: white; opacity: 0; transition: opacity 0.4s ease;
        }
        .gallery-item:hover .gallery-overlay { opacity: 1; }
        
        /* --- FOOTER --- */
        footer {
            background-color: var(--primary-dark); color: var(--text-light);
            text-align: center; padding: 4em 2em; font-size: 1em;
        }
        footer p { margin-top: 0.5em; opacity: 0.8; }
        
        /* Modals and other hidden elements remain functionally the same */
        .content-tab { display: none; /* ... rest of modal styles / } .tab-inner-content { background-color: var(--background); / ... / } .close-btn { / ... */ }
        .floating-support-hub { /* ... */ }
        
        /* Responsive styles */
        @media screen and (max-width: 900px) {
            .overlap-image { grid-column: 1 / span 12; }
            .overlap-content { grid-column: 2 / span 10; margin-top: -50px; }
        }
        @media screen and (max-width: 768px) {
            .main-nav { padding: 1em; flex-direction: column; }
            .nav-links { margin-top: 1em; }
            .hero-section h1 { font-size: 2.8em; }
            .section-title { font-size: 2.2em; }
        }
    </style>
</head>
<body>

    <nav class="main-nav">
        <a href="#" class="nav-logo-text">KARIGAR's HUB</a>
        <div class="nav-links">
            <a href="#art-of-weaving">The Craft</a>
            <a href="#learn">Learn</a>
            <a href="#schemes">Schemes</a>
            <a href="#sell">Sell</a>
            <a href="#register">Join Us</a>
        </div>
    </nav>

    <section class="hero-section" id="home">
        <h1 data-aos="fade-down">Weaving Dreams, Empowering Lives</h1>
        <p data-aos="fade-up" data-aos-delay="200">A digital gateway for the weavers of Taraboi, connecting timeless tradition with modern technology. {ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ପାଇଁ ଏକ ଡିଜିଟାଲ୍ ଗେଟୱେ, ପରମ୍ପରାକୁ ଆଧୁନିକ ପ୍ରଯୁକ୍ତିବିଦ୍ୟା ସହିତ ଯୋଡ଼ିବା।}</p>
        <a href="#art-of-weaving" class="btn" data-aos="fade-up" data-aos-delay="400">Discover the Craft</a>
    </section>

    <div class="container">
        
        <section id="art-of-weaving" class="feature-section">
            <h2 class="section-title" data-aos="fade-up">The Art of Weaving {ବୁଣାକାର୍ଯ୍ୟର କଳା}</h2>
            <div class="craft-process-container">
                <div class="craft-step" data-aos="fade-up" data-aos-delay="100">
                    <span class="icon"><i class="fas fa-palette"></i></span>
                    <h3>Dyeing the Threads</h3>
                    <p>The journey begins with vibrant colors, as artisans skillfully dye silk and cotton threads, preparing them for the loom.</p>
                </div>
                <div class="craft-step" data-aos="fade-up" data-aos-delay="200">
                    <span class="icon"><i class="fas fa-cogs"></i></span>
                    <h3>Setting the Loom</h3>
                    <p>Each thread is meticulously arranged on the handloom, a complex process that sets the foundation for the intricate patterns.</p>
                </div>
                <div class="craft-step" data-aos="fade-up" data-aos-delay="300">
                    <span class="icon"><i class="fas fa-magic"></i></span>
                    <h3>The Weaving Magic</h3>
                    <p>With skillful hands and feet, the weaver brings the design to life, interlacing threads to create a masterpiece.</p>
                </div>
            </div>
        </section>

        <section id="learn" class="feature-section">
            <div class="overlapping-layout">
                <div class="overlap-image" data-aos="fade-right">
                    <img src="images/KH pic 2.jpg" alt="Artisan learning">
                </div>
                <div class="overlap-content" data-aos="fade-left">
                    <h3>Learn & Grow {ଶିଖନ୍ତୁ ଓ ଆଗକୁ ବଢନ୍ତୁ}</h3>
                    <p>Access step-by-step video tutorials, learn about new design trends, and gain financial literacy to build your own brand and manage your business effectively.</p>
                    <a class="btn" data-target="tab-tutorials"><i class="fas fa-play-circle"></i> Watch Tutorials</a>
                    <a class="btn btn-secondary" data-target="tab-career" style="margin-left: 10px;"><i class="fas fa-lightbulb"></i> Career Guides</a>
                </div>
            </div>
        </section>

        <section id="schemes" class="feature-section" style="background-color: #fff; border: 1px solid var(--border-light); border-radius: 8px;">
            <h2 class="section-title" data-aos="fade-up">Find Your Perfect Scheme {AI ସ୍କିମ୍ ଫାଇଣ୍ଡର୍}</h2>
            <div style="max-width: 600px; margin: auto; text-align: center;" data-aos="fade-up" data-aos-delay="100">
                <p style="margin-top: -1em; margin-bottom: 2em;">Answer a few questions and our smart tool will find the best government schemes for loans, training, and support.</p>
                <button class="btn" data-target="tab-schemes"><i class="fas fa-magic"></i> Find My Schemes Now</button>
            </div>
        </section>
        
        <section id="sell" class="feature-section">
            <h2 class="section-title" data-aos="fade-up">Sell Your Craft {ନିଜ କଳା ବିକ୍ରି କରନ୍ତୁ}</h2>
            <p style="text-align:center; max-width:700px; margin:-1em auto 2em auto;" data-aos="fade-up" data-aos-delay="100">Get your own online storefront on Karigar's Hub. Showcase your products to a national audience and receive payments directly via UPI.</p>
             <div class="product-gallery"> 
                <div class="gallery-item" data-aos="zoom-in" data-aos-delay="100">
                    <img src="images/KH pic 2.jpg" alt="Woven craft 1">
                    <div class="gallery-overlay"><i class="fas fa-search"></i></div>
                </div>
                <div class="gallery-item" data-aos="zoom-in" data-aos-delay="200">
                    <img src="images/KH pic 3.jpg" alt="Woven craft 2">
                    <div class="gallery-overlay"><i class="fas fa-search"></i></div>
                </div>
                <div class="gallery-item" data-aos="zoom-in" data-aos-delay="300">
                    <img src="images/KH pic 4.jpg" alt="Woven craft 3">
                    <div class="gallery-overlay"><i class="fas fa-search"></i></div>
                </div>
                <div class="gallery-item" data-aos="zoom-in" data-aos-delay="400">
                    <img src="images/KH pic 1.jpg" alt="Woven craft 4">
                    <div class="gallery-overlay"><i class="fas fa-search"></i></div>
                </div>
             </div> 
        </section>
        
        <section id="register" class="feature-section" style="background-color: var(--primary-dark); color: var(--text-light); border-radius: 15px;">
            <div style="max-width: 600px; margin:auto; text-align: center;" data-aos="fade-up">
                <h2 class="section-title" style="color: var(--text-light);">Join Karigar Hub Today!</h2>
                <p style="opacity: 0.9;">{ଆଜି ହିଁ କାରିଗର ହବ୍‌ରେ ଯୋଗ ଦିଅନ୍ତୁ!}</p>
                <form style="margin-top: 2em;">
                    <input type="text" placeholder="Full Name {ପୂରା ନାମ}" required style="width:100%; padding:12px; margin-bottom:10px; border-radius:5px; border:none;">
                    <input type="tel" placeholder="Phone Number {ଫୋନ୍ ନମ୍ବର}" required style="width:100%; padding:12px; margin-bottom:10px; border-radius:5px; border:none;">
                    <input type="submit" value="Register Now {ପଞ୍ଜୀକରଣ କରନ୍ତୁ}" class="btn" style="width:100%;">
                </form>
            </div>
        </section>

    </div>

    <footer>
        <p>© 2025 Karigar's Hub | Designed to Uplift the Weavers of Taraboi.</p>
        <p>{© 2025 କାରିଗର ହବ୍ | ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ଉନ୍ନତି ପାଇଁ ପରିକଳ୍ପିତ।}</p>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize AOS
        AOS.init({
            duration: 800, // values from 0 to 3000, with step 50ms
            once: true, // whether animation should happen only once - while scrolling down
        });
        
        // Modal and other JS functionality remains the same
        document.addEventListener('DOMContentLoaded', function () {
            // ... (rest of the JS from previous version)
        });
    </script>
</body>
</html>
