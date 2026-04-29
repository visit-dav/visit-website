---
layout: page
show_meta: false
title: "VisIt 3.5 Release"
subheadline: "Numerous enhancements and bugfixes"
teaser: "Enhanced MFEM Low Order Refinement"
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

1. Enhanced MFEM Low Order Refinement.
  - The MultiresControl Operator has been enhanced with new High-Order Options for high-order data from the MFEM and Blueprint plugins. High-order options include refinement basis selection (Gauss Lobatto and Closed Uniform), grid function projection method selection (nodal and zonal projection), and mesh refinement method selection (continuous and discontinuous refinement).

2. Added several key enhancements.
  - Support has been added for ANARI advanced rendering. ANARI is a cross-platform 3D rendering engine that supports multiple rendering backends including RadeonProRender, OSPRay and VisRTX. It can generate USD output for use in the Omniverse platform. ANARI rendering is enabled in the *Advanced* tab on the *RenderingOptions* window.
  - Refactored how to import VisIt into a stand alone python module. This is now done via the *visit_launcher* module, avoiding module namespace issues.
  - Eliminated many memory leaks. These include leaks in ghost the zone removal and external facelist operator, the resample operator, the zone_centers expression and all the plots.
  - The Blueprint writer was enhanced to support YAML and JSON exports.
  - Ghost zone exchange was enhanced to handle tensors, symmetric tensors and array variables.

3. A number of key libraries used by VisIt have been upgraded.
  - VTK has been upgraded to version 9.5.0.
  - Silo has been updated to 4.12.0.
  - HDF5 has been updated to 2.0.0.
  - Conduit has been updated to 0.9.4.
  - MFEM has been updated to 4.8.
  - Python has been updated to 3.13.9.
  - NetCDF has been updated to 4.9.3.
  - VTK-m has been updated to 2.3.0.
  - CMake has been upgraded to 3.31.8.
  - OpenEXR has been upgraded to 3.3.4.
  - Zlib has been upgraded to 1.3.1.

* [Downloads]({{ site.baseurl }}/releases-as-tables#latest)
* [More details]({{ site.baseurl }}/releases/release-notes-3.5.0)
