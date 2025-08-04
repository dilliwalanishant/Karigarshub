<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Karigar's Hub | The Future of Craft</title>
    
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#111317">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700;800&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    
    <style>
        :root {
            --background: #111317;
            --surface: rgba(26, 29, 34, 0.6);
            --text-light: #F0F2F5;
            --text-secondary: #a8b3cf;
            --accent-blue: #40C4FF;
            --accent-glow: rgba(64, 196, 255, 0.2);
            --border-color: rgba(255, 255, 255, 0.1);

            --font-main: 'Poppins', sans-serif;
        }

        html { scroll-behavior: smooth; }

        body {
            font-family: var(--font-main);
            margin: 0;
            padding: 0;
            background-color: var(--background);
            color: var(--text-light);
            overflow-x: hidden;
        }
        
        /* Subtle Aurora Background Effect */
        body::before {
            content: '';
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 15% 25%, #1a2f4b 0%, var(--background) 25%),
                        radial-gradient(circle at 85% 75%, #3a1d4a 0%, var(--background) 25%);
            z-index: -1;
            animation: moveAurora 20s infinite alternate;
        }

        @keyframes moveAurora {
            from { transform: rotate(0deg) scale(1.2); }
            to { transform: rotate(360deg) scale(1.2); }
        }

        /* --- NAVIGATION --- */
        .main-nav {
            position: fixed;
            top: 0; left: 0; width: 100%;
            z-index: 1000;
            display: flex; justify-content: space-between; align-items: center;
            padding: 1.5em 3em;
            box-sizing: border-box;
            transition: background-color 0.3s, backdrop-filter 0.3s;
        }
        .main-nav.scrolled {
            background-color: rgba(17, 19, 23, 0.5);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border-color);
        }
        .nav-logo {
            width: 150px;
            height: auto;
        }
        .nav-links a {
            font-weight: 600; text-decoration: none;
            color: var(--text-light); padding: 0.5em 1em;
            margin: 0 0.5em; transition: color 0.3s;
        }
        .nav-links a:hover { color: var(--accent-blue); }

        /* --- HERO SECTION --- */
        .hero-section {
            height: 100vh;
            display: flex; flex-direction: column;
            justify-content: center; align-items: center;
            text-align: center; padding: 2em;
        }
        .hero-section h1 {
            font-size: 4.5em; font-weight: 800; margin: 0;
            background: linear-gradient(90deg, var(--text-light), var(--accent-blue));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient-text-flow 5s infinite ease-in-out;
        }
        @keyframes gradient-text-flow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        .hero-section p {
            font-size: 1.2em; max-width: 600px;
            margin: 1em 0 2em 0; color: var(--text-secondary);
        }
        
        .container { max-width: 1200px; margin: 0 auto; padding: 1em; }
        .feature-section { padding: 6em 2em; }
        .section-title {
            text-align: center; font-size: 3em; font-weight: 700;
            margin-bottom: 1.5em;
        }
        
        /* --- GLASSMORPHISM CARDS --- */
        .glass-card {
            background: var(--surface);
            backdrop-filter: blur(20px);
            border: 1px solid var(--border-color);
            border-radius: 15px;
            padding: 2.5em;
            box-shadow: 0 0 30px rgba(0,0,0,0.2);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .glass-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 0 50px var(--accent-glow);
        }

        .craft-process-container {
            display: flex; justify-content: space-around; flex-wrap: wrap;
            gap: 2em; text-align: center;
        }
        .craft-step { flex: 1; min-width: 280px; padding: 1em; }
        .craft-step .icon {
            font-size: 3em; margin-bottom: 0.5em; display: inline-block;
            color: var(--accent-blue);
            text-shadow: 0 0 15px var(--accent-glow);
        }
        .craft-step h3 { font-size: 1.8em; font-weight: 600; }
        .craft-step p { color: var(--text-secondary); }

        .overlapping-layout { display: flex; align-items: center; gap: 2em; margin: 4em 0; flex-wrap: wrap; }
        .overlap-text { flex: 1 1 400px; }
        .overlap-text h3 { font-size: 2em; font-weight: 700; margin-top: 0; }
        .overlap-image-stack { flex: 1 1 400px; position: relative; min-height: 350px; }
        .overlap-image-stack img {
            width: 70%; border-radius: 10px; position: absolute;
            border: 1px solid var(--border-color);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            transition: transform 0.4s;
        }
        .overlap-image-stack img:first-child { top: 0; left: 0; transform: rotate(-5deg); }
        .overlap-image-stack img:last-child { bottom: 0; right: 0; transform: rotate(5deg); }
        .overlap-image-stack:hover img { transform: rotate(0deg); }

        /* --- BUTTONS --- */
        .btn {
            display: inline-block; font-weight: 600;
            padding: 0.9em 2em;
            background: linear-gradient(45deg, var(--accent-blue), #00aaff);
            color: var(--background);
            text-decoration: none; border-radius: 50px;
            cursor: pointer; border: none;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 0 20px var(--accent-glow);
        }
        .btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 0 35px var(--accent-glow);
        }
        
        .product-gallery {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px; margin-top: 1.5em;
        }
        .gallery-item {
            position: relative; overflow: hidden; border-radius: 10px;
            border: 1px solid var(--border-color);
            transition: border-color 0.3s;
        }
        .gallery-item:hover { border-color: var(--accent-blue); }
        .gallery-item img {
            width: 100%; height: 100%; aspect-ratio: 1 / 1; object-fit: cover;
            transition: transform 0.4s ease;
        }
        .gallery-item:hover img { transform: scale(1.1); }
        
        footer {
            text-align: center; padding: 4em 2em;
            background-color: transparent;
            border-top: 1px solid var(--border-color);
            margin-top: 4em;
        }
        footer p { color: var(--text-secondary); }
        
        @media screen and (max-width: 768px) {
            .main-nav { padding: 1em; }
            .hero-section h1 { font-size: 2.8em; }
        }
    </style>
