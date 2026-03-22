---
layout: single
title: " "
permalink: /photography/
author_profile: false
---

<style>

/* ==================
   Hero Header
   ================== */
.photo-hero {
  width: 100%;
  height: 60vh;
  background-image: url('/images/photography/hero.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 3em;
  position: relative;
}

.photo-hero::before {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.45);
}

.photo-hero-text {
  position: relative;
  text-align: center;
  color: white;
  z-index: 1;
  padding: 2em;
}

.photo-hero-text h1 {
  font-size: 3em;
  font-weight: 300;
  letter-spacing: 8px;
  text-transform: uppercase;
  margin-bottom: 0.3em;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
}

.photo-hero-text p {
  font-size: 1.1em;
  font-weight: 300;
  letter-spacing: 3px;
  font-style: italic;
  text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
}

/* ==================
   Section Title
   ================== */
.section-title {
  text-align: center;
  font-size: 0.85em;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: #888;
  margin: 3em 0 0.5em 0;
  position: relative;
}

.section-title::before,
.section-title::after {
  content: '';
  display: inline-block;
  width: 60px;
  height: 1px;
  background: #ccc;
  vertical-align: middle;
  margin: 0 15px;
}

.section-desc {
  text-align: center;
  font-size: 0.85em;
  color: #aaa;
  font-style: italic;
  margin-bottom: 1.5em;
  letter-spacing: 1px;
}

/* ==================
   Masonry Grid
   ================== */
.masonry-grid {
  columns: 3;
  column-gap: 12px;
  margin-bottom: 3em;
}

@media screen and (max-width: 900px) {
  .masonry-grid { columns: 2; }
}

@media screen and (max-width: 500px) {
  .masonry-grid { columns: 1; }
}

.masonry-item {
  break-inside: avoid;
  margin-bottom: 12px;
  position: relative;
  overflow: hidden;
  border-radius: 4px;
  cursor: pointer;
}

.masonry-item img {
  width: 100%;
  display: block;
  transition: transform 0.6s ease;
  border-radius: 4px;
}

.masonry-item:hover img {
  transform: scale(1.06);
}

/* ==================
   Caption Overlay
   ================== */
.masonry-caption {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(
    to top,
    rgba(0,0,0,0.80) 0%,
    rgba(0,0,0,0) 100%
  );
  color: white;
  padding: 2.5em 1em 1em;
  opacity: 0;
  transition: opacity 0.4s ease;
  border-radius: 0 0 4px 4px;
}

.masonry-item:hover .masonry-caption {
  opacity: 1;
}

.masonry-caption p {
  margin: 0;
  font-size: 0.82em;
  font-style: italic;
  letter-spacing: 0.5px;
  color: white !important;
  line-height: 1.4;
}

.masonry-caption span {
  display: block;
  font-size: 0.68em;
  letter-spacing: 2px;
  text-transform: uppercase;
  opacity: 0.8;
  color: #ddd;
  margin-bottom: 4px;
}

/* ==================
   Lightbox
   ================== */
.lightbox-overlay {
  display: none;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.96);
  z-index: 9999;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.lightbox-overlay.active {
  display: flex;
}

.lightbox-overlay img {
  max-width: 85vw;
  max-height: 78vh;
  object-fit: contain;
  border-radius: 2px;
  box-shadow: 0 0 80px rgba(0,0,0,0.9);
}

.lightbox-meta {
  text-align: center;
  margin-top: 1.2em;
  padding: 0 1em;
}

.lightbox-location {
  display: block;
  font-size: 0.7em;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #aaa;
  margin-bottom: 5px;
}

.lightbox-caption {
  color: white;
  font-style: italic;
  font-size: 0.95em;
  letter-spacing: 0.5px;
  opacity: 0.85;
  max-width: 600px;
  margin: 0 auto;
}

.lightbox-year {
  display: block;
  font-size: 0.7em;
  color: #666;
  margin-top: 6px;
  letter-spacing: 2px;
}

.lightbox-close {
  position: absolute;
  top: 20px;
  right: 30px;
  color: white;
  font-size: 2em;
  cursor: pointer;
  opacity: 0.6;
  transition: opacity 0.2s;
  background: none;
  border: none;
  line-height: 1;
}

.lightbox-close:hover { opacity: 1; }

.lightbox-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  color: white;
  font-size: 3em;
  cursor: pointer;
  opacity: 0.4;
  transition: opacity 0.2s;
  background: none;
  border: none;
  padding: 0.3em 0.6em;
  font-weight: 100;
}

.lightbox-nav:hover { opacity: 1; }
.lightbox-prev { left: 10px; }
.lightbox-next { right: 10px; }

.lightbox-counter {
  position: absolute;
  top: 25px;
  left: 30px;
  color: #666;
  font-size: 0.75em;
  letter-spacing: 2px;
}

/* ==================
   Section Nav Tabs
   ================== */
