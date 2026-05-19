---
layout: single
title: "Resume"
permalink: /resume/
author_profile: true
classes: wide
---

<section class="resume-section">
  <h2>Summary</h2>
  <p class="career-summary">
   Senior Technical Writer with nearly a decade of experience architecting end-user education systems for SaaS platforms in cybersecurity, event management, and elections technology. Specializes in API documentation, information architecture, and in-app content strategy, with a proven track record of building documentation programs from the ground up for early-stage startups. Currently leading documentation migration and rebranding efforts at Arctic Wolf following the acquisition of Sevco Security, expanding scope to enterprise-scale documentation infrastructure and DITA-based topic authoring. Industry speaker and advocate for documentation as a core product function.
  </p>
</section>

<section class="resume-section">
  <h2>Skills</h2>
  {% for group in site.data.resume.skills %}
    <div class="skill-group">
      <h4>{{ group.category }}</h4>
      <div class="skill-tags">
        {% for item in group.items %}
          <span class="skill-tag">{{ item }}</span>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</section>

<section class="resume-section">
  <h2>Experience</h2>
  {% for job in site.data.resume.experience %}
    <div class="resume-entry">
      <div class="resume-entry__header">
        <h3>{{ job.title }}</h3>
        <span class="resume-entry__dates">{{ job.dates }}</span>
      </div>
      <p class="resume-entry__meta">{{ job.company }} · {{ job.location }}</p>
      <ul>
        {% for item in job.highlights %}
          <li>{{ item }}</li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</section>

<section class="resume-section">
  <h2>Education</h2>
  {% for school in site.data.resume.education %}
    <div class="resume-entry">
      <div class="resume-entry__header">
        <h3>{{ school.degree }}</h3>
        <span class="resume-entry__dates">{{ school.dates }}</span>
      </div>
      <p class="resume-entry__meta">{{ school.school }} · {{ school.location }}</p>
      {% if school.minor %}
        <p class="resume-entry__minor">Minor: {{ school.minor }}</p>
      {% endif %}
    </div>
  {% endfor %}
</section>