---
title: Yokohama Patch 3 Hotfix 1
description: The Yokohama Patch 3 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-05-15"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 3 Hotfix 1

The Yokohama Patch 3 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 05-09-2025\_1217

    Build tag: glide-yokohama-12-18-2024\_\_patch3-hotfix1-05-07-2025


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

Edge Encryption

 PRB1887439

</td><td>

In Yokohama, when a user goes through edge proxy with a home page that includes encoded characters such as %2f as a re-direction result after login, a 400 error occurs

</td><td>

When the user's default home page contains encoded characters, or is redirected to a URL with encoded characters, edge will throw the 400 error blocking access to the home page.

</td><td>

1.  Use an edge proxy in Yokohama.
2.  Add abel.tuter as a workspace\_admin and workspace\_user.
3.  Log in as abel.tuter through edge.
4.  Navigate to **Preferences**.
5.  Set the home page to **Default**.
6.  Log out.
7.  Log in as abel.tuter through edge again.

 Observe the http 400 error.

</td></tr><tr><td>

Flow Engine

 PRB1888071

</td><td>

Deserialization issue with 'Make a decision'

</td><td>

When upgrading from a Washington DC to Yokohama instance, flow executions created with **Decisions** in both families don't resume and result in an error.

</td><td>

1.  Open a Washington DC instance.
2.  Create waiting flows with **Decisions**.
3.  Upgrade to Yokohama.
4.  Create new flow executions on Yokohama.
5.  Create some error flows by processing a few waiting flows.
6.  Run a fix script for one or two flow executions.
7.  Create new flow executions on Yokohama.
8.  Upgrade the Yokohama instance.
9.  Open the Yokohama flows, the Washington DC waiting flows, and the fixed flows the by script.

 Expected behavior: Flows should resume and operation view should work.

 Actual behavior: Notice the error, 'Caused by: java.lang.IllegalState Exception: Cannot build UnsafeObject RefOrValue, some of required attributes are not set \[isRef\]'.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

