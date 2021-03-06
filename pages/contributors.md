---
layout: page
header:
  image_fullwidth: gallery-07a.png
permalink: "/contributors/"
foo: cyrush
---

{% comment %}
This is using Liquid to form a Markdown table. Others would use raw html for same.

Markdown is sensitive to spaces whereas HTML is not. So, one has to go to great lengths
to control the spacing here.

The capture newline is to capture an actual newline character in the newline variable
as Liquid doesn't understand "\n" as a newline.

The long sequence of non-breaking spaces (&nsbp;) is to ensure that the first column
of the table is wide enough to hold reasonably sized pictures.

The person's bio about themselves is truncated to 100 words.
{% endcomment %}

{% capture newline %}
{% endcapture %}

### Active Developers

|**Name**|**Bio**|
|:---|:---|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||
{% for person in site.data.developers.active -%}
  {%- assign pname = person | first -%}
|![]({%- if site.data.developers.active[pname].pic -%}{{ site.data.developers.active[pname].pic }}{%- else -%}{{site.url}}{{site.baseurl}}/images/default-developer-picture.png{%- endif -%})<br>{{- site.data.developers.active[pname].name -}}<br>{{- site.data.developers.active[pname].affiliation -}}&nbsp;[email](mailto:{{- site.data.developers.active[pname].email -}})&nbsp;[GitHub]({{- site.data.developers.active[pname].github -}})|{{- site.data.developers.active[pname].bio | replace: newline, " " | replace: "<p>", " " | replace: "</p>", " " | strip_newlines | truncatewords: 100 -}}|
{% endfor %}

### Former Developers

{% for person in site.data.developers.former -%}
|{{person.name}}{%- if person.affil -%}<br>({{person.affil}}){%- endif -%}{%- cycle "", "", "", newline -%}{%- endfor -%}
{{newline}}

### Other contributors and collaborators

{% for person in site.data.developers.contributors -%}
|{{person.name}}{%- if person.affil -%}<br>({{person.affil}}){%- endif -%}{%- cycle "", "", "", newline -%}{%- endfor -%}
