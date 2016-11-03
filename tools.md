---
layout: default
title: Seg3d Tools
category: info 
---

<script type="text/javascript">
<!--
    function toggle_visibility(id) {
       var e = document.getElementsByName(id)[0];
       if(e.style.display == 'block')
          e.style.display = 'none';
       else
          e.style.display = 'block';
    }
//-->
</script>

<style>
div.hidden {
    display: none;
}
</style>

<a id="top"></a>

# Seg3d Tools

{% comment %}from https://gist.github.com/pepelsbey/9334494{% endcomment %}
{% capture tmp %}
  {% for page in site.pages %}
    {% if page.category == "ToolDocs" %}
      {{ page.tool }}
    {% endif %}
  {% endfor %}
{% endcapture %}

{% assign categories = tmp | split: ' ' %}
{% assign tmp = categories[0] %}

{% for cat in categories %}
  {% unless tmp contains cat %}
    {% capture tmp %}{{ tmp }} {{ cat }}{% endcapture %}
  {% endunless %}
{% endfor %}

{% assign modulecategories = tmp | split: ' ' %}

{% capture modulepages %}
  {% for cat in modulecategories %}
    ?{{ cat }}
    {% for page in site.pages %}
      {% if page.tool == cat %}
        ${{ page.title }}#{{ page.url | prepend: site.github.url }}
      {% endif %}
    {% endfor %}
  {% endfor %}
{% endcapture %}

{% assign sortedpages = modulepages | strip | strip_newlines | split: '?' | sort %}

{% for pagestring in sortedpages %}
  {% assign pageitems = pagestring | split: '$' %}
  {% if pageitems[0] %}
## {{ pageitems[0] }}
    {% for item in pageitems %}
      {% comment %}skip category list item (index 0){% endcomment %}
      {% if forloop.first %} {% continue %} {% endif %}
      {% assign linkitem = item | split: '#' %}
      {% assign contentId = linkitem[0] | prepend: 'id_' %}

### <a name="{{linkitem[0]}}" data-proofer-ignore></a><a onclick="toggle_visibility('{{ contentId }}');" style="cursor: pointer;" data-proofer-ignore> {{ linkitem[0] }} </a>
      {% capture mdpath %}{{linkitem[1]}}{% endcapture %}
      {% capture my-include %}{% include {{mdpath}} %}  {% endcapture %}
      {% assign importantPart1 = my-include | split: 'Summary' %}
      {% assign importantPart2 = importantPart1[1] %}
<div class="hidden" markdown="1" name="{{contentId}}">{{ importantPart2  }} </div>
    {% endfor %}
  {% endif %}
{% endfor %}
