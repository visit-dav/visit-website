---
layout: page
title: "Release Notes for VisIt 3.4.2"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.4.2/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.4.2

* Fixed bug where user supplied legend labels were stored in config and session files wrapped in '()' and comma separated. This prevented the values from being parsed correctly and the '()' and commas appeared as part of the labels.
* Fixed a bug in the Blueprint reader causing it to handle unstructured topologies built on uniform coordinate sets incorrectly.
* The location where custom plugins are written when built against installed version of VisIt was corrected.
* Windows build issues for custom plugins against an installed version of VisIt was fixed.
* Fixed a bug in OpenPMD reader that subverted its ability to read chunked, as opposed to contiguous datasets.
* Enabled "Tunnel data connections through SSH" in the LLNL RZ host profiles where it was missing.
* Removed the obsolete LLNL host profiles for RZTopaz, Pascal, Surface and Vulcan.
* Fixed a bug where the LLNL host profiles for Boraxo, Dane and Ruby didn't get installed in some situations.
* Fixed a bug with rendering transparent surfaces with scalable rendering resulting in images with black horizontal bars or missing surface fragments.
* Fixed issues with build_visit when using gcc-13 and when Qt6 is present on the system.
* Fixed bug with Volume plot when SILRestriction applied, and when Composite rendering caused problem when a different RendererType used directly afterwards.
* The Blueprint writer no longer writes the wrong path to root files when specifying a directory to export files to.
* The Blueprint writer now correctly puts the right cycle number in file names.
* Fixed a bug in zonetype-label expression where unknown zone types would render a weird symbol, `&quot;?`.
* Disabled warning message regarding skipping of speculative expression generation for databases with many variables. For more information, read our documentation about [automatic expressions](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/using_visit/Quantitative/Expressions.html#automatic-expressions)
* Forced VTK file exports to use VTK data file format 4.2 instead of the new, not backwards compatible 5.1.
* Fixed a bug where the opaque geometry in an image containing both opaque and transparent geometry wouldn't be rendered poperly when rendered using scalable rendering.
* Fixed a bug where saving an image with transparent geometry would hang when using scalable rendering.
* Fixed a bug where perspective mode set to `off` in config files would not be restored correctly.
* Fixed an issue in the Mili plugin where requesting OriginalZoneLabels and OriginalNodeLabels did not work as intended.
* Fixed a bug in the Blueprint reader so it will use <i>elements/offsets</i>  for unstructured topologies, when present.
* Fixed a bug with transparent rendering where the transparent portions of the image were rendered with a white cast when in scalable rendering mode and all the geometry was on the first processor.
* Fixed a bug with point glyphing where points would be 'lost' and other miscolored if poly-vertex cells were present in the dataset.
* Fixed bug where hdf5_hl library wouldn't always be installed with VisIt.
* Fixed bug with Pseudocolor plots of datasets with very large or small extents being rendered black.
* ChooseCenter with a mouse on Scatter plot now works.
* The triad lines no longer disappear.
* Fixed an issue causing species set selection to only work on fields that were represented as floating point data.
* Fixed a bug in the Plaintext Reader causing reading variable names that were single-characters to fail.
* Fixed a bug where the operator attribute windows will show the default attributes when displaying the attributes for an operator applied to a plot after restoring a session. The plots displayed in the visualization windows will be correct, just the attributes displayed in the attribute window will be incorrect. This happens with session files saved with releases 3.4 and 3.4.1. To fix the issue you will need to save a new session file using a newer version of VisIt. If you restored a session with a bad session file, you will need to change the attributes of any affected operators before saving the new session file.
* Fixed a bug where the rubber band lines are either broken or missing when you click and move the mouse when zooming an image using zoom mode on Linux systems.
* Fixed a bug causing material edge lines to appear on Mili problems produced by parallel runs.
* Fixed a bug where trackpad on macOS laptops would get "sticky" never ending/releasing a rotation gesture.
* Fixed an issue causing L2 MFEM meshes stored as Conduit Blueprint data to render incorrectly when new Low-Order-Refinement was enabled.
* Fixed time slider annotation handling of printf-style format string.
* Fixed an issue with the displace operator where it would not accept vector mesh variables defined as expressions if the expressions had not been used in a plot already.
* Fixed an issue where the GUI panel's timeslider would display incorrect numerical values for cycle.
* Fixed a longstanding issue with Ghost Zone communication in parallel.

### Enhancements in version 3.4.2

* Qt6 is now the default version of Qt that is built with VisIt.
* The color table button (available in plot/operator windows), has a new option 'More Color Tables ...' which will open the Color Table Windows to easier find more options.
* A host profile has been added for running on LLNL's RZVernal system.
* The Blueprint reader and writer now supports mixed element topologies.
* The `VISIT_VERSION_GE()` macro useful in detecting the VisIt version being used at compile time has been made public in its own header file, `visit-version.h`, which is found in `VISIT_INSTALL/include/visit/include`.
* The Blueprint writer lets users specify Blueprint write options.
* The expression system now supports the `%` binary modulo operator. The `mod()` expression function is still supported but has been generalized to use the `fmod()` function from the C/C++ math library as does the new `%` binary operator.
* Host profiles for KAUST have been updated.
* The function `GetDefaultFileOpenOptions` in the Python scripting interface was enhanced to open a metadata server if one wasn't already open.
* The function `GetExportOptions` in the Python scripting interface was enhanced to open a metadata server if one wasn't already open.
* Re-enabled support for using VTKm, which was removed in the 3.4.0 release.
* Added species set support to the Blueprint Reader.
* Saving results of time queries to curve files now uses query name and/or variable names as curve names instead of just 'Curve'.
* Curves are now supported in Xdmf files. They are handled as 2DRectMesh objects with >1 points in X and 1 point in Y.
* The Silo plugin properly removes periodic boundary domain neighbors which can wholly enshroud a mesh rendering it invisible. This capability is restricted to rectangular arrangements of rectangular domains using the combination of a DBmultimeshadj object and auxiliary data structures to identify periodic domain neighbors.
* The OnionPeel and IndexSelect operator Windows now allow typing into the 'Set' option as well as selecting from the dropwdown box. Typing will filter the available entries to match what has been typed so far, allowing easier selection than the pulldown if there is a large number of sets. If typing is completed with text that doesn't match an available entry a Warning message will pop up.<li>
* Support has been added for using the `jsrun` parallel job launcher.
* Added the ability to skip the remote host validity check when using a gateway. This allows VisIt to work with gateways that are transparently handled by `ssh`. The check can now be bypassed by checking "Use gateway" and leaving the gateway name blank in the host profile for the remote system.
* Added support for MFEM Wedge (aka Prism) Meshes.
* Added new global mesh expressions: global_avg(), global_max(), global_min(), global_rms(), global_std_dev(), global_sum(), and global_variance(). These are expressions that calculate statistics across the mesh and the result is a constant variable that contains the result. So, global_max(d) produces a new variable that is the maximum of d at every zone or node across the mesh.
* The maximum image size that can be saved has been increased to a maximum of 32,768 for either the width or height with a total pixel count not to exceed 536,756,224 pixels. For a square image that corresponds to an image size of 23,170 by 23,168 or less. For a rectangular image that corresponds to an image size of 32,768 by 16,380 or less.
* Added host profiles for Crossroads.


### Changes for VisIt developers in version 3.4.2

* Updated Conduit to 0.9.2.
* Docker containers were added for RockyLinux (RHEL compatible).
* Qwt is now optional, but built by default. If you encounter issues with Qwt when running build_visit, add `--no-qwt` to the build_visit command line to disable Qwt. Historically, it has only ever been needed for advanced GUI features of LibSimV2 interface. Add `--system-qwt` to have VisIt attempt to find and use a system version of Qwt.  Add `--alt-qwt-dir /path/to/qwt/install` to use a pre-built version of Qwt installed somewhere else.
* Added ICE-T support for Windows builds.
* Fixed bug where printing the build_visit log file location prepended extra paths.
* Fixed glitch that prevented VISIT_CXX_FLAGS defined in config-site file from being applied.
* Removed the config site files for rztopaz and quartz since those machines have been retired.
* Updated Uintah to 2.6.3.
* Documented the -norun option in visit --fullhelp.
* Added support for GPU architectures in `CMake` and the `internallauncher`. When a `make package` comnand is executed, the GPU architecture will be added to the operating system and CPU identifier in the tar file name. For example, on a Linux system with an x86_64 CPU and an AMD MI250X GPU the tar file name will be `visit3_4_2.linux-x86_64-gfx90a.tar.gz`. Likewise, the operating system and CPU identifier identifier in a VisIt installation will include the GPU architecture in the same manner. As part of this change, the CPU identifier for a 64 bit, little endian, PowerPC processor will now be `ppc64le` instead of `intel`. The default CPU identifier for an unidentified CPU will now be `x86_64` instead of `intel`. Currently, only relatively new AMD GPUs are supported.
* When CMakeing VisIt, if `-C <cachefile>` is used or a slew of `-DVISIT_CMAKE_VARIABLE=VALUE` options are specified in lieu of a config-site file, the option `-DVISIT_CONFIG_SITE=NONE` is also required.
* Enhanced `build_visit` so that it pre-installs the OSPRay third party dependencies so that it can build OSPRay on a system without an internet connection if the tar file with the OSPRay third party libraries is present.


* Fixed a bug in the Wavefront OBJ Writer that would result in incorrect coloring for minimum or maximum values in downstream tools such as PowerPoint.
*  Fixed a bug with Pick unable to return results for 2D datasets.
*  Fixed a bug where vtk error messages were printed to the terminal when adding an Image Annotation Object to the viewer window.
*  Changed default logic for guessing cycles from file names to not consider any digits in the file name extension if present. This fixed the guessing logic for cases where a file extension includes a digit (e.g. `.h5m`)
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
