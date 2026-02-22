---
layout: default
title: SOC Level 1 Path
---

# SOC Level 1 Path – Progress

This page documents my progress through the **SOC Level 1 (Security Analyst Level 1)** path on TryHackMe.  
Each section represents a module in the path, and the status button indicates my progress.

## Sections

<div class="section-list">
{% for section in site.data.soc_rooms %}
  <div class="section-item">
    <h3>{{ section.title }}</h3>
    <p>{{ section.description }}</p>
    <span class="status status-{{ section.status }}">
      {{ section.status | capitalize }}
    </span>
    {% if section.rooms.size > 0 %}
      <ul class="room-list">
        {% for room in section.rooms %}
          <li>
            <a href="{{ room.url }}">{{ room.title }}</a>
            <span class="room-status status-{{ room.status }}">
              {{ room.status | capitalize }}
            </span>
          </li>
        {% endfor %}
      </ul>
    {% endif %}
  </div>
{% endfor %}
</div>