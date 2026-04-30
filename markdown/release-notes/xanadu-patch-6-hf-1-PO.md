---
title: Xanadu Patch 6 Hotfix 1
description: The Xanadu Patch 6 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-03-31"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 6 Hotfix 1

The Xanadu Patch 6 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: \_03-28-2025\_0050

    Build tag: glide-xanadu-07-02-2024\_\_patch6-hotfix1-03-24-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

UI Form Administration

 PRB1868782

</td><td>

While composing an email in Vendor Operations, the cursor occasionally jumps, making it difficult to continue typing

</td><td>

When the user types rapidly, the position event is triggered multiple times, resulting in the cursor unexpectedly jumping to the end.

</td><td>

1.  On a base instance, enable email reply recommendations on any table.
2.  Add a line to the end of the email's last line.
3.  Start typing in the first line quickly.

 Observe that the cursor jumps to the end of the file.

</td></tr><tr><td>

UX Framework

 PRB1869757

</td><td>

There is a performance degradation while loading the home page on Xanadu

</td><td>

When the system property glide.ux.user\_criteria\_enabled = true, there is a performance degradation between Washington DC and Xanadu upon loading the home page.

</td><td>

1.  On Washington DC Instance, set glide.ux.user\_criteria\_enabled to true on a Washington DC instance.
2.  Navigate to the instance home page.
3.  Measure the page load times.

Notice that the average page load time is less than five seconds.

4.  On a Xanadu Instance, set glide.ux.user\_criteria\_enabled to true.
5.  Navigate to the instance home page.
6.  Measure the page load times.

Notice that the average page load time is between eight and ten seconds.


 Observe the performance degradation between the two versions when the system property glide.ux.user\_criteria\_enabled is set to true.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5 Hotfix 1](xanadu-patch-5-hf-1-PO.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1774457)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

