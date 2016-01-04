---
layout: page
title: Events
permalink: /events/
inMenu: true
---

In addition to the work that our subteams do, we also host talks, workshops, and more throughout the year.
These can be a great way to dip your toes into UTRA if you aren't sure whether or not to commit to joining a team.

## upcoming events
{% capture nowunix %}{{'now' | date: '%s'}}{% endcapture %}
<ul class="post-list events-list">
    {% assign event_count = 0 %}
    {% for post in site.categories.events %}
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
    {% endfor %}
    {% if event_count == 0 %}
    <p>No upcoming events.</p>
    {% endif %}
</ul>

## past events
<ul class="post-list events-list">
    {% assign past_event_count = 0 %}
    {% for post in site.categories.events %}
      {% capture posttime %}{{post.date | date: '%s'}}{% endcapture %}
      {% if posttime <= nowunix and past_event_count < 3 %}
      {% assign past_event_count = past_event_count | plus:1 %}
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

[See all past events](/events/all-events)
