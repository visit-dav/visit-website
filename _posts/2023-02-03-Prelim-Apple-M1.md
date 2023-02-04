---
layout: page
show_meta: false
title: "Alpha Release for Apple M1"
subheadline: "First attempt at native build for Apple M1 machines"
tags:
    - post format
categories:
    - releases
header:
    image_fullwidth: release-banner.jpg
image:
    thumb: release-thumbnail.png
author: miller86
---

We've made an Alpha release of VisIt version 3.3.1 for native Apple M1 machines.
This release does not yet support parallel or all database plugins.
Features that were disabled, primarly to get to a point of early testing include Ospray, Adios2, Advio, Boxlib, GDAL, Icet, netCDF, PIDX, PySide, Xdmf, TBB, Embree.
These will be included in a future M1 native release.
We also did not package this release as a `.dmg` file or sign the release.
That said, those who wish to give it a try should be able to download [the release](https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.darwin-arm64.tar.xz), untar it and follow the *Linux* [install instructions](https://github.com/visit-dav/visit/releases/download/v3.3.1/INSTALL_NOTES.txt).

We would appreciate any feedback at our [GitHub discussions](https://github.com/visit-dav/visit/discussions).
