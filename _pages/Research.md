---
layout: archive
title: ""
permalink:  /research/
author_profile: true
---
<style>
.rx-flow{display:flex;flex-wrap:wrap;gap:.5em;margin:1em 0}
.rx-flow span{background:#f1f3f5;border-radius:999px;padding:.3em .9em;font-size:.85em}
.rx-fig{text-align:center;margin:1.4em 0}
.rx-fig img{max-width:100%;border-radius:6px;box-shadow:0 1px 6px rgba(0,0,0,.12)}
.rx-fig figcaption{font-family:inherit;font-size:.8em;color:#555;margin-top:.5em;text-align:left}
.archive a{overflow-wrap:anywhere}
</style>

PhD Research
======

A Framework to Support Functional Recovery-Based Design in a Multi-Hazard Context
------

How long does a steel building take to regain its function after an earthquake, and how much longer if a fire follows the shaking? My PhD develops a framework to answer this and turn it into design guidance.

<figure class="rx-fig">
  <img src="/images/research/fr-eq-vs-ffe.png" alt="Building function over time after an earthquake alone versus an earthquake followed by fire">
  <figcaption>Building function over time after (a) an earthquake and (b) an earthquake followed by fire. The shaded area is the function lost to fire.</figcaption>
</figure>

Functional recovery with Pelicun + ATC-138
------

I linked FEMA P-58 damage and loss assessment in Pelicun to the ATC-138 functional recovery framework and applied it to a steel moment-resisting frame inventory.

<div class="rx-flow"><span>Response</span><span>&rarr;</span><span>Damage &amp; loss (Pelicun)</span><span>&rarr;</span><span>Interface</span><span>&rarr;</span><span>Recovery (ATC-138)</span></div>

<figure class="rx-fig" style="max-width:640px;margin-left:auto;margin-right:auto">
  <img src="/images/research/pelicun-atc138-interface.png" alt="Pelicun to ATC-138 interface">
  <figcaption>The Pelicun&ndash;ATC-138 interface.</figcaption>
</figure>

How modeling decisions change seismic loss estimates
------

I compared three seismic loss methods (FEMA P-58 component-based, HAZUS assembly-based and story loss functions) on 621 steel moment frames. I also tested how analyst choices in the fragility and loss steps change the results.

<figure class="rx-fig">
  <img src="/images/research/loss-methods-flowchart.png" alt="Flowchart comparing seismic loss methodologies and sensitivity analyses">
  <figcaption>Comparison and sensitivity analysis of seismic loss assessment methods.</figcaption>
</figure>

<figure class="rx-fig" style="max-width:640px;margin-left:auto;margin-right:auto">
  <img src="/images/research/loss-methods-eal.png" alt="Normalized expected annual loss by method and number of stories">
  <figcaption>Normalized expected annual loss by method and building height.</figcaption>
</figure>

* The assembly-based method gives lower losses for short buildings, higher losses for tall ones, and about 3 times more variability.
* Story loss functions give about 16% lower losses than FEMA P-58 for multi-story buildings.
* The most critical decision depends on the method: EDP statistics for HAZUS, nonstructural quantities for FEMA P-58, and the IM-EDP model for story loss functions.

Earthquake-related carbon emissions
------

Earthquakes also cost carbon, because every repair needs new material. I estimated earthquake-related global warming potential (GWP) for 60 steel moment frames and compared a detailed repair-based LCA with simpler repair-cost-ratio methods.

<figure class="rx-fig">
  <img src="/images/research/carbon-methods-flowchart.png" alt="Flowchart linking seismic loss assessment to life cycle carbon emissions">
  <figcaption>Linking seismic loss assessment to life cycle environmental impact.</figcaption>
</figure>

<figure class="rx-fig">
  <img src="/images/research/carbon-gwp-results.png" alt="Earthquake-related GWP by building height and share of total embodied GWP">
  <figcaption>(a) Earthquake-related GWP by building height. (b) Its share of total embodied GWP for each method.</figcaption>
</figure>

* Earthquake-related GWP adds **20% to 72%** of a building's total embodied carbon.
* Simplified methods can overestimate it, up to 20 times for HAZUS in 19-story buildings. Story loss functions match the detailed approach best.

<figure class="rx-fig">
  <img src="/images/research/carbon-nonstructural.png" alt="Initial and earthquake-related GWP of structural and nonstructural components">
  <figcaption>(a) Initial and (b) earthquake-related GWP of structural and nonstructural components. (c) Earthquake-related GWP by component.</figcaption>
</figure>

* Nonstructural components are only 15% of initial carbon but cause about **10 times more** earthquake-related carbon than the structure. Gypsum walls and fa&ccedil;ades alone exceed all structural components by 3 to 6 times.

<figure class="rx-fig" style="max-width:640px;margin-left:auto;margin-right:auto">
  <img src="/images/research/carbon-design-correlation.png" alt="Spearman correlation between design parameters and carbon and loss metrics">
  <figcaption>Spearman correlation between design parameters and initial, earthquake-related and total GWP, and expected annual loss (EAL).</figcaption>
</figure>

* Seismic design parameters strongly reduce expected annual loss (&#124;&rho;&#124; = 0.55&ndash;0.87) but barely change earthquake-related carbon (&#124;&rho;&#124; &lt; 0.31). Cutting that carbon needs more resilient nonstructural components, not just a stronger frame.

Relevant Publications
------
1. Zaker Esteghamati, M., & **Baddipalli, S.** (2026). An ensemble learning-based approach to quantify post-earthquake functional recovery of a steel moment-resisting frame inventory. *Infrastructures*, 11(7), 213.
2. **Baddipalli, S.**, & Zaker Esteghamati, M. (2026). Sensitivity of post-earthquake functional recovery to modeling and design decisions in steel frame buildings. *AEI and IRD 2026: Hazard Resilience for an Integrated World*, ASCE, 305&ndash;312.
3. **Baddipalli, S.**, Leavitt, N., & Zaker Esteghamati, M. (2026). Quantifying the earthquake-related carbon emissions of steel moment-resisting framed buildings and their sensitivity to modeling and design decisions. *Journal of Building Engineering*, 125, 116190. [https://doi.org/10.1016/j.jobe.2026.116190](https://doi.org/10.1016/j.jobe.2026.116190)
4. **Baddipalli, S.**, Gentile, R., O'Reilly, G. J., Shahnazaryan, D., & Zaker Esteghamati, M. (2025). Impact of modeling decisions on seismic loss and fragility assessment of steel buildings. *Earthquake Spectra*, 41(5), 3858&ndash;3881. [https://doi.org/10.1177/87552930251360751](https://doi.org/10.1177/87552930251360751)

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
