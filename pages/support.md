---
layout: page
title: "Support"
meta_title: "Contacting us and getting help"
header:
    image_fullwidth: "llnl_machine.jpg"
permalink: "/support/"
---

* [Methods of Contact for Support](#methods-of-contact-for-support)
* [Supported Platforms and Operating Systems](#supported-platforms-and-operating-systems)

## Methods of Contact for Support

Methods of contact we offer differ in *requirements* and *privacy* level. In
addition, while we try to accommodate a variety of means of *initial contact*,
any issues involving *ongoing dialog* must use only a *preferred* method of
communication. Please read about our
[communication policies](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/dev_manual/SiteReliabilityEngineering.html#supported-methods-of-contact) for more details.

### Options for contacting us

Method | Privacy | Requirements | Preferred
--- | --- | ---
[GitHub issue][gh1]    | [None] | Must have a (free) [GitHub account][gh2]|Yes
[General email][ge1]   | [None] | Must [subscribe to visit-users][ge2] email list|Yes
[ASC email][ae1]       | [Some] | Must be ASC related work | No
[SciDAC email][se1]    | [Some] | Must be SciDAC related work | No
[Developer email][de1] | [Some] | Must be a VisIt developer & [subscribe<br>to visit-developers][de2] email list | Yes
[Hotline call][hc1]    | [Most] | Must be LLNL employee | No
[MS Teams Chat][mst]   | [Some] | Must be member of [VisIt channel](mst) | No 
Announcements | N/A    | Must [subscribe][An1] to get<br>important/release announcements | N/A

### More details

More recently, we have been
[trying get away from plain ole' email](https://github.com/visit-dav/live-customer-response/wiki/How-the-new-GitHub-visit-users-Email-Integration-Works)
in favor of GitHub issues and for this reason would prefer users contact
us through our [GitHub issue tracker][gh1] whenever possible.

In general, coverage is during normal West Coast business hours, 8am-12pm and
1-5pm (GMT-8, San Francisco time zone), Monday through Friday excluding
[LLNL holidays](https://supplychain.llnl.gov/poattach/pdf/llnl_holidays.pdf)
and response time may be as much as four hours due to team members multi-tasking
among many responsibilities.

If you are so inclined, we welcome you to read more about the VisIt project's
[Site Reliability Engineering](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/dev_manual/SiteReliabilityEngineering.html)
processes to understand how we aim to respond to inquiries.

## Supported Platforms and Operating Systems

Various VisIt developers routinely develop and run VisIt on Windows 10,
macOS 10.14/10.15 and Red Hat Enterprise Linux (RHEL). This means we 
are able reproduce bugs and test work-arounds and fixes reported on these
platforms and in general provide the highest quality of support services.

We do make an effort to provide pre-compiled binaries for other variants of
Linux. However, because we do not routinely develop or test on these platforms,
we are not able to provide the same level of support for them. We welcome
help from the community in supporting these platforms. When encountering issues
with these binaries, you may likely get faster resolution by first building VisIt
from sources using the
[`build_visit`](https://visit-sphinx-github-user-manual.readthedocs.io/en/develop/gui_manual/Building/index.html?highlight=build_visit)
script. And, if doing so does indeed resolve the issues you encountered, please
let us know your build recipe so we can improve our binaries.

[gh1]: https://github.com/visit-dav/live-customer-response/issues/new?assignees=&labels=&template=customer-response.md&title= "Submit an issue on GitHub"
[gh2]: https://github.com/join?source=header-home
[ge1]: mailto:visit-users@ornl.gov "Start an email to visit-users list"
[ge2]: https://elist.ornl.gov/mailman/listinfo/visit-users "Subscribe to visit-users email list"
[ae1]: mailto:visit-help-asc@ornl.gov "Start an email to visit-help-asc list"
[se1]: mailto:visit-help-scidac@ornl.gov "Start an email to visit-help-scidac list"
[hc1]: tel:42847 "Initiate a call to 42-Vis"
[de1]: mailto:visit-developers@ornl.gov "Start an email to visit-developers list"
[de2]: https://elist.ornl.gov/mailman/listinfo/visit-developers "Subscribe to visit-developers email list"
[An1]: https://elist.ornl.gov/mailman/listinfo/visit-announce "Subscribe to visit-announce email list"
[mst]: https://teams.microsoft.com/l/team/19%3af2ed7be3682d40d1b8e038744e500a09%40thread.skype/conversations?groupId=70162982-9587-4bcc-ad53-20178c76fe11&tenantId=a722dec9-ae4e-4ae3-9d75-fd66e2680a63

[None]: #none-privacy "World readable and discoverable"
[Some]: #some-privacy "Not archived or discoverable on any server"
[Most]: #most-privacy "Same privacy as any ordinary telephone call"

##### None privacy

All communications, including any attached images and data files are discoverable
and readable by anyone, anywhere in the world with a web browser.

##### Some privacy

All communications are *direct* emails (e.g. not an email list) to project members
and are not archived or discoverable on any email storage servers.

##### Most privacy

The same level of privacy as any ordinary telephone call.
