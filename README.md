<!DOCTYPE html>
<html lang="he">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>LifePilot - מצפן לחיים</title>
  <link href="https://fonts.googleapis.com/css2?family=Assistant:wght@400;600;700&display=swap" rel="stylesheet" />
  <script src="https://kit.fontawesome.com/a2e00b8a07.js" crossorigin="anonymous"></script>
  <style>
    body {
      margin: 0;
      font-family: 'Assistant', sans-serif;
      background: linear-gradient(135deg, #e0f7fa, #ffffff);
      color: #004d40;
      direction: rtl;
      scroll-behavior: smooth;
    }

    header {
      background-color: #00acc1;
      padding: 20px 10px;
      color: white;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header h1 {
      margin: 0;
      font-size: 2.5rem;
      display: inline-block;
      vertical-align: middle;
    }

    .tagline {
      font-size: 1.2rem;
      margin-top: 5px;
    }

    nav {
      margin-top: 10px;
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: 600;
      cursor: pointer;
      padding: 8px 12px;
      border-radius: 6px;
      transition: background-color 0.3s ease;
    }

    nav a:hover {
      background-color: #00838f;
    }

    #langToggle {
      position: absolute;
      left: 20px;
      top: 20px;
      background-color: #00796b;
      color: white;
      border: none;
      padding: 8px 14px;
      border-radius: 6px;
      cursor: pointer;
      font-weight: 600;
      transition: background-color 0.3s ease;
    }

    #langToggle:hover {
      background-color: #004d40;
    }

    section {
      margin: 40px 20px;
      max-width: 1000px;
      margin-left: auto;
      margin-right: auto;
    }

    /* Video Section */
    .video-section iframe {
      width: 100%;
      max-width: 800px;
      height: 450px;
      border-radius: 12px;
      box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
      display: block;
      margin: 0 auto;
    }

    /* Features */
    .features {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 40px;
    }

    .feature {
      background-color: #ffffff;
      border-radius: 12px;
      padding: 30px;
      width: 300px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      transition: transform 0.3s ease;
    }

    .feature:hover {
      transform: translateY(-5px);
    }

    .feature i {
      font-size: 3rem;
      color: #00838f;
      margin-bottom: 10px;
    }

    .feature h3 {
      margin-bottom: 10px;
      color: #00796b;
    }

    /* About Us */
    #about-us {
      background-color: #b2ebf2;
      border-radius: 12px;
      padding: 30px;
      text-align: center;
    }

    #about-us h2 {
      color: #006064;
      margin-bottom: 25px;
    }

    .founders {
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
    }

    .founder {
      background: white;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      padding: 20px;
      width: 220px;
      text-align: center;
    }

    .founder img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 15px;
      border: 3px solid #00838f;
    }

    .founder h3 {
      margin: 10px 0 5px;
      color: #00796b;
    }

    .founder p {
      font-size: 0.9rem;
      color: #004d40;
    }

    /* What We Offer */
    #offerings {
      margin-top: 60px;
      display: flex;
      justify-content: center;
      gap: 40px;
      flex-wrap: wrap;
    }

    .offering {
      background: white;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      padding: 25px;
      width: 280px;
      text-align: center;
    }

    .offering h3 {
      color: #00796b;
      margin-bottom: 15px;
    }

    /* App Download */
    #download {
      background-color: #e0f7fa;
      border-radius: 12px;
      padding: 30px;
      text-align: center;
      margin-top: 60px;
    }

    #download h2 {
      color: #006064;
      margin-bottom: 25px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 30px;
      flex-wrap: wrap;
    }

    .buttons a {
      text-decoration: none;
      background-color: #00acc1;
      color: white;
      padding: 14px 30px;
      border-radius: 30px;
      font-weight: 600;
      font-size: 1rem;
      box-shadow: 0 3px 7px rgba(0, 0, 0, 0.2);
      transition: background-color 0.3s ease;
      display: inline-flex;
      align-items: center;
      gap: 10px;
    }

    .buttons a:hover {
      background-color: #00838f;
    }

    /* Blog */
    #blog {
      margin-top: 60px;
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
    }

    #blog h2 {
      color: #006064;
      margin-bottom: 25px;
      text-align: center;
    }

    .blog-post {
      background: white;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      border-radius: 12px;
      padding: 20px;
      margin-bottom: 20px;
      direction: rtl;
    }

    .blog-post h3 {
      color: #00796b;
      margin-bottom: 10px;
    }

    .blog-post p {
      font-size: 1rem;
      line-height: 1.4;
      color: #004d40;
    }

    /* Contact */
    #contact {
      background-color: #b2ebf2;
      border-radius: 12px;
      padding: 40px 20px;
      max-width: 600px;
      margin: 60px auto;
      text-align: center;
    }

    #contact h2 {
      color: #006064;
      margin-bottom: 25px;
    }

    #contact form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }

    #contact input,
    #contact textarea {
      padding: 12px;
      border-radius: 8px;
      border: 1px solid #80deea;
      font-size: 1rem;
      resize: vertical;
      font-family: 'Assistant', sans-serif;
    }

    #contact textarea {
      min-height: 100px;
    }

    #contact button {
      background-color: #00acc1;
      color: white;
      border: none;
      border-radius: 8px;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    #contact button:hover {
      background-color: #00838f;
    }

    /* Footer */
    footer {
      background-color: #004d40;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
      margin-top: 60px;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .features,
      .founders,
      #offerings {
        flex-direction: column;
        align-items: center;
      }

      .feature,
      .founder,
      .offering {
        width: 90%;
      }

      nav {
        justify-content: center;
      }
    }
  </style>
