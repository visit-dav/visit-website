---
layout: page
title: "Release Notes for VisIt 3.4.1"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.4.1/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.4.1

* Fixed a bug in the Wavefront OBJ Writer that would result in incorrect coloring for minimum or maximum values in downstream tools such as PowerPoint.
*  Fixed a bug with Pick unable to return results for 2D datasets.
*  Fixed a bug where vtk error messages were printed to the terminal when adding an Image Annotation Object to the viewer window.
*  Changed default logic for guessing cycles from file names to not consider any digits in the file name extension if present. This fixed the guessing logic for cases where a file extension includes a digit (e.g. <code>.h5m</code>)
*  Fixed a bug where glyphed line endpoints could be colored incorrectly in the Pseudocolor plot.
*  Fixed a VTK Texture Buffer error that caused error messages to be printed to the command line.
*  Fixed a Mesh plot bug where transparency would not be honored.
*  Fixed compile error where some executable targets were missing QSurfaceFormat include.
*  Fixed a Volume plot but that would cause the parallel engine to crash when certain operators were used in conjunction with the plot.
*  Fixed a Cube reader bug that didn't read in multiple orbital data files correctly.
*  Fixed a bug with the Expression window that caused the 'Python' editor to be the default tab when the window was first opened.
*  Fixed a bug with the Cartographic Projection operator where the projections were a no-op.
*  Removed custom logic forcing the opacity slider to snap to zero if the mouse dragged the slider outside the widget it belongs to.
*  Fixed a bug in the Blueprint reader causing unstructured point topologies to display incorrectly if they did not use all of the provided coordinates.
*  Removed sxterm host profile options for LLNL LSF Machines. sxterm is not available on these systems.
*  Several bugs were fixed in UNV plugin including fixing normals for quads.
*  Fixed a problem with global node ids on point meshes from Silo plugin.
*  Fixed a bug in the Wavefront OBJ Writer that caused zonal variables saved out using the writer to have some incorrect colors in downstream tools such as PowerPoint.
*  Fixed srun launch issues on LLNL TOSS4 systems.


### Enhancements in version 3.4.1

* Added the ability to invert the color table for the Wavefront OBJ writer.
* Upgraded MFEM library version to 4.6.0.
* The <i>surface_normal</i> expression now accepts mesh types other than polydata, allowing it to be used more easily as an operator-created variable.
* Added more keywords ("MFA", "2fa", "Autentication", and "OTP") that cause VisIt clients to open a second popup for a password.
* Updated the ADIOS2 library version to 2.10.0-rc1, allowing BP5 files to be read by VisIt.
* Removed the dependency on C-Blosc1.
* Added a new dependency on C-Blosc2.
* VisIt's Blueprint reader was enhanced so fields in Blueprint index files can supply a <i>display_name</i> hint that specifies the name used to expose the field in VisIt. This feature enables the index file to group related variables under sub-menus if the names in include slash characters.
* VisIt's Blueprint reader was enhanced so fields that are low-order but are associated with a high-order mesh can be refined when the mesh is refined, as when the user applies a <i>MultiresControl</i> operator. This enables VisIt to correctly view such fields.
* VisIt's CLI has a new <i>GetLastMessage()</i> function that returns the last message that VisIt issued, regardless of its type.
* GetPlotInformation() can now contain entries for multiple-curves when Query-over-time is performed on multiple variables. For example, if a pick-through-time was performed for variables 'u' and 'v', the curve for 'v' would be retrieved via 'GetPlotInformation()['Curves']['v']. Single variable results will still be retrieved via 'GetPlotInformation()['Curve'].
* The ADIOS2 database plugin learned a new flavor of file type: Pixie3D.
* A number of improvements were made to the UNV plugin including quadric elements, support for antique SDRC/I-Deas files prior to Master Series (versions 4,5 and 6), GMSH hidden polygon linear element.
* The Docker files for Debian 10,11,12, Fedora 31, Ubuntu 18, 20,22 have all been updated for this release. All but Ubuntu 18 build Qt 6.
* Updated LLNL host profiles for new systems
* Ported VisIt to LANL's Crossroads (XR) System
* Refactored VisIt's CMake Python logic to use pip instead of distutils.
* Updated VisIt to use Python 3.9.

