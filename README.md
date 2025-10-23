<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Chintakrindi Venkata Mohan Sai — Portfolio / Resume</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg: #0f1724;
      --card: #0b1220;
      --muted: #94a3b8;
      --accent: #6c5ce7;
      --text: #e6eef8;
      --glass: rgba(255,255,255,0.03);
      --glass-2: rgba(255,255,255,0.02);
      --success: #34d399;
      --danger: #ff6b6b;
    }
    :root.light{
      --bg: #f6f8fb;
      --card: #ffffff;
      --muted: #44566a;
      --accent: #0b6cff;
      --text: #0b1220;
      --glass: rgba(11,18,32,0.03);
      --glass-2: rgba(11,18,32,0.02);
      --success: #059669;
      --danger: #e45656;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,var(--bg), #03070a 120%);
      color:var(--text);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      padding:36px 20px;
    }

    .container{
      max-width:1100px;
      margin:0 auto;
      display:grid;
      grid-template-columns: 320px 1fr;
      gap:28px;
    }

    /* SIDEBAR */
    .sidebar{
      background:linear-gradient(180deg,var(--card), rgba(255,255,255,0.01));
      border-radius:14px;
      padding:24px;
      position:sticky;
      top:36px;
      height:calc(100vh - 72px);
      overflow:auto;
      box-shadow: 0 10px 30px rgba(2,6,23,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
      border:1px solid rgba(255,255,255,0.03);
    }

    .profile-photo{
      width:110px;
      height:110px;
      border-radius:14px;
      background:linear-gradient(135deg,var(--accent), #8f7bff);
      display:flex;
      align-items:center;
      justify-content:center;
      font-weight:800;
      color:white;
      font-size:28px;
      margin-bottom:14px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.35);
    }

    .name{
      font-size:20px;
      letter-spacing:0.6px;
      font-weight:700;
      margin-bottom:6px;
    }
    .role{
      font-size:13px;
      color:var(--muted);
      margin-bottom:14px;
    }

    .contact-list{ list-style:none; padding:0; margin:10px 0 20px 0; }
    .contact-list li{ display:flex; gap:10px; align-items:center; font-size:13px; color:var(--muted); margin:10px 0; }
    .contact-icon{
      width:34px; height:34px; border-radius:8px; display:inline-flex; align-items:center; justify-content:center;
      background:var(--glass); color:var(--accent); flex: 0 0 34px;
    }
    a.link{ color:var(--text); text-decoration:none; font-weight:600; }
    a.sub{ color:var(--muted); text-decoration:none; font-size:13px }

    .section-title{
      display:flex; align-items:center; gap:12px; margin:18px 0 8px 0;
    }
    .section-title h3{
      margin:0; font-size:14px; letter-spacing:0.6px; font-weight:700;
    }

    .muted { color:var(--muted); font-size:13px }

    .skills-grid { display:flex; flex-wrap:wrap; gap:8px; margin-top:8px; }
    .chip{
      padding:8px 10px; background:var(--glass); border-radius:999px; font-weight:600; font-size:13px; color:var(--text);
      border:1px solid rgba(255,255,255,0.02);
    }

    .sidebar hr{ border:0; height:1px; background:var(--glass-2); margin:18px 0 }

    /* MAIN */
    .main{
      background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      border-radius:14px;
      padding:28px;
      min-height:300px;
    }
    .github1{
        cursor: pointer;
    }

    .top-row{ display:flex; justify-content:space-between; align-items:flex-start; gap:12px; margin-bottom:12px }
    .intro{
      font-size:18px; font-weight:700;
    }
    .summary{ margin:8px 0 18px 0; color:var(--muted); }

    /* cards / lists */
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      border-radius:12px;
      padding:16px;
      margin-bottom:14px;
      border:1px solid rgba(255,255,255,0.03);
    }
    .footer{
        cursor: pointer;
    }
    .edu-grid{ display:flex; gap:10px; align-items:center; justify-content:space-between; flex-wrap:wrap; }
    .edu-left{ max-width:75% }
    .edu-year{ color:var(--muted); font-weight:600 }

    /* Projects */
    .projects{ display:grid; grid-template-columns: 1fr 1fr; gap:14px; }
    .project{
      padding:14px; border-radius:10px; border:1px solid rgba(255,255,255,0.03);
      background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));
      transition: transform .25s ease, box-shadow .25s ease;
    }
    .project:hover{ transform: translateY(-6px); box-shadow: 0 14px 40px rgba(2,6,23,0.45) }
    .project h4{ margin:0 0 8px 0; font-size:15px }
    .project p{ margin:0; color:var(--muted); font-size:13px }

    /* skill bars */
    .skill-row{ display:flex; align-items:center; justify-content:space-between; gap:10px; margin:8px 0 }
    .skill-name{ font-weight:600; color:var(--muted); width:130px; font-size:13px }
    .bar{ flex:1; height:10px; background:var(--glass-2); border-radius:999px; overflow:hidden; position:relative }
    .bar > i{ position:absolute; left:0; top:0; bottom:0; width:0%; background:linear-gradient(90deg,var(--accent), #a88cff); display:block; border-radius:999px; transition:width .9s cubic-bezier(.2,.9,.3,1) }

    /* certificates & achievements */
    .badges{ display:flex; gap:8px; flex-wrap:wrap }
    .badge{ padding:8px 12px; border-radius:8px; background:var(--glass); color:var(--text); font-weight:700; font-size:13px }

    /* footer */
    footer{ text-align:center; font-size:12px; color:var(--muted); margin-top:18px; }

    /* theme toggle */
    .toggle{
      cursor:pointer;
      background:var(--glass);
      padding:8px;
      border-radius:10px;
      display:inline-flex;
      gap:8px;
      align-items:center;
      border:1px solid rgba(255,255,255,0.02);
    }
    .toggle svg{ width:18px; height:18px; display:block }

    /* responsive */
    @media (max-width:980px){
      .container{ grid-template-columns: 1fr; }
      .sidebar{ height:auto; position:static }
      .projects{ grid-template-columns: 1fr; }
    }

    /* print-friendly */
    @media print{
      body{ background:white; color:#000 }
      .container{ box-shadow:none; max-width:100% }
      .sidebar{ display:none }
    }
  </style>
</head>
<body>

  <div class="container" id="page-root">

    <!-- SIDEBAR -->
    <aside class="sidebar" aria-label="Sidebar with contact & skills">
      <div style="display:flex;align-items:center;gap:12px">
        <div class="profile-photo" >
            <img src="c:\Users\chmoh\Downloads\profilepic.jpeg" alt="">
        </div>
        <div style="flex:1">
          <div class="name">CHINTAKRINDI VENKATA MOHAN SAI</div>
          <div class="role">Aspiring Full-Stack Developer • Python Enthusiast</div>
        </div>
      </div>

      <ul class="contact-list" style="margin-top:12px">
        <li><span class="contact-icon">✉️</span><div><div class="link">mohansaichintakrindi.009@gmail.com</div><div class="muted">Email</div></div></li>
        <li><span class="contact-icon">📞</span><div><div class="link">+91 7569598651</div><div class="muted">Phone</div></div></li>
        <li><span class="contact-icon">📍</span><div><div class="link">Vijayawada, India</div><div class="muted">Location</div></div></li>
        <li><span class="contact-icon">🔗</span><div><a class="link" href="https://github.com/ChintakrindiVenkatMohanSai" target="_blank">github.com/ChintakrindiVenkatMohanSai</a><div class="muted">GitHub</div></div></li>
        <li><span class="contact-icon">💼</span><div><a class="link" href="https://linkedin.com/in/chintakrindi-venkata-mohan-sai-b2a70b252" target="_blank">linkedin.com/in/chintakrindi-venkata-mohan-sai</a><div class="muted">LinkedIn</div></div></li>
      </ul>

      <hr>

      <div class="section-title"><h3>Profile</h3></div>
      <div class="muted">Motivated student passionate about web development and continuous learning. Hands-on experience in Python full-stack development, with a strong interest in building interactive, responsive web applications and gaining practical experience through projects.</div>

      <div class="section-title" style="margin-top:18px"><h3>Skills</h3></div>
      <div class="skills-grid" style="margin-bottom:8px">
        <span class="chip">Python</span>
        <span class="chip">HTML</span>
        <span class="chip">CSS</span>
        <span class="chip">JavaScript</span>
        <span class="chip">React.js</span>
        <span class="chip">Angular</span>
        <span class="chip">MySQL</span>
        <span class="chip">Django</span>
      </div>

      <div class="section-title"><h3>Certificates</h3></div>
      <div class="badges" style="margin-top:8px">
        <div class="badge">Web Development — Corizo</div>
        <div class="badge">Wireless Communication</div>
        <div class="badge">Python</div>
      </div>

      <hr>

      <div style="display:flex;justify-content:space-between;align-items:center;margin-top:14px">
        <div>
          <div class="muted" style="font-weight:700">Theme</div>
          <div style="margin-top:8px">
            <div class="toggle" id="themeToggle" title="Toggle dark / light theme">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" style="width:16px;height:16px">
                <path d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path>
              </svg>
              <div style="font-weight:700;font-size:13px">Dark / Light</div>
            </div>
          </div>
        </div>

        <div style="text-align:right">
          <div class="muted" style="font-weight:700">Download</div>
          <div style="margin-top:8px"><button id="printBtn" style="padding:8px 12px;border-radius:8px;border:0;background:var(--accent);color:white;font-weight:700;cursor:pointer">Print / PDF</button></div>
        </div>
      </div>

      <footer style="margin-top:18px">© CHINTAKRINDI VENKATA MOHAN SAI</footer>
    </aside>


    <!-- MAIN CONTENT -->
    <main class="main" role="main" aria-label="Main resume content">
      <div class="top-row">
        <div>
          <div class="intro">Hi — I'm <strong>Chintakrindi Venkata Mohan Sai</strong></div>
          <div class="summary">4rd year B.Tech (ECE) student with practical experience in Python full-stack development and machine learning projects. Passionate about building interactive web applications and continuously learning new technologies.</div>
        </div>

        <div style="text-align:right">
          <div style="font-size:13px;color:var(--muted);font-weight:700">Currently Learning</div>
          <div style="font-size:13px;margin-top:6px" class="muted">MySQL, React.js, Django, Angular</div>
        </div>
      </div>

      <!-- Education -->
      <section class="card" aria-labelledby="education">
        <div class="section-title"><h3 id="education">Education</h3></div>
        
        <div class="edu-grid">
          <div class="edu-left">
            <div style="font-weight:700">Bachelor of Technology — Electronics & Communication Engineering</div>
            <div class="muted">VR Siddhartha Engineering College, Vijayawada</div>
          </div>
          <div class="edu-year">2022 — 2026</div>
        </div>
        
        <div class="edu-grid" style="margin-top:12px">
          <div class="edu-left">
            <div style="font-weight:700">Secondary Education</div>
            <div class="muted">Narayana Jr College, Vijayawada</div>
          </div>
          <div class="edu-year">2020 — 2022</div>
        </div>
        
        <div class="edu-grid" style="margin-top:12px">
          <div class="edu-left">
            <div style="font-weight:700">Primary School</div>
            <div class="muted">Sri Chaitanya School, Mangalagiri</div>
          </div>
          <div class="edu-year">2008 — 2019</div>
        </div>
      </section>

      <!-- Projects -->
      <section style="margin-top:12px">
        <div class="section-title"><h3>Projects</h3></div>
        <div class="projects">
          <article class="project">
            <h4>Diabetic Retinopathy Quality Estimation</h4>
            <p>Developing a machine learning model to evaluate retinal image quality for diabetic retinopathy, improving screening accuracy and automation.</p>
          </article>

          <article class="project">
            <h4>E-commerce Website</h4>
            <p>Developed a responsive eCommerce website using HTML, CSS, and JavaScript. Implemented interactive product pages, shopping cart, and search & sort functionality.</p>
          </article>

          <article class="project">
            <h4>Basic Calculators</h4>
            <p>Built web-based calculators performing addition, subtraction, multiplication, and division. Designed with clean UI, dark/light theme toggle, and responsive layout.</p>
          </article>

          <article class="project">
            <h4>Interest Calculator</h4>
            <p>Created a web application for calculating Simple and Compound Interest. Features modern UI, responsive design, dark/light mode, and real-time result display.</p>
          </article>
          
          <article class="project">
            <h4>Personal Portfolio</h4>
            <p>Developed a responsive portfolio website with interactive project sections and smooth animations using HTML, CSS, and JavaScript.</p>
          </article>
        </div>
      </section>

      <!-- Courses -->
      <section style="margin-top:18px" aria-labelledby="courses">
        <div class="section-title"><h3 id="courses">Courses</h3></div>

        <div class="card">
          <div style="display:flex;justify-content:space-between;align-items:flex-start">
            <div>
              <div style="font-weight:700">Web Development (HTML, CSS, JavaScript)</div>
              <div class="muted">Corizo Platform</div>
            </div>
          </div>
        </div>

        <div class="card" style="margin-top:10px">
          <div style="font-weight:700">Python Full Stack</div>
          <div class="muted" style="margin-top:6px">Nipuna Technologies</div>
          <div style="margin-top:8px;color:var(--muted)">Learned Python, HTML, CSS, and JavaScript; currently learning MySQL, React.js, Django, and Angular</div>
        </div>
      </section>

      <!-- Skills & proficiency -->
      <section style="margin-top:18px" aria-labelledby="skills">
        <div class="section-title"><h3 id="skills">Technical Skills</h3></div>

        <div class="card">
          <div class="skill-row"><div class="skill-name">Python</div>
            <div class="bar" data-p="80"><i style="width:0%"></i></div></div>

          <div class="skill-row"><div class="skill-name">HTML</div>
            <div class="bar" data-p="85"><i style="width:0%"></i></div></div>

          <div class="skill-row"><div class="skill-name">CSS</div>
            <div class="bar" data-p="80"><i style="width:0%"></i></div></div>

          <div class="skill-row"><div class="skill-name">JavaScript</div>
            <div class="bar" data-p="75"><i style="width:0%"></i></div></div>
            
          <div class="skill-row"><div class="skill-name">React.js</div>
            <div class="bar" data-p="70"><i style="width:0%"></i></div></div>
            
          <div class="skill-row"><div class="skill-name">Django</div>
            <div class="bar" data-p="65"><i style="width:0%"></i></div></div>
        </div>
      </section>

      <!-- Certificates & Achievements -->
      <section style="margin-top:18px">
        <div class="section-title"><h3>Certificates</h3></div>

        <div class="card">
          <div style="display:flex;gap:12px;flex-wrap:wrap">
            <div style="flex:1">
              <div style="font-weight:700">Web Development Certificate</div>
              <div class="muted" style="margin-top:6px">Corizo Platform</div>
            </div>
            <div style="flex:1">
              <div style="font-weight:700">Wireless Communication</div>
              <div class="muted" style="margin-top:6px">Certificate in wireless communication technologies</div>
            </div>
          </div>

          <div style="display:flex;gap:12px;flex-wrap:wrap; margin-top:12px">
            <div style="flex:1">
              <div style="font-weight:700">Python Programming</div>
              <div class="muted" style="margin-top:6px">Certificate in Python development</div>
            </div>
          </div>
        </div>
      </section>

      <footer style="margin-top:22px">Want the source? View on <a class="github1" href="https://github.com/ChintakrindiVenkatMohanSai" style="color:var(--accent);font-weight:800" target="_blank">GitHub</a></footer>

    </main>
  </div>

  <script>
    // theme toggle
    const root = document.documentElement;
    const toggle = document.getElementById('themeToggle');
    const printBtn = document.getElementById('printBtn');

    // load saved preference
    const saved = localStorage.getItem('cv-theme');
    if(saved === 'light') root.classList.add('light');

    toggle.addEventListener('click', () => {
      root.classList.toggle('light');
      localStorage.setItem('cv-theme', root.classList.contains('light') ? 'light' : 'dark');
    });

    // print / save as PDF
    printBtn.addEventListener('click', () => window.print());

    // animate skill bars on scroll into view
    function animateBars(){
      document.querySelectorAll('.bar').forEach(bar => {
        const p = parseInt(bar.dataset.p || 0,10);
        const inner = bar.querySelector('i');
        const rect = bar.getBoundingClientRect();
        if(rect.top < window.innerHeight - 60){
          inner.style.width = p + '%';
        }
      });
    }
    window.addEventListener('scroll', animateBars);
    window.addEventListener('load', animateBars);

    // small accessibility: keyboard toggle (T)
    window.addEventListener('keydown', (e) => {
      if(e.key === 't' || e.key === 'T'){
        toggle.click();
      }
    });
  </script>
</body>
</html>
