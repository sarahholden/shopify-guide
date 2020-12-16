# File Structure



### Start the Project

* [ ] `cd` into the theme folder in terminal.
* [ ] Run `theme watch` from the **main theme folder**
* [ ] Run `gulp watch` from the **dev** folder

### Setting up the file structure

Several of the following steps will require the same file structure. Follow these steps:

* [ ]  **Evaluate the designs** \(the header and footer are usually helpful for this\) and determine what pages should be included on the site. \[ \] For each collection in the design \(examples: “Shop” “Hair” “Body”\) **create a collection** in the admin panel under Products &gt; Collections. Some sites may only have a “Shop” collection.
* Tip: When creating a collection choose manual for sections where you think the client will want to pick products, automatic when the products should be pulled in \(for example, all haircare products\)

**Set up local files:**

* [ ] Make sure **themekit and gulp** are running. \[ \] For other site pages like about, contact, faq, etc., **create a template in the templates folder**.
* Examples: `page.about.liquid` or `page.contact.liquid`
* Check to make sure it doesn’t already exist since I’ve added some. 
* Name it `page.page-name.liquid` . 
* Skip legal pages like returns, privacy policy, terms of use, etc.
* Skip any collections listed in the nav. These will use the collection.liquid template.

  \[ \] In each template file you created **include a section by the same name** \(we’ll create these sections in the next step\). Add in something like the following, replacing with your page name. 

  Example: `{%- section 'section-about' -%}` or  `{%- section 'section-contact' -%}`

  \[ \] Now for each page **create a section file** in the sections/ folder. Name them section-page-name.liquid. These names should match the names you used in the last step.

  Examples: `section-faqs.liquid`   or `section-contact.liquid`

  \[ \] **Write some dummy text in each section file** so you’ll be able to see if these are hooked up before you start adding real content. I usually use the page name or something like “Hello from the about page”

  \[ \] Save, add, commit, and **Push to Github**

**Hook up files to Shopify Admin**

\[ \] Go to Online Store &gt; Pages in the left sidebar of the admin panel. \[ \] Create pages for any of the pages in the design \[ \] Give the page a name and select the template for that page in the right sidebar dropdown \(don’t see the template name? See tip below.\) \[ \] Save \[ \] Repeat \[ \] **💡 TIP:** If you’re not working on the published theme, you’ll need to create template files in that theme for them to be recognized in the template dropdowns when creating pages. 😞 IF that’s the case:

* Go to Online Store &gt; Themes 
* Actions &gt; Edit Code on the published theme \(careful not to edit any code on the live site!\)
* **If the page doesn’t already exist** under “Templates” click “Add a new template”
* Name the new file “Page” + the page name you used in your code editor. 
* Delete the dummy content Shopify adds to a new file and save the file. It should just be a blank file. 

