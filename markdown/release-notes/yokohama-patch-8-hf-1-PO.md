---
title: Yokohama Patch 8 Hotfix 1
description: The Yokohama Patch 8 Hotfix 1 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-10-29"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 8 Hotfix 1

The Yokohama Patch 8 Hotfix 1 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-26-2025\_2315

    Build tag: glide-yokohama-12-18-2024\_\_patch8-hotfix1-10-15-2025


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

Access Control

 PRB1893600

 [KB2178333](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2178333)

</td><td>

RecordFamilyResolver. archiveTable HasACLTerms needs more optimization

</td><td>

Performance issues with reports on customer instances with a big number of archive tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1928872

</td><td>

The CanReadRepo class encounters a Concurrent Modification Exception

</td><td>

This concurrency issue arises because the class uses a HashMap, which is not thread-safe. The HashMap should be replaced with a ConcurrentHashMap to ensure thread-safe operations and prevent the exception.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1639714

</td><td>

Alerts on an Application Service have empty PRCs

</td><td>

Alerts on an Application Service appear in the list of 'Impacted Services/CIs' of some change request. These alerts have empty PRCs and they have only one change request instead of two.

</td><td>

1.  Define the Manual Application Service.
2.  Define the Change Request for the Application Service.
3.  Send the event to some CI of the Application Service.
4.  Open the generated alert.
5.  Navigate to the PRC.
    -   Observe that the alert has the PRC 'Change on Application Service.'
6.  Send the event to the Application Service.
7.  Open the generated alert.
8.  Navigate to the PRC.
    -   Observe that the alert has the PRC 'Change on Application Service.'
9.  Create another change request on a different CI.
10. Add the defined Application Service to the list of Impacted CIs of the change request.
11. Send the event to the Application Service.
12. Open the generated alert.
13. Navigate to the PRC.

 Observe that the alert has only one change request, but it should have two.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 8](yokohama-patch-8.md)
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

