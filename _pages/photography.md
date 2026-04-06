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
  background: rgba(0,0,0,0.48);
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
  color: rgba(255,255,255,0.85);
}
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
}
.section-tab:hover { opacity: 1; border-color: currentColor; text-decoration: none; }
.section-title {
  text-align: center;
  font-family: 'Lora', 'Georgia', serif;
  font-size: 1.0em;
  font-weight: 400;
  letter-spacing: 6px;
  text-transform: uppercase;
  color: var(--global-text-color);
  opacity: 0.5;
  margin: 3.5em 0 0.4em;
}
.section-title::before, .section-title::after {
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
}
.masonry-grid {
  columns: 3;
  column-gap: 10px;
  margin-bottom: 1em;
}
@media (max-width: 900px) { .masonry-grid { columns: 2; } }
@media (max-width: 500px) { .masonry-grid { columns: 1; } }
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
}

/* ── LIGHTBOX ── */
#plb {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.97);
  z-index: 2147483647;          /* absolute maximum */
  display: none;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
#plb.on { display: flex; }

/* push masthead behind lightbox when open */
body.plb-open .masthead { z-index: 1 !important; }
body.plb-open { overflow: hidden; }

#plb-img {
  max-width: 88vw;
  max-height: 74vh;
  object-fit: contain;
  border-radius: 2px;
  box-shadow: 0 0 80px rgba(0,0,0,0.9);
  display: block;
  margin-top: 30px;
}
.plb-top {
  position: absolute;
  top: 0; left: 0; right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 16px 24px;
  z-index: 10;
}
.plb-cnt {
  color: rgba(255,255,255,0.3);
  font-size: 0.72em;
  letter-spacing: 3px;
}
.plb-close {
  color: rgba(255,255,255,0.5);
  font-size: 1.8em;
  cursor: pointer;
  background: none;
  border: none;
  line-height: 1;
  transition: color 0.2s;
  padding: 0;
}
.plb-close:hover { color: #fff; }
.plb-sec {
  font-size: 0.62em;
  letter-spacing: 5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.2);
  margin-bottom: 8px;
  margin-top: 4px;
}
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
}
.plb-cap {
  color: rgba(255,255,255,0.8);
  font-style: italic;
  font-size: 0.92em;
  font-family: 'Lora', Georgia, serif;
  max-width: 540px;
  margin: 0 auto;
}
.plb-yr {
  display: block;
  font-size: 0.65em;
  color: rgba(255,255,255,0.2);
  margin-top: 7px;
  letter-spacing: 3px;
}
.plb-arrow {
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
  z-index: 10;
  line-height: 1;
  user-select: none;
}
.plb-arrow:hover { color: rgba(255,255,255,0.9); }
#plb-prev { left: 8px; }
#plb-next { right: 8px; }

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
  font-weight: 600;
  transition: transform 0.3s, box-shadow 0.3s;
  box-shadow: 0 4px 15px rgba(220,39,67,0.28);
}
.insta-btn:hover { transform: translateY(-2px); box-shadow: 0 8px 28px rgba(220,39,67,0.45); }
.page__content { max-width: 100%; }
</style>

<!-- HERO -->
<div class="photo-hero">
  <div class="photo-hero-text">
    <h1>Through My Lens</h1>
    <p>Treks &nbsp;·&nbsp; Travels &nbsp;·&nbsp; Wildlife &nbsp;·&nbsp; Nature</p>
  </div>
</div>

<!-- TABS -->
<div class="section-tabs">
  <a href="#treks"   class="section-tab">🏔️ &nbsp; Treks</a>
  <a href="#travels" class="section-tab">🌍 &nbsp; Travels</a>
  <a href="#wildlife" class="section-tab">🦅 &nbsp; Wildlife</a>
  <a href="#nature"  class="section-tab">🌿 &nbsp; Nature</a>
</div>

<!-- LIGHTBOX -->
<div id="plb">
  <div class="plb-top">
    <span class="plb-cnt" id="plb-cnt"></span>
    <button class="plb-close" id="plb-close">&#10005;</button>
  </div>
  <button class="plb-arrow" id="plb-prev">&#8249;</button>
  <span class="plb-sec" id="plb-sec"></span>
  <img id="plb-img" src="" alt="">
  <div class="plb-meta">
    <span class="plb-loc" id="plb-loc"></span>
    <div class="plb-cap" id="plb-cap"></div>
    <span class="plb-yr" id="plb-yr"></span>
  </div>
  <button class="plb-arrow" id="plb-next">&#8250;</button>
</div>

