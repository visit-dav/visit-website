---
layout: page
title: "Release Notes for VisIt 3.3.2"
header:
  image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.3.2/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.3.2

* Fixed a bug on macOS that prevented VisIt from browsing files and folders in the Desktop, Documents, or Downloads folders when launched by double-clicking the icon, even when the user gave VisIt permission to do so.
* Fixed a bug reading Mili material variables when the mesh had multiple domains.
* Fixed a bug causing the blueprint plugin to incorrectly assign a zonal association to mfem grid functions that were neither H1 nor L2.
* Fixed a bug reading a ".visit" file with more than 10,000 files and comments for each file.
* Fixed a bug that caused the compute engine to crash when in scalable rendering mode. The specific bug involved saving non screen capture images, but the crash could occur whenever doing scalable rendering.
* Fixed a bug in the Mili reader where the Green Lagrange strain was using incorrect initial coordinates.
* Fixed a bug preventing files with the extension ".h5m" from being grouped with smart grouping turned on.
* Fixed a rare issue with the color table window that caused it to resize horizontally larger than the screen, causing buttons to be off the screen.
* Fixed a bug with Pick where it incorrectly used the node origin.
* Fixed a bug where "atan2" did not show up in the list of expressions in the Expressions window.
* Fixed a bug with the Mili reader where variables that were only defined on a portion of the nodes weren't being placed on the correct nodes.
* Fixed the default attributes repr() behavior in the CLI to again print attribute details. This was unintended change introduced with Python 3 support.
* VisIt's internal ssh (qtssh) was updated with latest putty version (0.78) to fix client-server connection issues from Windows.

### Enhancements in version 3.3.2

* Added a tutorial on Partitioning to the documentation.
* In the X Ray Image Query, a warning was added for the BMP output type, saying it may not function properly. This output type will be removed in the next major release of VisIt.
* For Blueprint output types from the X Ray Image Query, a host of new metadata has been added, as well as the imaging plane topologies.
* In the X Ray Image Query, users may optionally pass energy group bounds to the query, which will appear as part of the metadata in the Blueprint output types.
* In the X Ray Image Query, users may optionally pass the units for various input and output values through the query. These units will be propagated in the Blueprint output metadata.
* Added support to export PolyData with a single cell type to the Blueprint writer.
* The X Ray Image Query now outputs Blueprint meshes representing the rays used in the raytrace if the Blueprint output type is selected.
* The Blueprint output from the X Ray Image Query previously included coordinates for the spatial extents of the output image. These coordinates have been promoted to a valid blueprint mesh.
* Updated the Silo reader to support a rare decomposition format discovered in the wild.
* Added support for reading Blueprint data with blueprint_index per-mesh partition maps to the Blueprint reader.
* Extended support for reading sparsely populated Blueprint trees in the Blueprint reader.
* Enhanced the make movie script so that it sets the number of digits in the output file names based on the number needed rather than always using four when the number of frames in the movie is known ahead of time, which is when a session file or the current plot is used. Note that it uses a minimum of four digits to maintain backwards compatibility and a maximum of seven digits on the assumption you will not create a movie longer than 92 hours.
* Added initial support for reading Blueprint structured meshes with non-trivial strides to the Blueprint reader.
* The X Ray Image Query Documentation has been expanded. It now has its own [page](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/using_visit/Quantitative/XRayImageQuery.html), where all of the additions and features are extensively documented.
* Made some usability enhancements to the color table window; specifically, changed which color tables appear by default and removed some color tables that are superfluous.
