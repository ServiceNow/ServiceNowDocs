---
title: Copy an incident or create a child incident
description: Copy an incident or create a child incident without manually entering the value of all the fields in the new incident.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Copy an incident or create a child incident

Copy an incident or create a child incident without manually entering the value of all the fields in the new incident.

## Before you begin

-   Role required: itil, sn\_incident\_write, or admin
-   Select the **Enable copy incident feature** \(**com.snc.incident.copy.enable**\) and the **Enable create child incident feature** \(**com.snc.incident.create.child.enable**\) incident properties at **Incident** &gt; **Incident Properties**.

**Note:** An itil user can copy or create a child of any incident whereas a user without any role can copy only the incident which the user has created.

## About this task

The Copy Incident functionality copies the details of an existing incident record to a new incident record. The Create Child Incident functionality copies the details of the parent incident and links the new incident to the parent incident. You can enable the options as well as add or remove fields or related list using the copy incident and create child incident properties.

## Procedure

1.  Navigate to **Incident** &gt; **Open**.

2.  Open an existing incident that you want to copy or from which you want to create a child incident.

3.  Perform one of the following actions.

<table id="choicetable_rsq_41q_23b"><thead><tr><th align="left" id="d132840e107">

Option

</th><th align="left" id="d132840e110">

Action

</th></tr></thead><tbody><tr><td id="d132840e116">

**Copy an incident**

</td><td>

Click the Additional actions icon ![The Additional actions icon](../image/context-menu.png) and then click **Copy Incident**.**Note:** After the incident is copied, the **Work notes** field of the new incident is updated with the following message: `Created from a similar incident: INCXXXXXX`.

</td></tr><tr><td id="d132840e143">

**Create a child incident**

</td><td>

Click the Additional actions icon ![The Additional actions icon](../image/context-menu.png) and then click **Create Child Incident**.**Note:** Ensure you have added the **Parent Incident** field and the **Incident -&gt; Parent Incident** related list to the incident form. The incident, from which you have created the child incident, is considered as the parent incident.

</td></tr></tbody>
</table>4.  Fill out the other fields, as required.

5.  Click **Submit**.

    The default fields and related lists that are copied from the parent incident are:

<table id="table_qjs_htt_23b"><thead><tr><th>

From where

</th><th>

What are copied

</th></tr></thead><tbody><tr><td>

Fields

</td><td>

-   Category
-   Subcategory
-   Business Service
-   Configuration item
-   Impact
-   Urgency
-   Assignment group
-   Short Description
-   Description
-   Related lists
-   Caused by Change
-   Location
-   Company
-   Problem
-   Change Request
-   Parent incident
 **Note:** If the problem, change, or the parent incident is not active, then details of those fields are not copied.

</td></tr><tr><td>

Related lists

</td><td>

-   Affected CIs
-   Impacted Services
-   Service Offerings
 **Note:** The supported related tables are:

-   Affected CIs \(task\_ci\)
-   Impacted Services \(task\_cmdb\_ci\_service\)
-   Service Offerings \(task\_service\_offering\)
-   Business Applications \(task\_cmdb\_ci\_business\_app\)
You cannot add any other table in this field but you can remove any of the default values.

</td></tr></tbody>
</table>
