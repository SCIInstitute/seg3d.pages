{% if page.function.subchapter == null %}
[Back]({{ site.github.url }}/functionality.html)
{% else %}
{% assign cat = page.function.subchapter %}
  {% for pages in site.pages %}
    {% if pages.title == cat %}
[Back]({{ pages.url | prepend: site.github.url }})
    {% endif %}
  {% endfor %}
{% endif %}

