---
layout: category
title: Bikes
permalink: /bikes/
---

## Planning Of Bike Rides

{% for post in site.categories.biking %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
