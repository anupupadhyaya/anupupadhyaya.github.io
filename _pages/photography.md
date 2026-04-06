---
layout: single
title: " "
permalink: /photography/
author_profile: false
---

<style>
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
  bottom: 0; left: 0; right: 0;
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
.masonry-grid {
  columns: 3;
  column-gap: 10px;
  margin-bottom: 1em;
}
@media screen and (max-width: 900px) { .masonry-grid { columns: 2; } }
@media screen and (max-width: 500px) { .masonry-grid { columns: 1; } }
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
.masonry-caption {
  position: absolute;
  bottom: 0; left: 0; right: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.85) 0%, transparent 100%);
  color: white;
  padding: 3em 1em 0.9em;
  opacity: 0;
  transition: opacity 0.35s ease;
  border-radius: 0 0 3px 3px;
  pointer-events: none;
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

/* Lightbox */
#photo-lightbox {
  display: none;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.97);
  z-index: 999999;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
#photo-lightbox.active { display: flex; }
#photo-lightbox img {
  max-width: 85vw;
  max-height: 68vh;
  object-fit: contain;
  border-radius: 2px;
  box-shadow: 0 0 100px rgba(0,0,0,0.9);
  margin-top: 25px;
}
.lb-topbar {
  position: absolute;
  top: 0; left: 0; right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 18px 28px;
  z-index: 10;
}
.lb-back {
  color: rgba(255,255,255,0.5);
  font-size: 0.75em;
  letter-spacing: 3px;
  text-transform: uppercase;
  cursor: pointer;
  background: none;
  border: none;
  font-family: 'Source Sans 3', sans-serif;
  transition: color 0.2s;
}
.lb-back:hover { color: white; }
.lb-counter {
  color: rgba(255,255,255,0.3);
  font-size: 0.72em;
  letter-spacing: 3px;
  font-family: 'Source Sans 3', sans-serif;
}
.lb-x {
  color: rgba(255,255,255,0.5);
  font-size: 1.8em;
  cursor: pointer;
  background: none;
  border: none;
  line-height: 1;
  transition: color 0.2s;
}
.lb-x:hover { color: white; }
.lb-section {
  display: block;
  font-size: 0.6em;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.25);
  margin-bottom: 10px;
  font-family: 'Source Sans 3', sans-serif;
}
.lb-meta {
  text-align: center;
  margin-top: 1.2em;
  padding: 0 1em;
}
.lb-loc {
  display: block;
  font-size: 0.68em;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.4);
  margin-bottom: 6px;
  font-family: 'Source Sans 3', sans-serif;
}
.lb-cap {
  color: rgba(255,255,255,0.8);
  font-style: italic;
  font-size: 0.92em;
  font-family: 'Lora', Georgia, serif;
  letter-spacing: 0.3px;
  max-width: 560px;
  margin: 0 auto;
}
.lb-yr {
  display: block;
  font-size: 0.68em;
  color: rgba(255,255,255,0.25);
  margin-top: 8px;
  letter-spacing: 3px;
  font-family: 'Source Sans 3', sans-serif;
}
.lb-arrow {
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
  z-index: 10;
}
.lb-arrow:hover { color: rgba(255,255,255,0.9); }
.lb-left { left: 10px; }
.lb-right { right: 10px; }
body.lb-open .masthead,
body.lb-open .greedy-nav,
body.lb-open header { z-index: 1 !important; }

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
.insta-link { text-align: center; margin: 2.5em 0 5em; }
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
.page__content { max-width: 100%; }
</style>

<div class="photo-hero">
  <div class="photo-hero-text">
    <h1>Through My Lens</h1>
    <p>Treks &nbsp;·&nbsp; Travels &nbsp;·&nbsp; Wildlife &nbsp;·&nbsp; Nature</p>
  </div>
</div>

<div class="section-tabs">
  <a href="#treks" class="section-tab">🏔️ &nbsp; Treks</a>
  <a href="#travels" class="section-tab">🌍 &nbsp; Travels</a>
  <a href="#wildlife" class="section-tab">🦅 &nbsp; Wildlife</a>
  <a href="#nature" class="section-tab">🌿 &nbsp; Nature</a>
</div>

<!-- Lightbox (completely separate IDs to avoid conflicts) -->
<div id="photo-lightbox">
  <div class="lb-topbar">
    <button class="lb-back" id="lb-back">&#8592; Back to Gallery</button>
    <div class="lb-counter" id="lb-counter"></div>
    <button class="lb-x" id="lb-x">&#10005;</button>
  </div>
  <button class="lb-arrow lb-left" id="lb-left">&#8249;</button>
  <span class="lb-section" id="lb-section"></span>
  <img id="lb-img" src="" alt="">
  <div class="lb-meta">
    <span class="lb-loc" id="lb-loc"></span>
    <div class="lb-cap" id="lb-cap"></div>
    <span class="lb-yr" id="lb-yr"></span>
  </div>
  <button class="lb-arrow lb-right" id="lb-right">&#8250;</button>
</div>

