<script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "{% if page.type %}{{ page.type }}{% elsif page.is_post %}BlogPosting{% else %}WebPage{% endif %}",
        {% if page.title %}"name": "{{ page.title }}",{% endif %}
        {% if page.description %}"description": "{{ page.description }}",{% endif %}
        {% if page.author or site.author %}"author": 
            {
                "@type": "Person",
                "name": "{% if page.author %}{{ page.author }}{% else %}{{ site.author }}{% endif %}"
            },{% endif %}
        {% if page.date %}"dateCreated": "{{ page.date }}",{% endif %}

        {%- include json-ld-breadcrumb.md -%}

        "url": "{{ site.url }}{{ site.baseurl }}{{ page.url }}"
    }
</script>

