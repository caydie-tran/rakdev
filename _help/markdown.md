---
layout: page
title: Markdown Editor
top:
- excerpt_label: Markdown Editor
---
<link rel="stylesheet" href="https://cdn.jsdelivr.net/simplemde/latest/simplemde.min.css">
{% include feature_row id="top" %}
<textarea></textarea>

 <script src="https://cdn.jsdelivr.net/simplemde/latest/simplemde.min.js"></script>
  <script>
    var simplemde = new SimpleMDE({
        toolbar: ["bold", "italic", "strikethrough", "heading-smaller", "heading-bigger",  "code", "quote", "unordered-list", "ordered-list", "clean-block", "link", "image", "table", "horizontal-rule", "preview", "side-by-side", "fullscreen", "guide"]
    });
    simplemde.value("This editor will help you add Markdown to your content!");
  </script>  