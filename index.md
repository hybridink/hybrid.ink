---
layout: default
---

<div class="promo">
<h2>John Minichillo's <em>The Last Workshop</em> and mx jen durbent's <em>canon</em> now available!</h2>

<div class="col-40"><img src="/images/news/canon-tlw.jpg" alt="Two stacks of books" /></div>
<div class="col-60"><p>{{site.brand}} is happy to announce that both Minichillo's <em><a href="/the-last-workshop">The Last Workshop</a></em> and durbent's poetry collection <em><a href="/canon">canon</a></em> are available and ready to be shipped! While they may not make it in time for the holidays, you should have some good reading to bring you into the new year!</p></div>
</div>

<div class="hero">
<h2>{{site.name}}</h2>

<p>{{site.brand}} is a small publisher focused on thoughtful fiction, exploratory poetry, and creative non-fiction.</p>
</div>

<div class="col-60"><p>The goal of {{site.brand}} is to provide well-versed and sophisticated works of fiction, poetry, and creative non-fiction. We want writing that gets us thinking about ourselves, stories that span genres, words that change the way we look at the world. {{site.brand}} is now open for novel and non-fiction book queries, and will be open soon for shorter works to be included in anthologies.</p></div>
<div class="col-40"><h2 class="announcement"><a href="/submit">Learn More</a></h2></div>

-----

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
