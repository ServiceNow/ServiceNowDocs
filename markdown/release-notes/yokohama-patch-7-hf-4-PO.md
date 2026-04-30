---
title: Yokohama Patch 7 Hotfix 4
description: The Yokohama Patch 7 Hotfix 4 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-10-15"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 7 Hotfix 4

The Yokohama Patch 7 Hotfix 4 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-09-2025\_1925

    Build tag: glide-yokohama-12-18-2024\_\_patch7-hotfix4-10-07-2025


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

Analytics Data API

 PRB1945218

</td><td>

Memory leak of JSON serializer in multivis API

</td><td>

Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td><td>

1.  Create a dashboard.
2.  Add a tab and add 50 identical single score vis:
    -   Source: incident.
    -   Condition: sys\_id is empty.
3.  Duplicate the tab 9 times so there are 500 visualizations in total.
4.  Disable the property 'com.snc.dashboard.streaming.enabled'.
5.  Stop the instance and start again, but don't access the instance in the browser.
6.  Use VisualVM to capture the heapdump.
7.  Search for 'IntegerDateSerializer' in the object list.
    -   Observe that there are 0 results.
8.  Access the dashboard created in step 1.
9.  Go over all 10 tabs.
10. Use VisualVM to capture the heapdump.
11. Search for 'IntegerDateSerializer'.
    -   Observe that there are ~500 results.
12. Repeat steps 8 through 11 \(get the heapdump and search\).

 Observe that there are ~1000 results. Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td></tr><tr><td>

OneExtend

 PRB1944861

</td><td>

Revert NASK licensing charge by token to not include input tokens

</td><td>

The assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 7 Hotfix 3](yokohama-patch-7-hf-3-PO.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

