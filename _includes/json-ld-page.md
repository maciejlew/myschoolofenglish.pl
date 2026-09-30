<script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": {% if page.type %}{{ page.type }}{% elsif page.is_post %}BlogPosting{% else %}WebPage{% endif %},
        {% if page.title %}"name": {{ page.title | jsonify}},{% endif %}
        {% if page.description %}"description": {{ page.description | jsonify }},{% endif %}
        {% if page.author or site.author %}"author": 
            {
                "@type": "Person",
                "name": {% if page.author %}{{ page.author | jsonify }}{% else %}{{ site.author | jsonify }}{% endif %}
            },{% endif %}
        {% if page.date %}"dateCreated": {{ page.date }},{% endif %}

        "url": {{ site.url }}{{ site.baseurl }}{{ page.url }}

        {% if page.breadcrumbs %},{% endif %}
        {%- include json-ld-breadcrumb.md -%}

    }
</script>

