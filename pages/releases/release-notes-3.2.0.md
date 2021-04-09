---
layout: page
title: "Release Notes for VisIt 3.2.0"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.2.0/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### General features added in version 3.2

* Updated VisIt to use Python 3.
* Added the command line option **-py2to3** to the CLI, which enables limited on-the-fly Python 2 to Python 3 conversion for scripts passed via **-s** or **visit.Source()**. See VisIt's CLI manual for more details.
* Upgraded VTKm to a recent version. Support was added for zone centered variables and 3D unstructured meshes with tetrahedra, pyramid and prism cells, in addition to the existing support for hexahedra.
* PySide has been re-enabled using a version matching Qt-5.14.2.
* The Windows package has been digitally signed, and should prevent or reduce Windows Defender and antivirus blocking/warnings.

### Advanced features added in version 3.2

* The -disable-ghosts-for-t-intersections flag has been reverted back to -enable-ghosts-for-t-intersections, and the creation of ghosts for t-intersections will now be off by default. This will improve performance for the default situation where ghost t-intersections are not needed or desired.

### Changes in GUI behavior for version 3.2

* Fixed a bug in the GUI windows where changes sometimes would not take effect when the Apply button was clicked.

### File format reader changes in version 3.2

* A reader was added to support AVS ucd file format.
* A reader was added to support the FMS file format.
* Enhanced the MFEM reader so that it provides the original cell numbers that allow VisIt to successfully eliminate mesh lines that were not part of the original high order mesh.
* Enabled the Rect reader as an optional reader on Windows.
* Enabled the ZipWrapper reader on Windows.
* Upgraded the CGNS library used by the CGNS reader from 3.2.1 to 4.1.2. The new CGNS library includes a fix for the handling of RIND zones in structured grids, so the results may change when viewing that type of data.
* Enhanced the Conduit Blueprint reader to support material volume fractions and mixed-variable fields using [Blueprint Matsets](https://llnl-conduit.readthedocs.io/en/latest/blueprint_mesh.html#material-sets).
* Enhanced the Conduit Blueprint reader to support datasets written to YAML root and data files.
* Enhanced the boxlib reader to always return double precision data.
* Enhanced the PlainText reader to return double precision data.
* Enhanced the UNV reader to read gmsh legacy files (thanks Olivier Cessenat).
* Fixed a bug with the Tecplot reader for handling cell-centered data (Thank you [Phil Chiu!](https://github.com/whophil)).
* Fixed a bug with the Boxlib reader reading double precision data.
* Fixed a bug with the Silo reader that resulted in VisIt crashing whenever negative material numbers were encountered. VisIt will now display an error message noting that negative material numbers are not supported.
* Fixed a bug in the Stimulate Image reader (file extensions spr, sdt), where a negative pixel delta in the metadata resulted in incorrect pick results, incorrect sampled lineouts and potentially other erroneous behavior.
* Enhanced the Xolotl reader to support the ability to visualize super clusters.
* Enhanced the CGNS reader to support reading arbitrary polygons and polyhedra.
* Fixed a bug with the BoxLib reader causing VisIt to crash when opening files on OSX.
* Enhanced the Mili reader to support setting the global integration point for element sets. This can be accomplished by changing the default open options for Mili within the Plugin Manager. Available options are "Inner", "Middle", and "Outer".
* Enhanced the Mili reader to derive variables from stress and strain. If strain does not exist in the dataset, the plugin will derive four different versions of strain from the mesh.

### Changes to VisIt's plots in version 3.2

* Fixed a bug in the Histogram Plot where *Use Current Plot* will now use the actual data extents.

### Changes to VisIt's operators in version 3.2

* The Stagger operator is no longer enabled by default.
* Enhanced the Clip operator to support "Crinkle" clipping, which retains whole cells that intersect with the clip boundary.
* Threshold operations can now use the VTKm backend for structured meshes.
* Updated the documentation for the Smooth Operator.

### Other bugs fixed in version 3.2

* The checkbox in the Expression window that turns on the display of expressions from the database now indicates that it displays expressions from the database and auto generated ones.
* Fixed an issue preventing build_visit from being able to build IceT.
* When using the resample operator in VisIt's python interface, `useExtents` will now take precedence over setting the resample dimensions explicitly, which matches the behavior in the GUI.
* Fixed a bug with DataBinning (and DDFs) where it did not exclude Ghost Zones when binning.
* Fixed a bug preventing the Min/Max expressions from working with domain decomposed datasets.
* Fixed a bug that caused some LibSim examples to crash.

### Configuration changes in version 3.2

* Added host profiles for the Lawrence Livermore National Laboratory's Ruby system. Removed the host profiles for the Lawrence Livermore National Laboratory's Zin system.
* Added a host profile for the pdebug queue for the Lawrence Livermore National Laboratory's Magma system.
* Updated the job launching on Trinity so that the VisIt CLI could be launched from a batch job without having to load the module of the compiler used to build VisIt.
* Updated the Oak Ridge National Laboratory's host profiles to only include current machines.

### Build features added in version 3.2

* For build_visit, there is now only one way to specify a debug build: --build-mode "Debug". The --debug flag was removed. The default build-mode is "Release". If "Debug" is specified, all third-party libraries are built in debug mode. If the intention is only to build VisIt in debug mode, it should be compiled separately after all the third-party libraries are compiled, passing -DCMAKE_BUILD_TYPE:STRING=Debug to cmake when configuring VisIt.
* Removed FastBit and FastQuery from VisIt.
* Fixed a bug with build_visit building IceT with MPICH.
* Fixed a bug with build_visit building IceT on a system without OpenGL installed.

### Changes for VisIt developers in version 3.2

* Added support for link checking in Sphinx documentation.
* Added the ability to pass diff tolerances in Test()/TestText() testing methods in the test suite.
* Updated the developer documentation on fuzzy matching and thresholds for testing.
* Added support for `pdb` as a mode string for testing.
* Removed the emptydomain cases from skip list for the test suite.
* Added new assertion tests to ensure tests are running in the mode specified by the -m/--mode= command-line argument.
* Updated the version of Qt to 5.14.2.
* Replaced AssertXXXX() style test checks with TestValueXX, which supports more features, in the test suite.
* Enhanced build_visit so that the version on the develop branch will now look for tar files in the github master branch of visit-dav/thirdparty if all other avenues fail.
* Updated the version of LLVM version to 6.0.1 and added libclang to the build.
* Updated the version of Mesa/OSMesa to 17.3.9.
* Updated masonry to use Python 3.
* Fixed textual differencing in regression testing for Windows OS.
* Created a NotarizeAction in the masonry scripts so that notarization can be executed in the correct order with the rest of the actions.
