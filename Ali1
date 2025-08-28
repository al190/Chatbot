<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ChatBot Pro - AI Customer Service Solutions</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      line-height: 1.6;
      color: #333;
      background: linear-gradient(135deg, #28757b, #1e5b61, #28757b);
      background-attachment: fixed;
    }

    /* Navigation */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(40, 117, 123, 0.95);
      backdrop-filter: blur(10px);
      z-index: 1000;
      padding: 1rem 0;
      transition: all 0.3s ease;
      transform: translateY(-100%);
      animation: slideInFromTop 0.8s ease-out 0.2s forwards;
    }

    @keyframes slideInFromTop {
      to {
        transform: translateY(0);
      }
    }

    .nav-container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 2rem;
    }

    .logo {
      font-size: 1.8rem;
      font-weight: bold;
      color: #ffffff;
      text-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
      opacity: 0;
      animation: fadeInLeft 0.8s ease-out 0.5s forwards;
    }

    @keyframes fadeInLeft {
      from {
        opacity: 0;
        transform: translateX(-30px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    .nav-links {
      display: flex;
      list-style: none;
      gap: 2rem;
      opacity: 0;
      animation: fadeInRight 0.8s ease-out 0.7s forwards;
    }

    @keyframes fadeInRight {
      from {
        opacity: 0;
        transform: translateX(30px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      transition: all 0.3s ease;
      font-weight: 500;
      position: relative;
      padding: 0.5rem 0;
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 2px;
      background: #ffffff;
      transition: width 0.3s ease;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-links a:hover {
      color: #ffffff;
      text-shadow: 0 0 8px rgba(255, 255, 255, 0.6);
    }

    /* Sections */
    .section {
      position: relative;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 2rem;
      opacity: 0;
      transform: translateY(50px);
      transition: all 0.8s ease-out;
    }

    .section.animate-in {
      opacity: 1;
      transform: translateY(0);
    }

    .hero {
      background: rgba(255, 255, 255, 0.1);
      text-align: center;
      color: white;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translate(0, 0) rotate(0deg); }
      50% { transform: translate(-20px, -10px) rotate(180deg); }
    }

    .hero-content {
      position: relative;
      z-index: 2;
    }

    .hero h1 {
      font-size: 4rem;
      margin-bottom: 1rem;
      text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
      background: linear-gradient(45deg, #ffffff, #e0f7fa, #ffffff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: titleGlow 3s ease-in-out infinite alternate;
      opacity: 0;
      transform: translateY(30px);
      animation: fadeInUp 1s ease-out 0.5s forwards, titleGlow 3s ease-in-out 1.5s infinite alternate;
    }

    @keyframes titleGlow {
      from { filter: drop-shadow(0 0 5px rgba(255, 255, 255, 0.3)); }
      to { filter: drop-shadow(0 0 15px rgba(255, 255, 255, 0.6)); }
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .hero p {
      font-size: 1.5rem;
      margin-bottom: 3rem;
      max-width: 600px;
      text-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      opacity: 0;
      transform: translateY(30px);
      animation: fadeInUp 1s ease-out 0.8s forwards;
    }

    .btn {
      display: inline-block;
      background: linear-gradient(45deg, #ffffff, #e0f7fa);
      color: #28757b;
      text-decoration: none;
      padding: 1rem 2.5rem;
      border-radius: 50px;
      font-size: 1.2rem;
      font-weight: bold;
      transition: all 0.4s ease;
      box-shadow: 0 10px 30px rgba(255, 255, 255, 0.2);
      border: none;
      cursor: pointer;
      opacity: 0;
      transform: translateY(30px) scale(0.9);
      animation: btnFadeIn 1s ease-out 1.1s forwards;
      position: relative;
      overflow: hidden;
    }

    @keyframes btnFadeIn {
      to {
        opacity: 1;
        transform: translateY(0) scale(1);
      }
    }

    .btn::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
      transition: left 0.6s;
    }

    .btn:hover::before {
      left: 100%;
    }

    .btn:hover {
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0 15px 40px rgba(255, 255, 255, 0.4);
      background: linear-gradient(45deg, #e0f7fa, #ffffff);
    }

    .content-section {
      background: rgba(255, 255, 255, 0.95);
      backdrop-filter: blur(10px);
      border-radius: 20px;
      padding: 4rem;
      margin: 2rem;
      max-width: 1200px;
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
      transform: translateY(50px);
      opacity: 0;
      transition: all 0.8s ease-out;
    }

    .content-section.animate-in {
      transform: translateY(0);
      opacity: 1;
    }

    .section-title {
      font-size: 3rem;
      text-align: center;
      margin-bottom: 3rem;
      color: #28757b;
      position: relative;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease-out 0.2s;
    }

    .content-section.animate-in .section-title {
      opacity: 1;
      transform: translateY(0);
    }

    .section-title::after {
      content: '';
      display: block;
      width: 100px;
      height: 4px;
      background: linear-gradient(45deg, #28757b, #1e5b61);
      margin: 1rem auto;
      border-radius: 2px;
      transform: scaleX(0);
      transition: transform 0.6s ease-out 0.4s;
    }

    .content-section.animate-in .section-title::after {
      transform: scaleX(1);
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin-top: 3rem;
    }

    .service-card {
      background: white;
      padding: 2rem;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
      transition: all 0.4s ease;
      border: 2px solid transparent;
      opacity: 0;
      transform: translateY(30px) rotateX(15deg);
      transition: all 0.6s ease-out;
    }

    .content-section.animate-in .service-card {
      opacity: 1;
      transform: translateY(0) rotateX(0deg);
    }

    .content-section.animate-in .service-card:nth-child(1) { transition-delay: 0.1s; }
    .content-section.animate-in .service-card:nth-child(2) { transition-delay: 0.2s; }
    .content-section.animate-in .service-card:nth-child(3) { transition-delay: 0.3s; }
    .content-section.animate-in .service-card:nth-child(4) { transition-delay: 0.4s; }
    .content-section.animate-in .service-card:nth-child(5) { transition-delay: 0.5s; }
    .content-section.animate-in .service-card:nth-child(6) { transition-delay: 0.6s; }

    .service-card:hover {
      transform: translateY(-5px) scale(1.02);
      border-color: #28757b;
      box-shadow: 0 20px 40px rgba(40, 117, 123, 0.2);
    }

    .service-icon {
      width: 80px;
      height: 80px;
      background: linear-gradient(45deg, #28757b, #1e5b61);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 1rem;
      font-size: 2rem;
      color: white;
      transition: all 0.3s ease;
    }

    .service-card:hover .service-icon {
      transform: rotateY(360deg);
    }

    .contact-form {
      display: grid;
      gap: 1rem;
      max-width: 600px;
      margin: 0 auto;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      opacity: 0;
      transform: translateX(-30px);
      transition: all 0.6s ease-out;
    }

    .content-section.animate-in .form-group {
      opacity: 1;
      transform: translateX(0);
    }

    .content-section.animate-in .form-group:nth-child(1) { transition-delay: 0.1s; }
    .content-section.animate-in .form-group:nth-child(2) { transition-delay: 0.2s; }
    .content-section.animate-in .form-group:nth-child(3) { transition-delay: 0.3s; }
    .content-section.animate-in .form-group:nth-child(4) { transition-delay: 0.4s; }
    .content-section.animate-in .form-group:nth-child(5) { transition-delay: 0.5s; }

    .form-group label {
      margin-bottom: 0.5rem;
      font-weight: bold;
      color: #28757b;
    }

    .form-group input,
    .form-group textarea {
      padding: 1rem;
      border: 2px solid #e1e1e1;
      border-radius: 10px;
      font-size: 1rem;
      transition: all 0.3s ease;
    }

    .form-group input:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: #28757b;
      box-shadow: 0 0 10px rgba(40, 117, 123, 0.2);
      transform: scale(1.02);
    }

    .stats-container {
      display: flex;
      gap: 2rem;
      margin-top: 2rem;
      justify-content: center;
    }

    .stat-item {
      text-align: center;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease-out;
    }

    .content-section.animate-in .stat-item {
      opacity: 1;
      transform: translateY(0);
    }

    .content-section.animate-in .stat-item:nth-child(1) { transition-delay: 0.2s; }
    .content-section.animate-in .stat-item:nth-child(2) { transition-delay: 0.4s; }
    .content-section.animate-in .stat-item:nth-child(3) { transition-delay: 0.6s; }

    .stat-number {
      font-size: 2rem;
      font-weight: bold;
      color: #28757b;
      margin-bottom: 0.5rem;
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: center;
    }

    .about-text {
      opacity: 0;
      transform: translateX(-50px);
      transition: all 0.8s ease-out;
    }

    .about-image {
      opacity: 0;
      transform: translateX(50px);
      transition: all 0.8s ease-out 0.3s;
    }

    .content-section.animate-in .about-text,
    .content-section.animate-in .about-image {
      opacity: 1;
      transform: translateX(0);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 4rem;
      align-items: start;
    }

    .contact-info {
      opacity: 0;
      transform: translateX(-30px);
      transition: all 0.8s ease-out;
    }

    .contact-form-container {
      opacity: 0;
      transform: translateX(30px);
      transition: all 0.8s ease-out 0.3s;
    }

    .content-section.animate-in .contact-info,
    .content-section.animate-in .contact-form-container {
      opacity: 1;
      transform: translateX(0);
    }

    /* Responsive Design */
    @media (max-width: 768px) {
      .nav-links {
        display: none;
      }

      .hero h1 {
        font-size: 2.5rem;
      }

      .hero p {
        font-size: 1.2rem;
      }

      .content-section {
        padding: 2rem;
        margin: 1rem;
      }

      .section-title {
        font-size: 2rem;
      }

      .about-grid,
      .contact-grid {
        grid-template-columns: 1fr;
        gap: 2rem;
      }

      .stats-container {
        flex-direction: column;
        gap: 1rem;
      }
    }

    /* Smooth scrolling */
    html {
      scroll-behavior: smooth;
    }

    /* Scroll indicator */
    .scroll-indicator {
      position: fixed;
      top: 0;
      left: 0;
      width: 0%;
      height: 3px;
      background: linear-gradient(90deg, #ffffff, #e0f7fa);
      z-index: 1001;
      transition: width 0.1s ease;
    }
  </style>
</head>
<body>
  <div class="scroll-indicator"></div>
  
  <nav>
    <div class="nav-container">
      <div class="logo">ChatBot Pro</div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="section hero animate-in">
    <div class="hero-content">
      <h1>ChatBot Pro</h1>
      <p>Revolutionize your customer service with AI-powered chatbots that understand, learn, and deliver exceptional experiences 24/7</p>
      <a href="#services" class="btn">Explore Our Solutions</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="section">
    <div class="content-section">
      <h2 class="section-title">About Us</h2>
      <div class="about-grid">
        <div class="about-text">
          <h3 style="font-size: 1.8rem; color: #28757b; margin-bottom: 1rem;">Leading AI Innovation</h3>
          <p style="font-size: 1.1rem; margin-bottom: 1.5rem;">
            ChatBot Pro is at the forefront of artificial intelligence and customer service automation. We specialize in creating intelligent conversational agents that transform how businesses interact with their customers.
          </p>
          <p style="font-size: 1.1rem; margin-bottom: 1.5rem;">
            Our team of expert developers and AI specialists work tirelessly to deliver cutting-edge chatbot solutions that not only answer questions but truly understand context, emotion, and intent.
          </p>
          <div class="stats-container">
            <div class="stat-item">
              <div class="stat-number">500+</div>
              <div>Happy Clients</div>
            </div>
            <div class="stat-item">
              <div class="stat-number">1M+</div>
              <div>Conversations</div>
            </div>
            <div class="stat-item">
              <div class="stat-number">99.9%</div>
              <div>Uptime</div>
            </div>
          </div>
        </div>
        <div class="about-image">
          <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a0ccd86f-ba9e-4399-8811-2f88bb702c86.png" alt="Modern office environment with developers working on AI chatbot technology, multiple computer screens showing code and chat interfaces, collaborative workspace with futuristic lighting" style="width: 100%; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.2);">
        </div>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="section">
    <div class="content-section">
      <h2 class="section-title">Our Services</h2>
      <div class="services-grid">
        <div class="service-card">
          <div class="service-icon">🤖</div>
          <h3 style="text-align: center; margin-bottom: 1rem; color: #28757b;">Custom Chatbot Development</h3>
          <p>Tailored AI chatbots designed specifically for your business needs, industry requirements, and brand voice. From simple FAQ bots to complex conversational AI.</p>
        </div>
        <div class="service-card">
          <div class="service-icon">💬</div>
          <h3 style="text-align: center; margin-bottom: 1rem; color: #28757b;">24/7 Customer Support</h3>
          <p>Never miss a customer inquiry. Our AI-powered chatbots provide instant, accurate responses around the clock, improving customer satisfaction and reducing response times.</p>
        </div>
        <div class="service-card">
          <div class="service-icon">⚡</div>
          <h3 style="text-align: center; margin-bottom: 1rem; color: #28757b;">Integration Services</h3>
          <p>Seamlessly integrate chatbots with your existing systems, CRM, databases, and platforms. Compatible with websites, mobile apps, and social media channels.</p>
        </div>
        <div class="service-card">
          <div class="service-icon">📊</div>
          <h3 style="text-align: center; margin-bottom: 1rem; color: #28757b;">Analytics & Insights</h3>
          <p>Gain valuable insights into customer behavior, frequently asked questions, and conversation patterns with our comprehensive analytics dashboard.</p>
        </div>
        <div class="service-card">
          <div class="service-icon">🛠️</div>
          <h3 style="text-align: center; margin-bottom: 1rem; color: #28757b;">Maintenance & Updates</h3>
          <p>Continuous improvement and maintenance services to keep your chatbot performing optimally, with regular updates and feature enhancements.</p>
        </div>
        <div class="service-card">
          <div class="service-icon">🎯</div>
          <h3 style="text-align: center; margin-bottom: 1rem; color: #28757b;">Lead Generation</h3>
          <p>Convert visitors into leads with intelligent chatbots that qualify prospects, schedule appointments, and guide users through your sales funnel.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="section">
    <div class="content-section">
      <h2 class="section-title">Get In Touch</h2>
      <div class="contact-grid">
        <div class="contact-info">
          <h3 style="font-size: 1.8rem; color: #28757b; margin-bottom: 1rem;">Ready to Transform Your Customer Service?</h3>
          <p style="font-size: 1.1rem; margin-bottom: 2rem;">
            Let's discuss how our AI chatbot solutions can revolutionize your customer interactions and boost your business growth.
          </p>
          <div style="margin-bottom: 1.5rem;">
            <strong style="color: #28757b;">📍 Address:</strong><br>
            123 AI Technology Drive<br>
            Innovation District, Tech City 12345
          </div>
          <div style="margin-bottom: 1.5rem;">
            <strong style="color: #28757b;">📧 Email:</strong><br>
            hello@chatbotpro.com
          </div>
          <div style="margin-bottom: 1.5rem;">
            <strong style="color: #28757b;">📞 Phone:</strong><br>
            +1 (555) 123-CHAT
          </div>
          <div>
            <strong style="color: #28757b;">⏰ Business Hours:</strong><br>
            Monday - Friday: 9:00 AM - 6:00 PM<br>
            Weekend: Emergency support available
          </div>
        </div>
        <div class="contact-form-container">
          <form class="contact-form" onsubmit="handleSubmit(event)">
            <div class="form-group">
              <label for="name">Name</label>
              <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
              <label for="email">Email</label>
              <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
              <label for="company">Company</label>
              <input type="text" id="company" name="company">
            </div>
            <div class="form-group">
              <label for="message">Message</label>
              <textarea id="message" name="message" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn" style="background: linear-gradient(45deg, #28757b, #1e5b61); color: white;">Send Message</button>
          </form>
        </div>
      </div>
    </div>
  </section>

  <script>
    // Scroll animation observer
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('animate-in');
        }
      });
    }, observerOptions);

    // Observe all sections and content sections
    document.querySelectorAll('.section, .content-section').forEach(section => {
      observer.observe(section);
    });

    // Scroll progress indicator
    function updateScrollIndicator() {
      const scrollTop = window.pageYOffset;
      const docHeight = document.documentElement.scrollHeight - window.innerHeight;
      const scrollPercent = (scrollTop / docHeight) * 100;
      document.querySelector('.scroll-indicator').style.width = scrollPercent + '%';
    }

    window.addEventListener('scroll', updateScrollIndicator);

    // Contact form handler
    function handleSubmit(event) {
      event.preventDefault();
      const formData = new FormData(event.target);
      const data = Object.fromEntries(formData);
      
      // Simulate form submission with animation
      const submitBtn = event.target.querySelector('button[type="submit"]');
      const originalText = submitBtn.textContent;
      
      submitBtn.textContent = 'Sending...';
      submitBtn.style.background = 'linear-gradient(45deg, #4caf50, #45a049)';
      
      setTimeout(() => {
        alert(`Thank you ${data.name}! We'll get back to you soon at ${data.email}`);
        submitBtn.textContent = originalText;
        submitBtn.style.background = 'linear-gradient(45deg, #28757b, #1e5b61)';
        event.target.reset();
      }, 1500);
    }

    // Smooth scroll for navigation links
    document.querySelectorAll('.nav-links a').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const targetId = this.getAttribute('href');
        const targetSection = document.querySelector(targetId);
        
        // Add smooth scroll animation
        targetSection.scrollIntoView({ 
          behavior: 'smooth',
          block: 'start'
        });
        
        // Add active state to nav link
        document.querySelectorAll('.nav-links a').forEach(link => {
          link.style.fontWeight = '500';
        });
        this.style.fontWeight = 'bold';
      });
    });

    // Add parallax effect to hero section
    window.addEventListener('scroll', () => {
      const scrolled = window.pageYOffset;
      const hero = document.querySelector('.hero');
      const rate = scrolled * -0.5;
      
      if (hero) {
        hero.style.transform = `translateY(${rate}px)`;
      }
    });

    // Add counter animation for stats
    function animateCounter(element, target) {
      const duration = 2000;
      const start = performance.now();
      const startValue = 0;
      
      function update(currentTime) {
        const elapsed = currentTime - start;
        const progress = Math.min(elapsed / duration, 1);
        
        const current = startValue + (target - startValue) * progress;
        
        if (target >= 1000000) {
          element.textContent = (current / 1000000).toFixed(1) + 'M+';
        } else if (target >= 1000) {
          element.textContent = Math.floor(current) + '+';
        } else {
          element.textContent = current.toFixed(1) + '%';
        }
        
        if (progress < 1) {
          requestAnimationFrame(update);
        }
      }
      
      requestAnimationFrame(update);
    }

    // Animate stats when they come into view
    const statsObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const statNumbers = entry.target.querySelectorAll('.stat-number');
          const targets = [500, 1000000, 99.9];
          
          statNumbers.forEach((stat, index) => {
            setTimeout(() => {
              animateCounter(stat, targets[index]);
            }, index * 200);
          });
          
          statsObserver.unobserve(entry.target);
        }
      });
    });

    const aboutSection = document.querySelector('#about .content-section');
    if (aboutSection) {
      statsObserver.observe(aboutSection);
    }
  </script>
</body>
</html>

