---
layout: default
title: Blog Workshop
---

## Blogs Written by Participants in the Blogging Workshop

[For regular notanother.pizza updates click here](/index)

<div class="posts">
  {% for post in site.categories.workshop %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {% assign first_image = post.content | split: '<img ' | last %}
        {% if first_image and first_image != post.content %}
          {% assign src = first_image | split: 'src="' | last | split: '"' | first %}
          <img src="{{ src }}" alt="{{ post.title }}" style="max-width:100%; height:auto;" />
        {% else %}
          {{ post.excerpt }}
        {% endif %}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="button button-primary">Read More</a>
    </article>
  {% endfor %}
</div>