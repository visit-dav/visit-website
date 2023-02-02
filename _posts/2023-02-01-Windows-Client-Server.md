---
layout: page
show_meta: false
title: "Fix for Windows Client/Server to LC"
subheadline: "Fixes for client/server connections to Livermore Computing from Windows"
teaser: "If you cannot connect from Windows to LC, please read on..."
tags:
    - post format
categories:
    - releases
header:
    image_fullwidth: Windows-10-banner.jpg
image:
    thumb: Windows-10-thumb.jpg
author: biagas
---

We discovered a need to update the `qtssh` executable used on Windows (which uses [PuTTY]) with a newer version of [PuTTY] to address client-server connection issues to Livermore Computing.
The updated `qtssh` is provided for download as a convenience until VisIt 3.3.2 is released (which includes the updated `qtssh`).

If you discover issues connecting client-server using VisIt 3.x, you can download [`qtssh.zip`](https://github.com/visit-dav/visit/releases/download/v3.3.1/qtssh.zip), unzip it and place the executable in the root directory of VisIt's install, overwriting the existing version.

If [OpenSSH] is installed, another workaround is to use it (`C:\windows\system32\openssh\ssh.exe`) in place of VisIt's `qtssh`.
In order to use [OpenSSH], set `VISITSSH` environment variable to point to `/full/path/to/ssh.exe` before you next run VisIt.
When you do this VisIt will use that ssh, and its password window will not appear.

You can use any ssh you have installed that successfully connects to your remote machine (or download latest [PuTTY] and use it's `plink.exe`).

[PuTTY]: https://putty.org
[OpenSSH]: https://www.openssh.com
