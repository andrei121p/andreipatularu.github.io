<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MathMaiden — Andrei Patularu</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #fefcf7;
            color: #1e2a32;
            line-height: 1.5;
        }

        :root {
            --primary: #1f6e8c;
            --primary-dark: #0e4b64;
            --accent: #e76f51;
            --gray-light: #f0e5d8;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Header */
        .site-header {
            background: rgba(255, 250, 243, 0.96);
            backdrop-filter: blur(8px);
            border-bottom: 1px solid var(--gray-light);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 1rem 0;
        }

        .nav-wrapper {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .logo a {
            font-weight: 700;
            font-size: 1.4rem;
            text-decoration: none;
            color: var(--primary-dark);
        }

        .logo a:hover {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 1.8rem;
            list-style: none;
        }

        .nav-links a {
            text-decoration: none;
            font-weight: 500;
            color: #2c3e4e;
            font-size: 0.95rem;
            transition: 0.2s;
            border-bottom: 2px solid transparent;
            padding-bottom: 4px;
        }

        .nav-links a:hover {
            color: var(--primary);
            border-bottom-color: var(--accent);
        }

        /* Hero */
        .hero {
            padding: 4rem 0 5rem;
            background: linear-gradient(135deg, #fff6ed 0%, #fffef9 100%);
        }

        .hero-content {
            max-width: 800px;
        }

        .hero-name {
            font-size: 3.5rem;
            font-weight: 800;
            letter-spacing: -0.02em;
            color: #1a3a47;
            margin-bottom: 1rem;
        }

        .hero-titles {
            font-size: 1.1rem;
            font-weight: 600;
            color: #c45c2c;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1.5rem;
            border-left: 4px solid var(--accent);
            padding-left: 1rem;
        }

        .hero-description {
            font-size: 1.2rem;
            color: #2c3e4e;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        .btn-more {
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
            background: var(--primary);
            color: white;
            padding: 0.7rem 1.8rem;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 600;
            transition: 0.2s;
        }

        .btn-more:hover {
            background: var(--accent);
        }

        .social-icons {
            margin-top: 1.5rem;
        }

        .social-icons a {
            font-size: 1.5rem;
            color: #3f5e6b;
            margin-right: 1.2rem;
            transition: 0.2s;
        }

        .social-icons a:hover {
            color: var(--primary);
        }

        /* Sections */
        .section {
            padding: 4rem 0 3rem;
            border-bottom: 1px solid var(--gray-light);
        }

        .section-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            position: relative;
            display: inline-block;
        }

        .section-title:after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--accent);
        }

        .section-sub {
            color: #5f6c7a;
            margin-bottom: 2rem;
            font-size: 1rem;
        }

        /* Post list style */
        .post-list {
            list-style: none;
        }

        .post-list li {
            margin-bottom: 1.5rem;
            border-bottom: 1px solid #eee;
            padding-bottom: 1rem;
        }

        .post-list h3 {
            margin: 0;
        }

        .post-list time {
            color: #888;
            font-size: 0.85rem;
        }

        /* Footer */
        .footer {
            padding: 2rem 0;
            text-align: center;
            color: #8a7a6a;
            font-size: 0.85rem;
            border-top: 1px solid var(--gray-light);
        }

        @media (max-width: 768px) {
            .container { padding: 0 1.5rem; }
            .hero-name { font-size: 2.5rem; }
            .nav-links { gap: 1rem; }
        }
    </style>
</head>
<body>

<header class="site-header">
    <div class="container nav-wrapper">
        <div class="logo">
            <a href="#">MathMaiden</a>
        </div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#articole-matematica">Articole Matematica</a></li>
            <li><a href="#blog">Blog</a></li>
        </ul>
    </div>
</header>

<main>
    <!-- Hero section (home) – you can edit the text freely -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1 class="hero-name">Andrei‑Eugeniu Pătularu</h1>
            <div class="hero-titles">
                MATEMATICIAN | PROFESOR | PROGRAMATOR | OLIMPIADIC
            </div>
            <p class="hero-description">
                Îmi pasionează matematica, programarea și educația. Lucrez la intersecția dintre teorie și aplicații practice,
                iar în timpul liber creez resurse open-source pentru pregătirea olimpiadelor, proiecte de analiză de date și
                vizualizare interactivă. Cred într-o matematică vie, accesibilă și mereu plină de curiozitate.
            </p>
            <!-- Optional button – you can remove it if you want -->
            <a href="#about" class="btn-more">Mai multe despre mine <i class="fas fa-arrow-right"></i></a>
            <div class="social-icons">
                <a href="https://www.linkedin.com/in/andrei-eugeniu-p%C4%83tularu-aa5b29241/" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                <a href="https://github.com/andreipatularu" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
                <!-- add X/Twitter if you want -->
                <!-- <a href="#" aria-label="X"><i class="fab fa-x-twitter"></i></a> -->
            </div>
        </div>
    </section>

    <!-- About section – add your own content here -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About me</h2>
            <div class="section-sub">(Your subtitle, e.g. "Matematician, educator, programator")</div>
            <!-- =========================================== -->
            <!-- TODO: Replace this placeholder with your own about text. -->
            <!-- You can use paragraphs, lists, or any HTML you like. -->
            <p>Write your story here. Explain your background, interests, and what you do.</p>
            <!-- =========================================== -->
        </div>
    </section>

    <!-- Articole Matematica section – all math‑related posts go here -->
    <section id="articole-matematica" class="section">
        <div class="container">
            <h2 class="section-title">Articole Matematica</h2>
            <div class="section-sub">Resurse pentru liceu, olimpiadă și aplicații</div>

            <!-- =========================================== -->
            <!-- HOW TO ADD NEW POSTS:
                 1. Copy the entire <li> block below (including the <li> ... </li>).
                 2. Paste it right above the closing </ul> tag.
                 3. Update the title, date, and description.
            -->
            <ul class="post-list">
                <!-- Example post (you can delete this when you add your own) -->
                <li>
                    <h3><a href="#">Titlul primului articol de matematică</a></h3>
                    <time>28 Mar 2025</time>
                    <p>Un scurt rezumat. Poate include teoreme, probleme sau aplicații.</p>
                </li>
                <!-- Add more posts here -->
            </ul>
            <!-- =========================================== -->
            <p><a href="#" style="color: var(--primary);">Toate articolele →</a></p>
        </div>
    </section>

    <!-- Blog section – general / personal posts go here -->
    <section id="blog" class="section">
        <div class="container">
            <h2 class="section-title">Blog</h2>
            <div class="section-sub">Reflecții, experimente, idei diverse</div>

            <!-- =========================================== -->
            <!-- HOW TO ADD NEW POSTS:
                 1. Copy the entire <li> block below.
                 2. Paste it above the closing </ul> tag.
                 3. Change the title, date, and description.
            -->
            <ul class="post-list">
                <!-- Example blog post -->
                <li>
                    <h3><a href="#">Primul meu gând despre...</a></h3>
                    <time>28 Mar 2025</time>
                    <p>Un text scurt care să atragă cititorul. Poate fi despre programare, filosofie, sau orice altceva.</p>
                </li>
                <!-- Add more blog posts here -->
            </ul>
            <!-- =========================================== -->
            <p><a href="#" style="color: var(--primary);">Toate articolele →</a></p>
        </div>
    </section>
</main>

<footer class="footer">
    <div class="container">
        <p>© 2025 Andrei‑Eugeniu Pătularu</p>
    </div>
</footer>

</body>
</html>
