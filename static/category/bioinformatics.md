---
layout: category
title: Bioinformatics
permalink: /bioinformatics/
---

## Notes about Bioinformatics

{% for post in site.categories.bioinformatics %}
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}
