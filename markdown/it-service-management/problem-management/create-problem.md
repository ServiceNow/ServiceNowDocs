---
title: Create a problem \(legacy\)
description: A problem is a cause of one or more incidents. Create a problem to identify the root cause of the incidents and try to prevent them from happening again.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a problem, Managing Problems, Problem Management, IT Service Management]
---

# Create a problem \(legacy\)

A problem is a cause of one or more incidents. Create a problem to identify the root cause of the incidents and try to prevent them from happening again.

## Before you begin

Role required: itil

## Procedure

1.  Create the problem with one of these options.

<table id="choicetable_agp_ckc_3t"><tbody><tr><td id="d247431e54">

**From the Problem module**

</td><td>

Navigate to **Problem** &gt; **Create New**.

</td></tr><tr><td id="d247431e72">

**From an incident**

</td><td>

1.  Open the incident.
2.  On the context menu, click **Create Problem**.


</td></tr></tbody>
</table>2.  Complete the form, as appropriate.

    For a description of the field values, see [Legacy Problem form](../concept/legacy-problem-form.md).

3.  To enter work notes for the problem, click the **Notes** tab.

    When you initially create and save a problem, entering notes in the **Work notes** field is not mandatory. If you change the priority of the problem by selecting different **Impact** or **Urgency** values on an existing problem, the **Work notes** field becomes mandatory.

    **Note:** This feature is available only in new instances starting with Jakarta or a later release. The Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\) plugin must be activate.

4.  To enter notes on why the problem is closed, click the **Closure Information** tab and enter the information.

    The date on which the problem was closed and the user who closed it populate automatically.

5.  Click **Submit**.


## What to do next

Assess the problem.

**Parent Topic:**[Create a problem](create-a-problem-v2.md)

