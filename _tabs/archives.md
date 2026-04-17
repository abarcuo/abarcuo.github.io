---
layout: page
title: Archivo
order: 3
subtitle: Todas las publicaciones ordenadas por fecha.
---

{%- assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" -%}

{%- for year in posts_by_year -%}
  <h2 class="archive-year">{{ year.name }}</h2>
  <ul class="archive-list">
    {%- for post in year.items -%}
      <li>
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d %b" }}</time>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </li>
    {%- endfor -%}
  </ul>
{%- endfor -%}

{%- if site.posts.size == 0 -%}
  <p class="empty-state">Todavía no hay publicaciones. Muy pronto habrá novedades.</p>
{%- endif -%}
