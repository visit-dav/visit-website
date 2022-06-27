---
layout: page
title: "Release Notes for VisIt 3.3.0"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.3.0/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### General features added in version 3.3

* The handling of color tables has been enhanced and modified.
    * Many color tables from [Fabio Crameri](//www.fabiocrameri.ch/visualisation/) have been added for individuals who are color vision deficient (CVD).
    * To handle the expanded list of color tables a new tagging system has been introduced to allow users to reduce the color tables displayed in the color table controls in the rest of the GUI. All the tagging and filtering controls are located in the existing Color table window.
        * Every color table has one or more tags.
        * Color table filtering can be turned on or off.
        * When color table filtering is off all the color tables are displayed in the color table controls in the rest of the GUI.
        * When color table filtering is on only the color tables associated with the active flags are displayed.
        * The user can select if only the color tables that contain all the tags or any of the tags gets displayed.
    * The color table categroies have been eliminated since that functionality is now redundant with the introduction of the more flexible tagging system.
    * Changed *active* to *default* for everything related to color tables, including the GUI and the Python scripting interface.
* New capabilities have been added to allow repartitioning or flattening domain decomposed data when exporting to Blueprint.
    * When repartitioning data, the user can specify the number of domains to repartition the data into. The current repartitioning algoithm uses a simple spatial decomposition algorithm. The user can also specify a field to control the partitioning, enabling an arbitrary repartitioning.
    * When flattening the data, all the domains are merged into a single domain.
    * To export repartitioned data, go to the Blueprint export options, select the *Partition* operation and set the target number of domains field.
    * To export flattened data, go to the Blueprint export options, select *Flatten_CSV* to export the mesh data to vertex and element based CSV files, or *Flatten_HDF5* to export the data to a Blueprint *Table* node.
    * It is also possible to directly access flattened data from the Python scripting interface. The `Flatten` function uses the new Flatten Query to return the active plot data as a tabular, numpy compatible, 2D array.
* Support for *SeedMe* was removed since the service was retired.
* References to old email lists (@ornl.gov) throughout the code and documentation were replaced with references to the help pages of the new website.
* The behavior of Python's `help` was modified to first present what `help` would normally produce followed by the output from `apropos` when that output is non-empty.
* The French translation was updated thanks to [@cessenat](//github.com/cessenat). We are still looking for volunteers for translations in other languages. If interested, please [contact us](//visit-dav.github.io/visit-website/support/).
* A new (beta) [Castilian Spanish](//en.wikipedia.org/wiki/Names_given_to_the_Spanish_language) translation was created thanks to [@cessenat](//github.com/cessenat) using auto-translation from English. It likely still requires review by someone who is fluent in Spanish and we would welcome any volunteers.
* Added support and examples of 2D structured grids representing surfaces in 3 dimensions.

### Advanced features added in version 3.3

* Text annotation macros (e.g. `$time`, `$cycle`, ...) have been enhanced in some key ways. First, more macros are available including `$index`, `$dbcomment`, `$numstates`, etc.. Next, printf-style formatting can be specified for a macro and multiple instances of the same or different macros can appear in the same annotation object.
* Attribute assignment (e.g. `cylinderAtts.point1=...` or `cylinderAtts.SetPoint1(...)`) operations in the Python scripting interface were modified to catch and disallow incorrect usage instead of silently falling back to default values. Better error checks and messages were also added. It is possible these changes may cause code that worked fine to now terminate with a Python exception. In such cases, the resulting error message should explain the cause of the failure and the changes required to fix it should be obvious and minimal.
* A new function was added to the Python scripting interface named `apropos(regex)` similar in purpose to [Unix' apropos](https://en.wikipedia.org/wiki/Apropos_(Unix)). It makes finding the names of functions and objects much easier. It will return a list of the names of functions or objects where the regular expression matches either in the method name or in the documentation string for the method or in a stringified instance (objects only). All matching is case insensitive.
* `ColorControlPointsList` and `GaussianControlPointsList` now have a `SetNum` method for changing the size of the underlying controlPoints list. Control points will be added or removed based on the current size of the list. The `SetNum` method was also added to the script created by logging / command recording, so that the control points list has the correct size and the created script can execute correctly without crashing the Python scripting interface.
* A section was added to the *Developer Manual* describing process launching.
* A section was added to the *Developer Manual* describing building VisIt with spack.
* A tutorial on Python expressions was added to the tutorials section of the manual.

### Changes in GUI behavior for version 3.3

* In the file open window, next to *Open file as type:* when you click *Guess from file name/extension*, the list of file types is now sorted in alphabetical case-insensitive order. The same change has been made in the list of Databases in the Plugin Manager.
* In the plugin selection in the file open window, users can now delete the text that is there and start typing the name of the plugin that they wish to open files with, and VisIt will autocomplete the entered text to select a plugin.
* Custom titles for Legend annotation objects can now be set.
* *Dolly* and *FlyThrough* navigation modes now support mouse-wheel interaction for zooming.
* Changing the navigation mode (*Trackball*, *Dolly*, *FlyThrough*) will now trigger an automatic View reset.

### File format reader changes in version 3.3

* The informational message displayed after successfully exporting a database now contains the host and path to the file.
* The Chombo reader now supports anisotropic refinements.
* The WData reader was added.
* The Blueprint reader was enhanced to support the implicit points topology.
* The Xmdv reader was enhanced to allow users the ability to specify the output precision when exporting data.
* The Blueprint reader was enhanced to support polyhedral meshes. If you read a polyhedral mesh, it will automatically convert the mesh to a tetrahedral mesh, as well as convert the fields as needed. It will also keep track of original element ids so that you don't see the new lines from the resulting tetrahedra.
* The Xolotl reader was updated to support phase-space.
* The SW4 reader was renamed as sw4img to fix static builds.
* The NASTRAN reader was modified to reduce the amount of debug outputs and handle DOS line endings.
* The Blueprint reader now supports the option to choose between two different MFEM low order refinement schemes. The Legacy option is the original LOR scheme used by VisIt, and the new option preserves the continuity of meshes. The new option is enabled by default.
* VisIt-generated expressions are no longer included in VTK, Blueprint, and Silo exports.
* The ADIOS and ADIOS2 readers were updated to build with c-blosc, so blosc-compressed ADIOS-based files can now be read by VisIt.

### Changes to VisIt's plots in version 3.3

* Pseudocolor Plot Limits now say *Use Actual Data* instead of *Use Current Plot*.

### Changes to VisIt's expression language in version 3.3

* Added the *logical_nodeid*, *logical_zoneid*, *node_domain*, *zone_domain*, and *zone_centers* mesh expressions.
* Moved the *divergence*, *curl*, *Laplacian*, and *gradient* functions from the *Miscellaneous* submenu to the *Vector* submenu within the *Insert function...* menu in the Expressions window. 
* Added the new *ghost_zoneid* function to the *Mesh* submenu in the Expressions window.
* Added the new *crack_width* function to the *Misc* submenu in the Expressions window.

### Changes to VisIt's picks and queries in version 3.3

* Upgraded the *XRay Image* Query so it can now output Blueprint files.
* Upgraded the *XRay Image* Query so users can now specify an output directory for query results.
* The *Pick* operation now has the option to include the Euclidean distance between the current and previous *Pick* in the GUI's output window. To enable this option, check the *Distance to previous* box Pick output window. You should then see a new field in the tabular output display titled *Distance to previous*.

### Other bugs fixed in version 3.3

* Fixed a bug with expression insert-function for constant expressions, so that the usage is clearer. 
* Fixed a bug with the PlainText reader, where leading and trailing whitespace was included int the variable names.
* Fixed a bug with the time slider in the main window where it would resize to an extremely wide minimum width in some situations.
* Fixed an issue where the list of plugins in the File open window could disappear when selecting plugins from the list multiple times.
* Fixed a bug where changing the *Number format* for a Contour plot's legend would have no affect on the labels next to the tick marks.
* Fixed a bug that prevented users from comparing particular VisIt Python objects in the Python scripting interface with non-VisIt types.
* Fixed a crash with Libsim when attempting to Export databases that have export options specified as enums.
* Fixed a bug where right-clicking in the Viewer Window to access popup menu was preventing mouse-wheel navigation functionality until another mouse click was performed.
* Fixed several bugs with *Flythrough* navigation mode: multiple calls to *Reset View* would make the plot disappear; adding new plots would make them disappear from view; issuing a *Recenter View* would move the camera inside the plot.
* Fixed a bug where the bounding box extents would not be reset when *Scale 3D Axes* was turned off.
* Fixed a crash in the Python scripting interface when `DeleteAllPlots` is called when there are no plots and a callback has been registered for `SetActivePlots`.
* Fixed a bug in `visit_composite` where output formats like bmp, png could not be read back in by VisIt nor used to encode movies.
* Fixed a bug with the Python scripting interface where the PySide2 module wouldn't load when running one of the pre-built binaries.
* The Contour plot's fields were re-ordered internally to fix a bug where a command-recorded script of a Contour plot would crash the Python scripting interface if the number of contours had been increased from the default.
* The images and wording for *Curve Overlay* and *Reflected Curve Overlay* templates in the Save Movie Wizard were updated to demonstrate that they can be used on 3D plots, not just 2D plots.

### Configuration changes in version 3.3

* Added host profiles for the KAUST Supercomputing Laboratory.
* Updated the Ohio Supercomputing Center host profiles.
* Updated the ORNL host profiles to remove obsolete machines.
* Renamed the *mxterm* launch profiles to *sxterm* in the LLNL host profiles since *mxterm* has been replaced with *sxterm*."
* Updated the *TOSS3* installations at LLNL so that they would also run on *TOSS4* systems.
* Updated the LLNL host profiles for *TOSS* systems to use `sbatch` instead of `msub` when launching batch jobs.

### Build features added in version 3.3

* Build_visit was modified to do an out-of-source build for Qt.
* Enhanced build_visit to optionally build Qt 5.10.1 instead of Qt 5.14.2. To enable building Qt 5.10.1, add `--qt510` to the command line.
* Build_visit was enhanced to patch Xdmf so that it builds with gcc 11.2.
* The `--dry-run` command line option was removed from build_visit.

### Changes for VisIt developers in version 3.3

* VTK-m was updated to version 1.7.0 and VTK-h was updated to version 0.8.0.
* Added the spack environment files `compilers.yaml` and `packages.yaml` for crusher.olcf.ornl.gov.
* There is now a WIN32DEFINES xml tag for database plugins, used to specify preprocessor defines needed by a plugin on Windows. If the needed define comes from a thirdparty library, the Find module for that library should set a CMake var with those defines that the plugin could then use in the .xml file. See FindCGNS.cmake and CGNS.xml for an example.
* The minimum required version of CMake is now 3.14.
* The programs `qtviswinExample`, `qtvtkExample`, `qvtkopenglExample` were added to help with debugging OpenGL issues.
* VisIt test data archive tooling was changed from `7z` to `tar` with the same (lzma2) compression.
* The version of Conduit was upgraded to 0.8.2.
* VisIt now calculates the topological dimension of the data tree after the data was retrieved from the database, and after SIL and/or Material selection was applied. This should aid downstream filters that depend on an accurate topological dimension. For mixed-topology datasets the largest topological dimension is what gets reported. Filters that modify topological structure are still required to update the topological dimension.
* The `DEFINES`, `CXXFLAGS` and `LDFLAGS` tags in the xml files for plugins now support an optional `components` attribute specifying for which component(s) the tag applies. These are currently valid for the MDServer("M"), serial Engine ("ESer") and parallel Engine("EPar"). Multiple components may be specified, separated by commas. See `ADIOS2.xml` or `MOAB.xml` for an example.
* The DEFINES tag now supports surrounding definitions in quotes if the quotes are important to be carried through. They must be escaped with a '\'. See `uintah.xml` for an example.
* The version of MFEM was upgraded to 4.4.
* Added the script `run-build-visit` for running `build_visit` to build the third party libraries on LLNL systems. The script has the following usage:

    Usage: +"machine name" -v "version" -s "build_visit_script"
    Valid machine names:
        kickit_mesagl (B-Div, Linux, x86_64, mesagl),
        kickit_opengl (B-Div, Linux, x86_64, opengl),
        quartz (LC, Linux, x86_64),
        lassen (LC, Linux, power9),
        rztrona (LC, Linux, x86_64),
        rzansel (LC, Linux, power9),
        jade (LC, Linux, x86_64),
        sierra (LC, Linux, power9)

* Fixed a bug with the regression test suite where the image difference metrics were reported incorrectly in the HTML and JSON output.
* Added `TestAutoName()` method for automagically naming test baseline files.
* The signature for the `SET_UP_THIRD_PARTY` function for Find modules was modified to utilize keyword arguments:
    * **LIBS** (required) -- the list of libraries to be found
    * **LIBDIR** (optional) -- use when libs are located in an extension other than *lib64* or *lib*
    * **INCDIR** (optional) -- use when the headers are located in an extension other than *include*

    The first argument still must be the name of the package.
  
* The packaging was enhanced to add the `libicui18n`, `libicudata` and `libicuuc` system libraries used by Qt to the lib directory. This is done automaticallly if the libraries can be found in the `lib64` directory. The packaging logic was also enhanced to add the libstdc++ libraries to the lib directory of a distribution. The libstdc++ library depends on `VISIT_CXX_LIBRARY` being defined. This would typically be added to the config site file and would be set if using a non-standard compiler on a system. Both of these enhancements only apply to Linux systems.
* The version of Mili was upgraded to 22.1.
* VisIt now builds successfully with ADIOS enabled while MPI is disabled.
