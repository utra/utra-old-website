---
layout: page
title: Past events
permalink: /events/all-events/
---

{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
<ul class="post-list events-list">
  {{ site.posts.length}}
    {% for post in site.categories.events %}
      {% capture posttime %}{{post.date | date: '%s'}}{% endcapture %}
      {% if posttime <= nowunix %}
      <li>
          <h3>
              <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h3>
          <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}
          from {{ post.date | date: "%H:%M%p"}}
          to {{ post.endtime | date: "%H:%M%p"}}</span>
      </li>
      {% endif %}
    {% endfor %}
</ul>
