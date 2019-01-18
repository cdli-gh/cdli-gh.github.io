---
title: Intro for editors
sidebar:
  nav: "guides"
permalink: /guides/guide_docs_edit.html
---

## Quick steps to prepare a doc
To add a new documentation page to this site:

1. Create your doc page in the markdown format with the markdown extension (.md)  
2. Upload your file in the pages/cat/ folder (make sure it has a unique name)  
3. Add your page to the menu in \_data/sidebars/home_sidebar.html  
4. Wait two minutes and check that all is in order  

## YAML header
For your doc to work properly, it must have a YAML header. You can check out the other docs to use as a model or copy and paste this block at the head of your file:  

```md
---
title: Title here
keywords:
tags:
sidebar:
  nav: "research" || guide || cdli
permalink: /cat_nameofmyfile.html
summary:
---
````
The permalink field must contain the name of your markdown file with the extension removed and with .html added.

## The Markdown format
The markdown format is a simplified markup that can easily be converted to html. Basically, you write your doc in plain text and add structure elements to minimally style the content, eg. \# in front of a title will make it into "Header 1" format. Markdown syntax is very simple, see this link for a list of structure elements:
[GitHub markdown basic syntax guide](https://guides.github.com/features/mastering-markdown/#syntax).
If you have have questions or need assistance, get in touch with Émilie Pagé-Perron.

*Émilie Pagé-Perron*
