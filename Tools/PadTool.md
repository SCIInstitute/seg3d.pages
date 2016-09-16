---
layout: default
title: Pad
category: ToolDocs 
tool: Tools
---

# {{ page.title }} 

## Category

**{{ page.tool }}**

## Description

### Summary

The pad tool allows the user to pad one or more volumes. This tool can be used on both mask and data layers.

### Detailed Description

The pad amount is set manually using the sliders. There are options to resample with the same ratio in every direction (check "Constrain Aspect" option) or to resample each direction independently (must uncheck "Constrain Aspect" option to enable). Pad values can be zero, the dataset min or max.

![alt text]({{ site.github.url }}/images/{{ page.title }}GUI.png)

{% capture url %}{% include url.md%}{% endcapture %}
{{ url }}
