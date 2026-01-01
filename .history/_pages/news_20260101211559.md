---
layout: archive
title: "News"
permalink: /news/
author_profile: true
published: false
---

<section class="archive-list archive-list--news">
  <ul class="news-list">
    {% assign items = site.news | sort: 'date' | reverse %}
    {% for item in items %}
      <li class="news-item">
        <time datetime="{{ item.date | date_to_xmlschema }}">{{ item.date | date: "%B %Y" }}</time>
        <span class="news-title">{{ item.title }}</span>
        {% if item.excerpt %}
          <p class="news-excerpt">{{ item.excerpt | strip_html | truncate: 160 }}</p>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
