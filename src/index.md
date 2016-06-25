---
layout: page
title: Articles
---
<div class="three rightedge">
  <div id="pagination_block">
    {% for post in site.posts %}
    <div class="post listing">
      <h3>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </h3>
      <div class="single leftedge left">
        <a href="{{ post.url | prepend: site.baseurl }}">
          {% if post.image %}
          <img class="avatar" src="/file/post{{ post.url }}{{ post.image }}" alt="{{ post.title }}">
          {% else %}
          <img class="avatar" src="/file/site/calgary-under-construction.140.100.jpg" alt="{{ post.title }}">
          {% endif %}
        </a>
      </div>
      <p class="triple rightedge left">
        {{ post.date | date: "%b %-d, %Y" }}<br/>
        {% if post.excerpt %}{{ post.excerpt | strip_html | strip_newlines | truncate: 160 }}{% endif %}
      </p>
    </div>
    <div class="spacer">&nbsp;</div>
    {% endfor %}
  </div>
</div>
