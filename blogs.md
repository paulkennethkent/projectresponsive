---
layout: page
title: Blog
permalink: /blog/
---
<h1 class="page-heading">Posts</h1>
  {% for post in site.posts%}
  <h2>
    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}" title="Permanent link to {{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
  </h2>
    <p>
      <time datetime="{{post.date}}"{{post.date | date: "%-d %b, %Y "}}></time>
      <span class="post-meta">{{ post.date | date: " %-d %b, %Y" }}</span>
      <p>{{post.excerpt}}</p>
      <a href="{{ post.url | prepend: site.baseurl }}">Read more</a>
      <hr>
    </p>


  {% endfor %}
</div>

<p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
