---
layout: default
title: "Zeyu Yan"
---
<section class="home-hero-band">
  <section class="home-hero">
    <div class="home-hero-left">
      <p class="home-hero-lead">
          I study how physical objects can be reprogrammed as adaptable as digital information.
      </p>

      <p class="home-hero-sub">
      
          My research explores how interactive systems can be created so that they are easy to make, modify, and repurpose on demand. <br>
          My work brings together computing, engineering, and design, with a focus on accessibility, education, and sustainable technology. I develop new fabrication methods and interactive systems that lower barriers to creating physical artifacts and support more inclusive and responsible ways of building technology.
      </p>

      <p class="home-hero-links">
        Explore my <a href="#publications">publications</a>,
        or learn <a href="/about/">about me</a>.
      </p>
    </div>

    <div class="home-hero-right">
      <img src="/assets/img/headshot.webp"
        alt="Portrait of Zeyu Yan"
        class="home-avatar">

      <h1 class="home-name">Zeyu Yan 燕泽宇</h1>

      <p class="home-affiliation">
        Computer Science, University of Maryland
      </p>

      <p class="home-title">
        HCI Ph.D. Candidate｜Maker | Car Enthusiast
      </p>

      <div class="home-icons">
        <a href="mailto:zeyuy@umd.edu" class="icon-link" aria-label="Email">
          <img src="/assets/img/icons/email.svg" alt="Email" class="icon-img">
        </a>

        <a href="https://scholar.google.com/citations?hl=en&user=hZLGZQIAAAAJ"
          class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar">
          <img src="/assets/img/icons/scholar.svg" alt="Google Scholar" class="icon-img">
        </a>

        <a href="https://www.linkedin.com/in/zeyu-yan"
          class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
          <img src="/assets/img/icons/linkedin.svg" alt="LinkedIn" class="icon-img">
        </a>

        <a href="/assets/files/Zeyu-Yan-CV.pdf"
          class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Curriculum Vitae">
          <img src="/assets/img/icons/cv.svg" alt="CV" class="icon-img">
        </a>
      </div>
    </div>
  </section>
</section>

<!-- <section class="home-news">
  <h2 class="news-title">News</h2>

  <ul class="news-list" id="news-visible">
    {% assign visible_limit = 4 %}
    {% for item in site.data.news %}
      {% if forloop.index <= visible_limit %}
        {% include news-item.html item=item %}
      {% endif %}
    {% endfor %}
  </ul>

  <div class="news-hidden" id="news-hidden">
    <ul class="news-list">
      {% for item in site.data.news %}
        {% if forloop.index > visible_limit %}
          {% include news-item.html item=item %}
        {% endif %}
      {% endfor %}
    </ul>
  </div>

  <button class="news-toggle" type="button" onclick="toggleNews()">Show more ▼</button>
</section> -->


<section class="home-publications">
  <h2 class="pub-title-section">Publications</h2>

  {% for pub in site.data.publications %}
    {% include pub-item.html pub=pub %}
  {% endfor %}
</section>