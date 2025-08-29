---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

You can find all of my articles on <a href="https://scholar.google.com/citations?user=hZPIICQAAAAJ&hl" target="_blank">my Google Scholar profile</a>.

(* = equal contribution)

{% include base_path %}

---

## 🔍 Fairness

{% assign publicationsByYear = site.publications | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in publicationsByYear reversed %}
<!--   <h1 style="margin: 1.5em 0px -0.5em; padding: 0px; color: brown;">{{ year.name }}</h1> -->
  {% assign publicationsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
  {% for month in publicationsByMonth reversed %}
    {% for post in month.items reversed %}
      {% if post.selected == "true" %}
        {% if post.topic == "fairness" %}
          {% include archive-single.html %}
        {% endif %}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% endfor %}

## 🔍 Safety and Privacy

{% assign publicationsByYear = site.publications | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in publicationsByYear reversed %}
<!--   <h1 style="margin: 1.5em 0px -0.5em; padding: 0px; color: brown;">{{ year.name }}</h1> -->
  {% assign publicationsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
  {% for month in publicationsByMonth reversed %}
    {% for post in month.items reversed %}
      {% if post.selected == "true" %}
        {% if post.topic == "safety" %}
          {% include archive-single.html %}
        {% endif %}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% endfor %}

## 🔍 Factuality and Faithfulness

{% assign publicationsByYear = site.publications | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in publicationsByYear reversed %}
<!--   <h1 style="margin: 1.5em 0px -0.5em; padding: 0px; color: brown;">{{ year.name }}</h1> -->
  {% assign publicationsByMonth = year.items | group_by_exp:"post", "post.date | date: '%B'" %}
  {% for month in publicationsByMonth reversed %}
    {% for post in month.items reversed %}
      {% if post.selected == "true" %}
        {% if post.topic == "fact_faith" %}
          {% include archive-single.html %}
        {% endif %}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% endfor %}
