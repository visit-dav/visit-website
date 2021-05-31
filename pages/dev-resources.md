---
layout: page
title: "Developer Resources"
header:
   image_fullwidth: "gallery-33-large.jpg"
permalink: "/dev-resources/"
---

### Current

* [VisIt organization on GitHub](https://github.com/visit-dav)
* [Main code repo](https://github.com/visit-dav/visit)
* [Nightly test results](https://visit-dav.github.io/dashboard/) and [repo](https://github.com/visit-dav/dashboard)
* [RTD manuals](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/)
* [Website](https://visit-dav.github.io/visit-website/) and [repo](https://github.com/visit-dav/visit-website)
* [GitHub developer notes](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/dev_manual/GitHub.html)
* [Third party repo](https://github.com/visit-dav/visit-deps)
* [Large data shares](https://visit-dav.github.io/largedata/) and [repo](https://github.com/visit-dav/largedata)
* [GitHub releases](https://github.com/visit-dav/visit/releases) and [tables]({{site.baseurl}}/releases-as-tables/)

### Issues

* [Unreviewed](https://github.com/visit-dav/visit/issues?utf8=✓&q=is%3Aissue+is%3Aopen+-label%3Areviewed)
* [All Open](https://github.com/visit-dav/visit/issues)
* [Priority](https://github.com/visit-dav/visit/issues?q=is%3Aissue+is%3Aopen+label%3Apriority+sort%3Acreated-desc)
* [High Likelihood / High Impact](https://github.com/visit-dav/visit/issues?q=is%3Aopen+label%3A%22likelihood+high%22+label%3A%22impact+high%22)
* [Low hanging fruit](https://github.com/visit-dav/visit/issues?q=is%3Aissue+is%3Aopen+label%3A%22low-hanging+fruit%22+)
* [Good first issues](https://github.com/visit-dav/visit/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22)
* Issues Assigned to:
<form id="myForm" action="https://github.com/visit-dav/visit/issues" method="GET">
<select name="assignee">

{% comment %} Build string of space separated first name/github handle pairs {% endcomment %}
{% assign pairs = "" %}
{% for person in site.data.developers.active %}
  {% assign pname = person | first %}
  {% assign pobj = site.data.developers.active[pname] %}
  {% assign ghhandle =  pobj.github | remove_first: "https://github.com/" %}
  {% assign name =  pobj.name | split: ' ' | first %}
  {% assign pair = name | append: "/" | append: ghhandle %}
  {% assign pairs = pairs | append: " " | append: pair %} 
{% endfor %}

{% comment %} Turn space separated string into array and sort by first name {% endcomment %}
{% assign pairs = pairs | split: ' ' | sort %}

{% comment %} Output form options for each first name, github handle pair {% endcomment %}
{% comment %} Use special - form of liquid to avoid introducing embedding everything in <p></p> {% endcomment %}
{%- for pair in pairs -%}
  {%- assign name = pair | split: '/' | first -%}
  {%- assign ghandle = pair | split: '/' | last -%}
  {%- capture optline -%}
  <option value="{{ ghandle }}" ID="{{ ghandle }}">{{ name }}</option>
  {%- endcapture -%}
  {{- optline -}}
{%- endfor -%}
</select>
    <input type="submit" value="submit" />
</form>

### Older resources

* [Older releases](https://wci.llnl.gov/simulation/computer-codes/visit/executables)
* [VisIt User's Wiki]({{site.baseurl}}/visit-users-wiki/)
* VisIt User's Email list
  * [Admin Page](https://elist.ornl.gov/mailman/admindb/visit-users)
  * [Archive](https://elist.ornl.gov/mailman/private/visit-users)

