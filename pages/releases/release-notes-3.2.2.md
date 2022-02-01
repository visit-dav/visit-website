---
layout: page
title: "Release Notes for VisIt 3.2.2"
header:
  image_fullwidth: "titan-2012.jpg"
permalink: "/releases/release-notes-3.2.2/"
---

Welcome to VisIt's release notes page. This page describes the important
enhancements and bug-fixes that were added to this release.

1. TOC
{:toc}

### Bugs fixed in version 3.2.2

* Fixed a bug in the Blueprint reader preventing unsigned 64-bit array field values.
* Fixed a bug in the Blueprint reader that caused unnecessary copies of topology connectivity arrays.
* Fixed a bug in the Blueprint reader where YAML or JSON root files were rewritten on open, which could strip comments and change the file entires. The root file is now opened in a read only mode.
* Fixed a bug where versions of VisIt that supported hardware accelerated rendering would display a black image in the visualization window.
* Fixed a crash when saving images greater than approximately 8,000 x 8,000. Now images can be saved up to 16,384 x 16,384.
* Fixed a bug in the *Chombo Users* configuration that prevented the macros from being loaded and appearing in the *Macros* window.
* Fixed a bug where VisIt would hang when connecting to a remote system running Linux when connecting from a Linux or macOS system.
* The path is now stripped off the filename in the Pick output to be consistent with output on linux.
* The command recording for GlobalLineoutAttributes now works correctly.
* Fixed a bug with Pick for Rectilinear grids when real zones are completely surrounded by ghost zones.
* Fixed a bug where VisIt would hang when working with a AMR meshes and the number of active patches was less than the number of processors and the patches were not rectilinear.
* Fixed a bug where encoding an mpeg movie on an Ubuntu 21 system failed.
* Fixed a bug in the Uintah reader where long64 data was read as zeroes. This primarily impacted particle ids.

### Enhancements in version 3.2.2

* The VTK reader has been expanded to support .pvd files.
* A `-lang` command-line argument was added to start VisIt with a different language translation. For example, use `-lang fr` to run VisIt with the French translation.
* Updated the Los Alamos National Laboratory's Trinity host profile to no longer use the gateway.
* Improved the setting of the tick marks and labels for log scaled axes for curve plots.
* Python endpoint scripts (such as pip, pyenv) are now installed along with Python inside of VisIt on linux and macOS.

### Changes for VisIt developers in version 3.2.2

* Fixed a compile issue on a Fedora 31 Docker container that didn't have any OpenGL header files installed. This involved modifying `engine/main/CMakeLists.txt` to add `OPENGL_INCLUDE_DIR` to the include directories if building with IceT and MesaGL.
* Enhanced build_visit to apply a patch to fix a compile issue with VTK with gcc 10.3 on Ubuntu 21.04.
* Added a Docker file for Ubuntu 21.04.
* Fixed a bug where the test suite files displayed in the dashboard produced by the regression test suite were blank.
* Enhanced build_visit to apply a patch to fix a compile issue with `p7zip` with gcc 10.3 on Ubuntu 21.04.
* Enhanced build_visit so that it worked on systems that only have Python 3 installed.
* Enhanced build_visit to apply a patch that fixes a compile issue with Python on MacOS 11.
* Enhanced the building of Qt in build_visit to check for the system libraries being located in `/usr/lib` if `/usr/lib64` doesn't exist.
* Enhanced build_visit to apply a patch that fixes a compile issue with Qt with gcc-11.
* Added a Docker file for Debian 11.
* Added the spack environment files `compilers.yaml` and `packages.yaml` for spock.olcf.ornl.gov.
