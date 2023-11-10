---
layout: page
title: "Release Notes for VisIt 3.4.0"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.4.0/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### General features added in version 3.4

* A number of changes have been made to the handling of color tables. These include:
    * Users can no longer edit, delete, or export built-in color tables. Users must create new color tables to edit, export, and delete them. Color tables are no longer saved when saving state.
    * Color table tags are now editable from the GUI. Tags can be added and removed from color tables at will. Built-in color tables cannot have tags that they come with removed.
    * Color table tag changes can now be saved to and loaded from config/session files.
    * Color table tags are now restricted to contain only alphanumeric characters plus spaces, dashes, equals, greater-than or less-than characters .
    * Color table tag filtering is no longer optional; it is always on. There is also a new button to select (and deselect) all of the tags.
    * Color table searching is no longer optional; it is always on. A dedicated search bar has been added.
    * The color table window has a new horizontal layout.
* It is now possible to keyframe operator attributes. When in keyframe mode, VisIt will interpolate the operator attributes between operator keyframes. Keyframing makes it possible to easily create sophisticated animations such as animating slice planes, iso surfaces and any operator attributes available. Two new functions have been added to the Python scripting interface to support operator keyframing. They are `DeleteOperatorKeyframe` and `MoveOperatorKeyframe`.
* A tutorial has been added for creating keyframe animations.
* The Wavefront OBJ Writer has been upgraded to optionally output mtllib and texture files.
* To address an inclusivity bug regarding use of <em>Master/Slave</em> terminology, the interfaces to **LibSim** and **IntegralCurve, Poincare, LimitCycle** and **LCS** operators were changed. `Master` is replaced with `Manager`, `Slave` is replaced with `Worker` and `MasterSlave` is replaced with `ManagerWorker`. Old behavior will continue to be supported through this release of VisIt but will be removed after this release. You will want to update any LibSim code, any python CLI code and any saved settings that may use the old interface.
* A number of key libraries used by VisIt have been upgraded.
    * OSPRay has been updated to version 3.0.0.
    * VTK has been upgraded to version 9.2.6.
    * Qt has been upgraded to version 6.4.2.
* Support has been added for installing ffmpeg as part of a VisIt installation.

### Changes in GUI behavior for in version 3.4

