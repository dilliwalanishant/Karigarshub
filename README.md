<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title data-key="pageTitle">KARIGAR's HUB</title>
    
    <link rel="manifest" href='data:application/manifest+json;base64,ewogICAgIm5hbWUiOiAiS2FyaWdhcidzIEh1YiIsCiAgICAic2hvcnRfbmFtZSI6ICJLYXJpZ2FySHViIiwKICAgICJpY29ucyI6IFsKICAgICAgICB7CiAgICAgICAgICAgICJzcmMiOiAiaW1hZ2VzL2ljb24tMTkyLnBuZyIsCiAgICAgICAgICAgICJ0eXBlIjogImltYWdlL3BuZyIsCiAgICAgICAgICAgICJzaXplcyI6ICIxOTJ4MTkyIgogICAgICAgIH0sCiAgICAgICAgewogICAgICAgICAgICAic3JjIjogImltYWdlcy9pY29uLTUxMi5wbmciLAogICAgICAgICAgICAidHlwZSI6ICJpbWFnZS9wbmciLAogICAgICAgICAgICAic2l6ZXMiOiAiNTEyeDUxMiIKICAgICAgICB9CiAgICBdLAogICAgInN0YXJ0X3VybCI6ICIvIiwKICAgICJkaXNwbGF5IjogInN0YW5kYWxvbmUiLAogICAgInRoZW1lX2NvbG9yIjogIiMxRDFDM0IiLAogICAgImJhY2tncm91bmRfY29sb3IiOiAiI0M1RENBMiIKfQ=='>
    <meta name="theme-color" content="#1D1C3B">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        :root {
            --primary-dark: #1D1C3B;
            --primary-light: #FFFFFF;
            --accent-green: #4DB6AC;
            --accent-blue: #87CED9;
            --background-light: #f0f4f8; /* Softer background */
            --background-section: #ffffff;
            --highlight-yellow: #ffc107;
        }
        html { scroll-behavior: smooth; }
        body {
            font-family: 'Georgia', serif;
            margin: 0; padding: 0;
            background-color: var(--background-light);
            color: var(--primary-dark);
        }
        header {
            background-color: var(--primary-dark); color: var(--primary-light);
            padding: 1em 2em; display: flex; align-items: center; flex-wrap: wrap;
        }
        .logo {
            width: 120px; height: auto; margin-right: 20px;
            border-radius: 50%; border: 2px solid var(--accent-blue);
        }
        .header-text { flex-grow: 1; }
        h1, h2, h3 { margin: 0; }
        p { margin-top: 5px; line-height: 1.6; }
        nav {
            background-color: var(--accent-green); padding: 0.8em 1em;
            text-align: center; position: sticky; top: 0;
            z-index: 900; display: flex; justify-content: center;
            align-items: center; flex-wrap: wrap;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        nav a {
            text-decoration: none; color: var(--primary-dark);
            padding: 0.5em 1em; background-color: var(--accent-blue);
            border-radius: 5px; margin: 0.3em; display: inline-flex;
            align-items: center; gap: 8px;
            font-weight: bold; transition: all 0.3s;
        }
        nav a:hover, nav a.active {
            background-color: var(--primary-light);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.15);
        }
        .container { max-width: 1200px; margin: 0 auto; padding: 2em; }
        .feature-section {
            display: flex; flex-wrap: wrap; justify-content: space-around;
            margin-bottom: 2.5em; background-color: var(--background-section);
            padding: 2em; border-radius: 15px;
            border: 1px solid #ddd;
        }
        .event-section {
            background-color: var(--primary-dark);
            color: var(--primary-light);
            border: 2px solid var(--highlight-yellow);
            text-align: center;
        }
        .event-section .icon { color: var(--highlight-yellow); }
        .event-section h2 { color: var(--primary-light); }
        .event-section p { color: #e0e0e0; }
        
        .section-title {
            width: 100%; text-align: center; font-size: 2.2em;
            margin-bottom: 1em; color: var(--primary-dark);
        }
        .feature {
            flex: 1 1 45%; margin: 1em; padding: 1.5em;
            background-color: var(--accent-green); color: var(--primary-light);
            border-radius: 8px; text-align: center; display: flex;
            flex-direction: column; justify-content: space-between;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .feature h3 { color: var(--primary-light); margin-bottom: 0.5em; }
        .feature p { color: var(--primary-dark); }
        .feature .icon { font-size: 3em; color: var(--accent-blue); margin-bottom: 0.5em; }
        .btn {
            display: inline-block; padding: 0.8em 1.5em;
            background-color: var(--accent-blue); color: var(--primary-dark);
            text-decoration: none; border-radius: 5px; margin-top: 1em;
            cursor: pointer; font-weight: bold; border: 2px solid var(--primary-dark);
            transition: background-color 0.3s, color 0.3s;
        }
        .btn.btn-primary { background-color: var(--highlight-yellow); color: var(--primary-dark); border-color: var(--primary-dark);}
        .btn:hover { background-color: var(--primary-dark); color: var(--primary-light); }

        footer {
            background-color: var(--primary-dark); color: var(--primary-light);
            text-align: center; padding: 2em; font-size: 0.9em;
        }
        footer p { margin-top: 0.5em; }

        /* MODAL STYLES */
        .modal {
            display: none; position: fixed; z-index: 1000;
            left: 0; top: 0; width: 100%; height: 100%;
            overflow: auto; background-color: rgba(29, 28, 59, 0.9);
            padding-top: 50px;
        }
        .modal-content {
            background-color: var(--background-light); color: var(--primary-dark);
            margin: 5% auto; padding: 40px; border: 2px solid var(--accent-blue);
            width: 85%; max-width: 900px; border-radius: 10px; position: relative;
        }
        .close-btn {
            color: var(--primary-dark); position: absolute; top: 10px; right: 25px;
            font-size: 35px; font-weight: bold; cursor: pointer;
        }
        .close-btn:hover, .close-btn:focus { color: var(--accent-green); }
        .video-container {
            position: relative; padding-bottom: 56.25%; height: 0;
            overflow: hidden; max-width: 100%; background: #000;
            margin: 1em 0; border-radius: 8px;
        }
        .video-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
        .info-item { border-bottom: 2px solid var(--accent-blue); padding: 1em 0; margin-bottom: 1em; }
        .info-item:last-child { border-bottom: none; }
        .info-item h3 { color: var(--primary-dark); }
        .portal-list ul { list-style: none; padding: 0;}
        .portal-list li { background: #fff; margin-bottom: 10px; padding: 15px; border-radius: 8px; border-left: 5px solid var(--accent-green); }
        .portal-list li a { font-weight: bold; }
        
        /* LANGUAGE TOGGLE SWITCH */
        .lang-switch { display: flex; align-items: center; margin-left: 20px; }
        .lang-switch label { margin: 0 5px; font-weight: bold; color: var(--primary-dark); }
        .switch { position: relative; display: inline-block; width: 50px; height: 24px; }
        .switch input { opacity: 0; width: 0; height: 0; }
        .slider { position: absolute; cursor: pointer; top: 0; left: 0; right: 0; bottom: 0; background-color: var(--accent-blue); transition: .4s; border-radius: 24px; }
        .slider:before { position: absolute; content: ""; height: 18px; width: 18px; left: 3px; bottom: 3px; background-color: white; transition: .4s; border-radius: 50%; }
        input:checked + .slider { background-color: var(--primary-dark); }
        input:checked + .slider:before { transform: translateX(26px); }

        /* VOICE & CHATBOT STYLES */
        .floating-support-hub { position: fixed; bottom: 25px; right: 25px; z-index: 950; }
        .floating-btn {
            width: 60px; height: 60px; background-color: var(--primary-dark);
            color: var(--primary-light); border-radius: 50%; display: flex;
            justify-content: center; align-items: center; font-size: 1.8em;
            cursor: pointer; box-shadow: 2px 2px 10px rgba(0,0,0,0.3);
            transition: transform 0.2s;
        }
        .floating-btn:hover { transform: scale(1.1); }

        #chatbot-container {
            display: none; position: fixed; bottom: 100px; right: 25px;
            width: 350px; height: 500px; background: white;
            border-radius: 15px; box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            z-index: 998; flex-direction: column; overflow: hidden;
        }
        #chatbot-header {
            background: var(--primary-dark); color: white; padding: 15px;
            font-weight: bold; font-size: 1.2em; display: flex;
            justify-content: space-between; align-items: center;
        }
        #close-chatbot-btn { cursor: pointer; font-size: 1.2em; }
        #chatbot-messages { flex-grow: 1; padding: 15px; overflow-y: auto; background: var(--background-light); }
        .bot-message, .user-message {
            padding: 10px 15px; border-radius: 18px; margin-bottom: 10px;
            max-width: 80%; line-height: 1.4;
        }
        .bot-message { background: #e9ecef; color: var(--primary-dark); align-self: flex-start; }
        .user-message { background: var(--accent-blue); color: var(--primary-dark); align-self: flex-end; margin-left: auto; }
        #chatbot-faq-options { padding: 10px; border-top: 1px solid #ddd; }
        .faq-btn {
            width: 100%; background: var(--accent-blue); color: var(--primary-dark);
            border: none; padding: 10px; border-radius: 8px; margin-bottom: 8px;
            text-align: left; cursor: pointer; font-family: 'Georgia', serif; font-weight: bold;
        }
        #voice-popup {
            display: none; flex-direction: column; justify-content: center; align-items: center;
            position: fixed; z-index: 2000; left: 0; top: 0; width: 100%; height: 100%;
            background-color: rgba(29, 28, 59, 0.95);
        }
    </style>
</head>
<body>

    <header>
        <img src="images/karigars_hub_logo.jpg" alt="Karigar's Hub Logo" class="logo">
        <div class="header-text">
            <h1 data-key="headerTitle"></h1>
            <p data-key="headerSubtitle"></p>
        </div>
    </header>

    <nav>
        <a href="#about" data-key="navAbout"><i class="fas fa-info-circle"></i> </a>
        <a href="#learn" data-key="navLearn"><i class="fas fa-graduation-cap"></i> </a>
        <a href="#schemes" data-key="navSchemes"><i class="fas fa-search-dollar"></i> </a>
        <a class="btn" data-target="tab-govt-portals" data-key="navGovtLinks"><i class="fas fa-university"></i></a>
        <a href="#education" data-key="navEducation"><i class="fas fa-book-reader"></i> </a>
        <a href="#register" data-key="navRegister"><i class="fas fa-user-plus"></i> </a>
        <a href="#" id="voice-assist-btn" data-key="navVoice" title="Odia Voice Assistance">
            <i class="fas fa-microphone-alt"></i> 
        </a>
        <div class="lang-switch">
            <label>EN</label>
            <label class="switch">
                <input type="checkbox" id="language-toggle">
                <span class="slider"></span>
            </label>
            <label>ଓଡ଼ିଆ</label>
        </div>
    </nav>

    <div class="container">
        <section id="events" class="feature-section event-section">
            <div style="flex: 1 1 100%;">
                <h2 data-key="eventTitle"><i class="fas fa-calendar-check icon"></i></h2>
                <p data-key="eventName"></p>
                <p><strong data-key="eventDateLabel"></strong> <span data-key="eventDate"></span> | <strong data-key="eventLocationLabel"></strong> <span data-key="eventLocation"></span></p>
                <p data-key="eventDesc"></p>
            </div>
        </section>

        <section id="about" class="feature-section">
            <div class="feature" style="flex: 1 1 100%; text-align:center;">
                <h2 data-key="missionTitle"><i class="fas fa-bullseye"></i></h2>
                <p data-key="missionText"></p>
                <img src="images/KH pic 1.jpg" style="width: 80%; max-width: 500px; border-radius: 10px; margin: 1em auto;" alt="Weaver at a loom">
            </div>
        </section>

        <section id="learn" class="feature-section">
            <h2 class="section-title" data-key="learnTitle"></h2>
            <div class="feature">
                <i class="fas fa-video icon"></i>
                <h3 data-key="tutorialsTitle"></h3>
                <p data-key="tutorialsText"></p>
                <a class="btn" data-target="tab-tutorials"><i class="fas fa-play-circle"></i> <span data-key="watchVideosBtn"></span></a>
            </div>
            <div class="feature">
                <i class="fas fa-store icon"></i>
                <h3 data-key="sellCraftTitle"></h3>
                <p data-key="sellCraftText"></p>
                <a class="btn" data-target="tab-tutorials"><i class="fas fa-shopping-cart"></i> <span data-key="learnToSellBtn"></span></a>
            </div>
        </section>

        <section id="schemes" class="feature-section">
            <h2 class="section-title" data-key="aiFinderTitle"></h2>
            <div class="feature" style="flex: 1 1 100%; background-color: var(--primary-light); color: var(--primary-dark);">
                <h3 data-key="findSchemeTitle"></h3>
                <p data-key="findSchemeText"></p>
                <div class="recommender-form">
                    <label data-key="artisanIdLabel"></label>
                    <div style="margin-bottom: 1em;">
                        <input type="radio" id="hasArtisanIdYes" name="hasArtisanId" value="yes">
                        <label for="hasArtisanIdYes" data-key="yes"></label>
                        <input type="radio" id="hasArtisanIdNo" name="hasArtisanId" value="no" style="margin-left: 15px;">
                        <label for="hasArtisanIdNo" data-key="no"></label>
                    </div>
                    <div id="artisanIdInputContainer" style="display: none;">
                        <label for="artisanId" data-key="enterIdLabel"></label>
                        <input type="text" id="artisanId" name="artisanId" placeholder="123456789012">
                    </div>
                    <label for="age" data-key="ageLabel"></label>
                    <input type="number" id="age" name="age" data-key="agePlaceholder">
                    <label for="need" data-key="needLabel"></label>
                    <select id="need" name="need">
                        <option value="" data-key="selectOption"></option>
                        <option value="loan" data-key="needLoan"></option>
                        <option value="training" data-key="needTraining"></option>
                        <option value="pension" data-key="needPension"></option>
                        <option value="education" data-key="needEducation"></option>
                    </select>
                    <button id="findSchemeBtn" class="btn" style="width: 100%; margin-top: 15px;"><i class="fas fa-magic"></i> <span data-key="findSchemesBtn"></span></button>
                </div>
                <div id="scheme-results" style="margin-top: 20px; padding: 15px; border-radius: 8px; background-color: #e8f5e9; display: none;"></div>
            </div>
        </section>
        
        <section id="education" class="feature-section">
             <h2 class="section-title" data-key="childrensFutureTitle"></h2>
            <div class="feature">
                <i class="fas fa-graduation-cap icon"></i>
                <h3 data-key="scholarshipsTitle"></h3>
                <p data-key="scholarshipsText"></p>
                <a class="btn" data-target="tab-education"><i class="fas fa-search-dollar"></i> <span data-key="findScholarshipsBtn"></span></a>
            </div>
            <div class="feature">
                <i class="fas fa-hands-helping icon"></i>
                <h3 data-key="ngoSupportTitle"></h3>
                <p data-key="ngoSupportText"></p>
                <a class="btn" data-target="tab-education"><i class="fas fa-link"></i> <span data-key="connectNgoBtn"></span></a>
            </div>
        </section>
        
        <section id="register" class="feature-section">
            <h2 class="section-title" data-key="joinHubTitle"></h2>
            <div class="feature" style="flex: 1 1 100%; background: var(--primary-light); color: var(--primary-dark);">
                <form style="text-align: left; max-width: 500px; margin: auto;">
                    <label for="name" data-key="regName"></label>
                    <input type="text" id="name" name="name" required style="width: 100%; padding: 8px; margin: 6px 0; border-radius: 4px; border: 1px solid #ccc;"><br>
                    <label for="contact" data-key="regPhone"></label>
                    <input type="tel" id="contact" name="contact" required style="width: 100%; padding: 8px; margin: 6px 0; border-radius: 4px; border: 1px solid #ccc;"><br>
                    <input type="submit" data-key="regSubmitBtn" class="btn" style="width: 100%; font-size: 1.2em; margin-top: 10px;">
                </form>
            </div>
        </section>
    </div>

    <footer>
        <p><i class="fas fa-cloud-download-alt"></i> <span data-key="footerOfflineText"></span></p>
        <p data-key="footerCopyright"></p>
    </footer>

    <div id="tab-tutorials" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2 data-key="learnTitle"></h2>
            <div class="info-item">
                <h3 data-key="successStoriesTitle"><i class="fas fa-star" style="color: var(--highlight-yellow);"></i></h3>
                <p data-key="successStoriesText"></p>
                <div class="video-container"><iframe src="https://www.youtube.com/embed/placeholder_success_video_id" title="Success Story" frameborder="0" allowfullscreen></iframe></div>
            </div>
            <div class="info-item">
                <h3 data-key="howToSellTitle"><i class="fas fa-shopping-cart"></i></h3>
                <p data-key="howToSellText"></p>
                <div class="video-container"><iframe src="https://www.youtube.com/embed/placeholder_sell_video_id" title="How to Sell Tutorial" frameborder="0" allowfullscreen></iframe></div>
            </div>
            <div class="info-item">
                <h3 data-key="tutorialUpiTitle"></h3>
                <p data-key="tutorialUpiText"></p>
                <div class="video-container"><iframe src="https://www.youtube.com/embed/placeholder_upi_video_id" title="UPI Tutorial" frameborder="0" allowfullscreen></iframe></div>
            </div>
        </div>
    </div>
    
    <div id="tab-education" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2 data-key="childrensFutureTitle"></h2>
             <div class="info-item">
                <h3 data-key="centralGovtSchol"></h3>
                <div class="portal-list">
                    <ul><li><a href="https://scholarships.gov.in/" target="_blank" data-key="nsp"></a><p data-key="nspDesc"></p></li></ul>
                </div>
            </div>
             <div class="info-item">
                <h3 data-key="odishaGovtSchol"></h3>
                 <div class="portal-list">
                    <ul>
                        <li><a href="https://scholarship.odisha.gov.in/" target="_blank" data-key="osp"></a><p data-key="ospDesc"></p></li>
                         <li><a href="https://www.samsodisha.gov.in/" target="_blank" data-key="sams"></a><p data-key="samsDesc"></p></li>
                    </ul>
                </div>
            </div>
             <div class="info-item">
                <h3 data-key="ngoSchol"></h3>
                 <div class="portal-list">
                    <ul>
                        <li><a href="https://kiss.ac.in/" target="_blank" data-key="ngo1"></a><p data-key="ngo1Desc"></p></li>
                        <li><a href="https://www.adhikar.org.in/" target="_blank" data-key="ngo2"></a><p data-key="ngo2Desc"></p></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>

    <div id="tab-govt-portals" class="modal">
        <div class="modal-content">
            <span class="close-btn">&times;</span>
            <h2 data-key="govtPortalsTitle"></h2>
            <div class="portal-list">
                <ul>
                    <li><a href="https://handlooms.nic.in/" target="_blank" data-key="portalMinHT"></a><p data-key="portalMinHTDesc"></p></li>
                    <li><a href="https://odishaone.gov.in/" target="_blank" data-key="portalOdishaOne"></a><p data-key="portalOdishaOneDesc"></p></li>
                    <li><a href="https://www.boyanika.com/" target="_blank" data-key="portalBoyanika"></a><p data-key="portalBoyanikaDesc"></p></li>
                    <li><a href="#" target="_blank" data-key="portalSilpi"></a><p data-key="portalSilpiDesc"></p></li>
                    <li><a href="#" target="_blank" data-key="portalEBandhan"></a><p data-key="portalEBandhanDesc"></p></li>
                    <li><a href="https://www.ifmsodisha.gov.in/" target="_blank" data-key="portalIFMS"></a><p data-key="portalIFMSDesc"></p></li>
                    <li><a href="https://hrmsodisha.gov.in/" target="_blank" data-key="portalHRMS"></a><p data-key="portalHRMSDesc"></p></li>
                </ul>
            </div>
        </div>
    </div>

    <div id="welcome-popup" class="modal"><div class="modal-content" style="max-width: 500px; text-align: center;"><h2 data-key="welcomeTitle"></h2><p data-key="welcomeText"></p><button id="watch-tutorial-btn" class="btn btn-primary"><i class="fas fa-play"></i> <span data-key="watchTutorialBtn"></span></button><button id="close-welcome-btn" class="btn" style="background: #aaa;"><span data-key="noThanksBtn"></span></button></div></div>
    <div id="tutorial-video-popup" class="modal"><div class="modal-content"><span class="close-btn">&times;</span><h3 data-key="siteTutorialTitle"></h3><div class="video-container"><iframe src="https://www.youtube.com/embed/placeholder_website_tutorial_id" title="Website Tutorial" frameborder="0" allowfullscreen></iframe></div></div></div>
    <div id="artisan-id-popup" class="modal"><div class="modal-content" style="max-width: 600px; text-align: center;"><span class="close-btn">&times;</span><h2 data-key="artisanIdPopupTitle"></h2><p data-key="artisanIdPopupText"></p><a href="https://texmin.nic.in/weavers-pehchan-card-scheme" target="_blank" class="btn btn-primary"><i class="fas fa-external-link-alt"></i> <span data-key="registerNowBtn"></span></a></div></div>
    
    <div class="floating-support-hub"><div class="floating-btn" id="main-support-btn"><i class="fas fa-headset"></i></div></div>
    <div id="chatbot-container"><div id="chatbot-header"><span data-key="chatHeader"></span><span id="close-chatbot-btn">&times;</span></div><div id="chatbot-messages"></div><div id="chatbot-faq-options"></div></div>

    <script>
    // --- BILINGUAL & DYNAMIC CONTENT SCRIPT ---
    const languageData = {
        en: {
            pageTitle: "KARIGAR's HUB", headerTitle: "KARIGAR's HUB", headerSubtitle: "A Single Portal to Empower Weavers of Taraboi",
            navAbout: "About", navLearn: "Learn", navSchemes: "Find Schemes", navGovtLinks: "Govt. Links", navEducation: "For Children", navRegister: "Join Us", navVoice: "Voice Assist",
            eventTitle: "Upcoming Event", eventName: "Toshali National Crafts Mela", eventDateLabel: "Date:", eventDate: "15th - 28th December", eventLocationLabel: "Location:", eventLocation: "Bhubaneswar", eventDesc: "A great opportunity to showcase and sell your products. We can help with stall applications.",
            missionTitle: "Our Mission", missionText: "To provide the weavers of Taraboi with the digital tools, knowledge, and platform needed to grow their craft, improve their livelihood, and stand on their own feet.",
            learnTitle: "Learn & Grow", tutorialsTitle: "Tutorial Videos", tutorialsText: "Step-by-step video guides to help you master digital tools.", watchVideosBtn: "Watch Videos",
            sellCraftTitle: "Sell Your Craft", sellCraftText: "Learn how to photograph your products and sell them online effectively.", learnToSellBtn: "Learn to Sell",
            aiFinderTitle: "AI Scheme Finder", findSchemeTitle: "Find Your Perfect Scheme", findSchemeText: "Answer a few questions and our AI tool will suggest the best government schemes for you.",
            artisanIdLabel: "Do you have an Artisan ID Card (Pehchan Card)?", yes: "Yes", no: "No", enterIdLabel: "Please enter your 12-digit Artisan ID:",
            ageLabel: "What is your age?", agePlaceholder: "e.g., 45", needLabel: "What do you need help with?",
            selectOption: "-- Select an Option --", needLoan: "Loan for Business", needTraining: "New Design Training", needPension: "Pension for Old Age", needEducation: "Child's Education",
            findSchemesBtn: "Find My Schemes",
            childrensFutureTitle: "Future for Our Children", scholarshipsTitle: "Scholarships & Support", scholarshipsText: "Find government and NGO scholarships for your children's education.", findScholarshipsBtn: "Find Scholarships",
            ngoSupportTitle: "NGO Support", ngoSupportText: "Connect with non-profit organizations working to empower artisans in Odisha.", connectNgoBtn: "Connect with NGOs",
            joinHubTitle: "Join Karigar Hub Today!", regName: "Full Name:", regPhone: "Phone Number:", regSubmitBtn: "Register Now",
            footerOfflineText: "Portal works even with a weak signal. Install the app for offline use!", footerCopyright: "© 2025 Karigar's Hub | Designed to Uplift the Weavers of Taraboi.",
            successStoriesTitle: "Artisan Success Stories", successStoriesText: "Watch videos from weavers in our community who have benefited from this portal.",
            howToSellTitle: "How to Sell Your Products Online", howToSellText: "A detailed tutorial on taking good photos, writing descriptions, and managing online sales.",
            tutorialUpiTitle: "How to Use UPI", tutorialUpiText: "Learn to receive payments directly from customers using your phone.",
            centralGovtSchol: "Central Government Scholarships", nsp: "National Scholarship Portal (NSP)", nspDesc: "A single portal for various scholarships from the central government.",
            odishaGovtSchol: "Odisha State Scholarships", osp: "Odisha State Scholarship Portal", ospDesc: "The main portal for scholarships offered by the Government of Odisha.", sams: "SAMS Odisha", samsDesc: "Student Academic Management System for admissions and e-Administration in Odisha.",
            ngoSchol: "NGO Educational Support", ngo1: "Kalinga Institute of Social Sciences (KISS)", ngo1Desc: "Provides free education from KG to PG for tribal children.", ngo2: "Adhikar", ngo2Desc: "Works on livelihood and educational rights in Odisha.",
            govtPortalsTitle: "Important Government Portals",
            portalMinHT: "Ministry of Handlooms and Textiles", portalMinHTDesc: "Official portal for central government schemes and information.",
            portalOdishaOne: "Odisha One", portalOdishaOneDesc: "A single application for over 100 government services in Odisha.",
            portalBoyanika: "Boyanika", portalBoyanikaDesc: "The official e-commerce platform for Odisha Handloom products.",
            portalSilpi: "Silpi Unnati Yojana", portalSilpiDesc: "A scheme focused on the development and welfare of artisans.",
            portalEBandhan: "E-bandhan", portalEBandhanDesc: "Handloom Cluster Management System for information and management.",
            portalIFMS: "iFMS Odisha", portalIFMSDesc: "Integrated Financial Management System for treasury and accounts.",
            portalHRMS: "HRMS Odisha", portalHRMSDesc: "Human Resource Management System for government employees.",
            welcomeTitle: "Welcome to Karigar's Hub!", welcomeText: "Are you a new user? We have a short video to show you how to use the website.", watchTutorialBtn: "Watch Tutorial", noThanksBtn: "No, thanks",
            siteTutorialTitle: "How to use Karigar's Hub",
            artisanIdPopupTitle: "Artisan ID Card Required", artisanIdPopupText: "To find the best schemes, an Artisan ID (Pehchan Card) is very helpful. If you don't have one, you can register for it on the official government portal.", registerNowBtn: "Register for Pehchan Card",
            chatHeader: "Support Hub", chatWelcome: "Hello! How can I help you today? Please select an option.", chatFaq1: "How to get a loan?", chatFaq2: "How to sell my products?", chatFaq3: "How to find scholarships?", chatFaq4: "Need direct help?",
            chatAns1: "You can apply for a loan through the MUDRA scheme. Use our 'AI Scheme Finder' for details.",
            chatAns2: "Register on our portal by clicking 'Join Us'. Watch the 'How to Sell' video in the Learn section.",
            chatAns3: "Visit the 'For Children' section. We have links to the National and State Scholarship Portals.",
            chatAns4: "For direct help, you can call us or send a message on WhatsApp.",
            chatContactCall: "Call Us", chatContactWhatsapp: "WhatsApp"
        },
        or: {
            pageTitle: "କାରିଗର ହବ୍", headerTitle: "କାରିଗର ହବ୍", headerSubtitle: "ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ସଶକ୍ତ କରିବା ପାଇଁ ଏକକ ପୋର୍ଟାଲ୍",
            navAbout: "ଆମ ବିଷୟରେ", navLearn: "ଶିଖନ୍ତୁ", navSchemes: "ଯୋଜନା ଖୋଜନ୍ତୁ", navGovtLinks: "ସରକାରୀ ଲିଙ୍କ୍", navEducation: "ପିଲାଙ୍କ ପାଇଁ", navRegister: "ଯୋଗ ଦିଅନ୍ତୁ", navVoice: "ଭଏସ୍ ସହାୟତା",
            eventTitle: "ଆଗାମୀ କାର୍ଯ୍ୟକ୍ରମ", eventName: "ତୋଷାଳୀ ଜାତୀୟ ହସ୍ତଶିଳ୍ପ ମେଳା", eventDateLabel: "ତାରିଖ:", eventDate: "୧୫ - ୨୮ ଡିସେମ୍ବର", eventLocationLabel: "ସ୍ଥାନ:", eventLocation: "ଭୁବନେଶ୍ୱର", eventDesc: "ଆପଣଙ୍କ ଉତ୍ପାଦ ପ୍ରଦର୍ଶନ ଏବଂ ବିକ୍ରୟ ପାଇଁ ଏକ ବଡ଼ ସୁଯୋଗ। ଆମେ ଷ୍ଟଲ୍ ଆବେଦନରେ ସାହାଯ୍ୟ କରିପାରିବୁ।",
            missionTitle: "ଆମର ଲକ୍ଷ୍ୟ", missionText: "ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ଡିଜିଟାଲ୍ ଉପକରଣ, ଜ୍ଞାନ ଏବଂ ପ୍ଲାଟଫର୍ମ ପ୍ରଦାନ କରିବା ଯାହା ସେମାନଙ୍କର କଳାକୁ ବଢ଼ାଇବା, ଜୀବିକା ଉନ୍ନତ କରିବା ଏବଂ ନିଜ ଗୋଡ଼ରେ ଛିଡ଼ା ହେବା ପାଇଁ ଆବଶ୍ୟକ।",
            learnTitle: "ଶିଖନ୍ତୁ ଓ ଆଗକୁ ବଢନ୍ତୁ", tutorialsTitle: "ଟ୍ୟୁଟୋରିଆଲ୍ ଭିଡିଓ", tutorialsText: "ଡିଜିଟାଲ୍ ଉପକରଣଗୁଡ଼ିକୁ ବ୍ୟବହାର କରିବାରେ ସାହାଯ୍ୟ କରିବା ପାଇଁ ପର୍ଯ୍ୟାୟକ୍ରମେ ଭିଡିଓ ଗାଇଡ୍।", watchVideosBtn: "ଭିଡିଓ ଦେଖନ୍ତୁ",
            sellCraftTitle: "ଆପଣଙ୍କ କଳା ବିକ୍ରି କରନ୍ତୁ", sellCraftText: "ଆପଣଙ୍କ ଉତ୍ପାଦର ଫଟୋ କିପରି ଉଠାଇବେ ଏବଂ ଅନଲାଇନରେ ପ୍ରଭାବଶାଳୀ ଭାବରେ ବିକ୍ରି କରିବେ ତାହା ଶିଖନ୍ତୁ।", learnToSellBtn: "ବିକ୍ରି କରିବା ଶିଖନ୍ତୁ",
            aiFinderTitle: "AI ସ୍କିମ୍ ଫାଇଣ୍ଡର୍", findSchemeTitle: "ଆପଣଙ୍କ ପାଇଁ ସଠିକ୍ ଯୋଜନା ଖୋଜନ୍ତୁ", findSchemeText: "କିଛି ପ୍ରଶ୍ନର ଉତ୍ତର ଦିଅନ୍ତୁ ଏବଂ ଆମର AI ଉପକରଣ ଆପଣଙ୍କ ପାଇଁ ସର୍ବୋତ୍ତମ ସରକାରୀ ଯୋଜନାଗୁଡିକର ପରାମର୍ଶ ଦେବ।",
            artisanIdLabel: "ଆପଣଙ୍କ ପାଖରେ କାରିଗର ପରିଚୟ ପତ୍ର (ପେହଚାନ୍ କାର୍ଡ) ଅଛି କି?", yes: "ହଁ", no: "ନାହିଁ", enterIdLabel: "ଦୟାକରି ଆପଣଙ୍କ ୧୨-ଅଙ୍କ ବିଶିଷ୍ଟ କାରିଗର ID ପ୍ରବେଶ କରନ୍ତୁ:",
            ageLabel: "ଆପଣଙ୍କ ବୟସ କେତେ?", agePlaceholder: "ଉଦାହରଣ, ୪୫", needLabel: "ଆପଣଙ୍କୁ କେଉଁଥିରେ ସାହାଯ୍ୟ ଦରକାର?",
            selectOption: "-- ଏକ ବିକଳ୍ପ ବାଛନ୍ତୁ --", needLoan: "ବ୍ୟବସାୟ ପାଇଁ ଋଣ", needTraining: "ନୂଆ ଡିଜାଇନ୍ ତାଲିମ", needPension: "ବୃଦ୍ଧାବସ୍ଥା ପାଇଁ ପେନସନ", needEducation: "ପିଲାର ଶିକ୍ଷା",
            findSchemesBtn: "ମୋ ପାଇଁ ଯୋଜନା ଖୋଜନ୍ତୁ",
            childrensFutureTitle: "ଆମ ପିଲାମାନଙ୍କ ପାଇଁ ଭବିଷ୍ୟତ", scholarshipsTitle: "ଛାତ୍ରବୃତ୍ତି ଓ ସହାୟତା", scholarshipsText: "ଆପଣଙ୍କ ପିଲାଙ୍କ ଶିକ୍ଷା ପାଇଁ ସରକାରୀ ଏବଂ ଏନଜିଓ ଛାତ୍ରବୃତ୍ତି ଖୋଜନ୍ତୁ।", findScholarshipsBtn: "ଛାତ୍ରବୃତ୍ତି ଖୋଜନ୍ତୁ",
            ngoSupportTitle: "ଏନଜିଓ ସହାୟତା", ngoSupportText: "ଓଡିଶାର କାରିଗରମାନଙ୍କୁ ସଶକ୍ତ କରିବା ପାଇଁ କାର୍ଯ୍ୟ କରୁଥିବା ଅଣ-ଲାଭକାରୀ ସଂଗଠନ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ।", connectNgoBtn: "ଏନଜିଓ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ",
            joinHubTitle: "ଆଜି ହିଁ କାରିଗର ହବ୍‌ରେ ଯୋଗ ଦିଅନ୍ତୁ!", regName: "ପୂରା ନାମ:", regPhone: "ଫୋନ୍ ନମ୍ବର:", regSubmitBtn: "ବର୍ତ୍ତମାନ ପଞ୍ଜୀକରଣ କରନ୍ତୁ",
            footerOfflineText: "କମ୍ ସିଗନାଲରେ ବି ପୋର୍ଟାଲ୍ କାମ କରେ। ଅଫଲାଇନ୍ ବ୍ୟବହାର ପାଇଁ ଆପ୍ ଇନଷ୍ଟଲ୍ କରନ୍ତୁ!", footerCopyright: "© ୨୦୨୫ କାରିଗର ହବ୍ | ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ଉନ୍ନତି ପାଇଁ ପରିକଳ୍ପିତ।",
            successStoriesTitle: "କାରିଗରଙ୍କ ସଫଳତା କାହାଣୀ", successStoriesText: "ଆମ ସମ୍ପ୍ରଦାୟର ବୁଣାକାରମାନଙ୍କ ଭିଡିଓ ଦେଖନ୍ତୁ ଯେଉଁମାନେ ଏହି ପୋର୍ଟାଲରୁ ଲାଭ ପାଇଛନ୍ତି।",
            howToSellTitle: "ଅନଲାଇନରେ ଆପଣଙ୍କ ଉତ୍ପାଦ କିପରି ବିକ୍ରି କରିବେ", howToSellText: "ଭଲ ଫଟୋ ଉଠାଇବା, ବିବରଣୀ ଲେଖିବା ଏବଂ ଅନଲାଇନ୍ ବିକ୍ରୟ ପରିଚାଳନା କରିବା ଉପରେ ଏକ ବିସ୍ତୃତ ଟ୍ୟୁଟୋରିଆଲ୍।",
            tutorialUpiTitle: "UPI କିପରି ବ୍ୟବହାର କରିବେ", tutorialUpiText: "ଗ୍ରାହକଙ୍କଠାରୁ ସିଧାସଳଖ ଆପଣଙ୍କ ଫୋନ୍ ବ୍ୟବହାର କରି ପେମେଣ୍ଟ ଗ୍ରହଣ କରିବା ଶିଖନ୍ତୁ।",
            centralGovtSchol: "କେନ୍ଦ୍ର ସରକାରୀ ଛାତ୍ରବୃତ୍ତି", nsp: "ଜାତୀୟ ଛାତ୍ରବୃତ୍ତି ପୋର୍ଟାଲ୍ (NSP)", nspDesc: "କେନ୍ଦ୍ର ସରକାରଙ୍କ ବିଭିନ୍ନ ଛାତ୍ରବୃତ୍ତି ପାଇଁ ଏକକ ପୋର୍ଟାଲ୍।",
            odishaGovtSchol: "ଓଡିଶା ରାଜ୍ୟ ଛାତ୍ରବୃତ୍ତି", osp: "ଓଡିଶା ରାଜ୍ୟ ଛାତ୍ରବୃତ୍ତି ପୋର୍ଟାଲ୍", ospDesc: "ଓଡିଶା ସରକାରଙ୍କ ଦ୍ୱାରା ପ୍ରଦତ୍ତ ଛାତtr વૃત્તિ ପାଇଁ ମୁଖ୍ୟ ପୋର୍ଟାଲ୍।", sams: "ସାମ୍ସ ଓଡିଶା", samsDesc: "ଓଡିଶାରେ ଆଡମିଶନ ଏବଂ ଇ-ପ୍ରଶାସନ ପାଇଁ ଛାତ୍ର ଏକାଡେମିକ୍ ମ୍ୟାନେଜମେଣ୍ଟ ସିଷ୍ଟମ୍।",
            ngoSchol: "ଏନଜିଓ ଶିକ୍ଷାଗତ ସହାୟତା", ngo1: "କଳିଙ୍ଗ ଇନଷ୍ଟିଚ୍ୟୁଟ୍ ଅଫ୍ ସୋସିଆଲ୍ ସାଇନ୍ସେସ୍ (KISS)", ngo1Desc: "ଆଦିବାସୀ ପିଲାମାନଙ୍କ ପାଇଁ KG ରୁ PG ପର୍ଯ୍ୟନ୍ତ ମାଗଣା ଶିକ୍ଷା ପ୍ରଦାନ କରେ।", ngo2: "ଅଧିକାର", ngo2Desc: "ଓଡିଶାରେ ଜୀବିକା ଏବଂ ଶିକ୍ଷାଗତ ଅଧିକାର ଉପରେ କାର୍ଯ୍ୟ କରେ।",
            govtPortalsTitle: "ଗୁରୁତ୍ୱପୂର୍ଣ୍ଣ ସରକାରୀ ପୋର୍ଟାଲ୍",
            portalMinHT: "ବୟନଶିଳ୍ପ ମନ୍ତ୍ରାଳୟ", portalMinHTDesc: "କେନ୍ଦ୍ର ସରକାରଙ୍କ ଯୋଜନା ଏବଂ ସୂଚନା ପାଇଁ ସରକାରୀ ପୋର୍ଟାଲ୍।",
            portalOdishaOne: "ଓଡିଶା ୱାନ୍", portalOdishaOneDesc: "ଓଡିଶାରେ ୧୦୦ରୁ ଅଧିକ ସରକାରୀ ସେବା ପାଇଁ ଏକକ ଆପ୍ଲିକେସନ୍।",
            portalBoyanika: "ବୟନିକା", portalBoyanikaDesc: "ଓଡିଶା ହସ୍ତତନ୍ତ ଉତ୍ପାଦ ପାଇଁ ସରକାରୀ ଇ-କମର୍ସ ପ୍ଲାଟଫର୍ମ।",
            portalSilpi: "ଶିଳ୍ପୀ ଉନ୍ନତି ଯୋଜନା", portalSilpiDesc: "କାରିଗରମାନଙ୍କ ବିକାଶ ଏବଂ କଲ୍ୟାଣ ଉପରେ କେନ୍ଦ୍ରିତ ଏକ ଯୋଜନା।",
            portalEBandhan: "ଇ-ବନ୍ଧନ", portalEBandhanDesc: "ସୂଚନା ଏବଂ ପରିଚାଳନା ପାଇଁ ହସ୍ତତନ୍ତ କ୍ଲଷ୍ଟର ପରିଚାଳନା ପ୍ରଣାଳୀ।",
            portalIFMS: "ଆଇଏଫ୍ଏମ୍ଏସ୍ ଓଡିଶା", portalIFMSDesc: "କୋଷାଗାର ଏବଂ ହିସାବ ପାଇଁ ସମନ୍ୱିତ ଆର୍ଥିକ ପରିଚାଳନା ପ୍ରଣାଳୀ।",
            portalHRMS: "ଏଚ୍ଆର୍ଏମ୍ଏସ୍ ଓଡିଶା", portalHRMSDesc: "ସରକାରୀ କର୍ମଚାରୀଙ୍କ ପାଇଁ ମାନବ ସମ୍ବଳ ପରିଚାଳନା ପ୍ରଣାଳୀ।",
            welcomeTitle: "କାରିଗର ହବ୍‌କୁ ସ୍ୱାଗତ!", welcomeText: "ଆପଣ ଜଣେ ନୂଆ ବ୍ୟବହାରକାରୀ କି? ୱେବସାଇଟ୍ କିପରି ବ୍ୟବହାର କରିବେ ତାହା ଦେଖାଇବା ପାଇଁ ଆମ ପାଖରେ ଏକ ଛୋଟ ଭିଡିଓ ଅଛି।", watchTutorialBtn: "ଟ୍ୟୁଟୋରିଆଲ୍ ଦେଖନ୍ତୁ", noThanksBtn: "ନା, ଧନ୍ୟବାଦ",
            siteTutorialTitle: "କାରିଗର ହବ୍ କିପରି ବ୍ୟବହାର କରିବେ",
            artisanIdPopupTitle: "କାରିଗର ପରିଚୟ ପତ୍ର ଆବଶ୍ୟକ", artisanIdPopupText: "ସର୍ବୋତ୍ତମ ଯୋଜନା ଖୋଜିବା ପାଇଁ, ଏକ କାରିଗର ପରିଚୟ ପତ୍ର (ପେହଚାନ୍ କାର୍ଡ) ବହୁତ ସାହାଯ୍ୟକାରୀ। ଯଦି ଆପଣଙ୍କ ପାଖରେ ନାହିଁ, ଆପଣ ସରକାରୀ ପୋର୍ଟାଲରେ ଏଥିପାଇଁ ପଞ୍ଜୀକରଣ କରିପାରିବେ।", registerNowBtn: "ପେହଚାନ୍ କାର୍ଡ ପାଇଁ ପଞ୍ଜୀକରଣ କରନ୍ତୁ",
            chatHeader: "ସହାୟତା କେନ୍ଦ୍ର", chatWelcome: "ନମସ୍କାର! ମୁଁ କିପରି ସାହାଯ୍ୟ କରିପାରେ? ଦୟାକରି ଏକ ବିକଳ୍ପ ବାଛନ୍ତୁ।", chatFaq1: "ଋଣ କିପରି ପାଇବି?", chatFaq2: "ଉତ୍ପାଦ କିପରି ବିକ୍ରି କରିବି?", chatFaq3: "ଛାତ୍ରବୃତ୍ତି କିପରି ପାଇବି?", chatFaq4: "ସିଧାସଳଖ ସାହାଯ୍ୟ ଦରକାର କି?",
            chatAns1: "ଆପଣ ମୁଦ୍ରା ଯୋଜନା ମାଧ୍ୟମରେ ଋଣ ପାଇଁ ଆବେଦନ କରିପାରିବେ। 'AI ସ୍କିମ୍ ଫାଇଣ୍ଡର୍' ବ୍ୟବହାର କରନ୍ତୁ।",
            chatAns2: "'ଯୋଗ ଦିଅନ୍ତୁ' ଉପରେ କ୍ଲିକ୍ କରି ପଞ୍ଜୀକରଣ କରନ୍ତୁ। 'ଶିଖନ୍ତୁ' ବିଭାଗରେ 'କିପରି ବିକ୍ରି କରିବେ' ଭିଡିଓ ଦେଖନ୍ତୁ।",
            chatAns3: "'ପିଲାଙ୍କ ପାଇଁ' ବିଭାଗକୁ ଯାଆନ୍ତୁ। ସେଠାରେ ଜାତୀୟ ଏବଂ ରାଜ୍ୟ ଛାତ୍ରବୃତ୍ତି ପୋର୍ଟାଲର ଲିଙ୍କ୍ ଅଛି।",
            chatAns4: "ସିଧାସଳଖ ସାହାଯ୍ୟ ପାଇଁ, ଆପଣ ଆମକୁ କଲ୍ କରିପାରିବେ କିମ୍ବା ହ୍ଵାଟ୍ସଆପ୍‌ରେ ମେସେଜ୍ ପଠାଇପାରିବେ।",
            chatContactCall: "କଲ୍ କରନ୍ତୁ", chatContactWhatsapp: "ହ୍ଵାଟ୍ସଆପ୍"
        }
    };

    let currentLanguage = 'en';

    function updateLanguage(lang) {
        currentLanguage = lang;
        document.documentElement.lang = lang;
        document.querySelectorAll('[data-key]').forEach(el => {
            const key = el.dataset.key;
            const textData = languageData[lang][key];
            if (!textData) return;
            
            const icon = el.querySelector('i');
            const span = el.querySelector('span');
            
            if (el.tagName === 'INPUT') {
                if (el.type === 'submit' || el.type === 'button') el.value = textData;
                else el.placeholder = textData;
            } else if (span) {
                span.textContent = textData;
            } else {
                if (icon) el.innerHTML = icon.outerHTML + ' ' + textData;
                else el.innerHTML = textData;
            }
        });
    }
    
    document.addEventListener('DOMContentLoaded', function () {
        updateLanguage('en'); 
        
        const langToggle = document.getElementById('language-toggle');
        langToggle.addEventListener('change', function() {
            updateLanguage(this.checked ? 'or' : 'en');
        });

        const allModals = document.querySelectorAll('.modal');
        function openModal(modalId) {
            const modal = document.getElementById(modalId);
            if(modal) modal.style.display = 'block';
        }
        function closeModal(modal) {
            if(modal) modal.style.display = 'none';
        }
        document.querySelectorAll('.btn[data-target]').forEach(button => {
            button.addEventListener('click', e => openModal(e.currentTarget.dataset.target));
        });
        allModals.forEach(modal => {
            modal.querySelector('.close-btn')?.addEventListener('click', () => closeModal(modal));
        });
        window.addEventListener('click', event => {
            if (event.target.classList.contains('modal')) {
                closeModal(event.target);
            }
        });

        if (!sessionStorage.getItem('welcomePopupShown')) {
            setTimeout(() => openModal('welcome-popup'), 1500);
            sessionStorage.setItem('welcomePopupShown', 'true');
        }
        document.getElementById('watch-tutorial-btn').addEventListener('click', () => {
            closeModal(document.getElementById('welcome-popup'));
            openModal('tutorial-video-popup');
        });
        document.getElementById('close-welcome-btn').addEventListener('click', () => {
            closeModal(document.getElementById('welcome-popup'));
        });

        const hasIdYes = document.getElementById('hasArtisanIdYes');
        const hasIdNo = document.getElementById('hasArtisanIdNo');
        const idInputContainer = document.getElementById('artisanIdInputContainer');
        
        hasIdYes.addEventListener('change', () => {
            if(hasIdYes.checked) idInputContainer.style.display = 'block';
        });
        hasIdNo.addEventListener('change', () => {
            if(hasIdNo.checked) {
                idInputContainer.style.display = 'none';
                openModal('artisan-id-popup');
            }
        });

        // --- CHATBOT BILINGUAL LOGIC ---
        const mainSupportBtn = document.getElementById('main-support-btn');
        const chatbotContainer = document.getElementById('chatbot-container');
        const closeChatbotBtn = document.getElementById('close-chatbot-btn');
        const chatbotMessages = document.getElementById('chatbot-messages');
        const faqOptionsContainer = document.getElementById('chatbot-faq-options');

        function addMessage(text, type) {
            const messageDiv = document.createElement('div');
            messageDiv.className = type === 'bot' ? 'bot-message' : 'user-message';
            messageDiv.innerHTML = text; // Use innerHTML to render links
            chatbotMessages.appendChild(messageDiv);
            chatbotMessages.scrollTop = chatbotMessages.scrollHeight;
        }

        function showFaqOptions() {
            faqOptionsContainer.innerHTML = '';
            const faqs = ['chatFaq1', 'chatFaq2', 'chatFaq3', 'chatFaq4'];
            faqs.forEach(faqKey => {
                const faqBtn = document.createElement('button');
                faqBtn.className = 'faq-btn';
                faqBtn.textContent = languageData[currentLanguage][faqKey];
                faqBtn.onclick = () => {
                    addMessage(languageData[currentLanguage][faqKey], 'user');
                    setTimeout(() => {
                        let answer = languageData[currentLanguage][faqKey.replace('Faq', 'Ans')];
                        if (faqKey === 'chatFaq4') {
                            answer += <br><br><a href="tel:+91XXXXXXXXXX" class="btn" style="margin-right: 5px;">${languageData[currentLanguage].chatContactCall}</a> <a href="https://wa.me/91XXXXXXXXXX" target="_blank" class="btn">${languageData[currentLanguage].chatContactWhatsapp}</a>;
                        }
                        addMessage(answer, 'bot');
                    }, 500);
                };
                faqOptionsContainer.appendChild(faqBtn);
            });
        }

        mainSupportBtn.addEventListener('click', () => {
            chatbotContainer.style.display = 'flex';
            chatbotMessages.innerHTML = '';
            addMessage(languageData[currentLanguage].chatWelcome, 'bot');
            showFaqOptions();
        });

        closeChatbotBtn.addEventListener('click', () => {
            chatbotContainer.style.display = 'none';
        });
        
        langToggle.addEventListener('change', () => {
            if (chatbotContainer.style.display === 'flex') {
                chatbotMessages.innerHTML = '';
                addMessage(languageData[currentLanguage].chatWelcome, 'bot');
                showFaqOptions();
            }
        });

    });
    </script>
</body>
</html>
