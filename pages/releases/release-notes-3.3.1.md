---
layout: page
title: "Release Notes for VisIt 3.3.1"
header:
  image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.3.1/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.3.1

* Fixed a bug with the color table window where the list of color tables could be populated even when no tags were selected.
* Fixed a discrepancy with the x ray image query where, if Blueprint output was requested, the result message from the query would display differently than the other output types.
* Fixed a bug with the color table window searching feature where the name text box could no longer be properly edited.
* Fixed a rare bug in the color table where if tagging was enabled, certain tags were turned on, and searching was enabled, a crash could occur.
* Fixed a bug with the x ray image query, where a crash would occur if the specified output directory was too long.
* Fixed an issue with the Tag Bar in the Manager portion of the color table window that caused it to display incorrect information while using the search feature.
* The color table buttons now correctly preserve their value if the selected table has been filtered out of the list of color tables.
* Resolved a rare issue with the default color table buttons that caused them to occasionally select a different color table if tagging and searching were enabled at the same time.
* Fixed a bug where the default continuous and default discrete color table buttons no longer reflected accurate information when large numbers of color tables were deleted.
* Fixed a bug where if a user deleted the final continuous/discrete color table in a filtering selection, the default continuous/discrete button did not update to a fall-back color table.
* Fixed an issue where the default continuous and discrete color table buttons had a different idea of what the default color tables were than other parts of VisIt.
* Added a guard so that it is impossible to delete the last continuous or last discrete color table.
* Fixed a bug where it was possible to select a color table that was not in the tag-filtered list of color tables.
* Fixed a crash caused by deleting a color table that was not in the filtered list of color tables.
* Fixed a crash caused by clicking the delete button when no more color tables were in the filtered list.
* Fixed an issue with the x ray image query that caused rays to sometimes be cast incorrectly when specifying non-square output.
* Added a patch for the Mili reader that increases the maximum path length for input files from 300 to 4096 characters.
* The widget for displaying Blueprint export options was improved to use a fixed-width font and ensure newlines are preserved.
* The Mili reader now correctly computes displacements from the initial coordinates (via `mc_load_nodes()` from the Mili A file). Previously, it was computing displacements relative to the nodal positions (`nodpos` variable) at the initial timestep.
* Pick now correctly takes into account the node origin.

### Enhancements in version 3.3.1

* The x ray image query now supports file familying for Blueprint output.
* In the color table window, the popup menu accessed via clicking on the default continuous color table button now correctly only displays continuous color tables, and the popup menu accessed from clicking on the default discrete color table button now correctly only displays discrete color tables.
* Added a color table searching feature to help users more easily find the color tables they wish to use.
* Added support for MFEM Low Order Refinement of piece-wise constant (L2) basis functions.
* The x ray image query now outputs result messages in the case of failure while running in batch mode.
* The Nsight systems cli is now available to profile a VisIt component (viewer, gui, etc).
* The Tag Bar in the Manager portion of the Color Table Window is now always visible, instead of only being visible when tag filtering was enabled.
* Color Table Tags are now deleted once no more color tables are associated with them.
* There is no longer a limit on the number of color table tags VisIt supports.
* The Mili reader now provides the volumetric strain and relative volume derived variables.
* The x ray image query now outputs spatial extents metadata (the physical dimensions of the image).

### Changes for VisIt developers in version 3.3.1

* Added a patch to build_visit so that the Mili library will build on Debian 11 systems using gcc 10.2.
* Enhanced the cmake packaging logic that adds the `libicui18n`, `libicudata` and `libicuuc` system libraries used by Qt to the lib directory to look in additional directories for the libraries to work on a broader set of operating systems.
* Fixed a bug with `FindVTKh.cmake` where it wouldn't install the shared libraries when VTK-h was built with `spack`.
* Fixed build errors where avtqueries need `-lrt` on Linux, and visitpy needed thread libs.
* Removed `--hdf4` as an option from build_visit.
* Fixed VisIt's find module for Nektar++ so that it will correctly find the 5.0.0 version built by build_visit.
* Added a patch to build_visit so that Qt 5.14.2 will build on Arch Linux systems using gcc 12.2.
* Refactored the Blueprint and MFEM readers such that Blueprint to/from VTK, MFEM to/from VTK, and Blueprint to/from MFEM transformations are now widely available in the new avtBlueprint and avtMFEM libraries.
* Updated build_visit to build Conduit 0.8.4.
