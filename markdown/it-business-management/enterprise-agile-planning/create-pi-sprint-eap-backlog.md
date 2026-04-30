---
title: Create next PI and Sprint from EAP Backlog
description: Create iterations of Planning Intervals \(PI\) and Sprints so that teams can start prioritizing and scheduling their work from the Backlog in Enterprise Agile Planning \(EAP\).
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create next PI and Sprint from EAP Backlog

Create iterations of Planning Intervals \(PI\) and Sprints so that teams can start prioritizing and scheduling their work from the Backlog in Enterprise Agile Planning \(EAP\).

## Before you begin

Role required: sn\_apw\_advanced.eap\_user

## About this task

From the Backlog, create the next iteration for Agile Release Trains \(ARTs\) and Teams. Based on your EAP configuration of teams and planning calendars, you can create PIs, Sprints, or the iteration of any other calendar that you created.

This task is explained using the default Full Configuration as an example, where ARTs are mapped to Planning Intervals and Agile Teams are mapped to Sprints.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose your ART.

3.  Create Planning Intervals for ART.

    1.  From the Backlog tab of a selected ART, select **Create next Planning Interval**.

    2.  In the confirmation dialog box, select **Create**.

    A PI is created for the selected ART. The start and end dates are based on the next available business calendar span that was created by your system admin.

    The default name for the PI is **&lt;calendar name&gt; &lt;n+1&gt;** where:

    -   **calendar name** is the name of the business calendar entries that your system admin has created.
    -   **n** is the number of the last created PI.

        For example, if the name of your business calendar entry is set as **Greenbacks PI** and Greenbacks PI 1 and Greenbacks PI 2 exist already, then the new PI is named **Greenbacks PI 3**.

    After the PI is created, you can edit this name according to your naming convention. See [Update iteration details in EAP](edit-pi-sprint-iteration-details-in-eap.md).

    For more information on how a system admin can define the calendar entries and their dates, see [Create calendar entries for iterations in EAP](create-calendar-entries-in-eap.md).

    **Note:** If you have Agile Teams added to this ART, Sprints are automatically created for them too. The number of Sprints created for the teams are based on the child calendar spans that match with the PI dates. If you add Agile Teams to this ART later, Sprints aren’t added to them automatically. In that case, proceed to step 4.

4.  Create Sprints for Agile Teams.

    1.  From the left navigation panel, select an Agile Team.

    2.  From the Backlog tab of this team, select **Create next Sprint**.

    3.  Confirm by selecting **Create**.

    The default name and dates for this Sprint are according to the business calendar entry defined by the system admin.

    After the Sprint is created, you can edit this name according to your naming convention. See [Update iteration details in EAP](edit-pi-sprint-iteration-details-in-eap.md).


## What to do next

-   [Update iteration details in EAP](edit-pi-sprint-iteration-details-in-eap.md).
-   [Schedule work items into iterations in EAP Backlog](schedule-work-items-into-iterations-in-eap-backlog.md).

**Parent Topic:**[Manage team backlog in EAP](../concept/using-eap.md)

