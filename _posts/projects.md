---
Title: "Projects"
permalink: /posts/
author_profile: true
header:
  image: "/images/EF4_Tornado_12_26_2015_3.jpg"
---
{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
© 2020 GitHub, Inc.
