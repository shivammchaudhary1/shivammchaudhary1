<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Shivam Chaudhary - Full Stack Developer</title>
    <style>
      @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap");

      :root {
        --primary: #2563eb;
        --primary-dark: #1d4ed8;
        --secondary: #7c3aed;
        --dark: #1e293b;
        --light: #f8fafc;
        --gray: #64748b;
        --accent: #06b6d4;
        --gradient: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        --card-bg: rgba(255, 255, 255, 0.05);
      }

      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
      }

      body {
        font-family: "Poppins", sans-serif;
        background: #0f172a;
        color: #e2e8f0;
        line-height: 1.6;
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px;
      }

      .container {
        max-width: 1100px;
        margin: 0 auto;
      }

      /* Header Section */
      .header {
        text-align: center;
        padding: 2rem 0 3rem;
        position: relative;
        overflow: hidden;
      }

      .header-banner {
        border-radius: 20px;
        overflow: hidden;
        box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        margin-bottom: 2rem;
      }

      .profile-section {
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        gap: 3rem;
        margin-top: 2rem;
      }

      .profile-img {
        width: 300px;
        height: 300px;
        border-radius: 20px;
        object-fit: cover;
        border: 4px solid var(--primary);
        box-shadow: 0 10px 30px rgba(37, 99, 235, 0.3);
      }

      .profile-text {
        flex: 1;
        min-width: 300px;
        text-align: left;
      }

      h1 {
        font-size: 3.5rem;
        background: var(--gradient);
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent;
        margin-bottom: 0.5rem;
        font-weight: 700;
      }

      h2 {
        font-size: 1.8rem;
        color: var(--accent);
        margin-bottom: 1rem;
        font-weight: 600;
      }

      .tagline {
        font-size: 1.2rem;
        color: #94a3b8;
        margin-bottom: 1.5rem;
        max-width: 600px;
      }

      .badge {
        display: inline-block;
        background: var(--primary);
        color: white;
        padding: 0.3rem 0.8rem;
        border-radius: 20px;
        font-size: 0.9rem;
        margin: 0.3rem;
        font-weight: 500;
      }

      /* Cards */
      .card {
        background: var(--card-bg);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(255, 255, 255, 0.1);
        border-radius: 15px;
        padding: 1.5rem;
        margin-bottom: 2rem;
        transition:
          transform 0.3s ease,
          box-shadow 0.3s ease;
      }

      .card:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
      }

      .card-title {
        color: var(--accent);
        font-size: 1.5rem;
        margin-bottom: 1rem;
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .card-title i {
        font-size: 1.3rem;
      }

      /* Career Timeline */
      .timeline {
        position: relative;
        padding-left: 2rem;
      }

      .timeline::before {
        content: "";
        position: absolute;
        left: 7px;
        top: 0;
        bottom: 0;
        width: 2px;
        background: var(--gradient);
      }

      .timeline-item {
        position: relative;
        margin-bottom: 2rem;
        padding-left: 1.5rem;
      }

      .timeline-item::before {
        content: "";
        position: absolute;
        left: -8px;
        top: 5px;
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background: var(--primary);
        border: 3px solid var(--dark);
      }

      .timeline-title {
        color: white;
        font-size: 1.2rem;
        font-weight: 600;
      }

      .timeline-subtitle {
        color: var(--accent);
        font-size: 1rem;
        margin: 0.3rem 0;
      }

      .timeline-date {
        color: var(--gray);
        font-size: 0.9rem;
      }

      /* Quote Section */
      .quote-card {
        background: linear-gradient(
          135deg,
          rgba(37, 99, 235, 0.1),
          rgba(124, 58, 237, 0.1)
        );
        border-left: 4px solid var(--primary);
        padding: 1.5rem;
        font-style: italic;
        margin: 2rem 0;
      }

      .quote-author {
        text-align: right;
        color: var(--accent);
        margin-top: 1rem;
        font-weight: 500;
      }

      /* Skills Grid */
      .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
        gap: 1rem;
        margin-top: 1rem;
      }

      .skill-item {
        background: rgba(30, 41, 59, 0.7);
        border-radius: 10px;
        padding: 1rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        transition: all 0.3s ease;
      }

      .skill-item:hover {
        background: rgba(37, 99, 235, 0.2);
        transform: scale(1.05);
      }

      .skill-item img {
        width: 40px;
        height: 40px;
        margin-bottom: 0.5rem;
      }

      /* Stats Section */
      .stats-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1.5rem;
        margin-top: 2rem;
      }

      .stat-card {
        background: var(--card-bg);
        border-radius: 15px;
        padding: 1.5rem;
        text-align: center;
      }

      /* Footer */
      .footer {
        text-align: center;
        margin-top: 3rem;
        padding-top: 2rem;
        border-top: 1px solid rgba(255, 255, 255, 0.1);
        color: var(--gray);
      }

      @media (max-width: 768px) {
        h1 {
          font-size: 2.5rem;
        }
        h2 {
          font-size: 1.5rem;
        }
        .profile-section {
          flex-direction: column;
        }
        .profile-text {
          text-align: center;
        }
      }
    </style>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
  </head>
  <body>
    <div class="container">
      <!-- Header Section -->
      <header class="header">
        <div class="header-banner">
          <img
            width="100%"
            src="https://user-images.githubusercontent.com/109351602/202650321-7f4da361-f98f-4345-8df4-adf352a11322.gif"
            alt="Developer Banner"
          />
        </div>

        <div class="profile-section">
          <img
            src="https://cdn.dribbble.com/users/926537/screenshots/4502924/python-2.gif"
            alt="Shivam Chaudhary"
            class="profile-img"
          />

          <div class="profile-text">
            <h1>Shivam Chaudhary</h1>
            <h2>Full Stack Developer | MERN Specialist</h2>
            <p class="tagline">
              Crafting scalable, production-ready applications with modern
              technologies. Passionate about clean code, API design, and solving
              real-world problems.
            </p>

            <div>
              <span class="badge">React</span>
              <span class="badge">Node.js</span>
              <span class="badge">TypeScript</span>
              <span class="badge">MongoDB</span>
              <span class="badge">AWS</span>
              <span class="badge">AI/ML</span>
            </div>

            <p style="margin-top: 1rem">
              <img
                src="https://komarev.com/ghpvc/?username=shivammchaudhary1&label=Profile%20views&color=0e75b6&style=flat"
                alt="Profile views"
              />
            </p>
          </div>
        </div>
      </header>

      <!-- Career Timeline -->
      <section class="card">
        <h2 class="card-title">
          <i class="fas fa-briefcase"></i> Career Journey
        </h2>
        <div class="timeline">
          <div class="timeline-item">
            <h3 class="timeline-title">American Chase</h3>
            <p class="timeline-subtitle">Software Development Engineer</p>
            <p class="timeline-date">Present</p>
            <p>
              Building enterprise-level applications with modern tech stack.
            </p>
          </div>

          <div class="timeline-item">
            <h3 class="timeline-title">Clinvvo.ai</h3>
            <p class="timeline-subtitle">Software Development Engineer</p>
            <p class="timeline-date">Previous</p>
            <p>
              Developed AI-powered healthcare solutions and scalable systems.
            </p>
          </div>

          <div class="timeline-item">
            <h3 class="timeline-title">WLC Technology LLP</h3>
            <p class="timeline-subtitle">Software Developer</p>
            <p class="timeline-date">Earlier</p>
            <p>
              Started professional journey building web applications and
              services.
            </p>
          </div>
        </div>
      </section>

      <!-- Quote Section -->
      <section class="card">
        <h2 class="card-title">
          <i class="fas fa-quote-left"></i> Inspired By
        </h2>
        <div class="quote-card">
          <p>
            "The only way to do great work is to love what you do. If you
            haven't found it yet, keep looking. Don't settle."
          </p>
          <p class="quote-author">- Steve Jobs</p>
        </div>
        <div class="quote-card">
          <p>"First, solve the problem. Then, write the code."</p>
          <p class="quote-author">- John Johnson</p>
        </div>
      </section>

      <!-- About & Learning -->
      <section class="card">
        <h2 class="card-title"><i class="fas fa-user"></i> About & Learning</h2>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem">
          <div>
            <h3 style="color: var(--accent); margin-bottom: 1rem">Currently</h3>
            <p>
              <i
                class="fas fa-graduation-cap"
                style="color: var(--primary); margin-right: 10px"
              ></i>
              Deep diving into <strong>AI Engineering & LLMs</strong>, exploring
              the frontier of machine learning and large language models.
            </p>
          </div>
          <div>
            <h3 style="color: var(--accent); margin-bottom: 1rem">Portfolio</h3>
            <p>
              <i
                class="fas fa-laptop-code"
                style="color: var(--primary); margin-right: 10px"
              ></i>
              All projects available at:
              <a
                href="https://shivammchaudhary1.github.io/"
                style="color: var(--accent)"
                >shivammchaudhary1.github.io</a
              >
            </p>
          </div>
        </div>

        <div style="margin-top: 1.5rem">
          <h3 style="color: var(--accent); margin-bottom: 1rem">Expertise</h3>
          <p>
            <i
              class="fas fa-code"
              style="color: var(--primary); margin-right: 10px"
            ></i>
            Ask me about <strong>MERN Stack</strong>, scalable architecture, API
            design, and modern web development practices.
          </p>
        </div>

        <div style="margin-top: 1.5rem">
          <h3 style="color: var(--accent); margin-bottom: 1rem">Contact</h3>
          <p>
            <i
              class="fas fa-envelope"
              style="color: var(--primary); margin-right: 10px"
            ></i>
            Reach me at:
            <a
              href="mailto:shivamchaudhary75@gmail.com"
              style="color: var(--accent)"
              >shivamchaudhary75@gmail.com</a
            >
          </p>
        </div>
      </section>

      <!-- Skills & Technologies -->
      <section class="card">
        <h2 class="card-title">
          <i class="fas fa-tools"></i> Technologies & Tools
        </h2>
        <div class="skills-grid">
          <!-- JavaScript -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"
              alt="JavaScript"
            />
            <span>JavaScript</span>
          </div>

          <!-- TypeScript -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg"
              alt="TypeScript"
            />
            <span>TypeScript</span>
          </div>

          <!-- React -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg"
              alt="React"
            />
            <span>React</span>
          </div>

          <!-- Node.js -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg"
              alt="Node.js"
            />
            <span>Node.js</span>
          </div>

          <!-- MongoDB -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg"
              alt="MongoDB"
            />
            <span>MongoDB</span>
          </div>

          <!-- Express -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original-wordmark.svg"
              alt="Express"
            />
            <span>Express</span>
          </div>

          <!-- AWS -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg"
              alt="AWS"
            />
            <span>AWS</span>
          </div>

          <!-- Tailwind -->
          <div class="skill-item">
            <img
              src="https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg"
              alt="Tailwind"
            />
            <span>Tailwind</span>
          </div>

          <!-- Git -->
          <div class="skill-item">
            <img
              src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg"
              alt="Git"
            />
            <span>Git</span>
          </div>

          <!-- Docker -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg"
              alt="Docker"
            />
            <span>Docker</span>
          </div>

          <!-- Python -->
          <div class="skill-item">
            <img
              src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg"
              alt="Python"
            />
            <span>Python</span>
          </div>

          <!-- Postman -->
          <div class="skill-item">
            <img
              src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg"
              alt="Postman"
            />
            <span>Postman</span>
          </div>
        </div>
      </section>

      <!-- GitHub Trophies & Stats -->
      <section class="card">
        <h2 class="card-title">
          <i class="fas fa-trophy"></i> GitHub Achievements
        </h2>

        <!-- Trophies -->
        <div style="margin-bottom: 2rem">
          <h3 style="color: var(--accent); margin-bottom: 1rem">Trophies</h3>
          <a href="https://github.com/ryo-ma/github-profile-trophy">
            <img
              src="https://github-profile-trophy.vercel.app/?username=shivammchaudhary1&theme=onedark&row=2&column=4&margin-w=10&margin-h=10"
              alt="GitHub Trophies"
              style="width: 100%; border-radius: 10px"
            />
          </a>
        </div>

        <!-- Stats -->
        <div class="stats-container">
          <div class="stat-card">
            <h3>GitHub Stats</h3>
            <img
              src="https://github-readme-stats.vercel.app/api?username=shivammchaudhary1&show_icons=true&theme=onedark&hide_border=true"
              alt="GitHub Stats"
              style="width: 100%"
            />
          </div>

          <div class="stat-card">
            <h3>Top Languages</h3>
            <img
              src="https://github-readme-stats.vercel.app/api/top-langs/?username=shivammchaudhary1&layout=compact&theme=onedark&hide_border=true"
              alt="Top Languages"
              style="width: 100%"
            />
          </div>

          <div class="stat-card">
            <h3>Streak Stats</h3>
            <img
              src="https://github-readme-streak-stats.herokuapp.com/?user=shivammchaudhary1&theme=onedark&hide_border=true"
              alt="GitHub Streak"
              style="width: 100%"
            />
          </div>
        </div>
      </section>

      <!-- Connect Section -->
      <section class="card">
        <h2 class="card-title">
          <i class="fas fa-network-wired"></i> Connect With Me
        </h2>
        <div
          style="
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 1rem;
            flex-wrap: wrap;
          "
        >
          <a
            href="https://twitter.com/sivamchdhry"
            target="_blank"
            style="text-decoration: none"
          >
            <div class="skill-item" style="width: 120px">
              <i
                class="fab fa-twitter"
                style="font-size: 2rem; color: #1da1f2"
              ></i>
              <span>Twitter</span>
            </div>
          </a>

          <a
            href="https://linkedin.com/in/shivammchaudhary/"
            target="_blank"
            style="text-decoration: none"
          >
            <div class="skill-item" style="width: 120px">
              <i
                class="fab fa-linkedin-in"
                style="font-size: 2rem; color: #0077b5"
              ></i>
              <span>LinkedIn</span>
            </div>
          </a>

          <a
            href="https://github.com/shivammchaudhary1"
            target="_blank"
            style="text-decoration: none"
          >
            <div class="skill-item" style="width: 120px">
              <i
                class="fab fa-github"
                style="font-size: 2rem; color: white"
              ></i>
              <span>GitHub</span>
            </div>
          </a>

          <a
            href="mailto:shivamchaudhary75@gmail.com"
            style="text-decoration: none"
          >
            <div class="skill-item" style="width: 120px">
              <i
                class="fas fa-envelope"
                style="font-size: 2rem; color: #ea4335"
              ></i>
              <span>Email</span>
            </div>
          </a>
        </div>
      </section>

      <!-- Footer -->
      <footer class="footer">
        <p>© 2024 Shivam Chaudhary. All rights reserved.</p>
        <p style="margin-top: 0.5rem; font-size: 0.9rem">
          <i class="fas fa-map-marker-alt" style="margin-right: 5px"></i> Based
          in Lucknow, India
        </p>
      </footer>
    </div>
  </body>
</html>
