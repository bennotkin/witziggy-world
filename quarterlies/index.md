---
title: Quarterlies
layout: page
---
Roughly four times a year I send out a newsletter on a theme.

<div class="quarterly-index">
    {% for post in site.quarterlies %}
    <div class="">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <p>{{ post.summary | markdownify }}</p>
        <p class="postdate">{{ post.date | date_to_string }}</p>
    </div>
    {% endfor %}
</div>