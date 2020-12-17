---
description: >-
  I've set up a gulp task to automatically optimize any images that are saved
  into the dev/images_for_shopify folder when gulp is running. Images get
  exported to dev/images_for_shopify_optimized folder
---

# Image Optimization

### Start the Project

* [ ] `cd` into the theme folder in terminal.
* [ ] Run `theme watch` from the **main theme folder**
* [ ] Run `gulp watch` from the **dev** folder

### Export images from the Design

* [ ] **Export** all images from Sketch or XD. 
  * Export for **web at 2x**.  \(screenshots below\)
  * For vector images that need to stay crisp at all sizes \(logos, etc.\) export as .svg
  * For any images that don't need transparency, use .jpg/.jpeg file format. 
  * For images that need transparency export as .png
* [ ] **Save all images** to the **`dev/images_for_shopify`** 
  * Images will **auto-optimize** if gulp is running and the optimized versions will be spit out to **`dev/images_for_shopify_optimized`** folder.
* [ ] **Drag and drop the optimized images from `dev/images_for_shopify_optimized`**to a folder on your computer outside the project folder so they are ready when they need to be uploaded as you build out the site \(but we don't really need those on Github\)
* [ ] **Delete the original, unoptimized images** in **`dev/images_for_shopify`** 

### Sketch Screenshots:

![Select image then click &quot;Make Exportable&quot; in sidebar at 2x jpg](https://i.imgur.com/eWrSG4V.jpg)

![90% is fine for quality](https://i.imgur.com/UeSjPN3.jpg)



### XD Screenshots:

![](https://i.imgur.com/B1kMfwi.jpg)

![](https://i.imgur.com/fhdIKmr.jpg)















