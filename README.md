<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Brian Nthiwa website</title>
    <link rel="stylesheet" href="/Static/CSS/style.css">
  <styie>
     /* RESET + BASE STYLES */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: "Poppins", sans-serif;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: #f4f6f8;
      color: #333;
      line-height: 1.6;
      overflow-x: hidden;
      transition: background 0.5s ease, color 0.5s ease;
    }

    /* HEADER */
    header {
      background: #007bff;
      color: #fff;
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 2px 6px rgba(0, 0, 0, 0.15);
      animation: slideDown 0.8s ease forwards;
    }

    @keyframes slideDown {
      from { transform: translateY(-60px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    header h1 {
      font-size: 1.6rem;
      letter-spacing: 1px;
      animation: fadeIn 1.2s ease;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 1.5rem;
      align-items: center;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: 500;
      position: relative;
      transition: color 0.3s ease;
    }

    nav a::after {
      content: "";
      position: absolute;
      width: 0;
      height: 2px;
      left: 0;
      bottom: -4px;
      background: white;
      transition: width 0.3s ease;
    }

    nav a:hover::after {
      width: 100%;
    }

    nav a:hover {
      color: #e0e0e0;
    }

    /* DARK MODE TOGGLE BUTTON */
    .toggle-theme {
      background: none;
      border: 2px solid white;
      border-radius: 50%;
      color: white;
      cursor: pointer;
      font-size: 1.1rem;
      width: 35px;
      height: 35px;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.4s ease;
    }

    .toggle-theme:hover {
      background: white;
      color: #007bff;
    }

    /* HERO SECTION */
    .hero {
      background: linear-gradient(to right, #007bff, #00b4d8);
      color: white;
      text-align: center;
      padding: 6rem 2rem;
      animation: fadeIn 1.2s ease forwards;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .hero h2 {
      font-size: 2.8rem;
      margin-bottom: 1rem;
      animation: fadeInUp 1s ease forwards;
    }

    .hero p {
      font-size: 1.1rem;
      margin-bottom: 2rem;
      opacity: 0.9;
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .btn {
      background: white;
      color: #007bff;
      padding: 0.9rem 1.8rem;
      border: none;
      border-radius: 5px;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 8px rgba(255, 255, 255, 0.2);
    }

    .btn:hover {
      background: #e9ecef;
      transform: translateY(-3px);
      box-shadow: 0 6px 14px rgba(0, 0, 0, 0.2);
    }

    /* ABOUT SECTION */
    .about {
      background: white;
      text-align: center;
      padding: 4rem 2rem;
      animation: slideUp 1.2s ease forwards;
    }

    @keyframes slideUp {
      from { transform: translateY(40px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }

    .about h2 {
      color: #007bff;
      margin-bottom: 1rem;
      position: relative;
    }

    .about h2::after {
      content: "";
      width: 50px;
      height: 3px;
      background: #007bff;
      display: block;
      margin: 0.5rem auto;
      border-radius: 5px;
    }

    .about p {
      max-width: 750px;
      margin: 0 auto;
      color: #555;
    }

    /* SERVICES */
    .services {
      padding: 4rem 2rem;
      background: #f4f6f8;
      text-align: center;
    }

    .services h2 {
      color: #007bff;
      margin-bottom: 2rem;
    }

    .service-box {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 2rem;
    }

    .card {
      background: white;
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      width: 300px;
      transition: transform 0.4s ease, box-shadow 0.4s ease;
      animation: fadeInUp 1s ease;
    }

    .card: hover {
      transform: translateY(-12px) scale(1.03);
      box-shadow: 0 6px 18px rgba(0, 123, 255, 0.25);
    }

    .card h3 {
      color: #007bff;
      margin-bottom: 0.8rem;
    }

    /* CONTACT */
    .contact {
      background: white;
      text-align: center;
      padding: 4rem 2rem;
      animation: fadeIn 1s ease forwards;
    }

    .contact h2 {
      color: #007bff;
      margin-bottom: 1rem;
    }

    form {
      max-width: 500px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    input, textarea {
      padding: 0.8rem;
      border: 1px solid #ccc;
      border-radius: 5px;
      transition: all 0.3s;
    }

    input: focus, textarea: focus {
      border-color: #007bff;
      box-shadow: 0 0 6px rgba(0, 123, 255, 0.3);
      outline: none;
    }

    form button {
      background: #007bff;
      color: white;
      border: none;
      padding: 0.9rem;
      border-radius: 5px;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s ease, transform 0.3s ease;
    }

    form button: hover {
      background: #0056b3;
      transform: translateY(-3px);
    }

    /* FOOTER */
    footer {
      background: #007bff;
      color: white;
      text-align: center;
      padding: 1.5rem;
      margin-top: 3rem;
      font-size: 0.9rem;
      transition: background 0.5s ease;
    }

    /* RESPONSIVE MENU */
    .menu-toggle {
      display: none;
      font-size: 1.8rem;
      cursor: pointer;
    }

    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        display: none;
        background: #007bff;
        position: absolute;
        top: 60px;
        right: 0;
        width: 100%;
        text-align: center;
      }

      nav ul. active {
        display: flex;
        animation: fadeIn 0.4s ease;
      }

      .menu-toggle {
        display: block;
      }
    }

    /* 🌙 DARK MODE STYLES */
    body. dark {
      background: #121212;
      color: #f4f4f4;
    }

    body. dark header {
      background: #222;
    }

    body. dark .hero {
      background: linear-gradient(to right, #222, #333);
    }

    body. dark about,
    body.dark .contact {
      background: #1e1e1e;
      color: #e0e0e0;
    }

    body. dark .services {
      background: #171717;
    }

    body. dark card {
      background: #262626;
      color: #ddd;
      box-shadow: 0 2px 6px rgba(255, 255, 255, 0.05);
    }

    body. dark card: hover {
      box-shadow: 0 8px 16px rgba(255, 255, 255, 0.15);
    }

    body. dark footer {
      background: #222;
    }

    body. dark nav a::after {
      background: #00b4d8;
    }

    body dark toggle-theme {
      border-color: #00b4d8;
      color: #00b4d8;
    }

    body.dark .toggle-theme:hover {
      background: #00b4d8;
      color: #121212;
    }
  </styie>
</head>
<body>
  <header>
    <h1>Brian Nthiwa Website</h1>
    <span class="menu-toggle" onclick="toggleMenu()">☰</span>
    <nav>
      <ul id="nav-links">
        <li><a href="/Static/home.html" target="_blank">Home</a></li>
        <li><a href="/Static/about.html" target="_blank">About</a></li>
        <li><a href="/Static/services.html" target="_blank">Services</a></li>
        <li><a href="/Static/contacts.html" target="_blank">Contact</a></li>
        <li><button class="toggle-theme" onclick="toggleTheme()">🌙</button></li>
      </ul>
    </nav>
  </header>

  <section id="hero" class="hero">
    <h2>Welcome to My Animated Website</h2>
    <p>Experience clean, responsive, and user-friendly design — now with Dark Mode!</p>
    <button class="btn">Explore More</button>
  </section>

  <section id="about" class="about">
    <h2>About Us</h2>
    <p>
      We craft interactive and visually appealing websites that adapt seamlessly to your audience — day or night. Our designs are sleek, accessible, and always evolving.
    </p>
  </section>

  <section id="services" class="services">
    <h2>Our Services</h2>
    <div class="service-box">
      <div class="card">
        <h3>Web Design</h3>
        <p>Beautiful, responsive websites tailored to your brand identity.</p>
      </div>
      <div class="card">
        <h3>SEO Optimization</h3>
        <p>Boost your online visibility with data-driven SEO strategies.</p>
      </div>
      <div class="card">
        <h3>Maintenance</h3>
        <p>Keep your website secure, updated, and running smoothly 24/7.</p>
      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <h2>Contact Us</h2>
    <form>
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </section>
  <!--footer-->
<footer>
    <p>&copy; 2025 Brian Ntiwa Website. All rights reserved.</p>
  </footer>

  <script>
    function toggleMenu() {
      document.getElementById('nav-links').classList.toggle('active');
    }

    function toggleTheme() {
      const body = document.body;
      const button = document.querySelector('.toggle-theme');
      body.classList.toggle('dark');
      button.textContent = body.classList.contains('dark') ? '☀️' : '🌙';
    }
  </script>
</body>
</html>
