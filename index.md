---
permalink: /
title: "Boisvert Wildfire Intelligence Lab"
author_profile: true
---

Welcome to the Boisvert Wildfire Intelligence Lab at the University of Alberta.

Our interdisciplinary research develops machine learning and remote sensing methods
that address challenges in forestry, wildfire science, wildfire preparedness, and
wildfire response. We aim to create innovative solutions that enable and support
informed decision-making for communities preparing for wildfire, emergency responders
managing wildfire events, and organizations responsible for protecting people,
infrastructure, and our natural resources.

<div class="research-slideshow" id="research-slideshow">
  <div class="slideshow-track">
    {% assign research_images = site.static_files | where_exp: "file", "file.path contains '/images/research/'" %}
    {% for image in research_images %}
      <img src="{{ image.path | relative_url }}" alt="Research figure" class="slide{% if forloop.first %} active{% endif %}">
    {% endfor %}
  </div>
  <button class="slide-arrow slide-arrow-left" aria-label="Previous slide">&#10094;</button>
  <button class="slide-arrow slide-arrow-right" aria-label="Next slide">&#10095;</button>
</div>

<style>
.research-slideshow {
  position: relative;
  width: 100%;
  max-width: 800px;
  margin: 1.5rem auto;
  overflow: hidden;
  background: #111;
  border-radius: 6px;
}

.slideshow-track {
  position: relative;
  width: 100%;
}

/* Images control their own height */
.slide {
  display: block;
  width: 100%;
  height: auto;
  object-fit: initial;

  opacity: 0;
  transition: opacity 0.6s ease;

  position: absolute;
  top: 0;
  left: 0;
}

/* active slide */
.slide.active {
  opacity: 1;
  position: relative;
}

.slide-arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0, 0, 0, 0.4);
  color: #fff;
  border: none;
  font-size: 1.5rem;
  padding: 0.5rem 0.8rem;
  cursor: pointer;
  border-radius: 4px;
}

.slide-arrow:hover {
  background: rgba(0, 0, 0, 0.7);
}

.slide-arrow-left {
  left: 10px;
}

.slide-arrow-right {
  right: 10px;
}
</style>

<script>
(function () {
  var container = document.getElementById('research-slideshow');
  var slides = container.querySelectorAll('.slide');
  var current = 0;
  var intervalTime = 5000;
  var timer;

  function showSlide(index) {
    slides[current].classList.remove('active');
    current = (index + slides.length) % slides.length;
    slides[current].classList.add('active');
  }

  function nextSlide() {
    showSlide(current + 1);
  }

  function prevSlide() {
    showSlide(current - 1);
  }

  function resetTimer() {
    clearInterval(timer);
    timer = setInterval(nextSlide, intervalTime);
  }

  container.querySelector('.slide-arrow-right').addEventListener('click', function () {
    nextSlide();
    resetTimer();
  });

  container.querySelector('.slide-arrow-left').addEventListener('click', function () {
    prevSlide();
    resetTimer();
  });

  if (slides.length > 1) {
    resetTimer();
  }
})();
</script>

## Contact Us
We welcome and invite collaboration inquiries and prospective students to contact us at [email placeholder].

## Acknowledgements

Our research is supported by the following funding organizations.

<div class="funder-logos">
  <img src="{{ '/images/nserc.png' | relative_url }}" alt="NSERC">
  <img src="{{ '/images/csa.png' | relative_url }}" alt="Canadian Space Agency">
  <img src="{{ '/images/abi.png' | relative_url }}" alt="Alberta Innovates">
  <img src="{{ '/images/nrcan.png' | relative_url }}" alt="Natural Resources Canada">
</div>

<style>
.funder-logos {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  margin: 1.5rem 0;
}

.funder-logos img {
  height: 80px;
  width: auto;
  max-width: 160px;
  object-fit: contain;
}
</style>