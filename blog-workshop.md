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
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="button button-primary">Read More</a>
    </article>
  {% endfor %}
</div>