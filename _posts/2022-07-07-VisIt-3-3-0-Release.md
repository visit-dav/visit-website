---
layout: page
show_meta: false
title: "VisIt 3.3 Release"
subheadline: "Numerous enhancements and bugfixes"
teaser: "Enhanced color table support"
tags:
    - post format
categories:
    - releases
header:
    image_fullwidth: release-banner.jpg
image:
    thumb: release-thumbnail.png
author: brugger1
---

1. Enhanced and modified the color table handling.
  - Many color tables from [Fabio Crameri](//www.fabiocrameri.ch/visualisation/) have been added for individuals who are color vision deficient (CVD).
  - A new tagging system has been introduced to make it easier to handle the increased number of color tables.

2. Added the ability to repartition or flatten domain decomposed data.
  - When exporting data to Blueprint files, the user can now repartition or flatten the data.
  - It is now possible to directly access flattened data from the Python scripting interface.

3. Many enhancements to the database readers.
  - Numerous enhancements have been made to the Blueprint reader.
    - Adding support for implicit points.
    - Adding support for polyhedral meshes.
    - Added a new Low Order Refine method for MFEM meshes.
  - The WData reader was added.
  - Enhancements were made to the Chombo, Xmdv, Xolotl, NASTRAN and ADIOS2 readers.


* [Downloads]({{ site.baseurl }}/releases-as-tables#latest)
* [More details]({{ site.baseurl }}/releases/release-notes-3.3.0)
