  // ...

---
title: Multi file code demo
layout: sourcecode
---

# {{ page.title }}

## Try it out

{% include_relative demo.html %}
<style>{% include_relative styles.css %}</style>
<script>{% include_relative script.js %}</script>

## HTML 

<syntax-highlight language="html">
{% include_relative demo.html %}
</syntax-highlight>

## JavaScript

<syntax-highlight language="js">
{% include_relative script.js %}
</syntax-highlight>

## CSS

<syntax-highlight language="css">
{% include_relative styles.css %}
</syntax-highlight>
