---
layout: page
title: Events
permalink: /events/
inMenu: true
---

In addition to the work that our subteams do, we also host talks, workshops, and more throughout the year.
These can be a great way to dip your toes into UTRA if you aren't sure whether or not to commit to joining a team.

## Upcoming events
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
<ul class="post-list events-list">
    {% assign event_count = 0 %}
    {% for post in site.posts %}
        {% if post.category == events %}
          {% capture posttime %}{{post.date | date: '%s'}}{% endcapture %}
          {% if posttime > nowunix %}
          {% increment event_count %}
          <li>
              <h3>
                  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
              </h3>
              <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}
              from {{ post.date | date: "%H:%M%p"}}
              to {{ post.endtime | date: "%H:%M%p"}}</span>
          </li>
          {% endif %}
        {% endif %}
    {% endfor %}
    {% if event_count == 0 %}
    <p>No upcoming events.</p>
    {% endif %}
</ul>

## Past events
<ul class="post-list events-list">
    {% for post in site.posts %}
        {% if post.category == events %}
          {% capture posttime %}{{post.date | date: '%s'}}{% endcapture %}
          {% if posttime <= nowunix %}
              <h3>
                  <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
              </h3>
          <li>
              <span class="post-meta">{{ post.date | date: "%B %-d, %Y" }}
              from {{ post.date | date: "%H:%M%p"}}
              to {{ post.endtime | date: "%H:%M%p"}}</span>
          </li>
          {% endif %}
        {% endif %}
    {% endfor %}
</ul>
