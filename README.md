
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

  </style>
</head>
<body>

  <!-- Header -->
  <header>
    <img src="E:\images\Karigar's hub logo.jpg" alt="Karigar's Hub Logo" class="logo">
    <div class="header-text">
      <h1>KARIGAR's HUB {କାରିଗର ହବ୍}</h1>
      <p>PORTAL FOR ALL IN ONE {ସମସ୍ତଙ୍କ ପାଇଁ ପୋର୍ଟାଲ୍ }</p>
    </div>
  </header>

  <!-- Navigation -->
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

  <!-- Main Content -->
  <div class="container">
    <section id="about" class="feature-section">
      <div class="feature">
        <h2>About Karigar's Hub {କାରିଗରଙ୍କ ହବ୍ ବିଷୟରେ}</h2>
        <p>A platform to connect, empower, and celebrate traditional artisans across India. Discover their stories, their skills, and how you can support them.</p>
        <p>{ ସାରା ଭାରତରେ ପାରମ୍ପରିକ କାରିଗରମାନଙ୍କୁ ସଂଯୋଗ କରିବା, ସଶକ୍ତ କରିବା ଏବଂ ପାଳନ କରିବା ପାଇଁ ଏକ ପ୍ଲାଟଫର୍ମ। ସେମାନଙ୍କ କାହାଣୀ, ସେମାନଙ୍କ ଦକ୍ଷତା ଏବଂ ଆପଣ ସେମାନଙ୍କୁ କିପରି ସମର୍ଥନ କରିପାରିବେ ତାହା ଆବିଷ୍କାର କରନ୍ତୁ। }</p>

        <a href="#" class="btn">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
      </div>
    </section>

    <!-- Artisan Registration Section -->
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
        <a href="#" class="btn">Explore Crafts {ହସ୍ତଶିଳ୍ପ ଅନୁସନ୍ଧାନ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Terracotta & Pottery {ଟେରାକୋଟା ଏବଂ ମାଟି ପାତ୍ର}</h2>
        <p>Discover the beauty of natural clay artistry made with age-old techniques.</p>
        <p>{ ପୁରୁଣା କୌଶଳରେ ତିଆରି ପ୍ରାକୃତିକ ମାଟିର କଳାକୃତିର ସୌନ୍ଦର୍ଯ୍ୟ ଆବିଷ୍କାର କରନ୍ତୁ। }</p>
        <a href="#" class="btn">See Artisans {କାରିଗରମାନଙ୍କୁ ଦେଖନ୍ତୁ}</a>
      </div>
    </section>

    <section id="workshops" class="feature-section">
      <div class="feature">
        <h2>Upcoming Workshops {ଆଗାମୀ କର୍ମଶାଳାଗୁଡ଼ିକ}</h2>
        <p>Hands-on training and virtual sessions by master artisans and designers.</p>
        <p>{ ଦକ୍ଷ କାରିଗର ଏବଂ ଡିଜାଇନରମାନଙ୍କ ଦ୍ୱାରା ବ୍ୟବହାରିକ ତାଲିମ ଏବଂ ଭର୍ଚୁଆଲ୍ ଅଧିବେଶନ। }</p>
        <a href="#" class="btn">View Schedule {ସମୟସୂଚୀ ଦେଖନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Live Demonstrations {ଲାଇଭ୍ ପ୍ରଦର୍ଶନ}</h2>
        <p>Watch skilled craftsmen at work and learn the intricate process behind the art.</p>
        <p>{ ଦକ୍ଷ କାରିଗରମାନଙ୍କୁ କାମରେ ଦେଖନ୍ତୁ ଏବଂ କଳା ପଛରେ ଥିବା ଜଟିଳ ପ୍ରକ୍ରିୟା ଶିଖନ୍ତୁ। }</p>
        <a href="#" class="btn">Watch Live {ଲାଇଭ୍ ଦେଖନ୍ତୁ}</a>
      </div>
    </section>

    <section id="collab" class="feature-section">
      <div class="feature">
        <h2>Collaboration Board {ସହଯୋଗ ବୋର୍ଡ}</h2>
        <p>Connect with designers, brands, and NGOs for project-based collaboration.</p>
        <p>{ ପ୍ରକଳ୍ପ-ଭିତ୍ତିକ ସହଯୋଗ ପାଇଁ ଡିଜାଇନର, ବ୍ରାଣ୍ଡ ଏବଂ ଏନଜିଓମାନଙ୍କ ସହିତ ସଂଯୋଗ କରନ୍ତୁ। }</p>
        <a href="#" class="btn">Start Collaborating {ସହଯୋଗ କରିବା ଆରମ୍ଭ କରନ୍ତୁ}</a>
      </div>
   
    <section id="gallery" class="feature-section">
      <div class="feature" style="flex: 1 1 100%;">
    <h2>Artisan Gallery</h2>
    <div style="display: flex; flex-wrap: wrap; gap: 15px; justify-content: center;">
      <img src="images/Karigar's hub logo.jpg" style="width: 200px; border-radius: 10px;">
      <img src="images/KH pic 2.jpg" style="width: 200px; border-radius: 10px;">
      <img src="images/KH pic 3.jpg" style="width: 200px; border-radius: 10px;">
      <img src="E:\images\KH pic 4.jpg" style="width: 200px; border-radius: 10px;">
    </div>
    </div>
    </section>
     
      <div class="feature">
        <h2>Community Stories {ସମ୍ପ୍ରଦାୟ କାହାଣୀଗୁଡ଼ିକ}</h2>
        <p>Real stories from artisans about change, resilience, and creativity.</p>
        <p>{ ପରିବର୍ତ୍ତନ, ସ୍ଥିରତା ଏବଂ ସୃଜନଶୀଳତା ବିଷୟରେ କାରିଗରମାନଙ୍କଠାରୁ ପ୍ରକୃତ କାହାଣୀ। }</p>
        <a href="#" class="btn">Read Stories {କାହାଣୀ ପଢ଼ନ୍ତୁ}</a>
      </div>
    </section>

    <section id="schemes" class="feature-section">
      <div class="feature">
        <h2>Government Schemes {ସରକାରୀ ଯୋଜନା}</h2>
        <p>Get details of central and state schemes supporting artisan livelihoods.</p>
        <p>{ କାରିଗର ଜୀବିକା ନିର୍ବାହକୁ ସମର୍ଥନ କରୁଥିବା କେନ୍ଦ୍ରୀୟ ଏବଂ ରାଜ୍ୟ ଯୋଜନାଗୁଡ଼ିକର ବିବରଣୀ ପାଆନ୍ତୁ। }</p>
        <a href="#" class="btn">Explore Schemes {ସ୍କିମ୍‌ଗୁଡ଼ିକୁ ଏକ୍ସପ୍ଲୋର୍ କରନ୍ତୁ}</a>
      </div>
      <div class="feature">
        <h2>Grants & Loans {ଅନୁଦାନ ଏବଂ ଋଣ}</h2>
        <p>Information on how artisans can access financial assistance.</p>
        <p>{ କାରିଗରମାନେ କିପରି ଆର୍ଥିକ ସହାୟତା ପାଇପାରିବେ ସେ ବିଷୟରେ ସୂଚନା। }</p>
        <a href="#" class="btn">Learn More {ଅଧିକ ଜାଣନ୍ତୁ}</a>
      </div>
    </section>

    <section id="map" class="feature-section">
  <div class="feature" style="flex: 1 1 100%;">
    <h2>Our Artisan Network {ଆମର କାରିଗର ନେଟୱାର୍କ}</h2>
    <iframe 
      src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d12311.354886437517!2d85.6382472!3d20.1304679!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a19adaa7c57c07b%3A0x8690f38fb3d92fc0!2sTaraboi%2C%20Odisha%20752050!5e1!3m2!1sen!2sin!4v1754058175270!5m2!1sen!2sin"
      height="400" 
      style="border:0;" 
      allowfullscreen="" 
      loading="lazy">
    </iframe>
  </div>
</section>
      
      <section id="support" class="feature-section">
      <div class="feature">
        <h2>Contact & Support {ଯୋଗାଯୋଗ ଓ ସମର୍ଥନ}</h2>
        <p>Reach out to us for help, partnership inquiries, or general info.</p>
        <p>{ ସାହାଯ୍ୟ, ସହଭାଗୀତା ପ୍ରଶ୍ନ କିମ୍ବା ସାଧାରଣ ସୂଚନା ପାଇଁ ଆମ ସହିତ ଯୋଗାଯୋଗ କରନ୍ତୁ }</p>
        <a href="#" class="btn">Get in Touch {ସମ୍ପର୍କରେ ରୁହନ୍ତୁ}</a>
      </div>
    </section>
  </div>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Karigar's Hub | Empowering Artisans, Celebrating Craft.</p>
    <p>{ &copy; 2025 କାରିଗର ହବ୍ | କାରିଗରମାନଙ୍କୁ ସଶକ୍ତ କରିବା, ହସ୍ତଶିଳ୍ପ ପାଳନ କରିବା। }</p>
  </footer>

</body>
</html>
