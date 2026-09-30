{%- assign site_modified = nil -%}
{%- assign site_modified_ts = 0 -%}

{%- for post in site.posts -%}
  {%- if post.date -%}
    {%- assign site_modified = post.date -%}
    {%- assign site_modified_ts = post.date | date: "%s" | plus: 0 -%}
    {%- break -%}
  {%- endif -%}
{%- endfor -%}

{%- for p in site.pages -%}
  {%- if p.date -%}
    {%- assign p_ts = p.date | date: "%s" | plus: 0 -%}
    {%- if p_ts > site_modified_ts -%}
      {%- assign site_modified = p.date -%}
      {%- assign site_modified_ts = p_ts -%}
    {%- endif -%}
  {%- endif -%}
{%- endfor -%}

{%- unless site_modified -%}
  {%- assign site_modified = site.time -%}
{%- endunless -%}
<script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "WebSite",
        {% if site.name %}"name": {{ site.name | jsonify }},{% endif %}
        {% if site.description %}"description": {{ site.description | jsonify }},{% endif %}
        {% if site.url %}"url": {{ site.url | append: site.baseurl | jsonify }},{% endif %}
        {% if site.author %}"author": 
            {
                "@type": "Person",
                "name": {{ site.author | jsonify }}
            },{% endif %}
        "dateCreated": {{ "2012.08.27 17:28:35" | date_to_xmlschema | jsonify }},
        "dateModified": {{ site_modified | date_to_xmlschema | jsonify }}
    }
</script>

