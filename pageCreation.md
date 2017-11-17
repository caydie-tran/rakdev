---
layout: page
title: Adding Content
intro:
- image_path: /assets/images/flower.jpg
  excerpt_label: Introduction
  excerpt: The Rakuten Developer Portal uses the power of Jekyll's static site generation technology and the simplicity of yaml key value pairing to make creating documentation pages easy. On this page we will go over how to add content to your newly created documentation page using yaml.
sample:
- image_label: Sample File
  image_path: /assets/images/sample_yml.jpg
  excerpt: As you can see here the configuration required to create a good looking documentation page consists of simply filling out yaml key/value pairs. Styling and positioning is all taken care of. There is one concept that you really need to understand and that is "feature rows".
concept: 
- image_label: Feature Rows
  image_path: /assets/images/row.jpg
  excerpt: You can think of feature rows as the building blocks of your page. The first step to creating a feature row is to define a yaml key which you can name whatever you'd like. In the screenshot above we've named one of our feature rows "row1". We then added specific nested key/values that suit provide us with exactly what we need for our documentation page. Here is what this specific feature row configuration produces.
outcome:
- image_path: /assets/images/outcome.jpg
keys:
- excerpt_label: Feature Row Key/Value Cheatsheet
  excerpt: Here is a list of all the keys/values that are provided to build your documentation page.
  ul:
  - bullet: image_label - if you are planning on including an image in your feature row, this key will add a title/label to the top of it.
  - bullet: image_path - you can specify either a url or the root path to your image.
  - bullet: excerpt_label - if you plan on adding an excerpt to your row this key will add a label on top of it.
  - bullet: excerpt - add text in paragraph form to your feature row.
  - bullet: list_label - if you plan on adding a list to your feature row then this key will add a label on top of it.
  - bullet: ul/bullet - ul is a key that allows you to create a bulleted list. the bullet key/value pairs are nested within the ul key. Each bullet key will create an additional bullet point in the list.
  - bullet: codeBlock - if you have any code snippets that you want to include in your feature row, the codeBlock key provides a nice component for that.
include:
- excerpt: Once you configure the yaml for your feature row you then need to "include" it below your yaml configuration. As you can see in the screenshot above all you need is the name of your feature row which will be your ID. Here is the line that you need to "include" the "row1" feature row.
  image_label: Including your feature row
  image_path: /assets/images/include.jpg
--- 

{% include feature_row id="intro" %}
lala
{% include feature_row id="sample" %}
{% include feature_row id="concept" %}
{% include feature_row id="outcome" %}
{% include feature_row id="keys" %}
{% include feature_row id="include" %}