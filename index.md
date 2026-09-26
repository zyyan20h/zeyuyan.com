---
layout: default
title: "Zeyu Yan"
---
<section class="home-hero-band">
  <div class="hero-bg">
    <img src="/assets/img/web-front.jpg" alt="">
    <img src="/assets/img/web-front.jpg" alt="">
    <img src="/assets/img/web-front.jpg" alt="">
  </div>
  <section class="home-hero">
    <div class="home-hero-left">
      <div class="home-hero-right">
        <img src="/assets/img/headshot.webp"
          alt="Portrait of Zeyu Yan"
          class="home-avatar">
        <h1 class="home-name">Zeyu Yan 燕泽宇</h1>
        <p class="home-affiliation">
          School of Interactive Computing, Georgia Tech
        </p>
        <p class="home-affiliation">
          School of Electrical and Computer Engineering, Georgia Tech
        </p>
        <p class="home-affiliation">
          Ulu Lāhui Foundation
        </p>
        <p class="home-title">
          Postdoctoral Research Fellow | Maker | Car Enthusiast
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
      <p class="home-hero-lead">
            I am a postdoctoral research fellow at the <a href="https://kamoamoa.com/">Hale Ao o Ka Moamoa</a> School of Interactive Computing, with a courtesy appointment in the School of Electrical and Computer Engineering at the Georgia Institute of Technology. I study <span class="home-bold">physical intelligence and fabrication</span>: how digital intelligence can be embodied in physical systems, and how those systems can be fabricated for ease of manufacture, customization, reconfiguration, and sustainability.
      </p>
      <p class="home-hero-sub">
            I develop <span class="home-bold">embodied intelligent physical systems</span> that enhance perception in XR, expand access to technology for marginalized communities, and support intuitive learning. I also develop <span class="home-bold">accessible, localized manufacturing processes</span> that embed reprogrammability, enabling physical systems to adapt in appearance, form, and function to different needs throughout their lifecycles.
          </p>
          <p class="home-hero-sub">
            Before joining Georgia Tech, I earned a Ph.D. in Computer Science from the University of Maryland, College Park, where I worked in the <a href="https://smartlab.cs.umd.edu/" target="_blank" rel="noopener noreferrer">Small Artifacts Lab</a>, and an M.S. in Mechanical Engineering from Carnegie Mellon University, where I worked in the <a href="https://morphingmatter.org/" target="_blank" rel="noopener noreferrer">Morphing Matter Lab</a>. My work has appeared in leading HCI and computer science venues, including ACM CHI and UIST.
          </p>
      <!-- <p class="home-hero-links">
        Explore my <a href="#publications">publications</a>,
        or learn more <a href="/about/">about me</a>.
      </p> -->
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
  </section>
</section>

<section class="home-news" id="news">
  <h2 class="home-news-title">News</h2>

  <ul class="home-news-list">
    {% assign visible_limit = 6 %}
    {% for item in site.data.news limit: visible_limit %}
      {% include news-item.html item=item %}
    {% endfor %}
  </ul>

  <p class="home-news-more">
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
  const imgs = Array.from(bg.querySelectorAll("img"));

  if (!bg || imgs.length === 0) return;

  let offset = 0;
  let speed = 1; // ← CHANGE THIS and it WILL change
  let imgWidth = 0;

  function setup() {
    imgWidth = imgs[0].getBoundingClientRect().width;
    const viewportWidth = window.innerWidth;

    // Ensure enough tiles to cover viewport + one extra
    let totalWidth = imgs.length * imgWidth;
    while (totalWidth < viewportWidth + imgWidth) {
      const clone = imgs[0].cloneNode(true);
      bg.appendChild(clone);
      imgs.push(clone);
      totalWidth += imgWidth;
    }

    animate();
  }

  function animate() {
    offset -= speed;

    // Wrap only when passing one full image
    if (offset <= -imgWidth) {
      offset += imgWidth;
    }

    bg.style.transform = `translateX(${offset}px)`;
    requestAnimationFrame(animate);
  }

  // Wait for image to load
  if (imgs[0].complete) {
    setup();
  } else {
    imgs[0].addEventListener("load", setup);
  }
});
</script>
