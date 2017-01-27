---
layout: default
---

<span class="brand">Hybrid</span> is a themed, semiannual non-fiction publication focusing on exploring the furry subculture through a diverse range of articles, opinions, and personal stories, lightened with a dash of poetry. <span class="brand">Hybrid</span> is the literary journal to [\[adjective\]\[species\]](http://adjectivespecies.com)'s blog.

The goal of <span class="brand">Hybrid</span> is to provide a well-versed and sophisticated look at the furry community through the eyes of those most deeply involved. Articles should be well researched and opinion pieces should be backed up by fact to provide an intelligent discourse on what it means to be a furry. As with the experiences of those writing them, the articles and opinions will be diverse, giving many different points of view on the theme behind each issue. If you have something excellent to say, feel free to send it our way.

<h2 class="announcement"><a href="/write">Submit</a></h2>

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
