---
layout: page
title: "Release Notes for VisIt 3.1.3"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.1.3/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.1.3

* Fixed a bug preventing SaveWindow from saving OSPRay rendered images.
* Fixed a bug with the Pixie reader when it read 3D curvilinear meshes in parallel.
* Fixed a bug where the parallel engine crashed when creating ghost zones from global ids.
* Fixed a bug with the progress dialog staying visible when a client connection fails.
* Added a menu indicator icon to the Color Table buttons so that it is more obvious that the button can be pushed to see available options.
* Fixed a bug preventing the user from being able to performa a Pick Through Time using mesh quality metrics.
* Fixed a couple of bugs with the MutilCurve plot. Fixed a bug where portions of the axes were missing or incomplete after switching the orientation. Fixed a bug where there were no tickmarks when displaying 16 curves.
* Fixed a bug in the ColorTable window that limited the number of color control points to 200.
* Added Philip Blakely's code to fix the memory leak in the Lines Database.
* Fixed a bug in the ColorTable window that prevented colors on 'equal' control points from being changed.
* Modified the GUI so that duplicate expressions are now handled gracefully with an automatic name change.
* Fixed a bug preventing VisIt from correctly reading some types of files on Ubuntu when using non-English language settings.
* Adding and deleting expressions in the expressions window now only takes effect when actually clicking the apply button.
* Fixed a bug with the CGNS reader that caused VisIt to crash when doing a Subset plot of "zones" when reading data decomposed across multiple CGNS files.
* Fixed a bug preventing some multi-processor mili datasets from being properly read.
* Fixed a bug preventing database readers from being able to plot variables of the form "variable_name(subname)".
* Fixed a bug that caused the Mili database reader to add duplicate materials.
* Fixed a bug which caused external surfaces to be lost in the pseudocolor plot when using a gradient expression on a Curvilinear mesh (Structured Grid).
* Changed the vertical scroll bar mode for the plot list to <b>ScrollPerPixel</b> and to use a single step so that the bottom of the plot list is not cutoff.
* Fixed a bug preventing VisIt from displaying the manuals when using an out-of-source build.
* Fixed a bug where the Plots Add menu would become disabled after drawing plots via the CLI, then calling OpenGUI() and deleting a plot.

### Enhancements in version 3.1.3

* Increased the number of curves allowed by the MultiCurve plot from 16 to 20.
* The Revolve operator was enhanced to be capable of revolving points/particles.
* The Mili library was updated to version 19.2.
* The Lineout operator documentation was improved in the GUI manual to describe in detail how the sampling and interpolation is performed.
* Added the ability to generate ghost nodes for datasets that consist of collections of structured grids by matching the coordinates of the nodes on the exterior of individual structured grids. The coordinates must match exactly for them to be matched. Ghost nodes allow internal faces to be eliminated from Mesh, Filled Boundary, Pseudocolor and Subset plots. This improves rendering performance by reducing the amount of geometry to render. It also improves image quality for images rendered with transparency since it eliminates geometry that you are most likely not interested in seeing.
* Updated the host profiles for the Sandia National Laboratories computer systems, adding host profiles for new systems and removing ones for obsolete systems.
* Added support for the FILETYPE keyword to the Tecplot reader. The FULL type is the only type supported. If the FILETYPE keyword is specified and the type isn't FULL, an error is generated.
* Modified the startup script to unsetenv LD_PRELOAD to protect against users setting it for the GL library, which would break rendering.
* The Mili database reader was enhanced to create node displacements as derived variables when needed.
* Added the SW4 reader and deleted the WPPImage reader.
* Added the Tessellate operator, which tessellates high order elements into linear elements. The following high order cell types are supported: QUADRATIC_EDGE, CUBIC_LINE, LAGRANGE_TRIANGLE, QUADRATIC_TRIANGLE, BIQUADRATIC_TRIANGLE, LAGRANGE_QUADRILATERAL, BIQUADRATIC_QUAD, QUADRATIC_QUAD, LAGRANGE_TETRAHEDRON, QUATRADIC_TETRA, LAGRANGE_HEXAHEDRON and QUADRATIC_HEXAHEDRON. All unsupported types will be removed from the mesh.
* Added parallel support for Remap operator.
* Added host profiles for the Lawrence Livermore National Laboratory's Tron system. Removed the host profiles for the Lawrence Livermore National Laboratory's Cmax system.
* Enhanced the VisIt Help menu such that the VisIt Manuals are opened in the user's default web browser instead of being rendered in the GUI window.

### Changes for VisIt developers in version 3.1.3

* The build_visit script was enhanced to allow VisIt to build on Ubuntu 20.
* The build_visit script was enhanced to allow VisIt to build on Redhat Enterprise Linux 8.
* The build_visit script was enhanced to allow VisIt to build on Fedora Core 31.
* Updated masonry to optionally allow specify options to the codesign command.

### Documentation changes in version 3.1.3

* Updated sphinx docs for 3D view.