<!-- Treks -->
<div id="treks"></div>
<div class="section-title">🏔️ &nbsp; Treks</div>
<p class="section-desc">High passes and silences</p>
<div class="masonry-grid">
{% for photo in site.data.photography.treks %}
<div class="masonry-item" data-section="treks" data-index="{{ forloop.index0 }}" data-year="{{ photo.year }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<!-- Travels -->
<div id="travels"></div>
<div class="section-title">🌍 &nbsp; Travels</div>
<p class="section-desc">From Himalayan valleys to European cobblestones and American skylines</p>
<div class="masonry-grid">
{% for photo in site.data.photography.travels %}
<div class="masonry-item" data-section="travels" data-index="{{ forloop.index0 }}" data-year="{{ photo.year }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<!-- Wildlife -->
<div id="wildlife"></div>
<div class="section-title">🦅 &nbsp; Wildlife</div>
<p class="section-desc">Creatures that share this planet</p>
<div class="masonry-grid">
{% for photo in site.data.photography.wildlife %}
<div class="masonry-item" data-section="wildlife" data-index="{{ forloop.index0 }}" data-year="{{ photo.year }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<!-- Nature -->
<div id="nature"></div>
<div class="section-title">🌿 &nbsp; Nature</div>
<p class="section-desc">Flowers, skies, seasons and the quiet drama</p>
<div class="masonry-grid">
{% for photo in site.data.photography.nature %}
<div class="masonry-item" data-section="nature" data-index="{{ forloop.index0 }}" data-year="{{ photo.year }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<div class="insta-link">
  <a href="https://www.instagram.com/anup_upadhyaya?igsh=MW5vYjN1MW91ZnB5cA%3D%3D&utm_source=qr" target="_blank" class="insta-btn">
    📷 &nbsp; Follow on Instagram
  </a>
</div>

<!-- ZERO Jekyll inside this script. Reads everything from the DOM. -->
<script>
document.addEventListener('DOMContentLoaded', function() {

  // Build photo data from DOM only
  var sections = {};
  var items = document.querySelectorAll('.masonry-item');

  for (var i = 0; i < items.length; i++) {
    var el = items[i];
    var sec = el.getAttribute('data-section');
    if (!sec) continue;
    if (!sections[sec]) sections[sec] = [];

    var imgEl = el.querySelector('img');
    var locEl = el.querySelector('.masonry-caption span');
    var capEl = el.querySelector('.masonry-caption p');
    var yr = el.getAttribute('data-year') || '';

    sections[sec].push({
      src: imgEl ? imgEl.getAttribute('src') : '',
      location: locEl ? locEl.textContent : '',
      caption: capEl ? capEl.textContent : '',
      year: yr
    });
  }

  var names = { treks: 'Treks', travels: 'Travels', wildlife: 'Wildlife', nature: 'Nature' };
  var curSec = '';
  var curIdx = 0;

  var box = document.getElementById('photo-lightbox');
  var boxImg = document.getElementById('lb-img');
  var boxLoc = document.getElementById('lb-loc');
  var boxCap = document.getElementById('lb-cap');
  var boxYr = document.getElementById('lb-yr');
  var boxSec = document.getElementById('lb-section');
  var boxCnt = document.getElementById('lb-counter');

  function show() {
    var list = sections[curSec];
    if (!list || !list[curIdx]) return;
    var p = list[curIdx];
    boxImg.src = p.src;
    boxLoc.textContent = p.location;
    boxCap.textContent = p.caption;
    boxYr.textContent = p.year;
    boxSec.textContent = names[curSec] || curSec;
    boxCnt.textContent = (curIdx + 1) + ' / ' + list.length;
  }

  function open(sec, idx) {
    curSec = sec;
    curIdx = idx;
    show();
    box.classList.add('active');
    document.body.classList.add('lb-open');
    document.body.style.overflow = 'hidden';
  }

  function close() {
    box.classList.remove('active');
    document.body.classList.remove('lb-open');
    document.body.style.overflow = '';
  }

  function move(dir) {
    var list = sections[curSec];
    if (!list) return;
    curIdx = (curIdx + dir + list.length) % list.length;
    show();
  }

  // Attach click to every masonry item
  for (var j = 0; j < items.length; j++) {
    (function(el) {
      el.addEventListener('click', function(e) {
        e.preventDefault();
        e.stopPropagation();
        var s = el.getAttribute('data-section');
        var idx = parseInt(el.getAttribute('data-index'), 10);
        if (s && !isNaN(idx)) {
          open(s, idx);
        }
      });
    })(items[j]);
  }

  // Close buttons
  document.getElementById('lb-x').addEventListener('click', function(e) {
    e.stopPropagation();
    close();
  });
  document.getElementById('lb-back').addEventListener('click', function(e) {
    e.stopPropagation();
    close();
  });

  // Arrow buttons
  document.getElementById('lb-left').addEventListener('click', function(e) {
    e.stopPropagation();
    move(-1);
  });
  document.getElementById('lb-right').addEventListener('click', function(e) {
    e.stopPropagation();
    move(1);
  });

  // Click dark area to close
  box.addEventListener('click', function(e) {
    if (e.target === box) close();
  });

  // Keyboard
  document.addEventListener('keydown', function(e) {
    if (!box.classList.contains('active')) return;
    if (e.key === 'Escape') close();
    if (e.key === 'ArrowRight') move(1);
    if (e.key === 'ArrowLeft') move(-1);
  });

});
</script>
