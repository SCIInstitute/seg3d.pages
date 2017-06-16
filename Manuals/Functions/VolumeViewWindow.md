---
layout: default
title: VolumeViewWindow
category: FunctionDocs 
function: 
  chapter: Seg3DWindows
  subchapter: 
---

# {{ page.title }} 

## Category

**{{ page.function.chapter }}**

## Description

The Volume View Window is not opened by default when Seg3D is opened. To open the window, click the ’Window’ option in the task bar and select the Volume View option. The window may also be toggled by using the key command: Shift+CTRL/CMD+V. Once activated, the window will appear on the right and side of the Seg3D panel covering the layer mask window. To toggle back to the layer mask window, click the Layer Manager tab at the bottom of the page. The Volume View Window has three separate options for volume displaying.

{% comment %}from https://gist.github.com/pepelsbey/9334494{% endcomment %}
{% capture toolpages %}
  {% for page in site.pages %}
    {% if page.function.subchapter == "VolumeViewWindow" %}${{ page.title }}#{{ page.url | prepend: site.github.url }}
    {% endif %}
  {% endfor%}
{% endcapture %}

{% assign pageitems = toolpages | strip | strip_newlines | split: '$' | sort %}
{% if pageitems[0] %}
## Functions found within this section.
  {% for item in pageitems %}
    {%if forloop.first %} {% continue %} {% endif %}
    {% assign linkitem = item | split: '#' %}
**[{{ linkitem[0] }}]({{ linkitem[1] }})**
  {% endfor %}
{% endif %}

{% capture url %}{% include functionurl.md%}{% endcapture %}
{{ url }}

