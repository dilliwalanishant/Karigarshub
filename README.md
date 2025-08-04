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
    }

    .logo {
      width: 130px;
      height: auto;
      margin-right: 100px;
    }

    .header-text {
      flex-grow: 1;
    }

    nav {
      background-color: #4DB6AC;
      padding: 1em;
      text-align: center;
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
    }

    .feature {
      flex: 1 1 45%;
      margin: 1em;
      padding: 1.5em;
      background-color: #4DB6AC;
      border-radius: 8px;
      text-align: center;
    }

    .btn {
      display: inline-block;
      padding: 0.5em 1.5em;
      background-color: #87CED9;
      color: #1D1C3B;
      text-decoration: none;
      border-radius: 5px;
      margin-top: 1em;
      cursor: pointer;
    }

    footer {
      background-color: #1D1C3B;
      color: #FFFFFF;
      text-align: center;
      padding: 1em;
      font-size: 0.9em;
    }

    /* New Styles for Content Tabs */
    .content-tab {
        display: none; /* Hidden by default */
        position: fixed;
        z-index: 1000;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        overflow: auto;
        background-color: rgba(29, 28, 59, 0.7); /* Dark overlay */
        padding-top: 60px;
    }

    .tab-inner-content {
        background-color: #C5DCA2; /* Match body background */
        color: #1D1C3B; /* Match body text color */
        margin: 5% auto;
        padding: 40px;
        border: 1px solid #888;
        width: 80%;
        max-width: 800px;
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
      <p>PORTAL FOR ALL IN ONE {ସମସ୍ତଙ୍କ ପାଇଁ ପୋର୍ଟାଲ୍ }</p>
    </div>
  </header>

  <nav>
    <a href="#about">About Us {ଆମ ବିଷୟରେ}</a>
    <a href="#register">Join as Artisan {କାରିଗର ଭାବରେ ଯୋଗଦାନ କରନ୍ତୁ}</a>
    <a href="#crafts">Craft Categories {ହସ୍ତଶିଳ୍ପ ବର୍ଗଗୁଡ଼ିକ}</a>
    <a href="#workshops">Workshops {କର୍ମଶାଳା}</a>
    <a href="#collab">Collaborations {ସହଯୋଗିତା}</a>
    <a href="#gallery">Gallery {ଗ୍ୟାଲେରୀ}</a>
    <a href="#schemes">Schemes {ସ୍କିମ୍‌ଗୁଡ଼ିକ}</a>
    <a href="#support">Support {ସମର୍ଥନ}</a>
  </nav>

  <div class="container">
    <section id="about" class="feature-section">
      <div class="feature">
        <h2>About Karigar's Hub {କାରିଗରଙ୍କ ହବ୍ ବିଷୟରେ}</h2>
        <p>A platform to connect, empower, and celebrate traditional artisans across India. Discover their stories, their skills, and how you can support them.</p>
        <p>{ ସାରା ଭାରତରେ ପାରମ୍ପରିକ କାରିଗରମାନଙ୍କୁ ସଂଯୋଗ କରିବା, ସଶକ୍ତ କରିବା ଏବଂ ପାଳନ କରିବା ପାଇଁ ଏକ ପ୍ଲାଟଫର୍ମ। ସେମାନଙ୍କ କାହାଣୀ, ସେମାନଙ୍କ ଦକ୍ଷତା ଏବଂ ଆପଣ ସେମାନଙ୍କୁ କିପରି ସମର୍ଥନ କରିପାରିବେ ତାହା ଆବିଷ୍କାର କରନ୍ତୁ। }</p>
        <a class="btn" data-target="tab-about">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
      </div>
    </section>

    <section id="register" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Join as an Artisan {ଜଣେ କାରିଗର ଭାବରେ ଯୋଗଦାନ କରନ୍ତୁ}</h2>
        <p>Register to be part of Karigar's Hub and showcase your work to the world.</p>
        <p>{ କାରିଗର ହବ୍‌ର ଅଂଶ ହେବା ପାଇଁ ପଞ୍ଜୀକରଣ କରନ୍ତୁ ଏବଂ ଆପଣଙ୍କ କାମକୁ ବିଶ୍ୱ ସମ୍ମୁଖରେ ପ୍ରଦର୍ଶନ କରନ୍ତୁ। }</p>
        <form style="text-align: left; max-width: 500px; margin: auto;">
          <label for="name">Full Name {ପୂରା ନାମ}:</label><br>
          <input type="text" id="name" name="name" style="width: 100%; padding: 8px; margin: 6px 0;"><br>
          <label for="craft">Type of Craft {ହସ୍ତଶିଳ୍ପର ପ୍ରକାର}:</label><br>
          <input type="text" id="craft" name="craft" style="width: 100%; padding: 8px; margin: 6px 0;"><br>
          <label for="location">Location {ଲୋକେସନ୍}:</label><br>
          <input type="text" id="location" name="location" style="width: 100%; padding: 8px; margin: 6px 0;"><br>
          <label for="contact">Contact Info {ଯୋଗାଯୋଗ ସୂଚନା}:</label><br>
          <input type="text" id="contact" name="contact" style="width: 100%; padding: 8px; margin: 6px 0;"><br>
          <input type="submit" value="Register {ପଞ୍ଜୀକୃତ କରନ୍ତୁ}" style="margin-top: 10px; padding: 10px 20px; background-color: #87CED9; color: #1D1C3B; border: none; border-radius: 5px;">
        </form>
      </div>
    </section>

    <section id="crafts" class="feature-section">
      <div class="feature">
        <h2>Handloom & Weaving {ହସ୍ତତନ୍ତ ଏବଂ ବୟନ}</h2>
        <p>Explore India's rich textile traditions and regional weaves by artisans.</p>
        <p>{ ଭାରତର ସମୃଦ୍ଧ ବୟନ ପରମ୍ପରା ଏବଂ କାରିଗରମାନଙ୍କ ଦ୍ୱାରା ଆଞ୍ଚଳିକ ବୟନକୁ ଅନୁସନ୍ଧାନ କରନ୍ତୁ। }</p>
        <a class="btn" data-target="tab-crafts">Explore Crafts {ହସ୍ତଶିଳ୍ପ ଅନୁସନ୍ଧାନ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Terracotta & Pottery {ଟେରାକୋଟା ଏବଂ ମାଟି ପାତ୍ର}</h2>
        <p>Discover the beauty of natural clay artistry made with age-old techniques.</p>
        <p>{ ପୁରୁଣା କୌଶଳରେ ତିଆରି ପ୍ରାକୃତିକ ମାଟିର କଳାକୃତିର ସୌନ୍ଦର୍ଯ୍ୟ ଆବିଷ୍କାର କରନ୍ତୁ। }</p>
        <a class="btn" data-target="tab-artisans">See Artisans {କାରିଗରମାନଙ୍କୁ ଦେଖନ୍ତୁ}</a>
      </div>
    </section>

    <section id="workshops" class="feature-section">
      <div class="feature">
        <h2>Upcoming Workshops {ଆଗାମୀ କର୍ମଶାଳାଗୁଡ଼ିକ}</h2>
        <p>Hands-on training and virtual sessions by master artisans and designers.</p>
        <p>{ ଦକ୍ଷ କାରିଗର ଏବଂ ଡିଜାଇନରମାନଙ୍କ ଦ୍ୱାରା ବ୍ୟବହାରିକ ତାଲିମ ଏବଂ ଭର୍ଚୁଆଲ୍ ଅଧିବେଶନ। }</p>
        <a class="btn" data-target="tab-schedule">View Schedule {ସମୟସୂଚୀ ଦେଖନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Live Demonstrations {ଲାଇଭ୍ ପ୍ରଦର୍ଶନ}</h2>
        <p>Watch skilled craftsmen at work and learn the intricate process behind the art.</p>
        <p>{ ଦକ୍ଷ କାରିଗରମାନଙ୍କୁ କାମରେ ଦେଖନ୍ତୁ ଏବଂ କଳା ପଛରେ ଥିବା ଜଟିଳ ପ୍ରକ୍ରିୟା ଶିଖନ୍ତୁ। }</p>
        <a class="btn" data-target="tab-live">Watch Live {ଲାଇଭ୍ ଦେଖନ୍ତୁ}</a>
      </div>
    </section>

    <section id="collab" class="feature-section">
      <div class="feature">
        <h2>Collaboration Board {ସହଯୋଗ ବୋର୍ଡ}</h2>
        <p>Connect with designers, brands, and NGOs for project-based collaboration.</p>
        <p>{ ପ୍ରକଳ୍ପ-ଭିତ୍ତିକ ସହଯୋଗ ପାଇଁ ଡିଜାଇନର, ବ୍ରାଣ୍ଡ ଏବଂ ଏନଜିଓମାନଙ୍କ ସହିତ ସଂଯୋଗ କରନ୍ତୁ। }</p>
        <a class="btn" data-target="tab-collab">Start Collaborating {ସହଯୋଗ କରିବା ଆରମ୍ଭ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Community Stories {ସମ୍ପ୍ରଦାୟ କାହାଣୀଗୁଡ଼ିକ}</h2>
        <p>Real stories from artisans about change, resilience, and creativity.</p>
        <p>{ ପରିବର୍ତ୍ତନ, ସ୍ଥିରତା ଏବଂ ସୃଜନଶୀଳତା ବିଷୟରେ କାରିଗରମାନଙ୍କଠାରୁ ପ୍ରକୃତ କାହାଣୀ। }</p>
        <a class="btn" data-target="tab-stories">Read Stories {କାହାଣୀ ପଢ଼ନ୍ତୁ}</a>
      </div>
    </section>

    <section id="gallery" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Artisan Gallery</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 15px; justify-content: center;">
          <img src="images/KH pic 1.jpg" style="width: 200px; border-radius: 10px;">
          <img src="images/KH pic 2.jpg" style="width: 200px; border-radius: 10px;">
          <img src="images/KH pic 3.jpg" style="width: 200px; border-radius: 10px;">
          <img src="images/KH pic 4.jpg" style="width: 200px; border-radius: 10px;">
        </div>
      </div>
    </section>

    <section id="schemes" class="feature-section">
      <div class="feature">
        <h2>Government Schemes {ସରକାରୀ ଯୋଜନା}</h2>
        <p>Get details of central and state schemes supporting artisan livelihoods.</p>
        <p>{ କାରିଗର ଜୀବିକା ନିର୍ବାହକୁ ସମର୍ଥନ କରୁଥିବା କେନ୍ଦ୍ରୀୟ ଏବଂ ରାଜ୍ୟ ଯୋଜନାଗୁଡ଼ିକର ବିବରଣୀ ପାଆନ୍ତୁ। }</p>
        <a class="btn" data-target="tab-schemes">Explore Schemes {ସ୍କିମ୍‌ଗୁଡ଼ିକୁ ଏକ୍ସପ୍ଲୋର୍ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Grants & Loans {ଅନୁଦାନ ଏବଂ ଋଣ}</h2>
        <p>Information on how artisans can access financial assistance.</p>
        <p>{ କାରିଗରମାନେ କିପରି ଆର୍ଥିକ ସହାୟତା ପାଇପାରିବେ ସେ ବିଷୟରେ ସୂଚନା। }</p>
        <a class="btn" data-target="tab-grants">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
      </div>
    </section>

    <section id="map" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Our Artisan Network {ଆମର କାରିଗର ନେଟୱାର୍କ}</h2>
        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12311.354886437517!2d85.6382472!3d20.1304679!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a19adaa7c57c07b%3A0x8690f38fb3d92fc0!2sTaraboi%2C%20Odisha%20752050!5e1!3m2!1sen!2sin!4v1754058175270!5m2!1sen!2sin" height="400" style="border:0; width: 100%;" allowfullscreen="" loading="lazy">
        </iframe>
      </div>
    </section>

    <section id="support" class="feature-section">
      <div class="feature">
        <h2>Contact & Support {ଯୋଗାଯୋଗ ଓ ସମର୍ଥନ}</h2>
        <p>Reach out to us for help, partnership inquiries, or general info.</p>
        <p>{ ସାହାଯ୍ୟ, ସହଭାଗୀତା ପ୍ରଶ୍ନ କିମ୍ବା ସାଧାରଣ ସୂଚନା ପାଇଁ ଆମ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ }</p>
        <a class="btn" data-target="tab-support">Get in Touch {ସମ୍ପର୍କରେ ରୁହନ୍ତୁ}</a>
      </div>
    </section>
  </div>

  <footer>
    <p>© 2025 Karigar's Hub | Empowering Artisans, Celebrating Craft.</p>
    <p>{ © 2025 କାରିଗର ହବ୍ | କାରିଗରମାନଙ୍କୁ ସଶକ୍ତ କରିବା, ହସ୍ତଶିଳ୍ପ ପାଳନ କରିବା। }</p>
  </footer>

  <div id="tab-about" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>More About Karigar's Hub</h2>
      <p>Karigar's Hub is a platform dedicated to connecting, empowering, and celebrating traditional artisans across India. Here, timeless skills meet modern support, as we spotlight the stories, craftsmanship, and cultural heritage of our artisans. More than just a space—it's a growing community where traditions come alive, talents are recognized, and collaboration thrives. Whether it's through workshops, showcasing crafts, or offering support, Karigar's Hub is where artisans and admirers come together—hand in hand—to preserve and promote the soul of Indian artistry.</p>
    </div>
  </div>

  <div id="tab-crafts" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Explore Handloom & Weaving</h2>
      <p>Add detailed descriptions, images, and histories of the different handloom and weaving crafts featured on your platform. You can categorize them by region or technique.</p>
    </div>
  </div>

  <div id="tab-artisans" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Terracotta & Pottery Artisans</h2>
      <p>Showcase the profiles of artisans specializing in terracotta and pottery. Include their stories, photos of their work, and links to their portfolios.</p>
    </div>
  </div>

  <div id="tab-schedule" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Workshop Schedule</h2>
      <p>List all upcoming workshops here. Include details like the date, time, topic, instructor, cost (if any), and a registration link for each workshop.</p>
    </div>
  </div>

  <div id="tab-live" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Live Demonstrations</h2>
      <p>Embed live stream videos here or provide a schedule of upcoming live sessions where users can watch artisans at work in real-time.</p>
    </div>
  </div>

  <div id="tab-collab" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Collaboration Opportunities</h2>
      <p>This space can function as a bulletin board. Post collaboration requests from designers, brands, or NGOs looking for artisans. Artisans can also post their availability for projects.</p>
    </div>
  </div>

  <div id="tab-stories" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Community Stories</h2>
      <p>Feature in-depth articles, interviews, and photo-essays about the artisans. These stories can highlight their journey, the impact of the hub, and the cultural significance of their craft.</p>
    </div>
  </div>

  <div id="tab-schemes" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Government Schemes for Artisans</h2>
      <p>Provide a comprehensive list of relevant government schemes. For each scheme, explain the benefits, eligibility criteria, and the application process with direct links to official portals.</p>
    </div>
  </div>

  <div id="tab-grants" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Financial Assistance: Grants & Loans</h2>
      <p>Detail the various grants, loans, and other financial support options available to artisans from different organizations (government, NGOs, private sector). Provide clear guidance on how to apply.</p>
    </div>
  </div>

  <div id="tab-support" class="content-tab">
    <div class="tab-inner-content">
      <span class="close-btn">&times;</span>
      <h2>Contact & Support Information</h2>
      <p>Provide detailed contact information here, such as an email address, phone number, and a contact form. You can also include an FAQ section to answer common questions.</p>
    </div>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', function () {
      // Get all the buttons that open a tab
      const openButtons = document.querySelectorAll('.btn[data-target]');
      
      // Get all the close buttons
      const closeButtons = document.querySelectorAll('.content-tab .close-btn');

      // Function to open a tab
      function openTab(tabId) {
        const tab = document.getElementById(tabId);
        if (tab) {
          tab.style.display = 'block';
        }
      }

      // Function to close a tab
      function closeTab(tab) {
        tab.style.display = 'none';
      }

      // Add click event to all open buttons
      openButtons.forEach(button => {
        button.addEventListener('click', function (event) {
          event.preventDefault(); // Prevent page from jumping
          const targetTabId = this.getAttribute('data-target');
          openTab(targetTabId);
        });
      });

      // Add click event to all close buttons
      closeButtons.forEach(button => {
        button.addEventListener('click', function () {
          const tabToClose = this.closest('.content-tab');
          closeTab(tabToClose);
        });
      });

      // Add click event to window to close tab if clicking outside the content
      window.addEventListener('click', function (event) {
        if (event.target.classList.contains('content-tab')) {
          closeTab(event.target);
        }
      });
    });
  </script>

</body>
</html>
