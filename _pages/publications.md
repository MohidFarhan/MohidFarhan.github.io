---
layout: page
permalink: /publications/
title: Scholarly Works
description: Peer-reviewed publications, preprints, and pedagogical notes.
nav: true
nav_order: 3
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

<h2 class="bibliography">Peer-Reviewed Publications</h2>

{% bibliography --query @*[keywords=published] %}

<h2 class="bibliography">Under Review</h2>

{% bibliography --query @*[keywords=preprint] %}

<h2 class="bibliography">Pedagogical Notes</h2>

{% bibliography --query @*[keywords=notes] %}

</div>