### Third-party Libraries used for version 3.4.1

| adios2-2.10.0-rc1 |
| adios-1.13.1 |
| AdvIO-1.2 |
| c-blosc2-2.11.3 |
| boost_1_67_0 |
| ccse-1.3.5 |
| cfe-6.0.1.src |
| llvm-6.0.1.src |
| cfitsio3006 |
| CGNS-4.1.0 |
| cmake-3.24.3 |
| conduit-v0.9.1 |
| embree-3.2.0.x86_64.macosx |
| FMS-0.2 |
| gdal-2.2.4 |
| glu-9.0.0 |
| H5Part-1.6.6 |
| hdf5-1.8.14 |
| icet-master-77c708f9090236b576669b74c53e9f105eedbd7e |
| ilmbase-2.2.0 |
| ispc-v1.9.2-osx |
| mdsplus-5.0 |
| mesa-17.3.9 |
| mfem-4.6 |
| mili-23.02 |
| moab-5.5.0 |
| mpich-3.3.1 |
| nektar-5.0.0 |
| netcdf-4.1.1 |
| openexr-2.2.0 |
| mesa-17.3.9 |
| ospray-3.0.0 |
| PIDX-0.9.3 |
| **Qt6** |
| qtbase-everywhere-src-6.4.2 |
| qtsvg-everywhere-src-6.4.2 |
| qttools-everywhere-src-6.4.2 |
| qwt-git-d3706f6e7f0351d278be2d989a4caaf92b399bbd |
| **-** |
| **Qt5** |
| qt-everywhere-src-5.14.2 |
| qwt-6.1.2.tar.bz2 |
| **-** |
| silo-4.10.2 |
| stripack-ACM.RJRenka.Sep97 |
| szip-2.1 |
| tbb2018_20171205oss_mac |
| Uintah-2.6.2 |
| VTK-9.2.6 |
| vtk-m-v1.9.0 |
| Xdmf-2.1.1 |
| zlib-1.2.13 |
| **Python** |
| Python-3.9.18 |
| alabaster-0.7.13 |
| Babel-2.12.1 |
| calver-2022.6.26 |
| certifi-2023.5.7 |
| charset-normalizer-3.2.0 |
| Cython-3.0.0 |
| docutils-0.18.1 |
| editables-0.5 |
| flit_core-3.9.0 |
| hatchling-1.18.0 |
| idna-3.4 |
| imagesize-1.4.1 |
| importlib_metadata-6.8.0 |
| Jinja2-3.1.2 |
| MarkupSafe-2.1.3 |
| mpi4py-3.1.4 |
| numpy-1.25.1 |
| packaging-23.1 |
| pathspec-0.11.2 |
| Pillow-10.0.0 |
| pluggy-1.2.0 |
| Pygments-2.15.1 |
| pyside-setup-5.14.2 |
| requests-2.31.0 |
| setuptools-68.0.0 |
| snowballstemmer-2.2.0 |
| sphinxcontrib-applehelp-1.0.4 |
| sphinxcontrib-devhelp-1.0.2 |
| sphinxcontrib-htmlhelp-2.0.1 |
| sphinxcontrib-jquery-4.1 |
| sphinxcontrib-jsmath-1.0.1 |
| sphinxcontrib-qthelp-1.0.3 |
| sphinxcontrib-serializinghtml-1.1.5 |
| Sphinx-7.0.1 |
| sphinx_rtd_theme-1.2.2 |
| sphinx-tabs-3.4.1 |
| tomli-2.0.1 |
| toml-0.10.2 |
| trove-classifiers-2023.8.7 |
| urllib3-2.0.3 |
| wheel-0.41.1 |
| zipp-3.16.2 |
