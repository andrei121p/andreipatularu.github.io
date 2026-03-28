---
layout: default
title: "MathMaiden"
---

<!-- Hero section -->
<section id="home" class="hero">
    <div class="container hero-content">
        <h1 class="hero-name">Andrei‑Eugeniu Pătularu</h1>
        <div class="hero-titles">
        </div>
        <p class="hero-description">
            Îmi pasionează matematica, programarea și educația. Lucrez la intersecția dintre teorie și aplicații practice,
            iar în timpul liber creez resurse open-source pentru pregătirea olimpiadelor, proiecte de analiză de date și
            vizualizare interactivă. Cred într-o matematică vie, accesibilă și mereu plină de curiozitate.
        </p>
        <a href="#about" class="btn-more">Mai multe despre mine <i class="fas fa-arrow-right"></i></a>
        <div class="social-icons">
            <a href="https://github.com/andrei121p" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
            <a href="https://www.linkedin.com/in/andrei-eugeniu-p%C4%83tularu-aa5b29241/" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        </div>
    </div>
</section>

<!-- About section – edit this freely -->
<section id="about" class="section">
    <div class="container">
        <h2 class="section-title">About me</h2>
        <div class="section-sub">Matematician, educator, programator</div>
        <p>Scrie aici povestea ta. Explică-ți backgroundul, pasiunile și ceea ce faci.</p>
    </div>
</section>

<!-- Articole Matematica section – shows posts with category "matematica" -->
<section id="articole-matematica" class="section">
    <div class="container">
        <h2 class="section-title">Articole Matematica</h2>
        <div class="section-sub">Resurse pentru liceu, olimpiadă și aplicații</div>

        <ul class="post-list">
            {% assign matematica_posts = site.posts | where: "category", "matematica" %}
            {% for post in matematica_posts limit:5 %}
            <li>
                <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
                <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b %Y" }}</time>
                <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
            </li>
            {% else %}
            <li>Niciun articol încă. Adaugă un post cu categoria "matematica".</li>
            {% endfor %}
        </ul>
        <p><a href="#" style="color: var(--primary);">Toate articolele →</a></p>
    </div>
</section>

<!-- Blog section – shows posts with category "blog" -->
<section id="blog" class="section">
    <div class="container">
        <h2 class="section-title">Blog</h2>
        <div class="section-sub">Reflecții, experimente, idei diverse</div>

        <ul class="post-list">
            {% assign blog_posts = site.posts | where: "category", "blog" %}
            {% for post in blog_posts limit:5 %}
            <li>
                <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
                <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b %Y" }}</time>
                <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
            </li>
            {% else %}
            <li>Niciun articol încă. Adaugă un post cu categoria "blog".</li>
            {% endfor %}
        </ul>
        <p><a href="#" style="color: var(--primary);">Toate articolele →</a></p>
    </div>
</section>
