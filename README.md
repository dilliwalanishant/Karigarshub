
<!DOCTYPE html>
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
      /* Added for smooth scrolling */
      scroll-margin-top: 20px;
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
    }

    footer {
      background-color: #1D1C3B;
      color: #FFFFFF;
      text-align: center;
      padding: 1em;
      font-size: 0.9em;
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
        <a href="#about-details" class="btn">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
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
        <a href="#crafts-details" class="btn">Explore Crafts {ହସ୍ତଶିଳ୍ପ ଅନୁସନ୍ଧାନ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Terracotta & Pottery {ଟେରାକୋଟା ଏବଂ ମାଟି ପାତ୍ର}</h2>
        <p>Discover the beauty of natural clay artistry made with age-old techniques.</p>
        <p>{ ପୁରୁଣା କୌଶଳରେ ତିଆରି ପ୍ରାକୃତିକ ମାଟିର କଳାକୃତିର ସୌନ୍ଦର୍ଯ୍ୟ ଆବିଷ୍କାର କରନ୍ତୁ। }</p>
        <a href="#artisan-profiles" class="btn">See Artisans {କାରିଗରମାନଙ୍କୁ ଦେଖନ୍ତୁ}</a>
      </div>
    </section>

    <section id="workshops" class="feature-section">
      <div class="feature">
        <h2>Upcoming Workshops {ଆଗାମୀ କର୍ମଶାଳାଗୁଡ଼ିକ}</h2>
        <p>Hands-on training and virtual sessions by master artisans and designers.</p>
        <p>{ ଦକ୍ଷ କାରିଗର ଏବଂ ଡିଜାଇନରମାନଙ୍କ ଦ୍ୱାରା ବ୍ୟବହାରିକ ତାଲିମ ଏବଂ ଭର୍ଚୁଆଲ୍ ଅଧିବେଶନ। }</p>
        <a href="#workshops-schedule" class="btn">View Schedule {ସମୟସୂଚୀ ଦେଖନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Live Demonstrations {ଲାଇଭ୍ ପ୍ରଦର୍ଶନ}</h2>
        <p>Watch skilled craftsmen at work and learn the intricate process behind the art.</p>
        <p>{ ଦକ୍ଷ କାରିଗରମାନଙ୍କୁ କାମରେ ଦେଖନ୍ତୁ ଏବଂ କଳା ପଛରେ ଥିବା ଜଟିଳ ପ୍ରକ୍ରିୟା ଶିଖନ୍ତୁ। }</p>
        <a href="#live-demos" class="btn">Watch Live {ଲାଇଭ୍ ଦେଖନ୍ତୁ}</a>
      </div>
    </section>

    <section id="collab" class="feature-section">
      <div class="feature">
        <h2>Collaboration Board {ସହଯୋଗ ବୋର୍ଡ}</h2>
        <p>Connect with designers, brands, and NGOs for project-based collaboration.</p>
        <p>{ ପ୍ରକଳ୍ପ-ଭିତ୍ତିକ ସହଯୋଗ ପାଇଁ ଡିଜାଇନର, ବ୍ରାଣ୍ଡ ଏବଂ ଏନଜିଓମାନଙ୍କ ସହିତ ସଂଯୋଗ କରନ୍ତୁ। }</p>
        <a href="#collaboration-details" class="btn">Start Collaborating {ସହଯୋଗ କରିବା ଆରମ୍ଭ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Community Stories {ସମ୍ପ୍ରଦାୟ କାହାଣୀଗୁଡ଼ିକ}</h2>
        <p>Real stories from artisans about change, resilience, and creativity.</p>
        <p>{ ପରିବର୍ତ୍ତନ, ସ୍ଥିରତା ଏବଂ ସୃଜନଶୀଳତା ବିଷୟରେ କାରିଗରମାନଙ୍କଠାରୁ ପ୍ରକୃତ କାହାଣୀ। }</p>
        <a href="#community-stories-details" class="btn">Read Stories {କାହାଣୀ ପଢ଼ନ୍ତୁ}</a>
      </div>
    </section>
    
    <section id="gallery" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Artisan Gallery {କାରିଗର ଗ୍ୟାଲେରୀ}</h2>
        <div style="display: flex; flex-wrap: wrap; gap: 15px; justify-content: center;">
          <img src="images/KH pic 1.jpg" alt="Artisan work 1" style="width: 200px; border-radius: 10px;">
          <img src="images/KH pic 2.jpg" alt="Artisan work 2" style="width: 200px; border-radius: 10px;">
          <img src="images/KH pic 3.jpg" alt="Artisan work 3" style="width: 200px; border-radius: 10px;">
          <img src="images/KH pic 4.jpg" alt="Artisan work 4" style="width: 200px; border-radius: 10px;">
        </div>
      </div>
    </section>
      
    <section id="schemes" class="feature-section">
      <div class="feature">
        <h2>Government Schemes {ସରକାରୀ ଯୋଜନା}</h2>
        <p>Get details of central and state schemes supporting artisan livelihoods.</p>
        <p>{ କାରିଗର ଜୀବିକା ନିର୍ବାହକୁ ସମର୍ଥନ କରୁଥିବା କେନ୍ଦ୍ରୀୟ ଏବଂ ରାଜ୍ୟ ଯୋଜନାଗୁଡ଼ିକର ବିବରଣୀ ପାଆନ୍ତୁ। }</p>
        <a href="#schemes-details" class="btn">Explore Schemes {ସ୍କିମ୍‌ଗୁଡ଼ିକୁ ଏକ୍ସପ୍ଲୋର୍ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Grants & Loans {ଅନୁଦାନ ଏବଂ ଋଣ}</h2>
        <p>Information on how artisans can access financial assistance.</p>
        <p>{ କାରିଗରମାନେ କିପରି ଆର୍ଥିକ ସହାୟତା ପାଇପାରିବେ ସେ ବିଷୟରେ ସୂଚନା। }</p>
        <a href="#grants-details" class="btn">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
      </div>
    </section>

    <div id="about-details" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>More About Karigar's Hub {କାରିଗରଙ୍କ ହବ୍ ବିଷୟରେ ଅଧିକ}</h2>
        <p>Add your detailed information about the hub's mission, vision, and the team behind it here.</p>
        <p>{ ଏଠାରେ ହବ୍‌ର ଲକ୍ଷ୍ୟ, ଦୃଷ୍ଟିକୋଣ ଏବଂ ଏହା ପଛରେ ଥିବା ଦଳ ବିଷୟରେ ଆପଣଙ୍କର ବିସ୍ତୃତ ସୂଚନା ଯୋଗ କରନ୍ତୁ। }</p>
      </div>
    </div>
    
    <div id="crafts-details" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Explore Crafts In-Depth {ହସ୍ତଶିଳ୍ପକୁ ଗଭୀର ଭାବରେ ଅନୁସନ୍ଧାନ କରନ୍ତୁ}</h2>
        <p>Provide detailed information on various craft categories, their history, and significance.</p>
        <p>{ ବିଭିନ୍ନ ହସ୍ତଶିଳ୍ପ ବର୍ଗ, ସେଗୁଡିକର ଇତିହାସ ଏବଂ ମହତ୍ତ୍ୱ ଉପରେ ବିସ୍ତୃତ ସୂଚନା ପ୍ରଦାନ କରନ୍ତୁ। }</p>
      </div>
    </div>

    <div id="artisan-profiles" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Meet Our Artisans {ଆମର କାରିଗରମାନଙ୍କୁ ଭେଟନ୍ତୁ}</h2>
        <p>Showcase profiles of registered artisans, their stories, and their products here.</p>
        <p>{ ପଞ୍ଜୀକୃତ କାରିଗରମାନଙ୍କର ପ୍ରୋଫାଇଲ୍, ସେମାନଙ୍କର କାହାଣୀ ଏବଂ ସେମାନଙ୍କର ଉତ୍ପାଦଗୁଡ଼ିକୁ ଏଠାରେ ପ୍ରଦର୍ଶନ କରନ୍ତୁ। }</p>
      </div>
    </div>

    <div id="workshops-schedule" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Workshop Schedule {କର୍ମଶାଳା ସମୟସୂଚୀ}</h2>
        <p>Display a detailed schedule of upcoming workshops, including dates, times, topics, and registration links.</p>
        <p>{ ଆଗାମୀ କର୍ମଶାଳାଗୁଡ଼ିକର ଏକ ବିସ୍ତୃତ ସମୟସୂଚୀ, ତାରିଖ, ସମୟ, ବିଷୟ ଏବଂ ପଞ୍ଜୀକରଣ ଲିଙ୍କ୍ ସହିତ ପ୍ରଦର୍ଶନ କରନ୍ତୁ। }</p>
      </div>
    </div>

    <div id="live-demos" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Live Demonstration Streams {ଲାଇଭ୍ ପ୍ରଦର୍ଶନ ଧାରା}</h2>
        <p>Embed live video streams or list scheduled live events with links to watch them.</p>
        <p>{ ଲାଇଭ୍ ଭିଡିଓ ଷ୍ଟ୍ରିମ୍ ଏମ୍ବେଡ୍ କରନ୍ତୁ କିମ୍ବା ସେଗୁଡିକୁ ଦେଖିବା ପାଇଁ ଲିଙ୍କ୍ ସହିତ ଅନୁସୂଚିତ ଲାଇଭ୍ ଇଭେଣ୍ଟଗୁଡିକ ତାଲିକାଭୁକ୍ତ କରନ୍ତୁ। }</p>
      </div>
    </div>

    <div id="collaboration-details" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Collaboration Opportunities {ସହଯୋଗ ସୁଯୋଗ}</h2>
        <p>Provide details on how designers, brands, and artisans can connect and collaborate on projects.</p>
        <p>{ ଡିଜାଇନର୍, ବ୍ରାଣ୍ଡ୍, ଏବଂ କାରିଗରମାନେ କିପରି ପ୍ରକଳ୍ପଗୁଡ଼ିକରେ ସଂଯୋଗ ଏବଂ ସହଯୋଗ କରିପାରିବେ ସେ ସମ୍ବନ୍ଧରେ ବିବରଣୀ ପ୍ରଦାନ କରନ୍ତୁ। }</p>
      </div>
    </div>
    
    <div id="community-stories-details" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Inspirational Artisan Stories {ପ୍ରେରଣାଦାୟୀ କାରିଗର କାହାଣୀ}</h2>
        <p>Feature full-length stories and testimonials from artisans in the community here.</p>
        <p>{ ଏଠାରେ ସମ୍ପ୍ରଦାୟର କାରିଗରମାନଙ୍କଠାରୁ ପୂର୍ଣ୍ଣ-ଦୈର୍ଘ୍ୟ କାହାଣୀ ଏବଂ ପ୍ରଶଂସାପତ୍ର ବୈଶିଷ୍ଟ୍ୟ କରନ୍ତୁ। }</p>
      </div>
    </div>

    <div id="schemes-details" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Detailed Government Schemes {ବିସ୍ତୃତ ସରକାରୀ ଯୋଜନା}</h2>
        <p>List and explain various government schemes, eligibility criteria, and application processes.</p>
        <p>{ ବିଭିନ୍ନ ସରକାରୀ ଯୋଜନା, ଯୋଗ୍ୟତା ମାନଦଣ୍ଡ, ଏବଂ ଆବେଦନ ପ୍ରକ୍ରିୟାକୁ ତାଲିକାଭୁକ୍ତ କରନ୍ତୁ ଏବଂ ବୁଝାନ୍ତୁ। }</p>
      </div>
    </div>
    
    <div id="grants-details" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Financial Assistance: Grants & Loans {ଆର୍ଥିକ ସହାୟତା: ଅନୁଦାନ ଏବଂ ଋଣ}</h2>
        <p>Provide detailed information on available grants, loans, and how artisans can apply for them.</p>
        <p>{ ଉପଲବ୍ଧ ଅନୁଦାନ, ଋଣ, ଏବଂ କାରିଗରମାନେ କିପରି ସେଗୁଡିକ ପାଇଁ ଆବେଦନ କରିପାରିବେ ସେ ସମ୍ବନ୍ଧରେ ବିସ୍ତୃତ ସୂଚନା ପ୍ରଦାନ କରନ୍ତୁ। }</p>
      </div>
    </div>
    
    <section id="map" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
        <h2>Our Artisan Network {ଆମର କାରିଗର ନେଟୱାର୍କ}</h2>
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15020356.34057863!2d70.83510842234554!3d22.87123996229564!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x306357421b5e4a23%3A0x96c02b2b54249a8!2sIndia!5e0!3m2!1sen!2sin!4v1663412221684!5m2!1sen!2sin"
          width="100%"
          height="400" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>
    </section>
      
    <section id="support" class="feature-section">
      <div class="feature">
        <h2>Contact & Support {ଯୋଗାଯୋଗ ଓ ସମର୍ଥନ}</h2>
        <p>Reach out to us for help, partnership inquiries, or general info.</p>
        <p>{ ସାହାଯ୍ୟ, ସହଭାଗୀତା ପ୍ରଶ୍ନ କିମ୍ବା ସାଧାରଣ ସୂଚନା ପାଇଁ ଆମ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ }</p>
        <a href="mailto:support@karigarshub.com" class="btn">Get in Touch {ସମ୍ପର୍କରେ ରୁହନ୍ତୁ}</a>
      </div>
    </section>
  </div>

  <footer>
    <p>© 2025 Karigar's Hub | Empowering Artisans, Celebrating Craft.</p>
    <p>{ © 2025 କାରିଗର ହବ୍ | କାରିଗରମାନଙ୍କୁ ସଶକ୍ତ କରିବା, ହସ୍ତଶିଳ୍ପ ପାଳନ କରିବା। }</p>
  </footer>

</body>
</html>
