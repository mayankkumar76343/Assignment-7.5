Assignment 7.5 — Flexbox Mini-Project1. Project structure
Create a folder named Assignment-7.5 with these files:

Assignment-7.5/

index.html

style.css

2. HTML file — index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flexi - Flexbox Mini Project</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- Navigation Bar -->
  <header class="navbar">
    <a href="#home" class="logo">Flexi.</a>

    <nav class="nav-links" aria-label="Main navigation">
      <a href="#home">Home</a>
      <a href="#features">Features</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>

    <a href="#get-started" class="btn nav-btn">Get Started</a>
  </header>

  <main>
    <!-- Hero Section -->
    <section class="hero" id="home">
      <div class="hero-content">
        <span class="tagline">WELCOME TO FLEXI</span>
        <h1>Build Something <span>Amazing.</span></h1>
        <p>
          Turn your ideas into reality with simple, smart,
          and modern digital solutions. Start building your
          future today.
        </p>

        <div class="hero-buttons">
          <a href="#get-started" class="btn">Get Started →</a>
          <a href="#features" class="btn btn-outline">
            Explore Features
          </a>
        </div>
      </div>

      <div class="hero-visual">
        <div class="visual-card">
          <div class="visual-icon">🚀</div>
          <h2>Dream Big. Build Better.</h2>
          <p>Your next great idea starts here.</p>
          <div class="progress">
            <span></span>
          </div>
          <small>Innovation in progress...</small>
        </div>
        <div class="floating-badge">✨ Think Different</div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
      <div class="section-heading">
        <span class="tagline">OUR FEATURES</span>
        <h2>Everything You Need</h2>
        <p>Powerful features to help you work smarter.</p>
      </div>

      <div class="feature-container">
        <article class="feature-card">
          <div class="feature-icon purple">⚡</div>
          <h3>Fast Performance</h3>
          <p>
            Enjoy a smooth and efficient experience
            designed to save your valuable time.
          </p>
        </article>

        <article class="feature-card">
          <div class="feature-icon blue">🎨</div>
          <h3>Modern Design</h3>
          <p>
            Clean layouts and beautiful visuals
            make every interaction enjoyable.
          </p>
        </article>

        <article class="feature-card">
          <div class="feature-icon green">📱</div>
          <h3>Fully Responsive</h3>
          <p>
            Access your experience on mobile,
            tablet, and desktop devices.
          </p>
        </article>
      </div>
    </section>

    <!-- Call-to-Action Section -->
    <section class="cta" id="get-started">
      <h2>Ready to Get Started?</h2>
      <p>
        Take the first step toward building something great.
      </p>
      <a href="mailto:hello@example.com" class="btn cta-btn">
        Let's Get Started →
      </a>
    </section>
  </main>

  <!-- Footer -->
  <footer class="footer" id="contact">
    <a href="#home" class="logo footer-logo">Flexi.</a>
    <p>Creating better digital experiences.</p>
    <p class="copyright">
      &copy; 2026 Flexi. All rights reserved.
    </p>
  </footer>

</body>
</html>
3. CSS file — style.css

css

/* General Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  color: #1e293b;
  background: #f8fafc;
  line-height: 1.6;
}

a {
  text-decoration: none;
}

:root {
  --primary: #6c4cf1;
  --primary-dark: #5135d5;
  --text: #1e293b;
  --muted: #64748b;
  --white: #ffffff;
}

/* Navigation Bar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  padding: 20px 8%;
  background: var(--white);
  box-shadow: 0 2px 12px rgba(15, 23, 42, 0.05);
}

.logo {
  color: var(--primary);
  font-size: 28px;
  font-weight: 800;
}

.nav-links {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 28px;
}

.nav-links a {
  color: var(--text);
  font-size: 15px;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: var(--primary);
}

/* Buttons */
.btn {
  display: inline-block;
  padding: 12px 24px;
  background: var(--primary);
  color: var(--white);
  border: 2px solid var(--primary);
  border-radius: 8px;
  font-size: 15px;
  font-weight: 700;
  text-align: center;
  transition: 0.3s ease;
}

.btn:hover {
  background: var(--primary-dark);
  border-color: var(--primary-dark);
  transform: translateY(-2px);
}

.btn-outline {
  color: var(--primary);
  background: transparent;
}

.btn-outline:hover {
  color: var(--white);
}

/* Hero Section */
.hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 50px;
  padding: 90px 8%;
  min-height: 520px;
  background: linear-gradient(135deg, #f5f3ff, #eff6ff);
}

.hero-content {
  flex: 1 1 320px;
  min-width: 0;
}

.tagline {
  display: inline-block;
  margin-bottom: 16px;
  color: var(--primary);
  font-size: 13px;
  font-weight: 800;
  letter-spacing: 2px;
}

.hero h1 {
  margin-bottom: 22px;
  color: var(--text);
  font-size: clamp(36px, 5vw, 58px);
  line-height: 1.15;
  overflow-wrap: anywhere;
}

.hero h1 span {
  color: var(--primary);
}

.hero-content > p {
  max-width: 520px;
  margin-bottom: 28px;
  color: var(--muted);
  font-size: 17px;
}

