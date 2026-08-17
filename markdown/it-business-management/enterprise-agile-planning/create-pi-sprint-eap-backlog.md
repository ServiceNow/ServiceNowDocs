---
title: Create a Planning Interval or Sprint from EAP Backlog
description: Create iterations of Planning Intervals \(PI\) and Sprints so that teams can start prioritizing and scheduling their work from the Backlog in Enterprise Agile Planning \(EAP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/enterprise-agile-planning/create-pi-sprint-eap-backlog.html
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 3
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create a Planning Interval or Sprint from EAP Backlog

Create iterations of Planning Intervals \(PI\) and Sprints so that teams can start prioritizing and scheduling their work from the Backlog in Enterprise Agile Planning \(EAP\).

## Before you begin

Whether you can create an iteration depends on your role and on whether a timeline already exists for the team. Only an EAP scrum master can create the first iteration for a set of teams that share a planning calendar. For more information, see .

Role required: sn\_apw\_advanced.eap\_user or sn\_apw\_advanced.eap\_scrum\_master

## About this task

From the Backlog, create the next iteration for Agile Release Trains \(ARTs\) and Teams. Based on your EAP configuration of teams and planning calendars, you can create PIs, Sprints, or the iteration of any other calendar that you created.

This task is explained using the default Full Configuration as an example, where ARTs are mapped to Planning Intervals and Agile Teams are mapped to Sprints.

From EAP version 4.17.0, enter the start and end dates directly on the modal. The underlying planning calendar entries are created automatically, so nobody has to define them first. If a calendar entry already matches the team, the date fields are read-only and the system uses the dates from that entry. For details, see .

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose your ART.

3.  Create a Planning Interval for the ART.

    1.  From the Backlog tab of the selected ART, select **Create next Planning Interval**.

    2.  In the **Create Planning Interval** modal, enter values in the **Name**, **Start date**, and **End date** fields.

    3.  To create child Sprints for the Planning Interval at the same time, turn on **Create child entries on Sprint**, then enter the number of child Sprints and the Sprint length in days.

        If the ART shares its planning calendar with sibling ARTs that already have Sprints, child Sprints are automatically created to match the existing calendar. In that case, you don't have to specify the count or length.

    4.  Select **Create**.

    A Planning Interval is created for the selected ART with the dates you entered. If Agile Teams are associated with the ART, Sprints are created for those teams that align with the Planning Interval and its child spans. A confirmation message identifies the new iteration.

    If a new Agile Team is added to this ART later, the in-progress Sprint and the upcoming Sprints are automatically created for that team to match its sibling teams. Sprints that already ended aren't copied.

4.  To add more child Sprints to an existing Planning Interval, use the team-level Backlog.

    1.  From the left navigation panel, select the Planning Interval on the ART Backlog.

    2.  Select **Add child sprints**.

    3.  In the modal, enter the count and length for the new child Sprints, and select **Create**.

        Child Sprints are added to every Agile Team in the ART. Editing the start date of a Sprint shifts its end date to keep the Sprint length consistent.

5.  Create Sprints for an Agile Team directly, if needed.

    An Agile Team gets its Sprints from the parent ART's Planning Interval. Create a Sprint from the team-level Backlog only if the team needs a Sprint that doesn't align with the ART's Planning Interval, or if the team isn't yet linked to an ART calendar.

    1.  From the left navigation panel, select an Agile Team.

    2.  From the Backlog tab of the team, select **Create next Sprint**.

    3.  In the modal, enter values in the **Name**, **Start date**, and **End date** fields, then select **Create**.


## What to do next

See [Update iteration details in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/edit-pi-sprint-iteration-details-in-eap.md) and [Schedule work items into iterations in EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/schedule-work-items-into-iterations-in-eap-backlog.md).

**Parent Topic:**[Manage team backlog in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/enterprise-agile-planning/using-eap.md)

