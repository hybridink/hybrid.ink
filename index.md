---
layout: default
---

<div class="hero">
<h2>The {{site.brand}} Award</h2>

<p>{{site.brand}} is an award recognizing excellence in furry nonfiction across all media. Fiction, visual art, and even movies play a large role within the furry fandom, but non-fiction as a genre, spread across several media, is growing in prevalence.</p>
</div>

<div class="col-60"><p>The goal of {{site.brand}} is to provide a well-versed and sophisticated look at works of non-fiction within the furry community, as seen through the eyes of those most deeply involved. As a juried award, nominees will be chosen from eligible productions within a set of categories, and winners chosen for each category by a jury of peers.</p></div>
<div class="col-40"><h2 class="announcement"><a href="/award">Learn More</a></h2></div>

-----

## Recent posts
{% for post in site.posts limit:5 %}
<div class="post-list">
    <p><a class="post-link" href="{{ post.url }}">{{ post.title }}</a></p>
    <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} &bullet; <a href="/admins#{{ post.author }}">{{ post.author }}</a>{% endif %}{% if post.meta %} &bullet; {{ post.meta }}{% endif %}</p>
    <p>{{ post.excerpt | remove: '<p>' | remove: '</p>' }}</p>
</div>
{% endfor %}
{% if site.posts.size > 5 %}
<a href="/updates">Older posts</a>
{% endif %}
