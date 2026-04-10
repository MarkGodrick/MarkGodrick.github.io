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
      <div class="cv-timeline-date">2026 – 2031 (expected)</div>
      <div class="cv-timeline-title">Ph.D. Student, Peking University</div>
      <div class="cv-timeline-subtitle">Wangxuan Institute of Computer Technology</div>
    </div>
    <div class="cv-timeline-item">
      <div class="cv-timeline-date">2022 – 2026 (expected)</div>
      <div class="cv-timeline-title">B.S. in Computer Science, Peking University</div>
      <div class="cv-timeline-subtitle">School of Electronics Engineering and Computer Science (EECS)</div>
    </div>
  </div>
</div>

<div class="cv-section">
  <h2><i class="fas fa-award cv-icon"></i> Honors &amp; Awards</h2>
  <div class="cv-timeline">
    <div class="cv-timeline-item">
      <div class="cv-timeline-date">October 2025</div>
      <div class="cv-timeline-title">Zhiban Scholarship (智班奖学金)</div>
      <div class="cv-timeline-subtitle">Peking University</div>
    </div>
    <div class="cv-timeline-item">
      <div class="cv-timeline-date">2023</div>
      <div class="cv-timeline-title">Academic Excellence Award &amp; Huawei Scholarship (学习优秀奖, 华为奖学金)</div>
      <div class="cv-timeline-subtitle">Peking University</div>
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
  <h2><i class="fas fa-briefcase cv-icon"></i> Experience</h2>
  <div class="cv-timeline">
    <div class="cv-timeline-item">
      <div class="cv-timeline-date">Spring 2026</div>
      <div class="cv-timeline-title">Teaching Assistant, Introduction to Artificial Intelligence</div>
      <div class="cv-timeline-subtitle">Peking University</div>
    </div>
    <div class="cv-timeline-item">
      <div class="cv-timeline-date">January 2026</div>
      <div class="cv-timeline-title">Reviewer, ACL Rolling Review (ARR)</div>
    </div>
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