.hero-buttons {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 14px;
}

/* Hero Illustration */
.hero-visual {
  position: relative;
  display: flex;
  flex: 1 1 300px;
  justify-content: center;
  align-items: center;
  min-width: 0;
  padding: 20px 0;
}

.visual-card {
  width: 100%;
  max-width: 390px;
  padding: 40px 28px;
  text-align: center;
  background: var(--white);
  border: 1px solid #e2e8f0;
  border-radius: 24px;
  box-shadow: 0 24px 60px rgba(108, 76, 241, 0.13);
}

.visual-icon {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 100px;
  height: 100px;
  margin-bottom: 24px;
  background: #ede9fe;
  border-radius: 24px;
  font-size: 48px;
}

.visual-card h2 {
  margin-bottom: 10px;
  font-size: 22px;
}

.visual-card p,
.visual-card small {
  color: var(--muted);
}

.progress {
  height: 8px;
  margin: 24px 0 12px;
  overflow: hidden;
  background: #e2e8f0;
  border-radius: 10px;
}

.progress span {
  display: block;
  width: 75%;
  height: 100%;
  background: var(--primary);
  border-radius: 10px;
}

.floating-badge {
  position: absolute;
  right: 0;
  bottom: 0;
  padding: 12px 18px;
  background: var(--white);
  border-radius: 12px;
  box-shadow: 0 8px 25px rgba(15, 23, 42, 0.1);
  font-size: 14px;
  font-weight: 700;
}

/* Features Section */
.features {
  padding: 85px 8%;
}

.section-heading {
  margin-bottom: 45px;
  text-align: center;
}

.section-heading h2 {
  margin-bottom: 10px;
  font-size: clamp(28px, 4vw, 40px);
}

.section-heading p {
  color: var(--muted);
}

.feature-container {
  display: flex;
  justify-content: center;
  align-items: stretch;
  flex-wrap: wrap;
  gap: 25px;
}

.feature-card {
  flex: 1 1 250px;
  min-width: 0;
  padding: 32px 26px;
  background: var(--white);
  border: 1px solid #e2e8f0;
  border-radius: 16px;
  box-shadow: 0 8px 25px rgba(15, 23, 42, 0.04);
  transition: transform 0.3s, box-shadow 0.3s;
}

.feature-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px rgba(15, 23, 42, 0.08);
}

.feature-icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 58px;
  height: 58px;
  margin-bottom: 22px;
  border-radius: 14px;
  font-size: 27px;
}

.purple {
  background: #ede9fe;
}

.blue {
  background: #dbeafe;
}

.green {
  background: #dcfce7;
}

.feature-card h3 {
  margin-bottom: 12px;
  font-size: 21px;
}

.feature-card p {
  color: var(--muted);
  font-size: 15px;
}

/* Call-to-Action Section */
.cta {
  margin: 20px 8% 80px;
  padding: 60px 25px;
  text-align: center;
  color: var(--white);
  background: linear-gradient(135deg, #6c4cf1, #4338ca);
  border-radius: 22px;
}

.cta h2 {
  margin-bottom: 12px;
  font-size: clamp(28px, 4vw, 38px);
}

.cta p {
  margin-bottom: 25px;
  color: #ede9fe;
}

.cta-btn {
  color: var(--primary);
  background: var(--white);
  border-color: var(--white);
}

.cta-btn:hover {
  color: var(--white);
}

/* Footer */
.footer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 12px;
  padding: 40px 8%;
  text-align: center;
  background: #0f172a;
  color: var(--white);
}

.footer-logo {
  color: var(--white);
}

.footer > p {
  color: #cbd5e1;
}

.copyright {
  padding-top: 15px;
  border-top: 1px solid #334155;
  width: 100%;
  font-size: 14px;
}

/* Responsive Design */
@media (max-width: 768px) {
  .navbar {
    justify-content: center;
    padding: 20px 5%;
  }

  .nav-links {
    order: 3;
    width: 100%;
    gap: 18px;
  }

  .hero {
    justify-content: center;
    text-align: center;
    padding: 60px 6%;
    gap: 35px;
  }

  .hero-content {
    flex-basis: 100%;
  }

  .hero-content > p {
    margin-right: auto;
    margin-left: auto;
  }

  .hero-buttons {
    justify-content: center;
  }

  .hero-visual {
    flex-basis: 100%;
  }

  .floating-badge {
    right: 2%;
  }

  .features {
    padding: 65px 6%;
  }

  .feature-card {
    flex-basis: 280px;
  }

  .cta {
    margin-right: 6%;
    margin-left: 6%;
  }
}

@media (max-width: 420px) {
  .nav-links {
    gap: 12px;
  }

  .nav-links a {
    font-size: 14px;
  }

  .nav-btn {
    padding: 10px 16px;
  }

  .hero-buttons {
    flex-direction: column;
    align-items: stretch;
  }

  .visual-card {
    padding: 30px 18px;
  }

  .floating-badge {
    right: -4px;
    font-size: 12px;
  }

  .cta {
    padding: 45px 18px;
  }
}