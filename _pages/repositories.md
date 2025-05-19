---
layout: page
title: "Repositories"
permalink: /repositories/
nav: true
nav_order: 2
description: "A curated look at the code I craft, the ideas I prototype, and the coursework that keeps my skills sharp."
---

> *“Code is how I think out loud.”*  
> Below is a hand‑picked collection of projects I’m most proud of, followed by the full list of everything I tinker with on GitHub.

---

## ✨ Featured Projects

{% comment %}
List the 3 repos you want to spotlight **first** in `_data/repositories.yml`.
`github_repos` order = priority order.
{% endcomment %}

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {%- assign featured = site.data.repositories.github_repos | slice: 0, 4 -%}
  {%- for repo in featured -%}
    {% include repository/repo.liquid repository=repo %}
  {%- endfor -%}
</div>
{% endif %}

---

## 🏆 GitHub Trophy Wall

{% if site.repo_trophies.enabled and site.data.repositories.github_users %}
{%- for user in site.data.repositories.github_users -%}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center mb-4">
  {% include repository/repo_trophies.liquid username=user %}
</div>
{%- endfor -%}
{% endif %}

---

## 👥 GitHub Profiles

{% if site.data.repositories.github_users %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>
{% endif %}

---

*Want to see something in more detail or collaborate?* Feel free to [open an issue](https://github.com/{{ site.data.repositories.github_users[0] }}) or [drop me a message](mailto:sakshipandey@cse.iitb.ac.in).
