---
layout: page
title: "Release Notes for VisIt 3.3.3"
header:
  image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.3.3/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.3.3

* Fixed a bug in the Exodus reader where it would display an erroneous error message when the array with the simulation times had zero length.
* Fixed a bug with Swivel focus where it didn't properly center the picked point in the window when the image was panned.
* Fixed a bug with Swivel focus where the view in locked windows didn't get updated.
* Fixed a bug with the Pseudocolor, Vector and Tensor plots where the limits displayed at the bottom of the color bar displayed the original data limits even when "Use Actual Data" was specified for the "Limits".
* Fixed blank viewer window on first plot on macOS by resetting layout briefly on first plot.

### Enhancements in version 3.3.3

* Added domain variable ordering to the metadata that comes out of the X Ray Image Query Conduit outputs.
* Changed the metadata coming out of the X Ray Image Query Conduit outputs to use pot_hole_case as opposed to camelCase.
* Built and installed an x86_64 toss4 version of VisIt on the LLNL systems.
* Added support for plot boundary topologies and boundary attribute fields to the MFEM Plugin.
* Added support to directly open ".mesh" files with MFEM Plugin.
* Updated the VTKm library from version 1.7.0 to 1.9.0 to add support for AMD GPUs.
* Added original cell id support for MFEM Meshes in the Blueprint Plugin. With this change the Mesh plot will now plot outlines of high order elements, instead of the elements of the low order refined mesh.
* The X Ray Image Query now includes two new topologies (and associated fields) when using a Conduit Blueprint output type, the Spatial Energy Reduced Mesh and the Spectra Mesh.
* Added support to read RZ (2D cylindrical) meshes to the Blueprint Plugin.
* Added support to handle 1D meshes as curves to the Blueprint Plugin.
