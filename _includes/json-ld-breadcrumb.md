{% if page.breadcrumbs %}
"breadcrumb": {
  "@type": "BreadcrumbList",
  "itemListElement": [
      {% for breadcrumb in page.breadcrumbs %}
      {
        "@type": "ListItem",
        "position": {{ forloop.index }},
        "item": {
          "@type": {% if breadcrumb.type %}{{ breadcrumb.type | jsonify }}{% else %}"WebPage"{% endif %},
          "@id": {% if breadcrumb.url == 'page.url' %}{{ site.url | append: site.baseurl | append: page.url | jsonify }}{% else %}{{ site.url | append: site.baseurl | append: breadcrumb.url | jsonify }}{% endif %},
          "name": {% if breadcrumb.title == 'page.title' %}{{ page.title | jsonify }}{% else %}{{ breadcrumb.title | jsonify }}{% endif %}
        }
      }{% unless forloop.last %},{% endunless %}
  {% endfor %}]
}
{% endif %}

