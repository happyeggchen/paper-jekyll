---
layout: default
permalink: /pages/tags
title: Tags
row: true
list: main
---
{% for tag in site.tags %}
  <div class="container s12 m12 l12">
    <div class="black-text">
      <h3>{{ tag[0] }}</h3>
    </div>
          {% for post in tag[1] %}
            {% if post.hidden != true %}
              <a href="{{ post.url }}" class="waves-effect waves-grey btn {{ site.css }} z-depth-1">{{ post.title }}</a>
            {% endif %}
          {% endfor %}
      <br>
  </div>
{% endfor %}
