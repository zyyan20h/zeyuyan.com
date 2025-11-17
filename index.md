---
layout: default
title: "Zeyu Yan"
---


<section class="home-top">
  <div class="home-sidebar">
    <div class="home-top-left">
      <!-- Avatar will go here -->
      <img src="{{ '/assets/img/headshot.webp' | relative_url }}"
        alt="Portrait of Zeyu Yan"
        class="home-avatar">
    </div>

    <div class="home-top-middle">
      <h1 class="home-name">Zeyu Yan  燕泽宇</h1>
      <p class="home-affiliation">
        Computer Science, University of Maryland
      </p>
      <p class="home-title">
        HCI Ph.D. Candidate｜Maker | Car Enthusiast
      </p>
      

      <!-- Social icons will go here -->
      <div class="home-icons">

        <!-- Email -->
        <a href="mailto:zeyuy@umd.edu" class="icon-link" aria-label="Email">
          <img src="{{ '/assets/img/icons/email.svg' | relative_url }}" alt="Email" class="icon-img">
        </a>

        <!-- Google Scholar -->
        <a href="https://scholar.google.com/citations?hl=en&user=hZLGZQIAAAAJ"
          class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Google Scholar">
          <img src="{{ '/assets/img/icons/scholar.svg' | relative_url }}" alt="Google Scholar" class="icon-img">
        </a>

        <!-- LinkedIn -->
        <a href="https://www.linkedin.com/in/zeyu-yan"
          class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
          <img src="{{ '/assets/img/icons/linkedin.svg' | relative_url }}" alt="LinkedIn" class="icon-img">
        </a>

        <!-- CV -->
        <a href="{{ '/assets/files/Zeyu_Yan_CV.pdf' | relative_url }}"
          class="icon-link" target="_blank" rel="noopener noreferrer" aria-label="Curriculum Vitae">
          <img src="{{ '/assets/img/icons/cv.svg' | relative_url }}" alt="CV" class="icon-img">
        </a>

      </div>
    </div>
  </div>

  
  <p class="home-text">
    I am a Computer Science Ph.D. candidate at the 
    <a href="https://smartlab.cs.umd.edu/" target="_blank" rel="noopener noreferrer">
      Small Artifacts Lab
    </a> 
    in University of Maryland, College Park, advised by 
    <a href="https://huaishu.me/" target="_blank" rel="noopener noreferrer">Huaishu Peng</a>. 
    I work in the area of Digital Fabrication, Tangible User Interface, Accessibility, and Haptic Interaction. 
  </p>  

  <p class="home-text">
    <strong>I envision a future where Physical Matter can be reprogrammed as easy as digital bits, code, and pixels.</strong> To move toward this goal, I create computational methods, invent hardware systems, and design new material compositions that enable the making and transformation of interactive artifacts in both their physical form and function. My research draws from HCI, computer science, engineering, and materials science, integrating technical innovation with human-centered empirical inquiry and formative study.
    I have published my work in top-tier Human Computer Interaction (HCI) venues including ACM CHI and UIST and received multiple award and recognitions.
  </p>

  <p class="home-announcement">
    📣 <strong>I am actively seeking academic positions in HCI and related fields.</strong>
  </p>


  
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