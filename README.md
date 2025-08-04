<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
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
        h1 {
            margin: 0;
        }
        p {
            margin-top: 5px;
        }
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
        nav a:hover {
            background-color: #FFFFFF;
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
        .close-btn:focus {
            color: #FFFFFF;
        }
        .video-container { /* For embedding tutorial videos */
            position: relative;
            padding-bottom: 56.25%; /* 16:9 aspect ratio */
            height: 0;
            overflow: hidden;
            max-width: 100%;
            background: #000;
            margin: 1em 0;
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
        .scheme-item, .event-item { /* For styling lists of schemes/events */
           border-bottom: 2px solid #87CED9;
           padding: 1em 0;
           margin-bottom: 1em;
        }
        .scheme-item:last-child, .event-item:last-child {
            border-bottom: none;
        }

        @media screen and (max-width: 768px) {
            .feature-section {
                flex-direction: column;
                align-items: center;
            }
            header {
                flex-direction: column;
                text-align: center;
            }
            .logo {
                margin: 0 auto 10px auto;
            }
            nav a {
                display: block;
                margin: 0.5em auto;
            }
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
        <a href="#about">About Us {ଆମ ବିଷୟରେ}</a>
        <a href="#learn">Learn & Grow {ଶିଖନ୍ତୁ ଓ ଆଗକୁ ବଢନ୍ତୁ}</a>
        <a href="#schemes">Schemes & Support {ଯୋଜନା ଓ ସହାୟତା}</a>
        <a href="#events">Events & Fairs {ମେଳା ଓ ଇଭେଣ୍ଟ}</a>
        <a href="#sell">Sell Your Craft {ନିଜ କଳା ବିକ୍ରି କରନ୍ତୁ}</a>
        <a href="#register">Join Us {ଆମ ସହ ଯୋଗ ଦିଅନ୍ତୁ}</a>
    </nav>

    <div class="container">
        
        <section id="about" class="feature-section">
            <div class="feature" style="flex: 1 1 100%; text-align:center;">
                <h2>Our Mission {ଆମର ଲକ୍ଷ୍ୟ}</h2>
                <p>To provide the weavers of Taraboi with the digital tools, knowledge, and platform needed to grow their craft, improve their livelihood, and stand on their own feet. We aim to connect tradition with technology.</p>
                <p>{ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କୁ ଡିଜିଟାଲ୍ ଉପକରଣ, ଜ୍ଞାନ ଏବଂ ପ୍ଲାଟଫର୍ମ ପ୍ରଦାନ କରିବା ଯାହା ସେମାନଙ୍କର କଳାକୁ ବଢ଼ାଇବା, ଜୀବିକା ଉନ୍ନତ କରିବା ଏବଂ ନିଜ ଗୋଡ଼ରେ ଛିଡ଼ା ହେବା ପାଇଁ ଆବଶ୍ୟକ। ଆମର ଲକ୍ଷ୍ୟ ହେଉଛି ପରମ୍ପରାକୁ ପ୍ରଯୁକ୍ତିବିଦ୍ୟା ସହିତ ଯୋଡ଼ିବା।}</p>
                <img src="images/KH pic 1.jpg" style="width: 80%; max-width: 500px; border-radius: 10px; margin: 1em auto;">
            </div>
        </section>

        <section id="learn" class="feature-section">
            <h2 class="section-title">Learn & Grow {ଶିଖନ୍ତୁ ଓ ଆଗକୁ ବଢନ୍ତୁ}</h2>
            <div class="feature">
                <h3>Tutorial Videos {ଟ୍ୟୁଟୋରିଆଲ୍ ଭିଡିଓ}</h3>
                <p>Step-by-step video guides in Odia to help you with everything you need.</p>
                <p>{ଆପଣଙ୍କୁ ଆବଶ୍ୟକ କରୁଥିବା ସମସ୍ତ ବିଷୟରେ ସାହାଯ୍ୟ କରିବା ପାଇଁ ଓଡ଼ିଆରେ ପର୍ଯ୍ୟାୟକ୍ରମେ ଭିଡିଓ ଗାଇଡ୍।}</p>
                <a class="btn" data-target="tab-tutorials">Watch Videos {ଭିଡିଓ ଦେଖନ୍ତୁ}</a>
            </div>
            <div class="feature">
                <h3>Build Your Career {ନିଜ କ୍ୟାରିୟର ଗଢନ୍ତୁ}</h3>
                <p>Learn how to create new designs, manage your money, and build your own brand.</p>
                <p>{ନୂଆ ଡିଜାଇନ୍ କିପରି ତିଆରି କରିବେ, ଟଙ୍କା ପରିଚାଳନା କରିବେ ଏବଂ ନିଜର ବ୍ରାଣ୍ଡ୍ କିପରି ତିଆରି କରିବେ ଶିଖନ୍ତୁ।}</p>
                <a class="btn" data-target="tab-career">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
            </div>
        </section>

        <section id="schemes" class="feature-section">
            <h2 class="section-title">Schemes & Support {ଯୋଜନା ଓ ସହାୟତା}</h2>
            <div class="feature">
                <h3>Government Schemes {ସରକାରୀ ଯୋଜନା}</h3>
                <p>All Central and State Government schemes available for handloom artisans in Odisha.</p>
                <p>{ଓଡ଼ିଶାର ହସ୍ତତନ୍ତ କାରିଗରମାନଙ୍କ ପାଇଁ ଉପଲବ୍ଧ ସମସ୍ତ କେନ୍ଦ୍ର ଓ ରାଜ୍ୟ ସରକାରୀ ଯୋଜନା।}</p>
                <a class="btn" data-target="tab-schemes">Explore Schemes {ଯୋଜନା ଦେଖନ୍ତୁ}</a>
            </div>
            <div class="feature">
                <h3>Bank Loans & Investments {ବ୍ୟାଙ୍କ ଋଣ ଓ ନିବେଶ}</h3>
                <p>Information on low-interest loans from banks and how to apply.</p>
                <p>{ବ୍ୟାଙ୍କରୁ କମ୍ ସୁଧରେ ଋଣ ଏବଂ କିପରି ଆବେଦନ କରିବେ ସେ ବିଷୟରେ ସୂଚନା।}</p>
                <a class="btn" data-target="tab-loans">Find Loans {ଋଣ ଖୋଜନ୍ତୁ}</a>
            </div>
        </section>
        
        <section id="events" class="feature-section">
            <h2 class="section-title">Events & Fairs {ମେଳା ଓ ଇଭେଣ୍ଟ}</h2>
            <div class="feature" style="flex: 1 1 100%;">
                <h3>Exhibitions & Melas {ପ୍ରଦର୍ଶନୀ ଓ ମେଳା}</h3>
                <p>Find out about upcoming handloom events and craft fairs in Odisha and across India.</p>
                <p>{ଓଡ଼ିଶା ଏବଂ ସାରା ଭାରତରେ ହେବାକୁ ଥିବା ହସ୍ତତନ୍ତ ଇଭେଣ୍ଟ ଏବଂ ହସ୍ତଶିଳ୍ପ ମେଳା ବିଷୟରେ ଜାଣନ୍ତୁ।}</p>
                <a class="btn" data-target="tab-events">View Event List {ଇଭେଣ୍ଟ ତାଲିକା ଦେଖନ୍ତୁ}</a>
            </div>
        </section>

        <section id="sell" class="feature-section">
            <h2 class="section-title">Sell Your Craft {ନିଜ କଳା ବିକ୍ରି କରନ୍ତୁ}</h2>
            <div class="feature" style="flex: 1 1 100%;">
                <h3>Showcase Your Products {ଆପଣଙ୍କ ଉତ୍ପାଦ ପ୍ରଦର୍ଶନ କରନ୍ତୁ}</h3>
                <p>Register with us to create your own page on Karigar Hub and sell your products directly to customers.</p>
                <p>{ଆମ ସହିତ ପଞ୍ଜୀକରଣ କରନ୍ତୁ ଏବଂ କାରିଗର ହବ୍‌ରେ ନିଜର ପେଜ୍ ତିଆରି କରି ଗ୍ରାହକମାନଙ୍କୁ ସିଧାସଳଖ ଆପଣଙ୍କ ଉତ୍ପାଦ ବିକ୍ରି କରନ୍ତୁ।}</p>
                 <div style="display: flex; flex-wrap: wrap; gap: 15px; justify-content: center; margin-top: 1em;">
                    <img src="images/KH pic 2.jpg" style="width: 200px; height:200px; object-fit:cover; border-radius: 10px;">
                    <img src="images/KH pic 3.jpg" style="width: 200px; height:200px; object-fit:cover; border-radius: 10px;">
                    <img src="images/KH pic 4.jpg" style="width: 200px; height:200px; object-fit:cover; border-radius: 10px;">
                </div>
            </div>
        </section>
        
        <section id="register" class="feature-section">
            <h2 class="section-title">Join Karigar Hub Today! {ଆଜି ହିଁ କାରିଗର ହବ୍‌ରେ ଯୋଗ ଦିଅନ୍ତୁ!}</h2>
            <div class="feature" style="flex: 1 1 100%;">
                <form style="text-align: left; max-width: 500px; margin: auto;">
                    <label for="name">Full Name {ପୂରା ନାମ}:</label><br>
                    <input type="text" id="name" name="name" required style="width: 100%; padding: 8px; margin: 6px 0;"><br>
                    <label for="contact">Phone Number {ଫୋନ୍ ନମ୍ବର}:</label><br>
                    <input type="tel" id="contact" name="contact" required style="width: 100%; padding: 8px; margin: 6px 0;"><br>
                    <label for="location">Village/Address {ଗାଁ/ଠିକଣା}:</label><br>
                    <input type="text" id="location" name="location" value="Taraboi" style="width: 100%; padding: 8px; margin: 6px 0;"><br>
                    <label for="craft">Type of Weaving {ବୁଣାକାର୍ଯ୍ୟର ପ୍ରକାର}:</label><br>
                    <input type="text" id="craft" name="craft" placeholder="e.g., Bomkai, Sambalpuri" style="width: 100%; padding: 8px; margin: 6px 0;"><br>
                    <input type="submit" value="Register Now {ବର୍ତ୍ତମାନ ପଞ୍ଜୀକରଣ କରନ୍ତୁ}" style="margin-top: 10px; padding: 10px 20px; background-color: #87CED9; color: #1D1C3B; border: none; border-radius: 5px; width: 100%; font-size: 1.2em; cursor: pointer;">
                </form>
            </div>
        </section>

        <section id="map" class="feature-section">
            <h2 class="section-title">Our Artisan Network in Taraboi {ତାରାବୋଇରେ ଆମର କାରିଗର ନେଟୱାର୍କ}</h2>
            <div class="feature" style="flex: 1 1 100%;">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3748.807914481075!2d85.52928801486898!3d20.017180986556156!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a19001362e33671%3A0x67341b525f0a207!2sTaraboi%2C%20Odisha%20752020!5e0!3m2!1sen!2sin!4v1660000000000!5m2!1sen!2sin" height="400" style="border:0; width: 100%;" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </section>

    </div>

    <footer>
        <p>© 2025 Karigar's Hub | Designed to Uplift the Weavers of Taraboi.</p>
        <p>{© 2025 କାରିଗର ହବ୍ | ତାରାବୋଇର ବୁଣାକାରମାନଙ୍କ ଉନ୍ନତି ପାଇଁ ପରିକଳ୍ପିତ।}</p>
    </footer>

    <div id="tab-tutorials" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Tutorial Videos {ଟ୍ୟୁଟୋରିଆଲ୍ ଭିଡିଓ}</h2>
            <p>Watch these videos in Odia to learn important skills.</p>
            <div class="scheme-item">
                <h3>How to Register for an Artisan Card {କାରିଗର କାର୍ଡ ପାଇଁ କିପରି ପଞ୍ଜୀକରଣ କରିବେ}</h3>
                <p>This video shows you step-by-step how to fill the form on the government portal and what documents are needed.</p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/VIDEO_ID" title="Artisan Card Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
            <div class="scheme-item">
                <h3>How to Take Good Photos of Your Products {ଉତ୍ପାଦର ଭଲ ଫଟୋ କିପରି ଉଠାଇବେ}</h3>
                <p>Learn how to use any mobile phone to take clear and beautiful photos of your sarees and fabrics to attract customers.</p>
                <div class="video-container">
                    <iframe src="https://www.youtube.com/embed/VIDEO_ID" title="Product Photography Tutorial" frameborder="0" allowfullscreen></iframe>
                </div>
            </div>
        </div>
    </div>
    
    <div id="tab-career" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Build Your Career {ନିଜ କ୍ୟାରିୟର ଗଢନ୍ତୁ}</h2>
             <p>Resources to help you grow your skills and income.</p>
            <div class="scheme-item">
                <h3>New Design Ideas {ନୂଆ ଡିଜାଇନ୍ ਵਿਚਾਰ}</h3>
                <p>Learn about new color combinations and patterns that are popular in the market. We will share new design books and ideas here every month.</p>
            </div>
            <div class="scheme-item">
                <h3>Financial Literacy {ଆର୍ଥିକ ସାକ୍ଷରତା}</h3>
                <p>Learn how to open a bank account, how to use digital payments like PhonePe or Google Pay, and why saving money is important. We will organize local workshops for this.</p>
            </div>
        </div>
    </div>

    <div id="tab-schemes" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Government Schemes for Handloom Artisans {ହସ୍ତତନ୍ତ କାରିଗରଙ୍କ ପାଇଁ ସରକାରୀ ଯୋଜନା}</h2>
            <div class="scheme-item">
                <h3>National Handloom Development Programme (NHDP)</h3>
                <p><strong>Benefit:</strong> Provides financial assistance for looms, accessories, design innovation, and skill upgradation.</p>
                <p><strong>Who can apply:</strong> Weavers who have an Artisan Card.</p>
                <a href="https://handlooms.nic.in/" target="_blank" class="btn">Official Portal</a>
            </div>
             <div class="scheme-item">
                <h3>Pradhan Mantri Weavers MUDRA Scheme</h3>
                <p><strong>Benefit:</strong> Provides loans at a very low interest rate (6%) for working capital needs.</p>
                <p><strong>Who can apply:</strong> All handloom weavers.</p>
                <a href="https://www.mudra.org.in/" target="_blank" class="btn">Learn More</a>
            </div>
             <div class="scheme-item">
                <h3>"Baristha Bunakar Sahayata Yojana" (Odisha State Scheme)</h3>
                <p><strong>Benefit:</strong> Monthly financial assistance for weavers above the age of 60.</p>
                <p><strong>Who can apply:</strong> Senior weavers of Odisha.</p>
                <a href="https://handloom.odisha.gov.in/schemes/" target="_blank" class="btn">State Portal</a>
            </div>
        </div>
    </div>

    <div id="tab-loans" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Bank Loans & Financial Support {ବ୍ୟାଙ୍କ ଋଣ ଓ ଆର୍ଥିକ ସହାୟତା}</h2>
            <p>Many banks offer special loans for artisans under the MUDRA scheme. We can help you connect with the nearest bank branch and assist with the application process.</p>
            <p><strong>Banks providing MUDRA loans:</strong></p>
            <ul>
                <li>State Bank of India (SBI)</li>
                <li>Punjab National Bank (PNB)</li>
                <li>Utkal Grameen Bank</li>
                <li>Bandhan Bank</li>
            </ul>
            <p>We will soon upload a video tutorial explaining the full loan application process.</p>
        </div>
    </div>
    
    <div id="tab-events" class="content-tab">
        <div class="tab-inner-content">
            <span class="close-btn">&times;</span>
            <h2>Upcoming Events & Fairs {ଆଗାମୀ ମେଳା ଓ ଇଭେଣ୍ଟ}</h2>
            <div class="event-item">
                <h3>Toshali National Crafts Mela, Bhubaneswar</h3>
                <p><strong>When:</strong> Usually in December every year.</p>
                <p><strong>What it is:</strong> One of the biggest craft fairs in Eastern India. A great opportunity to showcase and sell products.</p>
                <p><strong>How to Enroll:</strong> We will provide updates and help with the application form when the dates are announced.</p>
            </div>
            <div class="event-item">
                <h3>Dilli Haat, New Delhi - Odisha Handloom Stall</h3>
                <p><strong>When:</strong> Stalls are rotated. Dates are announced by the Handloom department.</p>
                <p><strong>What it is:</strong> A permanent exhibition space in Delhi. Getting a stall here means huge exposure.</p>
                 <p><strong>How to Enroll:</strong> Applications are usually submitted through the State Handloom Directorate. We will notify you.</p>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const openButtons = document.querySelectorAll('.btn[data-target]');
            const closeButtons = document.querySelectorAll('.content-tab .close-btn');

            function openTab(tabId) {
                const tab = document.getElementById(tabId);
                if (tab) {
                    tab.style.display = 'block';
                }
            }

            function closeAllTabs() {
                document.querySelectorAll('.content-tab').forEach(tab => {
                    tab.style.display = 'none';
                });
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
    </script>

</body>
</html>
