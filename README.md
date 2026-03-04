<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Toni Junior Deeb | Teacher Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --cream:    #FDF6EC;
      --warm1:    #F4A535;
      --warm2:    #E8793A;
      --warm3:    #D45F2A;
      --brown:    #3B2314;
      --light:    #FEF9F2;
      --muted:    #9A7355;
      --card-bg:  #FFFAF3;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--cream);
      color: var(--brown);
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 1.2rem 3rem;
      background: rgba(253,246,236,0.85);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(244,165,53,0.2);
    }
    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.15rem; font-weight: 700;
      color: var(--warm3); letter-spacing: 0.02em;
    }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      text-decoration: none; color: var(--muted);
      font-size: 0.875rem; font-weight: 500; letter-spacing: 0.05em;
      text-transform: uppercase; transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--warm2); }

    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: grid; grid-template-columns: 1fr 1fr; align-items: center;
      padding: 8rem 6rem 4rem;
      position: relative; overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute; top: -10%; right: -5%;
      width: 55vw; height: 110vh;
      background: radial-gradient(ellipse at 60% 40%, #F4A53530 0%, #E8793A18 40%, transparent 70%);
      border-radius: 40% 60% 60% 40% / 50% 50% 50% 50%;
      animation: blobFloat 8s ease-in-out infinite;
    }
    @keyframes blobFloat {
      0%,100% { transform: translateY(0) rotate(0deg); }
      50%      { transform: translateY(-20px) rotate(3deg); }
    }
    .hero-text { position: relative; z-index: 2; }
    .hero-eyebrow {
      display: inline-block;
      font-size: 0.75rem; font-weight: 500; letter-spacing: 0.18em;
      text-transform: uppercase; color: var(--warm2);
      background: rgba(244,165,53,0.12);
      padding: 0.4rem 1rem; border-radius: 20px;
      margin-bottom: 1.5rem;
      animation: fadeUp 0.8s ease both;
    }
    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.8rem, 5vw, 4.5rem);
      line-height: 1.1; font-weight: 700;
      color: var(--brown);
      animation: fadeUp 0.8s 0.15s ease both;
    }
    .hero h1 em { color: var(--warm2); font-style: italic; }
    .hero-tagline {
      margin-top: 1.5rem;
      font-size: 1.15rem; line-height: 1.7;
      color: var(--muted); max-width: 420px;
      animation: fadeUp 0.8s 0.3s ease both;
    }
    .hero-cta {
      margin-top: 2.5rem; display: flex; gap: 1rem; flex-wrap: wrap;
      animation: fadeUp 0.8s 0.45s ease both;
    }
    .btn {
      display: inline-block; padding: 0.85rem 2rem;
      border-radius: 50px; font-size: 0.9rem; font-weight: 500;
      text-decoration: none; transition: all 0.25s;
      cursor: pointer;
    }
    .btn-primary {
      background: linear-gradient(135deg, var(--warm1), var(--warm2));
      color: #fff; box-shadow: 0 4px 20px rgba(232,121,58,0.35);
    }
    .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 28px rgba(232,121,58,0.45); }
    .btn-outline {
      border: 1.5px solid var(--warm2); color: var(--warm2); background: transparent;
    }
    .btn-outline:hover { background: rgba(232,121,58,0.08); transform: translateY(-2px); }

    /* Hero visual */
    .hero-visual {
      position: relative; z-index: 2;
      display: flex; justify-content: center; align-items: center;
      animation: fadeIn 1s 0.5s ease both;
    }
    .hero-card {
      width: 340px; height: 400px;
      background: linear-gradient(145deg, #FFF4E0, #FFE0B2);
      border-radius: 30px 30px 120px 30px;
      display: flex; flex-direction: column;
      align-items: center; justify-content: center; gap: 1rem;
      box-shadow: 0 20px 60px rgba(212,95,42,0.15), 0 4px 12px rgba(0,0,0,0.05);
      position: relative; overflow: hidden;
    }
    .hero-card::after {
      content: '';
      position: absolute; bottom: -30px; right: -30px;
      width: 120px; height: 120px;
      background: rgba(244,165,53,0.2);
      border-radius: 50%;
    }
    .avatar-circle {
      width: 110px; height: 110px; border-radius: 50%;
      background: linear-gradient(135deg, var(--warm1), var(--warm3));
      display: flex; align-items: center; justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 2.5rem; color: #fff; font-weight: 700;
      box-shadow: 0 8px 24px rgba(212,95,42,0.3);
    }
    .hero-card-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.3rem; font-weight: 700; color: var(--brown);
      text-align: center; padding: 0 1.5rem;
    }
    .hero-card-sub {
      font-size: 0.8rem; color: var(--muted); text-align: center;
      letter-spacing: 0.08em; text-transform: uppercase;
    }
    .floating-badge {
      position: absolute;
      background: #fff;
      border-radius: 14px;
      padding: 0.6rem 1rem;
      display: flex; align-items: center; gap: 0.5rem;
      box-shadow: 0 4px 16px rgba(0,0,0,0.08);
      font-size: 0.8rem; font-weight: 500; color: var(--brown);
    }
    .badge-1 { top: -15px; left: -30px; animation: badgeFloat 4s ease-in-out infinite; }
    .badge-2 { bottom: 20px; left: -40px; animation: badgeFloat 4s 1.5s ease-in-out infinite; }
    .badge-3 { top: 40px; right: -40px; animation: badgeFloat 4s 0.8s ease-in-out infinite; }
    @keyframes badgeFloat {
      0%,100% { transform: translateY(0); }
      50%      { transform: translateY(-8px); }
    }
    .badge-icon { font-size: 1.1rem; }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to   { opacity: 1; }
    }

    /* ── SECTIONS ── */
    section { padding: 6rem 6rem; }
    .section-label {
      display: inline-flex; align-items: center; gap: 0.6rem;
      font-size: 0.72rem; font-weight: 500; letter-spacing: 0.18em;
      text-transform: uppercase; color: var(--warm2);
      margin-bottom: 1rem;
    }
    .section-label::before {
      content: ''; display: block;
      width: 24px; height: 2px;
      background: var(--warm1);
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2rem, 3.5vw, 3rem);
      font-weight: 700; line-height: 1.2;
      color: var(--brown);
      margin-bottom: 1.5rem;
    }

    /* ── ABOUT ── */
    .about { background: var(--light); }
    .about-grid { display: grid; grid-template-columns: 1fr 1.5fr; gap: 5rem; align-items: center; }
    .about-image-block {
      position: relative;
    }
    .about-img-placeholder {
      width: 100%; aspect-ratio: 4/5;
      background: linear-gradient(160deg, #FFE8C8, #FFCB8A);
      border-radius: 20px 20px 80px 20px;
      display: flex; flex-direction: column;
      align-items: center; justify-content: center; gap: 1rem;
      font-size: 4rem;
      box-shadow: 0 16px 48px rgba(212,95,42,0.12);
    }
    .about-img-note {
      font-size: 0.75rem; color: var(--muted); text-align: center; padding: 0 1.5rem;
    }
    .stat-chips { display: flex; gap: 0.8rem; flex-wrap: wrap; margin-top: 1.5rem; }
    .chip {
      background: #fff;
      border: 1px solid rgba(244,165,53,0.3);
      border-radius: 30px; padding: 0.5rem 1.2rem;
      font-size: 0.8rem; font-weight: 500; color: var(--muted);
    }
    .chip span { color: var(--warm2); font-weight: 700; margin-right: 0.3rem; }
    .about-text p {
      font-size: 1.05rem; line-height: 1.85;
      color: #6B4C35; margin-bottom: 1.2rem;
    }

    /* ── PHILOSOPHY ── */
    .philosophy { background: var(--cream); }
    .pillars { display: grid; grid-template-columns: repeat(3,1fr); gap: 2rem; margin-top: 3rem; }
    .pillar {
      background: var(--card-bg);
      border: 1px solid rgba(244,165,53,0.2);
      border-radius: 20px; padding: 2.5rem 2rem;
      position: relative; overflow: hidden;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .pillar:hover { transform: translateY(-6px); box-shadow: 0 16px 40px rgba(212,95,42,0.1); }
    .pillar::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0; height: 4px;
      background: linear-gradient(90deg, var(--warm1), var(--warm2));
    }
    .pillar-icon { font-size: 2.2rem; margin-bottom: 1rem; }
    .pillar h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.25rem; font-weight: 700;
      color: var(--brown); margin-bottom: 0.8rem;
    }
    .pillar p { font-size: 0.92rem; line-height: 1.7; color: var(--muted); }

    /* ── PORTFOLIO ── */
    .portfolio-section { background: var(--light); }
    .portfolio-grid { display: grid; grid-template-columns: repeat(2,1fr); gap: 2rem; margin-top: 3rem; }
    .portfolio-card {
      background: var(--card-bg);
      border-radius: 20px; overflow: hidden;
      border: 1px solid rgba(244,165,53,0.15);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .portfolio-card:hover { transform: translateY(-5px); box-shadow: 0 16px 40px rgba(212,95,42,0.1); }
    .card-header {
      height: 140px;
      display: flex; align-items: center; justify-content: center;
      font-size: 3rem;
      position: relative; overflow: hidden;
    }
    .card-h1 { background: linear-gradient(135deg, #FFE0A0, #FFBB55); }
    .card-h2 { background: linear-gradient(135deg, #FFD0B0, #FF9060); }
    .card-h3 { background: linear-gradient(135deg, #FFDDC0, #FFAA70); }
    .card-h4 { background: linear-gradient(135deg, #FFF0C0, #FFD060); }
    .card-body { padding: 1.8rem; }
    .card-tag {
      display: inline-block;
      background: rgba(244,165,53,0.12); color: var(--warm2);
      font-size: 0.7rem; font-weight: 500; letter-spacing: 0.1em;
      text-transform: uppercase; border-radius: 20px; padding: 0.3rem 0.8rem;
      margin-bottom: 0.8rem;
    }
    .card-body h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.2rem; font-weight: 700; color: var(--brown);
      margin-bottom: 0.6rem;
    }
    .card-body p { font-size: 0.88rem; line-height: 1.65; color: var(--muted); }
    .card-footer {
      padding: 1rem 1.8rem; border-top: 1px solid rgba(244,165,53,0.1);
      display: flex; align-items: center; justify-content: space-between;
    }
    .card-meta { font-size: 0.78rem; color: var(--muted); }
    .card-link {
      font-size: 0.8rem; font-weight: 500; color: var(--warm2);
      text-decoration: none; display: flex; align-items: center; gap: 0.3rem;
    }
    .card-link:hover { color: var(--warm3); }

    /* ── SKILLS ── */
    .skills-section { background: var(--cream); }
    .skills-grid { display: grid; grid-template-columns: repeat(4,1fr); gap: 1.5rem; margin-top: 3rem; }
    .skill-item {
      background: var(--card-bg);
      border: 1px solid rgba(244,165,53,0.2);
      border-radius: 16px; padding: 1.8rem 1.5rem;
      text-align: center;
      transition: transform 0.3s;
    }
    .skill-item:hover { transform: translateY(-4px); }
    .skill-icon { font-size: 2rem; margin-bottom: 0.8rem; }
    .skill-name { font-size: 0.88rem; font-weight: 500; color: var(--brown); }

    /* ── CONTACT ── */
    .contact-section {
      background: linear-gradient(135deg, #3B2314 0%, #5C3620 100%);
      color: #fff; text-align: center;
    }
    .contact-section .section-label { color: var(--warm1); }
    .contact-section .section-label::before { background: var(--warm1); }
    .contact-section .section-title { color: #fff; }
    .contact-subtitle {
      font-size: 1.05rem; color: rgba(255,255,255,0.6);
      max-width: 500px; margin: 0 auto 2.5rem; line-height: 1.7;
    }
    .contact-links { display: flex; justify-content: center; gap: 1.5rem; flex-wrap: wrap; }
    .contact-chip {
      display: inline-flex; align-items: center; gap: 0.6rem;
      background: rgba(255,255,255,0.08);
      border: 1px solid rgba(255,255,255,0.15);
      border-radius: 50px; padding: 0.75rem 1.5rem;
      color: rgba(255,255,255,0.85);
      font-size: 0.9rem; text-decoration: none;
      transition: all 0.25s;
    }
    .contact-chip:hover {
      background: rgba(244,165,53,0.2);
      border-color: var(--warm1); color: #fff;
      transform: translateY(-2px);
    }

    /* ── FOOTER ── */
    footer {
      background: #2A1A0E; color: rgba(255,255,255,0.4);
      text-align: center; padding: 2rem;
      font-size: 0.8rem;
    }
    footer span { color: var(--warm1); }

    /* ── SCROLL REVEAL ── */
    .reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s ease, transform 0.7s ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }

    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      nav { padding: 1rem 1.5rem; }
      .nav-links { display: none; }
      .hero { grid-template-columns: 1fr; padding: 7rem 2rem 3rem; text-align: center; }
      .hero-tagline { margin: 1.5rem auto; }
      .hero-cta { justify-content: center; }
      .hero-visual { display: none; }
      section { padding: 4rem 2rem; }
      .about-grid { grid-template-columns: 1fr; gap: 2rem; }
      .pillars { grid-template-columns: 1fr; }
      .portfolio-grid { grid-template-columns: 1fr; }
      .skills-grid { grid-template-columns: repeat(2,1fr); }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <div class="nav-logo">Toni Junior Deeb</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#philosophy">Philosophy</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-text">
      <div class="hero-eyebrow">✦ K–5 English & Language Arts</div>
      <h1>Toni<br/><em>Junior Deeb</em></h1>
      <p class="hero-tagline">Leading through kindness, music and creativity — shaping young readers, writers, and thinkers one story at a time.</p>
      <div class="hero-cta">
        <a href="#portfolio" class="btn btn-primary">View My Work</a>
        <a href="#contact" class="btn btn-outline">Get in Touch</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-card">
        <div class="floating-badge badge-1"><span class="badge-icon">📖</span> ELA Specialist</div>
        <div class="floating-badge badge-2"><span class="badge-icon">🎵</span> Music-Integrated</div>
        <div class="floating-badge badge-3"><span class="badge-icon">⭐</span> K–5 Educator</div>
        <div class="avatar-circle">TJ</div>
        <div class="hero-card-name">Toni Junior Deeb</div>
        <div class="hero-card-sub">Elementary Teacher · Language Arts</div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">
    <div class="about-grid reveal">
      <div class="about-image-block">
        <div class="about-img-placeholder">
          🎨
          <div class="about-img-note">Add your photo here by replacing this block</div>
        </div>
        <div class="stat-chips">
          <div class="chip"><span>K–5</span> Grade Level</div>
          <div class="chip"><span>ELA</span> Subject</div>
          <div class="chip"><span>🎵</span> Music-Integrated</div>
        </div>
      </div>
      <div class="about-text">
        <div class="section-label">About Me</div>
        <h2 class="section-title">A classroom built on kindness & creativity</h2>
        <p>Hello! I'm Toni Junior Deeb, an elementary English and Language Arts teacher who believes that every child has a story worth telling. My classroom is a place where words come alive through music, art, and imagination.</p>
        <p>I specialize in teaching K–5 students the joy of reading and writing — weaving songs, creative play, and storytelling into every lesson so that literacy feels like an adventure, not a chore.</p>
        <p>My teaching philosophy is rooted in three core beliefs: that kindness is the foundation of learning, that creativity unlocks every child's potential, and that music is a universal language that connects us all.</p>
        <a href="#contact" class="btn btn-primary" style="margin-top:1rem;">Let's Connect</a>
      </div>
    </div>
  </section>

  <!-- PHILOSOPHY -->
  <section class="philosophy" id="philosophy">
    <div class="reveal" style="text-align:center; max-width: 600px; margin: 0 auto;">
      <div class="section-label">Teaching Philosophy</div>
      <h2 class="section-title">Three pillars of my classroom</h2>
    </div>
    <div class="pillars reveal">
      <div class="pillar">
        <div class="pillar-icon">🤝</div>
        <h3>Kindness First</h3>
        <p>A safe, caring environment is the precondition for all learning. I build classrooms where every student feels seen, heard, and valued — because children learn best when they feel loved.</p>
      </div>
      <div class="pillar">
        <div class="pillar-icon">🎵</div>
        <h3>Music as Language</h3>
        <p>Rhythm, rhyme, and melody are powerful tools for literacy. I integrate songs, chants, and musical patterns into reading and writing to engage every type of learner.</p>
      </div>
      <div class="pillar">
        <div class="pillar-icon">🎨</div>
        <h3>Creative Expression</h3>
        <p>Creativity is not a subject — it's a mindset. Through storytelling, illustration, and imaginative projects, students discover their voice and fall in love with language.</p>
      </div>
    </div>
  </section>

  <!-- PORTFOLIO -->
  <section class="portfolio-section" id="portfolio">
    <div class="reveal" style="text-align:center; max-width: 600px; margin: 0 auto;">
      <div class="section-label">Portfolio</div>
      <h2 class="section-title">Lessons, units & classroom work</h2>
    </div>
    <div class="portfolio-grid reveal">
      <div class="portfolio-card">
        <div class="card-header card-h1">📚</div>
        <div class="card-body">
          <div class="card-tag">Reading Unit</div>
          <h3>Story Elements & Narrative Structure</h3>
          <p>A 3-week unit helping K–2 students identify characters, setting, and plot through interactive read-alouds, song, and student-created mini-books.</p>
        </div>
        <div class="card-footer">
          <span class="card-meta">Grades K–2 · 3 weeks</span>
          <a href="#" class="card-link">View lesson →</a>
        </div>
      </div>
      <div class="portfolio-card">
        <div class="card-header card-h2">✍️</div>
        <div class="card-body">
          <div class="card-tag">Writing Unit</div>
          <h3>My Story, My Voice — Personal Narratives</h3>
          <p>Grades 3–5 personal narrative unit using music and mentor texts to inspire authentic student writing. Includes graphic organizers, rubrics, and peer feedback tools.</p>
        </div>
        <div class="card-footer">
          <span class="card-meta">Grades 3–5 · 4 weeks</span>
          <a href="#" class="card-link">View lesson →</a>
        </div>
      </div>
      <div class="portfolio-card">
        <div class="card-header card-h3">🎵</div>
        <div class="card-body">
          <div class="card-tag">Music-Integrated</div>
          <h3>Phonics Through Song — Rhyme & Rhythm</h3>
          <p>A phonics program using original songs and chants to teach letter patterns, blends, and sight words to K–1 learners. Highly engaging for auditory learners.</p>
        </div>
        <div class="card-footer">
          <span class="card-meta">Grades K–1 · Ongoing</span>
          <a href="#" class="card-link">View lesson →</a>
        </div>
      </div>
      <div class="portfolio-card">
        <div class="card-header card-h4">🌟</div>
        <div class="card-body">
          <div class="card-tag">Student Project</div>
          <h3>Our Class Book — Collaborative Storytelling</h3>
          <p>Students co-author and illustrate a class storybook. Each child writes one page, developing voice, creativity, and pride in their work. Published digitally each year.</p>
        </div>
        <div class="card-footer">
          <span class="card-meta">All Grades · End of Year</span>
          <a href="#" class="card-link">View project →</a>
        </div>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section class="skills-section">
    <div class="reveal" style="text-align:center; max-width: 600px; margin: 0 auto;">
      <div class="section-label">Skills & Tools</div>
      <h2 class="section-title">What I bring to the classroom</h2>
    </div>
    <div class="skills-grid reveal">
      <div class="skill-item"><div class="skill-icon">📖</div><div class="skill-name">Guided Reading</div></div>
      <div class="skill-item"><div class="skill-icon">✏️</div><div class="skill-name">Writers' Workshop</div></div>
      <div class="skill-item"><div class="skill-icon">🎵</div><div class="skill-name">Music Integration</div></div>
      <div class="skill-item"><div class="skill-icon">🎭</div><div class="skill-name">Drama & Storytelling</div></div>
      <div class="skill-item"><div class="skill-icon">🖥️</div><div class="skill-name">Google Classroom</div></div>
      <div class="skill-item"><div class="skill-icon">🌈</div><div class="skill-name">Differentiated Instruction</div></div>
      <div class="skill-item"><div class="skill-icon">💬</div><div class="skill-name">Social-Emotional Learning</div></div>
      <div class="skill-item"><div class="skill-icon">🎨</div><div class="skill-name">Arts Integration</div></div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact-section" id="contact">
    <div class="reveal">
      <div class="section-label">Contact</div>
      <h2 class="section-title">Let's work together</h2>
      <p class="contact-subtitle">Whether you're a fellow educator, school administrator, or parent — I'd love to connect and share ideas.</p>
      <div class="contact-links">
        <a href="mailto:your@email.com" class="contact-chip">📧 your@email.com</a>
        <a href="https://github.com/your-username" class="contact-chip">🐙 GitHub</a>
        <a href="https://linkedin.com/in/your-profile" class="contact-chip">💼 LinkedIn</a>
        <a href="#" class="contact-chip">📄 Download CV</a>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer>
    <p>© 2026 <span>Toni Junior Deeb</span> · Built with GitHub Pages · Made with ❤️ and creativity</p>
  </footer>

  <script>
    // Scroll reveal
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
    }, { threshold: 0.12 });
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
  </script>
</body>
</html>
