---
layout: page
title: "VisIt Releases"
header:
  image_fullwidth: mfem-hires-1.png
permalink: "/releases-as-tables/"
---
* [Series 3.3 (latest)](#series-33)
* [Series 3.2](#series-32)
* [Series 3.1](#series-31)
* [Series 3.0](#series-30)
* [Older releases](https://wci.llnl.gov/simulation/computer-codes/visit/executables)

VisIt is supported by the Department of Energy with funding from the
[Advanced Simulation and Computing Program](https://asc.llnl.gov), the
[Scientific Discovery through Advanced Computing Program](https://www.scidac.gov),
and the [Exascale Computing Project](https://www.exascaleproject.org).

If you use VisIt to generate images or movies please help us by
[citing](citing-visit.md) VisIt in your paper or in the credits of your movie.
Doing so helps us sustain funding for on going maintenance and future improvements.

### Series 3.3

* Links to checksums and file sizes are provided for confirming download integrity.
* Hover over a link to reveal additional details about a download.
* For linux, the [`visit-install`][vm2] script is needed to complete an *install*.
* The Ubuntu 20 version will run on Ubuntu 22.

Date | Dec 2022 | Sep 2022 | Jun 2022
---:|:---:|:---:|:---:
Version                   |[3.3.2]|[3.3.1]|[3.3.0]
Win 10<br>development     |[use][332w]<br>[dev][332wd]|[use][331w]<br>[dev][331wd]|[use][330w]<br>[dev][330wd]
Mac 10.15<br>12.6 (M1)    |[dmg][332m1015dmg]/[tgz][332m1015tgz]<br>|[dmg][331m1015dmg]/[tgz][331m1015tgz]<br>[txz][331m126txz]|[dmg][330m1015dmg]/[tgz][330m1015tgz]<br>
Ubuntu 20<br>18           |[tgz][332u20]<br>[tgz][332u18]|[tgz][331u20]<br>[tgz][331u18]|[tgz][330u20]<br>[tgz][330u18]
RedHat EL7<br>w/ Mesa     |[tgz][332rh]<br>[tgz][332rhwm]|[tgz][331rh]<br>[tgz][331rhwm]|[tgz][330rh]<br>[tgz][330rhwm]
Fedora 31                 |[tgz][332f31]|[tgz][331f31]|[tgz][330f31]
11<br>Debian 10<br>9      |[tgz][332d11]<br>[tgz][332d10]<br>[tgz][332d9]|[tgz][331d11]<br>[tgz][331d10]<br>|[tgz][330d11]<br>[tgz][330d10]<br>
Java client               |[tgz][332j]|[tgz][331j]|[tgz][330j]
[visit-install][vm1]      |[sh][332vi]|[sh][331vi]|[sh][330vi]
[build_visit][vm2]        |[sh][332bv]|[sh][331bv]|[sh][330bv]
Source                    |[tgz][332stgz]|[tgz][331stgz]|[tgz][330stgz]
Rel notes<br>Install notes |[html][332rn]<br>[txt][332in]|[html][331rn]<br>[txt][331in]|[html][330rn]<br>[txt][330in]
Checksums<br><br><br>File sizes |[md5][332md5]<br>[sh1][332sha1]<br>[sh256][332sha256]<br>[txt][332fs]|[md5][331md5]<br>[sh1][331sha1]<br>[sh256][331sha256]<br>[txt][331fs]|[md5][330md5]<br>[sh1][330sha1]<br>[sh256][330sha256]<br>[txt][330fs]
Manuals                   |[html][332doc]/[pdf][332pdf]|[html][331doc]/[pdf][331pdf]|[html][330doc]/[pdf][330pdf]

<!-- 3.3.0 release asset links -->
[3.3.0]: https://github.com/visit-dav/visit/releases/tag/v3.3.0 "All GitHub release assets"
[330w]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3.3.0_x64.exe "Windows 10, 64-bit Visual Studio 2017"
[330wd]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit_windowsdev_3.3.0.zip "Windows 10 for VisIt development, 64-bit Visual Studio 2017"
[330m1015dmg]: https://github.com/visit-dav/visit/releases/download/v3.3.0/Visit-3.3.0.dmg "Darwin 10.15, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[330m1015tgz]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3.3.0.darwin-x86_64-10_15.tar.gz "Darwin 10.15, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[330u22]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-ubuntu22.tar.gz "Ubuntu 22, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.3"
[330u20]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3"
[330u18]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 7.5"
[330rh]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[330rhwm]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[330f31]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-fedora31.tar.gz "Fedora 31, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3.1"
[330d9]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-debian9.tar.gz "Debian 9, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 6.3"
[330d10]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-debian10.tar.gz "Debian 10, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3"
[330d11]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3_3_0.linux-x86_64-debian11.tar.gz "Debian 11, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.2"
[330j]: https://github.com/visit-dav/visit/releases/download/v3.3.0/jvisit3.3.0.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[330vi]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit-install3_3_0 "Linux installer script needed to install linux binaries"
[330bv]: https://github.com/visit-dav/visit/releases/download/v3.3.0/build_visit3_3_0 "Download *only* this script to build VisIt from sources"
[330stgz]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit3.3.0.tar.gz
[330rn]: ../releases/release-notes-3.3.0
[330in]: https://github.com/visit-dav/visit/releases/download/v3.3.0/INSTALL_NOTES.txt
[330sha256]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[330sha1]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[330md5]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[330fs]: https://github.com/visit-dav/visit/releases/download/v3.3.0/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[330doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.3.0/
[330pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.3.0/pdf/

<!-- 3.3.1 release asset links -->
[3.3.1]: https://github.com/visit-dav/visit/releases/tag/v3.3.1 "All GitHub release assets"
[331w]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3.3.1_x64.exe "Windows 10, 64-bit Visual Studio 2017"
[331wd]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit_windowsdev_3.3.1.zip "Windows 10 for VisIt development, 64-bit Visual Studio 2017"
[331m1015dmg]: https://github.com/visit-dav/visit/releases/download/v3.3.1/Visit-3.3.1.dmg "Darwin 10.15, Darwin Kernel Version 19.6.0, clang-1100.0.33.16, MPICH"
[331m1015tgz]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3.3.1.darwin-x86_64-10_15.tar.gz "Darwin 10.15, Darwin Kernel Version 19.6.0, clang-1100.0.33.16, MPICH"
[331m126txz]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.darwin-arm64.tar.xz "Darwin 12.6, Darwin Kernel Version 21.6.0, clang-1400.0.29.202, arm64, Python 3.9.6"
[331u22]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-ubuntu22.tar.gz "Ubuntu 22, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.3"
[331u20]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3"
[331u18]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 7.5"
[331rh]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[331rhwm]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[331f31]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-fedora31.tar.gz "Fedora 31, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3.1"
[331d9]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-debian9.tar.gz "Debian 9, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 6.3"
[331d10]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-debian10.tar.gz "Debian 10, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3"
[331d11]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3_3_1.linux-x86_64-debian11.tar.gz "Debian 11, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.2"
[331j]: https://github.com/visit-dav/visit/releases/download/v3.3.1/jvisit3.3.1.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[331vi]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit-install3_3_1 "Linux installer script needed to install linux binaries"
[331bv]: https://github.com/visit-dav/visit/releases/download/v3.3.1/build_visit3_3_1 "Download *only* this script to build VisIt from sources"
[331stgz]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit3.3.1.tar.gz
[331rn]: ../releases/release-notes-3.3.1
[331in]: https://github.com/visit-dav/visit/releases/download/v3.3.1/INSTALL_NOTES.txt
[331sha256]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[331sha1]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[331md5]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[331fs]: https://github.com/visit-dav/visit/releases/download/v3.3.1/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[331doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.3.1/
[331pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.3.1/pdf/

<!-- 3.3.2 release asset links -->
[3.3.2]: https://github.com/visit-dav/visit/releases/tag/v3.3.2 "All GitHub release assets"
[332w]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3.3.2_x64.exe "Windows 10, 64-bit Visual Studio 2017"
[332wd]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit_windowsdev_3.3.2.zip "Windows 10 for VisIt development, 64-bit Visual Studio 2017"
[332m1015dmg]: https://github.com/visit-dav/visit/releases/download/v3.3.2/Visit-3.3.2.dmg "Darwin 10.15, Darwin Kernel Version 19.6.0, clang-1100.0.33.16, MPICH"
[332m1015tgz]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3.3.2.darwin-x86_64-10_15.tar.gz "Darwin 10.15, Darwin Kernel Version 19.6.0, clang-1100.0.33.16, MPICH"
[332m126txz]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.darwin-arm64.tar.xz "Darwin 12.6, Darwin Kernel Version 21.6.0, clang-1400.0.29.202, arm64, Python 3.9.6"
[332u22]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-ubuntu22.tar.gz "Ubuntu 22, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.3"
[332u20]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3"
[332u18]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 7.5"
[332rh]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[332rhwm]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[332f31]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-fedora31.tar.gz "Fedora 31, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3.1"
[332d9]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-debian9.tar.gz "Debian 9, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 6.3"
[332d10]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-debian10.tar.gz "Debian 10, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3"
[332d11]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3_3_2.linux-x86_64-debian11.tar.gz "Debian 11, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.2"
[332j]: https://github.com/visit-dav/visit/releases/download/v3.3.2/jvisit3.3.2.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[332vi]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit-install3_3_2 "Linux installer script needed to install linux binaries"
[332bv]: https://github.com/visit-dav/visit/releases/download/v3.3.2/build_visit3_3_2 "Download *only* this script to build VisIt from sources"
[332stgz]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit3.3.2.tar.gz
[332rn]: ../releases/release-notes-3.3.2
[332in]: https://github.com/visit-dav/visit/releases/download/v3.3.2/INSTALL_NOTES.txt
[332sha256]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[332sha1]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[332md5]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[332fs]: https://github.com/visit-dav/visit/releases/download/v3.3.2/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[332doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.3.2/
[332pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.3.2/pdf/

### Series 3.2

* Links to checksums and file sizes are provided for confirming download integrity.
* Hover over a link to reveal additional details about a download.
* For linux, the [`visit-install`][vm2] script is needed to complete an *install*.

Date | Jan 2022 | Jul 2021 | Apr 2021
---:|:---:|:---:
Version               |[3.2.2]|[3.2.1]|[3.2.0]
Win 10<br>development |[use][322w]<br>[dev][322wd]|[use][321w]<br>[dev][321wd]|[use][320w]<br>[dev][320wd]
Mac 10.15<br>10.14    |[dmg][322m1015dmg]<br>|<br>[dmg][321m1014dmg]|<br>[dmg][320m1014dmg]/[tgz][320m1014tgz]
21<br>Ubuntu 20<br>18 |[tgz][322u21]<br>[tgz][322u20]<br>[tgz][322u18]|[tgz][321u21]<br>[tgz][321u20]<br>[tgz][321u18]|<br>[tgz][320u20]<br>[tgz][320u18]
RedHat EL7<br>w/ Mesa |[tgz][322rh]<br>[tgz][322rhwm]|[tgz][321rh]<br>[tgz][321rhwm]|<br>[tgz][320rhwm]
Fedora 31             |[tgz][322f31]|[tgz][321f31]|[tgz][320f31]
11<br>Debian 10<br>9  |[tgz][322d11]<br>[tgz][322d10]<br>[tgz][322d9]|[tgz][321d11]<br>[tgz][321d10]<br>[tgz][321d9]|<br>[tgz][320d10]<br>[tgz][320d9]
Centos 8              |[tgz][322c8]|[tgz][321c8]|[tgz][320c8]
Java client           |[tgz][322j]|[tgz][321j]|[tgz][320j]
[visit-install][vm1]  |[sh][322vi]|[sh][321vi]|[sh][320vi]
[build_visit][vm2]    |[sh][322bv]|[sh][321bv]|[sh][320bv]
Source                |[tgz][322stgz]|[tgz][321stgz]|[tgz][320stgz]
Rel notes<br>Install notes |[html][322rn]<br>[txt][322in]|[html][321rn]<br>[txt][321in]|[html][320rn]<br>[txt][320in]
Checksums<br><br><br>File sizes |[md5][322md5]<br>[sh1][322sha1]<br>[sh256][322sha256]<br>[txt][322fs]|[md5][321md5]<br>[sh1][321sha1]<br>[sh256][321sha256]<br>[txt][321fs]|[md5][320md5]<br>[sh1][320sha1]<br>[sh256][320sha256]<br>[txt][320fs]
Manuals               |[html][322doc]/[pdf][322pdf]|[html][321doc]/[pdf][321pdf]|[html][320doc]/[pdf][320pdf]

[dev]: # "For development on Windows"
[vm1]: https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/gui_manual/Intro/Installing_VisIt.html?highlight=visit-install#installing-on-linux "Use to install Linux binaries"
[vm2]: https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/building_visit/index.html#building-visit

<!-- 3.2.2 release asset links -->
[3.2.2]: https://github.com/visit-dav/visit/releases/tag/v3.2.2 "All GitHub release assets"
[322w]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3.2.2_x64.exe "Windows 10, 64-bit Visual Studio 2017"
[322wd]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit_windowsdev_3.2.2.zip "Windows 10 for VisIt development, 64-bit Visual Studio 2017"
[322m1015dmg]: https://github.com/visit-dav/visit/releases/download/v3.2.2/Visit-3.2.2.dmg "Darwin 10.15, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[322u21]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-ubuntu21.tar.gz "Ubuntu 21, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.3"
[322u20]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3"
[322u18]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 7.5"
[322rh]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[322rhwm]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[322f31]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-fedora31.tar.gz "Fedora 31, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3.1"
[322d9]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-debian9.tar.gz "Debian 9, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 6.3"
[322d10]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-debian10.tar.gz "Debian 10, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3"
[322d11]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-debian11.tar.gz "Debian 11, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.2"
[322c8]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3_2_2.linux-x86_64-centos8.tar.gz "CentOS 8, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3.1"
[322j]: https://github.com/visit-dav/visit/releases/download/v3.2.2/jvisit3.2.2.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[322vi]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit-install3_2_2 "Linux installer script needed to install linux binaries"
[322bv]: https://github.com/visit-dav/visit/releases/download/v3.2.2/build_visit3_2_2 "Download *only* this script to build VisIt from sources"
[322stgz]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit3.2.2.tar.gz
[322rn]: ../releases/release-notes-3.2.2
[322in]: https://github.com/visit-dav/visit/releases/download/v3.2.2/INSTALL_NOTES.txt
[322sha256]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[322sha1]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[322md5]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[322fs]: https://github.com/visit-dav/visit/releases/download/v3.2.2/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[322doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.2.2/
[322pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.2.2/pdf/

<!-- 3.2.1 release asset links -->
[3.2.1]: https://github.com/visit-dav/visit/releases/tag/v3.2.1 "All GitHub release assets"
[321w]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3.2.1_x64.exe "Windows 10, 64-bit Visual Studio 2017"
[321wd]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visitdev3.2.1.exe "Windows 10 for VisIt development, 64-bit Visual Studio 2017"
[321m1014dmg]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3.2.1.darwin-x86_64-10_14.dmg "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[321u21]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-ubuntu21.tar.gz "Ubuntu 21, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.3"
[321u20]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3"
[321u18]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 7.5"
[321rh]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[321rhwm]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[321f31]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-fedora31.tar.gz "Fedora 31, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 9.3.1"
[321d9]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-debian9.tar.gz "Debian 9, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 6.3"
[321d10]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-debian10.tar.gz "Debian 10, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3"
[321d11]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-debian11.tar.gz "Debian 11, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 10.2"
[321c8]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3_2_1.linux-x86_64-centos8.tar.gz "CentOS 8, 5.4.72-microsoft-standard-WSL2 #1 SMP, gcc 8.3.1"
[321j]: https://github.com/visit-dav/visit/releases/download/v3.2.1/jvisit3.2.1.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[321vi]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit-install3_2_1 "Linux installer script needed to install linux binaries"
[321bv]: https://github.com/visit-dav/visit/releases/download/v3.2.1/build_visit3_2_1 "Download *only* this script to build VisIt from sources"
[321stgz]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit3.2.1.tar.gz
[321rn]: ../releases/release-notes-3.2.1
[321in]: https://github.com/visit-dav/visit/releases/download/v3.2.1/INSTALL_NOTES.txt
[321sha256]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[321sha1]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[321md5]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[321fs]: https://github.com/visit-dav/visit/releases/download/v3.2.1/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[321doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.2.1/
[321pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.2.1/pdf/

<!-- 3.2.0 release asset links -->
[3.2.0]: https://github.com/visit-dav/visit/releases/tag/v3.2.0 "All GitHub release assets"
[320w]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3.2.0_x64.exe "Windows 10, 64-bit Visual Studio 2017"
[320wd]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visitdev3.2.0.exe "Windows 10 for VisIt development, 64-bit Visual Studio 2017"
[320m1014dmg]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3.2.0.darwin-x86_64-10_14.dmg "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[320m1014tgz]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3.2.0.darwin-x86_64-10_14.tar.gz "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[320u20]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 4.19.76-linuxkit #1 SMP, gcc 9.3"
[320u18]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.19.76-linuxkit #1 SMP, gcc 7.5"
[320rh]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[320rhwm]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[320f31]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-fedora31.tar.gz "Fedora 31, 4.19.76-linuxkit #1 SMP, gcc 9.3.1"
[320d9]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-debian9.tar.gz "Debian 9, 4.19.76-linuxkit #1 SMP, gcc 6.3"
[320d10]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-debian10.tar.gz "Debian 10, 4.19.76-linuxkit #1 SMP, gcc 8.3"
[320c8]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3_2_0.linux-x86_64-centos8.tar.gz "CentOS 8, 4.19.76-linuxkit #1 SMP, gcc 8.3.1"
[320j]: https://github.com/visit-dav/visit/releases/download/v3.2.0/jvisit3.2.0.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[320vi]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit-install3_2_0 "Linux installer script needed to install linux binaries"
[320bv]: https://github.com/visit-dav/visit/releases/download/v3.2.0/build_visit3_2_0 "Download *only* this script to build VisIt from sources"
[320stgz]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit3.2.0.tar.gz
[320rn]: ../releases/release-notes-3.2.0
[320in]: https://github.com/visit-dav/visit/releases/download/v3.2.0/INSTALL_NOTES.txt
[320sha256]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[320sha1]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[320md5]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[320fs]: https://github.com/visit-dav/visit/releases/download/v3.2.0/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[320doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.2.0/
[320pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.2.0/pdf/

### Series 3.1

* Links to checksums and file sizes are provided for confirming download integrity.
* Hover over a link to reveal additional details about a download.
* For linux, the [`visit-install`][vm2] script is needed to complete an *install*.

Date | Nov 2020 | Sep 2020 | May 2020 | Feb 2020 | Dec 2019
---:|:---:|:---:|:---:|:---:|:---:
Version&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     | [3.1.4] | [3.1.3] | [3.1.2] | [3.1.1] | [3.1.0]
Win 10/8/7<br>development|[user][314w]<br>[dev][314wd]|[user][313w]<br>[dev][313wd]|[user][312w]<br>[dev][312wd]|[user][311w]<br>[dev][311wd]|[user][310w]<br>[dev][310wd]
Mac 10.15<br>10.14<br>10.13|[dmg][314m1015dmg]/[tgz][314m1015tgz]<br>[dmg][314m1014dmg]/[tgz][314m1014tgz]<br>&nbsp;|&nbsp;<br>[dmg][313m1014dmg]/[tgz][313m1014tgz]<br>&nbsp;|&nbsp;<br>[dmg][312m1014dmg]/[tgz][312m1014tgz]<br>&nbsp;|&nbsp;<br>[dmg][311m1014dmg]/[tgz][311m1014tgz]<br>[dmg][311m1013dmg]/[tgz][311m1013tgz]|&nbsp;<br>&nbsp;<br>[dmg][310m1013dmg]/[tgz][310m1013tgz]
20<br>Ubuntu 19<br>18<br>16 |[tgz][314u20]<br><br>[tgz][314u18]<br>[tgz][314u16]|[tgz][313u20]<br><br>[tgz][313u18]<br>[tgz][313u16]|<br>[tgz][312u19]<br>[tgz][312u18]<br>[tgz][312u16]|<br>[tgz][311u19]<br>[tgz][311u18]<br>[tgz][311u16]|<br>[tgz][310u19]<br>[tgz][310u18]<br>[tgz][310u16]
RedHat EL7<br>w/ Mesa|[tgz][314rh]<br>[tgz][314rhwm]|[tgz][313rh]<br>[tgz][313rhwm]|[tgz][312rh]<br>[tgz][312rhwm]|[tgz][311rh]<br>[tgz][311rhwm]|[tgz][310rh]<br>[tgz][310rhwm]
Fedora 31<br>27 |[tgz][314f31]<br>|[tgz][313f31]<br>|<br>[tgz][312f27]|<br>[tgz][311f27]|<br>[tgz][310f27]
Debian 10<br>9 |[tgz][314d10]<br>[tgz][314d9]|[tgz][313d10]<br>[tgz][313d9]|<br>[tgz][312d9]|<br>[tgz][311d9]|<br>[tgz][310d9]
Centos 8    |[tgz][314c8]|[tgz][313c8]|[tgz][312c8]|[tgz][311c8]|[tgz][310c8]
Java client |[tgz][314j]|[tgz][313j]|[tgz][312j]|[tgz][311j]|[tgz][310j]
[visit-install][vm1]|[sh][314vi]|[sh][313vi]|[sh][312vi]|[sh][311vi]|[sh][310vi]
[build_visit][vm2] |[sh][314bv]|[sh][313bv]|[sh][312bv]|[sh][311bv]|[sh][310bv]
Source      |[tgz][314stgz]|[tgz][313stgz]|[tgz][312stgz]|[tgz][311stgz]|[tgz][310stgz]
Rel notes<br>Install notes |[html][314rn]<br>[txt][314in]|[html][313rn]<br>[txt][313in]|[html][312rn]<br>[txt][312in]|[html][311rn]<br>[txt][311in]|[html][310rn]<br>[txt][310in]
Checksums<br><br><br>File sizes   |[md5][314md5]<br>[sh1][314sha1]<br>[sh256][314sha256]<br>[txt][314fs]|[md5][313md5]<br>[sh1][313sha1]<br>[sh256][313sha256]<br>[txt][313fs]|[md5][312md5]<br>[sh1][312sha1]<br>[sh256][312sha256]<br>[txt][312fs]|[md5][311md5]<br>[sh1][311sha1]<br>[sh256][311sha256]<br>[txt][311fs]|[md5][310md5]<br>[sh1][310sha1]<br>[sh256][310sha256]<br>[txt][310fs]
Manuals     |[html][314doc]/[pdf][314pdf]|[html][313doc]/[pdf][313pdf]|[html][312doc]/[pdf][312pdf]|[html][311doc]/[pdf][311pdf]|[html][310doc]/[pdf][310pdf]

<!-- 3.1.4 release asset links -->
[3.1.4]: https://github.com/visit-dav/visit/releases/tag/v3.1.4 "All GitHub release assets"
[314w]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3.1.4_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[314wd]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visitdev3.1.4.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[314m1014dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3.1.4.darwin-x86_64-10_14.dmg "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[314m1014tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3.1.4.darwin-x86_64-10_14.tar.gz "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[314m1015dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3.1.4.darwin-x86_64-10_15.dmg "Darwin 10.15, Darwin Kernel Version 19.6.0, clang-1100.0.33.16, MPICH"
[314m1015tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3.1.4.darwin-x86_64-10_15.tar.gz "Darwin 10.15, Darwin Kernel Version 19.6.0, clang-1100.0.33.16, MPICH"
[314u20]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 4.19.76-linuxkit #1 SMP, gcc 9.3"
[314u18]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.19.76-linuxkit #1 SMP, gcc 7.5"
[314u16]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.19.76-linuxkit #1 SMP, gcc 5.4"
[314rh]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[314rhwm]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[314f31]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-fedora27.tar.gz "Fedora 31, 4.19.76-linuxkit #1 SMP, gcc 9.3.1"
[314d9]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-debian9.tar.gz "Debian 9, 4.19.76-linuxkit #1 SMP, gcc 6.3"
[314d10]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-debian10.tar.gz "Debian 10, 4.19.76-linuxkit #1 SMP, gcc 8.3"
[314c8]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3_1_4.linux-x86_64-centos8.tar.gz "CentOS 8, 4.19.76-linuxkit #1 SMP, gcc 8.3.1"
[314j]: https://github.com/visit-dav/visit/releases/download/v3.1.4/jvisit3.1.4.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[314vi]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit-install3_1_4 "Linux installer script needed to install linux binaries"
[314bv]: https://github.com/visit-dav/visit/releases/download/v3.1.4/build_visit3_1_4 "Download *only* this script to build VisIt from sources"
[314stgz]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit3.1.4.tar.gz
[314rn]: ../releases/release-notes-3.1.4
[314in]: https://github.com/visit-dav/visit/releases/download/v3.1.4/INSTALL_NOTES.txt
[314sha256]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[314sha1]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[314md5]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[314fs]: https://github.com/visit-dav/visit/releases/download/v3.1.4/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[314doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.1.4/
[314pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.1.4/pdf/

<!-- 3.1.3 release asset links -->
[3.1.3]: https://github.com/visit-dav/visit/releases/tag/v3.1.3 "All GitHub release assets"
[313w]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3.1.3_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[313wd]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visitdev3.1.3.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[313m1014dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3.1.3.darwin-x86_64-10_14.dmg "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[313m1014tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3.1.3.darwin-x86_64-10_14.tar.gz "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[313u20]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-ubuntu20.tar.gz "Ubuntu 20, 4.19.76-linuxkit #1 SMP, gcc 9.3"
[313u18]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.19.76-linuxkit #1 SMP, gcc 7.5"
[313u16]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.19.76-linuxkit #1 SMP, gcc 5.4"
[313rh]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[313rhwm]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[313f31]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-fedora27.tar.gz "Fedora 31, 4.19.76-linuxkit #1 SMP, gcc 9.3.1"
[313d9]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-debian9.tar.gz "Debian 9, 4.19.76-linuxkit #1 SMP, gcc 6.3"
[313d10]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-debian10.tar.gz "Debian 10, 4.19.76-linuxkit #1 SMP, gcc 8.3"
[313c8]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3_1_3.linux-x86_64-centos8.tar.gz "CentOS 8, 4.19.76-linuxkit #1 SMP, gcc 8.3.1"
[313j]: https://github.com/visit-dav/visit/releases/download/v3.1.3/jvisit3.1.3.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[313vi]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit-install3_1_3 "Linux installer script needed to install linux binaries"
[313bv]: https://github.com/visit-dav/visit/releases/download/v3.1.3/build_visit3_1_3 "Download *only* this script to build VisIt from sources"
[313stgz]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit3.1.3.tar.gz
[313rn]: ../releases/release-notes-3.1.3
[313in]: https://github.com/visit-dav/visit/releases/download/v3.1.3/INSTALL_NOTES.txt
[313sha256]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[313sha1]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[313md5]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[313fs]: https://github.com/visit-dav/visit/releases/download/v3.1.3/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[313doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.1.3/
[313pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.1.3/pdf/

<!-- 3.1.2 release asset links -->
[3.1.2]: https://github.com/visit-dav/visit/releases/tag/v3.1.2 "All GitHub release assets"
[312w]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3.1.2_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[312wd]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visitdev3.1.2.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[312m1014dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3.1.2.darwin-x86_64-10_14.dmg "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[312m1014tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3.1.2.darwin-x86_64-10_14.tar.gz "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[312u19]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-ubuntu19.tar.gz "Ubuntu 19, 4.9.184-linuxkit #1 SMP, gcc 8.3"
[312u18]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.9.184-linuxkit #1 SMP, gcc 7.4"
[312u16]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.9.184-linuxkit #1 SMP, gcc 5.4"
[312rh]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[312rhwm]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[312f27]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-fedora27.tar.gz "Fedora 27, 4.9.184-linuxkit #1 SMP, gcc 7.3.1"
[312d9]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-debian9.tar.gz "Debian 9, 4.9.184-linuxkit #1 SMP, gcc 6.3"
[312d10]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-debian10.tar.gz "Debian 10, 4.19.76-linuxkit #1 SMP, gcc 8.3"
[312c8]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3_1_2.linux-x86_64-centos8.tar.gz "CentOS 8, 4.9.184-linuxkit #1 SMP, gcc 8.2.1"
[312j]: https://github.com/visit-dav/visit/releases/download/v3.1.2/jvisit3.1.2.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[312vi]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit-install3_1_2 "Linux installer script needed to install linux binaries"
[312bv]: https://github.com/visit-dav/visit/releases/download/v3.1.2/build_visit3_1_2 "Download *only* this script to build VisIt from sources"
[312stgz]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit3.1.2.tar.gz
[312rn]: ../releases/release-notes-3.1.2
[312in]: https://github.com/visit-dav/visit/releases/download/v3.1.2/INSTALL_NOTES.txt
[312sha256]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[312sha1]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[312md5]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[312fs]: https://github.com/visit-dav/visit/releases/download/v3.1.2/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[312doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.1.2/
[312pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.1.2/pdf/

<!-- 3.1.1 release asset links -->
[3.1.1]: https://github.com/visit-dav/visit/releases/tag/v3.1.1 "All GitHub release assets"
[311w]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3.1.1_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[311wd]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visitdev3.1.1.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[311m1014dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3.1.1.darwin-x86_64-10_14.dmg "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[311m1014tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3.1.1.darwin-x86_64-10_14.tar.gz "Darwin 10.14, Darwin Kernel Version 18.7.0, clang-1000.11.45.5, MPICH"
[311m1013dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3.1.1.darwin-x86_64-10.13.dmg "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH"
[311m1013tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3.1.1.darwin-x86_64-10.13.tar.gz "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH"
[311u19]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-ubuntu19.tar.gz "Ubuntu 19, 4.9.184-linuxkit #1 SMP, gcc 8.3"
[311u18]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.9.184-linuxkit #1 SMP, gcc 7.4"
[311u16]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.9.184-linuxkit #1 SMP, gcc 5.4"
[311rh]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[311rhwm]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[311f27]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-fedora27.tar.gz "Fedora 27, 4.9.184-linuxkit #1 SMP, gcc 7.3.1"
[311d9]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-debian9.tar.gz "Debian 9, 4.9.184-linuxkit #1 SMP, gcc 6.3"
[311c8]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3_1_1.linux-x86_64-centos8.tar.gz "CentOS 8, 4.9.184-linuxkit #1 SMP, gcc 8.2.1"
[311j]: https://github.com/visit-dav/visit/releases/download/v3.1.1/jvisit3.1.1.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[311vi]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit-install3_1_1 "Linux installer script needed to install linux binaries"
[311bv]: https://github.com/visit-dav/visit/releases/download/v3.1.1/build_visit3_1_1 "Download *only* this script to build VisIt from sources"
[311stgz]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit3.1.1.tar.gz
<!--
[311rn]: https://wci.llnl.gov/simulation/computer-codes/visit/releases/release-notes-3.1.1
[311in]: https://github.com/visit-dav/visit/releases/download/v3.1.1/INSTALL_NOTES.txt
Below is using a special github feature, htmlpreview.github.io to render the html from the source repo
[311rn]: https://htmlpreview.github.io/?https://raw.githubusercontent.com/visit-dav/visit/3.1RC/src/resources/help/en_US/relnotes3.1.0.html
-->
[311rn]: ../releases/release-notes-3.1.1
[311in]: https://github.com/visit-dav/visit/blob/3.1RC/src/INSTALL_NOTES
[311sha256]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit_sha256_checksums.txt "List of all download file names and their sha256 checksums"
[311sha1]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit_sha1_checksums.txt "List of all download file names and their sha1 checksums"
[311md5]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit_md5_checksums.txt "List of all download file names and their md5 checksums"
[311fs]: https://github.com/visit-dav/visit/releases/download/v3.1.1/visit_filesizes.txt "List of all download file names and their sizes in bytes"
[311doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.1.1/
[311pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.1.1/pdf/

<!-- 3.1.0 release asset links -->
[3.1.0]: https://github.com/visit-dav/visit/releases/tag/v3.1.0 "All GitHub release assets"
[310w]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3.1.0_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[310wd]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visitdev3.1.0.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[310m1013dmg]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3.1.0.darwin-x86_64-10.13.dmg "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[310m1013tgz]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3.1.0.darwin-x86_64-10.13.tar.gz "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[310u19]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-ubuntu19.tar.gz "Ubuntu 19, 4.9.184-linuxkit #1 SMP, gcc 8.3"
[310u18]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.9.184-linuxkit #1 SMP, gcc 7.4"
[310u16]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.9.184-linuxkit #1 SMP, gcc 5.4"
[310rh]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[310rhwm]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[310f27]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-fedora27.tar.gz "Fedora 27, 4.9.184-linuxkit #1 SMP, gcc 7.3.1"
[311rn]: ../releases/release-notes-3.1.1
[310d9]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-debian9.tar.gz "Debian 9, 4.9.184-linuxkit #1 SMP, gcc 6.3"
[310c8]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3_1_0.linux-x86_64-centos8.tar.gz "CentOS 8, 4.9.184-linuxkit #1 SMP, gcc 8.2.1"
[310j]: https://github.com/visit-dav/visit/releases/download/v3.1.0/jvisit3.1.0.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[310vi]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit-install3_1_0 "Linux installer script needed to install linux binaries"
[310bv]: https://github.com/visit-dav/visit/releases/download/v3.1.0/build_visit3_1_0 "Download *only* this script to build VisIt from sources"
[310stgz]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit3.1.0.tar.gz
[310rn]: ../releases/release-notes-3.1.0
[310in]: https://github.com/visit-dav/visit/releases/download/v3.1.0/INSTALL_NOTES.txt
[310sha256]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit_sha256_checksums.txt
[310sha1]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit_sha1_checksums.txt
[310md5]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit_md5_checksums.txt
[310fs]: https://github.com/visit-dav/visit/releases/download/v3.1.0/visit_filesizes.txt
[310doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.1.0/
[310pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.1.0/pdf/

### Series 3.0

* Links to checksums and file sizes are provided for confirming download integrity.
* Hover over a link to reveal additional details about a download.
* For linux, the [`visit-install`][vm2] script is needed to complete an *install*.

Date | Sep 2019 | Jul 2019 | Apr 2019
---:|:---:|:---:|:---:
Version     |[3.0.2] | [3.0.1] | [3.0.0]
Windows     |[use][302w]/[dev][302wd]|[use][301w]/[dev][301wd]|[use][300w]/[dev][300wd]
OSX 10.13   |[dmg][302m1013dmg]/[tgz][302m1013tgz]|[dmg][301m1013dmg]/[tgz][301m1013tgz]|[dmg][300m1013dmg]/[tgz][300m1013tgz]
Ubuntu 19   |[tgz][302u19]|[tgz][301u19]|[tgz][300u19]
Ubuntu 18   |[tgz][302u18]|[tgz][301u18]|[tgz][300u18]
Ubuntu 16   |[tgz][302u16]|[tgz][301u16]|[tgz][300u16]
RedHat EL 7 |[tgz][302rh]|[tgz][301rh]|[tgz][300rh]
RedHat EL 7 w/ Mesa |[tgz][302rhwm]|[tgz][301rhwm]|[tgz][300rhwm]
Fedora 27   |[tgz][302f27]|[tgz][301f27]|[tgz][300f27]
Debian 9    |[tgz][302d9]|[tgz][301d9]|[tgz][300d9]
Centos 8    |[tgz][302c8]|[tgz][301c8]|[tgz][300c8]
Java client |[tgz][302j]|[tgz][301j]|[tgz][300j]
[visit-install][vm1]|[sh][302vi]|[sh][301vi]|[sh][300vi]
[build_visit][vm2]|[sh][302bv]|[sh][301bv]|[sh][300bv]
Source      |[tgz][302stgz]|[tgz][301stgz]|[tgz][300stgz]
Release notes |[html][302rn]|[html][301rn]|[html][300rn]
Install notes |[txt][302in]|[txt][301in]|[txt][300in]
Checksums   |[md5][302md5]/[sh1][302sha1]/[sh256][302sha256]|[md5][301md5]/[sh1][301sha1]/[sh256][301sha256]|[md5][300md5]/[sh1][300sha1]/[sh256][300sha256]
File sizes  |[txt][302fs]|[txt][301fs]|[txt][300fs]
Manuals     |[html][302doc]/[pdf][302pdf]|[html][301doc]/[pdf][301pdf]|[html][300doc]/[pdf][300pdf]

<!-- 3.0.2 release asset links -->
[3.0.2]: https://github.com/visit-dav/visit/releases/tag/v3.0.2 "All GitHub release assets"
[302w]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3.0.2_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[302wd]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visitdev3.0.2.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[302m1013dmg]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3.0.2.darwin-x86_64-10.13.dmg "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[302m1013tgz]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3.0.2.darwin-x86_64-10.13.tar.gz "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[302u19]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-ubuntu19.tar.gz "Ubuntu 19, 4.9.184-linuxkit #1 SMP, gcc 8.3"
[302u18]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.9.184-linuxkit #1 SMP, gcc 7.4"
[302u16]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.9.184-linuxkit #1 SMP, gcc 5.4"
[302rh]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[302rhwm]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[302f27]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-fedora27.tar.gz "Fedora 27, 4.9.184-linuxkit #1 SMP, gcc 7.3.1"
[302d9]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-debian9.tar.gz "Debian 9, 4.9.184-linuxkit #1 SMP, gcc 6.3"
[302c8]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3_0_2.linux-x86_64-centos8.tar.gz "CentOS 8, 4.9.184-linuxkit #1 SMP, gcc 8.2.1"
[302j]: https://github.com/visit-dav/visit/releases/download/v3.0.2/jvisit3.0.2.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[302vi]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit-install3_0_2 "Linux installer script needed to install linux binaries"
[302bv]: https://github.com/visit-dav/visit/releases/download/v3.0.2/build_visit3_0_2 "Download *only* this script to build VisIt from sources"
[302stgz]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit3.0.2.tar.gz
[302rn]: ../releases/release-notes-3.0.2
[302in]: https://github.com/visit-dav/visit/releases/download/v3.0.2/INSTALL_NOTES.txt
[302sha256]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit_sha256_checksums.txt
[302sha1]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit_sha1_checksums.txt
[302md5]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit_md5_checksums.txt
[302fs]: https://github.com/visit-dav/visit/releases/download/v3.0.2/visit_filesizes.txt
[302doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.0.2/
[302pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.0.2/pdf/

<!-- 3.0.1 release asset links -->
[3.0.1]: https://github.com/visit-dav/visit/releases/tag/v3.0.1 "All GitHub release assets"
[301w]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3.0.1_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[301wd]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visitdev3.0.1.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[301m1013dmg]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3.0.1.darwin-x86_64-10.13.dmg "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[301m1013tgz]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3.0.1.darwin-x86_64-10.13.tar.gz "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[301u19]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-ubuntu19.tar.gz "Ubuntu 19, 4.9.184-linuxkit #1 SMP, gcc 8.3"
[301u18]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.9.184-linuxkit #1 SMP, gcc 7.4"
[301u16]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.9.184-linuxkit #1 SMP, gcc 5.4"
[301rh]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[301rhwm]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[301f27]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-fedora27.tar.gz "Fedora 27, 4.9.184-linuxkit #1 SMP, gcc 7.3.1"
[301d9]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-debian9.tar.gz "Debian 9, 4.9.184-linuxkit #1 SMP, gcc 6.3"
[301c8]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3_0_1.linux-x86_64-centos8.tar.gz "CentOS 8, 4.9.184-linuxkit #1 SMP, gcc 8.2.1"
[301j]: https://github.com/visit-dav/visit/releases/download/v3.0.1/jvisit3.0.1.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[301vi]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit-install3_0_1 "Linux installer script needed to install linux binaries"
[301bv]: https://github.com/visit-dav/visit/releases/download/v3.0.1/build_visit3_0_1 "Download *only* this script to build VisIt from sources"
[301stgz]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit3.0.1.tar.gz
[301rn]: ../releases/release-notes-3.0.1
[301in]: https://github.com/visit-dav/visit/releases/download/v3.0.1/INSTALL_NOTES.txt
[301sha256]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit_sha256_checksums.txt
[301sha1]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit_sha1_checksums.txt
[301md5]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit_md5_checksums.txt
[301fs]: https://github.com/visit-dav/visit/releases/download/v3.0.1/visit_filesizes.txt
[301doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.0.1/
[301pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.0.1/pdf/

<!-- 3.0.0 release asset links -->
[3.0.0]: https://github.com/visit-dav/visit/releases/tag/v3.0.0 "All GitHub release assets"
[300w]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3.0.0_x64.exe "Windows 10/8/7, 64-bit Visual Studio 2017"
[300wd]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visitdev3.0.0.exe "Windows 10/8/7 for VisIt development, 64-bit Visual Studio 2017"
[300m1013dmg]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3.0.0.darwin-x86_64-10.13.dmg "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[300m1013tgz]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3.0.0.darwin-x86_64-10.13.tar.gz "Darwin 10.13, Darwin Kernel Version 17.7.0, clang-900.39.2, MPICH (Works on Mac OS X 10.13 and later.)"
[300u19]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-ubuntu19.tar.gz "Ubuntu 19, 4.9.184-linuxkit #1 SMP, gcc 8.3"
[300u18]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-ubuntu18.tar.gz "Ubuntu 18, 4.9.184-linuxkit #1 SMP, gcc 7.4"
[300u16]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-ubuntu16.tar.gz "Ubuntu 16, 4.9.184-linuxkit #1 SMP, gcc 5.4"
[300rh]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-rhel7.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5"
[300rhwm]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-rhel7-wmesa.tar.gz "Redhat Enterprise Linux 7.5, 4.18.9-1.el7.elrepo.x86_64 #1 SMP, gcc 4.8.5 (Includes Mesa support for rendering without a display. Only use on servers without a display.)"
[300f27]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-fedora27.tar.gz "Fedora 27, 4.9.184-linuxkit #1 SMP, gcc 7.3.1"
[300d9]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-debian9.tar.gz "Debian 9, 4.9.184-linuxkit #1 SMP, gcc 6.3"
[300c8]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3_0_0.linux-x86_64-centos8.tar.gz "CentOS 8, 4.9.184-linuxkit #1 SMP, gcc 8.2.1"
[300j]: https://github.com/visit-dav/visit/releases/download/v3.0.0/jvisit3.0.0.tar.gz "VisIt client only: Java(TM) SE Runtime Environment (build 1.6.0_161-b13) Java HotSpot(TM) 64-Bit Server VM (build 20.161-b13, mixed mode)"
[300vi]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit-install3_0_0 "Linux installer script needed to install linux binaries"
[300bv]: https://github.com/visit-dav/visit/releases/download/v3.0.0/build_visit3_0_0 "Download *only* this script to build VisIt from sources"
[300stgz]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit3.0.0.tar.gz
[300rn]: ../releases/release-notes-3.0.0
[300in]: https://github.com/visit-dav/visit/releases/download/v3.0.0/INSTALL_NOTES.txt
[300sha256]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit_sha256_checksums.txt
[300sha1]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit_sha1_checksums.txt
[300md5]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit_md5_checksums.txt
[300fs]: https://github.com/visit-dav/visit/releases/download/v3.0.0/visit_filesizes.txt
[300doc]: https://visit-sphinx-github-user-manual.readthedocs.io/en/v3.0.0/
[300pdf]: https://visit-sphinx-github-user-manual.readthedocs.io/_/downloads/en/v3.0.0/pdf/
