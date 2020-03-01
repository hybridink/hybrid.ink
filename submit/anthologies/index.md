---
layout: page
title: Anthologies
---

<style>
li.closed {
    display: none;
}
li.closed.show {
    display:block;
}
#toggle {
    font-size: 12pt;
}
</style>

<ul>
{% for entry in site.data.anthologies %}
{% assign anthology = entry[1] %}
    <li class="{% if anthology.open %}open{% else %}closed{% endif %}">
        <a href="{{anthology.slug}}"><em>{{anthology.title}}</em></a> &mdash;
        <strong class="{% if anthology.open %}open{% else %}closed{% endif %}"><em>{% if anthology.open %}Open{% else %}Closed{% endif %}</em></strong> &mdash;
        <em>Submissions open {{anthology.schedule.open}} and close {{anthology.schedule.close}}</em>
        {{anthology.short_description|markdownify}}
    </li>
{%endfor %}
</ul>
<script type="text/javascript">
window.showClosed = false;
window.toggleClosed = function() {
    window.showClosed = !window.showClosed;
    document.querySelector('#toggle').innerText = `${window.showClosed ? 'Hide' : 'Show'} closed anthologies`;
    document.querySelectorAll('li.closed').forEach((el) => {
        el.classList.toggle('show');
    });
}
</script>
<a id="toggle" href="javascript:window.toggleClosed()">Show closed anthologies</a>

-----

<iframe src="https://calendar.google.com/calendar/embed?src=hybrid.ink_85s829p5vf38rk6o5addi90sl0%40group.calendar.google.com&ctz=America%2FLos_Angeles" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
