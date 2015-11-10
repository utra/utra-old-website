---
layout: page
title: Events
permalink: /events/
inMenu: true
---

We have events all the time blahblah hello the quick brown fox jumps over the lazy dog. We have events all the time blahblah lorem ipsum hello the quick brown fox jumps over the lazy dog. We have blahblah lorem ipsum hello the quick brown fox jumps over the lazy dog.

### Upcoming events
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
<ul class="post-list">
    {% for post in site.posts %}
        {% if post.category == events %}
          {% capture posttime %}{{post.date | date: '%s'}}{% endcapture %}
          {% if posttime > nowunix %}
          <li>
              <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

              <h2>
                  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
              </h2>
          </li>
          {% endif %}
        {% endif %}
    {% endfor %}
</ul>

### Past events
<ul class="post-list">
    {% for post in site.posts %}
        {% if post.category == events %}
          {% capture posttime %}{{post.date | date: '%s'}}{% endcapture %}
          {% if posttime <= nowunix %}
          <li>
              <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

              <h2>
                  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
              </h2>
          </li>
          {% endif %}
        {% endif %}
    {% endfor %}
</ul>
