---
title: "Witziggy World"
layout: default
---
This is the homepage where people first land. They're greeted with a two sentence description of the project.

Then they're invited to subscribe. Below that are the new posts.

_Dividing line / different styling._

{% for post in site.posts limit:1 %}
<div class="newest-post">
    <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
    {{ post.excerpt }}
    <p class="postdate">{{ post.date | date_to_string }}</p>
</div>
{% endfor %}

<div class="post-index">
    {% for post in site.posts offset:1 %}
    <div class="">
        <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
        <p>{{ post.summary | markdownify }}</p>
        <p class="postdate">{{ post.date | date_to_string }}</p>
    </div>
    {% endfor %}
</div>