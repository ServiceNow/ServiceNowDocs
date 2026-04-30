---
title: Yokohama Patch 7 Hotfix 1
description: The Yokohama Patch 7 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-09-17"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 7 Hotfix 1

The Yokohama Patch 7 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 09-09-2025\_1515

    Build tag: glide-yokohama-12-18-2024\_\_patch7-hotfix1-09-09-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

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

Mobile Platform

 PRB1916821

</td><td>

The prefetch logic for the parameter screen is broken when using scripted variables

</td><td>

When using scripted variables, the prefetch logic for the parameter screen is broken. As a result, the input form screen contains an empty input

</td><td>

Scenario 1:

 1.  Create a button with an input form screen.
2.  Add an input and a scripted variable to the input form screen.
3.  Make the script of the scripted variable execute longer than ten milliseconds.
4.  Auto-fill the input with the scripted variable.
5.  Add the button to the 'Navigation' section.
6.  In the online mode, select the button.

 Expected behavior: The input form screen contains the input with the auto-filled value.

 Actual behavior: The input form screen contains an empty input.

 Scenario 2:

 1.  Provision an instance with the following applications installed: app-wsd-core, app-wsd-reservation, app-wsd-mobile, and app-wsd-space-mgmt.
2.  Log in to the instance using the requestor mobile application.
3.  Select the top menu.
4.  Create a new reservation with the building and floor.
5.  Open the 'My Reservations' list screen.
6.  Swipe an item.
7.  Select the **Edit** button.
8.  View the input form.

 Expected behavior: The building input is prefilled with the selected floor.

 Actual behavior: The building input is empty. This problem occurs because the building or floor calculation occasionally times out and is skipped. In the previous logic, the prefetch mechanism was used for evaluation.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

