---
layout: page
title: Team
permalink: /team/
---

Find our awesome team here!

---

## Faculty Adviser

<div class="faculty-advisers">
{% for adviser in site.data.club_members.faculty_advisers %}
  <div class="member-card">
    <img src="{{ adviser.image | relative_url }}" alt="{{ adviser.name }}" class="member-photo">
    <h3>
      {% if adviser.website %}
        <a href="{{ adviser.website }}" target="_blank" rel="noopener noreferrer">{{ adviser.name }}</a>
      {% else %}
        {{ adviser.name }}
      {% endif %}
    </h3>
    <p><strong>Email:</strong> <a href="mailto:{{ adviser.email }}">{{ adviser.email }}</a></p>
  </div>
{% endfor %}
</div>

---

## Core Members

<div class="core-members">
{% for core in site.data.club_members.core_members %}
  <div class="member-card">
    <img src="{{ core.image | default: '/assets/images/placeholder.webp' | relative_url }}" alt="{{ core.name }}" class="member-photo">
    <h3>
      {% if adviser.website %}
        <a href="{{ core.website }}" target="_blank" rel="noopener noreferrer">{{ core.name }}</a>
      {% else %}
        {{ core.name }}
      {% endif %}
    </h3>
    <p><strong>Email:</strong> <a href="mailto:{{ core.email }}">{{ core.email }}</a></p>
  </div>
{% endfor %}
</div>

---