</head>
<body>

    <nav class="main-nav" id="main-nav">
        <a href="#home">
            <svg class="nav-logo" viewBox="0 0 150 40" xmlns="http://www.w3.org/2000/svg">
                <defs>
                    <linearGradient id="logoGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                        <stop offset="0%" style="stop-color:white;"/>
                        <stop offset="100%" style="stop-color:var(--accent-blue);"/>
                    </linearGradient>
                </defs>
                <path d="M10 5 L10 35 L20 35 L20 22 L30 35 L40 35 L30 20 L40 5 L30 5 L20 18 L20 5 Z" fill="url(#logoGradient)"/>
                <path d="M45 5 L45 35 L55 35 L55 5 Z M45 20 L55 20" stroke="url(#logoGradient)" stroke-width="5"/>
                <text x="65" y="28" font-family="Poppins, sans-serif" font-size="16" font-weight="600" fill="var(--text-light)">KARIGAR'S HUB</text>
            </svg>
        </a>
        <div class="nav-links">
            <a href="#art-of-weaving">The Craft</a>
            <a href="#learn">Learn</a>
            <a href="#sell">Sell</a>
            <a href="#register">Join Us</a>
        </div>
    </nav>

    <section class="hero-section" id="home">
        <h1 data-aos="fade-down">The Future of Craft is Here.</h1>
        <p data-aos="fade-up" data-aos-delay="200">A digital ecosystem designed for the artisans of Taraboi. We fuse timeless tradition with tomorrow's technology to empower your craft.</p>
        <a href="#art-of-weaving" class="btn" data-aos="fade-up" data-aos-delay="400">Explore the Vision</a>
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
                <div class="overlap-text" data-aos="fade-right">
                    <h2 class="section-title" style="text-align: left;">Learn & Grow.</h2>
                    <p style="color: var(--text-secondary); font-size: 1.1em;">Master your craft and your business. Access our library of video tutorials, get insights on new design trends, and learn financial skills to build a powerful, independent brand.</p>
                    <a class="btn" style="margin-top: 1em;">Access Learning Hub</a>
                </div>
                <div class="overlap-image-stack" data-aos="fade-left">
                    <img src="images/KH pic 2.jpg" alt="Artisan learning">
                    <img src="images/KH pic 3.jpg" alt="Artisan learning 2">
                </div>
            </div>
        </section>
        
        <section id="sell" class="feature-section">
            <h2 class="section-title" data-aos="fade-up">Your Global Storefront.</h2>
            <p style="text-align:center; max-width:700px; margin:-1em auto 2em auto; color: var(--text-secondary);" data-aos="fade-up" data-aos-delay="100">Launch your personal online store on the Hub. Showcase your unique creations to a worldwide audience and get paid instantly with direct UPI payments.</p>
             <div class="product-gallery"> 
                <div class="gallery-item" data-aos="zoom-in-up" data-aos-delay="100"><img src="images/KH pic 2.jpg" alt="Woven craft 1"></div>
                <div class="gallery-item" data-aos-="zoom-in-up" data-aos-delay="200"><img src="images/KH pic 3.jpg" alt="Woven craft 2"></div>
                <div class="gallery-item" data-aos="zoom-in-up" data-aos-delay="300"><img src="images/KH pic 4.jpg" alt="Woven craft 3"></div>
                <div class="gallery-item" data-aos="zoom-in-up" data-aos-delay="400"><img src="images/KH pic 1.jpg" alt="Woven craft 4"></div>
             </div> 
        </section>
        
        <section id="register" class="feature-section">
            <div class="glass-card" data-aos="zoom-in">
                <div style="max-width: 600px; margin:auto; text-align: center;">
                    <h2 class="section-title">Join the Movement.</h2>
                    <p style="color: var(--text-secondary); margin-top: -1em; margin-bottom: 2em;">Become a part of the Karigar's Hub ecosystem. Register today to unlock your potential and take your craft to the next level.</p>
                    <a href="#" class="btn" style="padding: 1em 3em; font-size: 1.1em;">Register Now {ପଞ୍ଜୀକରଣ କରନ୍ତୁ}</a>
                </div>
            </div>
        </section>

    </div>

    <footer>
        <p>© 2025 Karigar's Hub | Designed in Jamshedpur, India, for the Weavers of Taraboi.</p>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize Animate on Scroll
        AOS.init({
            duration: 800,
            once: true,
            offset: 50,
        });

        // Sticky navigation on scroll
        const nav = document.getElementById('main-nav');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                nav.classList.add('scrolled');
            } else {
                nav.classList.remove('scrolled');
            }
        });
    </script>
</body>
</html>
