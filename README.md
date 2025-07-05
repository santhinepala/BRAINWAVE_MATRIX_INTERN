<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LearnAI - AI Learning Platform</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', sans-serif;
      line-height: 1.6;
      background: #f9f9f9;
      color: #333;
    }

    .container {
      width: 90%;
      max-width: 1100px;
      margin: auto;
    }

    header {
      background: #111;
      color: #fff;
      padding: 20px 0;
    }

    .nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 24px;
    }

    .logo span {
      color: #00d8a7;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
    }

    nav ul li a {
      color: #fff;
      text-decoration: none;
    }

    .hero {
      background: linear-gradient(to right, #00d8a7, #007bff);
      color: #fff;
      padding: 100px 0;
      text-align: center;
    }

    .hero h2 {
      font-size: 40px;
      margin-bottom: 10px;
    }

    .hero .btn {
      background: #fff;
      color: #007bff;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 30px;
      font-weight: bold;
      transition: 0.3s;
    }

    .hero .btn:hover {
      background: #eee;
    }

    .features {
      padding: 60px 0;
      background: #fff;
      text-align: center;
    }

    .features h2 {
      margin-bottom: 30px;
    }

    .feature-box {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }

    .feature {
      flex: 1;
      margin: 20px;
      max-width: 300px;
      background: #f2f2f2;
      padding: 20px;
      border-radius: 10px;
    }

    .about {
      padding: 60px 0;
      background: #f0f0f0;
      text-align: center;
    }

    .cta {
      padding: 60px 0;
      background: #007bff;
      color: white;
      text-align: center;
    }

    .cta input {
      padding: 10px;
      width: 250px;
      border: none;
      border-radius: 5px;
      margin-right: 10px;
    }

    .cta button {
      padding: 10px 20px;
      background: #00d8a7;
      border: none;
      border-radius: 5px;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }

    footer {
      text-align: center;
      padding: 20px;
      background: #111;
      color: white;
    }

    @media (max-width: 768px) {
      .feature-box {
        flex-direction: column;
        align-items: center;
      }
      nav ul {
        flex-direction: column;
        gap: 10px;
        margin-top: 10px;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <header>
    <div class="container nav">
      <h1 class="logo">Learn<span>AI</span></h1>
      <nav>
        <ul>
          <li><a href="#features">Features</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#cta">Join</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <div class="container">
      <h2>Master AI Skills from Experts</h2>
      <p>Learn Machine Learning, Deep Learning, and Data Science from industry professionals.</p>
      <a href="#cta" class="btn">Get Started</a>
    </div>
  </section>

  <!-- Features Section -->
  <section class="features" id="features">
    <div class="container">
      <h2>Why Choose LearnAI?</h2>
      <div class="feature-box">
        <div class="feature">
          <h3>👨‍🏫 Expert Mentors</h3>
          <p>Courses taught by Google, Meta, and OpenAI professionals.</p>
        </div>
        <div class="feature">
          <h3>📚 Real-World Projects</h3>
          <p>Hands-on projects for real industry experience.</p>
        </div>
        <div class="feature">
          <h3>📈 Career Growth</h3>
          <p>Get certified and boost your job prospects globally.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section class="about" id="about">
    <div class="container">
      <h2>About Us</h2>
      <p>LearnAI is an education platform that helps students, professionals, and AI enthusiasts to build a successful career in Artificial Intelligence and related fields. Join 100,000+ learners today!</p>
    </div>
  </section>

  <!-- Call to Action -->
  <section class="cta" id="cta">
    <div class="container">
      <h2>Join the AI Revolution</h2>
      <form id="signup-form">
        <input type="email" placeholder="Enter your email" required />
        <button type="submit">Subscribe</button>
      </form>
    </div>
  </section>

  <footer>
    <p>&copy; 2025 LearnAI. All rights reserved.</p>
  </footer>

  <script>
    document.getElementById("signup-form").addEventListener("submit", function (e) {
      e.preventDefault();
      const email = this.querySelector("input").value;
      if (email) {
        alert("Thanks for subscribing! We'll send updates to " + email);
        this.reset();
      }
    });
  </script>
</body>
</html>
