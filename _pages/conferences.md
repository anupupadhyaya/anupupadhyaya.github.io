---
layout: single
title: "Conferences & Presentations"
permalink: /conferences/
author_profile: true
---

<style>
.conf-section-title {
  font-size: 1.15em;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin: 2em 0 1em;
  padding-bottom: 6px;
  border-bottom: 2px solid var(--global-border-color);
  color: var(--global-text-color);
}

.conf-card {
  margin-bottom: 1.8em;
  padding: 1.2em 1.4em;
  border-left: 4px solid #ccc;
  background: rgba(128,128,128,0.04);
  border-radius: 0 6px 6px 0;
  transition: all 0.25s ease;
}

.conf-card:hover {
  transform: translateX(3px);
  box-shadow: 0 2px 10px rgba(0,0,0,0.06);
}

.conf-card.major {
  border-left: 4px solid #2a7ae2;
  background: rgba(42,122,226,0.04);
}

.conf-title {
  font-size: 1.02em;
  font-weight: 600;
  margin-bottom: 4px;
  color: var(--global-text-color);
}

.conf-title a {
  color: inherit;
  text-decoration: none;
  border-bottom: 1px dashed rgba(128,128,128,0.4);
  transition: border-color 0.2s, color 0.2s;
}

.conf-title a:hover {
  color: #2a7ae2;
  border-bottom-color: #2a7ae2;
}

.conf-venue {
  font-size: 0.88em;
  color: var(--global-text-color);
  opacity: 0.7;
  margin-bottom: 4px;
}

.conf-cite {
  font-size: 0.78em;
  color: var(--global-text-color);
  opacity: 0.5;
  margin-top: 6px;
  font-family: 'Source Sans 3', sans-serif;
  line-height: 1.5;
}

.conf-cite a {
  color: #2a7ae2;
  text-decoration: none;
  border-bottom: 1px dotted #2a7ae2;
}

.conf-cite a:hover {
  opacity: 0.8;
}

.conf-badge {
  display: inline-block;
  font-size: 0.68em;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 3px 10px;
  border-radius: 20px;
  margin-right: 6px;
  margin-top: 4px;
  font-weight: 600;
}

.badge-poster {
  background: rgba(156,39,176,0.12);
  color: #9c27b0;
}

.badge-oral {
  background: rgba(42,122,226,0.12);
  color: #2a7ae2;
}

.badge-attended {
  background: rgba(46,160,67,0.12);
  color: #2ea043;
}

.badge-grant {
  background: rgba(230,145,20,0.14);
  color: #b26a00;
}

.conf-gallery {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 12px;
  margin-top: 16px;
}

@media (max-width: 600px) {
  .conf-gallery { grid-template-columns: 1fr; }
}

.conf-shot {
  margin: 0;
}

.conf-shot .shot-frame {
  display: block;
  width: 100%;
  aspect-ratio: 3 / 2;
  overflow: hidden;
  border-radius: 6px;
  cursor: zoom-in;
  background: rgba(128,128,128,0.08);
}

.conf-shot .shot-frame img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 18%;
  display: block;
  margin: 0;
  border-radius: 6px;
  transition: transform 0.35s ease;
}

.conf-shot .shot-frame:hover img {
  transform: scale(1.05);
}

.conf-cap {
  font-size: 0.75em;
  opacity: 0.55;
  margin-top: 6px;
  line-height: 1.45;
}

/* ── Lightbox ── */
#lb-overlay {
  position: fixed;
  inset: 0;
  z-index: 9999;
  background: rgba(0,0,0,0.88);
  display: none;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  cursor: zoom-out;
}

#lb-overlay.open { display: flex; }

#lb-overlay img {
  max-width: 92vw;
  max-height: 88vh;
  border-radius: 4px;
  transform-origin: center center;
  transition: transform 0.12s ease-out;
  cursor: grab;
  user-select: none;
  -webkit-user-drag: none;
}

#lb-overlay img.panning { cursor: grabbing; transition: none; }

#lb-cap {
  position: absolute;
  bottom: 22px;
  left: 0;
  right: 0;
  text-align: center;
  color: rgba(255,255,255,0.75);
  font-size: 0.82em;
  padding: 0 20px;
  pointer-events: none;
}

#lb-hint {
  position: absolute;
  top: 18px;
  right: 22px;
  color: rgba(255,255,255,0.45);
  font-size: 0.72em;
  letter-spacing: 0.5px;
  pointer-events: none;
}

.conf-desc {
  font-size: 0.88em;
  margin-top: 8px;
  color: var(--global-text-color);
  opacity: 0.8;
  line-height: 1.6;
}
</style>

A record of conference presentations, workshops, and invited talks.

