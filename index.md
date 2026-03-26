<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Andrei Patularu — Matematică & Programare</title>
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

        /* Simple row style (replaces cards) */
        .row-list {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .row-item {
            border-bottom: 1px solid #f0e5d8;
            padding-bottom: 1rem;
        }

        .row-item h3 {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 0.25rem;
            color: var(--primary-dark);
        }

        .row-item p {
            color: #4a5b68;
            font-size: 0.95rem;
        }

        .row-item .meta {
            font-size: 0.8rem;
            color: #a18262;
            margin-top: 0.25rem;
        }

        /* Two‑column layout for the merged math section */
        .two-col {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .col h3 {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--primary-dark);
            border-left: 3px solid var(--accent);
            padding-left: 0.8rem;
        }

        .col ul {
            list-style: none;
            padding-left: 0;
        }

        .col li {
            margin-bottom: 1rem;
            border-bottom: 1px solid #f5ede5;
            padding-bottom: 0.75rem;
        }

        .col li strong {
            display: block;
            font-weight: 600;
            color: #1f3b44;
        }

        .col li span {
            font-size: 0.85rem;
            color: #7c6e5e;
        }

        /* Post list (like original) */
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

        /* Footer clean */
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
            .two-col { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>

<header class="site-header">
    <div class="container nav-wrapper">
        <div class="logo">
            <a href="#">Andrei Patularu</a>
        </div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#posts">Posts</a></li>
            <li><a href="#articole-matematica">Articole Matematica</a></li>
            <li><a href="#miscellaneous">Miscellaneous</a></li>
        </ul>
    </div>
</header>

<main>
    <!-- Hero -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1 class="hero-name">Andrei Patularu</h1>
            <div class="hero-titles">
                MATEMATICIAN | PROFESOR | PROGRAMATOR | OLIMPIADIC
            </div>
            <p class="hero-description">
                Îmi pasionează matematica, programarea și educația. Lucrez la intersecția dintre teorie și aplicații practice,
                iar în timpul liber creez resurse open-source pentru pregătirea olimpiadelor, proiecte de analiză de date și
                vizualizare interactivă. Cred într-o matematică vie, accesibilă și mereu plină de curiozitate.
            </p>
            <a href="#about" class="btn-more">Mai multe despre mine <i class="fas fa-arrow-right"></i></a>
            <div class="social-icons">
                <a href="#" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" aria-label="GitHub"><i class="fab fa-github"></i></a>
                <a href="#" aria-label="X"><i class="fab fa-x-twitter"></i></a>
            </div>
        </div>
    </section>

    <!-- About -->
    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About me</h2>
            <div class="section-sub">Matematician, educator și pasionat de cod</div>
            <div class="row-list">
                <div class="row-item">
                    <h3>Research & teaching</h3>
                    <p>Doctorand în statistică cu focus pe procese stochastice. Pasionat să fac matematica avansată accesibilă prin exemple din lumea reală și predare interactivă.</p>
                </div>
                <div class="row-item">
                    <h3>Quant & coding</h3>
                    <p>Dezvoltator cantitativ, construind modele pentru risc, derivate și trading algoritmic. Cod curat și matematică riguroasă.</p>
                </div>
                <div class="row-item">
                    <h3>Open source & community</h3>
                    <p>Creator de biblioteci Python/Julia pentru vizualizare, optimizare și probleme de tip olimpiadă. Toate resursele sunt gratuite.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Posts -->
    <section id="posts" class="section">
        <div class="container">
            <h2 class="section-title">Latest Posts</h2>
            <div class="section-sub">Idei noi, probleme interesante și reflecții despre matematică și programare</div>
            <ul class="post-list">
                <li>
                    <h3><a href="#">Primul meu articol</a></h3>
                    <time>26 Mar 2025</time>
                    <p>Un scurt rezumat al articolului.</p>
                </li>
            </ul>
            <p><a href="#" style="color: var(--primary);">Toate articolele →</a></p>
        </div>
    </section>

    <!-- Articole Matematica (merged section) -->
    <section id="articole-matematica" class="section">
        <div class="container">
            <h2 class="section-title">Articole Matematica</h2>
            <div class="section-sub">Resurse pentru liceu, olimpiadă și aplicații ale matematicii</div>
            <div class="two-col">
                <div class="col">
                    <h3>Liceu & Olimpiadă</h3>
                    <ul>
                        <li><strong>Algebră & Analiză</strong> — Inegalități, ecuații funcționale, limite, integrale <span>teorie + probleme</span></li>
                        <li><strong>Geometrie (sintetică, vectorială, complexe)</strong> — Configurații remarcabile, puterea punctului, transformări <span>probleme rezolvate</span></li>
                        <li><strong>Teoria numerelor & Combinatorică</strong> — Congruențe, invarianți, numere prime, probleme de numărare <span>olimpiadă națională</span></li>
                        <li><strong>Lecții interactive + foi de lucru</strong> — Materiale pentru clasele IX–XII și pregătire avansată <span>PDF & cod sursă</span></li>
                    </ul>
                </div>
                <div class="col">
                    <h3>Aplicații ale matematicii</h3>
                    <ul>
                        <li><strong>Quantitative Finance</strong> — Stochastic calculus, risk management, algorithmic strategies (notebooks, modele live)</li>
                        <li><strong>Optimization & Machine Learning</strong> — Gradient descent, convex optimisation, neural networks</li>
                        <li><strong>Data Science & Visualisation</strong> — Statistical inference, Bayesian methods, storytelling cu Plotly/D3</li>
                    </ul>
                </div>
            </div>
            <div style="margin-top: 1.5rem; text-align: right;">
                <a href="#" style="color: var(--primary); font-weight: 500;">Acces arhivă completă <i class="fas fa-arrow-right"></i></a>
            </div>
        </div>
    </section>

    <!-- Miscellaneous (corrected spelling, no boxes) -->
    <section id="miscellaneous" class="section">
        <div class="container">
            <h2 class="section-title">Miscellaneous</h2>
            <div class="section-sub">Proiecte diverse, experimente vizuale și unelte open-source</div>
            <div class="row-list">
                <div class="row-item">
                    <h3>Math + Art</h3>
                    <p>Generative art, L-systems, chaotic attractors — unde codul întâlnește estetica.</p>
                </div>
                <div class="row-item">
                    <h3>Educational bots</h3>
                    <p>Telegram & Discord bots care rezolvă integrale, desenează funcții și explică teoreme.</p>
                </div>
                <div class="row-item">
                    <h3>Unconventional reads</h3>
                    <p>Book notes, philosophy of math, and essays on productivity for researchers.</p>
                </div>
            </div>
            <div style="margin-top: 2rem; background: #fbf5ea; border-radius: 40px; padding: 1rem 1.5rem;">
                <i class="fab fa-github"></i> <strong>github.com/andreipatularu</strong> — cod sursă pentru toate proiectele open-source
            </div>
        </div>
    </section>
</main>

<footer class="footer">
    <div class="container">
        <p>© 2025 · Toate resursele sunt liber accesibile</p>
    </div>
</footer>

</body>
</html>
