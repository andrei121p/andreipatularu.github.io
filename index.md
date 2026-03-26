---
layout: default
title: "Andrei Patularu"
---

<!-- Hero section -->
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

<!-- About section -->
<section id="about" class="section">
    <div class="container">
        <h2 class="section-title">About me</h2>
        <div class="section-sub">Matematician, educator și pasionat de cod</div>
        <div class="card-grid">
            <div class="card">
                <i class="fas fa-chalkboard-user" style="font-size: 2rem; color: #e76f51;"></i>
                <h3>Research & teaching</h3>
                <p>Doctorand în statistică cu focus pe procese stochastice. Pasionat să fac matematica avansată accesibilă prin exemple din lumea reală și predare interactivă.</p>
            </div>
            <div class="card">
                <i class="fas fa-chart-line" style="font-size: 2rem; color: #2a9d8f;"></i>
                <h3>Quant & coding</h3>
                <p>Dezvoltator cantitativ, construind modele pentru risc, derivate și trading algoritmic. Cod curat și matematică riguroasă.</p>
            </div>
            <div class="card">
                <i class="fas fa-heart" style="font-size: 2rem; color: #f4a261;"></i>
                <h3>Open source & community</h3>
                <p>Creator de biblioteci Python/Julia pentru vizualizare, optimizare și probleme de tip olimpiadă. Toate resursele sunt gratuite.</p>
            </div>
        </div>
    </div>
</section>

<!-- Posts section – this will automatically list your blog posts -->
<section id="posts" class="section">
    <div class="container">
        <h2 class="section-title">Latest Posts</h2>
        <div class="section-sub">Idei noi, probleme interesante și reflecții despre matematică și programare</div>
        <ul class="post-list">
            {% for post in site.posts limit:3 %}
            <li>
                <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
                <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b %Y" }}</time>
                <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
            </li>
            {% endfor %}
        </ul>
        <p><a href="{{ '/posts/' | relative_url }}" style="color: var(--primary);">Toate articolele →</a></p>
    </div>
</section>

<!-- Matematica de liceu & olimpiada -->
<section id="matematica" class="section">
    <div class="container">
        <h2 class="section-title">Matematica de liceu & olimpiada</h2>
        <div class="section-sub">Resurse, probleme și metode pentru performanță în matematică</div>
        <div class="resource-list">
            <div class="resource-item">
                <i class="fas fa-square-root-alt"></i>
                <span><strong>Algebră & Analiză</strong> — Inegalități, ecuații funcționale, limite, integrale</span>
                <small>teorie + probleme</small>
            </div>
            <div class="resource-item">
                <i class="fas fa-shapes"></i>
                <span><strong>Geometrie sintetică & vectorială</strong> — Configurații remarcabile, puterea punctului, transformări</span>
                <small>probleme rezolvate</small>
            </div>
            <div class="resource-item">
                <i class="fas fa-dice-d6"></i>
                <span><strong>Teoria numerelor & combinatorică</strong> — Congruențe, invarianți, numere prime, probleme de numărare</span>
                <small>olimpiadă națională</small>
            </div>
            <div class="resource-item">
                <i class="fas fa-chalkboard"></i>
                <span><strong>Lecții interactive + foi de lucru</strong> — Materiale pentru clasele IX-XII și pregătire avansată</span>
                <small>PDF & cod sursă</small>
            </div>
        </div>
        <div style="margin-top: 1.5rem; text-align: right;">
            <a href="#" style="color: var(--primary); font-weight: 500;">Acces arhivă completă <i class="fas fa-arrow-right"></i></a>
        </div>
    </div>
</section>

<!-- Applications of Math -->
<section id="applications" class="section">
    <div class="container">
        <h2 class="section-title">Applications of Math</h2>
        <div class="section-sub">Where theory meets reality — quantitative finance, AI, engineering</div>
        <div class="card-grid">
            <div class="card">
                <i class="fas fa-chart-line" style="font-size: 2rem; color: #1f6e8c;"></i>
                <h3>Quantitative Finance</h3>
                <p>Stochastic calculus, risk management, algorithmic strategies — notebooks and live models.</p>
            </div>
            <div class="card">
                <i class="fas fa-microchip" style="font-size: 2rem; color: #1f6e8c;"></i>
                <h3>Optimization & ML</h3>
                <p>Gradient descent, convex optimisation, and neural networks from a mathematical lens.</p>
            </div>
            <div class="card">
                <i class="fas fa-database" style="font-size: 2rem; color: #1f6e8c;"></i>
                <h3>Data Science & Visualisation</h3>
                <p>Statistical inference, Bayesian methods, and beautiful visual storytelling with Plotly/D3.</p>
            </div>
        </div>
    </div>
</section>

<!-- Misceláneos -->
<section id="misc" class="section">
    <div class="container">
        <h2 class="section-title">Misceláneos</h2>
        <div class="section-sub">Curiosity-driven projects, visual experiments & open-source tools</div>
        <div class="card-grid">
            <div class="card">
                <i class="fas fa-cubes" style="font-size: 2rem; color: #1f6e8c;"></i>
                <h3>Math + Art</h3>
                <p>Generative art, L-systems, and chaotic attractors — where code meets creativity.</p>
                <div><span class="tag">creative coding</span></div>
            </div>
            <div class="card">
                <i class="fas fa-robot" style="font-size: 2rem; color: #1f6e8c;"></i>
                <h3>Educational bots</h3>
                <p>Telegram & Discord bots that solve integrals, plot functions, and explain theorems.</p>
            </div>
            <div class="card">
                <i class="fas fa-glasses" style="font-size: 2rem; color: #1f6e8c;"></i>
                <h3>Unconventional reads</h3>
                <p>Book notes, philosophy of math, and essays on productivity for researchers.</p>
            </div>
        </div>
        <div style="margin-top: 2rem; background: #fbf5ea; border-radius: 40px; padding: 1rem 1.5rem; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap;">
            <span><i class="fab fa-github"></i> <strong>github.com/andreipatularu</strong> — cod sursă pentru toate proiectele open-source</span>
            <a href="#" style="color: var(--primary); font-weight: 500;">explorează <i class="fas fa-external-link-alt"></i></a>
        </div>
    </div>
</section>