.section-tabs {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin: 2em 0 3em;
  flex-wrap: wrap;
}

.section-tab {
  padding: 8px 20px;
  font-size: 0.75em;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #888;
  border: 1px solid #ddd;
  border-radius: 30px;
  cursor: pointer;
  text-decoration: none;
  transition: all 0.3s ease;
}

.section-tab:hover {
  color: #333;
  border-color: #999;
  text-decoration: none;
}

/* ==================
   Instagram Button
   ================== */
.insta-link {
  text-align: center;
  margin: 1em 0 4em;
}

.insta-btn {
  display: inline-block;
  background: linear-gradient(
    45deg,
    #f09433, #e6683c,
    #dc2743, #cc2366, #bc1888
  );
  color: white !important;
  padding: 12px 30px;
  border-radius: 30px;
  text-decoration: none !important;
  font-size: 0.8em;
  letter-spacing: 3px;
  text-transform: uppercase;
  transition: transform 0.3s ease,
              box-shadow 0.3s ease;
  box-shadow: 0 4px 15px rgba(220,39,67,0.3);
}

.insta-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(220,39,67,0.5);
}

</style>

<!-- ==================
     Hero Section
     ================== -->
<div class="photo-hero">
  <div class="photo-hero-text">
    <h1>Through My Lens</h1>
    <p>Treks &nbsp;·&nbsp; Travels &nbsp;·&nbsp; 
       Wildlife &nbsp;·&nbsp; Nature &nbsp;·&nbsp; 
       People</p>
  </div>
</div>

<!-- ==================
     Section Jump Tabs
     ================== -->
<div class="section-tabs">
  <a href="#treks" class="section-tab">🏔️ &nbsp; Treks</a>
  <a href="#travels" class="section-tab">🌍 &nbsp; Travels</a>
  <a href="#wildlife" class="section-tab">🦅 &nbsp; Wildlife</a>
  <a href="#nature" class="section-tab">🌿 &nbsp; Nature</a>
  <a href="#human" class="section-tab">🧍 &nbsp; Human Emotions</a>
</div>

<!-- ==================
     Lightbox
     ================== -->
<div class="lightbox-overlay" id="lightbox">
  <button class="lightbox-close" onclick="closeLightbox()">✕</button>
  <button class="lightbox-nav lightbox-prev" onclick="changePhoto(-1)">&#8249;</button>
  <div class="lightbox-counter" id="lightbox-counter"></div>
  <img id="lightbox-img" src="" alt="">
  <div class="lightbox-meta">
    <span class="lightbox-location" id="lightbox-location"></span>
    <div class="lightbox-caption" id="lightbox-caption"></div>
    <span class="lightbox-year" id="lightbox-year"></span>
  </div>
  <button class="lightbox-nav lightbox-next" onclick="changePhoto(1)">&#8250;</button>
</div>

<!-- ==================
     Treks Section
     ================== -->
<div id="treks"></div>
<div class="section-title">🏔️ &nbsp; Treks</div>
<p class="section-desc">High passes, glacial moraines and silences that only mountains know</p>

<div class="masonry-grid">
{% assign trek_start = 0 %}
{% for photo in site.data.photography.treks %}
  <div class="masonry-item" onclick="openLightbox({{ trek_start | plus: forloop.index0 }})">
    <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
    <div class="masonry-caption">
      <span>{{ photo.location }}</span>
      <p>{{ photo.caption }}</p>
    </div>
  </div>
{% endfor %}
</div>

<!-- ==================
     Travels Section
     ================== -->
<div id="travels"></div>
<div class="section-title">🌍 &nbsp; Travels</div>
<p class="section-desc">From Himalayan valleys to European cobblestones and American skylines</p>

<div class="masonry-grid">
{% assign travel_start = site.data.photography.treks | size %}
{% for photo in site.data.photography.travels %}
  <div class="masonry-item" onclick="openLightbox({{ travel_start | plus: forloop.index0 }})">
    <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
    <div class="masonry-caption">
      <span>{{ photo.location }}</span>
      <p>{{ photo.caption }}</p>
    </div>
  </div>
{% endfor %}
</div>

<!-- ==================
     Wildlife Section
     ================== -->
<div id="wildlife"></div>
<div class="section-title">🦅 &nbsp; Wildlife</div>
<p class="section-desc">Creatures that share this planet — caught in an unguarded moment</p>

<div class="masonry-grid">
{% assign t_size = site.data.photography.treks | size %}
{% assign tr_size = site.data.photography.travels | size %}
{% assign wildlife_start = t_size | plus: tr_size %}
{% for photo in site.data.photography.wildlife %}
  <div class="masonry-item" onclick="openLightbox({{ wildlife_start | plus: forloop.index0 }})">
    <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
    <div class="masonry-caption">
      <span>{{ photo.location }}</span>
      <p>{{ photo.caption }}</p>
    </div>
  </div>
{% endfor %}
</div>

