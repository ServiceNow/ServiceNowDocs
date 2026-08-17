---
title: Update iteration details in EAP
description: Edit details of a PI or a Sprint to update details such as name, team capacity, committed points.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/edit-pi-sprint-iteration-details-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage team backlog, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Update iteration details in EAP

Edit details of a PI or a Sprint to update details such as name, team capacity, committed points.

## Before you begin

[Create a Planning Interval or Sprint from EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-pi-sprint-eap-backlog.md).

Role required: sn\_apw\_advanced.eap\_user or sn\_apw\_advanced.eap\_scrum\_master

## About this task

Only an EAP scrum master can change the **Start date** and **End date** of an iteration. Users with the EAP user role can update the other iteration details, such as the name and the team capacity.

When you change the start date or end date of an iteration, the change updates the underlying planning calendar entry. The iterations on all other teams that share that entry are updated too, which keeps iteration timelines aligned across teams that plan together. Iterations that are complete or cancelled aren't updated.

Date changes must pass the same rules that apply on creation. For the full list, see [Creating iterations for teams in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/simplified-iteration-creation-in-eap.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose your EAP team.

3.  From the Backlog tab of an ART or an Agile Team, select the name of the iteration to open its details in the side panel.

4.  From the side panel, edit details such as Name, **Start date**, **End date**, Capacity, Committed points and others.

    The **Start date** and **End date** fields are editable only for an EAP scrum master.

    \[Omitted image "eap-edit-sprint.png"\] Alt text: Sprint details in the side panel in EAP.

5.  Save changes by selecting **Save**.

    If the new dates conflict with existing iterations or the underlying calendar entry, the changes aren't saved and an error message identifies the conflict.


**Parent Topic:**[Manage team backlog in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/using-eap.md)

**Related topics**  


[Schedule work items into iterations in EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/schedule-work-items-into-iterations-in-eap-backlog.md)

