---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: pres_movie_b_smaller_banner_ezgif.gif
widget1:
  title: "Why use VisIt?"
  url: '/about/'
  text: '= Proven [scaling](./visit-top-50) to &gt;10<sup>12</sup> zone meshes.<br/>= Windows, Mac, <a href="" title="Unbuntu, Centos, Debian, RedHat, Fedora">, 5+ Linux distros.</a><br/>= Free, <a href="https://github.com/visit-dav/visit/blob/develop/LICENSE">BSD Open Source</a>.<br/>= Reads 130+ <a href="https://www.visitusers.org/index.php?title=Detailed_list_of_file_formats_VisIt_supports">File Formats</a>.<br/>= Supported on many <a href="https://science.osti.gov/User-Facilities/User-Facilities-at-a-Glance/ASCR">LCFs</a>'
  video: '<a href="#" data-reveal-id="videoModal"><img src="images/wing_tip_streamlines_thumb.png" width="303" align="middle"/></a>'
widget2:
  title: "Download Now"
  url: 'https://github.com/visit-dav/visit'
  image: widget-github-303x182.jpg
  text: 'Get the [latest release](./releases-as-tables/#latest) to start visualizing and analyzing your data today. Or, download the <a href="https://github.com/visit-dav/visit/releases/latest/download/build_visit3_1_3">latest build_visit</a> script to build a custom version. Please <a href="https://github.com/visit-dav/live-customer-response/issues/new?assignees=&labels=&template=customer-response.md&title=">share a comment</a> with us about your experiences with VisIt.'
widget3:
  title: "What's new?"
  url: '/science/ShockPhysics'
  image: gallery-00b.png
  text: 'Learn about recent releases, <a href="https://github.com/visit-dav/visit/milestones">plans for upcomming releases</a>, <a href="https://github.com/visit-dav/visit/branches/active">works in progress</a> and other stuff about VisIt, its related technologies and visualization and data analysis in general.'
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
  <iframe width="1280" height="720" src="https://www.youtube.com/embed/aRV5etrNlAQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
