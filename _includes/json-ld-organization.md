{%- assign org = site.organization -%}
{%- if org -%}
{%- assign site_root = site.url | append: site.baseurl -%}
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": ["EducationalOrganization", "LocalBusiness"],
  "@id": {{ site_root | append: "/#organization" | jsonify }},
  "name": {{ org.name | default: site.title | jsonify }},
  "url": {{ site_root | append: "/" | jsonify }}

  {% if site.description %},
  "description": {{ site.description | jsonify }}
  {% endif %}

  {% if org.telephone %},
  "telephone": {{ org.telephone | jsonify }}
  {% endif %}

  {% if org.email %},
  "email": {{ org.email | jsonify }}
  {% endif %}

  {% if org.price_range %},
  "priceRange": {{ org.price_range | jsonify }}
  {% endif %}

  {% if org.address %},
  "address": {
    "@type": "PostalAddress",
    "streetAddress": {{ org.address.street | jsonify }},
    "postalCode": {{ org.address.postal_code | jsonify }},
    "addressLocality": {{ org.address.city | jsonify }},
    "addressRegion": {{ org.address.region | jsonify }},
    "addressCountry": {{ org.address.country | jsonify }}
  }
  {% endif %}

  {% if org.geo %},
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": {{ org.geo.latitude }},
    "longitude": {{ org.geo.longitude }}
  }
  {% endif %}

  {% if org.same_as and org.same_as.size > 0 %},
  "sameAs": {{ org.same_as | jsonify }}
  {% endif %}
}
</script>
{%- endif -%}