<div class="conf-section-title">Major International Conferences</div>

<div class="conf-card major">
  <div class="conf-title">
    <a href="https://ui.adsabs.harvard.edu/abs/2024AGUFMA23F.2044U" target="_blank">
      Record Breaking Heatwave of 2022 over the Northwest Himalayas (NWH) of India
    </a>
  </div>
  <div class="conf-venue">AGU Fall Meeting, Washington DC, USA &nbsp;|&nbsp; December 9 to 13, 2024</div>
  <span class="conf-badge badge-poster">Poster Presentation</span>
  <span class="conf-badge badge-attended">Attended In-Person</span>
  <div class="conf-desc">
    Presented research on the record-breaking heatwave of 2022 over the Northwest Himalayas, 
    examining its drivers and implications.
  </div>
  <div class="conf-cite">
    Upadhyaya, A. and Rai, A. K. (2024). Record Breaking Heatwave of 2022 over the Northwest 
    Himalayas (NWH) of India. <i>AGU Fall Meeting Abstracts</i>, A23F-2044. 
    [<a href="https://ui.adsabs.harvard.edu/abs/2024AGUFMA23F.2044U" target="_blank">ADS</a>]
  </div>
  <div class="conf-gallery">
    <div class="conf-shot">
      <span class="shot-frame" data-full="/images/conferences/agu-2024-01.jpg" data-cap="At the AGU Fall Meeting, Washington DC">
        <img src="/images/conferences/agu-2024-01.jpg" alt="At the AGU Fall Meeting, Washington DC">
      </span>
      <div class="conf-cap">At the AGU Fall Meeting, Washington DC</div>
    </div>
    <div class="conf-shot">
      <span class="shot-frame" data-full="/images/conferences/agu-2024-02.jpg" data-cap="At my poster during the session">
        <img src="/images/conferences/agu-2024-02.jpg" alt="At my poster during the AGU poster session">
      </span>
      <div class="conf-cap">At my poster during the session</div>
    </div>
  </div>
</div>

<div class="conf-card major">
  <div class="conf-title">
    <a href="https://doi.org/10.5194/egusphere-egu24-15032" target="_blank">
      Identification of Potentially Dangerous Glacial Lakes (PDGLs) in the Northwest Himalayas
    </a>
  </div>
  <div class="conf-venue">EGU General Assembly, Vienna, Austria &nbsp;|&nbsp; April 14 to 19, 2024</div>
  <span class="conf-badge badge-poster">Poster Presentation</span>
  <span class="conf-badge badge-attended">Attended In-Person</span>
  <div class="conf-desc">
    Presented findings on potentially dangerous glacial lakes in the Northwest Himalayas 
    using multi-criteria hazard assessment.
  </div>
  <div class="conf-cite">
    Upadhyaya, A. and Rai, A. K. (2024). Identification of Potentially Dangerous Glacial Lakes 
    (PDGLs) in the Northwest Himalayas. <i>EGU General Assembly Conference Abstracts</i>, EGU24-15032. 
    DOI: <a href="https://doi.org/10.5194/egusphere-egu24-15032" target="_blank">10.5194/egusphere-egu24-15032</a> 
    &nbsp;|&nbsp; [<a href="https://ui.adsabs.harvard.edu/abs/2024EGUGA..2615032U" target="_blank">ADS</a>]
  </div>
  <div class="conf-gallery">
    <div class="conf-shot">
      <span class="shot-frame" data-full="/images/conferences/egu-2024-01.jpg" data-cap="At the EGU General Assembly, Vienna">
        <img src="/images/conferences/egu-2024-01.jpg" alt="At the EGU General Assembly, Vienna">
      </span>
      <div class="conf-cap">At the EGU General Assembly, Vienna</div>
    </div>
    <div class="conf-shot">
      <span class="shot-frame" data-full="/images/conferences/egu-2024-02.jpg" data-cap="Talking through the poster with a visitor">
        <img src="/images/conferences/egu-2024-02.jpg" alt="Discussing the poster with a visitor at EGU">
      </span>
      <div class="conf-cap">Talking through the poster with a visitor</div>
    </div>
  </div>
</div>

<div class="conf-section-title">Summer Schools & Workshops</div>

