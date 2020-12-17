---
description: >-
  Objective of this page: Explain Shopify's URL conventions for images and how
  to automatically pull in the smallest image size needed for display.
---

# Liquid Images

### Overview on how Shopify sizes images based on the URL:

Shopify allows you to pull in a scaled image through its CDN by adding a width to the URL. 

For example the \_720x.jpg part of this url will pull in a 720px wide version of this image:

`https://cdn.shopify.com/s/files/1/0502/0286/9911/files/Screen_Shot_2020-08-28_at_2.34.07_PM_2x_10598356-b0bb-45c5-ab9e-986c9b25df3e_720x.jpg`

And the 320x part here will pull in a an image that's 320px wide.

`https://cdn.shopify.com/s/files/1/0502/0286/9911/files/Screen_Shot_2020-08-28_at_2.34.07_PM_2x_10598356-b0bb-45c5-ab9e-986c9b25df3e_720x.jpg`

You can add any size you want here - these are not predefined. 

\*\*\*\*❗ **To ensure responsiveness, never use a height, just a width!**

\*\*\*\*

### **LazySizes Plugin**

💡 **Tip:** use the snippet `lazyimg` to autocomplete the following code :\) 

Instead of pulling in the largest size of an image that will be needed, use the LazySizes plugin to dynamically pull in the right size image. For a small screen this might be 320px wide. For a large screen this might be 2800px wide. 

LazySizes and the Rias plugins are already installed on the starter theme - here's how to use this in liquid:

* **data-src** is used on this image in place of a src attribute
* **data-widths** specifies the widths that will be generated. 
* **data-sizes="auto"** will automatically pull in the right size image for the browser width.
* The lazyload class will lazy load this image, only loading it when it's close to being in viewport. 
* The `.fade-in` class is an animation I've set in images.scss to fade the image in on load.
  * You can also use `.fade-and-scale` to fade an image in and scale it down \(nice animation for hero images\)
* The weird **assign img\_url** line ties in with the Rias plugin for LazySizes to create the URL options

\*\*\* All you need to add here is to replace `section.settings.image` with your image and `section.settings.image_alt` with the alt text for your image.

```text
{% assign image = section.settings.image %}
{% assign alt_text = section.settings.image_alt | escape %}
{% assign img_url = image | img_url: '1x1' | replace: '_1x1.', '_{width}x.' %}

<img
class="lazyload fade-in"
data-src="{{ img_url }}"
data-widths="[360, 540, 720, 900, 1080, 1600, 2200, 2800]"
data-sizes="auto"
alt="{{ alt_text }}"
>
```

Here's the generated output. If you open the network tab starting on a small screen and resize the screen to be larger, you'll notice it will pull in larger images as the screen gets wider. 🔮 

![](https://i.imgur.com/jp5DIZY.png)

For reference, here's how to add image fields to the CMS in the schema.

💡 **Tip:** use the snippet `schimage` to autocomplete the image and image\_alt inside a section schema.

```text
{% schema %}
{
  "name": "demo",
  "settings": [
    {
      "id": "image",
      "type": "image_picker",
      "label": "Image"
    },
    {
      "id": "image_alt",
      "type": "text",
      "label": "Image Alt",
      "info": "Write a brief description of this image to improve search engine optimization (SEO) and ADA accessibility."
    }
  ]
}
{% endschema %}
```

