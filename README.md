<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    
    <meta name="theme-color" content="#1D1C3B"/>
    <link rel="manifest" href="manifest.json">
    
    <title>KARIGAR's HUB</title>
    <style>
        body {
            font-family: 'Georgia', serif;
            margin: 0;
            padding: 0;
            background-color: #C5DCA2;
            color: #1D1C3B;
        }
        header {
            background-color: #1D1C3B;
            color: #FFFFFF;
            padding: 1em 2em;
            display: flex;
            align-items: center;
            flex-wrap: wrap; /* Allows wrapping on small screens */
        }
        .logo {
            width: 120px; /* Slightly smaller for better balance */
            height: auto;
            margin-right: 20px; /* Reduced margin */
        }
        .header-text {
            flex-grow: 1;
        }
        .voice-nav-icon { /* Style for the new microphone icon */
            font-size: 2em;
            cursor: pointer;
            margin-left: 20px;
            padding: 5px;
            border-radius: 50%;
            transition: background-color 0.3s;
        }
        .voice-nav-icon:hover {
            background-color: #4DB6AC;
        }
        h1 { margin: 0; }
        p { margin-top: 5px; }
        nav {
            background-color: #4DB6AC;
            padding: 1em;
            text-align: center;
            position: sticky; /* Makes nav bar stick to the top when scrolling */
            top: 0;
            z-index: 900;
        }
        nav a {
            text-decoration: none;
            color: #1D1C3B;
            padding: 0.5em 1em;
            background-color: #87CED9;
            border-radius: 5px;
            margin: 0.3em;
            display: inline-block;
            font-weight: bold;
            transition: background-color 0.3s;
        }
        nav a:hover { background-color: #FFFFFF; }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2em;
        }
        .feature-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-bottom: 2em;
            background-color: #ffffff50; /* Light background for sections */
            padding: 1.5em;
            border-radius: 10px;
        }
        .section-title {
            width: 100%;
            text-align: center;
            font-size: 2em;
            margin-bottom: 1em;
            color: #1D1C3B;
        }
        .feature {
            flex: 1 1 45%;
            margin: 1em;
            padding: 1.5em;
            background-color: #4DB6AC;
            border-radius: 8px;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        .feature h3 {
             margin-top:0;
        }
        .btn {
            display: inline-block;
            padding: 0.8em 1.5em; /* Larger button */
            background-color: #87CED9;
            color: #1D1C3B;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 1em;
            cursor: pointer;
            font-weight: bold;
            border: 2px solid #1D1C3B;
            transition: background-color 0.3s, color 0.3s;
        }
        .btn:hover {
            background-color: #1D1C3B;
            color: #FFFFFF;
        }
        footer {
            background-color: #1D1C3B;
            color: #FFFFFF;
            text-align: center;
            padding: 1.5em;
            font-size: 0.9em;
        }
        .content-tab {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(29, 28, 59, 0.8);
            padding-top: 50px;
        }
        .tab-inner-content {
            background-color: #C5DCA2;
            color: #1D1C3B;
            margin: 5% auto;
            padding: 40px;
            border: 2px solid #4DB6AC;
            width: 85%;
            max-width: 900px;
            border-radius: 10px;
            position: relative;
        }
        .close-btn {
            color: #1D1C3B;
            position: absolute;
            top: 10px;
            right: 25px;
            font-size: 35px;
            font-weight: bold;
            cursor: pointer;
        }
        .close-btn:hover,
        .close-btn:focus { color: #FFFFFF; }
        .video-container {
            position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; background: #000; margin: 1em 0;
        }
        .video-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
        .scheme-item, .event-item, .power-feature-item {
           border-bottom: 2px solid #87CED9; padding: 1em 0; margin-bottom: 1em;
        }
        .scheme-item:last-child, .event-item:last-child, .power-feature-item:last-child { border-bottom: none; }
        
        @media screen and (max-width: 768px) {
            .feature-section, header { flex-direction: column; align-items: center; text-align: center; }
            .logo { margin: 0 auto 10px auto; }
            nav a { display: block; margin: 0.5em auto; }
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
        <div class="voice-nav-icon" onclick="startVoiceNavigation()" title="Start Voice Navigation">🎤</div>
    </header>

    <nav>
        <a href="#power-features">Power Features {ମୁଖ୍ୟ ସୁବିଧା}</a>
        <a href="#learn">Learn & Grow {ଶିଖନ୍ତୁ ଓ ବଢନ୍ତୁ}</a>
        <a href="#schemes">Schemes {ଯୋଜନା}</a>
        <a href="#sell">Sell Your Craft {ବିକ୍ରି କରନ୍ତୁ}</a>
        <a href="#register">Join Us {ଯୋଗ ଦିଅନ୍ତୁ}</a>
    </nav>

    <div class="container">
        
        <section id="power-features" class="feature-section">
            <h2 class="section-title">Power Features {ମୁଖ୍ୟ ସୁବିଧା}</h2>
            <div class="feature">
                <h3>Offline Mode & Voice Control {ଅଫଲାଇନ୍ ମୋଡ୍ ଓ ଭଏସ୍ କଣ୍ଟ୍ରୋଲ୍}</h3>
                <p>Use the portal even with bad internet. Navigate hands-free using your voice in Odia.</p>
                <p>{ଖରାପ ଇଣ୍ଟରନେଟରେ ମଧ୍ୟ ପୋର୍ଟାଲ୍ ବ୍ୟବହାର କରନ୍ତୁ। ଓଡ଼ିଆରେ ନିଜ ସ୍ୱରରେ ହାତମୁକ୍ତ ଭାବେ ନାଭିଗେଟ୍ କରନ୍ତୁ।}</p>
                <a class="btn" data-target="tab-accessibility">Learn How {କିପରି ଜାଣନ୍ତୁ}</a>
            </div>
            <div class="feature">
                <h3>My Personal Store & UPI Payments {ମୋର ଦୋକାନ ଓ UPI ପେମେଣ୍ଟ}</h3>
                <p>Get your own e-commerce page. Create UPI QR codes instantly for cashless sales.</p>
                <p>{ନିଜର ଇ-କମର୍ସ ପେଜ୍ ପାଆନ୍ତୁ। କ୍ୟାସଲେସ୍ ବିକ୍ରି ପାଇଁ ତୁରନ୍ତ UPI QR କୋଡ୍ ତିଆରି କରନ୍ତୁ।}</p>
                <a class="btn" data-target="tab-mystore">Setup My Store {ମୋ ଦୋକାନ ସେଟ୍ କରନ୍ତୁ}</a>
            </div>
             <div class="feature">
                <h3>AI Scheme Advisor {AI ଯୋଜନା ପରାମର୍ଶଦାତା}</h3>
                <p>Answer simple questions and get a personalized checklist of schemes and loans you are eligible for.</p>
                <p>{ସରଳ ପ୍ରଶ୍ନର ଉତ୍ତର ଦିଅନ୍ତୁ ଏବଂ ଆପଣ ଯୋଗ୍ୟ ଥିବା ଯୋଜନା ଓ ଋଣର ଏକ ବ୍ୟକ୍ତିଗତ ତାଲିକା ପାଆନ୍ତୁ।}</p>
                <a class="btn" data-target="tab-ai-advisor">Find My Schemes {ମୋ ଯୋଜନା ଖୋଜନ୍ତୁ}</a>
            </div>
             <div class="feature">
                <h3>WhatsApp & Phone Support {WhatsApp ଓ ଫୋନ୍ ସହାୟତା}</h3>
                <p>Get instant answers and alerts on WhatsApp. Talk to our automated phone support anytime.</p>
                <p>{WhatsApp ରେ ତୁରନ୍ତ ଉତ୍ତର ଓ ଆଲର୍ଟ ପାଆନ୍ତୁ। ଆମର ସ୍ୱୟଂଚାଳିତ ଫୋନ୍ ସହାୟତା ସହ କେବେବି କଥା ହୁଅନ୍ତୁ।}</p>
                <a class="btn" data-target="tab-bots">Connect Now {ଏବେ ସଂଯୋଗ କରନ୍ତୁ}</a>
            </div>
        </section>

        <div id="tab-accessibility" class="content-tab">
            <div class="tab-inner-content">
                <span class="close-btn">×</span>
                <h2>Accessibility Features {ବ୍ୟବହାର ସୁବିଧା}</h2>
                <div class="power-feature-item">
                    <h3>Full Odia Voice Navigation (TTS/STT) {ସମ୍ପୂର୍ଣ୍ଣ ଓଡ଼ିଆ ଭଏସ୍ ନାଭିଗେସନ୍}</h3>
                    <p><strong>Benefit:</strong> Low-literacy artisans can navigate the entire website hands-free just by speaking commands in Odia. The website will also speak back to you.</p>
                    <p><strong>Technology:</strong> This uses open-source Text-to-Speech (TTS) and Speech-to-Text (STT) engines integrated into the browser via the Web Speech API.</p>
                </div>
                <div class="power-feature-item">
                    <h3>Progressive Web App (PWA) & Offline Caching {ପ୍ରୋଗ୍ରେସିଭ୍ ୱେବ୍ ଆପ୍ ଓ ଅଫଲାଇନ୍ କ୍ୟାଚିଂ}</h3>
                    <p><strong>Benefit:</strong> The portal works even with patchy or no internet connection. You can browse information, and any forms you fill will sync automatically when the signal returns.</p>
                    <p><strong>Technology:</strong> This is achieved by making the site a PWA. A 'Service Worker' script runs in the background to save important pages and data on your device for offline use.</p>
                </div>
            </div>
        </div>
        
        <div id="tab-mystore" class="content-tab">
            <div class="tab-inner-content">
                <span class="close-btn">×</span>
                <h2>My Personal Store & Payments {ମୋର ଦୋକାନ ଓ ପେମେଣ୍ଟ}</h2>
                <div class="power-feature-item">
                    <h3>E-commerce Micro-Storefronts {ଇ-କମର୍ସ ମାଇକ୍ରୋ-ଷ୍ଟୋରଫ୍ରଣ୍ଟ}</h3>
                    <p><strong>Benefit:</strong> Each registered artisan gets a simple, personal webpage to showcase their products, story, and contact information for direct B2C sales.</p>
                    <p><strong>Technology:</strong> This requires a back-end database to store artisan and product data. The website reads from this database to create a unique page for each artisan.</p>
                </div>
                <div class="power-feature-item">
                    <h3>Digital Payment Gateway & UPI QR Generation {ଡିଜିଟାଲ୍ ପେମେଣ୍ଟ ଗେଟୱେ ଓ UPI QR ଜେନେରେସନ୍}</h3>
                    <p><strong>Benefit:</strong> Faster, cash-less transactions at fairs or for online sales. Generate a unique UPI QR code for any amount instantly.</p>
                    <p><strong>Technology:</strong> This involves integrating with a payment gateway service like Razorpay or PhonePe. Their APIs allow us to create dynamic QR codes and confirm payments automatically.</p>
                    <img src="https://i.imgur.com/gA49n2c.png" alt="Sample UPI QR Code" style="max-width:200px; margin:1em auto; display:block;">
                </div>
            </div>
        </div>

        <div id="tab-ai-advisor" class="content-tab">
            <div class="tab-inner-content">
                <span class="close-btn">×</span>
                <h2>AI Scheme Advisor {AI ଯୋଜନା ପରାମର୍ଶଦାତା}</h2>
                <div class="power-feature-item">
                    <h3>AI-Driven Scheme Recommender {AI-ଚାଳିତ ଯୋଜନା ରେକମେଣ୍ଡର୍}</h3>
                    <p><strong>Benefit:</strong> No more confusion. The AI asks you simple questions (like your age, income, type of craft) and gives you a personalised checklist of government subsidies and bank loans you are most likely eligible for.</p>
                    <p><strong>Technology:</strong> This uses a combination of a rules-based engine for simple logic and a Machine Learning (ML) model on the back-end. The ML model can learn over time which schemes are most successful for different types of artisans.</p>
                </div>
            </div>
        </div>

        <div id="tab-bots" class="content-tab">
            <div class="tab-inner-content">
                <span class="close-btn">×</span>
                <h2>WhatsApp & Phone Support {WhatsApp ଓ ଫୋନ୍ ସହାୟତା}</h2>
                <div class="power-feature-item">
                    <h3>WhatsApp & IVR Bots {WhatsApp ଓ IVR ବଟ୍}</h3>
                    <p><strong>Benefit:</strong> Get instant answers, scheme alerts, and event notifications directly on your WhatsApp, a channel you are already familiar with. You can also call a number and interact with our automated IVR (Interactive Voice Response) system in Odia.</p>
                    <p><strong>Technology:</strong> This requires integrating with WhatsApp's Business API and a cloud telephony service (like Twilio or Exotel) for the IVR bot. These bots are connected to our main database for information.</p>
                </div>
            </div>
        </div>

        </div>

    <footer>
        <p>© 2025 Karigar's Hub | Designed to Uplift the Weavers of Taraboi.</p>
        <p>{© 2025 କାରିଗର ହବ୍ | ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ଉନ୍ନତି ପାଇଁ ପରିକଳ୍ପିତ।}</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const openButtons = document.querySelectorAll('.btn[data-target]');
            const closeButtons = document.querySelectorAll('.content-tab .close-btn');

            function openTab(tabId) {
                const tab = document.getElementById(tabId);
                if (tab) { tab.style.display = 'block'; }
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
        });

        // --- PLACEHOLDER FUNCTIONS FOR ADVANCED FEATURES ---

        function startVoiceNavigation() {
            // TODO: This would trigger the Web Speech API to start listening for Odia commands.
            alert("Voice Navigation Activated! (This is a demo)");
            console.log("Starting voice recognition...");
        }

        // PWA Installation Script (to be placed in a separate file, e.g., app.js)
        /*
        if ('serviceWorker' in navigator) {
            navigator.serviceWorker.register('/service-worker.js')
            .then((reg) => console.log('Service worker registered.', reg))
            .catch((err) => console.log('Service worker not registered.', err));
        }
        */
    </script>

</body>
</html>
