---
layout: default
title: ainorenvall.fi - kotisivu
---

<div id="posts">

<p>Blog RSS here: <a title="blog RSS" href="http://ainorenvall.fi/feed.xml">
                    <i class="fa fa-rss"></i></a></p>


    {% for post in site.posts offset: 0 limit: 10 %}
        <div style="border-bottom: 1px solid gray; padding: 5px 0;">
        <small style="color: #999;">{{ post.date | date: "%b %d, %Y" }}</small> 
        <a href="{{ post.url }}">{{ post.title }}</a>
        <br />
        {% if post.summary %}
            <small>{{ post.summary }}</small>
        {% endif %}
        </div>
    {% endfor %}

<div style="margin: 15px 0; padding-top: 5px;">
<small>
    <a href="/archive.html" title="an archive of all posts">&larr; More posts</a>
</small>
</div>

</div>
