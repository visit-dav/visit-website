---
layout: page
title: "Release Notes for VisIt 3.2.1"
header:
  image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.2.1/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.2.1

* Fixed a bug that resulted in incorrect plots of mesh_quality/min_side_volume and mesh_quality/max_side_volume.
* Fixed a few issues running build_visit with `--static`.
* Fixed a bug with the CreateBonds operator window displaying %.1 in Bonds list Max field instead of correct value.
* Fixed a bug where the splash screen in some binary distributions would display "Unknown" for the git version instead of the actual git version.
* Fixed a bug with the Xdmf Reader not reading TIME_LIST for temporal data collections.
* Fixed a bug with the Mili reader where some of the material colors in a filled boundary plot would be black. The Mili reader would assign random colors to materials when no material colors were specified in the file, which resulted in some materials being black. Now the reader doesn't specify any colors in that case so that the material colors are chosen using the filled boundary plot's default color selection algorithm.
* Fixed a bug with the DataBinning operator window where the Dimension 2 variable would be disabled for 3D.
* Fixed a bug with ghost zone generation that caused VisIt to not display any data when displaying data from a parallel Exodus file when subsetting based on ElementBlock.
* Fixed a bug with full frame mode that resulted in the labels from the label plot not being drawn correctly.
* Fixed a bug launching the CLI when specifying `-v 3.2` when the default version in that installation was still an older version of VisIt (e.g. 3.1.4).
* Fixed a crash with the Molecule plot when drawn with Sphere Imposters for atoms and either the 'scaleRadiusBy' or 'radiusScaleFactor' options are changed.
* Fixed a bug in the Molecule plot where created bonds colored by atom were being colored incorrectly.
* Fixed a crash in the CLI when attempting to 'print' a legend annotation object.
* Fixed a bug with the Legend annotation object window where the *Values* column in the *Values/Labels* table in the *Tick marks* tab wasn't being prefilled.
* Fixed a bug for Windows where importing VisIt into python failed due to an inability to retrieve necessary enviroment variable information.
* Fixed a bug that resulted in the rubber band zoom box being rendered incorrectly on Mac retina displays.
* Fixed a bug for Windows where exporting a multi-block Silo file into a non-default directory would make the file unreadable by VisIt.

### Enhancements in version 3.2.1

* Added a section on developing at GitHub to the developers manual.
* Datasets that contain AMR meshes are now treated as time varying by default. This will guard against issues that arise with time varying AMR meshes that aren't explicitly tagged as time varying within the datasets.
* Added support for reading Rind values for structured grids from CGNS files to provide ghost zone information. To enable the reading of Rind values you must set the environment variable CGNS_USE_RIND (i.e. "setenv CGNS_USE_RIND").
* When exporting a database on a remote machine, the window will now display the host name next to the Directory name text field.

### Changes for VisIt developers in version 3.2.1

* When viewing test results in a web browser, the text tests will now correctly display leading spaces.
* The build_visit python module was changed so that when `--system-python` or `--alt-python3-dir` is specified, python3 is searched for first.
* Removed tcmalloc from VisIt.
* Fixed problems building Mesa and VTK (with python wrappers) with gcc 10.
* Fixed a bug in build_visit where specifying `--no-sphinx` resulted in the failure of being able to build VisIt.
* Fixed a bug in build_visit that caused it to improperly set the architecture directory name when using gcc 10.2. For example, on a linux system with an x86_64 processor, it previously set it to *linux-x86_64_gcc* instead of the correct *linux-x86_64_gcc-10.2*.
* Fixed a bug in build_visit that prevented CGNS from building on Linux systems.
