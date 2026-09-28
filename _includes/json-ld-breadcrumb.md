{% if page.breadcrumbs %}
"breadcrumb": {
  "@type": "BreadcrumbList",
  "itemListElement": [
      {% for breadcrumb in page.breadcrumbs %}
      {
        "@type": "ListItem",
        "position": {{ forloop.index }},
        "item": {
          "@type": "{% if breadcrumb.type %}{{ breadcrumb.type }}{% else %}WebPage{% endif %}",
          "@id": "{{ site.url }}{{ site.baseurl }}{% if breadcrumb.url == 'page.url' %}{{ page.url }}{% else %}{{ breadcrumb.url }}{% endif %}",
          "name": "{% if breadcrumb.title == 'page.title' %}{{ page.title }}{% else %}{{ breadcrumb.title }}{% endif %}"
        }
      }{% unless forloop.last %},{% endunless %}
  {% endfor %}]
}
{% endif %}

