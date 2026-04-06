---
layout: single
title: " "
permalink: /photography/
author_profile: false
---

<style>
/* Photography page, no sidebar, full-width artistic layout */

/* ==================
   Hero Header
   ================== */
.photo-hero {
  width: 100vw;
  margin-left: calc(-50vw + 50%);
  height: 65vh;
  min-height: 380px;
  background-image: url('/images/photography/hero.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 0;
  position: relative;
  background-color: #1a2a1e;
  background-image: url('/images/photography/hero.jpg'),
    linear-gradient(135deg, #1a2a1e 0%, #2d4a35 50%, #1a3028 100%);
}

.photo-hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.48);
}

.photo-hero::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 80px;
  background: linear-gradient(to bottom, transparent, var(--global-bg-color));
}

.photo-hero-text {
  position: relative;
  text-align: center;
  color: white;
  z-index: 1;
  padding: 2em;
}

.photo-hero-text h1 {
  font-family: 'Lora', 'Georgia', serif;
  font-size: clamp(2em, 5vw, 3.5em);
  font-weight: 400;
  letter-spacing: 10px;
  text-transform: uppercase;
  margin-bottom: 0.5em;
  text-shadow: 0 2px 20px rgba(0,0,0,0.6);
}

.photo-hero-text p {
  font-size: clamp(0.8em, 2vw, 1em);
  font-weight: 300;
  letter-spacing: 5px;
  font-style: italic;
  text-shadow: 1px 1px 6px rgba(0,0,0,0.6);
  color: rgba(255,255,255,0.85);
}

/* ==================
   Section Tabs
   ================== */
.section-tabs {
  display: flex;
  justify-content: center;
  gap: 10px;
  margin: 2.5em 0 2.5em;
  flex-wrap: wrap;
}

.section-tab {
  padding: 7px 20px;
  font-size: 0.72em;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--global-text-color);
  opacity: 0.6;
  border: 1px solid var(--global-border-color);
  border-radius: 30px;
  cursor: pointer;
  text-decoration: none;
  transition: all 0.25s ease;
  font-family: 'Source Sans 3', sans-serif;
}

.section-tab:hover {
  opacity: 1;
  border-color: currentColor;
  text-decoration: none;
}

/* ==================
   Section Title
   ================== */
.section-title {
  text-align: center;
  font-family: 'Lora', 'Georgia', serif;
  font-size: 1.0em;
  font-weight: 400;
  letter-spacing: 6px;
  text-transform: uppercase;
  color: var(--global-text-color);
  opacity: 0.5;
  margin: 3.5em 0 0.4em 0;
  position: relative;
}

.section-title::before,
.section-title::after {
  content: '';
  display: inline-block;
  width: 50px;
  height: 1px;
  background: var(--global-border-color);
  vertical-align: middle;
  margin: 0 14px;
}

.section-desc {
  text-align: center;
  font-size: 0.83em;
  color: var(--global-text-color);
  opacity: 0.45;
  font-style: italic;
  margin-bottom: 1.8em;
  letter-spacing: 0.5px;
}

/* ==================
   Masonry Grid
   ================== */
.masonry-grid {
  columns: 3;
  column-gap: 10px;
  margin-bottom: 1em;
}

@media screen and (max-width: 900px)  { .masonry-grid { columns: 2; } }
@media screen and (max-width: 500px)  { .masonry-grid { columns: 1; } }

.masonry-item {
  break-inside: avoid;
  margin-bottom: 10px;
  position: relative;
  overflow: hidden;
  border-radius: 3px;
  cursor: pointer;
  background: var(--global-border-color);
}

.masonry-item img {
  width: 100%;
  display: block;
  transition: transform 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  border-radius: 3px;
}

.masonry-item:hover img { transform: scale(1.05); }

/* ==================
   Caption Overlay
   ================== */
.masonry-caption {
  position: absolute;
  bottom: 0; left: 0; right: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.85) 0%, transparent 100%);
  color: white;
  padding: 3em 1em 0.9em;
  opacity: 0;
  transition: opacity 0.35s ease;
  border-radius: 0 0 3px 3px;
}

.masonry-item:hover .masonry-caption { opacity: 1; }

