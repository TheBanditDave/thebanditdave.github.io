---
layout: blog
title: Blog
permalink: /blog/
---

<div class="blog">

<div class="row column text-center">
<br>
<h1>TheBanditDave's Blog</h1>
<hr>

</div>

  {% for post in site.posts %}  
    <div class="row">
      <div class="small-7 large-centered columns text-center">
        <h2> {{ post.title }} <small> &#x25cf; {{ post.date | date: "%b %-d, %Y" }}</small></h2>
        {% if post.image %}
          <img class="thumbnail" src="{{site.url}}/img/{{ post.image }}">
        {% endif %}
        <p> By: {{ post.author }} </p>
        <p>{{ post.excerpt }}</p>
        <a class="button" href="{{ post.url | prepend: site.baseurl }}">Read more</a>
        <hr>
      </div>
    </div>
  {% endfor %}  

</div>