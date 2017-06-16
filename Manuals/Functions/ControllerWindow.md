---
layout: default
title: ControllerWindow
category: FunctionDocs 
function: 
  chapter: Seg3DWindows
  subchapter: 
---

# {{ page.title }} 

## Category

**{{ page.function.chapter }}**

## Description

The Controller Window is not opened by default when Seg3D is opened. To open the window, click the ’Window’ option in the task bar and select the Controller option. The window may also be toggled by using the key command: Shift+CTRL/CMD+C. Notice the Controller Window option in the window drop-down menu is located below a separator. This indicates that the window will open a new pop-up window outside of the general Seg3D user interface.

The Controller window supplies the user with all of the data, variables, history, and logs of the current Seg3D session. There are four tabs that can be selected in this window:

{% comment %}from https://gist.github.com/pepelsbey/9334494{% endcomment %}
{% capture toolpages %}
  {% for page in site.pages %}
    {% if page.function.subchapter == "ControllerWindow" %}${{ page.title }}#{{ page.url | prepend: site.github.url }}
    {% endif %}
  {% endfor%}
{% endcapture %}

{% assign pageitems = toolpages | strip | strip_newlines | split: '$' | sort %}
{% if pageitems[0] %}
  {% for item in pageitems %}
    {%if forloop.first %} {% continue %} {% endif %}
    {% assign linkitem = item | split: '#' %}
**[{{ linkitem[0] }}]({{ linkitem[1] }})**
  {% endfor %}
{% endif %}

{% capture url %}{% include functionurl.md%}{% endcapture %}
{{ url }}

