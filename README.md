<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title data-key="pageTitle">KARIGAR's HUB</title>
    
    <link rel="manifest" href='data:application/manifest+json;base64,ewogICAgIm5hbWUiOiAiS2FyaWdhcidzIEh1YiIsCiAgICAic2hvcnRfbmFtZSI6ICJLYXJpZ2FySHViIiwKICAgICJpY29ucyI6IFsKICAgICAgICB7CiAgICAgICAgICAgICJzcmMiOiAiaW1hZ2VzL2ljb24tMTkyLnBuZyIsCiAgICAgICAgICAgICJ0eXBlIjogImltYWdlL3BuZyIsCiAgICAgICAgICAgICJzaXplcyI6ICIxOTJ4MTkyIgogICAgICAgIH0sCiAgICAgICAgewogICAgICAgICAgICAic3JjIjogImltYWdlcy9pY29uLTUxMi5wbmciLAogICAgICAgICAgICAidHlwZSI6ICJpbWFnZS9wbmciLAogICAgICAgICAgICAic2l6ZXMiOiAiNTEyeDUxMiIKICAgICAgICB9CiAgICBdLAogICAgInN0YXJ0X3VybCI6ICIvIiwKICAgICJkaXNwbGF5IjogInN0YW5kYWxvbmUiLAogICAgInRoZW1lX2NvbG9yIjogIiNGRkZGRkYiLAogICAgImJhY2tncm91bmRfY29sb3IiOiAiI0Y4RjlGQSINCn0='>
    <meta name="theme-color" content="#FFFFFF">

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <style>
        :root {
            --primary-accent: #17A2B8; /* A professional, muted teal */
            --primary-accent-dark: #138496;
            --text-dark: #343A40;       /* Dark charcoal for text */
            --text-light: #FFFFFF;
            --background-light: #F8F9FA; /* Off-white for the page background */
            --background-card: #FFFFFF; /* White for cards/sections */
            --border-color: #DEE2E6;     /* Light grey for borders */
        }

        /* --- KEYFRAME ANIMATIONS --- */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        html { scroll-behavior: smooth; }
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0; padding: 0;
            background-color: var(--background-light);
            color: var(--text-dark);
        }

        /* --- HEADER & LOGO --- */
        header {
            background-color: var(--background-card);
            color: var(--text-dark);
            padding: 1.5em 2.5em; display: flex; align-items: center; flex-wrap: wrap;
            border-bottom: 1px solid var(--border-color);
        }
        .logo {
            width: 90px; height: 90px; margin-right: 20px;
            border-radius: 50%; border: 3px solid var(--primary-accent);
            padding: 4px; background-color: white;
            transition: transform 0.3s ease;
        }
        .logo:hover {
            transform: scale(1.05);
        }
        .header-text { flex-grow: 1; }
        h1, h2, h3 { margin: 0; font-weight: 600; }
        h1 { color: var(--primary-accent); font-weight: 700; }
        p { margin-top: 5px; line-height: 1.7; color: #6C757D; }
        
        /* --- NAVIGATION --- */
        nav {
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(8px);
            padding: 0.8em 1em;
            text-align: center; position: sticky; top: 0;
            z-index: 900; display: flex; justify-content: center;
            align-items: center; flex-wrap: wrap;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        nav a {
            text-decoration: none; color: var(--text-dark);
            padding: 0.6em 1.2em; background: transparent;
            border: 1px solid transparent;
            border-radius: 8px; margin: 0.4em;
            font-weight: 500; transition: all 0.3s ease;
        }
        nav a:hover {
            background-color: var(--primary-accent);
            color: var(--text-light);
        }
        nav a.active {
             background-color: var(--primary-accent);
             color: var(--text-light);
             font-weight: 600;
        }
        
        /* --- MAIN CONTENT & SECTIONS --- */
        .container { max-width: 1200px; margin: 0 auto; padding: 2em; }
        .feature-section {
            background-color: transparent;
            margin-bottom: 3em;
            padding: 0; /* No padding on the container */
            border: none;
            /* Animation class */
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .feature-section.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .section-title {
            width: 100%; text-align: center; font-size: 2.5em;
            margin-bottom: 1.2em; color: var(--text-dark);
            font-weight: 700;
        }

        /* --- FEATURE CARDS --- */
        .feature-wrapper {
             display: flex; flex-wrap: wrap; justify-content: center; gap: 2em;
        }
        .feature {
            flex: 1 1 400px; /* Base size */
            max-width: 480px; /* Max size to prevent becoming too wide */
            margin: 0; /* Removed margin, using gap instead */
            padding: 2.5em;
            background-color: var(--background-card);
            border: 1px solid var(--border-color);
            color: var(--text-dark);
            border-radius: 12px; text-align: center; display: flex;
            flex-direction: column; justify-content: space-between;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .feature:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
        }
        .feature h3 { color: var(--text-dark); margin-bottom: 0.5em; font-weight: 600; }
        .feature p { color: #6C757D; }
        .feature .icon {
            font-size: 3em; color: var(--primary-accent); margin-bottom: 0.7em;
            transition: transform 0.3s ease;
        }
        .feature:hover .icon {
            transform: scale(1.1);
        }
        
        /* --- BUTTONS & FORMS --- */
        .btn {
            display: inline-block; padding: 0.8em 1.8em;
            background-color: var(--primary-accent);
            color: var(--text-light);
            text-decoration: none; border-radius: 8px; margin-top: 1.5em;
            cursor: pointer; font-weight: 500; border: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(23, 162, 184, 0.2);
        }
        .btn:hover {
            background-color: var(--primary-accent-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(23, 162, 184, 0.3);
        }
        .recommender-form input, .recommender-form select, #register form input, #register form textarea {
            width: 100%; padding: 12px; margin: 8px 0 16px 0;
            border-radius: 8px; border: 1px solid var(--border-color);
            background-color: var(--background-light);
            color: var(--text-dark); font-family: 'Poppins', sans-serif;
            transition: border-color 0.3s ease;
        }
        .recommender-form input:focus, .recommender-form select:focus {
            outline: none;
            border-color: var(--primary-accent);
        }
        
        /* --- FOOTER --- */
        footer {
            background-color: var(--text-dark);
            color: var(--background-light); text-align: center; padding: 2.5em; font-size: 0.9em;
        }
        footer p { color: #adb5bd; margin-top: 0.5em; }

        /* --- MODAL (CONTENT TAB) STYLES --- */
        .content-tab {
            display: none; position: fixed; z-index: 1000;
            left: 0; top: 0; width: 100%; height: 100%;
            overflow: auto; background-color: rgba(33, 37, 41, 0.7);
            backdrop-filter: blur(5px);
            padding: 50px 15px;
        }
        .tab-inner-content {
            background-color: var(--background-card);
            color: var(--text-dark);
            margin: 5% auto; padding: 40px; border: 1px solid var(--border-color);
            width: 90%; max-width: 900px; border-radius: 12px; position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        .close-btn {
            color: #6C757D; position: absolute; top: 15px; right: 25px;
            font-size: 35px; font-weight: bold; cursor: pointer;
            transition: color 0.3s, transform 0.3s;
        }
        .close-btn:hover, .close-btn:focus { color: var(--text-dark); transform: rotate(90deg); }
        .video-container {
            position: relative; padding-bottom: 56.25%; height: 0;
            overflow: hidden; max-width: 100%; background: #000;
            margin: 1em 0; border-radius: 10px;
        }
        .video-container iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }
        .info-item { border-bottom: 1px solid var(--border-color); padding: 1.5em 0; margin-bottom: 1em; }
        .info-item:last-child { border-bottom: none; }
        .info-item h3 { color: var(--primary-accent); }
        .info-item ul li a { color: var(--primary-accent); }
        
        /* --- LANGUAGE TOGGLE SWITCH --- */
        .lang-switch { display: flex; align-items: center; margin-left: auto; }
        .lang-switch label { margin: 0 8px; font-weight: 500; color: var(--text-dark); }
        .switch { position: relative; display: inline-block; width: 50px; height: 26px; }
        .switch input { opacity: 0; width: 0; height: 0; }
        .slider { position: absolute; cursor: pointer; top: 0; left: 0; right: 0; bottom: 0; background-color: #ccc; transition: .4s; border-radius: 26px; }
        .slider:before { position: absolute; content: ""; height: 20px; width: 20px; left: 3px; bottom: 3px; background-color: white; transition: .4s; border-radius: 50%; }
        input:checked + .slider { background-color: var(--primary-accent); }
        input:checked + .slider:before { transform: translateX(24px); }

        /* --- VOICE ASSISTANT & CHATBOT --- */
        #voice-popup {
            display: none; flex-direction: column; justify-content: center; align-items: center;
            position: fixed; z-index: 2000; left: 0; top: 0;
            width: 100%; height: 100%; background-color: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
        }
        #voice-popup-icon { font-size: 5em; margin-bottom: 20px; color: var(--primary-accent); }
        #voice-popup-text { font-size: 1.8em; font-weight: 600; }
        @keyframes pulse-light {
             0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); }
        }
        #voice-popup-icon.listening { animation: pulse-light 1.5s infinite; }
        
        #chatbot-container {
            display: none; position: fixed; bottom: 100px; right: 25px;
            width: 350px; height: 500px; background: var(--background-card);
            border-radius: 15px; box-shadow: 0 5px 25px rgba(0,0,0,0.1);
            z-index: 998; flex-direction: column; overflow: hidden;
            border: 1px solid var(--border-color);
        }
        #chatbot-header {
            background: var(--primary-accent); color: white; padding: 15px;
            font-weight: 600; font-size: 1.2em; display: flex;
            justify-content: space-between; align-items: center;
        }
        #close-chatbot-btn { cursor: pointer; font-size: 1.2em; }
        #chatbot-messages { flex-grow: 1; padding: 15px; overflow-y: auto; background: var(--background-light); }
        .bot-message, .user-message { padding: 10px 15px; border-radius: 18px; margin-bottom: 10px; max-width: 85%; line-height: 1.5; }
        .bot-message { background: #E9ECEF; color: var(--text-dark); align-self: flex-start; }
        .user-message { background: var(--primary-accent); color: var(--text-light); align-self: flex-end; margin-left: auto; }
        #chatbot-faq-options { padding: 10px; border-top: 1px solid var(--border-color); background: var(--background-card); }
        .faq-btn {
            width: 100%; background: #E9ECEF; color: var(--text-dark);
            border: none; padding: 12px; border-radius: 8px; margin-bottom: 8px;
            text-align: left; cursor: pointer; font-family: 'Poppins', sans-serif; font-weight: 500;
            transition: background-color 0.3s ease;
        }
        .faq-btn:hover { background: #DEE2E6; }
        
        .floating-support-hub { position: fixed; bottom: 25px; right: 25px; z-index: 950; }
        .floating-btn {
            width: 60px; height: 60px; background-color: var(--primary-accent);
            color: var(--text-light); border-radius: 50%; display: flex;
            justify-content: center; align-items: center; font-size: 1.8em;
            cursor: pointer; box-shadow: 0 4px 15px rgba(23, 162, 184, 0.4);
            transition: all 0.3s ease;
        }
        .floating-btn:hover { transform: scale(1.1) rotate(15deg); box-shadow: 0 6px 20px rgba(23, 162, 184, 0.5); }

        /* --- MISC & RESPONSIVE --- */
        #sell .feature img {
            border: 1px solid var(--border-color);
            padding: 5px; background: white;
        }
        #about .feature {
            background: transparent; border: none; box-shadow: none;
        }
        #about .feature:hover {
            transform: none; box-shadow: none;
        }
        @media screen and (max-width: 768px) {
            header { flex-direction: column; text-align: center; }
            .logo { margin: 0 auto 15px auto; }
            nav a { width: 80%; margin: 0.5em auto; text-align: center; }
            .lang-switch { margin: 10px auto 0 auto; }
            .feature-wrapper { flex-direction: column; gap: 1.5em; }
            .feature { flex-basis: auto; } /* Let it grow naturally */
            #chatbot-container { width: 90%; height: 70%; bottom: 90px; right: 5%; }
        }

    </style>
