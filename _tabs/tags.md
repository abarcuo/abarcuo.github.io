---
layout: page
title: Etiquetas
order: 2
subtitle: Todas las etiquetas del blog.
---

{%- assign tags = site.tags | sort -%}

{%- if tags.size > 0 -%}
<div class="taxonomy-list">
  {%- for tag in tags -%}
    <a href="{{ '/tags/' | append: tag[0] | slugify | relative_url }}/">
      #{{ tag[0] }}
      <span class="count">{{ tag[1].size }}</span>
    </a>
  {%- endfor -%}
</div>
{%- else -%}
  <p class="empty-state">Todavía no hay etiquetas.</p>
{%- endif -%}
