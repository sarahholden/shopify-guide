# Navigation



### Start the Project

* [ ] `cd` into the theme folder in terminal.
* [ ] Run `theme watch` from the **main theme folder**
* [ ] Run `gulp watch` from the **dev** folder

### Setting up the navigation

1. **Set up Menus in admin panel**
   * [ ]  Go to Online Store &gt; **Navigation**
   * [ ]  **Create a new menu** \(Or menus if breaking it up makes sense\) for the header nav. 
     * If menus exist and this is a live site, create new menus. Don’t edit existing menus. 
   * [ ]    **Add links for each page.**
     * The login / account link is : `/account/login`
     * Menus can be **nested** inside each other if needed. For example, you can add a submenu under "Shop" with categories.
   * [ ] Save after adding links 
2. **Add the menus to the schema in your code editor**

   * [ ] Make sure themekit and gulp are running
   * [ ] Open sections &gt; header.liquid
   * [ ] Scroll down to the schema. There’s one menu added at the bottom. If the site has more than one header nav, copy this block & give the copied block a new label and id \(type should stay the same\)
   * [ ] Scroll back up in that file. For each linklist include the nav menu snippet by updating the id on this line:
   * [ ] Repeat this process for sections/footer.liquid to include any footer menus
   * [ ] Save, add, commit, and Push to Github



   **3. Connect in the theme**

   * [ ] Go to the admin panel - Online Store &gt; Themes &gt; Customize \(make sure to select the theme you’re working on\)
   * [ ] Click “Header” in the customizer
   * [ ] Select the menus you need in the sidebar
   * [ ] Menus should appear on the page!
   * [ ] Repeat for the Footer

