---
title: Multi file code demo
layout: sourcecode
---

# {{ page.title }}

{% include_relative demo.html %}
<style>{% include_relative styles.css %}</style>
<script>{% include_relative script.js %}</script>

## HTML 

```html
{% include_relative demo.html %}
```

## JavaScript

```javascript
{% include_relative script.js %}
```

## CSS

```css
{% include_relative styles.css %}
```
