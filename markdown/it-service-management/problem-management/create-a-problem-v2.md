---
title: Create a problem
description: A problem is a cause of one or more incidents. Create a problem to identify the root cause of the incidents and try to prevent them from happening again.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing Problems, Problem Management, IT Service Management]
---

# Create a problem

A problem is a cause of one or more incidents. Create a problem to identify the root cause of the incidents and try to prevent them from happening again.

## Before you begin

Role required: itil, sn\_problem\_write, admin, problem\_admin, problem\_manager, or problem\_coordinator

If you do not have Problem Management Best Practice — Madrid plugin \(com.snc.best\_practice.problem.madrid\) activated, see [Create a problem \(legacy\)](create-problem.md#).

## About this task

-   You can generate a problem record manually from the problem module.
-   You can generate a problem from an incident.
-   You can create a record producer to log problems from the service catalog.
-   You can also generate a problem from an email when an appropriate inbound email action is configured.

## Procedure

1.  Create the problem with one of these options.

<table id="choicetable_agp_ckc_3t"><tbody><tr><td id="d333143e77">

**From the Problem module**

</td><td>

Navigate to **Problem** &gt; **Create New**.

</td></tr><tr><td id="d333143e95">

**From an incident**

</td><td>

1.  Open the incident.
2.  On the context menu, click **Create Problem**.
 **Note:** Use the property **List of attributes \(comma-separated\) that will be copied from the incident to create a new problem** \(**com.snc.problem.create\_from\_incident.attributes**\) to specify fields on the Incident form. The values of these fields are copied to the respective fields on the Problem form.

</td></tr></tbody>
</table>2.  On the Problem form, fill in the fields.

    For a description of the field values, see [Problem form](../reference/problem-form.md)

3.  Click **Submit**.

    The problem enters the **New** state. If you have filled the mandatory fields that are necessary to move a problem record to the **Assess** state, the problem record directly moves to the **Assess** state. If you want to add any additional field for the assess state, you must add the field at **System UI** &gt; **Form Sections**. For more information, refer [Add a field in the assess mandatory field dialog](add-field-in-assess-dialog-form.md).

    **Note:**

    When an incident is promoted as major incident, a problem record is created automatically if the following conditions are met:

    -   The incident does not have a problem record associated with it.
    -   Major Incident Management is installed along with problem management.
    -   The Problem Management Best Practice – Madrid plugin \(com.snc.best\_practice.problem.madrid\) and Incident Management - Major Incident Management plugin \(com.snc.incident.mim\) must be active.
    -   You must activate **Create Problem from Major incident** flow, which is inactive when shipped in base system.
    To configure the incident field information which must be copied to problem record, activate the **List of Attributes \(comma-seperated\) that will be copied from the incident to create a new problem** \(com.snc.problem.create\_from\_incident.attributes\) property.

    You can copy attachments and knowledge articles if the Problem Management Best Practice – Madrid plugin \(com.snc.best\_practice.problem.madrid\) is active and **com.snc.problem.create\_from\_incident.copy\_attachments** property is true.


## What to do next

Assess the problem.

-   **[Create a problem \(legacy\)](create-problem.md#)**  
A problem is a cause of one or more incidents. Create a problem to identify the root cause of the incidents and try to prevent them from happening again.

**Parent Topic:**[Managing Problems](../concept/problem-mgmt-lifecycle.md)

