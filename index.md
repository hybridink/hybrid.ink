---
layout: default
---

<div class="promo">
<p><strong>Holiday shipping:</strong> Looking to get some books for the holidays? Please make sure to order by December 15th for the best chance of getting your package on time!</p>
</div>

<div class="hero">
<h2>{{site.name}}</h2>

<p>{{site.brand}} is a small publisher focused on thoughtful fiction, exploratory poetry, and creative non-fiction.<br />
<a href="/about">Learn more...</a></p>
</div>

<div class="col-60"><p>The goal of {{site.brand}} is to provide well-versed and sophisticated works of fiction, poetry, and creative non-fiction. We want writing that gets us thinking about ourselves, stories that span genres, words that change the way we look at the world. {{site.brand}} is now open for anthology submissions, and will soon re-open for larger work queries.</p></div>

<div class="col-40"><h2 class="announcement"><a href="/submit">Submit to {{site.brand}}</a></h2></div>

-----

## Recent posts
{% for post in site.posts limit:5 %}
<div class="post-list">
    <p><a class="post-link" href="{{ post.url }}">{{ post.title }}</a></p>
    <p class="post-meta">{{ post.date | date: "%b %-d, %Y" }}{% if post.author %} &bullet; <a href="/editors#{{ post.author }}">{{ post.author }}</a>{% endif %}{% if post.meta %} &bullet; {{ post.meta }}{% endif %}</p>
    {{ post.excerpt }}
    <p><a href="{{ post.url }}">Read more...</a></p>
</div>
{% endfor %}
{% if site.posts.size > 5 %}
<a href="/updates">Older posts</a>
{% endif %}
