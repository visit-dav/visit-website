---
layout: page
title: Examples Gallery
header:
    image_fullwidth: "summit_and_sierra-fs8.png"
permalink: "/examples/"
---

{% comment %}
This Liquid coding is doing a few things. First, it is using Liquid's sample filter to
randomize the contents of the gallery each time the site is generated. This helps newer
content appear near the top of the gallery instead of always at the bottom. Next, it 
is using Liquid's cycle filter to produce output lines in groups of 5. Next, it
is actually templating a markdown line for each row of images in the gallery, not an html
line. That is, it is ultimately creating a markdown table where each entry in the table
is of the form...

    [![](path/to/image)](path/to/example "example title")

This is actually an image that is itself a link to another URL. The image refernece,
![]()/path/to/image), is itself embedded in the `[]` block of a `[]()` markdown link.
{% endcomment %}

{% capture newline %}
{% endcapture %}

{% assign n = site.examples | size %}
{% assign shuffled_examples = site.examples | sample: n %}
{%- for ex in shuffled_examples -%}
{%- assign split_url = ex.image | split: '.' -%}
{%- capture thumb_url -%}{{split_url[0]}}-thumb.{{split_url[1]}}{%- endcapture -%}
|[![]({{ site.urlimg }}{{ thumb_url }})]({{ site.baseurl }}{{ ex.url }} "{{ ex.title}}"){%- cycle "", "", "", "", newline -%}{%- endfor -%}
