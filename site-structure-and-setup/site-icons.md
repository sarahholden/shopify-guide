# Site Icons

### Setting up Site Icons

Using SVG icons and including them as inline SVGs will allow you to update the SVG with CSS as needed. For example, the hover color. Any icons used throughout the site should be turned into snippets and included as inline SVGs using the following steps:

\[ \] Check to make sure **gulp** is running \[ \] Go through the designs and **find any icons**. See examples of common icons below. \[ \] **Export all icons as** **svgs** to the dev/images\_for\_shopify folder. Optimized svg files will be output to dev/images\_for\_shopify\_optimized \[ \] Move all the optimized icons from **dev/images\_for\_shopify\_optimized** to the **snippets** folder. \[ \] **Rename** all files to start with `icon-` have a .liquid extension instead of .svg, and dashes between words, all lowercase. Example: `icon-caret-right.liquid` \[ \] Open the SVG files with your code editor and a**dd these attributes** to each svg, inside the opening tag:  
`class="sh-icon" aria-hidden="true" focusable="false" role="presentation"` \[ \] **When you want to use an icon**, use an include tag to include an icon in liquid. Example: \`

\` \[ \] **Push your changes to Github.**

**Examples of common icons that should be turned into snippets:**

![](https://i.imgur.com/4mfw9uP.png)

[https://i.imgur.com/4mfw9uP.png](https://i.imgur.com/4mfw9uP.png)

