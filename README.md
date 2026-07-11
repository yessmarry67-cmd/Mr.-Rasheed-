<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdul-Rasheed | Developer Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background: #f2f5f9;
            color: #1e293b;
            line-height: 1.7;
            padding: 2rem;
            transition: background 0.3s, color 0.3s;
        }

        /* ---- DARK MODE ---- */
        body.dark-mode {
            background: #090f18;
            color: #e2e8f0;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            color: #000000;
            background: white;
            padding: 3rem 3.5rem;
            border-radius: 30px;
            box-shadow: 0 25px 50px -12px rgba(22, 22, 22, 0);
            transition: background 0.3s;
        }

        body.dark-mode .container {
            background: #000000;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
        }

        /* ---- HEADER ---- */
        .header {
            text-align: center;
            padding-bottom: 2.5rem;
            border-bottom: 2px solid #e9edf4;
            margin-bottom: 2.5rem;
            position: relative;
        }

        body.dark-mode .header {
            border-bottom-color: #334155;
        }

        .header-img-wrapper {
            display: inline-block;
            padding: 6px;
            border-radius: 50%;
            background: linear-gradient(135deg, #2563eb, #7c3aed);
            margin-bottom: 1.2rem;
        }

        .header img {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid white;
            display: block;
        }

        body.dark-mode .header img {
            border-color: #1e293b;
            background-color: #000000;
            color: white;
        }

        .header h1 {
            font-size: 3rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            color: #0f172a;
        }

        body.dark-mode .header h1 {
            color: #f1f5f9;
        }

        .header .badge {
            display: inline-block;
            background: #eef2ff;
            color: #2563eb;
            font-weight: 600;
            font-size: 1rem;
            padding: 0.4rem 1.4rem;
            border-radius: 40px;
            margin-top: 0.5rem;
        }

        body.dark-mode .badge {
            background: #1e293b;
            color: #60a5fa;
        }

        .header p {
            margin-top: 0.8rem;
            color: #64748b;
            font-size: 1.05rem;
        }

        body.dark-mode .header p {
            color: #94a3b8;
        }

        /* ---- DARK MODE TOGGLE ---- */
        .theme-toggle {
            position: absolute;
            top: 0;
            right: 0;
            background: none;
            border: none;
            font-size: 1.8rem;
            cursor: pointer;
            color: #2563eb;
            transition: 0.2s;
        }

        body.dark-mode .theme-toggle {
            color: #fbbf24;
        }

        /* ---- TYPING EFFECT ---- */
        .typing-text {
            color: #2563eb;
        }

        /* ---- SECTIONS ---- */
        .section { margin: 3rem 0; }

        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            color: #0f172a;
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 1.8rem;
            border-left: 6px solid #2563eb;
            padding-left: 1rem;
        }

        body.dark-mode .section-title {
            color: #f1f5f9;
        }

        .section-title i { color: #2563eb; font-size: 1.6rem; }

        /* ---- ABOUT ---- */
        .about-card {
            background: #f8fafc;
            padding: 2rem 2.5rem;
            border-radius: 24px;
            border: 1px solid #e9edf4;
            font-size: 1.05rem;
            color: #334155;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.04);
            transform: translateY(30px);
            opacity: 0;
            transition: all 0.6s ease;
        }

        body.dark-mode .about-card {
            background: #0f172a;
            border-color: #334155;
            color: #e2e8f0;
        }

        .about-card .quote {
            font-weight: 600;
            color: #2563eb;
            font-size: 1.1rem;
            margin-bottom: 1rem;
            display: block;
        }

        /* ---- SKILLS ---- */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background: white;
            padding: 1.5rem 1.8rem;
            border-radius: 20px;
            border: 1px solid #e9edf4;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.04);
            transition: all 0.25s ease;
            transform: translateY(30px);
            opacity: 0;
        }

        body.dark-mode .skill-card {
            background: #0f172a;
            border-color: #334155;
        }

        .skill-card:hover {
            border-color: #2563eb;
            box-shadow: 0 12px 24px -8px rgba(37, 99, 235, 0.12);
            transform: translateY(-4px);
        }

        .skill-card i {
            font-size: 1.6rem;
            color: #2563eb;
            margin-right: 12px;
            width: 32px;
        }

        .skill-card strong {
            display: block;
            font-size: 1.1rem;
            color: #0f172a;
            margin-bottom: 0.3rem;
        }

        body.dark-mode .skill-card strong {
            color: #f1f5f9;
        }

        .skill-card span {
            color: #64748b;
            font-size: 0.95rem;
            display: block;
            margin-top: 0.2rem;
        }

        body.dark-mode .skill-card span {
            color: #94a3b8;
        }

        /* ---- EXPERIENCE ---- */
        .exp-item {
            background: #f8fafc;
            padding: 1.5rem 2rem;
            border-radius: 20px;
            border-left: 6px solid #2563eb;
            margin-bottom: 1.2rem;
            border: 1px solid #e9edf4;
            border-left-width: 6px;
            transition: 0.2s;
            transform: translateX(-30px);
            opacity: 0;
        }

        body.dark-mode .exp-item {
            background: #0f172a;
            border-color: #334155;
        }

        .exp-item:hover { background: #f1f5f9; }

        body.dark-mode .exp-item:hover {
            background: #1e293b;
        }

        .exp-item h4 {
            font-size: 1.25rem;
            color: #0f172a;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        body.dark-mode .exp-item h4 {
            color: #f1f5f9;
        }

        .exp-item h4 i { color: #2563eb; }
        .exp-item p { color: #475569; margin-top: 0.4rem; }

        body.dark-mode .exp-item p {
            color: #cbd5e1;
        }

        .exp-item .highlight {
            color: #2563eb;
            font-weight: 600;
            margin-top: 0.6rem;
            display: block;
        }

        /* ---- PROJECTS ---- */
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: white;
            border-radius: 24px;
            border: 1px solid #e9edf4;
            padding: 1.8rem 1.8rem 2rem;
            text-align: center;
            transition: all 0.25s ease;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.04);
            transform: scale(0.95);
            opacity: 0;
        }

        body.dark-mode .project-card {
            background: #0f172a;
            border-color: #334155;
        }

        .project-card:hover {
            border-color: #2563eb;
            box-shadow: 0 20px 30px -10px rgba(37, 99, 235, 0.12);
            transform: translateY(-6px) scale(1);
        }

        .project-card img {
            width: 100%;
            height: 170px;
            object-fit: cover;
            border-radius: 16px;
            background: #e2e8f0;
            margin-bottom: 1.2rem;
        }

        body.dark-mode .project-card img {
            background: #334155;
        }

        .project-card h4 {
            font-size: 1.2rem;
            color: #0f172a;
        }

        body.dark-mode .project-card h4 {
            color: #f1f5f9;
        }

        .project-card p {
            color: #64748b;
            font-size: 0.95rem;
            margin-top: 0.3rem;
        }

        body.dark-mode .project-card p {
            color: #94a3b8;
        }

        /* ---- MESSAGE ---- */
        .message-box {
            background: linear-gradient(135deg, #eff6ff, #f0f4ff);
            padding: 2.5rem 3rem;
            border-radius: 30px;
            text-align: center;
            font-size: 1.2rem;
            font-style: italic;
            color: #1e293b;
            border: 1px solid #dbeafe;
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.05);
            transform: translateY(30px);
            opacity: 0;
        }

        body.dark-mode .message-box {
            background: linear-gradient(135deg, #1e293b, #0f172a);
            border-color: #334155;
            color: #e2e8f0;
        }

        .message-box strong {
            display: block;
            margin-top: 1rem;
            font-style: normal;
            font-weight: 700;
            color: #2563eb;
            font-size: 1.1rem;
        }

        body.dark-mode .message-box strong {
            color: #60a5fa;
        }

        /* ---- CONTACT ---- */
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
            background: #f8fafc;
            padding: 2rem 2.5rem;
            border-radius: 30px;
            border: 1px solid #e9edf4;
            transform: translateY(30px);
            opacity: 0;
        }

        body.dark-mode .contact-info {
            background: #0f172a;
            border-color: #334155;
        }

        .contact-info a, .contact-info span {
            color: #1e293b;
            text-decoration: none;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 1rem;
        }

        body.dark-mode .contact-info a, body.dark-mode .contact-info span {
            color: #e2e8f0;
        }

        .contact-info a:hover { color: #2563eb; }

        body.dark-mode .contact-info a:hover {
            color: #60a5fa;
        }

        .contact-info i {
            color: #2563eb;
            font-size: 1.3rem;
            width: 28px;
        }

        body.dark-mode .contact-info i {
            color: #60a5fa;
        }

        /* ---- FOOTER ---- */
        footer {
            text-align: center;
            padding: 2rem 0 0.5rem 0;
            margin-top: 3rem;
            border-top: 1px solid #e9eaf4;
            color: #64748b;
            font-size: 0.9rem;
        }

        body.dark-mode footer {
            border-top-color: #334155;
            color: #94a3b8;
        }

        footer .heart { color: #f43f5e; }

        /* ---- ANIMATION CLASS ---- */
        .visible {
            transform: translate(0) scale(1) !important;
            opacity: 1 !important;
        }

        /* ---- RESPONSIVE ---- */
        @media (max-width: 700px) {
            .container { padding: 1.8rem; }
            .header h1 { font-size: 2.2rem; }
            .message-box { padding: 1.8rem; font-size: 1rem; }
            .contact-info { flex-direction: column; align-items: center; text-align: center; }
        }
    </style>
</head>
<body>

<div class="container">

    <!-- HEADER -->
    <div class="header">
        <button class="theme-toggle" id="themeToggle">
            <i class="fas fa-moon"></i>
        </button>
        <div class="header-img-wrapper" width="200px">
            <img src="https://i.pinimg.com/736x/de/ad/06/dead065f08ba93f2502cec0ab8bf60ae.jpg" alt="Abdul-Rasheed">
        </div>
        <h1>Hello, I'm <span class="typing-text"></span></h1>
        <div class="badge"><i class="fas fa-code"></i> Developer &amp; Mentor</div>
        <p><i class="fas fa-map-pin"></i> Hyderabad, Pakistan</p>
    </div>

    <!-- ABOUT -->
    <div class="section">
        <div class="section-title">
            <i class="fas fa-user-circle"></i> About Him
        </div>
        <div class="about-card scroll-animate">
            <span class="quote">“A developer by profession, a teacher by heart, and a father above all.”</span>
            Mr. Abdul-Rasheed is a passionate developer with over 10 years of experience in the tech and creative industry. Known for his sharp problem-solving skills and his ability to teach complex ideas with patience and warmth, he has inspired many — both in the workplace and at home. 
            He believes that code is not just logic; it’s a language of creation. And beyond screens and servers, his greatest legacy is the values he passed on to his family.
        </div>
    </div>

    <!-- SKILLS -->
    <div class="section">
        <div class="section-title">
            <i class="fas fa-cogs"></i> Key Skills
        </div>
        <div class="skills-grid">
            <div class="skill-card scroll-animate"><i class="fas fa-code"></i><strong>Development</strong><span>HTML, CSS, JS, Bootstrap, Laravel, jQuery, SQL/MySQL, Full Stack</span></div>
            <div class="skill-card scroll-animate"><i class="fas fa-video"></i><strong>Editing</strong><span>Video/Photo Editing, Content Creation, UI/UX Design</span></div>
            <div class="skill-card scroll-animate"><i class="fas fa-users"></i><strong>Leadership</strong><span>Empathy, Clarity, Strong Decision-Making</span></div>
            <div class="skill-card scroll-animate"><i class="fas fa-chalkboard-teacher"></i><strong>Teaching &amp; Mentoring</strong><span>10+ years mentoring young developers &amp; students</span></div>
            <div class="skill-card scroll-animate"><i class="fas fa-microphone-alt"></i><strong>Acting &amp; Communication</strong><span>Natural Presenter, Storyteller, Communicator</span></div>
        </div>
    </div>

    <!-- EXPERIENCE -->
    <div class="section">
        <div class="section-title">
            <i class="fas fa-trophy"></i> Experience &amp; Achievements
        </div>
        <div class="exp-item scroll-animate">
            <h4><i class="fas fa-briefcase"></i> Experience</h4>
            <p>10+ years in software development &amp; IT solutions · Worked on business websites, educational platforms · Corporate &amp; freelance environments</p>
        </div>
        <div class="exp-item scroll-animate">
            <h4><i class="fas fa-award"></i> Awards</h4>
            <p>Best Developer (2005–2017 &amp; 2024–present) · Best Employee (Chandni / SRTC Mobile Market) · Best Teacher (Private School Principal)</p>
            <span class="highlight"><i class="fas fa-heart" style="color: #000000;"></i> “Best Father in the World” – given by his proud daughter, Jaja</span>
        </div>
    </div>

    <!-- PROJECTS -->
    <div class="section">
        <div class="section-title">
            <i class="fas fa-folder-open"></i> Sample Projects
        </div>
        <div class="project-grid">
            <div class="project-card scroll-animate">
                <img src="https://i.pinimg.com/736x/59/22/3a/59223a43e4c1c5bf299b69cb2dc40e0c.jpg" alt="E-Commerce">
                <h4><i class="fas fa-shopping-cart" style="color: #2563eb;"></i> E-Commerce Website</h4>
                <p>Full-featured online store with cart &amp; payment integration</p>
            </div>
            <div class="project-card scroll-animate">
                <img src="https://i.pinimg.com/736x/58/d8/a5/58d8a5a883c509cb3bb1652e5c4861bb.jpg" alt="Gaming">
                <h4><i class="fas fa-gamepad" style="color: #2563eb;"></i> Gaming Website</h4>
                <p>Interactive gaming portal with user profiles &amp; leaderboards</p>
            </div>
            <div class="project-card scroll-animate">
                <img src="https://i.pinimg.com/1200x/62/f8/8d/62f88d5bcc2d6d0b26e62534c7d4eec8.jpg" alt="Learning App">
                <h4><i class="fas fa-graduation-cap" style="color: #2563eb;"></i> Learning App</h4>
                <p>Educational platform for students and teachers</p>
            </div>
        </div>
    </div>

    <!-- MESSAGE -->
    <div class="section">
        <div class="section-title">
            <i class="fas fa-envelope" style="color: #2563eb;"></i> A Message from her daughter
        </div>
        <div class="message-box scroll-animate">
            “To my father — my first teacher, my biggest supporter, and the best developer I’ve ever known. You taught me that hard work and kindness go hand in hand. You’re not just a developer; you’re the builder of my world. I’m proud to be your daughter. I love you, Baba.”
            <strong>– Thank you <i class="fas fa-heart" style="color: #000000;"></i></strong>
        </div>
    </div>

    <!-- CONTACT -->
    <div class="section">
        <div class="section-title">
            <i class="fas fa-address-card"></i> Contact
        </div>
        <div class="contact-info scroll-animate">
            <span><i class="fas fa-envelope"></i> <a href="mailto:abdul-rasheed@gmail.com">abdul-rasheed@gmail.com</a></span>
            <span><i class="fas fa-phone-alt"></i> <a href="tel:03163964590">03163964590</a></span>
            <span><i class="fas fa-globe"></i> Portfolio Website (coming soon)</span>
            <span><i class="fas fa-map-marker-alt"></i> Hyderabad, Pakistan</span>
        </div>
    </div>

    <!-- FOOTER -->
    <footer>
        <p>Built with <span class="heart"></span> by Abdul-Rasheed</p>
        <p>&copy; 2026 Abdul-Rasheed. All rights reserved.</p>
    </footer>

</div>

<script>
    // ===== 1. DARK MODE TOGGLE =====
    const themeToggle = document.getElementById('themeToggle');
    themeToggle.addEventListener('click', () => {
        document.body.classList.toggle('dark-mode');
        const icon = themeToggle.querySelector('i');
        if (document.body.classList.contains('dark-mode')) {
            icon.className = 'fas fa-sun';
        } else {
            icon.className = 'fas fa-moon';
        }
    });

    // ===== 2. TYPING EFFECT =====
    const text = "Abdul-Rasheed";
    const typingElement = document.querySelector('.typing-text');
    let index = 0;

    function typeEffect() {
        if (index < text.length) {
            typingElement.textContent += text.charAt(index);
            index++;
            setTimeout(typeEffect, 100);
        }
    }
    typeEffect();

    // ===== 3. SCROLL REVEAL ANIMATION =====
    const animateElements = document.querySelectorAll('.scroll-animate');

    const revealOnScroll = () => {
        const windowHeight = window.innerHeight;
        const revealThreshold = 150;

        animateElements.forEach(element => {
            const rect = element.getBoundingClientRect();
            if (rect.top < windowHeight - revealThreshold) {
                element.classList.add('visible');
            }
        });
    };

    window.addEventListener('scroll', revealOnScroll);
    window.addEventListener('load', revealOnScroll);
</script>

</body>
</html>
