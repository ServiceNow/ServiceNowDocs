---
title: Manually create an SRM incident
description: Create an incident if you think an issue poses a serious risk and should be taken care of as soon as possible.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Working with incidents in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Manually create an SRM incident

Create an incident if you think an issue poses a serious risk and should be taken care of as soon as possible.

## Before you begin

Role required: srm\_manager, srm\_responder, or srm\_admin

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Reliability tasks** \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  Select the Incidents tab.

4.  Select **New**.

5.  Fill in the fields on the Create New Incident form, as appropriate.

    Only the **Short Description** field is required.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

Add brief description of the incident.

</td></tr><tr><td>

Description

</td><td>

Add detailed description of the incident.

</td></tr><tr><td>

Number

</td><td>

Identifier assigned to the incident.

</td></tr><tr><td>

Impact

</td><td>

Select is a measure of the effect of the incident. Impact affects **Priority**. Choices are:

-   1 - High
-   2 - Medium
-   3 - Low


</td></tr><tr><td>

Assignment group

</td><td>

Select a team to work on the incident by typing or searching.

</td></tr><tr><td>

Priority

</td><td>

Automatically set based on **Impact** and **Urgency**. It identifies how quickly the incident should be addressed. See **Priority Data lookup rules** table below.

Values are:

-   3 - Moderate
-   4 - Low
-   5 - Planning


</td></tr><tr><td>

Category

</td><td>

Select a category for the incident. Choices are:-   --None--
-   Inquiry/Help \(default\)
-   Software
-   Hardware
-   Network
-   Database


</td></tr><tr><td>

Urgency

</td><td>

Select a measure of how long the resolution can be delayed until an incident has a significant business impact. Urgency affects **Priority**.

</td></tr><tr><td>

Service

</td><td>

Select a service associated with the incident.

</td></tr><tr><td>

Severity

</td><td>

Select a severity to associate with the incident by typing or searching. Choices are: -   1 - High
-   2 - Medium
-   3 - Low


</td></tr><tr><td>

Configuration item

</td><td>

Select a asset to associate with the incident by typing or searching.

</td></tr><tr><td>

Assigned to

</td><td>

Assign team member to work on the incident by typing or searching.

</td></tr><tr><td>

State

</td><td>

Choose a state for the incident. Choices are:-   New \(default\)
-   In Progress
-   On Hold
-   Resolved
-   Canceled
See [SRM incident states](../concept/sr-incident-states.md) for more information.

</td></tr><tr><td>

Watchlist

</td><td>

Select individuals to watch the incident by typing or searching.

</td></tr><tr><td>

Resolution code

</td><td>

Select a resolution code when you have one. Choices are:-   None \(default\)
-   Duplicate
-   Known error
-   No resolution provided
-   Resolved by caller
-   Resolved by change
-   Resolved by problem
-   Resolved by request
-   Solution provided


</td></tr><tr><td>

Resolution notes

</td><td>

Enter any relevant resolution information.

</td></tr></tbody>
</table>    **Note:** Priority is calculated according to the following sample data lookup rules:

    |Impact|Urgency|Priority|
    |------|-------|--------|
    |1 - High|1 - High|1 - Critical|
    |1 - High|2 - Medium|2 - High|
    |1 - High|3 - Low|3 - Moderate|
    |2 - Medium|1 - High|2 - High|
    |2 - Medium|2 - Medium|3 - Moderate|
    |2 - Medium|3 - Low|4 - Low|
    |3 - Low|1 - High|3 - Moderate|
    |3 - Low|2 - Medium|4 - Low|
    |3 - Low|3 - Low|5 - Planning|

6.  Select **Save**.

    The incident is created and the new incident form displayed.

7.  Add an attachment related to the incident in the **Actions** panel using the **Attachments** icon ![Attachments icon](../image/icon-sr-attachment.png).

8.  Create an incident template using the Template icon ![Template icon](../image/icon-sr-template.png).

9.  Start or join a Zoom meeting, Microsoft Teams, or Slack channel in the **Collaboration** panel..

10. Select **Save**.

    The incident appears with comments, work notes, and incident activity captured in the **Activity** stream. For more information on incident fields, see [SRM incidents](../reference/sr-incidents-workspace.md).


**Parent Topic:**[Working with incidents in SRM](../concept/sr-work-incidents.md)