* Added `$<T>tafile<I>` [text annotation macros](//visit-sphinx-github-user-manual.readthedocs.io/en/develop/using_visit/MakingItPretty/Annotations.html?highlight=text%20annotation#named-database-values-in-text-annotations) to read each time step's annotation, line-by-line, from a text file.

### File format reader changes in version 3.4

* Added the ability to export [VTK HyperTreeGrid](//www.kitware.com/hypertreegrid-in-vtk-an-introduction/) files. HyperTreeGrids are uniform hierarchical meshes. When exporting HyperTreeGrids the following restrictions apply:
    * The mesh must be a 3 dimensional rectilinear mesh.
    * The mesh spacing must be uniform in each direction.
    * The mesh dimensions must be equal in each direction.
    * The mesh dimensions must be a power of 2.
    * The variable must be zone centered.
    Typically you would use the "Resample" operator to resample the variable to meet the restrictions above.
* Added the MFEM LOR setting to the MFEM Reader. Users may now choose between the new LOR scheme and the legacy LOR scheme. The new scheme is the default.
* VisIt's Blueprint reader has been enhanced so related high order volume fraction fields from a *matset* are grouped into a material that can be used with the FilledBoundary plot. The high order material data fields are refined through MFEM LOR, whose refinement level can be controlled with the *MultiresControl* operator.
* Removed the HDF 4 based readers, which include the Cosmos, RAGE, and ZeusMP readers.
* Removed the HDF 4 support in the Enzo reader.
* VisIt's Blueprint reader now supports materials with material numbers that do NOT fall in the range \[0, N\), where N is the number of materials.
* VisIt's Blueprint reader now detects high-order volume fractions fields following the naming pattern *volume_fraction_ZZZ* as a material.
* VisIt's Blueprint reader now limits the total number of open HDF5 file handles.

### Changes to VisIt's plots in version 3.4

* The volume plot was completely revamped for VTK-9 and OSPRay 3. Please see the [new docs](//visit-sphinx-github-user-manual.readthedocs.io/en/develop/using_visit/Plots/PlotTypes/VolumePlot.html) for more information.

### Changes to VisIt's expression language in version 3.4

* The *matvf* expression now works with high order materials so it returns refined LOR volume fractions when the *MultiresControl* operator is used.

### Changes to VisIt's picks and queries in version 3.4

* The X Ray Image Query now supports three different file naming "schemes". The default is "none", which will attempt to keep the filename as simple as possible. There is an option to "family" output files, which has nearly the same behavior as the old "family_files" option. The final option is to have "cycle" information in filenames. The "family_files" option has not been removed to preserve backwards compatibility. If both options are present, "filename_scheme" will be used instead.
* The filenaming conventions have been updated and standardized for the X Ray Image Query outputs.
* The BMP output type for the X Ray Image Query has been removed.
* The X Ray Image Query warns users if their camera setup is error-prone.
* The X Ray Image Query now allows users to specify a view width, which can cause pixels in the output to not be square.
* The X Ray Image Query now defaults to using its complete camera specification instead of its simplified camera specification. Both are still available.
* The X Ray Image Query now returns a Python Dictionary containing information about the files written using the query. This object is `None` if the query failed, making it easy to check if the query was successful or not.
* The CLI function `GetQueryOutputValue` now returns `None` when there is no return value. This typically happens when an error with the query occurs.

### Other bugs fixed in version 3.4

* A better error message was added for Revolved volume query when applied to meshes whose spatial dimension is not 2.
* Avert potential crash in mdserver matching file names for virtual database recognition.
* Fixed a bug where an error would incorrectly be detected when creating ghost zones. Specifically, it occurred when a block had mixed materials and the block didn't contain the material the variable was defined on.
* Fixed a bug reading particle data from Mili files. The particle data would not appear and could cause the engine to crash if the number of particles was larger than the number of elements.
* Fixed a bug where the pseudocolor plot would have NaNs in the legend if the mesh contained no elements or all the elements were ghost elements. Now it prints an error message with a description of the error.
* Fixed a bug where 'LaunchNowin' would fail on Windows when additional launch arguments were specified with `AddArgument`.
* Fixed a bug where the time scale and offset were not honored by the time slider annotation or `$time` annotation macro.
* Fixed a bug that caused VisIt's viewer to crash in rare occasions involving failed queries.
* Fixed an issue that caused VisIt to treat color tables created via the CLI as though they were built-in color tables.
* Fixed an issue that caused the "No Tags" tag to not appear in the tag table.
* The Color Table Attributes now no longer can set default continuous and/or default discrete color tables to not continuous and not discrete color tables, respectively, when a color table is removed.
* Fixed a bug with the python cli's `TurnOffMaterials()` method where it would give a poor error message when passing an integer instead of a string.
* The `GetLastError()` CLI method now accepts an optional integer argument indicating whether to clear out the last error message after retrieving it.
* For the Mili plugin, if a class is missing from a top level mili file, the plugin will now throw an exception explaining what happened instead of failing mysteriously.
* Fixed a bug where the Pseudocolor plot's legend would state 'Constant' when the data limits weren't constant.
* Improved the performance when working with large numbers of very complicated expressions.
* Fixed an issue where adding an item to the preferred plugin list in the plugin manager would add the wrong plugin.
* Fixed a bug where the Blueprint reader would fail to read polytopal meshes missing offsets.
* Our launcher now unsets the `QT_SCALE_FACTOR` environment variable, preventing graphical issues with Qt.

### Configuration changes in version 3.4

* A host profile has been added for running on Lawrence Livermore National Laboratory's RZWhippet system.
* A host profile has been added for running on Oak Ridge National Laboratory's Frontier system.
* A host profile has been added for running on NERSC's Perlmutter system.

### Build features added in version 3.4

* The Mili library was upgraded to version 23.02 from 22.1.
* The Uintah libary was upgraded to version 2.6.2 from 2.6.1.
* Removed HDF 4 support.
* Added support for building VisIt on NVIDIA Grace CPU and Arm Architecture.

### Changes for VisIt developers in version 3.4

* Support for boolArray and boolVector was added to the XML code generation tools.
* Updated the "Creating a Release" section of the developer manual to describe the current process.
* The Building with Spack section of the user manual was enhanced with instructions for building with the develpment version of spack. Specific instructions for building on Frontier and Perlmutter were also added.
* Add support for Qt6. The build_visit option is `--qt6`, which will build qt version 6.4.2, and also force building of VTK-9 if `--vtk` is also enabled.
* Added the ability to create tabbed content in the sphinx documentation by adding the sphinx-tabs extension.
* The released Windows version is now compiled with MSVC2022.
