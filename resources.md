---
layout: page
title: Resources
permalink: /resources/
---

# Heartfulness Master Classes

<div class="video-container">
  <!-- Day 1 -->
  <div class="video-card">
    <h3 class="video-title">Day 1</h3>
    <div class="video-embed">
      <iframe 
        src="https://www.youtube.com/embed/0TYhuDb7WNQ?si=8nmuWGIrWIpqQ9Ux" 
        frameborder="0" 
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <!-- Day 2 -->
  <div class="video-card">
    <h3 class="video-title">Day 2</h3>
    <div class="video-embed">
      <iframe 
        src="https://www.youtube.com/embed/ePiMdh5X_r0?si=C6z74QHEK6D3aO1L" 
        frameborder="0" 
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>

  <!-- Day 3 -->
  <div class="video-card">
    <h3 class="video-title">Day 3</h3>
    <div class="video-embed">
      <iframe 
        src="https://www.youtube.com/embed/WuKgVWXpcD0?si=lerFj3LTU0izZFpq" 
        frameborder="0" 
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>
  </div>
</div>

# Featured Posts

<div class="featured-posts">
{% if site.paginate %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts | where: "tags", "featured" %}
{% endif %}

{%- if posts.size > 0 -%}
  {%- if page.list_title -%}
    <h2 class="post-list-heading">{{ page.list_title }}</h2>
  {%- endif -%}
  <ul class="post-list">
    {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
    {%- for post in posts -%}
    <li>
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>

  {% if site.paginate %}
    <div class="pager">
      <ul class="pagination">
        {%- if paginator.previous_page %}
          <li><a href="{{ paginator.previous_page_path | relative_url }}" class="previous-page">{{ paginator.previous_page }}</a></li>
        {%- else %}
          <li><div class="pager-edge">•</div></li>
        {%- endif %}
        <li><div class="current-page">{{ paginator.page }}</div></li>
        {%- if paginator.next_page %}
          <li><a href="{{ paginator.next_page_path | relative_url }}" class="next-page">{{ paginator.next_page }}</a></li>
        {%- else %}
          <li><div class="pager-edge">•</div></li>
        {%- endif %}
      </ul>
    </div>
  {%- endif %}

{%- endif -%}

</div>


