---
permalink: /
title: "Anup Upadhyaya"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
/* ── Intro ── */
.intro-text {
  font-size: 0.95em;
  line-height: 1.8;
  color: var(--global-text-color);
  margin-bottom: 1.5em;
  padding-left: 28px;
  text-align: justify;
}
.intro-text a {
  color: #2a7ae2;
  text-decoration: none;
  border-bottom: 1px dashed rgba(42,122,226,0.4);
}
.intro-text a:hover {
  border-bottom-color: #2a7ae2;
}

/* ── Section Titles ── */
.about-section-title {
  font-size: 1.15em;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin: 2.2em 0 1em;
  padding-bottom: 6px;
  padding-left: 28px;
  border-bottom: 2px solid var(--global-border-color);
  color: var(--global-text-color);
}

/* ── Research Card ── */
.research-card {
  padding: 1.3em 1.5em;
  background: rgba(42,122,226,0.04);
  border-left: 4px solid #2a7ae2;
  border-radius: 0 6px 6px 0;
  margin-bottom: 1.5em;
  line-height: 1.75;
  font-size: 0.93em;
  color: var(--global-text-color);
  text-align: justify;
}
.research-points {
  list-style: none;
  padding: 0;
  margin: 1em 0 0;
}
.research-points li {
  font-size: 0.92em;
  color: var(--global-text-color);
  opacity: 0.85;
  padding: 4px 0 4px 18px;
  position: relative;
  line-height: 1.6;
  text-align: justify;
}
.research-points li::before {
  content: "▸";
  position: absolute;
  left: 0;
  color: #2a7ae2;
  opacity: 0.6;
}

/* ── Education Cards ── */
.edu-card {
  padding: 1em 1.2em;
  margin-bottom: 10px;
  border-left: 4px solid #ccc;
  background: rgba(128,128,128,0.04);
  border-radius: 0 6px 6px 0;
  transition: all 0.25s ease;
}
.edu-card:hover {
  transform: translateX(3px);
  box-shadow: 0 2px 10px rgba(0,0,0,0.06);
}
.edu-card.highlight {
  border-left-color: #2a7ae2;
  background: rgba(42,122,226,0.04);
}
.edu-degree {
  font-weight: 600;
  font-size: 0.95em;
  color: var(--global-text-color);
}
.edu-meta {
  font-size: 0.84em;
  color: var(--global-text-color);
  opacity: 0.6;
  margin-top: 2px;
}
.edu-note {
  font-size: 0.8em;
  color: #2a7ae2;
  margin-top: 2px;
}

/* ── Work Cards ── */
.work-card {
  padding: 1.2em 1.4em;
  margin-bottom: 12px;
  border-left: 4px solid #ccc;
  background: rgba(128,128,128,0.04);
  border-radius: 0 6px 6px 0;
  transition: all 0.25s ease;
}
.work-card:hover {
  transform: translateX(3px);
  box-shadow: 0 2px 10px rgba(0,0,0,0.06);
}
.work-card.featured {
  border-left-color: #2a7ae2;
  background: rgba(42,122,226,0.04);
}
.work-title {
  font-weight: 600;
  font-size: 0.95em;
  color: var(--global-text-color);
}
.work-org {
  font-size: 0.85em;
  color: var(--global-text-color);
  opacity: 0.65;
  margin: 2px 0 8px;
}
.work-points {
  list-style: none;
  padding: 0;
  margin: 0;
}
.work-points li {
  font-size: 0.85em;
  color: var(--global-text-color);
  opacity: 0.8;
  padding: 3px 0 3px 18px;
  position: relative;
  line-height: 1.55;
  text-align: justify;
}
.work-points li::before {
  content: "▸";
  position: absolute;
  left: 0;
  color: #2a7ae2;
  opacity: 0.6;
}

/* ── Achievements ── */
.achieve-wrapper {
  padding-left: 28px;
}
.achieve-item {
  display: flex;
  align-items: flex-start;
  gap: 12px;
  padding: 10px 0;
  border-bottom: 1px solid rgba(128,128,128,0.08);
  font-size: 0.9em;
  color: var(--global-text-color);
}
.achieve-item:last-child {
  border-bottom: none;
}
.achieve-text {
  flex: 1;
  line-height: 1.55;
}
.achieve-text strong {
  color: var(--global-text-color);
}
.achieve-year {
  font-size: 0.8em;
  opacity: 0.5;
  white-space: nowrap;
}

