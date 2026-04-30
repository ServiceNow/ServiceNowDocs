---
title: Yokohama Patch 7 Hotfix 5
description: The Yokohama Patch 7 Hotfix 5 release contains fixes to these problems.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-20"
reading_time_minutes: 3
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 7 Hotfix 5

The Yokohama Patch 7 Hotfix 5 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-16-2025\_1204

    Build tag: glide-yokohama-12-18-2024\_\_patch7-hotfix5-11-11-2025


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

History Set

 PRB1892171

 [KB2565900](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2565900)

</td><td>

setJournalEntry\(data, 'user name'\) API doesn't work as expected

</td><td>

When the API setJournalEntry\(data, 'user name'\)​ is used, the sys\_audit.user correctly reflects the user passed into the API, but sys\_created\_by captures the user that's currently logged in.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1936445

</td><td>

Instance is getting 'session out' because the AI user doesn't work properly

</td><td>

During the agentic workflow, the instance calls the image processor agent and asks to upload an image. After some time, the session times out. This only happens for the AI user; it works correctly for the dynamic user.

</td><td>

1.  Log in to an instance.
2.  Navigate to AI Studio.
3.  Select **Create Work Order**.
4.  Save it.
5.  Try to create a work order with a description.
6.  Say 'yes' to 'create a work order'.
7.  When it asks to upload an image, select the link.
8.  Attach an image from local.

 Expected behavior: It doesn't session out. Ideally, it should attach the image to the work order.

 Actual behavior: The instance says 'session out' and logs out the user. Every time the user attempts to log in again, it immediately logs out.

</td></tr><tr><td>

Virtual Agent

 PRB1947698

</td><td>

Only one agentic workflow executes successfully when the same trigger fires simultaneously

</td><td>

When a workflow trigger fires simultaneously multiple times, only one of the resulting agentic workflows executes successfully. The other workflows terminate immediately with an error indicating that no session ID could be found. Each trigger correctly creates a new execution plan and a new conversation record, but only one conversation proceeds, while the others fail at the start.

</td><td>

1.  Create the agentic workflow named 'Test multiple case executions'.
2.  Select three or more case records and update them simultaneously so that the trigger fires for all at once.
3.  Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error 'No session ID found'.

 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 7 Hotfix 4](yokohama-patch-7-hf-4-PO.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

