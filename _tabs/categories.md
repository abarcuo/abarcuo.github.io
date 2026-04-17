---
layout: page
title: Categorías
order: 1
subtitle: Explora los artículos por tema.
---

{%- assign categories = site.categories | sort -%}

{%- if categories.size > 0 -%}
<div class="taxonomy-list">
  {%- for cat in categories -%}
    <a href="{{ '/categories/' | append: cat[0] | slugify | relative_url }}/">
      {{ cat[0] }}
      <span class="count">{{ cat[1].size }}</span>
    </a>
  {%- endfor -%}
</div>
{%- else -%}
  <p class="empty-state">Todavía no hay categorías.</p>
{%- endif -%}
