---
layout: help
title: Publishing Content
fork:
- image_label: 1. Fork the rakDev repository
  image_path: /assets/images/git-fork.png
  image_caption: Go to https://github.com/Melvine/rakdev and fork the repository.
folder:
- image_label: 2. Create your department folder in the root directory
  image_path: /assets/images/create-folder.png
  image_caption: Once you clone the newly forked repo and have it open in your IDE/Text Editor create a new folder with your department or company name in the root directory.
pages:
- image_label: 3. Create pages within your department folder 
  image_path: /assets/images/create-page.png
  image_caption: Create pages within the department folder you just created. Any pages within this folder will automatically populate of your department page sidemenu.
contents:
- image_label: 4. Add content to your page with YAML, Markdown or HTML
  image_path: /assets/images/moreContent.png
  image_caption: Content can be added to your page using our custom yaml key/value pairs, markdown or HTML. You can also use a combination of the three if you prefer!
push:
- image_label: 5. Push your new folder and pages and create a Pull Request 
  image_path: /assets/images/pull-request.png
  image_caption: Commit/push your changes. Then make a pull request. We will review the changes you've made and then merge them. The changes you made should be automatically deployed shortly after.
---
{% include feature_row id="fork" %}
{% include feature_row id="folder" %}
{% include feature_row id="pages" %}
{% include feature_row id="contents" %}
{% include feature_row id="push" %}

