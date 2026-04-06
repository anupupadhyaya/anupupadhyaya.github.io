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
  width: 100vw;
  margin-left: calc(-50vw + 50%);
  height: 65vh;
  min-height: 380px;
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
  margin: 2.5em 0;
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
  display: none;
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

@media screen and (max-width: 900px) {
  .masonry-grid { columns: 2; }
}

@media screen and (max-width: 500px) {
  .masonry-grid { columns: 1; }
}

.masonry-item {
  break-inside: avoid;
  margin-bottom: 10px;
  position: relative;
  overflow: hidden;
  border-radius: 3px;
  cursor: zoom-in;
  background: var(--global-border-color);
}

.masonry-item img {
  width: 100%;
  display: block;
  transition: transform 0.7s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  border-radius: 3px;
  pointer-events: none;
}

.masonry-item:hover img {
  transform: scale(1.05);
}

/* ==================
   Caption Overlay
   ================== */
.masonry-caption {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.85) 0%, transparent 100%);
  color: white;
  padding: 3em 1em 0.9em;
  opacity: 0;
  transition: opacity 0.35s ease;
  border-radius: 0 0 3px 3px;
  pointer-events: none;
}

.masonry-item:hover .masonry-caption {
  opacity: 1;
}

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
#plb {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.97);
  z-index: 2147483647;
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

#plb img {
  max-width: 88vw;
  max-height: 72vh;
  object-fit: contain;
  border-radius: 2px;
  box-shadow: 0 0 80px rgba(0,0,0,0.9);
  display: block;
  margin-top: 30px;
  pointer-events: none;
  transition: transform 0.2s ease;
}

/* Top bar */
.plb-top {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 24px;
  z-index: 10;
}

.plb-back {
  color: rgba(255,255,255,0.5);
  font-size: 0.75em;
  letter-spacing: 3px;
  text-transform: uppercase;
  cursor: pointer;
  background: none;
  border: none;
  font-family: 'Source Sans 3', sans-serif;
  transition: color 0.2s;
  padding: 5px 10px;
}

.plb-back:hover {
  color: white;
}

.plb-cnt {
  color: rgba(255,255,255,0.3);
  font-size: 0.72em;
  letter-spacing: 3px;
  font-family: 'Source Sans 3', sans-serif;
}

.plb-x {
  color: rgba(255,255,255,0.5);
  font-size: 1.8em;
  cursor: pointer;
  background: none;
  border: none;
  line-height: 1;
  transition: color 0.2s;
  padding: 0;
}

.plb-x:hover {
  color: #fff;
}

/* Section label */
.plb-sec {
  font-size: 0.62em;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.2);
  margin-bottom: 6px;
  margin-top: 4px;
  font-family: 'Source Sans 3', sans-serif;
}

/* Meta info */
.plb-meta {
  text-align: center;
  margin-top: 1.1em;
  padding: 0 1em;
}

.plb-loc {
  display: block;
  font-size: 0.68em;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.35);
  margin-bottom: 5px;
  font-family: 'Source Sans 3', sans-serif;
}

.plb-cap {
  color: rgba(255,255,255,0.8);
  font-style: italic;
  font-size: 0.92em;
  font-family: 'Lora', Georgia, serif;
  letter-spacing: 0.3px;
  max-width: 540px;
  margin: 0 auto;
}

.plb-yr {
  display: block;
  font-size: 0.65em;
  color: rgba(255,255,255,0.2);
  margin-top: 7px;
  letter-spacing: 3px;
  font-family: 'Source Sans 3', sans-serif;
}

/* Arrow buttons */
.plb-arr {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  color: rgba(255,255,255,0.35);
  font-size: 3.5em;
  cursor: pointer;
  background: rgba(0,0,0,0.25);
  border: none;
  padding: 10px 18px;
  border-radius: 6px;
  font-weight: 100;
  transition: color 0.2s, background 0.2s;
  z-index: 10;
  line-height: 1;
  user-select: none;
  font-family: 'Lora', Georgia, serif;
}

.plb-arr:hover {
  color: rgba(255,255,255,0.95);
  background: rgba(0,0,0,0.5);
}

#plb-prev {
  left: 12px;
}

#plb-next {
  right: 12px;
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
   Full-width override
   ================== */
.page__content {
  max-width: 100%;
}
</style>

<!-- ==================
     Lightbox
     ================== -->
<div id="plb" onclick="if(event.target===this)plbClose()">
  <div class="plb-top">
    <button class="plb-back" onclick="plbClose()">&#8592; Back to Gallery</button>
    <span class="plb-cnt" id="plb-cnt"></span>
    <button class="plb-x" onclick="plbClose()">&#10005;</button>
  </div>
  <button class="plb-arr" id="plb-prev" onclick="plbMove(-1)">&#8249;</button>
  <span class="plb-sec" id="plb-sec"></span>
  <img id="plb-img" src="" alt="">
  <div class="plb-meta">
    <span class="plb-loc" id="plb-loc"></span>
    <div class="plb-cap" id="plb-cap"></div>
    <span class="plb-yr" id="plb-yr"></span>
  </div>
  <button class="plb-arr" id="plb-next" onclick="plbMove(1)">&#8250;</button>
</div>

<!-- ==================
     Hero Section
     ================== -->
<div class="photo-hero">
  <div class="photo-hero-text">
    <h1>Through My Lens</h1>
    <p>Treks &nbsp;·&nbsp; Travels &nbsp;·&nbsp;
       Wildlife &nbsp;·&nbsp; Nature</p>
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
</div>

<!-- ==================
     Treks Section
     ================== -->
<div id="treks"></div>
<div class="section-title">🏔️ &nbsp; Treks</div>
<p class="section-desc">High passes and silences </p>

