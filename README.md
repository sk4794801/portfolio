<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Siddhant Kumar | Portfolio</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <!-- Font Awesome (for icons) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <style>
    /* Reset + Base */
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Poppins', sans-serif;
      background: #0d1b2a;
      color: #ffffff;
      line-height: 1.6;
    }
    a { text-decoration: none; color: inherit; transition: 0.3s; }
    ul { list-style: none; }

    /* Navbar */
    header {
      position: fixed;
      top: 0; left: 0; width: 100%;
      background: #0d1b2a;
      padding: 15px 60px;
      display: flex; justify-content: space-between; align-items: center;
      z-index: 1000;
      box-shadow: 0 2px 10px rgba(0,0,0,0.5);
    }
    header h1 { font-size: 20px; font-weight: 600; color: #00b4d8; }
    header nav ul { display: flex; gap: 25px; }
    header nav ul li a { color: #fff; font-weight: 400; }
    header nav ul li a:hover { color: #00b4d8; }

    /* Hero */
    .hero {
      min-height: 100vh;
      display: flex; justify-content: space-between; align-items: center;
      padding: 100px 60px 60px;
      gap: 40px;
      flex-wrap: wrap;
    }
    .hero-text { max-width: 600px; }
    .hero-text h2 { font-size: 50px; font-weight: 700; }
    .hero-text h2 span { color: #00b4d8; }
    .hero-text h3 { font-size: 22px; margin-top: 10px; color: #e0e1dd; }
    .hero-text p { margin: 20px 0; }
    .btn { display: inline-block; padding: 10px 20px; border-radius: 6px; margin-right: 10px; font-weight: 500; }
    .btn-primary { background: #00b4d8; color: #fff; }
    .btn-outline { border: 2px solid #00b4d8; color: #00b4d8; }
    .btn:hover { opacity: 0.85; }

    /* Animated Profile Photo */
    .hero img {
      width: 320px;
      border-radius: 50%;
      border: 4px solid #00b4d8;
      box-shadow: 0 0 25px rgba(0,180,216,0.6);
      animation: glow 3s infinite ease-in-out;
    }
    @keyframes glow {
      0% { box-shadow: 0 0 15px rgba(0,180,216,0.4); }
      50% { box-shadow: 0 0 40px rgba(0,180,216,0.8); }
      100% { box-shadow: 0 0 15px rgba(0,180,216,0.4); }
    }

    /* Social Icons */
    .social-icons { margin-top: 20px; }
    .social-icons a {
      display: inline-block;
      margin-right: 15px;
      font-size: 26px;
      color: #00b4d8;
      transition: transform 0.3s, color 0.3s;
    }
    .social-icons a:hover { color: #0096c7; transform: scale(1.2); }

    /* Section */
    section { padding: 80px 60px; }
    h2.section-title {
      font-size: 32px; margin-bottom: 30px;
      color: #00b4d8; text-align: center; font-weight: 600;
    }

    /* About */
    .about { text-align: center; }
    .about img {
      width: 180px;
      border-radius: 50%;
      border: 4px solid #00b4d8;
      margin-bottom: 20px;
      box-shadow: 0 0 15px rgba(0,180,216,0.5);
      animation: glow 3s infinite ease-in-out;
    }
    .about p { max-width: 700px; margin: 0 auto; color: #e0e1dd; }

    /* Journey */
    .journey {
      display: flex; justify-content: space-around; gap: 40px; flex-wrap: wrap;
    }
    .journey-card {
      background: #1b263b; padding: 20px; border-radius: 10px; width: 45%;
      border-left: 4px solid #00b4d8;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .journey-card:hover { transform: translateY(-5px); box-shadow: 0 8px 20px rgba(0,180,216,0.3); }
    .journey-card h3 { margin-bottom: 5px; color: #00b4d8; }
    .journey-card small { display: block; margin-bottom: 10px; font-size: 13px; color: #adb5bd; }

    /* Skills */
    .skills { display: flex; justify-content: space-around; gap: 40px; flex-wrap: wrap; }
    .skill-box { width: 45%; }
    .skill-box h3 { margin-bottom: 15px; color: #00b4d8; }
    .bar { background: #1b263b; border-radius: 6px; margin: 10px 0; overflow: hidden; height: 10px; }
    .bar span { display: block; height: 100%; background: #00b4d8; transition: width 1s ease-in-out; }

    /* Contact */
    .contact-form {
      max-width: 700px; margin: auto; background: #1b263b;
      padding: 30px; border-radius: 10px; box-shadow: 0 8px 20px rgba(0,0,0,0.4);
    }
    .contact-form input, .contact-form textarea {
      width: 100%; padding: 12px; margin: 10px 0;
      border: none; outline: none; border-radius: 6px; font-size: 14px;
    }
    .contact-form textarea { resize: none; }
    .contact-form button {
      background: #00b4d8; color: #fff; padding: 12px 20px;
      border: none; border-radius: 6px; cursor: pointer; font-weight: 600;
    }
    .contact-form button:hover { background: #0096c7; }

    /* Footer */
    footer {
      background: #0d1b2a; text-align: center;
      padding: 20px; font-size: 14px; margin-top: 30px;
      border-top: 1px solid #1b263b; color: #adb5bd;
    }

    /* Scroll-to-top */
    #topBtn {
      position: fixed; bottom: 20px; right: 20px;
      background: #00b4d8; color: #fff; border: none;
      border-radius: 50%; width: 40px; height: 40px;
      cursor: pointer; font-size: 18px; display: none;
      transition: background 0.3s;
    }
    #topBtn:hover { background: #0096c7; }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <h1>My Portfolio</h1>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#journey">Education</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero -->
  <section class="hero" id="hero">
    <div class="hero-text">
      <h2>Hi, I'm <span>Siddhant Kumar</span></h2>
      <h3>Web Developer</h3>
      <p>I love building websites as a Web Developer and am keenly exploring Cybersecurity to ensure my applications are both functional and secure.</p>
      <a href="#contact" class="btn btn-primary">Hire Me</a>
      <a href="#contact" class="btn btn-outline">Let's Talk</a>

      <!-- Social Media -->
      <div class="social-icons">
        <a href="https://github.com/yourusername" target="_blank"><i class="fab fa-github"></i></a>
        <a href="www.linkedin.com/in/ustadsiddhu" target="_blank"><i class="fab fa-linkedin"></i></a>
        <a href="https://twitter.com/yourusername" target="_blank"><i class="fab fa-twitter"></i></a>
      </div>
    </div>
    <img src="Siddhu.jpg" alt="Siddhant Kumar">
  </section>

  <!-- About -->
  <section id="about" class="about">
    <h2 class="section-title">About Me</h2>
    <img src="img.jpg" alt="Siddhant Kumar">
    <p>I specialize in turning ideas into functional and engaging web experiences. With expertise in HTML, CSS, JavaScript, and React, I create applications that balance performance and usability. I enjoy building web projects, interactive interfaces, and learning Cybersecurity practices to make my applications secure and reliable.</p>
  </section>

  <!-- Journey -->
  <section id="journey">
    <h2 class="section-title">My Journey</h2>
    <div class="journey">
      <div class="journey-card">
        <h3>Education</h3>
        <p>10th Degree – High School Parari, Sitamarhi (Bihar)</p>
        <small>2017–2018</small>
        <p>Intermediate in Science – High School Parari, Sitamarhi (Bihar)</p>
        <small>2018–2020</small>
        <p>Bachelor's Degree – Lalit Narayan Mithila University, Darbhanga (Bihar)</p>
        <small>2021–2024</small>
      </div>
      <div class="journey-card">
        <h3>Experience</h3>
        
        <p></p>
        
      </div>
    </div>
  </section>

  <!-- Skills -->
  <section id="skills">
    <h2 class="section-title">My Skills</h2>
    <div class="skills">
      <div class="skill-box">
        <h3>Coding Skills</h3>
        <p>HTML</p><div class="bar"><span style="width:90%"></span></div>
        <p>CSS</p><div class="bar"><span style="width:60%"></span></div>
        <p>JavaScript</p><div class="bar"><span style="width:60%"></span></div>
        <p>Python</p><div class="bar"><span style="width:80%"></span></div>
        <p>Java</p><div class="bar"><span style="width:60%"></span></div>
      </div>
      <div class="skill-box">
        <h3>Professional Skills</h3>
        <p>Web Design</p><div class="bar"><span style="width:85%"></span></div>
        <p>Web Development</p><div class="bar"><span style="width:80%"></span></div>
        <p>Social Media Design</p><div class="bar"><span style="width:70%"></span></div>
        
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2 class="section-title">Contact Me</h2>
    <form class="contact-form">
      <input type="text" placeholder="Full Name" required>
      <input type="email" placeholder="Email Address" required>
      <input type="text" placeholder="Mobile Number">
      <input type="text" placeholder="Subject">
      <textarea placeholder="Your Message" rows="6"></textarea>
      <button type="submit">Submit</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Siddhant Kumar | All Rights Reserved.</p>
  </footer>

  <!-- Scroll to Top -->
  <button id="topBtn">↑</button>
  <script>
    const topBtn = document.getElementById("topBtn");
    window.onscroll = () => {
      if (document.body.scrollTop > 200 || document.documentElement.scrollTop > 200) {
        topBtn.style.display = "block";
      } else {
        topBtn.style.display = "none";
      }
    };
    topBtn.onclick = () => { window.scrollTo({ top: 0, behavior: 'smooth' }); };
  </script>
</body>
</html>
