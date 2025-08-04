<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>KARIGAR's HUB</title>
    
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#1D1C3B">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        :root {
            --primary-dark: #1D1C3B;
            --primary-light: #FFFFFF;
            --accent-green: #4DB6AC;
            --accent-blue: #87CED9;
            --background-light: #C5DCA2;
            --background-section: #ffffff80;
        }

        body {
            font-family: 'Georgia', serif;
            margin: 0;
            padding: 0;
            background-color: var(--background-light);
            color: var(--primary-dark);
        }

        header {
            background-color: var(--primary-dark);
            color: var(--primary-light);
            padding: 1em 2em;
            display: flex;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            width: 120px;
            height: auto;
            margin-right: 20px;
            border-radius: 50%;
            border: 2px solid var(--accent-blue);
        }

        .header-text {
            flex-grow: 1;
        }

        h1, h2, h3 {
            margin: 0;
        }

        p {
            margin-top: 5px;
            line-height: 1.6;
        }

        nav {
            background-color: var(--accent-green);
            padding: 0.8em 1em;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 900;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
        }

        nav a {
            text-decoration: none;
            color: var(--primary-dark);
            padding: 0.5em 1em;
            background-color: var(--accent-blue);
            border-radius: 5px;
            margin: 0.3em;
            display: inline-block;
            font-weight: bold;
            transition: background-color 0.3s, transform 0.2s;
        }

        nav a:hover {
            background-color: var(--primary-light);
            transform: translateY(-2px);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2em;
        }

        .feature-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-bottom: 2.5em;
            background-color: var(--background-section);
            padding: 2em;
            border-radius: 15px;
            border: 1px solid var(--accent-green);
        }

        .section-title {
            width: 100%;
            text-align: center;
            font-size: 2.2em;
            margin-bottom: 1em;
            color: var(--primary-dark);
        }

        .feature {
            flex: 1 1 45%;
            margin: 1em;
            padding: 1.5em;
            background-color: var(--accent-green);
            color: var(--primary-light);
            border-radius: 8px;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .feature h3 {
             color: var(--primary-light);
             margin-bottom: 0.5em;
        }
        .feature p {
             color: var(--primary-dark);
        }
        .feature .icon {
            font-size: 3em;
            color: var(--accent-blue);
            margin-bottom: 0.5em;
        }


        .btn {
            display: inline-block;
            padding: 0.8em 1.5em;
            background-color: var(--accent-blue);
            color: var(--primary-dark);
            text-decoration: none;
            border-radius: 5px;
            margin-top: 1em;
            cursor: pointer;
            font-weight: bold;
            border: 2px solid var(--primary-dark);
            transition: background-color 0.3s, color 0.3s;
        }

        .btn:hover {
            background-color: var(--primary-dark);
            color: var(--primary-light);
        }

        footer {
            background-color: var(--primary-dark);
            color: var(--primary-light);
            text-align: center;
            padding: 2em;
            font-size: 0.9em;
        }
        footer p { margin-top: 0.5em; }

        /* MODAL (CONTENT TAB) STYLES */
        .content-tab {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0; top: 0;
            width: 100%; height: 100%;
            overflow: auto;
            background-color: rgba(29, 28, 59, 0.9);
            padding-top: 50px;
        }
        .tab-inner-content {
            background-color: var(--background-light);
            color: var(--primary-dark);
            margin: 5% auto;
            padding: 40px;
            border: 2px solid var(--accent-blue);
            width: 85%;
            max-width: 900px;
            border-radius: 10px;
            position: relative;
        }
        .close-btn {
            color: var(--primary-dark);
            position: absolute;
            top: 10px; right: 25px;
            font-size: 35px;
            font-weight: bold;
            cursor: pointer;
        }
        .close-btn:hover, .close-btn:focus { color: var(--accent-green); }

        .video-container {
            position: relative; padding-bottom: 56.25%; /* 16:9 */
            height: 0; overflow: hidden; max-width: 100%;
            background: #000; margin: 1em 0; border-radius: 8px;
        }
        .video-container iframe {
            position: absolute; top: 0; left: 0;
            width: 100%; height: 100%;
        }

        .info-item { /* Replaces scheme-item and event-item for consistency */
            border-bottom: 2px solid var(--accent-blue);
            padding: 1em 0; margin-bottom: 1em;
        }
        .info-item:last-child { border-bottom: none; }
        .info-item h3 { color: var(--primary-dark); }
        
        /* New AI Recommender Styles */
        .recommender-form {
            text-align: left; max-width: 600px; margin: auto;
            background: #fff; padding: 2em; border-radius: 10px;
        }
        .recommender-form label { display: block; margin: 10px 0 5px 0; font-weight: bold;}
        .recommender-form input, .recommender-form select {
            width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 5px; border: 1px solid #ccc;
        }
        
        /* Floating Support Button */
        .floating-support-hub {
            position: fixed;
            bottom: 25px;
            right: 25px;
            z-index: 950;
        }
        .floating-btn {
            width: 60px; height: 60px;
            background-color: var(--primary-dark);
            color: var(--primary-light);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.8em;
            cursor: pointer;
            box-shadow: 2px 2px 10px rgba(0,0,0,0.3);
            transition: transform 0.2s;
        }
        .floating-btn:hover { transform: scale(1.1); }
        .support-options {
            display: none;
            position: absolute;
            bottom: 70px; /* Position above the main button */
            right: 0;
            flex-direction: column;
        }
        .support-option {
            background-color: var(--accent-green);
            color: var(--primary-dark);
            padding: 10px 15px;
            margin-bottom: 10px;
            border-radius: 10px;
            text-decoration: none;
            display: flex;
            align-items: center;
            font-weight: bold;
            white-space: nowrap;
        }
        .support-option i { margin-right: 8px; }

        /* Responsive Design */
        @media screen and (max-width: 768px) {
            .feature-section { flex-direction: column; align-items: center; }
            header { flex-direction: column; text-align: center; }
            .logo { margin: 0 auto 10px auto; }
            nav a { display: block; width: 80%; margin: 0.5em auto; }
        }
    </style>
</head>
<body>

    <header>
        <img src="images/Karigar's hub logo.jpg" alt="Karigar's Hub Logo" class="logo">
        <div class="header-text">
            <h1>KARIGAR's HUB {କାରିଗର ହବ୍}</h1>
            <p>A Single Portal to Empower Weavers of Taraboi {ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ସଶକ୍ତ କରିବା ପାଇଁ ଏକକ ପୋର୍ଟାଲ୍}</p>
        </div>
    </header>

    <nav>
        <a href="#about"><i class="fas fa-info-circle"></i> About</a>
        <a href="#learn"><i class="fas fa-graduation-cap"></i> Learn</a>
        <a href="#schemes"><i class="fas fa-search-dollar"></i> Find Schemes</a>
        <a href="#sell"><i class="fas fa-store"></i> Sell Craft</a>
        <a href="#education"><i class="fas fa-book-reader"></i> For Children</a>
        <a href="#register"><i class="fas fa-user-plus"></i> Join Us</a>
        <a href="#" id="voice-assist-btn" title="Odia Voice Assistance">
            <i class="fas fa-microphone-alt"></i> Voice Assist {ଭଏସ୍}
        </a>
    </nav>

    <div class="container">
        
        <section id="about" class="feature-section">
            <div class="feature" style="flex: 1 1 100%; text-align:center;">
                <h2><i class="fas fa-bullseye"></i> Our Mission {ଆମର ଲକ୍ଷ୍ୟ}</h2>
                <p>To provide the weavers of Taraboi with the digital tools, knowledge, and platform needed to grow their craft, improve their livelihood, and stand on their own feet. We aim to connect tradition with technology.</p>
                <p>{ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ଡିଜିଟାଲ୍ ଉପକରଣ, ଜ୍ଞାନ ଏବଂ ପ୍ଲାଟଫର୍ମ ପ୍ରଦାନ କରିବା ଯାହା ସେମାନଙ୍କର କଳାକୁ ବଢ଼ାଇବା, ଜୀବିକା ଉନ୍ନତ କରିବା ଏବଂ ନିଜ ଗୋଡ଼ରେ ଛିଡ଼ା ହେବା ପାଇଁ ଆବଶ୍ୟକ। ଆମର ଲକ୍ଷ୍ୟ ହେଉଛି ପରମ୍ପରାକୁ ପ୍ରଯୁକ୍ତିବିଦ୍ୟା ସହିତ ଯୋଡ଼ିବା।}</p>
                <img src="images/KH pic 1.jpg" style="width: 80%; max-width: 500px; border-radius: 10px; margin: 1em auto;">
            </div>
        </section>

        <section id="learn" class="feature-section">
            <h2 class="section-title">Learn & Grow {ଶିଖନ୍ତୁ ଓ ଆଗକୁ ବଢନ୍ତୁ}</h2>
            <div class="feature">
                <i class="fas fa-video icon"></i>
                <h3>Tutorial Videos {ଟ୍ୟୁଟୋରିଆଲ୍ ଭିଡିଓ}</h3>
                <p>Step-by-step video guides in Odia to help you with everything you need.</p>
                <a class="btn" data-target="tab-tutorials"><i class="fas fa-play-circle"></i> Watch Videos</a>
            </div>
            <div class="feature">
                <i class="fas fa-chart-line icon"></i>
                <h3>Build Your Career {ନିଜ କ୍ୟାରିୟର ଗଢନ୍ତୁ}</h3>
                <p>Learn new designs, manage money, and build your own brand online.</p>
                <a class="btn" data-target="tab-career"><i class="fas fa-lightbulb"></i> Learn More</a>
            </div>
        </section>

        <section id="schemes" class="feature-section">
            <h2 class="section-title">AI Scheme Finder {AI ସ୍କିମ୍ ଫାଇଣ୍ଡର୍}</h2>
            <div class="feature" style="flex: 1 1 100%; background-color: var(--primary-light); color: var(--primary-dark);">
                 <h3>Find Your Perfect Scheme {ଆପଣଙ୍କ ପାଇଁ ସଠିକ୍ ଯୋଜନା ଖୋଜନ୍ତୁ}</h3>
                 <p>Answer a few questions and our AI tool will suggest the best government schemes for you. {କିଛି ପ୍ରଶ୍ନର ଉତ୍ତର ଦିଅନ୍ତୁ ଏବଂ ଆମର AI ଉପକରଣ ଆପଣଙ୍କ ପାଇଁ ସର୍ବୋତ୍ତମ ସରକାରୀ ଯୋଜନାଗୁଡିକର ପରାମର୍ଶ ଦେବ।}</p>
                 <div class="recommender-form">
                     <label for="age">What is your age? {ଆପଣଙ୍କ ବୟସ କେତେ?}</label>
                     <input type="number" id="age" name="age" placeholder="e.g., 45">
                     <label for="need">What do you need help with? {ଆପଣଙ୍କୁ କେଉଁଥିରେ ସାହାଯ୍ୟ ଦରକାର?}</label>
                     <select id="need" name="need">
                         <option value="loan">Loan for Business (ବ୍ୟବସାୟ ପାଇଁ ଋଣ)</option>
                         <option value="training">New Design Training (ନୂଆ ଡିଜାଇନ୍ ତାଲିମ)</option>
                         <option value="pension">Pension for Old Age (ବୃଦ୍ଧାବସ୍ଥା ପାଇଁ ପେନସନ)</option>
                         <option value="education">Child's Education (ପିଲାର ଶିକ୍ଷା)</option>
                     </select>
                     <button class="btn" style="width: 100%; margin-top: 15px;"><i class="fas fa-magic"></i> Find My Schemes</button>
                 </div>
                 <hr style="margin: 1.5em 0;">
                 <a class="btn" data-target="tab-schemes"><i class="fas fa-list-ul"></i> View All Government Schemes</a>
                 <a class="btn" data-target="tab-loans" style="margin-left: 10px;"><i class="fas fa-university"></i> View Bank Loan Info</a>
            </div>
        </section>

        <section id="sell" class="feature-section">
            <h2 class="section-title">Your Online Shop {ଆପଣଙ୍କ ଅନଲାଇନ୍ ଦୋକାନ}</h2>
            <div class="feature" style="flex: 1 1 55%;">
                <i class="fas fa-store-alt icon"></i>
                <h3>Micro-Storefronts for Artisans {କାରିଗରଙ୍କ ପାଇଁ ମାଇକ୍ରୋ-ଷ୍ଟୋରଫ୍ରଣ୍ଟ}</h3>
                <p>Register to get your own personal webpage on Karigar's Hub. Showcase your products, tell your story, and sell directly to customers all over India.</p>
                <p>{ପଞ୍ଜୀକରଣ କରନ୍ତୁ ଏବଂ କାରିଗର ହବ୍‌ରେ ନିଜର ବ୍ୟକ୍ତିଗତ ୱେବପେଜ୍ ପାଆନ୍ତୁ। ଆପଣଙ୍କ ଉତ୍ପାଦ ପ୍ରଦର୍ଶନ କରନ୍ତୁ, ନିଜ କାହାଣୀ କୁହନ୍ତୁ, ଏବଂ ସାରା ଭାରତର ଗ୍ରାହକଙ୍କୁ ସିଧାସଳଖ ବିକ୍ରି କରନ୍ତୁ।}</p>
                <a href="#register" class="btn"><i class="fas fa-user-plus"></i> Create Your Shop</a>
            </div>
            <div class="feature" style="flex: 1 1 35%;">
                <i class="fas fa-qrcode icon"></i>
                <h3>Direct UPI Payments {ସିଧା UPI ପେମେଣ୍ଟ}</h3>
                <p>We create a unique UPI QR code for your shop. Customers can scan and pay you directly, instantly. No extra fees!</p>
                <p>{ଆମେ ଆପଣଙ୍କ ଦୋକାନ ପାଇଁ ଏକ ସ୍ୱତନ୍ତ୍ର UPI QR କୋଡ୍ ତିଆରି କରୁ। ଗ୍ରାହକମାନେ ସ୍କାନ୍ କରି ସିଧା ଆପଣଙ୍କୁ ଟଙ୍କା ପଠାଇ ପାରିବେ।}</p>
                <img src="https://i.ibb.co/9vGo2j3/qr-code-generic.png" alt="Sample QR Code" style="width: 150px; margin: 1em auto; border-radius: 8px;">
            </div>
        </section>
        
        <section id="education" class="feature-section">
            <h2 class="section-title">Future for Our Children {ଆମ ପିଲାମାନଙ୍କ ପାଇଁ ଭବିଷ୍ୟତ}</h2>
            <div class="feature">
                <i class="fas fa-graduation-cap icon"></i>
                <h3>Scholarships & Support {ଛାତ୍ରବୃତ୍ତି ଓ ସହାୟତା}</h3>
                <p>Find government scholarships for your children's education, from school to college.</p>
                <a class="btn" data-target="tab-education"><i class="fas fa-search-dollar"></i> Find Scholarships</a>
            </div>
            <div class="feature">
                <i class="fas fa-compass-drafting icon"></i>
                <h3>Career Pathways {କ୍ୟାରିୟର୍ ପଥ}</h3>
                <p>Explore modern careers in design, technology, and business that build on your traditional skills.</p>
                <a class="btn" data-target="tab-education"><i class="fas fa-road"></i> Explore Careers</a>
            </div>
        </section>
        
        <section id="support" class="feature-section">
            <h2 class="section-title">Partners & Support {ସହଯୋଗୀ ଓ ସହାୟତା}</h2>
            <div class="feature">
                <i class="fas fa-calendar-alt icon"></i>
                <h3>Events & Fairs {ମେଳା ଓ ଇଭେଣ୍ଟ}</h3>
                <p>Find out about upcoming handloom events and craft fairs to sell your products.</p>
                <a class="btn" data-target="tab-events"><i class="fas fa-list"></i> View Event List</a>
            </div>
             <div class="feature">
                <i class="fas fa-hands-helping icon"></i>
                <h3>NGO Partners {ଏନଜିଓ ସହଯୋଗୀ}</h3>
                <p>Connect with non-profit organizations working to empower artisans in Odisha.</p>
                 <a class="btn" data-target="tab-partners"><i class="fas fa-link"></i> Connect with NGOs</a>
            </div>
        </section>
        
        <section id="register" class="feature-section">
            <h2 class="section-title">Join Karigar Hub Today! {ଆଜି ହିଁ କାରିଗର ହବ୍‌ରେ ଯୋଗ ଦିଅନ୍ତୁ!}</h2>
            <div class="feature" style="flex: 1 1 100%; background: var(--primary-light); color: var(--primary-dark);">
                <form style="text-align: left; max-width: 500px; margin: auto;">
                    <label for="name">Full Name {ପୂରା ନାମ}:</label>
                    <input type="text" id="name" name="name" required style="width: 100%; padding: 8px; margin: 6px 0; border-radius: 4px; border: 1px solid #ccc;"><br>
                    <label for="contact">Phone Number {ଫୋନ୍ ନମ୍ବର}:</label>
                    <input type="tel" id="contact" name="contact" required style="width: 100%; padding: 8px; margin: 6px 0; border-radius: 4px; border: 1px solid #ccc;"><br>
                    <label for="location">Village/Address {ଗାଁ/ଠିକଣା}:</label>
                    <input type="text" id="location" name="location" value="Taraboi" style="width: 100%; padding: 8px; margin: 6px 0; border-radius: 4px; border: 1px solid #ccc;"><br>
                    <label for="craft">Type of Weaving {ବୁଣାକାର୍ଯ୍ୟର ପ୍ରକାର}:</label>
                    <input type="text" id="craft" name="craft" placeholder="e.g., Bomkai, Sambalpuri" style="width: 100%; padding: 8px; margin: 6px 0; border-radius: 4px; border: 1px solid #ccc;"><br>
                    <input type="submit" value="Register Now {ବର୍ତ୍ତମାନ ପଞ୍ଜୀକରଣ କରନ୍ତୁ}" class="btn" style="width: 100%; font-size: 1.2em; margin-top: 10px;">
                </form>
            </div>
        </section>

    </div>

    <footer>
        <p><i class="fas fa-cloud-download-alt"></i> Portal works even with a weak signal. Install the app for offline use! {କମ୍ ସିଗନାଲରେ ବି ପୋର୍ଟାଲ୍ କାମ କରେ। ଅଫଲାଇନ୍ ବ୍ୟବହାର ପାଇଁ ଆପ୍ ଇନଷ୍ଟଲ୍ କରନ୍ତୁ!}</p>
        <p>© 2025 Karigar's Hub | Designed to Uplift the Weavers of Taraboi.</p>
        <p>{© 2025 କାରିଗର ହବ୍ | ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ଉନ୍ନତି ପାଇଁ ପରିକଳ୍ପିତ।}</p>
    </footer>

    <div id="tab-tutorials" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Tutorial Videos {ଟ୍ୟୁଟୋରିଆଲ୍ ଭିଡିଓ}</h2>
            <div class="info-item">
                <h3>How to Use UPI (PhonePe/Google Pay) {UPI କିପରି ବ୍ୟବହାର କରିବେ}</h3>
                <p>This video explains how to receive money from customers using a QR code on your phone. {ଏହି ଭିଡିଓରେ, ଆପଣଙ୍କ ଫୋନରେ QR କୋଡ୍ ବ୍ୟବହାର କରି ଗ୍ରାହକଙ୍କଠାରୁ କିପରି ଟଙ୍କା ଗ୍ରହଣ କରିବେ ତାହା ବୁଝାଯାଇଛି।}</p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/your-upi-tutorial-video-id" title="UPI Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="info-item">
                <h3>How to Register for an Artisan Card {କାରିଗର କାର୍ଡ ପାଇଁ କିପରି ପଞ୍ଜୀକରଣ କରିବେ}</h3>
                <p>This video shows you step-by-step how to fill the form on the government portal.</p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/your-artisan-card-video-id" title="Artisan Card Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="info-item">
                <h3>How to Take Good Photos of Your Products {ଉତ୍ପାଦର ଭଲ ଫଟୋ କିପରି ଉଠାଇବେ}</h3>
                <p>Learn how to use any mobile phone to take clear photos of your sarees to attract customers.</p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/your-photography-video-id" title="Product Photography Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </div>
    
    <div id="tab-career" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Build Your Career {ନିଜ କ୍ୟାରିୟର ଗଢନ୍ତୁ}</h2>
            <div class="info-item">
                <h3>New Design Ideas {ନୂଆ ଡିଜାଇନ୍ ବିଚାର}</h3>
                <p>Learn about new color combinations and patterns that are popular. We will share new design books and ideas here every month.</p>
            </div>
            <div class="info-item">
                <h3>Financial Literacy {ଆର୍ଥିକ ସାକ୍ଷରତା}</h3>
                <p>Learn how to open a bank account, use digital payments, and why saving is important. We will organize local workshops for this.</p>
            </div>
        </div>
    </div>

    <div id="tab-schemes" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Government Schemes {ସରକାରୀ ଯୋଜନା}</h2>
            <div class="info-item">
                <h3>National Handloom Development Programme (NHDP)</h3>
                <p><strong>Benefit:</strong> Financial assistance for looms, accessories, and skill upgradation.</p>
                <a href="https://handlooms.nic.in/" target="_blank" class="btn">Official Portal</a>
            </div>
            <div class="info-item">
                <h3>Pradhan Mantri Weavers MUDRA Scheme</h3>
                <p><strong>Benefit:</strong> Loans at 6% interest rate for working capital.</p>
                <a href="https://www.mudra.org.in/" target="_blank" class="btn">Learn More</a>
            </div>
            <div class="info-item">
                <h3>"Baristha Bunakar Sahayata Yojana" (Odisha State Scheme)</h3>
                <p><strong>Benefit:</strong> Monthly financial assistance for weavers above the age of 60.</p>
                <a href="https://handloom.odisha.gov.in/schemes/" target="_blank" class="btn">State Portal</a>
            </div>
        </div>
    </div>
    
    <div id="tab-education" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>For Our Children {ଆମ ପିଲାମାନଙ୍କ ପାଇଁ}</h2>
             <div class="info-item">
                <h3>Scholarships for Children {ପିଲାମାନଙ୍କ ପାଇଁ ଛାତ୍ରବୃତ୍ତି}</h3>
                <p>The government provides financial support for the education of artisans' children. You can apply for these schemes on the National Scholarship Portal (NSP).</p>
                 <p><strong>Major Scheme:</strong> Scholarship to Children of Beedi/Cine/IOMC/LSDM Workers. Many weaver families are eligible under this.</p>
                <a href="https://scholarships.gov.in/" target="_blank" class="btn"><i class="fas fa-external-link-alt"></i> Go to National Scholarship Portal</a>
            </div>
             <div class="info-item">
                <h3>Career Pathways in Design & Technology {ଡିଜାଇନ୍ ଓ ଟେକ୍ନୋଲୋଜିରେ କ୍ୟାରିୟର୍}</h3>
                 <p>If your children are interested in art and computers, they can have a great career. They can combine traditional weaving knowledge with modern skills.</p>
                <ul>
                    <li><strong>Fashion/Textile Design:</strong> They can study at colleges like NIFT to become designers.</li>
                    <li><strong>Digital Marketing:</strong> They can learn how to sell handloom products online on websites like Amazon, or on Instagram.</li>
                    <li><strong>Graphic Design:</strong> They can create new 'bandha' patterns using computer software.</li>
                </ul>
            </div>
        </div>
    </div>

    <div id="tab-loans" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Bank Loans & Financial Support {ବ୍ୟାଙ୍କ ଋଣ ଓ ଆର୍ଥିକ ସହାୟତା}</h2>
            <p>Banks offer special loans for artisans under the MUDRA scheme. We can help you connect with the nearest bank and assist with the application.</p>
            <p><strong>Banks providing MUDRA loans:</strong></p>
            <ul><li>State Bank of India (SBI)</li><li>Punjab National Bank (PNB)</li><li>Utkal Grameen Bank</li><li>Bandhan Bank</li></ul>
        </div>
    </div>
    
    <div id="tab-events" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Upcoming Events & Fairs {ଆଗାମୀ ମେଳା ଓ ଇଭେଣ୍ଟ}</h2>
            <div class="info-item">
                <h3>Toshali National Crafts Mela, Bhubaneswar</h3>
                <p><strong>When:</strong> Usually in December. We will provide updates when dates are announced.</p>
            </div>
            <div class="info-item">
                <h3>Dilli Haat, New Delhi - Odisha Handloom Stall</h3>
                <p><strong>When:</strong> Dates are announced by the Handloom department. We will notify you.</p>
            </div>
        </div>
    </div>
    
    <div id="tab-partners" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Our NGO Partners {ଆମର ଏନଜିଓ ସହଯୋଗୀ}</h2>
            <p>These organizations work to support and empower handloom artisans in Odisha.</p>
            <div class="info-item">
                <h3>Odisha Rural Development and Marketing Society (ORMAS)</h3>
                <p>Helps artisans with marketing, skill development, and forming self-help groups (SHGs).</p>
                <a href="#" class="btn">Learn More</a>
            </div>
            <div class="info-item">
                <h3>Gramin Vikas Sewa Sansthan</h3>
                <p>Focuses on livelihood promotion and providing training to weavers in rural areas.</p>
                <a href="#" class="btn">Learn More</a>
            </div>
        </div>
    </div>

    <div class="floating-support-hub">
        <div class="support-options" id="support-options-menu">
            <a href="https://wa.me/910000000000?text=Hello%20Karigar's%20Hub,%20I%20need%20help." target="_blank" class="support-option"><i class="fab fa-whatsapp"></i> WhatsApp Help</a>
            <a href="tel:+910000000000" class="support-option"><i class="fas fa-phone-alt"></i> Call for IVR Help</a>
        </div>
        <div class="floating-btn" id="main-support-btn">
            <i class="fas fa-headset"></i>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            // Modal/Tab functionality
            const openButtons = document.querySelectorAll('.btn[data-target]');
            const closeButtons = document.querySelectorAll('.content-tab .close-btn');

            function openTab(tabId) {
                const tab = document.getElementById(tabId);
                if (tab) {
                    tab.style.display = 'block';
                }
            }
            
            openButtons.forEach(button => {
                button.addEventListener('click', function (event) {
                    event.preventDefault();
                    const targetTabId = this.getAttribute('data-target');
                    openTab(targetTabId);
                });
            });

            closeButtons.forEach(button => {
                button.addEventListener('click', function () {
                    this.closest('.content-tab').style.display = 'none';
                });
            });

            window.addEventListener('click', function (event) {
                if (event.target.classList.contains('content-tab')) {
                    event.target.style.display = 'none';
                }
            });

            // Floating Support Hub functionality
            const mainSupportBtn = document.getElementById('main-support-btn');
            const supportOptionsMenu = document.getElementById('support-options-menu');
            
            mainSupportBtn.addEventListener('click', function() {
                if (supportOptionsMenu.style.display === 'flex') {
                    supportOptionsMenu.style.display = 'none';
                } else {
                    supportOptionsMenu.style.display = 'flex';
                }
            });
            
            // This is a placeholder for the PWA install prompt.
            // A real PWA would have a more complex service worker.
            // You would need a sw.js and manifest.json file.
        });
        
        // This is a stub for Voice Navigation. A real implementation
        // would require the Web Speech API.
        const voiceAssistBtn = document.getElementById('voice-assist-btn');
        voiceAssistBtn.addEventListener('click', (e) => {
            e.preventDefault();
            alert("Voice Assistance Feature Coming Soon!\n{ଭଏସ୍ ସହାୟତା ବୈଶିଷ୍ଟ୍ୟ ଶୀଘ୍ର ଆସୁଛି!}");
        });

    </script>
    <script src="sw.js"></script>
</body>
</html>