<!-- ==================
     Nature Section
     ================== -->
<div id="nature"></div>
<div class="section-title">🌿 &nbsp; Nature</div>
<p class="section-desc">Flowers, skies, seasons and the quiet drama of the natural world</p>

<div class="masonry-grid">
{% assign t_size = site.data.photography.treks | size %}
{% assign tr_size = site.data.photography.travels | size %}
{% assign w_size = site.data.photography.wildlife | size %}
{% assign nature_start = t_size | plus: tr_size | plus: w_size %}
{% for photo in site.data.photography.nature %}
  <div class="masonry-item" onclick="openLightbox({{ nature_start | plus: forloop.index0 }})">
    <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
    <div class="masonry-caption">
      <span>{{ photo.location }}</span>
      <p>{{ photo.caption }}</p>
    </div>
  </div>
{% endfor %}
</div>

<!-- ==================
     Human Emotions Section
     ================== -->
<div id="human"></div>
<div class="section-title">🧍 &nbsp; Human Emotions</div>
<p class="section-desc">Strangers in motion — streets, fields, laughter and the in-between moments</p>

<div class="masonry-grid">
{% assign t_size = site.data.photography.treks | size %}
{% assign tr_size = site.data.photography.travels | size %}
{% assign w_size = site.data.photography.wildlife | size %}
{% assign n_size = site.data.photography.nature | size %}
{% assign human_start = t_size | plus: tr_size | plus: w_size | plus: n_size %}
{% for photo in site.data.photography.human %}
  <div class="masonry-item" onclick="openLightbox({{ human_start | plus: forloop.index0 }})">
    <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
    <div class="masonry-caption">
      <span>{{ photo.location }}</span>
      <p>{{ photo.caption }}</p>
    </div>
  </div>
{% endfor %}
</div>

<!-- ==================
     Instagram Button
     ================== -->
<div class="insta-link">
  <a href="https://www.instagram.com/anup_upadhyaya?igsh=MW5vYjN1MW91ZnB5cA%3D%3D&utm_source=qr"
     target="_blank"
     class="insta-btn">
    📷 &nbsp; Follow on Instagram
  </a>
</div>

<!-- ==================
     Lightbox Script
     ================== -->
<script>
const photos = [
  {% for photo in site.data.photography.treks %}
  {
    src: "/images/{{ photo.file }}",
    caption: "{{ photo.caption }}",
    location: "{{ photo.location }}",
    year: "{{ photo.year }}"
  }{% unless forloop.last %},{% endunless %}
  {% endfor %},
  {% for photo in site.data.photography.travels %}
  {
    src: "/images/{{ photo.file }}",
    caption: "{{ photo.caption }}",
    location: "{{ photo.location }}",
    year: "{{ photo.year }}"
  }{% unless forloop.last %},{% endunless %}
  {% endfor %},
  {% for photo in site.data.photography.wildlife %}
  {
    src: "/images/{{ photo.file }}",
    caption: "{{ photo.caption }}",
    location: "{{ photo.location }}",
    year: "{{ photo.year }}"
  }{% unless forloop.last %},{% endunless %}
  {% endfor %},
  {% for photo in site.data.photography.nature %}
  {
    src: "/images/{{ photo.file }}",
    caption: "{{ photo.caption }}",
    location: "{{ photo.location }}",
    year: "{{ photo.year }}"
  }{% unless forloop.last %},{% endunless %}
  {% endfor %},
  {% for photo in site.data.photography.human %}
  {
    src: "/images/{{ photo.file }}",
    caption: "{{ photo.caption }}",
    location: "{{ photo.location }}",
    year: "{{ photo.year }}"
  }{% unless forloop.last %},{% endunless %}
  {% endfor %}
];

let currentPhoto = 0;

function openLightbox(index) {
  currentPhoto = index;
  updateLightbox();
  document.getElementById('lightbox').classList.add('active');
  document.body.style.overflow = 'hidden';
}

function updateLightbox() {
  const photo = photos[currentPhoto];
  document.getElementById('lightbox-img').src = photo.src;
  document.getElementById('lightbox-caption').textContent = photo.caption;
  document.getElementById('lightbox-location').textContent = photo.location;
  document.getElementById('lightbox-year').textContent = photo.year;
  document.getElementById('lightbox-counter').textContent = 
    (currentPhoto + 1) + ' / ' + photos.length;
}

function closeLightbox() {
  document.getElementById('lightbox').classList.remove('active');
  document.body.style.overflow = '';
}

function changePhoto(direction) {
  currentPhoto = (currentPhoto + direction + photos.length) % photos.length;
  updateLightbox();
}

document.getElementById('lightbox').addEventListener('click', function(e) {
  if (e.target === this) closeLightbox();
});

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') closeLightbox();
  if (e.key === 'ArrowRight') changePhoto(1);
  if (e.key === 'ArrowLeft') changePhoto(-1);
});
</script>
