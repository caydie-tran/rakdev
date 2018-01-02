---
layout: help
weight: 2
stepone:
- image_path: /assets/images/root_product_folder.png
  image_label: Product/Feature Root Directory
  excerpt: Whatever product/feature you are creating documentation for will have it's own directory in the root of the repository. This should have already been created for you by the Admins of the portal. If it has not yet been created please contact <nicholas.foti@rakuten.com>. All of your documentation files will live in this product /feature specific directory.
steptwo:
- image_path: /assets/images/parent_markdown.png
  image_label: Parent Markdown files
  excerpt: You will separate your markdown files into parents and children of those parents. This is how we organize what is displayed on the side menu of your documentation page. The parent markdown files will become the main items on the side menu and the child markdown files will be organized under their respective parent menu item. All parent markdown files will be located in the root of your product specific directory.
stepthree:
- image_path: /assets/images/side-menu.png
stepfour:
- image_label: Child Markdown files
  image_path: /assets/images/child-markdown.png
  excerpt: Each parent markdown file (located in the specific Product/Feature directory root) should have it's own corresponding folder (also located in the root of the Product/Feature directory). In that corresponding folder is whaere all of the children of that parent will be located. There is also an optional images folder within the corresponding parent folder that houses all of the images that the children pull from.
stepfive: 
- image_label: YAML for parent markdown files
  image_path: assets/images/parent-yml.png
  excerpt: Each markdown file (this includes both parent and children) require a small amount of Yaml at the top of the page. The Yaml section of the page is separated by a triple hyphen "---". The required Yaml for Parent files is as follows.
  ul:
  - bullet: <strong>title:</strong> Whatever title you would like this parent page to have.
  - bullet: <strong>layout:</strong> This will be the same name of whatever product/feature you are creating documentation on.
  - bullet: <strong>weight:</strong> Weight is not required but this will determine the ordering of your parent menu items on the side menu. Lower weights rise to the top!
  - bullet: <strong>permalink:</strong> This is how you set the URL path to each menu item. In this particular screenshot we have set the url to "/helpcenter-mobile/features/analytics/". This url is navigating through the folder structure to serve a specific markdown file to the browser. helpcenter-mobile directory --> features folder --> analytics.md file. In this case the parent item is serving as a placeholder and just links to the first child item "analytics".
stepsix:
- image_label: YAML for child markdown files
  image_path: /assets/images/child-yml.png
  excerpt: The markdown required for child markdown files is similar to the markdown required for parent markdown files.
  ul:
  - bullet: <strong>title:</strong> Whatever title you would like your child page to have.
  - bullet: <strong>layout:</strong> This will be the same name of whatever product/feature you are creating documentation on.
  - bullet: <strong>parent:</strong> Absolute path to the parent markdown file which will always be /[product/feature directory located in root]/[parent markdown file].
  - bullet: <strong>categories:</strong> The developer portal serch function works based on the categories you set here. So make sure to include relevant keywords within these square brackets "[]".
  - bullet: <strong>permalink:</strong> This is how you set the URL path to each menu item. As you may have noticed the url path for this child item is the same as the url for the parent item in the above screenshot. That is because they are linking to the same thing (with the parent item serving as a placeholder).
  - bullet: <strong>weight:</strong> Weight is not required but will determine the order of your child elements. Lower weights rise to the top!
---

{% include feature_row id="stepone" %}
{% include feature_row id="steptwo" %}
{% include feature_row id="stepthree" %}
{% include feature_row id="stepfour" %}
{% include feature_row id="stepfive" %}
{% include feature_row id="stepsix" %}