/* ── Skills ── */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 12px;
  margin-top: 10px;
}
.skill-group {
  padding: 1em 1.2em;
  background: rgba(128,128,128,0.04);
  border-radius: 6px;
  border: 1px solid rgba(128,128,128,0.08);
}
.skill-label {
  font-size: 0.75em;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  color: var(--global-text-color);
  opacity: 0.5;
  margin-bottom: 8px;
}
.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
}
.skill-tag {
  display: inline-block;
  font-size: 0.78em;
  padding: 4px 12px;
  border-radius: 20px;
  background: rgba(42,122,226,0.08);
  color: #2a7ae2;
  font-weight: 500;
}

/* ── Responsive ── */
@media (max-width: 600px) {
  .intro-text,
  .about-section-title,
  .achieve-wrapper {
    padding-left: 0;
  }
  .skills-grid {
    grid-template-columns: 1fr;
  }
  .achieve-item {
    flex-direction: column;
    gap: 4px;
  }
}
</style>

<div class="intro-text">
I am a PhD Candidate (<strong>Prime Minister's Research Fellow</strong>) at the Centre for Ocean, 
River, Atmosphere and Land Sciences (CORAL), 
<a href="https://www.iitkgp.ac.in" target="_blank"><strong>Indian Institute of Technology Kharagpur</strong></a>, 
India (2019 to present), working under the supervision of 
<a href="https://www.iitkgp.ac.in/department/CL/faculty/cl-abhishek" target="_blank">Dr. Abhishek K. Rai</a>.
<br><br>
My research addresses the growing threat of <strong>climate extremes and associated natural hazards</strong> 
in the Northwest Himalayan region of India, integrating statistical analysis, machine learning, 
geospatial modelling, and hydrodynamic simulations to understand and anticipate disaster risk 
in one of the world's most climate-sensitive landscapes.
</div>

<div class="about-section-title">PhD Research</div>

<div class="research-card">
The Himalayas are warming fast, and my work tries to understand what that means for the 
people living downstream.
<br><br>
I study how heatwaves and extreme rainfall have changed across the Northwest Himalayas, 
and where they are headed under future climate scenarios. From there, I look at what 
these extremes trigger on the ground: unstable slopes, dangerous glacial lakes, and 
catastrophic floods.
<br><br>
The work moves from atmosphere to hillslope to river valley, using climate models, 
machine learning, remote sensing, and flood simulation to connect a warming climate 
to real risks faced by Himalayan communities.

<ul class="research-points">
  <li>Investigated heatwaves, extreme precipitation, glacial lake outburst floods, and landslide susceptibility across the Northwest Himalayas</li>
  <li>Applied machine learning methods (Random Forest, XGBoost, SVM) for spatial susceptibility mapping of landslides and glacial lake hazards</li>
  <li>Processed satellite and reanalysis datasets including Landsat, Sentinel-2, MODIS, and ERA5 using Python and Google Earth Engine</li>
  <li>Analysed CMIP6 projections under multiple SSP scenarios and applied causal discovery methods including PCMCI+</li>
  <li>Performed WRF simulations on IIT Kharagpur's Param Shakti HPC facility and conducted HEC-RAS 2D hydrodynamic modelling for glacial lake flood propagation</li>
</ul>
</div>

<div class="about-section-title">Education</div>

<div class="edu-card highlight">
  <div class="edu-degree">Ph.D. in Climate Change & Extreme Events</div>
  <div class="edu-meta">IIT Kharagpur &nbsp;|&nbsp; 2019 to Present</div>
  <div class="edu-note">Prime Minister's Research Fellow</div>
</div>

<div class="edu-card">
  <div class="edu-degree">M.Sc. Applied Geology</div>
  <div class="edu-meta">University of Mysore &nbsp;|&nbsp; 2017 to 2019</div>
  <div class="edu-note">Gold Medallist &nbsp;·&nbsp; CGPA: 8.62</div>
</div>

<div class="edu-card">
  <div class="edu-degree">M.Sc. Geoinformatics</div>
  <div class="edu-meta">BIT Mesra, Ranchi &nbsp;|&nbsp; 2012 to 2014</div>
  <div class="edu-note">CGPA: 8.64</div>
</div>

<div class="edu-card">
  <div class="edu-degree">B.Sc. Hons. Geology</div>
  <div class="edu-meta">University of Delhi &nbsp;|&nbsp; 2009 to 2012</div>
</div>

<div class="about-section-title">Work Experience</div>

<div class="work-card featured">
  <div class="work-title">Consultant (Statistical Analyst)</div>
  <div class="work-org">Ministry of Environment, Forest and Climate Change (MoEFCC), New Delhi &nbsp;|&nbsp; June to September 2025</div>
  <ul class="work-points">
    <li>Analysed global indices including the Environmental Performance Index and Climate Change Performance Index</li>
    <li>Reviewed UN technical reports and provided statistical inputs for national climate assessments</li>
  </ul>
</div>

<div class="work-card featured">
  <div class="work-title">PhD Research Fellow</div>
  <div class="work-org">IIT Kharagpur &nbsp;|&nbsp; July 2019 to Present</div>
  <ul class="work-points">
    <li>Statistical analysis of extreme climate events, GLOFs, and landslide susceptibility in the NW Himalayas</li>
    <li>High-performance computing using IIT Kharagpur's Param Shakti facility (WRF model runs)</li>
  </ul>
</div>

<div class="work-card">
  <div class="work-title">Junior Research Fellow</div>
  <div class="work-org">G.B. Pant National Institute of Himalayan Environment, Almora &nbsp;|&nbsp; December 2014 to July 2015</div>
  <ul class="work-points">
    <li>Forest cover modelling using remote sensing and GIS for Manas Biosphere Reserve, Assam</li>
  </ul>
</div>

<div class="about-section-title">Academic Achievements</div>

<div class="achieve-wrapper">
  <div class="achieve-item">
    <div class="achieve-text"><strong>Prime Minister's Research Fellow</strong></div>
    <div class="achieve-year">December 2020</div>
  </div>

  <div class="achieve-item">
    <div class="achieve-text"><strong>Best Oral Presentation Award</strong> &nbsp;|&nbsp; Research Scholar Day, CORAL, IIT Kharagpur</div>
    <div class="achieve-year">January 2024</div>
  </div>

  <div class="achieve-item">
    <div class="achieve-text"><strong>Gold Medal</strong> &nbsp;|&nbsp; M.Sc. Applied Geology, University of Mysore</div>
    <div class="achieve-year">2019</div>
  </div>

  <div class="achieve-item">
    <div class="achieve-text"><strong>GATE 2019</strong> &nbsp;|&nbsp; AIR 430, Score 487</div>
    <div class="achieve-year">2019</div>
  </div>

  <div class="achieve-item">
    <div class="achieve-text"><strong>KSET 2018</strong> &nbsp;|&nbsp; Karnataka State Eligibility Test for Lectureship</div>
    <div class="achieve-year">2018</div>
  </div>
</div>

<div class="about-section-title">Skills</div>

<div class="skills-grid">
  <div class="skill-group">
    <div class="skill-label">Programming</div>
    <div class="skill-tags">
      <span class="skill-tag">Python</span>
      <span class="skill-tag">R</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-label">Python Libraries</div>
    <div class="skill-tags">
      <span class="skill-tag">scikit-learn</span>
      <span class="skill-tag">pandas</span>
      <span class="skill-tag">xarray</span>
      <span class="skill-tag">rasterio</span>
      <span class="skill-tag">matplotlib</span>
      <span class="skill-tag">numpy</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-label">Geospatial Tools</div>
    <div class="skill-tags">
      <span class="skill-tag">ArcGIS</span>
      <span class="skill-tag">QGIS</span>
      <span class="skill-tag">SNAP</span>
      <span class="skill-tag">Google Earth Engine</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-label">Satellite Data</div>
    <div class="skill-tags">
      <span class="skill-tag">Landsat</span>
      <span class="skill-tag">Sentinel-2</span>
      <span class="skill-tag">MODIS</span>
      <span class="skill-tag">ASTER DEM</span>
      <span class="skill-tag">SRTM</span>
      <span class="skill-tag">ALOS PALSAR</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-label">Reanalysis & Climate Data</div>
    <div class="skill-tags">
      <span class="skill-tag">ERA5</span>
      <span class="skill-tag">ERA5-Land</span>
      <span class="skill-tag">CMIP6</span>
      <span class="skill-tag">SSP Scenarios</span>
      <span class="skill-tag">Bias Correction</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-label">Modelling</div>
    <div class="skill-tags">
      <span class="skill-tag">WRF</span>
      <span class="skill-tag">HEC-RAS 2D</span>
      <span class="skill-tag">Random Forest</span>
      <span class="skill-tag">XGBoost</span>
      <span class="skill-tag">SVM</span>
      <span class="skill-tag">MCDM</span>
    </div>
  </div>
  <div class="skill-group">
    <div class="skill-label">Other</div>
    <div class="skill-tags">
      <span class="skill-tag">Param Shakti HPC</span>
      <span class="skill-tag">DGPS Surveying</span>
    </div>
  </div>
</div>
