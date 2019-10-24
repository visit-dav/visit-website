---
layout: page
header:
  image_fullwidth: gallery_10a.png
permalink: "/examples/"
---

{% capture newline %}
{% endcapture %}

{%- for ex in site.examples -%}
{%- assign split_url = ex.image | split: '.' -%}
{%- capture thumb_url -%}{{split_url[0]}}-thumb.{{split_url[1]}}{%- endcapture -%}
|[![]({{ site.urlimg }}{{ thumb_url }})]({{ ex.url }}){%- cycle "", "", "", newline -%}{%- endfor -%}