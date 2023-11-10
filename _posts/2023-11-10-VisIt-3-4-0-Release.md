---
layout: page
show_meta: false
title: "VisIt 3.4 Release"
subheadline: "Numerous enhancements and bugfixes"
teaser: "Added operator keyframing support"
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

Coming Soon!

1. Added the ability to keyframe operator attributes.

  - When in keyframe mode, VisIt will interpolate the operator attributes between operator keyframes.
  - Keyframing makes it possible to easily create sophisticated animations such as animating slice planes, iso surfaces and any operator attributes available.
  - Two new functions have been added to the Python scripting interface to support operator keyframing. They are `DeleteOperatorKeyframe` and `MoveOperatorKeyframe`.
  - A [tutorial](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/tutorials/KeyframeAnimation.html#keyframe-animation) has been added for creating keyframe animations.

2. Numerous enhancements have been made to the Blueprint reader.

  - Added the MFEM LOR setting to the MFEM Reader. Users may now choose between the new LOR scheme and the legacy LOR scheme. The new scheme is the default.
  - VisIt's Blueprint reader has been enhanced so related high order volume fraction fields from a matset are grouped into a material that can be used with the FilledBoundary plot. The high order material data fields are refined through MFEM LOR, whose refinement level can be controlled with the MultiresControl operator.
  - VisIt's Blueprint reader now supports materials with material numbers that do NOT fall in the range \[0, N\), where N is the number of materials.
  - VisIt's Blueprint reader now detects high-order volume fractions fields following the naming pattern volume_fraction_ZZZ as a material.
  - VisIt’s Blueprint reader now limits the total number of open HDF5 file handles.

3. A number of key libraries used by VisIt have been upgraded.

  - OSPRay has been updated to version 3.0.0.
  - VTK has been upgraded to version 9.2.6.
  - Qt has been upgraded to version 6.4.2.

* [Downloads]({{ site.baseurl }}/releases-as-tables#latest)
* [More details]({{ site.baseurl }}/releases/release-notes-3.4.0)
