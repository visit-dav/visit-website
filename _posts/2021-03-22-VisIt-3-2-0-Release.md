---
layout: page
show_meta: false
title: "VisIt 3.2 Release"
subheadline: "Numerous enhancements and bugfixes"
teaser: "Updated to support Python 3"
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

1. Updated to support Python 3.
  - Python 3 must now be used with VisIt. To support existing Python 2
    scripts, the **-py2to3** command line option has been added that
    performs limited Python 2 to Python 3 conversions.

2. Many new and enhanced database readers.
  - AVS ucd and FMS readers added.
  - Enhanced the MFEM, CGNS, Conduit Blueprint, boxlib, PlaninText, UNV, Tecplot, Silo, Stimulate, and Xolotl readers.

3. VTKm support has been enhanced.
  - Updated VTKm to a much newer version.
  - Added support for zone centered variables.
  - Added support for tetrahedra, pyramid and prism cells.

* [Downloads]({{ site.baseurl }}/releases-as-tables#latest)
* [More details]({{ site.baseurl }}/releases/release-notes-3.2.0)
