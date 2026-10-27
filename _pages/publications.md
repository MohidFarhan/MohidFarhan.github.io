---
layout: page
permalink: /publications/
title: Scholarly Works
description: Peer-reviewed publications, preprints, and pedagogical notes.
nav: true
nav_order: 3
---

{% include bib_search.liquid %}

<div class="publications">

<div class="header-bar" style="text-align: left; margin-top: 2rem; margin-bottom: 1rem;">
  <h2 style="font-weight: bold;">Peer-Reviewed Publications</h2>
</div>
{% bibliography --query @*[keywords=published] %}

<div class="header-bar" style="text-align: left; margin-top: 2rem; margin-bottom: 1rem;">
  <h2 style="font-weight: bold;">Under Review</h2>
</div>
{% bibliography --query @*[keywords=preprint] %}

<div class="header-bar" style="text-align: left; margin-top: 2rem; margin-bottom: 1rem;">
  <h2 style="font-weight: bold;">Pedagogical Notes</h2>
</div>
{% bibliography --query @*[keywords=notes] %}

</div>