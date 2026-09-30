<script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": {% if page.type %}{{ page.type | jsonify }}{% elsif page.is_post %}"BlogPosting"{% else %}"WebPage"{% endif %},
        "url": {{ site.url | append: site.baseurl | append: page.url | jsonify }}

        {% if page.title %},
        "name": {{ page.title | jsonify}}
        {% endif %}

        {% if page.description %},
        "description": {{ page.description | jsonify }}
        {% endif %}

        {% if page.author or site.author %},
        "author": 
            {
                "@type": "Person",
                "name": {% if page.author %}{{ page.author | jsonify }}{% else %}{{ site.author | jsonify }}{% endif %}
            }
        {% endif %}

        {% if page.date %},
        "dateCreated": {{ page.date| date_to_xmlschema | jsonify }}
        {% endif %}

        {% if page.breadcrumbs %},
        {%- include json-ld-breadcrumb.md -%}
        {% endif %}

    }
</script>