<div class="masonry-grid">
{% assign i = 0 %}
{% for photo in site.data.photography.treks %}
<div class="masonry-item" onclick="plbOpen('treks',{{ i }})">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% assign i = i | plus: 1 %}
{% endfor %}
</div>

<!-- ==================
     Travels Section
     ================== -->
<div id="travels"></div>
<div class="section-title">🌍 &nbsp; Travels</div>
<p class="section-desc">From Himalayan valleys to European cobblestones and American skylines</p>

<div class="masonry-grid">
{% assign i = 0 %}
{% for photo in site.data.photography.travels %}
<div class="masonry-item" onclick="plbOpen('travels',{{ i }})">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% assign i = i | plus: 1 %}
{% endfor %}
</div>

<!-- ==================
     Wildlife Section
     ================== -->
<div id="wildlife"></div>
<div class="section-title">🦅 &nbsp; Wildlife</div>
<p class="section-desc">Creatures that share this planet</p>

<div class="masonry-grid">
{% assign i = 0 %}
{% for photo in site.data.photography.wildlife %}
<div class="masonry-item" onclick="plbOpen('wildlife',{{ i }})">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% assign i = i | plus: 1 %}
{% endfor %}
</div>

<!-- ==================
     Nature Section
     ================== -->
<div id="nature"></div>
<div class="section-title">🌿 &nbsp; Nature</div>
<p class="section-desc">Skies, seasons and the quiet drama </p>

<div class="masonry-grid">
{% assign i = 0 %}
{% for photo in site.data.photography.nature %}
<div class="masonry-item" onclick="plbOpen('nature',{{ i }})">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% assign i = i | plus: 1 %}
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
/* Photo data built by Jekyll (escape filter handles special chars) */
var PLB_DATA = {
  treks: [
    {% for p in site.data.photography.treks %}
    {
      src: "/images/{{ p.file }}",
      loc: "{{ p.location | escape }}",
      cap: "{{ p.caption | escape }}",
      yr: "{{ p.year }}"
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ],
  travels: [
    {% for p in site.data.photography.travels %}
    {
      src: "/images/{{ p.file }}",
      loc: "{{ p.location | escape }}",
      cap: "{{ p.caption | escape }}",
      yr: "{{ p.year }}"
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ],
  wildlife: [
    {% for p in site.data.photography.wildlife %}
    {
      src: "/images/{{ p.file }}",
      loc: "{{ p.location | escape }}",
      cap: "{{ p.caption | escape }}",
      yr: "{{ p.year }}"
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ],
  nature: [
    {% for p in site.data.photography.nature %}
    {
      src: "/images/{{ p.file }}",
      loc: "{{ p.location | escape }}",
      cap: "{{ p.caption | escape }}",
      yr: "{{ p.year }}"
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ]
};

/* Section display names */
var PLB_LABELS = {
  treks: 'Treks',
  travels: 'Travels',
  wildlife: 'Wildlife',
  nature: 'Nature'
};

/* State */
var plbSec = '';
var plbIdx = 0;
var plbEl = document.getElementById('plb');
var plbImgEl = document.getElementById('plb-img');

/* Render current photo in lightbox */
function plbRender() {
  var p = PLB_DATA[plbSec][plbIdx];
  plbImgEl.src = p.src;
  document.getElementById('plb-loc').textContent = p.loc;
  document.getElementById('plb-cap').textContent = p.cap;
  document.getElementById('plb-yr').textContent = p.yr;
  document.getElementById('plb-sec').textContent = PLB_LABELS[plbSec];
  document.getElementById('plb-cnt').textContent =
    (plbIdx + 1) + ' / ' + PLB_DATA[plbSec].length;

  /* Preload next image for smoother navigation */
  var list = PLB_DATA[plbSec];
  var nextIdx = (plbIdx + 1) % list.length;
  var preload = new Image();
  preload.src = list[nextIdx].src;
}

/* Open lightbox with subtle zoom animation */
function plbOpen(sec, idx) {
  plbSec = sec;
  plbIdx = idx;
  plbRender();
  plbEl.style.display = 'flex';
  document.body.style.overflow = 'hidden';

  /* Push navbar behind lightbox */
  var mh = document.querySelector('.masthead');
  if (mh) mh.style.zIndex = '1';

  /* Subtle zoom-in animation */
  plbImgEl.style.transform = 'scale(0.95)';
  setTimeout(function() {
    plbImgEl.style.transform = 'scale(1)';
  }, 50);
}

/* Close lightbox */
function plbClose() {
  plbEl.style.display = 'none';
  document.body.style.overflow = '';
  plbImgEl.src = '';

  /* Restore navbar */
  var mh = document.querySelector('.masthead');
  if (mh) mh.style.zIndex = '';
}

/* Move within current section only */
function plbMove(dir) {
  var n = PLB_DATA[plbSec].length;
  plbIdx = (plbIdx + dir + n) % n;
  plbRender();
}

/* Keyboard navigation */
document.addEventListener('keydown', function(e) {
  if (plbEl.style.display !== 'flex') return;
  if (e.key === 'Escape') plbClose();
  if (e.key === 'ArrowRight') plbMove(1);
  if (e.key === 'ArrowLeft') plbMove(-1);
});

/* Touch/Swipe support for mobile */
var plbTouchStartX = 0;

plbEl.addEventListener('touchstart', function(e) {
  plbTouchStartX = e.touches[0].clientX;
});

plbEl.addEventListener('touchend', function(e) {
  var endX = e.changedTouches[0].clientX;
  var diff = plbTouchStartX - endX;

  if (Math.abs(diff) > 50) {
    if (diff > 0) {
      plbMove(1);
    } else {
      plbMove(-1);
    }
  }
});
</script>
