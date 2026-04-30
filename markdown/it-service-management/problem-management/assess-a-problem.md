---
title: Assess a problem
description: Assess a problem to determine whether the problem requires a thorough investigation.
locale: en-US
release: yokohama
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing Problems, Problem Management, IT Service Management]
---

# Assess a problem

Assess a problem to determine whether the problem requires a thorough investigation.

## Before you begin

-   Role required: admin, problem\_admin, problem\_manager, or problem\_coordinator
-   Activate the Problem Management Best Practice — Madrid — State Model \(com.snc.best\_practice.problem.madrid.state\_model\) to get the new best practice states and guided actions to navigate the lifecycle of a problem. For details, see [Activate Problem Management Best Practice — Madrid — State Model](act-pm-best-prac-madrid-state-mod.md).

## About this task

Assessing a problem involves analyzing the scale and extent of the problem, as well as its cause and effect.

## Procedure

1.  Click **Assess** and fill the mandatory fields.

    ![assess state](../image/pm-confirm.png)

    After assessing the problem, you can perform any one of the following actions:

<table id="choicetable_fnv_jzj_wfb"><thead><tr><th align="left" id="d110236e96">

Option

</th><th align="left" id="d110236e99">

Action to be taken

</th></tr></thead><tbody><tr><td id="d110236e105">

**If the problem is valid and requires a resolution**

</td><td>

Click **Confirm**.

</td></tr><tr><td id="d110236e117">

**If there is an existing problem with similar issue**

</td><td>

Click **Mark Duplicate**.**Note:**

-   When you mark a problem as duplicate, the related records from the duplicate problem are moved to the existing problem.
-   The **List of related task records \(comma-separated\) to move over when a problem is marked as a duplicate of another** \(**problem.duplicate.records\_to\_move**\) problem management property controls the related records that are copied from the existing to the original problem.


</td></tr><tr><td id="d110236e145">

**If the problem is not a valid problem**

</td><td>

Click **Cancel**.

</td></tr></tbody>
</table>
## What to do next

After you confirm that the problem needs investigation and a resolution, the problem enters the **Root Cause Analysis** state.

**Parent Topic:**[Managing Problems](../concept/problem-mgmt-lifecycle.md)

