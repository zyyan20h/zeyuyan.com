---
layout: default
title: "Zeyu Yan"
---
<section class="home-hero-band">
  <div class="hero-bg">
    <img src="/assets/img/web-front.jpg" alt="">
    <img src="/assets/img/web-front.jpg" alt="">
  </div>
  <section class="home-hero">
    <div class="home-hero-left">
      <p class="home-hero-lead">
          I study physical interaction, specifically how smart hardware systems are built, evolve, and enable novel and impactful interaction experiences.
      </p>
      <p class="home-hero-sub">
          My work centers on <span class="home-bold">reprogramming physical matters</span> beyond their original form and function. Physical artifacts are typically rigid once produced, with their geometry and functionality tightly coupled to the creation processes, making post-production modification difficult. By exploring <span class="home-bold">novel materials</span>, <span class="home-bold">fabrication methods</span>, <span class="home-bold">design strategies</span>, and <span class="home-bold">system architectures</span>, I investigate how interactive hardware can remain adaptable over time. Such reprogrammability supports longer-lasting devices with on-demand upgrades, reduce production and logistics overhead, and develop longer-term relationships between human and physical matters.
      </p>
      <p class="home-hero-sub">
          My research also examines how physical interaction can reshape how people perceive, access, and engage with the world. I develop haptic and embodied interaction systems in extended reality, and tangible interfaces that serve as accessible physical extensions. I also explore physical interaction through robotic systems.
      </p>
      <p class="home-hero-links">
        Explore my <a href="#publications">publications</a>,
        or learn more <a href="/about/">about me</a>.
      </p>
      <p class="home-announcement">
        📣 I am actively seeking academic positions in HCI and related fields.
      </p>
      <!-- <div class="home-link-divider">
      </div>
      <p class="home-hero-links">
        <a href="mailto:zeyuy@umd.edu" class="home-link">Email</a>
        <a href="https://scholar.google.com/citations?hl=en&user=hZLGZQIAAAAJ" class="home-link">Google Scholar</a> 
        <a href="https://www.linkedin.com/in/zeyu-yan" class="home-link">Linkedin</a>
        <a href="/asset/files/Zeyu_Yan_CV.pdf" class="home-link">CV</a>
      </p> -->
    </div>
    <!-- <div class="home-hero-right">
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
    </div> -->
    <!-- <p class="home-announcement">
        📣 I am actively seeking academic positions in HCI and related fields.
    </p> -->
  </section>
</section>

<section class="home-news" id="news">
  <h2 class="news-title">News</h2>

  <ul class="news-list">
    {% assign visible_limit = 4 %}
    {% for item in site.data.news limit: visible_limit %}
      {% include news-item.html item=item %}
    {% endfor %}
  </ul>

  <p class="news-more">
    <a href="/news/">More news →</a>
  </p>
</section>


<section class="home-publications" id="publications">
  <h2 class="pub-title-section">Publications</h2>

  {% for pub in site.data.publications %}
    {% include pub-item.html pub=pub %}
  {% endfor %}
</section>

<script>
  document.addEventListener("DOMContentLoaded", () => {
    const bg = document.querySelector(".hero-bg");
    const imgs = bg.querySelectorAll("img");

    let offset = 0;
    const speed = 0.8; // px per frame (tune this)

    function animate() {
      const imgWidth = imgs[0].getBoundingClientRect().width;

      offset -= speed;

      if (-offset >= imgWidth) {
        offset += imgWidth;
      }

      bg.style.transform = `translateX(${offset}px)`;
      requestAnimationFrame(animate);
    }

    // respect reduced motion
    if (!window.matchMedia("(prefers-reduced-motion: reduce)").matches) {
      animate();
    }
  });
</script>

include float-back.html