</head>
<body>

    <header>
        <img src="images/Karigar's hub logo.jpg" alt="Karigar's Hub Logo" class="logo">
        <div class="header-text">
            <h1 data-key="headerTitle"></h1>
            <p data-key="headerSubtitle"></p>
        </div>
    </header>

    <nav>
        <a href="#about" data-key="navAbout"><i class="fas fa-info-circle"></i> </a>
        <a href="#learn" data-key="navLearn"><i class="fas fa-graduation-cap"></i> </a>
        <a href="#schemes" data-key="navSchemes"><i class="fas fa-search-dollar"></i> </a>
        <a href="#sell" data-key="navSell"><i class="fas fa-store"></i> </a>
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
        
        <section id="about" class="feature-section">
             <div class="feature">
                <h2 data-key="missionTitle" class="section-title"></h2>
                <p data-key="missionText" style="max-width: 800px; margin: 0 auto 1.5em auto; font-size: 1.1em;"></p>
                <img src="images/KH pic 1.jpg" style="width: 100%; max-width: 600px; border-radius: 12px; margin: 1em auto; box-shadow: 0 8px 24px rgba(0,0,0,0.1);" alt="Weaver at a loom">
            </div>
        </section>

        <section id="learn" class="feature-section">
            <h2 class="section-title" data-key="learnTitle"></h2>
            <div class="feature-wrapper">
                <div class="feature">
                    <i class="fas fa-video icon"></i>
                    <h3 data-key="tutorialsTitle"></h3>
                    <p data-key="tutorialsText"></p>
                    <a class="btn" data-target="tab-tutorials"><i class="fas fa-play-circle"></i> <span data-key="watchVideosBtn"></span></a>
                </div>
                <div class="feature">
                    <i class="fas fa-chart-line icon"></i>
                    <h3 data-key="careerTitle"></h3>
                    <p data-key="careerText"></p>
                    <a class="btn" data-target="tab-career"><i class="fas fa-lightbulb"></i> <span data-key="learnMoreBtn"></span></a>
                </div>
            </div>
        </section>

        <section id="schemes" class="feature-section">
            <h2 class="section-title" data-key="aiFinderTitle"></h2>
            <div class="feature" style="flex: 1 1 100%; max-width: 800px; margin: 0 auto;">
                <h3 data-key="findSchemeTitle"></h3>
                <p data-key="findSchemeText"></p>
                <div class="recommender-form" style="text-align: left;">
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
                <div id="scheme-results" style="margin-top: 20px; padding: 15px; border-radius: 8px; background-color: #e9ecef; display: none;"></div>
                <hr style="margin: 2em 0; border-color: var(--border-color);">
                <a class="btn" data-target="tab-schemes"><i class="fas fa-list-ul"></i> <span data-key="viewAllGovtSchemes"></span></a>
                <a class="btn" data-target="tab-loans" style="margin-left: 10px;"><i class="fas fa-university"></i> <span data-key="viewBankLoans"></span></a>
            </div>
        </section>

        <section id="sell" class="feature-section">
            <h2 class="section-title" data-key="onlineShopTitle"></h2>
            <div class="feature-wrapper">
                <div class="feature">
                    <i class="fas fa-store-alt icon"></i>
                    <h3 data-key="microStorefrontsTitle"></h3>
                    <p data-key="microStorefrontsText"></p>
                    <a href="#register" class="btn"><i class="fas fa-user-plus"></i> <span data-key="createShopBtn"></span></a>
                </div>
                <div class="feature">
                    <i class="fas fa-qrcode icon"></i>
                    <h3 data-key="upiPaymentsTitle"></h3>
                    <p data-key="upiPaymentsText"></p>
                    <img src="https://i.ibb.co/9vGo2j3/qr-code-generic.png" alt="Sample QR Code" style="width: 150px; margin: 1em auto; border-radius: 8px;">
                </div>
            </div>
        </section>
        
        <section id="education" class="feature-section">
            <h2 class="section-title" data-key="childrensFutureTitle"></h2>
            <div class="feature-wrapper">
                <div class="feature">
                    <i class="fas fa-graduation-cap icon"></i>
                    <h3 data-key="scholarshipsTitle"></h3>
                    <p data-key="scholarshipsText"></p>
                    <a class="btn" data-target="tab-education"><i class="fas fa-search-dollar"></i> <span data-key="findScholarshipsBtn"></span></a>
                </div>
                <div class="feature">
                    <i class="fas fa-compass-drafting icon"></i>
                    <h3 data-key="careerPathwaysTitle"></h3>
                    <p data-key="careerPathwaysText"></p>
                    <a class="btn" data-target="tab-education"><i class="fas fa-road"></i> <span data-key="exploreCareersBtn"></span></a>
                </div>
            </div>
        </section>
        
        <section id="support" class="feature-section">
            <h2 class="section-title" data-key="partnersTitle"></h2>
             <div class="feature-wrapper">
                <div class="feature">
                    <i class="fas fa-calendar-alt icon"></i>
                    <h3 data-key="eventsTitle"></h3>
                    <p data-key="eventsText"></p>
                    <a class="btn" data-target="tab-events"><i class="fas fa-list"></i> <span data-key="viewEventsBtn"></span></a>
                </div>
                 <div class="feature">
                    <i class="fas fa-hands-helping icon"></i>
                    <h3 data-key="ngoTitle"></h3>
                    <p data-key="ngoText"></p>
                    <a class="btn" data-target="tab-partners"><i class="fas fa-link"></i> <span data-key="connectNgoBtn"></span></a>
                </div>
            </div>
        </section>
        
        <section id="register" class="feature-section">
            <h2 class="section-title" data-key="joinHubTitle"></h2>
            <div class="feature" style="flex: 1 1 100%; max-width: 600px; margin: 0 auto;">
                <form style="text-align: left; margin: auto;">
                    <label for="name" data-key="regName"></label>
                    <input type="text" id="name" name="name" required><br>
                    <label for="contact" data-key="regPhone"></label>
                    <input type="tel" id="contact" name="contact" required><br>
                    <label for="location" data-key="regAddress"></label>
                    <input type="text" id="location" name="location" value="Taraboi"><br>
                    <label for="craft" data-key="regWeavingType"></label>
                    <input type="text" id="craft" name="craft" data-key="regWeavingPlaceholder"><br>
                    <input type="submit" data-key="regSubmitBtn" class="btn" style="width: 100%; font-size: 1.2em; margin-top: 10px;">
                </form>
            </div>
        </section>
    </div>

    <footer>
        <p><i class="fas fa-cloud-download-alt"></i> <span data-key="footerOfflineText"></span></p>
        <p data-key="footerCopyright"></p>
    </footer>

    <div id="tab-tutorials" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">×</span>
            <h2 data-key="tutorialsTitle"></h2>
            <div class="info-item">
                <h3 data-key="tutorialUpiTitle"></h3>
                <p data-key="tutorialUpiText"></p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/your-upi-tutorial-video-id" title="UPI Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="info-item">
                <h3 data-key="tutorialCardTitle"></h3>
                <p data-key="tutorialCardText"></p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/your-artisan-card-video-id" title="Artisan Card Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </div>
    
    <div id="tab-career" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">×</span>
            <h2 data-key="careerTitle"></h2>
            <div class="info-item">
                <h3 data-key="careerDesignsTitle"></h3>
                <p data-key="careerDesignsText"></p>
            </div>
            <div class="info-item">
                <h3 data-key="careerFinanceTitle"></h3>
                <p data-key="careerFinanceText"></p>
            </div>
        </div>
    </div>

    <div id="tab-schemes" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">×</span>
            <h2 data-key="govtSchemesTitle"></h2>
            </div>
    </div>
    
    <div id="tab-education" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">×</span>
            <h2 data-key="childrensFutureTitle"></h2>
             <div class="info-item">
                <h3 data-key="eduScholarshipsTitle"></h3>
                <p data-key="eduScholarshipsText"></p>
                <a href="https://scholarships.gov.in/" target="_blank" class="btn"><i class="fas fa-external-link-alt"></i> <span data-key="goToNSP"></span></a>
            </div>
             <div class="info-item">
                <h3 data-key="eduCareerPathsTitle"></h3>
                <p data-key="eduCareerPathsText"></p>
                <ul>
                    <li><strong data-key="eduNift"></strong> <a href="https://www.nift.ac.in/" target="_blank">National Institute of Fashion Technology (NIFT)</a></li>
                    <li><strong data-key="eduNid"></strong> <a href="https://www.nid.edu/" target="_blank">National Institute of Design (NID)</a></li>
                    <li><strong data-key="eduIiht"></strong> <a href="http://www.iihts.csm.in/" target="_blank">Indian Institute of Handloom Technology (IIHT)</a></li>
                </ul>
            </div>
        </div>
    </div>
    <div class="floating-support-hub">
        <div class="floating-btn" id="main-support-btn">
            <i class="fas fa-headset"></i>
        </div>
    </div>

    <div id="chatbot-container">
        <div id="chatbot-header">
            <span data-key="chatHeader"></span>
            <span id="close-chatbot-btn">×</span>
        </div>
        <div id="chatbot-messages">
            </div>
        <div id="chatbot-faq-options">
            </div>
    </div>
    
    <div id="voice-popup">
        <div id="voice-popup-content">
            <i id="voice-popup-icon" class="fas fa-microphone-alt"></i>
            <p id="voice-popup-text" data-key="voiceListening"></p>
        </div>
    </div>
    
    <script>
    // --- ANIMATION SCRIPT ---
    document.addEventListener('DOMContentLoaded', function () {
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, {
            threshold: 0.1
        });

        const sections = document.querySelectorAll('.feature-section');
        sections.forEach(section => {
            observer.observe(section);
        });
    });


    // --- BILINGUAL & DYNAMIC CONTENT SCRIPT (Unchanged) ---
    const languageData = {
        en: {
            pageTitle: "KARIGAR's HUB",
            headerTitle: "KARIGAR's HUB", headerSubtitle: "A Single Portal to Empower Weavers of Taraboi",
            navAbout: "About", navLearn: "Learn", navSchemes: "Find Schemes", navSell: "Sell Craft", navEducation: "For Children", navRegister: "Join Us", navVoice: "Voice Assist",
            missionTitle: "Our Mission", missionText: "To provide the weavers of Taraboi with the digital tools, knowledge, and platform needed to grow their craft, improve their livelihood, and stand on their own feet. We aim to connect tradition with technology.",
            learnTitle: "Learn & Grow",
            tutorialsTitle: "Tutorial Videos", tutorialsText: "Step-by-step video guides in Odia to help you with everything you need.", watchVideosBtn: "Watch Videos",
            careerTitle: "Build Your Career", careerText: "Learn new designs, manage money, and build your own brand online.", learnMoreBtn: "Learn More",
            aiFinderTitle: "AI Scheme Finder", findSchemeTitle: "Find Your Perfect Scheme", findSchemeText: "Answer a few questions and our AI tool will suggest the best government schemes for you.",
            ageLabel: "What is your age?", agePlaceholder: "e.g., 45", needLabel: "What do you need help with?",
            selectOption: "-- Select an Option --", needLoan: "Loan for Business", needTraining: "New Design Training", needPension: "Pension for Old Age", needEducation: "Child's Education",
            findSchemesBtn: "Find My Schemes",
            viewAllGovtSchemes: "View All Government Schemes", viewBankLoans: "View Bank Loan Info",
            onlineShopTitle: "Your Online Shop",
            microStorefrontsTitle: "Micro-Storefronts for Artisans", microStorefrontsText: "Register to get your own personal webpage on Karigar's Hub. Showcase your products, tell your story, and sell directly to customers all over India.", createShopBtn: "Create Your Shop",
            upiPaymentsTitle: "Direct UPI Payments", upiPaymentsText: "We create a unique UPI QR code for your shop. Customers can scan and pay you directly, instantly. No extra fees!",
            childrensFutureTitle: "Future for Our Children",
            scholarshipsTitle: "Scholarships & Support", scholarshipsText: "Find government scholarships for your children's education, from school to college.", findScholarshipsBtn: "Find Scholarships",
            careerPathwaysTitle: "Career Pathways", careerPathwaysText: "Explore modern careers in design, technology, and business that build on your traditional skills.", exploreCareersBtn: "Explore Careers",
            partnersTitle: "Partners & Support",
            eventsTitle: "Events & Fairs", eventsText: "Find out about upcoming handloom events and craft fairs to sell your products.", viewEventsBtn: "View Event List",
            ngoTitle: "NGO Partners", ngoText: "Connect with non-profit organizations working to empower artisans in Odisha.", connectNgoBtn: "Connect with NGOs",
            joinHubTitle: "Join Karigar Hub Today!",
            regName: "Full Name:", regPhone: "Phone Number:", regAddress: "Village/Address:", regWeavingType: "Type of Weaving:", regWeavingPlaceholder: "e.g., Bomkai, Sambalpuri", regSubmitBtn: "Register Now",
            footerOfflineText: "Portal works even with a weak signal. Install the app for offline use!",
            footerCopyright: "© 2025 Karigar's Hub | Designed to Uplift the Weavers of Taraboi.",
            tutorialUpiTitle: "How to Use UPI (PhonePe/Google Pay)", tutorialUpiText: "This video explains how to receive money from customers using a QR code on your phone.",
            tutorialCardTitle: "How to Register for an Artisan Card", tutorialCardText: "This video shows you step-by-step how to fill the form on the government portal.",
            careerDesignsTitle: "New Design Ideas", careerDesignsText: "Learn about new color combinations and patterns that are popular. We will share new design books and ideas here every month.",
            careerFinanceTitle: "Financial Literacy", careerFinanceText: "Learn how to open a bank account, use digital payments, and why saving is important. We will organize local workshops for this.",
            govtSchemesTitle: "Government Schemes",
            eduScholarshipsTitle: "Scholarships for Children", eduScholarshipsText: "The government provides financial support for the education of artisans' children. You can apply for these schemes on the National Scholarship Portal (NSP).", goToNSP: "Go to National Scholarship Portal",
            eduCareerPathsTitle: "Career Pathways in Design & Technology", eduCareerPathsText: "If your children are interested in art and computers, they can have a great career. They can combine traditional weaving knowledge with modern skills. Here are some top institutions:",
            eduNift: "Fashion/Textile Design:", eduNid: "Product/Graphic Design:", eduIiht: "Handloom Technology:",
            voiceListening: "Listening...", voiceError: "Sorry, I didn't understand. Please try again.", voiceNavigating: "Taking you to the section.", voiceOpening: "Opening.",
            chatHeader: "Support Hub", chatWelcome: "Hello! How can I help you today? Please select an option below, or you can contact us directly.",
            chatFaq1: "How to get a loan?", chatFaq2: "How to sell my products?", chatFaq3: "How to find scholarships?", chatFaq4: "Need direct help?",
            chatAns1: "You can apply for a loan through the MUDRA scheme. Our 'AI Scheme Finder' can give you more details. We can also help you connect with the local bank.",
            chatAns2: "Register on our portal by clicking 'Join Us'. We will help you create your own online shop with a QR code for direct payments.",
            chatAns3: "Visit the 'For Children' section. We have links to the National Scholarship Portal where you can find and apply for various scholarships for your children's education.",
            chatAns4: "For direct help, you can call us or send a message on WhatsApp.",
            chatContactCall: "Call Us", chatContactWhatsapp: "WhatsApp Us"
        },
        or: {
            pageTitle: "କାରିଗର ହବ୍",
            headerTitle: "କାରିଗର ହବ୍", headerSubtitle: "ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ସଶକ୍ତ କରିବା ପାଇଁ ଏକକ ପୋର୍ଟାଲ୍",
            navAbout: "ଆମ ବିଷୟରେ", navLearn: "ଶିଖନ୍ତୁ", navSchemes: "ଯୋଜନା ଖୋଜନ୍ତୁ", navSell: "ବିକ୍ରି କରନ୍ତୁ", navEducation: "ପିଲାଙ୍କ ପାଇଁ", navRegister: "ଯୋଗ ଦିଅନ୍ତୁ", navVoice: "ଭଏସ୍ ସହାୟତା",
            missionTitle: "ଆମର ଲକ୍ଷ୍ୟ", missionText: "ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ଡିଜିଟାଲ୍ ଉପକରଣ, ଜ୍ଞାନ ଏବଂ ପ୍ଲାଟଫର୍ମ ପ୍ରଦାନ କରିବା ଯାହା ସେମାନଙ୍କର କଳାକୁ ବଢ଼ାଇବା, ଜୀବିକା ଉନ୍ନତ କରିବା ଏବଂ ନିଜ ଗୋଡ଼ରେ ଛିଡ଼ା ହେବା ପାଇଁ ଆବଶ୍ୟକ। ଆମର ଲକ୍ଷ୍ୟ ହେଉଛି ପରମ୍ପରାକୁ ପ୍ରଯୁକ୍ତିବିଦ୍ୟା ସହିତ ଯୋଡ଼ିବା।",
            learnTitle: "ଶିଖନ୍ତୁ ଓ ଆଗକୁ ବଢନ୍ତୁ",
            tutorialsTitle: "ଟ୍ୟୁଟୋରିଆଲ୍ ଭିଡିଓ", tutorialsText: "ଆପଣଙ୍କୁ ଆବଶ୍ୟକ କରୁଥିବା ସବୁକିଛିରେ ସାହାଯ୍ୟ କରିବା ପାଇଁ ଓଡ଼ିଆରେ ପର୍ଯ୍ୟାୟକ୍ରମେ ଭିଡିଓ ଗାଇଡ୍।", watchVideosBtn: "ଭିଡିଓ ଦେଖନ୍ତୁ",
            careerTitle: "ନିଜ କ୍ୟାରିୟର ଗଢନ୍ତୁ", careerText: "ନୂଆ ଡିଜାଇନ୍ ଶିଖନ୍ତୁ, ଟଙ୍କା ପରିଚାଳନା କରନ୍ତୁ, ଏବଂ ଅନଲାଇନରେ ନିଜର ବ୍ରାଣ୍ଡ୍ ତିଆରି କରନ୍ତୁ।", learnMoreBtn: "ଅଧିକ ଜାଣନ୍ତୁ",
            aiFinderTitle: "AI ସ୍କିମ୍ ଫାଇଣ୍ଡର୍", findSchemeTitle: "ଆପଣଙ୍କ ପାଇଁ ସଠିକ୍ ଯୋଜନା ଖୋଜନ୍ତୁ", findSchemeText: "କିଛି ପ୍ରଶ୍ନର ଉତ୍ତର ଦିଅନ୍ତୁ ଏବଂ ଆମର AI ଉପକରଣ ଆପଣଙ୍କ ପାଇଁ ସର୍ବୋତ୍ତମ ସରକାରୀ ଯୋଜନାଗୁଡିକର ପରାମର୍ଶ ଦେବ।",
            ageLabel: "ଆପଣଙ୍କ ବୟସ କେତେ?", agePlaceholder: "ଉଦାହରଣ, ୪୫", needLabel: "ଆପଣଙ୍କୁ କେଉଁଥିରେ ସାହାଯ୍ୟ ଦରକାର?",
            selectOption: "-- ଏକ ବିକଳ୍ପ ବାଛନ୍ତୁ --", needLoan: "ବ୍ୟବସାୟ ପାଇଁ ଋଣ", needTraining: "ନୂଆ ଡିଜାଇନ୍ ତାଲିମ", needPension: "ବୃଦ୍ଧାବସ୍ଥା ପାଇଁ ପେନସନ", needEducation: "ପିଲାର ଶିକ୍ଷା",
            findSchemesBtn: "ମୋ ପାଇଁ ଯୋଜନା ଖୋଜନ୍ତୁ",
            viewAllGovtSchemes: "ସମସ୍ତ ସରକାରୀ ଯୋଜନା ଦେଖନ୍ତୁ", viewBankLoans: "ବ୍ୟାଙ୍କ ଋଣ ସୂଚନା ଦେଖନ୍ତୁ",
            onlineShopTitle: "ଆପଣଙ୍କ ଅନଲାଇନ୍ ଦୋକାନ",
            microStorefrontsTitle: "କାରିଗରଙ୍କ ପାଇଁ ମାଇକ୍ରୋ-ଷ୍ଟୋରଫ୍ରଣ୍ଟ", microStorefrontsText: "ପଞ୍ଜୀକରଣ କରନ୍ତୁ ଏବଂ କାରିଗର ହବ୍‌ରେ ନିଜର ବ୍ୟକ୍ତିଗତ ୱେବପେଜ୍ ପାଆନ୍ତୁ। ଆପଣଙ୍କ ଉତ୍ପାଦ ପ୍ରଦର୍ଶନ କରନ୍ତୁ, ନିଜ କାହାଣୀ କୁହନ୍ତୁ, ଏବଂ ସାରା ଭାରତର ଗ୍ରାହକଙ୍କୁ ସିଧାସଳଖ ବିକ୍ରି କରନ୍ତୁ।", createShopBtn: "ଆପଣଙ୍କ ଦୋକାନ ସୃଷ୍ଟି କରନ୍ତୁ",
            upiPaymentsTitle: "ସିଧା UPI ପେମେଣ୍ଟ", upiPaymentsText: "ଆମେ ଆପଣଙ୍କ ଦୋକାନ ପାଇଁ ଏକ ସ୍ୱତନ୍ତ୍ର UPI QR କୋଡ୍ ତିଆରି କରୁ। ଗ୍ରାହକମାନେ ସ୍କାନ୍ କରି ସିଧା ଆପଣଙ୍କୁ ଟଙ୍କା ପଠାଇ ପାରିବେ।",
            childrensFutureTitle: "ଆମ ପିଲାମାନଙ୍କ ପାଇଁ ଭବିଷ୍ୟତ",
            scholarshipsTitle: "ଛାତ୍ରବୃତ୍ତି ଓ ସହାୟତା", scholarshipsText: "ଆପଣଙ୍କ ପିଲାଙ୍କ ସ୍କୁଲରୁ କଲେଜ ପର୍ଯ୍ୟନ୍ତ ଶିକ୍ଷା ପାଇଁ ସରକାରୀ ଛାତ୍ରବୃତ୍ତି ଖୋଜନ୍ତୁ।", findScholarshipsBtn: "ଛାତ୍ରବୃତ୍ତି ଖୋଜନ୍ତୁ",
            careerPathwaysTitle: "କ୍ୟାରିୟର୍ ପଥ", careerPathwaysText: "ଆପଣଙ୍କ ପାରମ୍ପରିକ କୌଶଳ ଉପରେ ଆଧାରିତ ଡିଜାଇନ୍, ଟେକ୍ନୋଲୋଜି ଏବଂ ବ୍ୟବସାୟରେ ଆଧୁନିକ କ୍ୟାରିୟର୍ ବିଷୟରେ ଜାଣନ୍ତୁ।", exploreCareersBtn: "କ୍ୟାରିୟର୍ ବିଷୟରେ ଜାଣନ୍ତୁ",
            partnersTitle: "ସହଯୋଗୀ ଓ ସହାୟତା",
            eventsTitle: "ମେଳା ଓ ଇଭେଣ୍ଟ", eventsText: "ଆପଣଙ୍କ ଉତ୍ପାଦ ବିକ୍ରି କରିବା ପାଇଁ ଆଗାମୀ ହସ୍ତତନ୍ତ ମେଳା ଏବଂ କ୍ରାଫ୍ଟ ମେଳା ବିଷୟରେ ଜାଣନ୍ତୁ।", viewEventsBtn: "ଇଭେଣ୍ଟ ତାଲିକା ଦେଖନ୍ତୁ",
            ngoTitle: "ଏନଜିଓ ସହଯୋଗୀ", ngoText: "ଓଡିଶାର କାରିଗରମାନଙ୍କୁ ସଶକ୍ତ କରିବା ପାଇଁ କାର୍ଯ୍ୟ କରୁଥିବା ଅଣ-ଲାଭକାରୀ ସଂଗଠନ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ।", connectNgoBtn: "ଏନଜିଓ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ",
            joinHubTitle: "ଆଜି ହିଁ କାରିଗର ହବ୍‌ରେ ଯୋଗ ଦିଅନ୍ତୁ!",
            regName: "ପୂରା ନାମ:", regPhone: "ଫୋନ୍ ନମ୍ବର:", regAddress: "ଗାଁ/ଠିକଣା:", regWeavingType: "ବୁଣାକାର୍ଯ୍ୟର ପ୍ରକାର:", regWeavingPlaceholder: "ଉଦାହରଣ, ବୋମକାଇ, ସମ୍ବଲପୁରୀ", regSubmitBtn: "ବର୍ତ୍ତମାନ ପଞ୍ଜୀକରଣ କରନ୍ତୁ",
            footerOfflineText: "କମ୍ ସିଗନାଲରେ ବି ପୋର୍ଟାଲ୍ କାମ କରେ। ଅଫଲାଇନ୍ ବ୍ୟବହାର ପାଇଁ ଆପ୍ ଇନଷ୍ଟଲ୍ କରନ୍ତୁ!",
            footerCopyright: "© ୨୦୨୫ କାରିଗର ହବ୍ | ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ଉନ୍ନତି ପାଇଁ ପରିକଳ୍ପିତ।",
            tutorialUpiTitle: "UPI କିପରି ବ୍ୟବହାର କରିବେ (ଫୋନ୍‌ପେ/ଗୁଗଲ୍ ପେ)", tutorialUpiText: "ଏହି ଭିଡିଓରେ, ଆପଣଙ୍କ ଫୋନରେ QR କୋଡ୍ ବ୍ୟବହାର କରି ଗ୍ରାହକଙ୍କଠାରୁ କିପରି ଟଙ୍କା ଗ୍ରହଣ କରିବେ ତାହା ବୁଝାଯାଇଛି।",
            tutorialCardTitle: "କାରିଗର କାର୍ଡ ପାଇଁ କିପରି ପଞ୍ଜୀକରଣ କରିବେ", tutorialCardText: "ଏହି ଭିଡିଓରେ ସରକାରୀ ପୋର୍ଟାଲରେ ଫର୍ମ କିପରି ପୂରଣ କରିବେ ତାହା ଦର୍ଶାଯାଇଛି।",
            careerDesignsTitle: "ନୂଆ ଡିଜାଇନ୍ ବିଚାର", careerDesignsText: "ଲୋକପ୍ରିୟ ଥିବା ନୂଆ ରଙ୍ଗ ସଂଯୋଜନା ଏବଂ ପ୍ୟାଟର୍ନ ବିଷୟରେ ଜାଣନ୍ତୁ। ଆମେ ପ୍ରତି ମାସରେ ଏଠାରେ ନୂଆ ଡିଜାଇନ୍ ବହି ଏବଂ ବିଚାର ସେୟାର କରିବୁ।",
            careerFinanceTitle: "ଆର୍ଥିକ ସାକ୍ଷରତା", careerFinanceText: "ବ୍ୟାଙ୍କ ଆକାଉଣ୍ଟ କିପରି ଖୋଲିବେ, ଡିଜିଟାଲ ପେମେଣ୍ଟ କିପରି ବ୍ୟବହାର କରିବେ, ଏବଂ ସଞ୍ଚୟ କାହିଁକି ଗୁରୁତ୍ୱପୂର୍ଣ୍ଣ ତାହା ଜାଣନ୍ତୁ। ଆମେ ଏଥିପାଇଁ ସ୍ଥାନୀୟ କର୍ମଶାଳାର ଆୟୋଜନ କରିବୁ।",
            govtSchemesTitle: "ସରକାରୀ ଯୋଜନା",
            eduScholarshipsTitle: "ପିଲାମାନଙ୍କ ପାଇଁ ଛାତ୍ରବୃତ୍ତି", eduScholarshipsText: "ସରକାର କାରିଗରଙ୍କ ପିଲାଙ୍କ ଶିକ୍ଷା ପାଇଁ ଆର୍ଥିକ ସହାୟତା ପ୍ରଦାନ କରନ୍ତି। ଆପଣ ଜାତୀୟ ଛାତ୍ରବୃତ୍ତି ପୋର୍ଟାଲ୍ (NSP) ରେ ଏହି ଯୋଜନାଗୁଡିକ ପାଇଁ ଆବେଦନ କରିପାରିବେ।", goToNSP: "ଜାତୀୟ ଛାତ୍ରବୃତ୍ତି ପୋର୍ଟାଲକୁ ଯାଆନ୍ତୁ",
            eduCareerPathsTitle: "ଡିଜାଇନ୍ ଓ ଟେକ୍ନୋଲୋଜିରେ କ୍ୟାରିୟର୍", eduCareerPathsText: "ଯଦି ଆପଣଙ୍କ ପିଲାମାନେ କଳା ଏବଂ କମ୍ପ୍ୟୁଟରରେ ଆଗ୍ରହୀ, ତେବେ ସେମାନେ ଏକ ଭଲ କ୍ୟାରିୟର୍ ଗଢିପାରିବେ। ସେମାନେ ପାରମ୍ପରିକ ବୁଣାକାରୀ ଜ୍ଞାନକୁ ଆଧୁନିକ କୌଶଳ ସହିତ ମିଶାଇ ପାରିବେ। ଏଠାରେ କିଛି ପ୍ରମୁଖ ଅନୁଷ୍ଠାନ ଅଛି:",
            eduNift: "ଫ୍ୟାଶନ୍/ଟେକ୍ସଟାଇଲ୍ ଡିଜାଇନ୍:", eduNid: "ପ୍ରଡକ୍ଟ/ଗ୍ରାଫିକ୍ ଡିଜାଇନ୍:", eduIiht: "ହସ୍ତତନ୍ତ ପ୍ରଯୁକ୍ତିବିଦ୍ୟା:",
            voiceListening: "ଶୁଣୁଛି...", voiceError: "କ୍ଷମା କରନ୍ତୁ, ମୁଁ ବୁଝିପାରିଲି ନାହିଁ। ଦୟାକରି ପୁଣି ଚେଷ୍ଟା କରନ୍ତୁ।", voiceNavigating: "ଆପଣଙ୍କୁ ବିଭାଗକୁ ନେଉଛି।", voiceOpening: "ଖୋଲୁଛି।",
            chatHeader: "ସହାୟତା କେନ୍ଦ୍ର", chatWelcome: "ନମସ୍କାର! ମୁଁ ଆଜି ଆପଣଙ୍କୁ କିପରି ସାହାଯ୍ୟ କରିପାରେ? ଦୟାକରି ନିମ୍ନରେ ଏକ ବିକଳ୍ପ ବାଛନ୍ତୁ, କିମ୍ବା ଆପଣ ଆମ ସହିତ ସିଧାସଳଖ ଯୋଗାଯୋଗ କରିପାରିବେ।",
            chatFaq1: "ଋଣ କିପରି ପାଇବି?", chatFaq2: "ମୋ ଉତ୍ପାଦ କିପରି ବିକ୍ରି କରିବି?", chatFaq3: "ଛାତ୍ରବୃତ୍ତି କିପରି ପାଇବି?", chatFaq4: "ସିଧାସଳଖ ସାହାଯ୍ୟ ଦରକାର କି?",
            chatAns1: "ଆପଣ ମୁଦ୍ରା ଯୋଜନା ମାଧ୍ୟମରେ ଋଣ ପାଇଁ ଆବେଦନ କରିପାରିବେ। ଆମର 'AI ସ୍କିମ୍ ଫାଇଣ୍ଡର୍' ଆପଣଙ୍କୁ ଅଧିକ ସୂଚନା ଦେଇପାରିବ। ଆମେ ଆପଣଙ୍କୁ ସ୍ଥାନୀୟ ବ୍ୟାଙ୍କ ସହିତ ଯୋଗାଯୋଗ କରିବାରେ ମଧ୍ୟ ସାହାଯ୍ୟ କରିପାରିବୁ।",
            chatAns2: "'ଯୋଗ ଦିଅନ୍ତୁ' ଉପରେ କ୍ଲିକ୍ କରି ଆମ ପୋର୍ଟାଲରେ ପଞ୍ଜୀକରଣ କରନ୍ତୁ। ଆମେ ଆପଣଙ୍କୁ ସିଧାସଳଖ ପେମେଣ୍ଟ ପାଇଁ QR କୋଡ୍ ସହିତ ନିଜର ଅନଲାଇନ୍ ଦୋକାନ ସୃଷ୍ଟି କରିବାରେ ସାହାଯ୍ୟ କରିବୁ।",
            chatAns3: "'ପିଲାଙ୍କ ପାଇଁ' ବିଭାଗକୁ ଯାଆନ୍ତୁ। ଆମ ପାଖରେ ଜାତୀୟ ଛାତ୍ରବୃତ୍ତି ପୋର୍ଟାଲର ଲିଙ୍କ୍ ଅଛି ଯେଉଁଠାରେ ଆପଣ ଆପଣଙ୍କ ପିଲାଙ୍କ ଶିକ୍ଷା ପାଇଁ ବିଭିନ୍ନ ଛାତ୍ରବୃତ୍ତି ପାଇପାରିବେ ଏବଂ ଆବେଦନ କରିପାରିବେ।",
            chatAns4: "ସିଧାସଳଖ ସାହାଯ୍ୟ ପାଇଁ, ଆପଣ ଆମକୁ କଲ୍ କରିପାରିବେ କିମ୍ବା ହ୍ଵାଟ୍ସଆପ୍‌ରେ ଏକ ମେସେଜ୍ ପଠାଇପାରିବେ।",
            chatContactCall: "ଆମକୁ କଲ୍ କରନ୍ତୁ", chatContactWhatsapp: "ଆମକୁ ହ୍ଵାଟ୍ସଆପ୍ କରନ୍ତୁ"
        }
    };

    let currentLanguage = 'en';

    function updateLanguage(lang) {
        currentLanguage = lang;
        document.documentElement.lang = lang;
        const elements = document.querySelectorAll('[data-key]');
        
        elements.forEach(el => {
            const key = el.dataset.key;
            const textData = languageData[lang][key];
            if (textData) {
                if (['P', 'H1', 'H2', 'H3', 'SPAN', 'A', 'LABEL', 'OPTION', 'STRONG'].includes(el.tagName)) {
                   const icon = el.querySelector('i');
                    if (icon) {
                        el.innerHTML = icon.outerHTML + ' ' + textData;
                    } else {
                        el.innerHTML = textData;
                    }
                } 
                else if (el.tagName === 'INPUT' || el.tagName === 'TEXTAREA') {
                    if (el.type === 'submit' || el.type === 'button') {
                        el.value = textData;
                    } else if (key.includes('Placeholder')) {
                         el.placeholder = textData;
                    }
                }
                 else if (el.tagName === 'TITLE') {
                    el.textContent = textData;
                }
            }
        });
        document.querySelector('[data-key="selectOption"]').textContent = languageData[lang].selectOption;
        document.querySelector('[data-key="needLoan"]').textContent = languageData[lang].needLoan;
        document.querySelector('[data-key="needTraining"]').textContent = languageData[lang].needTraining;
        document.querySelector('[data-key="needPension"]').textContent = languageData[lang].needPension;
        document.querySelector('[data-key="needEducation"]').textContent = languageData[lang].needEducation;
    }
    
    document.addEventListener('DOMContentLoaded', function () {
        updateLanguage('en'); 
        
        const langToggle = document.getElementById('language-toggle');
        langToggle.addEventListener('change', function() {
            updateLanguage(this.checked ? 'or' : 'en');
        });

        const openButtons = document.querySelectorAll('.btn[data-target]');
        const closeButtons = document.querySelectorAll('.content-tab .close-btn');

        function openTab(tabId) {
            const tab = document.getElementById(tabId);
            if (tab) tab.style.display = 'block';
        }
        
        openButtons.forEach(button => {
            button.addEventListener('click', function (event) {
                event.preventDefault();
                openTab(this.getAttribute('data-target'));
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

        const mainSupportBtn = document.getElementById('main-support-btn');
        const chatbotContainer = document.getElementById('chatbot-container');
        const closeChatbotBtn = document.getElementById('close-chatbot-btn');
        const chatbotMessages = document.getElementById('chatbot-messages');
        const faqOptionsContainer = document.getElementById('chatbot-faq-options');

        function addMessage(text, type) {
            const messageDiv = document.createElement('div');
            messageDiv.className = type === 'bot' ? 'bot-message' : 'user-message';
            messageDiv.innerHTML = text;
            chatbotMessages.appendChild(messageDiv);
            chatbotMessages.scrollTop = chatbotMessages.scrollHeight;
        }

        function showFaqOptions() {
            faqOptionsContainer.innerHTML = '';
            const faqs = [
                { key: 'chatFaq1', answerKey: 'chatAns1' },
                { key: 'chatFaq2', answerKey: 'chatAns2' },
                { key: 'chatFaq3', answerKey: 'chatAns3' },
                { key: 'chatFaq4', answerKey: 'chatAns4' }
            ];

            faqs.forEach(faq => {
                const faqBtn = document.createElement('button');
                faqBtn.className = 'faq-btn';
                faqBtn.textContent = languageData[currentLanguage][faq.key];
                faqBtn.onclick = () => {
                    addMessage(languageData[currentLanguage][faq.key], 'user');
                    setTimeout(() => {
                        addMessage(languageData[currentLanguage][faq.answerKey], 'bot');
                        if (faq.key === 'chatFaq4') {
                           const contactDiv = document.createElement('div');
                            contactDiv.className = 'bot-message';
                            contactDiv.innerHTML = `
                             <a href="tel:+91XXXXXXXXXX" class="btn" style="margin-right: 5px;">${languageData[currentLanguage].chatContactCall}</a>
                             <a href="https://wa.me/91XXXXXXXXXX" target="_blank" class="btn">${languageData[currentLanguage].chatContactWhatsapp}</a>`;
                            chatbotMessages.appendChild(contactDiv);
                            chatbotMessages.scrollTop = chatbotMessages.scrollHeight;
                        }
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
    
    const voiceAssistBtn = document.getElementById('voice-assist-btn');
    const voicePopup = document.getElementById('voice-popup');
    const voicePopupIcon = document.getElementById('voice-popup-icon');

    const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
    if (SpeechRecognition) {
        const recognition = new SpeechRecognition();
        recognition.onstart = () => {
            recognition.lang = currentLanguage === 'or' ? 'or-IN' : 'en-US';
            voicePopup.style.display = 'flex';
            voicePopupIcon.classList.add('listening');
        };
        recognition.onend = () => {
            voicePopup.style.display = 'none';
            voicePopupIcon.classList.remove('listening');
        };
        recognition.onerror = () => {
            speak(languageData[currentLanguage].voiceError);
        };
        recognition.onresult = (event) => {
            const transcript = event.results[0][0].transcript.toLowerCase();
            processVoiceCommand(transcript);
        };
        voiceAssistBtn.addEventListener('click', (e) => {
            e.preventDefault();
            recognition.start();
        });
    } else {
        voiceAssistBtn.addEventListener('click', (e) => {
            e.preventDefault();
            alert("Voice assistance is not supported in your browser.");
        });
    }

    function speak(text) {
        const utterance = new SpeechSynthesisUtterance(text);
        utterance.lang = currentLanguage === 'or' ? 'or-IN' : 'en-US';
        speechSynthesis.speak(utterance);
    }
    
    function processVoiceCommand(command) {
        let actionTaken = false;
        const commands = {
            en: { learn: 'learn', sell: 'sell', schemes: 'schemes', tutorials: 'tutorials', career: 'career'},
            or: { learn: 'ଶିଖ', sell: 'ବିକ୍ରି', schemes: 'ଯୋଜନା', tutorials: 'ଟ୍ୟୁଟୋରିଆଲ', career: 'କ୍ୟାରିୟର' }
        };
        const currentCommands = commands[currentLanguage];
        const openTabAndSpeak = (selector) => {
            speak(languageData[currentLanguage].voiceOpening);
            document.querySelector(selector).click();
            actionTaken = true;
        };
        const scrollToAndSpeak = (selector) => {
            document.getElementById(selector).scrollIntoView();
            speak(languageData[currentLanguage].voiceNavigating);
            actionTaken = true;
        };

        if (command.includes(currentCommands.learn)) scrollToAndSpeak('learn');
        else if (command.includes(currentCommands.sell)) scrollToAndSpeak('sell');
        else if (command.includes(currentCommands.schemes)) scrollToAndSpeak('schemes');
        else if (command.includes(currentCommands.tutorials)) openTabAndSpeak('.btn[data-target="tab-tutorials"]');
        else if (command.includes(currentCommands.career)) openTabAndSpeak('.btn[data-target="tab-career"]');
        
        if (!actionTaken) {
            speak(languageData[currentLanguage].voiceError);
        }
    }
    
    if ('serviceWorker' in navigator) {
        window.addEventListener('load', () => {
            navigator.serviceWorker.register('/sw.js')
                .then(reg => console.log('Service worker registered.', reg))
                .catch(err => console.log('Service worker not registered.', err));
        });
    }
    </script>
</body>
</html>
