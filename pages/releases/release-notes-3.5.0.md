---
layout: page
title: "Release Notes for VisIt 3.5.0"
header:
   image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.5.0/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### General features added in version 3.5

* Added command recording for Annotation Objects.
* Added new surface rendering option using [ANARI](//github.com/KhronosGroup/ANARI-SDK).
* Added support to the AMR plugin for reading multiple AMR roots, multiple species, and mixtrue equations of state.
* Added support to the AMR plugin for reading files with only selected variables. 
* [cmocean](//matplotlib.org/cmocean/) color maps were added.
* Added `-python-log-file` command line option to control the name of the file used to log python methods (default=`visitlog.py`).
* Add individual stress components to the PVLD plugin metadata.
* Refactored how to import visit into a stand alone python module. This is now done via the `visit_launcher` module, avoiding module namespace issues.
* Antialiasing is no longer an on/off option, there are two modes: MSAA (when available) and FXAA. The default is still no antialiasing. (Due to a crash discovered during the final hours of 3.5.0 release creation, MSAA is disabled for now.)
* Added environment variable logging to VisIt's debug vlog files.
* Fix bug in PVLD reader that caused some files to not open.
* Updated Python to 3.13.9, support for Python 2 was removed.
* Updated encoding recipe for mp4 to use the ubiquitous x264 codec.
* Added encoding recipe for gif movie files.
* Changed the preferred movie format encoding to default to mp4 if available.
* Removed extraneous python modules from visit installs to avoid unnecessary security scan blocks.
* Added support for Sidre Tuple Views to the Blueprint Database Reader.

### Advanced features added in version 3.5

* Ghost Zone exchange was enhanced to handle not only scalars, material species, and vectors as before, but also tensors, symmetric tensors, and array variables.
* The `-compositer-debug` command line option was added, which dumps intermediate image results during the compositing process of scalable rendering.
* Added host profiles for ANL systems Aurora and Polaris. Removed hosts for ANL systems Cooley and Theta, as they were decommissioned.

### Changes in GUI behavior for in version 3.5

* Fixed an error appearing which states that the properties from a disabled light were modified even though no changes were made and "Apply" was pressed. Now, the error will only appear when a change was made and the light is still disabled as well as listing with all modified lights.
* Fixed bug with xmledit where changing a Field's type to `att` or `attvector` crashed the tool.
* Disabled rich text paste support in the Commands Window and Expressions Editor. Avoids battles with cut and pasted text from editors that embed formatting, such as vscode.
* Fixed a bug causing Color Table Window tags to be duplicated when loading a session file.
* Save session file now takes existing session file names into account to avoid naming collisions.
* Fixed a bug where bottom of main GUI window would be hidden behind the Windows taskbar.
* Fixed bugs with viewer text annotation sizes and layout when moving viewer windows between displays with different DPIs.
* Fixed Windows displaying as too tall on smaller laptop displays by adding Scroll bars where needed.  Some of the windows changed: Set Save options, Annotation, Integral Curve.
* Fixed bug with interaction tools (line/plane, etc) so that they will be updated by an operators atts at first enablement.
* Fixed a bug with the Line tool where it would hide behind 2D plots during interaction.
* Ensure Line tool is disabled for Curve plots, because it shouldn't be enabled in this situation.
* Fixed a bug where the line cue in Lineout mode would be drawn far from the mouse location when running on a laptop monitor.
* Fixed a bug with layout changes causing existing viewer windows to be drawn blank until they were resized.

### Changes in CLI behavior for in version 3.5

* Added a `GetActiveWindow()` method to return the currently active window.
* Ultrawrapper has been removed from VisIt. For similar functionality, please see: [PyDV](//pydv.readthedocs.io/en/latest/).
* CLI objects and functions improved in various ways including fixing `dir()` for them.
* `apropos()` help function is improved with additional arguments to control searches.
* Enhanced `DefineArrayExpression`, `DefineCurveExpression`, `DefineMaterialExpression`, `DefineMeshExpression`, `DefineScalarExpression`, `DefineSpeciesExpression`, `DefineTensorExpression` and `DefineVectorExpression` to take a list of expression names and expression definitions in addition to a single name of an expression and a single definition of an expression. Defining many expressions at once when the Graphical User Interface is active is much faster than defining them one at a time.
* Added support for PySide6 to visit_utils annotation and curve renders.

### File format reader changes in version 3.5

* The VTK database reader was modified to support GEOS flavor of .pvd and .vtm files.
* Updated Conduit to 0.9.4.
* Updated MFEM to 4.8.
* The Blueprint writer now supports YAML and JSON exports.
* Fixed a bug in the Blueprint reader causing unstructured points topology fields to display incorrectly.
* Fixed a bug in the Blueprint reader causing successful reading of Sidre data to trigger the failure case, leading to significantly degraded performance.
* The VisItXdmf reader has been removed, it hasn't been maintained. The Xdmf reader that utilizes the Xdmf library is still available.
* Added support for MFEM Quadrature Functions to the MFEM and Blueprint database plugins.
* Fixed a bug in the Blueprint reader where converting Blueprint species sets to the internal representation was performing an unnecessary conversion of the associated material set as well.

### Changes to VisIt's plots in version 3.5

* Added ANARI rendering support for volume plots.
* Enhanced the Pseudocolor plot to allow using the default variable for coloring the wireframe and points, as long as rendering of surfaces is turned off.

### Changes to VisIt's operators in version 3.5

* The MultiresControl Operator has been enhanced with new High-Order Options for high-order data from the MFEM and Blueprint plugins. High-order options include refinement basis selection (Gauss Lobatto and Closed Uniform), grid function projection method selection (nodal and zonal projection), and mesh refinement method selection (continuous and discontinuous refinement).

### Changes to VisIt's expression language in version 3.5

* Fixed a bug causing the min, max, and divide expressions to crash the compute engine when given a single variable as input. Min and max now return the result of that single variable, and divide throws an error instead of crashing.
* The Verdict mesh quality library that is builtin to VisIt was enhanced to handle degenerate hexahedra. This improves expressions and queries that use the Verdict library.
* Changed the `global_variance` expression to `global_var` and the `global_std_dev` expression to `global_std`.

### Changes to VisIt's picks and queries in version 3.5

* The X Ray Image Query now clips results beyond the far clipping plane.
* The Verdict mesh quality library that is builtin to VisIt was enhanced to handle generate hexahedra. This improves expressions and queries that use the Verdict library.
* Fixed a bug with the X Ray Image Query where VisIt would in some rare instances either crash or create an image that was too dark when running in parallel.
* The X Ray Image Query Blueprint output types now have "blueprint" in their names, so, for example, "hdf5" is now "blueprint hdf5". The original names are still supported.
* The X Ray Image Query Spatial Extents and Spatial Energy Reduced Meshes are now centered at the origin.

### Other bugs fixed in version 3.5

* Fixed command recording for a Pick query with global element.
* Fixed a crash in structured domain boundaries when exchanging materials that lack a *mix_zone* array.
* Fixed a crash in structured domain boundaries when exchanging mixed material data using local boundary data.
* Fixed a potential infinite loop in our internal string helper utilities.
* Fixed error in Command Recording of a Query, where python tuples weren't represented correctly.
* 3D Text Annotation's relative height widget has been fixed so that whether the value is changed via the spin box up/down arrows or a new value is typed, the widget will update and so will the height of the text.
* View computations become garbled when Viewport Coordinate values are set outside the range of [0,1]. The docs specify the values should be in this range, and they are now automatically clamped to this range when being set via the GUI or CLI.
* Fixed a bug crashing viewer if label tick spacing was too cramped exceeding a builtin threshold of 200 labels.
* [#20396](//github.com/visit-dav/visit/issues/20396) Fixed bug in Exodus reader where simple expressions involving some Exodus variables may wind up getting garbage data.
* Fixed a Tecplot reader bug that crashed the engine.
* Fixed a memory bug in AMR plugin when reading velocity magnitude.
* In the PVLD plugin, show SPH in metadata at the first time step even when there are no SPH particles initially.
* Fixed a viewer crash with transparency.
* Fixed a bug when CLI would not exit if GUI was also open and exit was initiated from the GUI.
* Fixed a command recording bug with the Expression window where all the operator generated expressions would get recorded.
* Added a descriptive error message for when a movie encoding format is not supported on the current platform.
* Fixed a bug where rendering with shadows would result in an all black image except for the annotations when the image contained transparent geometry.
* Fixed a bug where RPATHs weren't stripped from distributions. This could lead to issues for users that didn't build the distribution. It could also cause issues when a distribution is installed on a machine different from where it was built.
* Fixed crash loading SILO files when compiled with version 4.11 of the SILO library.
* Fixed a bug with global mesh expressions causing them to only work on single domain data. They now function across all domains in parallel and in serial.
* Eliminated many memory leaks. Here is a summary of the fixed leaks.
    * Fixed a leak in the operator that removes ghost zones and calculates external faces.
    * Fixed a leak in the Resample operator.
    * Fixed a leak with the zone_centers expression.
    * Fixed memory leaks in all the plots.
* Modified the SAMRAI reader to free most of its cached data when the timestep was changed.
* Fixed a crash with Curve plot when Curve contained more than 100000 points.
* Fixed a crash in the PVLD parallel test suite.
* Fixed a problem where the Silo plugin would not honor major_order setting for vector variables (e.g. more than one component) on 2 or 3D point- or quad- meshes.
* Fixed a bug that prevented Silex from being distributed with the installation on Windows.
* Added more robust error messages when VisIt's launcher on Windows cannot determine a writeable folder for use as VISITUSERHOME.
* Fixed a bug with Save Movie Wizard that prevented extra movie formats being available on Windows even if ffmpeg present on the system.

### Build features added in version 3.5

* Removed support for VTK-8, VTK version is now 9.5.0.
* Removed support for Qt 5, QT version is now 6.4.2.
* Removed support for SZIP compression library.
* CMake updated to version 3.31.8.
* Zlib updated to version 1.3.1.
* HDF5 updated to version 2.0.0.
* Silo updated to version 4.12.0.
* NetCDF updated to version 4.9.3.
* Added support for building `meson`, `ninja`, `xcb` and `xkbcommon` to allow building VisIt with Qt6 on systems that do not have all the `xcb` and `xkbcommon` development packages installed. `xcb` and `xkbcommon` are used by Qt6. `meson` and `ninja` are used to build `xkbcommon`. By enabling all four of these packages, Qt6 can be built on systems that don't have `xcb` and `xkbcommon` installed on them.
* Added a patch for building MPICH on a system that has a newer version of SLURM installed.
* Fixed a bug where cloning and checking out VisIt could fail silently without providing error messages.
* Added support for building `anari` to allow building VisIt with ANARI rendering support.
* Updated VTK build script, `bv_vtk.sh`, to enable ANARI rendering module in VTK.
* The command line options `--all-io`, `--dbio-only`, `--nonio` and  `--advanced` were removed.  This was done to simplify maintenance and addition of new modules. The `--optional` option still turns on most optional libraries. The `--no-thirdparty` option still turns off the required libraries. Otherwise individual libraries can be enabled/disabled by `--` or `--no` syntax e.g. `--mpich --no-python`.  Please run `build_visit --help` for more information on available options.
* A patch was added for compiling Mili on RockyLinux 8 and 9.
* Patches were added for compiling PIDX, ADVIO and CFISTIO on Fedora40 with gcc14.
* OpenEXR updated to version 3.3.4.
* VTK-m updated to version 2.3.0.
* Added a patch to bv_vtk.sh that exposes the vtkAnariPass in the ANARI volume mapper and adds panning and zooming capabilities to the ANARI camera.
* Added command line options `--print-files` and `--print-files-html`. Both options list all the files that `build_visit` may download grouped by "Required", "Optional" and "Explicit". The first lists the files as text and the second lists the files as an HTML table.
* Added a patch to `bv_vtk.sh` that brings in critical updates from [https://gitlab.kitware.com/vtk/vtk/-/merge_requests/12759](//gitlab.kitware.com/vtk/vtk/-/merge_requests/12759) that fixes texture issues and crashes when switching between ANARI back-ends.
* Added patches to `bv_silo.sh` for delimiter bracketing of constant nameschemes, mpio virtual file driver enablement in HDF5, confusion of lib/lib64 install paths, correct cmake handling of zlib dependence, and erroneous extents calculations when writing meshes.

### Changes for VisIt developers in version 3.5

* xmledit and other xml code gen tools have been fixed such that all logic in a '.code' file will be properly displayed in 'xmledit' and also saved accurately when 'save' issued from xmledit. The 'Target' designator is now always written to the .code file, even if the target is the default 'xml2atts' target. Unix-style line endings are now always used when writing files from 'xmledit'.

### Third-party libraries used for version 3.5

| Required      |
| ------------- |
| cmake-3.31.8.tar.gz |
| zlib-1.3.1.tar.xz |
| ninja-1.12.1.tar.gz |
| meson_python-0.18.0.tar.gz |
| Python-3.13.9.tgz |
| scikit_build_core-0.11.6.tar.gz |
| sphinxcontrib_qthelp-2.0.0.tar.gz |
| mpi4py-4.1.1.tar.gz |
| idna-3.11.tar.gz |
| imagesize-1.4.1.tar.gz |
| requests-2.32.5.tar.gz |
| sphinx-tabs-3.4.7.tar.gz |
| editables-0.5.tar.gz |
| roman_numerals-3.1.0.tar.gz |
| pluggy-1.6.0.tar.gz |
| wheel-0.45.1.tar.gz |
| sphinxcontrib-jquery-4.1.tar.gz |
| hatch_vcs-0.5.0.tar.gz |
| pathspec-0.12.1.tar.gz |
| importlib_metadata-8.7.0.tar.gz |
| markupsafe-3.0.3.tar.gz |
| hatchling-1.27.0.tar.gz |
| pyproject_metadata-0.9.1.tar.gz |
| numpy-2.3.4.tar.gz |
| urllib3-2.5.0.tar.gz |
| jinja2-3.1.6.tar.gz |
| docutils-0.21.2.tar.gz |
| sphinxcontrib-jsmath-1.0.1.tar.gz |
| alabaster-1.0.0.tar.gz |
| charset_normalizer-3.4.4.tar.gz |
| sphinxcontrib_serializinghtml-2.0.0.tar.gz |
| setuptools-80.9.0.tar.gz |
| pygments-2.19.1.tar.gz |
| sphinx_rtd_theme-3.0.2.tar.gz |
| sphinxcontrib_htmlhelp-2.1.0.tar.gz |
| packaging-25.0.tar.gz |
| tomli-2.3.0.tar.gz |
| sphinxcontrib_devhelp-2.0.0.tar.gz |
| zipp-3.23.0.tar.gz |
| toml-0.10.2.tar.gz |
| babel-2.17.0.tar.gz |
| sphinxcontrib_applehelp-2.0.0.tar.gz |
| pillow-12.0.0.tar.gz |
| cython-3.2.1.tar.gz |
| calver-2025.10.20.tar.gz |
| snowballstemmer-3.0.1.tar.gz |
| certifi-2025.11.12.tar.gz |
| colorama-0.4.6.tar.gz |
| pybind11-3.0.1.tar.gz |
| flit_core-3.12.0.tar.gz |
| sphinx-8.2.3.tar.gz |
| trove_classifiers-2025.9.11.17.tar.gz |
| setuptools_scm-9.2.2.tar.gz |
| qttools-everywhere-src-6.4.2.tar.xz |
| qtbase-everywhere-src-6.4.2.tar.xz |
| qtsvg-everywhere-src-6.4.2.tar.xz |
| VTK-9.5.0.tar.gz |
| vtk-m-v2.3.0.tar.gz |
| mesa-17.3.9.tar.xz |
| cfe-6.0.1.src.tar.xz |
| llvm-6.0.1.src.tar.xz |

| Optional |
| -------- |
| adios2-2.10.0-rc1.tar.gz |
| adios-1.13.1.tar.gz |
| adios2-2.10.0-rc1.tar.gz |
| AdvIO-1.2.tar.gz |
| c-blosc2-2.11.3.tar.gz |
| boost_1_67_0.tar.gz |
| ccse-1.3.5.tar.gz |
| cfitsio-4.6.3.tar.gz |
| CGNS-4.1.0.tar.gz |
| conduit-v0.9.4-src-with-blt.tar.gz |
| FMS-0.2.tar.gz |
| gdal-2.2.4.tar.gz |
| H5Part-1.6.6.tar.gz |
| hdf5-2.0.0.tar.xz |
| icet-master-77c708f9090236b576669b74c53e9f105eedbd7e.tar.gz |
| mfem-4.8.tar.gz |
| mili-23.02.tar.gz |
| moab-5.5.0.tar.gz |
| netcdf-c-4.9.3.tar.gz |
| Imath-3.1.12.tar.gz |
| openexr-3.3.4.tar.gz |
| embree-3.2.0.x86_64.linux.tar.gz |
| embree-3.2.0.x86_64.macosx.tar.gz |
| ispc-v1.21.1-linux-oneapi.tar.gz |
| ospray-libs-3.0.0.tar.gz |
| ospray-3.2.0.arm64.macosx.zip |
| ospray-3.2.0.x86_64.macosx.zip |
| ospray-3.0.0.tar.gz |
| PIDX-0.9.3.tar.gz |
| qwt-git-d3706f6e7f0351d278be2d989a4caaf92b399bbd.tar.xz |
| Silo-4.12.0.tar.xz |
| Uintah-2.6.3.tar.gz |
| vtk-m-v2.3.0.tar.gz |
| Xdmf-2.1.1.tar.gz |

| Explicit |
| -------- |
| ANARI-SDK-0.15.0_with_deps.zip |
| glu-9.0.0.tar.gz |
| mesa-17.3.9.tar.xz |
| meson-1.9.1.tar.gz |
| mpich-3.3.1.tar.gz |
| libxcb-image-xcb-util-image-0.4.1.tar.gz |
| libxcb-m4-xcb-util-m4-0.4.1.tar.gz |
| libxcb-wm-xcb-util-wm-0.4.2.tar.gz |
| libxcb-keysyms-xcb-util-keysyms-0.4.1.tar.gz |
| libxcb-render-util-xcb-util-renderutil-0.3.10.tar.gz |
| libxcb-util-xcb-util-0.4.1.tar.gz |
| libxkbcommon-1.7.0.tar.xz |
| macros-util-macros-1.20.2.tar.gz |

