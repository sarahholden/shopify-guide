# Home Page Sections

​

{% code title="sections/home-featured-collection.liquid" %}
```text
{% schema %}
  {
    "name": "Featured collection",
    "settings": [
      {
        "type": "text",
        "id": "title",
        "label": "Heading",
        "default": "Featured collection"
      },
      {
        "id": "collection",
        "type": "collection",
        "label": "Collection"
      }
    ],
    "presets": [
      {
        "name": "Featured collection",
        "category": "Collection"
      }
    ]
  }

{% endschema %}
```
{% endcode %}

![](https://i.imgur.com/z1PLbFK.png)

​[  
](https://shopify-docs-1.gitbook.io/shopify-docs/site-structure-and-setup/site-icons)

