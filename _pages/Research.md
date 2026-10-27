---
layout: archive
title: ""
permalink:  /research/
author_profile: true
---
<style>
.rx-lead{font-size:1.05em;line-height:1.6}
.rx-q{border-left:4px solid #e8590c;background:#fff4e6;padding:.8em 1.1em;margin:1.2em 0;border-radius:4px}
.rx-flow{display:grid;grid-template-columns:repeat(auto-fit,minmax(170px,1fr));gap:.7em;margin:1.4em 0;counter-reset:x}
.rx-step{min-width:0;border-radius:8px;padding:.8em .9em;font-size:.82em;line-height:1.4;color:#222;position:relative}
.rx-step b{display:block;font-size:1.05em;margin-bottom:.3em}
.rx-step .n{display:inline-block;width:1.6em;height:1.6em;border-radius:50%;background:#fff;text-align:center;line-height:1.6em;font-weight:700;margin-bottom:.4em}
.s1{background:#e7f5ff}.s2{background:#e6fcf5}.s3{background:#fff9db}.s4{background:#f3f0ff}.s5{background:#ffe8cc}.s6{background:#fff0f6}
.rx-stats{display:flex;flex-wrap:wrap;gap:.8em;margin:1.2em 0}
.rx-stat{flex:1 1 140px;min-width:0;border:1px solid #e5e5e5;border-radius:8px;padding:.8em;text-align:center}
.rx-stat .v{font-size:1.7em;font-weight:700;color:#1c7ed6;line-height:1.1}
.rx-stat .l{font-size:.75em;color:#555;margin-top:.3em}
.rx-obj{border:1px solid #e5e5e5;border-radius:8px;padding:.9em 1.1em;margin:1em 0}
.rx-obj h3{margin:.1em 0 .4em;font-size:1.05em}
.rx-tag{display:inline-block;font-size:.7em;font-weight:700;padding:.15em .6em;border-radius:999px;margin-left:.4em;vertical-align:middle}
.t-done{background:#d3f9d8;color:#2b8a3e}.t-prog{background:#fff3bf;color:#e67700}.t-next{background:#e7f5ff;color:#1864ab}
.rx-fig{text-align:center;margin:1.4em 0}
.rx-fig img{max-width:100%;border-radius:6px;box-shadow:0 1px 6px rgba(0,0,0,.12)}
.rx-fig figcaption{font-family:inherit;font-size:.8em;color:#555;margin-top:.5em;text-align:left}
details.rx-more{margin:1em 0;border:1px solid #e5e5e5;border-radius:8px;padding:.6em 1em}
details.rx-more summary{cursor:pointer;font-weight:600}
.archive a{overflow-wrap:anywhere}
</style>

PhD Research
======

A Framework to Support Functional Recovery-Based Design in a Multi-Hazard Context
------

<p class="rx-lead">Modern buildings are designed so people get out alive after an earthquake. But the bigger loss for a community is often what comes next: offices, homes and hospitals that stay closed for months. My PhD, at the <b>StocStruct Computational Lab, Utah State University</b> (advisor: Dr. Mohsen Zaker Esteghamati), asks a simple question: <b>how long does a steel building take to get back to work after an earthquake, and how much longer if a fire follows the shaking?</b></p>

<div class="rx-q">The 1906 San Francisco earthquake set off fires that destroyed 28,000 buildings. After the 1995 Kobe earthquake, fires burned over 1 million m&sup2; of floor area. Yet today's recovery tools treat the earthquake as the last event.</div>

<figure class="rx-fig">
  <img src="/images/research/fr-eq-vs-ffe.png" alt="Building function over time after an earthquake alone versus an earthquake followed by fire">
  <figcaption><b>The big picture.</b> Building function over time after (a) an earthquake and (b) an earthquake followed by fire. Fire ignites before repairs begin. If it spreads, fire investigation, smoke and hazardous-material cleanup, assessment of fire-damaged steel, insurance settlement and re-certification of fire protection delay every recovery state. The shaded area is the function lost to fire, which my research quantifies.</figcaption>
</figure>

How I model functional recovery: Pelicun + ATC-138
------

I built a pipeline that links **FEMA P-58** damage and loss assessment in **Pelicun** (NHERI SimCenter) to the **ATC-138 / PBEE-Recovery** functional recovery framework, and ran it on an inventory of steel moment-resisting frames.

<div class="rx-flow">
  <div class="rx-step s1"><span class="n">1</span><b>Building inventory</b>100 steel SMRFs, 1 to 19 stories, with OpenSees nonlinear models (Guan et al.)</div>
  <div class="rx-step s2"><span class="n">2</span><b>Response</b>Nonlinear time-history analysis gives story drift, floor acceleration and residual drift</div>
  <div class="rx-step s3"><span class="n">3</span><b>Damage &amp; loss (Pelicun)</b>FEMA P-58 fragilities, 10,000 Monte Carlo realizations per building: damaged quantities, repair cost and worker-days per floor</div>
  <div class="rx-step s4"><span class="n">4</span><b>Interface</b>Damage mapped to functional systems, red tags, inspection triggers and racked stair doors, then packed into ATC-138 inputs</div>
  <div class="rx-step s5"><span class="n">5</span><b>Recovery (ATC-138)</b>Fault trees decide re-occupancy and function; impeding factors and repair scheduling give the timeline</div>
  <div class="rx-step s6"><span class="n">6</span><b>Insight</b>Sensitivity analysis and explainable ML (random forest + SHAP) find what drives downtime</div>
</div>

<figure class="rx-fig">
  <img src="/images/research/pelicun-atc138-interface.png" alt="Pelicun to ATC-138 interface" style="max-width:640px">
  <figcaption><b>The Pelicun&ndash;ATC-138 interface I developed.</b> FEMA P-58 damage from Pelicun is mapped into the building function and recovery time modules of ATC-138, together with building, tenant, impedance, repair-time and functionality options.</figcaption>
</figure>

<details class="rx-more"><summary>See the full workflow and the ATC-138 fault tree</summary>
<figure class="rx-fig">
  <img src="/images/research/recovery-methodology.png" alt="PBEE to ATC-138 methodology with sensitivity analysis">
  <figcaption>End-to-end methodology: PBEE (response, fragility, loss) feeds ATC-138 functional recovery, followed by sensitivity analysis of modeling and design parameters.</figcaption>
</figure>
<figure class="rx-fig">
  <img src="/images/research/atc138-fault-tree.png" alt="ATC-138 building function fault tree" style="max-width:640px">
  <figcaption>ATC-138 building function module (Cook et al., 2022): building safety, story access, tenant safety and tenant function decide re-occupancy and function. I am extending each stage with fire-induced branches.</figcaption>
</figure>
</details>

### What we found (earthquake only)

<div class="rx-stats">
  <div class="rx-stat"><div class="v">127 days</div><div class="l">median functional recovery at the design earthquake (DBE)</div></div>
  <div class="rx-stat"><div class="v">158 days</div><div class="l">median functional recovery at the maximum considered earthquake (MCE)</div></div>
  <div class="rx-stat"><div class="v">+33&ndash;35%</div><div class="l">recovery time when impeding delays go from 80% to 140% of baseline</div></div>
  <div class="rx-stat"><div class="v">R&sup2; = 0.94</div><div class="l">random forest prediction of recovery time at MCE</div></div>
</div>

* **Tall buildings stay closed longest:** 14 to 19 story buildings need a median of 144 days (DBE) and 187 days (MCE) to regain function.
* **Pooled design trends can mislead:** across the whole inventory, larger design drift seems to shorten recovery, but that is a height effect. Within one-story buildings, higher design drift lengthens recovery.
* **A few design parameters predict recovery:** SHAP shows building weight, floor area, bay width and strong-column weak-beam ratio govern recovery time.

<figure class="rx-fig">
  <img src="/images/research/recovery-shap.png" alt="SHAP feature importance for functional recovery time">
  <figcaption>Mean absolute SHAP value of each design feature in the random forest model of functional recovery time at DBE and MCE.</figcaption>
</figure>

Adding fire: fire following earthquake
------

The same shaking that damages a building also breaks partitions, glazing, ceilings, fireproofing and the sprinkler water supply that are supposed to contain a fire. I built a building-scale FFE model of a **19-story steel SMRF with 475 compartments**, analyzed under **354 ground motions with 100 fire realizations each**. Drift and acceleration from OpenSees drive ignition, nonstructural damage and the survival of every link in the sprinkler chain (water source, fire pump, standpipe risers, branch lines, heads). OZone compartment fires then spread minute by minute for 3 hours.

<figure class="rx-fig">
  <img src="/images/research/ffe-simulation-workflow.png" alt="Fire following earthquake simulation workflow">
  <figcaption>FFE simulation: earthquake shaking, fire ignition, fire barrier damage, sprinkler system damage, fire spread, and fragility with its main drivers.</figcaption>
</figure>

* **The water supply, not the sprinkler head, decides how much burns.** In one design-level record, modeling sprinkler survival cut burned compartments from 475 to 113. Riser failure alone burns 14% of the building; heads and branch lines add under 1% each.
* **Fire spreads fast.** About 70% of the final burned area is reached within the first hour.
* **Shaking intensity alone is a poor predictor.** Burned fraction tracks the number of ignited floors far better than spectral acceleration.

<figure class="rx-fig">
  <img src="/images/research/ffe-fragility.png" alt="Fire following earthquake attribution and fragility curves">
  <figcaption>(a, b) Increase in burned fraction when a single sprinkler, barrier or spread-rule component fails. (c) Preliminary FFE fragility curves for 10%, 25% and 50% of the building burned.</figcaption>
</figure>

Research roadmap
------

<div class="rx-obj"><h3>1. Earthquake-only functional recovery <span class="rx-tag t-done">COMPLETE</span></h3>Pelicun&ndash;ATC-138 interface for 100 steel SMRFs, sensitivity analysis, and explainable ML surrogates of recovery time.</div>
<div class="rx-obj"><h3>2. Functional recovery under fire following earthquake <span class="rx-tag t-prog">IN PROGRESS</span></h3>FFE spread and fragility are done. Next: carry combined earthquake and fire damage into ATC-138 with fire branches in the fault trees, fire-specific impeding factors (fire investigation, smoke and hazardous-material remediation, air-quality clearance, insurance) and fire-restoration repair sequencing, to measure the downtime fire adds.</div>
<div class="rx-obj"><h3>3. Recovery-based design under earthquake and FFE <span class="rx-tag t-next">NEXT</span></h3>An open database of about 850 redesigned SMRFs (drift limit, strong-column weak-beam ratio, importance factor) and explainable surrogates inverted into <b>recovery-based design charts</b>: read off the drift limit and fire-protection measures needed for a target such as 30-day functional recovery.</div>

All models, data and code will be released openly on NHERI DesignSafe. This work is in collaboration with Dr. Negar Elhami-Khorasani (University at Buffalo).

Relevant Publications
------
1. Zaker Esteghamati, M., & **Baddipalli, S.** (2026). An ensemble learning-based approach to quantify post-earthquake functional recovery of a steel moment-resisting frame inventory. *Infrastructures*, 11(7), 213.
2. **Baddipalli, S.**, & Zaker Esteghamati, M. (2026). Sensitivity of post-earthquake functional recovery to modeling and design decisions in steel frame buildings. *AEI and IRD 2026: Hazard Resilience for an Integrated World*, ASCE, 305&ndash;312.
3. **Baddipalli, S.**, Elhami-Khorasani, N., & Zaker Esteghamati, M. (2026). A multi-hazard computational approach for damage assessment of steel buildings under fire-following-earthquake scenarios. *NHERI Computational Symposium 2026*, UC Berkeley. (Oral presentation)
4. **Baddipalli, S.**, & Zaker Esteghamati, M. (2025). Influence of analysis decisions on post-earthquake functional recovery of a steel frame building inventory. *ICOSSAR 2025*, Los Angeles. (Oral presentation)

See the full list on my [Publications](/publications/) page.

Master's Research:
======

Influence of Masonry Infills on Blast Response of Earthquake-Resistant RC Buildings
======

Team
======
1. Shiva Baddipalli, Project Associate, IIT Mandi
2. Mahipal Khulariya, PhD Research Scholar, IIT Mandi
3. Dr Sandip Kumar Saha, Assistant Professor, IIT Mandi

Description
======
This study aims to investigate the influence of the masonry infill strength on the blast performance of the masonry infilled RC buildings designed to withstand different levels of seismic demand. Based on the extensive literature review, the specific objectives of this study are: (i) to examine the effect of the infill’s nonlinearity on the blast response of the earthquake-resistant RC buildings, and (ii) to probabilistically assess the effect of infill panel strength and seismic design level on the blast response of the considered buildings subjected to the surface burst. It is observed that the consideration of infill’s nonlinearity influences the blast response up to a certain scaled distance only. Moreover, increasing the infill strength does not necessarily enhance the blast performance; however, designing the building to higher seismic demand results in improved blast performance. In addition, proper insight into seismic design level and infill strength of any RC building is required prior to plan and design them with suitable blast-mitigation measures.

![Editing a markdown file for a talk](/images/Graphical_Abstract_PNG.png)

Relevant Publications
======
1. Baddipalli, S., Kulariya, M., & Saha, S. K. (2023). Influence of Masonry Infills on Blast Response of Earthquake-Resistant Reinforced Concrete Buildings Structures. Structures, 50, 908-924. [https://doi.org/10.1016/j.istruc.2023.02.078](https://www.sciencedirect.com/science/article/abs/pii/S2352012423002369)

Construction Practices and Seismic Vulnerability of Buildings in Indian Himalayan Region: A Case Study
======

Team
======
1. Yati Aggarwal, PhD Research Scholar, IIT Mandi
2. Shiva Baddipalli, Project Associate, IIT Mandi
3. Dr Sandip Kumar Saha, Assistant Professor, IIT Mandi

Description
======
Due to rapid growth in tourism and other economic activities, several small cities and towns in the Indian Himalayan region are facing problem of unplanned construction and extended use of deteriorating old structures. Despite being in the most active zone of seismic activity, significant non-engineered construction is practiced in this region. Hence, it becomes essential to examine the existing engineered and non-engineered building typologies and assess their vulnerabilities against earthquake shaking. This study presents typical engineered and non-engineered construction practices observed through a survey of 1009 buildings located within Mandi, a small town in the lap of the great Himalayas in the Indian state of Himachal Pradesh. An attempt is made to identify the typical building typologies, visible structural irregular features and their seismic vulnerability. A few building typologies are found typically predominantly prevail in northern zone of Indian Himalayan region. Rapid visual screening (RVS) of the surveyed buildings is performed using different existing guidelines. It is observed that a substantial number of buildings with hybrid typology (stone masonry mixed with brick masonry or reinforced concrete) are prevailing in the study area. It is also observed that the seismic vulnerability, as per the adopted RVS guidelines, of majority of the buildings is high, indicating urgent demand for safeguarding the vulnerable built environment and develop the framework for seismic resilient society. It is further concluded that use of region-specific vulnerability attributes can improve the segregate of buildings based on the expected damage.

Relevant Publications
======
1. Aggarwal, Y., Baddipalli, S., & Saha, S. K. (2023). Construction Practices and Seismic Vulnerability of Buildings in Indian Himalayan Region: A Case Study. Natural Hazards Review, 25(2), p.05024002.[https://doi.org/10.1061/NHREFO.NHENG-1902](https://ascelibrary.org/doi/10.1061/NHREFO.NHENG-1902)
