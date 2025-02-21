---
layout: page
permalink: /publications/
title: publications
description: publications in reversed chronological order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

<h3 style="border-top: 1px solid var(--global-divider-color);"><br>publications empowered by dtool<br></h3>

{% bibliography --file empowered %}

<h3 style="border-top: 1px solid var(--global-divider-color);"><br>dtool core publications<br></h3>

{% bibliography %}



</div>
