---
title: Multi file code demo
layout: sourcecode
---

# {{ page.title }}

{% include_relative styles.css %}
{% include_relative script.js %}
{% include_relative demo.html %}

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
