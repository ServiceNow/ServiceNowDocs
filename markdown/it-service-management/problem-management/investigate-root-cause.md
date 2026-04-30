---
title: Investigate root cause of a problem
description: Identify the root cause of the problem to analyze, track, and resolve recurring incidents permanently.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing Problems, Problem Management, IT Service Management]
---

# Investigate root cause of a problem

Identify the root cause of the problem to analyze, track, and resolve recurring incidents permanently.

## Before you begin

Role required: problem\_admin, problem\_coordinator, problem\_manager, or admin

## About this task

Activate the Problem Management Best Practice — Madrid — State Model \(com.snc.best\_practice.problem.madrid.state\_model\) to get the new best practice states and guided actions to navigate the life cycle of a problem. For details, see [Activate Problem Management Best Practice — Madrid — State Model](act-pm-best-prac-madrid-state-mod.md).

![root cause analysis state](../image/pm-fix.png "Root cause analysis")

## Procedure

1.  You can perform any one of the following tasks.

<table id="choicetable_v1k_dbk_wfb"><thead><tr><th align="left" id="d214902e83">

Option

</th><th align="left" id="d214902e86">

Actions to be taken

</th></tr></thead><tbody><tr><td id="d214902e92">

**Investigate the problem**

</td><td>

-   If you are the subject matter expert for this problem area, carry out the investigation and provide the cause notes and fix notes on this problem.
-   If you are not the subject matter expert and you want help with the investigation, create a problem task of type root cause analysis and assign that to the relevant team. Once the subject matter expert has completed the problem task, then you can manually copy the cause notes and proposed fix from the problem task to this problem.
 For more information about creating a problem task, see [Create a problem task](create-problem-task.md).

</td></tr><tr><td id="d214902e120">

**If you can resolve the problem**

</td><td>

Click **Fix**. The problem state changes to **Fix in Progress**. You can then create a new Change Request or link to an existing Change Request to apply a permanent fix to the problem. **Note:** Notification is sent to the problem coordinator, who is assigned to the Problem, when all the related Change Requests are completed or canceled.

</td></tr><tr><td id="d214902e138">

**If you acknowledge the problem but there is no permanent resolution to the problem**

</td><td>

Click **Accept Risk**. The problem directly enters the **Closed** or **Resolved** state with the **Resolution code** as **Risk accepted**.**Note:** Whether the problem enters the **Closed** state or the **Resolved** state, depends on the property **Accept Risk moves the Problem to Closed state instead of Resolved state** \(**problem.acceptrisk.move\_to\_closed**\).

</td></tr><tr><td id="d214902e178">

**If you decide to reanalyze the problem**

</td><td>

Click **Re-analyze**. The problem opens for reanalysis and the state is changed to **Root Cause Analysis**.

</td></tr></tbody>
</table>    If you had created any known error article for this problem or any similar problem, you can add the reference of that article in the **Primary Known Error article** field.

    **Note:** The **Primary Known Error article** field is available only when you activate the Problem Management Best Practice — Madrid — Knowledge Integration plugin \(com.snc.best\_practice.problem.madrid.knowledge\).


## What to do next

You can resolve and complete the problem. You can also create a change request to implement a fix for the problem.

**Parent Topic:**[Managing Problems](../concept/problem-mgmt-lifecycle.md)

