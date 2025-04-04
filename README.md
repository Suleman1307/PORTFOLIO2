# PORTFOLIO2
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Professional video editing and social media marketing services by Editkaro.in">
  <meta name="keywords" content="video editing, social media marketing, content creation, video production">
  <title>Editkaro.in | Professional Video Editing & Marketing Services</title>
  <style>
    :root {
      --primary: #6C63FF;
      --dark: #2F2E41;
      --light: #F8F9FA;
      --accent: #FF6584;
    }
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }
    body {
      background: var(--light);
      color: var(--dark);
      line-height: 1.6;
    }
    header {
      background: white;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      position: fixed;
      width: 100%;
      z-index: 100;
      padding: 1rem 2rem;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1rem;
    }
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      font-weight: 700;
      font-size: 1.5rem;
      color: var(--primary);
    }
    .nav-links {
      display: flex;
      list-style: none;
    }
    .nav-links li {
      margin-left: 2rem;
    }
    .nav-links a {
      text-decoration: none;
      color: var(--dark);
      font-weight: 500;
      transition: color 0.3s;
    }
    .nav-links a:hover {
      color: var(--primary);
    }
    .hamburger {
      display: none;
      cursor: pointer;
      font-size: 1.5rem;
    }
    .hero {
      height: 100vh;
      display: flex;
      align-items: center;
      background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                  url('https://images.unsplash.com/photo-1579389083078-4e7018379f7e?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80') no-repeat center/cover;
      color: white;
      text-align: center;
      padding: 0 1rem;
    }
    .hero-content h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }
    .hero-content p {
      max-width: 600px;
      margin: 0 auto 2rem;
    }
    .btn {
      display: inline-block;
      background: var(--primary);
      color: white;
      padding: 0.8rem 1.8rem;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 500;
      transition: all 0.3s;
      border: none;
      cursor: pointer;
    }
    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(108, 99, 255, 0.3);
    }
    section {
      padding: 5rem 0;
    }
    .section-title {
      text-align: center;
      margin-bottom: 3rem;
    }
    .section-title h2 {
      font-size: 2rem;
      color: var(--primary);
      position: relative;
      display: inline-block;
    }
    .section-title h2::after {
      content: '';
      position: absolute;
      bottom: -10px;
      left: 50%;
      transform: translateX(-50%);
      width: 50px;
      height: 3px;
      background: var(--accent);
    }
    .filters {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 2rem;
    }
    .filter-btn {
      background: white;
      border: 1px solid #ddd;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      cursor: pointer;
      transition: all 0.3s;
    }
    .filter-btn.active, .filter-btn:hover {
      background: var(--primary);
      color: white;
      border-color: var(--primary);
    }
    .portfolio-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1.5rem;
    }
    .portfolio-item {
      background: white;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }
    .portfolio-item:hover {
      transform: translateY(-10px);
    }
    .portfolio-item img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .portfolio-info {
      padding: 1rem;
    }
    .portfolio-info h3 {
      margin-bottom: 0.5rem;
      color: var(--dark);
    }
    .portfolio-info p {
      color: #666;
      font-size: 0.9rem;
    }
    .portfolio-info .category {
      display: inline-block;
      background: #f0f0f0;
      padding: 0.2rem 0.5rem;
      border-radius: 4px;
      font-size: 0.8rem;
      margin-top: 0.5rem;
      color: var(--primary);
    }
    .team-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }
    .team-member {
      text-align: center;
      background: white;
      padding: 1.5rem;
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    .team-member img {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 1rem;
    }
    .contact-form {
      display: grid;
      gap: 1rem;
      max-width: 600px;
      margin: 0 auto;
      background: white;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    }
    .contact-form input,
    .contact-form textarea {
      padding: 0.8rem;
      border: 1px solid #ddd;
      border-radius: 4px;
      width: 100%;
    }
    .contact-form textarea {
      height: 150px;
      resize: vertical;
    }
    .email-collector {
      margin-top: 2rem;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 0.5rem;
    }
    .email-collector input {
      padding: 0.8rem;
      border: none;
      border-radius: 4px;
      min-width: 300px;
    }
    footer {
      background: var(--dark);
      color: white;
      text-align: center;
      padding: 2rem 0;
    }
    @media (max-width: 768px) {
      .nav-links {
        position: fixed;
        top: 70px;
        left: -100%;
        width: 100%;
        height: calc(100vh - 70px);
        background: white;
        flex-direction: column;
        align-items: center;
        padding-top: 2rem;
        transition: all 0.5s;
      }
      .nav-links.active {
        left: 0;
      }
      .nav-links li {
        margin: 1rem 0;
      }
      .hamburger {
        display: block;
      }
      .hero-content h1 {
        font-size: 2rem;
      }
      .email-collector input {
        min-width: 200px;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container">
      <nav class="navbar">
        <div class="logo">Editkaro.in</div>
        <ul class="nav-links">
          <li><a href="#home">Home</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="hamburger">☰</div>
      </nav>
    </div>
  </header>

  <section class="hero" id="home">
    <div class="container">
      <div class="hero-content">
        <h1>Professional Video Editing Services</h1>
        <p>We transform your raw footage into engaging stories that captivate your audience and grow your brand.</p>
        <a href="#portfolio" class="btn">View Our Work</a>
        
        <div class="email-collector">
          <form id="subscribe-form">
            <input type="email" placeholder="Your email address" required>
            <button type="submit" class="btn">Subscribe</button>
          </form>
          <p style="width: 100%; text-align: center; margin-top: 1rem; font-size: 0.9rem;">
            Get updates on our latest work and offers
          </p>
        </div>
      </div>
    </div>
  </section>

  <section id="portfolio">
    <div class="container">
      <div class="section-title">
        <h2>Our Portfolio</h2>
      </div>
      <div class="filters">
        <button class="filter-btn active" data-filter="all">All</button>
        <button class="filter-btn" data-filter="short">Short-form</button>
        <button class="filter-btn" data-filter="long">Long-form</button>
        <button class="filter-btn" data-filter="gaming">Gaming</button>
        <button class="filter-btn" data-filter="football">Football Edits</button>
        <button class="filter-btn" data-filter="ecommerce">eCommerce Ads</button>
        <button class="filter-btn" data-filter="documentary">Documentary Style</button>
        <button class="filter-btn" data-filter="grading">Color Grading</button>
        <button class="filter-btn" data-filter="antine">Antine Videos</button>
        <button class="filter-btn" data-filter="ads">Ads</button>
      </div>
      <div class="portfolio-grid">
        <div class="portfolio-item" data-category="short">
          <img src="https://images.unsplash.com/photo-1611162617213-7d7a39e9b1d7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1074&q=80" alt="Instagram Reel">
          <div class="portfolio-info">
            <h3>Instagram Reel</h3>
            <p>30-second engaging clip for fashion brand</p>
            <span class="category">Short-form</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="long">
          <img src="https://images.unsplash.com/photo-1552581234-26160f608093?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Corporate Documentary">
          <div class="portfolio-info">
            <h3>Corporate Documentary</h3>
            <p>15-minute company profile video</p>
            <span class="category">Long-form</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="gaming">
          <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Gameplay Montage">
          <div class="portfolio-info">
            <h3>Gameplay Montage</h3>
            <p>Valorant highlights with sync edits</p>
            <span class="category">Gaming</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="football">
          <img src="https://images.unsplash.com/photo-1574629810360-7efbbe195018?ixlib=rb-4.0.3&auto=format&fit=crop&w=1293&q=80" alt="Football Highlights">
          <div class="portfolio-info">
            <h3>Football Highlights</h3>
            <p>Match highlights with dynamic editing</p>
            <span class="category">Football Edits</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="ecommerce">
          <img src="https://images.unsplash.com/photo-1607082348824-0a96f2a4b9da?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Product Ad">
          <div class="portfolio-info">
            <h3>Product Ad</h3>
            <p>60-second spot for skincare product</p>
            <span class="category">eCommerce Ads</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="documentary">
          <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Travel Documentary">
          <div class="portfolio-info">
            <h3>Travel Documentary</h3>
            <p>Short film capturing location essence</p>
            <span class="category">Documentary Style</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="grading">
          <img src="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Color Grading Sample">
          <div class="portfolio-info">
            <h3>Color Grading Sample</h3>
            <p>Before/after color correction</p>
            <span class="category">Color Grading</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="antine">
          <img src="https://images.unsplash.com/photo-1579389083078-4e7018379f7e?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80" alt="Antine Video">
          <div class="portfolio-info">
            <h3>Antine Video</h3>
            <p>Special effects showcase</p>
            <span class="category">Antine Videos</span>
          </div>
        </div>
        <div class="portfolio-item" data-category="ads">
          <img src="https://images.unsplash.com/photo-1563986768609-322da13575f3?ixlib=rb-4.0.3&auto=format&fit=crop&w=1170&q=80" alt="Brand Commercial">
          <div class="portfolio-info">
            <h3>Brand Commercial</h3>
            <p>30-second TV spot for beverage company</p>
            <span class="category">Ads</span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="about">
    <div class="container">
      <div class="section-title">
        <h2>About Us</h2>
      </div>
      <div style="max-width: 800px; margin: 0 auto; text-align: center;">
        <p>Editkaro.in is a video editing agency specializing in creating compelling content for brands, creators, and businesses. Our team of skilled editors combines technical expertise with creative storytelling to deliver videos that engage audiences and drive results.</p>
        <p style="margin-top: 1rem;">Founded in 2020, we've worked with over 50 clients across various industries, helping them communicate their message effectively through video.</p>
      </div>
      
      <div class="team-grid">
        <div class="team-member">
          <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Team Member">
          <h4>Rahul Sharma</h4>
          <p style="color: var(--primary);">Lead Editor</p>
        </div>
        <div class="team-member">
          <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Team Member">
          <h4>Priya Patel</h4>
          <p style="color: var(--primary);">Motion Graphics Designer</p>
        </div>
        <div class="team-member">
          <img src="https://randomuser.me/api/portraits/men/67.jpg" alt="Team Member">
          <h4>Arjun Mehta</h4>
          <p style="color: var(--primary);">Color Grading Specialist</p>
        </div>
        <div class="team-member">
          <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Team Member">
          <h4>Neha Gupta</h4>
          <p style="color: var(--primary);">Social Media Strategist</p>
        </div>
      </div>
    </div>
  </section>

  <section id="contact" style="background: white;">
    <div class="container">
      <div class="section-title">
        <h2>Get In Touch</h2>
      </div>
      <form class="contact-form" id="contact-form">
        <input type="text" placeholder="Your Name" name="name" required>
        <input type="email" placeholder="Your Email" name="email" required>
        <input type="tel" placeholder="Your Phone Number" name="phone">
        <textarea placeholder="Your Message" name="message" required></textarea>
        <button type="submit" class="btn">Send Message</button>
      </form>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; 2025 Editkaro.in. All rights reserved.</p>
    </div>
  </footer>

  <script>
    // Mobile Navigation
    const hamburger = document.querySelector('.hamburger');
    const navLinks = document.querySelector('.nav-links');
    hamburger.addEventListener('click', () => {
      navLinks.classList.toggle('active');
    });

    // Close mobile menu when clicking a link
    document.querySelectorAll('.nav-links a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('active');
      });
    });

    // Portfolio Filtering
    const filterButtons = document.querySelectorAll('.filter-btn');
    const portfolioItems = document.querySelectorAll('.portfolio-item');
    
    filterButtons.forEach(button => {
      button.addEventListener('click', () => {
        // Update active button
        filterButtons.forEach(btn => btn.classList.remove('active'));
        button.classList.add('active');
        
        const filterValue = button.getAttribute('data-filter');
        
        // Filter items
        portfolioItems.forEach(item => {
          if (filterValue === 'all' || item.getAttribute('data-category') === filterValue) {
            item.style.display = 'block';
          } else {
            item.style.display = 'none';
          }
        });
      });
    });

    // Smooth scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          window.scrollTo({
            top: target.offsetTop - 80,
            behavior: 'smooth'
          });
        }
      });
    });

    // Form Submissions
    document.getElementById('subscribe-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const email = this.querySelector('input[type="email"]').value;
      
      // In a real implementation, replace with your Google Apps Script URL
      // const scriptURL = 'YOUR_GOOGLE_SCRIPT_URL';
      
      // For demo purposes, we'll just show an alert
      alert('Thank you for subscribing! We would normally send this to our database.\nEmail: ' + email);
      this.reset();
    });

    document.getElementById('contact-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const formData = new FormData(this);
      const formObject = {};
      formData.forEach((value, key) => formObject[key] = value);
      
      // In a real implementation, replace with your Google Apps Script URL
      // const scriptURL = 'YOUR_GOOGLE_SCRIPT_URL';
      
      // For demo purposes, we'll just show an alert
      alert('Message sent successfully! We would normally send this to our database.\n\nDetails:\n' + 
            `Name: ${formObject.name}\n` +
            `Email: ${formObject.email}\n` +
            `Phone: ${formObject.phone}\n` +
            `Message: ${formObject.message}`);
      this.reset();
    });
  </script>
</body>
</html>
