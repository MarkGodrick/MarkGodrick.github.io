---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<div class="cv-section">
  <h2><i class="fas fa-graduation-cap cv-icon"></i> Education</h2>
  <div class="cv-timeline">
    <div class="cv-timeline-item">
      <div class="cv-timeline-date">2022 – 2026 (expected)</div>
      <div class="cv-timeline-title">B.S. in Computer Science, Peking University</div>
      <div class="cv-timeline-subtitle">School of Electronics Engineering and Computer Science (EECS)</div>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2><i class="fas fa-flask cv-icon"></i> Research Interests</h2>
  <div class="cv-badges">
    <span class="cv-badge">Large Language Models (LLM)</span>
    <span class="cv-badge">AI Safety</span>
    <span class="cv-badge">Reinforcement Learning (RL)</span>
    <span class="cv-badge">Multi-modal Learning</span>
  </div>
</div>

<div class="cv-section">
  <h2><i class="fas fa-file-alt cv-icon"></i> Publications</h2>
  <div class="cv-list">
    <ul>{% for post in site.publications reversed %}
      {% include archive-single-cv.html %}
    {% endfor %}</ul>
  </div>
</div>

<div class="cv-section">
  <h2><i class="fas fa-chalkboard-teacher cv-icon"></i> Teaching</h2>
  <div class="cv-list">
    <ul>{% for post in site.teaching reversed %}
      {% include archive-single-cv.html %}
    {% endfor %}</ul>
  </div>
</div>

<!-- Work experience
======
* Spring 2024: Academic Pages Collaborator
  * Github University
  * Duties includes: Updates and improvements to template
  * Supervisor: The Users

* Fall 2015: Research Assistant
  * Github University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub

* Summer 2015: Research Assistant
  * Github University
  * Duties included: Tagging issues
  * Supervisor: Professor Git -->

<!-- Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul> -->

<!-- Service and leadership
======
* Currently signed in to 43 different slack teams -->