<div class="conf-card major">
  <div class="conf-title">
    <a href="https://iaeg.info/" target="_blank">
      5th IAEG International Summer School on Engineering Geology
    </a>
  </div>
  <div class="conf-venue">Aosta, Italy &nbsp;|&nbsp; June 29 to July 7, 2026</div>
  <span class="conf-badge badge-oral">Oral Presentation</span>
  <span class="conf-badge badge-attended">Attended In-Person</span>
  <span class="conf-badge badge-grant">YEG Travel Grant</span>
  <div class="conf-desc">
    Selected participant at the 5th IAEG International Summer School, supported by a Young Engineering
    Geologists (YEG) Travel Grant from the International Association for Engineering Geology and the
    Environment. Presented work on SAR-based flood mapping alongside field sessions on slope stability
    and mass movement processes in the Aosta Valley.
  </div>
  <div class="conf-gallery">
    <div class="conf-shot">
      <span class="shot-frame" data-full="/images/conferences/iaeg-2026-01.jpg" data-cap="At the IAEG Summer School, Aosta">
        <img src="/images/conferences/iaeg-2026-01.jpg" alt="At the 5th IAEG International Summer School, Aosta">
      </span>
      <div class="conf-cap">At the IAEG Summer School, Aosta</div>
    </div>
    <div class="conf-shot">
      <span class="shot-frame" data-full="/images/conferences/iaeg-2026-02.jpg" data-cap="Field session in the Aosta Valley">
        <img src="/images/conferences/iaeg-2026-02.jpg" alt="Field session in the Aosta Valley">
      </span>
      <div class="conf-cap">Field session in the Aosta Valley</div>
    </div>
  </div>
</div>

<div class="conf-section-title">National Conferences</div>

<div class="conf-card">
  <div class="conf-title">Record-breaking April to May 2024 Heatwave in West Bengal: Multi-parameter Assessment</div>
  <div class="conf-venue">ISG-ISRS National Symposium 2025, IIT Kharagpur Research Park, Kolkata, India &nbsp;|&nbsp; November 25 to 27, 2025</div>
  <span class="conf-badge badge-oral">Oral Presentation</span>
  <div class="conf-desc">
    Presented multi-parameter assessment of intensity, duration, and land-atmosphere anomalies 
    during the record-breaking April to May 2024 heatwave in West Bengal.
  </div>
</div>

<div class="conf-card">
  <div class="conf-title">Changing Patterns of Extreme Rainfall Events in the Northwest Himalayas</div>
  <div class="conf-venue">Biodiversity and Climate Change (BDCC), IIT Kharagpur, India &nbsp;|&nbsp; February 16 to 19, 2023</div>
  <span class="conf-badge badge-oral">Paper Presentation</span>
  <div class="conf-desc">
    Paper presentation on changing patterns of extreme rainfall events in the Northwest Himalayas.
  </div>
</div>

<div id="lb-overlay">
  <span id="lb-hint">scroll to zoom · click outside to close</span>
  <img id="lb-img" src="" alt="">
  <div id="lb-cap"></div>
</div>

<script>
(function () {
  var overlay = document.getElementById('lb-overlay');
  var img     = document.getElementById('lb-img');
  var cap     = document.getElementById('lb-cap');
  var scale = 1, tx = 0, ty = 0, dragging = false, sx = 0, sy = 0;

  function apply() {
    img.style.transform = 'translate(' + tx + 'px,' + ty + 'px) scale(' + scale + ')';
  }

  function open(src, text) {
    img.src = src;
    cap.textContent = text || '';
    scale = 1; tx = 0; ty = 0; apply();
    overlay.classList.add('open');
    document.body.style.overflow = 'hidden';
  }

  function close() {
    overlay.classList.remove('open');
    document.body.style.overflow = '';
    img.src = '';
  }

  document.querySelectorAll('.shot-frame').forEach(function (el) {
    el.addEventListener('click', function () {
      open(el.getAttribute('data-full'), el.getAttribute('data-cap'));
    });
  });

  overlay.addEventListener('click', function (e) {
    if (e.target === overlay) close();
  });

  document.addEventListener('keydown', function (e) {
    if (e.key === 'Escape' && overlay.classList.contains('open')) close();
  });

  overlay.addEventListener('wheel', function (e) {
    if (!overlay.classList.contains('open')) return;
    e.preventDefault();
    var next = scale * (e.deltaY < 0 ? 1.15 : 1 / 1.15);
    scale = Math.min(6, Math.max(1, next));
    if (scale === 1) { tx = 0; ty = 0; }
    apply();
  }, { passive: false });

  img.addEventListener('mousedown', function (e) {
    if (scale === 1) return;
    e.preventDefault();
    dragging = true; sx = e.clientX - tx; sy = e.clientY - ty;
    img.classList.add('panning');
  });

  window.addEventListener('mousemove', function (e) {
    if (!dragging) return;
    tx = e.clientX - sx; ty = e.clientY - sy; apply();
  });

  window.addEventListener('mouseup', function () {
    dragging = false; img.classList.remove('panning');
  });

  img.addEventListener('dblclick', function () {
    scale = 1; tx = 0; ty = 0; apply();
  });
})();
</script>