.masonry-caption p {
  margin: 0;
  font-size: 0.8em;
  font-style: italic;
  letter-spacing: 0.3px;
  color: rgba(255,255,255,0.9) !important;
  line-height: 1.4;
}

.masonry-caption span {
  display: block;
  font-size: 0.67em;
  letter-spacing: 3px;
  text-transform: uppercase;
  opacity: 0.75;
  color: #ddd;
  margin-bottom: 5px;
  font-family: 'Source Sans 3', sans-serif;
}

/* ==================
   Lightbox
   ================== */
.lightbox-overlay {
  display: none;
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.97);
  z-index: 9999;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.lightbox-overlay.active { display: flex; }

.lightbox-overlay img {
  max-width: 88vw;
  max-height: 80vh;
  object-fit: contain;
  border-radius: 2px;
  box-shadow: 0 0 100px rgba(0,0,0,0.9);
}

.lightbox-meta {
  text-align: center;
  margin-top: 1.4em;
  padding: 0 1em;
}

.lightbox-location {
  display: block;
  font-size: 0.68em;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.4);
  margin-bottom: 6px;
  font-family: 'Source Sans 3', sans-serif;
}

.lightbox-caption {
  color: rgba(255,255,255,0.8);
  font-style: italic;
  font-size: 0.92em;
  font-family: 'Lora', Georgia, serif;
  letter-spacing: 0.3px;
  max-width: 560px;
  margin: 0 auto;
}

.lightbox-year {
  display: block;
  font-size: 0.68em;
  color: rgba(255,255,255,0.25);
  margin-top: 8px;
  letter-spacing: 3px;
  font-family: 'Source Sans 3', sans-serif;
}

.lightbox-close {
  position: absolute;
  top: 22px; right: 28px;
  color: rgba(255,255,255,0.5);
  font-size: 1.8em;
  cursor: pointer;
  background: none;
  border: none;
  line-height: 1;
  transition: color 0.2s;
}
.lightbox-close:hover { color: white; }

.lightbox-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  color: rgba(255,255,255,0.3);
  font-size: 3.5em;
  cursor: pointer;
  background: none;
  border: none;
  padding: 0.2em 0.5em;
  font-weight: 100;
  transition: color 0.2s;
  font-family: 'Lora', Georgia, serif;
}
.lightbox-nav:hover { color: rgba(255,255,255,0.9); }
.lightbox-prev { left: 10px; }
.lightbox-next { right: 10px; }

.lightbox-counter {
  position: absolute;
  top: 28px; left: 30px;
  color: rgba(255,255,255,0.3);
  font-size: 0.72em;
  letter-spacing: 3px;
  font-family: 'Source Sans 3', sans-serif;
}

/* ==================
   Empty section placeholder
   ================== */
.coming-soon {
  text-align: center;
  padding: 3em 1em;
  font-size: 0.82em;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--global-text-color);
  opacity: 0.3;
  font-family: 'Source Sans 3', sans-serif;
}

/* ==================
   Instagram Button
   ================== */
.insta-link {
  text-align: center;
  margin: 2.5em 0 5em;
}

.insta-btn {
  display: inline-block;
  background: linear-gradient(45deg, #f09433, #e6683c, #dc2743, #cc2366, #bc1888);
  color: white !important;
  padding: 11px 28px;
  border-radius: 30px;
  text-decoration: none !important;
  font-size: 0.78em;
  letter-spacing: 3px;
  text-transform: uppercase;
  font-family: 'Source Sans 3', sans-serif;
  font-weight: 600;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 4px 15px rgba(220,39,67,0.28);
}

.insta-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 28px rgba(220,39,67,0.45);
}

/* ==================
   Full-width override, no sidebar on this page
   ================== */
.page__content {
  max-width: 100%;
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
  <!-- <a href="#human" class="section-tab">🧍 &nbsp; Human Emotions</a> -->
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
<p class="section-desc">High passes and silences </p>

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
{% if site.data.photography.treks.size == 0 %}
  <div class="coming-soon">Photos coming soon</div>
{% endif %}
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
<p class="section-desc">Creatures that share this planet</p>

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
<p class="section-desc">Flowers, skies, seasons and the quiet drama </p>

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
<p class="section-desc">Strangers in motion, streets, fields, laughter and the in-between moments</p>

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
