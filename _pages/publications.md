---
layout: page
permalink: /publications/
title: publications
description:
nav: true
nav_order: 2
_styles: |
  .post > .post-header {
    display: none;
  }
---

<!-- _pages/publications.md -->

<div class="publications-heading">
  <h1><i class="ti ti-file-pencil" aria-hidden="true"></i> Recent Publications</h1>
  <p class="publication-note">* indicates the corresponding author. <sup>1</sup> indicates co-first authorship.</p>
</div>

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
