<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",

  {% if page.title %}
  "headline": {{ page.title | jsonify }},
  {% endif %}

  {% if page.description %}
  "description": {{ page.description | jsonify }},
  {% endif %}

  "url": {{ site.url | append: site.baseurl | append: page.url | jsonify }},

  {% if page.date %}
  "datePublished": "{{ page.date | date_to_xmlschema }}",
  {% endif %}

  {% if page.last_modified_at %}
  "dateModified": "{{ page.last_modified_at | date_to_xmlschema }}",
  {% elsif page.date %}
  "dateModified": "{{ page.date | date_to_xmlschema }}",
  {% endif %}

  {% if page.author or site.author %}
  "author": {
    "@type": "Person",
    "name": {{ page.author | default: site.author | jsonify }}
  },
  {% endif %}

  {% if site.name %}
  "publisher": {
    "@type": "Organization",
    "name": {{ site.name | jsonify }}
  }
  {% endif %}
}
</script>

