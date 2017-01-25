---
layout: default
---

**Hybrid**{: class="brand" } is a themed, semiannual non-fiction publication focusing on exploring the furry subculture through a diverse range of articles, opinions, and personal stories, lightened with a dash of poetry. <span class="brand">Hybrid</span> is the journal to [\[adjective\]\[species\]](http://adjectivespecies.com) blog.

The goal of the review is to provide a sophisticated, intellectual look at the furry subculture through the eyes of those most deeply involved. Articles should be well researched and opinions should be backed up by fact to provide an intelligent discourse on what it means to be a furry. The articles, opinions, and experiences will be diverse, and will give many different points of view on various topics. If you have something excellent to say, feel free to send it our way.

## Recent posts
{% for post in site.posts limit:5 %}
<div class="post-list">
    <p><a class="post-link" href="{{ post.url }}">{{ post.title }}</a></p>
    <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} &bullet; <a href="/editors#{{ post.author }}">{{ post.author }}</a>{% endif %}{% if post.meta %} &bullet; {{ post.meta }}{% endif %}</p>
    <p>{{ post.excerpt | remove: '<p>' | remove: '</p>' }}</p>
</div>
{% endfor %}
{% if site.posts.size > 5 %}
<a href="/updates">Older posts</a>
{% endif %}
