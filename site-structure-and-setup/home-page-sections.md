# Home Page Sections

​

* [ ] For each section on the home page, **create a file in the sections folder**.
  * Files should be formatted: `home-section-name.liquid` 
  * Example: `home-slideshow.liquid`
* [ ] Add a schema tag at the bottom of the file using the snippet below as a template.
* [ ] Replace the name & category in the presets
  * Presents are _only_ used for the home page
  * The name and category will be shown in the CMS when the client is adding a new section \(see screenshot\)
* [ ] Replace other text that says "Featured collection" with your section name
* [ ] Repeat for each section on the home page

{% code title="sections/home-featured-collection.liquid" %}
```text
{{ section.settings.title }}

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