<!-- TREKS -->
<div id="treks"></div>
<div class="section-title">🏔️ &nbsp; Treks</div>
<p class="section-desc">High passes, glacial moraines and silences that only mountains know</p>
<div class="masonry-grid" data-section="treks">
{% for photo in site.data.photography.treks %}
<div class="masonry-item" data-idx="{{ forloop.index0 }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<!-- TRAVELS -->
<div id="travels"></div>
<div class="section-title">🌍 &nbsp; Travels</div>
<p class="section-desc">From Himalayan valleys to European cobblestones and American skylines</p>
<div class="masonry-grid" data-section="travels">
{% for photo in site.data.photography.travels %}
<div class="masonry-item" data-idx="{{ forloop.index0 }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<!-- WILDLIFE -->
<div id="wildlife"></div>
<div class="section-title">🦅 &nbsp; Wildlife</div>
<p class="section-desc">Creatures that share this planet — caught in an unguarded moment</p>
<div class="masonry-grid" data-section="wildlife">
{% for photo in site.data.photography.wildlife %}
<div class="masonry-item" data-idx="{{ forloop.index0 }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<!-- NATURE -->
<div id="nature"></div>
<div class="section-title">🌿 &nbsp; Nature</div>
<p class="section-desc">Flowers, skies, seasons and the quiet drama of the natural world</p>
<div class="masonry-grid" data-section="nature">
{% for photo in site.data.photography.nature %}
<div class="masonry-item" data-idx="{{ forloop.index0 }}">
  <img src="/images/{{ photo.file }}" alt="{{ photo.location }}" loading="lazy">
  <div class="masonry-caption">
    <span>{{ photo.location }}</span>
    <p>{{ photo.caption }}</p>
  </div>
</div>
{% endfor %}
</div>

<div class="insta-link">
  <a href="https://www.instagram.com/anup_upadhyaya?igsh=MW5vYjN1MW91ZnB5cA%3D%3D&utm_source=qr"
     target="_blank" class="insta-btn">📷 &nbsp; Follow on Instagram</a>
</div>

<script>
(function(){
  // Build photo arrays per section from DOM
  var secs = {};
  var labels = { treks:'Treks', travels:'Travels', wildlife:'Wildlife', nature:'Nature' };

  document.querySelectorAll('.masonry-grid[data-section]').forEach(function(grid){
    var sec = grid.getAttribute('data-section');
    secs[sec] = [];
    grid.querySelectorAll('.masonry-item').forEach(function(item){
      var img = item.querySelector('img');
      var loc = item.querySelector('.masonry-caption span');
      var cap = item.querySelector('.masonry-caption p');
      secs[sec].push({
        src: img ? img.src : '',
        loc: loc ? loc.textContent.trim() : '',
        cap: cap ? cap.textContent.trim() : '',
        yr:  item.getAttribute('data-yr') || ''
      });
    });

    // Attach click handlers
    grid.querySelectorAll('.masonry-item').forEach(function(item){
      item.addEventListener('click', function(e){
        e.preventDefault();
        open(sec, parseInt(item.getAttribute('data-idx'), 10));
      });
    });
  });

  var lb    = document.getElementById('plb');
  var lbImg = document.getElementById('plb-img');
  var lbLoc = document.getElementById('plb-loc');
  var lbCap = document.getElementById('plb-cap');
  var lbYr  = document.getElementById('plb-yr');
  var lbSec = document.getElementById('plb-sec');
  var lbCnt = document.getElementById('plb-cnt');

  var curSec = '', curIdx = 0;

  function render(){
    var list = secs[curSec];
    if(!list || !list[curIdx]) return;
    var p = list[curIdx];
    lbImg.src      = p.src;
    lbLoc.textContent = p.loc;
    lbCap.textContent = p.cap;
    lbYr.textContent  = p.yr;
    lbSec.textContent = labels[curSec] || curSec;
    lbCnt.textContent = (curIdx+1) + ' / ' + list.length;
  }

  function open(sec, idx){
    curSec = sec; curIdx = idx;
    render();
    lb.classList.add('on');
    document.body.classList.add('plb-open');
  }

  function close(){
    lb.classList.remove('on');
    document.body.classList.remove('plb-open');
    lbImg.src = '';
  }

  function move(dir){
    var list = secs[curSec];
    if(!list) return;
    curIdx = (curIdx + dir + list.length) % list.length;
    render();
  }

  document.getElementById('plb-close').addEventListener('click', close);
  document.getElementById('plb-prev').addEventListener('click', function(e){ e.stopPropagation(); move(-1); });
  document.getElementById('plb-next').addEventListener('click', function(e){ e.stopPropagation(); move(1); });
  lb.addEventListener('click', function(e){ if(e.target===lb) close(); });
  document.addEventListener('keydown', function(e){
    if(!lb.classList.contains('on')) return;
    if(e.key==='Escape') close();
    if(e.key==='ArrowRight') move(1);
    if(e.key==='ArrowLeft')  move(-1);
  });
})();
</script>