</head>

<body>
  <header>
    <h1>LifePilot</h1>
    <button id="langToggle">English</button>
    <p class="tagline">האפליקציה שתכוון אותך בחיים</p>
    <nav>
      <a href="#advantages">יתרונות</a>
      <a href="#video">סרטון</a>
      <a href="#about-us">מי אנחנו</a>
      <a href="#offerings">מה אנחנו נותנים</a>
      <a href="#download">הורדת האפליקציה</a>
      <a href="#blog">בלוג</a>
      <a href="#contact">צור קשר</a>
    </nav>
  </header>

  <section id="advantages" class="features">
    <div class="feature">
      <i class="fas fa-map-signs"></i>
      <h3>מצפן חכם</h3>
      <p>מקבל החלטות מושכלות ומכוון אותך להצלחה בחיים.</p>
    </div>
    <div class="feature">
      <i class="fas fa-bolt"></i>
      <h3>חיסכון בזמן</h3>
      <p>כלים שיקצרו את הדרך להשגת המטרות שלך.</p>
    </div>
    <div class="feature">
      <i class="fas fa-users"></i>
      <h3>תמיכה חברתית</h3>
      <p>קהילה תומכת והכוונה פרטנית לכל משתמש.</p>
    </div>
  </section>

  <section id="video" class="video-section">
    <iframe src="https://www.youtube.com/embed/_YOUR_VIDEO_ID_" title="LifePilot Intro Video" frameborder="0" allowfullscreen></iframe>
  </section>

  <section id="about-us">
    <h2>מי אנחנו</h2>
    <div class="founders">
      <div class="founder">
        <img src="https://i.pravatar.cc/120?img=12" alt="איליה גונצ׳ר" />
        <h3>איליה גונצ׳ר</h3>
        <p>מייסד </p>
      </div>
      <div class="founder">
        <img src="https://i.pravatar.cc/120?img=20" alt="אביחי דהן" />
        <h3>אביחי דהן</h3>
        <p>מייסד</p>
      </div>
      <div class="founder">
        <img src="https://i.pravatar.cc/120?img=32" alt="טל זית" />
        <h3>טל זית</h3>
        <p>מייסד</p>
      </div>
    </div>
  </section>

  <section id="offerings">
    <div class="offering">
      <h3>B2C - עבור משתמשים פרטיים</h3>
      <p>כלים להתמודדות יומיומית, תכנון אישי והכוונה להשגת מטרות.</p>
    </div>
    <div class="offering">
      <h3>B2B - עבור ארגונים</h3>
      <p>מערכות לשיפור פרודוקטיביות, ניהול צוותים והעצמת עובדים.</p>
    </div>
  </section>

  <section id="download">
    <h2>הורדת האפליקציה</h2>
    <div class="buttons">
      <a href="#" aria-label="Download on Google Play"><i class="fab fa-google-play"></i> הורדה ל-Android</a>
      <a href="#" aria-label="Download on App Store"><i class="fab fa-apple"></i> הורדה ל-iOS</a>
    </div>
  </section>

  <section id="blog">
    <h2>בלוג וטיפים</h2>
    <article class="blog-post">
      <h3>5 טיפים לניהול זמן יעיל</h3>
      <p>למדו כיצד לנהל את הזמן שלכם בצורה חכמה יותר ולהגיע ליותר הישגים.</p>
    </article>
    <article class="blog-post">
      <h3>כיצד לשפר את התקשורת בארגון</h3>
      <p>כלים ושיטות לקידום תקשורת בין עובדים ולשיפור האווירה בצוות.</p>
    </article>
    <article class="blog-post">
      <h3>היתרונות בשימוש ב-LifePilot</h3>
      <p>גלו איך האפליקציה שלנו תוכל לשנות את חייכם לטובה.</p>
    </article>
  </section>

  <section id="contact">
    <h2>צור קשר</h2>
    <form>
      <input type="text" id="name" name="name" placeholder="שם מלא" required />
      <input type="email" id="email" name="email" placeholder="אימייל" required />
      <textarea id="message" name="message" placeholder="הודעה" required></textarea>
      <button type="submit">שלח</button>
    </form>
  </section>

  <footer>
    &copy; 2025 LifePilot - כל הזכויות שמורות
  </footer>

  <script>
    const langToggle = document.getElementById('langToggle');
    let isHebrew = true;

    langToggle.addEventListener('click', () => {
      if (isHebrew) {
        // Change to English
        document.documentElement.lang = 'en';
        document.body.style.direction = 'ltr';
        langToggle.textContent = 'עברית';
        document.querySelector('header h1').textContent = 'LifePilot';
        document.querySelector('.tagline').textContent = 'Your compass for life';
        document.querySelector('nav a[href="#advantages"]').textContent = 'Advantages';
        document.querySelector('nav a[href="#video"]').textContent = 'Video';
        document.querySelector('nav a[href="#about-us"]').textContent = 'About Us';
        document.querySelector('nav a[href="#offerings"]').textContent = 'What We Offer';
        document.querySelector('nav a[href="#download"]').textContent = 'Download App';
        document.querySelector('nav a[href="#blog"]').textContent = 'Blog';
        document.querySelector('nav a[href="#contact"]').textContent = 'Contact';

        // Advantages section
        document.querySelector('#advantages .feature:nth-child(1) h3').textContent = 'Smart Compass';
        document.querySelector('#advantages .feature:nth-child(1) p').textContent = 'Make informed decisions and guide yourself to success.';
        document.querySelector('#advantages .feature:nth-child(2) h3').textContent = 'Time Saving';
        document.querySelector('#advantages .feature:nth-child(2) p').textContent = 'Tools to shorten your path to achieving goals.';
        document.querySelector('#advantages .feature:nth-child(3) h3').textContent = 'Social Support';
        document.querySelector('#advantages .feature:nth-child(3) p').textContent = 'Supportive community and personal guidance for every user.';

        // About Us
        document.querySelector('#about-us h2').textContent = 'About Us';
        document.querySelectorAll('.founder h3')[0].textContent = 'Iliya Goncher';
        document.querySelectorAll('.founder p')[0].textContent = 'Founder and project manager, commander in Egoz unit, with logistics and business experience';
        document.querySelectorAll('.founder h3')[1].textContent = 'Avichai Dahan';
        document.querySelectorAll('.founder p')[1].textContent = 'Lead developer, expert in advanced technologies and cybersecurity';
        document.querySelectorAll('.founder h3')[2].textContent = 'Tal Zeit';
        document.querySelectorAll('.founder p')[2].textContent = 'UX manager, graphic designer and communications consultant';

        // Offerings
        document.querySelector('#offerings .offering:nth-child(1) h3').textContent = 'B2C - For Individual Users';
        document.querySelector('#offerings .offering:nth-child(1) p').textContent = 'Tools for daily coping, personal planning and goal guidance.';
        document.querySelector('#offerings .offering:nth-child(2) h3').textContent = 'B2B - For Organizations';
        document.querySelector('#offerings .offering:nth-child(2) p').textContent = 'Systems to improve productivity, team management and employee empowerment.';

        // Download section
        document.querySelector('#download h2').textContent = 'Download the App';
        document.querySelector('#download .buttons a:nth-child(1)').textContent = 'Download for Android';
        document.querySelector('#download .buttons a:nth-child(2)').textContent = 'Download for iOS';

        // Blog
        document.querySelector('#blog h2').textContent = 'Blog and Tips';
        const blogPosts = document.querySelectorAll('.blog-post');
        blogPosts[0].querySelector('h3').textContent = '5 Tips for Effective Time Management';
        blogPosts[0].querySelector('p').textContent = 'Learn how to manage your time smarter and achieve more.';
        blogPosts[1].querySelector('h3').textContent = 'How to Improve Communication in Organizations';
        blogPosts[1].querySelector('p').textContent = 'Tools and methods to promote employee communication and improve team atmosphere.';
        blogPosts[2].querySelector('h3').textContent = 'Benefits of Using LifePilot';
        blogPosts[2].querySelector('p').textContent = 'Discover how our app can positively change your life.';

        // Contact
        document.querySelector('#contact h2').textContent = 'Contact Us';
        document.getElementById('name').placeholder = 'Full Name';
        document.getElementById('email').placeholder = 'Email';
        document.getElementById('message').placeholder = 'Message';
        document.querySelector('#contact button').textContent = 'Send';

        // Footer
        document.querySelector('footer').textContent = '© 2025 LifePilot - All rights reserved';

        isHebrew = false;
      } else {
        // Switch back to Hebrew
        document.documentElement.lang = 'he';
        document.body.style.direction = 'rtl';
        langToggle.textContent = 'English';
        document.querySelector('header h1').textContent = 'LifePilot';
        document.querySelector('.tagline').textContent = 'האפליקציה שתכוון אותך בחיים';
        document.querySelector('nav a[href="#advantages"]').textContent = 'יתרונות';
        document.querySelector('nav a[href="#video"]').textContent = 'סרטון';
        document.querySelector('nav a[href="#about-us"]').textContent = 'מי אנחנו';
        document.querySelector('nav a[href="#offerings"]').textContent = 'מה אנחנו נותנים';
        document.querySelector('nav a[href="#download"]').textContent = 'הורדת האפליקציה';
        document.querySelector('nav a[href="#blog"]').textContent = 'בלוג';
        document.querySelector('nav a[href="#contact"]').textContent = 'צור קשר';

        // Advantages section
        document.querySelector('#advantages .feature:nth-child(1) h3').textContent = 'מצפן חכם';
        document.querySelector('#advantages .feature:nth-child(1) p').textContent = 'מקבל החלטות מושכלות ומכוון אותך להצלחה בחיים.';
        document.querySelector('#advantages .feature:nth-child(2) h3').textContent = 'חיסכון בזמן';
        document.querySelector('#advantages .feature:nth-child(2) p').textContent = 'כלים שיקצרו את הדרך להשגת המטרות שלך.';
        document.querySelector('#advantages .feature:nth-child(3) h3').textContent = 'תמיכה חברתית';
        document.querySelector('#advantages .feature:nth-child(3) p').textContent = 'קהילה תומכת והכוונה פרטנית לכל משתמש.';

        // About Us
        document.querySelector('#about-us h2').textContent = 'מי אנחנו';
        document.querySelectorAll('.founder h3')[0].textContent = 'איליה גונצ׳ר';
        document.querySelectorAll('.founder p')[0].textContent = 'מייסד ומנהל פרויקט, מפקד ביחידת אגוז, בעל ניסיון לוגיסטי ועסקי';
        document.querySelectorAll('.founder h3')[1].textContent = 'אביחי דהן';
        document.querySelectorAll('.founder p')[1].textContent = 'מפתח ראשי, מומחה טכנולוגיות מתקדמות ואבטחת מידע';
        document.querySelectorAll('.founder h3')[2].textContent = 'טל זית';
        document.querySelectorAll('.founder p')[2].textContent = 'אחראי חווית משתמש, מעצב גרפי ויועץ תקשורת';

        // Offerings
        document.querySelector('#offerings .offering:nth-child(1) h3').textContent = 'B2C - עבור משתמשים פרטיים';
        document.querySelector('#offerings .offering:nth-child(1) p').textContent = 'כלים להתמודדות יומיומית, תכנון אישי והכוונה להשגת מטרות.';
        document.querySelector('#offerings .offering:nth-child(2) h3').textContent = 'B2B - עבור ארגונים';
        document.querySelector('#offerings .offering:nth-child(2) p').textContent = 'מערכות לשיפור פרודוקטיביות, ניהול צוותים והעצמת עובדים.';

        // Download section
        document.querySelector('#download h2').textContent = 'הורדת האפליקציה';
        document.querySelector('#download .buttons a:nth-child(1)').textContent = 'הורדה ל-Android';
        document.querySelector('#download .buttons a:nth-child(2)').textContent = 'הורדה ל-iOS';

        // Blog
        document.querySelector('#blog h2').textContent = 'בלוג וטיפים';
        const blogPosts = document.querySelectorAll('.blog-post');
        blogPosts[0].querySelector('h3').textContent = '5 טיפים לניהול זמן יעיל';
        blogPosts[0].querySelector('p').textContent = 'למדו כיצד לנהל את הזמן שלכם בצורה חכמה יותר ולהגיע ליותר הישגים.';
        blogPosts[1].querySelector('h3').textContent = 'כיצד לשפר את התקשורת בארגון';
        blogPosts[1].querySelector('p').textContent = 'כלים ושיטות לקידום תקשורת בין עובדים ולשיפור האווירה בצוות.';
        blogPosts[2].querySelector('h3').textContent = 'היתרונות בשימוש ב-LifePilot';
        blogPosts[2].querySelector('p').textContent = 'גלו איך האפליקציה שלנו תוכל לשנות את חייכם לטובה.';

        // Contact
        document.querySelector('#contact h2').textContent = 'צור קשר';
        document.getElementById('name').placeholder = 'שם מלא';
        document.getElementById('email').placeholder = 'אימייל';
        document.getElementById('message').placeholder = 'הודעה';
        document.querySelector('#contact button').textContent = 'שלח';

        // Footer
        document.querySelector('footer').textContent = '© 2025 LifePilot - כל הזכויות שמורות';

        isHebrew = true;
      }
    });
  </script>
</body>
</html>
