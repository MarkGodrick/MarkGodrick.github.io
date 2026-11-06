---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% include base_path %}
{% assign boundary_paper = site.publications | where: "permalink", "/publications/2026-05-01-dynamic-boundary-evaluation/" | first %}
{% assign spti_paper = site.publications | where: "permalink", "/publications/2025-09-20-spti/" | first %}

Hi! I am **Haoxiang Wang** (王浩翔), a Ph.D. student at the [Wangxuan Institute of Computer Technology](https://www.icst.pku.edu.cn/), Peking University. I received my B.S. in Computer Science from the School of EECS, Peking University in 2026.

Recently, my research has focused on evaluating the dynamic capability boundaries of large language models, especially how to move beyond fixed benchmarks and static worst-case attacks toward skill-guided search and calibrated difficulty estimation.

<div class="cv-section">
  <h2><i class="fas fa-flask cv-icon"></i> Research Interests</h2>
  <div class="cv-badges">
    <span class="cv-badge">Large Language Models (LLM)</span>
    <span class="cv-badge">LLM Evaluation</span>
    <span class="cv-badge">AI Safety</span>
    <span class="cv-badge">Reinforcement Learning (RL)</span>
    <span class="cv-badge">Multi-modal Learning</span>
  </div>
</div>

<div class="cv-section">
  <h2><i class="fas fa-bullhorn cv-icon"></i> News</h2>
  <div class="home-news">
    <ul>
      <li>
        <span class="news-date">Nov 2026</span>
        <span class="news-content">Our work <a href="{{ base_path }}{{ boundary_paper.url }}"><em>{{ boundary_paper.title }}</em></a> has been accepted to <strong>NeurIPS 2026 (Poster)</strong>!</span>
      </li>
      <li>
        <span class="news-date">May 2026</span>
        <span class="news-content">My undergraduate thesis on dynamic boundary evaluation for language models, titled <em>大语言模型动态能力边界评测：技能引导搜索与难度校准</em>, was selected as an <strong>Outstanding Undergraduate Thesis</strong>.</span>
      </li>
      <li>
        <span class="news-date">Jan 2026</span>
        <span class="news-content">Serving as a reviewer for <strong>ACL Rolling Review (ARR)</strong>.</span>
      </li>
      <li>
        <span class="news-date">Oct 2025</span>
        <span class="news-content">Awarded the <strong>Zhiban Scholarship</strong> (智班奖学金), Peking University.</span>
      </li>
      <li>
        <span class="news-date">Sep 2025</span>
        <span class="news-content">Our paper <a href="{{ base_path }}{{ spti_paper.url }}"><em>SPTI</em></a> has been accepted to <strong>NeurIPS 2025 (Poster)</strong>!</span>
      </li>
    </ul>
  </div>
</div>

<div class="cv-section">
  <h2><i class="fas fa-file-alt cv-icon"></i> Selected Works</h2>
  <div class="home-pub">
    {% for post in site.publications reversed %}
    <div class="pub-card">
      <div class="pub-title"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></div>
      <div class="pub-authors">{% for author in post.authors %}{% if author == site.author.name %}<strong>{{ author }}</strong>{% else %}{{ author }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}</div>
      <div class="pub-venue">{{ post.venue }}</div>
      <div class="pub-links">
        <a href="{{ base_path }}{{ post.url }}"><i class="fas fa-file-alt"></i>Details</a>
        {% if post.paperurl %}<a href="{{ post.paperurl }}"><i class="fas fa-file-pdf"></i>Paper</a>{% endif %}
        {% if post.codeurl %}<a href="{{ post.codeurl }}"><i class="fab fa-github"></i>Code</a>{% endif %}
      </div>
    </div>
    {% endfor %}
  </div>
</div>
