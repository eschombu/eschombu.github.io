---
layout: default
title: Erik Schomburg
nav_order: 1
nav_title: About
---

<div class="intro">
  <img class="headshot" src="{{ '/assets/img/erik-schomburg.jpg' | relative_url }}"
       alt="Erik Schomburg" width="256" height="256" loading="eager" decoding="async">
  <div class="intro-text">
    <h1>Erik Schomburg</h1>
    <p class="lead">Data scientist and software engineer in New York.</p>
  </div>
</div>

I build machine learning systems — training and inference pipelines, model
services, and the analysis tooling that surrounds them. My background is in
physics and neuroscience, and most of my work sits where careful analysis of
messy, high-dimensional data meets the engineering required to run it in
production.

I'm currently a Research Scientist and Software Engineer on the Connectomics
project at the [Flatiron Institute Center for Computational Neuroscience](https://www.simonsfoundation.org/flatiron/center-for-computational-neuroscience/),
where we reconstruct the wiring of a brain from electron microscope imagery.
Before that I spent several years building machine learning systems in industry,
on problems spanning personalization, sensor and signal interpretation, and
location inference.

I did my Ph.D. in physics at Caltech, studying the biophysical origins of
electrical signals recorded in the brain, and continued that work as a
postdoctoral researcher before moving into industry.

Outside of work, I'm involved with [New York Kayak Polo](https://nykayakpolo.org/),
where I served as President for several years and am currently Vice President.

<h2>Elsewhere</h2>

<ul class="profile-links" style="font-size: 1rem;">
  <li><a href="https://github.com/{{ site.profiles.github }}" rel="me">GitHub</a></li>
  {%- if site.profiles.linkedin %}
  <li><a href="https://www.linkedin.com/in/{{ site.profiles.linkedin }}" rel="me">LinkedIn</a></li>
  {%- endif %}
  {%- if site.profiles.scholar %}
  <li><a href="https://scholar.google.com/citations?user={{ site.profiles.scholar }}" rel="me">Google Scholar</a></li>
  {%- endif %}
  {%- if site.email_user and site.email_domain %}
  <li>{% include email.html %}</li>
  {%- endif %}
</ul>
