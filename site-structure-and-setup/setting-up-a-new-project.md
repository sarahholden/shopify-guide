# Setting Up a New Project

**First Time Setup instructions:**

* [ ] If you haven't already installed Themekit on your command line [follow the instructions here](https://shopify.github.io/themekit/) to do so. 
* [ ] You'll also want to install the Gulp command line utility. Instructions [here](https://gulpjs.com/docs/en/getting-started/quick-start/).

**Code Setup:**

* [ ] Open the Themekit documentation [here](https://shopify.github.io/themekit/) and keep this handy.
* [ ] Fork this [repository](https://github.com/sarahholden/shopify_themekit_starter)
* [ ] Download to your computer

**Create a Private App:**

* [ ] Open the Shopify admin panel for the site, or create a development store from your partners account to get started.
  * [ ] Example: https://my-store-name.myshopify.com**/admin/**
* [ ] Create a private app
  * [ ] In the store’s Shopify admin, click **Apps**. 
  * [ ] Near the bottom of the page, click on **Manage private apps**.
    * If you see a notice that “Private app development is disabled”, then click “Enable private app development”. \(**Note:** Only the store owner can enable private app development\).
  * [ ] Click **Create new private app**.
  * [ ] Fill out your **name and email**
  * [ ] Toggle the **Show inactive Admin API permissions.** 
  * [ ] Scroll to the “Themes” section and select **Read and write** from the dropdown.
  * [ ] **Save**
  * [ ] **Copy the password** and keep it handy for a step soon :\)

**Connect your theme to the store**

* [ ] In the Shopify admin, go to Online Store &gt; Themes and **upload the starter theme zip** you downloaded from Github.
* [ ] **Rename** the theme for clarity using the "Actions" dropdown. Something like "Store Name Custom Theme". Example: "Troop Custom Theme"
* [ ] Click "**Customize**" on the theme you uploaded & renamed
* [ ] **Copy the theme ID** from the URL bar - it's the ~12 digit number - you'll use this in the next step.
  * Example: 116370440343
* [ ] **Update the "variables" file** in the starter theme you downloaded from Github:
  * [ ] Replace the **Theme ID** from the last step next to `SH_DEV_THEMEID=`
  * [ ] Replace in the **API password** you copied earlier next to `SH_DEV_PASSWD=`
  * [ ] Replace the **Store URL** in the variables file next to `SH_DEV_SHOP=`
    * No final "/" after the URL. 
* [ ] Go to the command line - cd into the theme folder and run this command:  `theme watch`
  * If this theme is live on the development store - you may need to use this: `theme watch --allow-live`

**Make sure you're hooked up**

* [ ] Go to Online Store &gt; Themes and click "Actions" &gt; "Preview" on the theme you uploaded. 
* [ ] Add "Hello World" in layout &gt; theme.liquid
* [ ] Save & make sure you see this message on the site
* [ ] cd into the "dev" folder, run `gulp watch`, and make sure this is set by changing the background of the body to red 

You're set!

[https://screenshot.click/themekit-private-app-setup-1000p15-192kbps.mp4](https://screenshot.click/themekit-private-app-setup-1000p15-192kbps.mp4)

