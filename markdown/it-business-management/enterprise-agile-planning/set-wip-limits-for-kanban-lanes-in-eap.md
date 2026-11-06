---
title: Set WIP limits for Kanban lanes in EAP
description: Limit the amount of work in progress for each state or substate of an Agile Team in Enterprise Agile Planning so that the team keeps its workload under control.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/enterprise-agile-planning/set-wip-limits-for-kanban-lanes-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 2
keywords: [WIP limits, Kanban lanes, Team Settings, Planning board]
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Set WIP limits for Kanban lanes in EAP

Limit the amount of work in progress for each state or substate of an Agile Team in Enterprise Agile Planning so that the team keeps its workload under control.

## Before you begin

Role required: sn\_apw\_advanced.eap\_scrum\_master

## About this task

A WIP limit sets the maximum amount of work for one lane of a team. A lane is a story state or one of the substates of the team. For more information about substates, see [Substates in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/substates-in-eap.md).

Each lane of a team can have one WIP limit. If you rename a substate, the lane name on its WIP limit is updated automatically.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose your Agile Team.

3.  In the page header, select **Team settings**.

4.  Select the **Kanban WIP limits** tab.

    \[Omitted image "eap-wip-limits-tab.png"\] Alt text: Kanban WIP limits tab listing a limit for the Code review and Design Ready lanes.

5.  Select **New**.

    \[Omitted image "eap-wip-limit-form.png"\] Alt text: Kanban WIP limit form with the Kanban lane, WIP limit and Team fields.

6.  In the **Kanban lane** field, select the state or substate that you want to limit.

    The list matches the lanes on the Planning board. A state that has substates is replaced in the list by its substates.

7.  In the **WIP limit** field, enter the maximum number of work items for the lane.

    The limit can't be a negative number.

8.  Select **Save**.

    The **Team** field is read-only and is set to the team that you opened.

    If the limit isn't valid, the record isn't saved and one of the following messages appears:

    -   `WIP limit can't be a negative number.`
    -   `A WIP limit already exists for this team and Kanban lane.`
    -   `Select a valid Kanban lane for the WIP limit.`

## Result

The WIP limit appears in the list on the **Kanban WIP limits** tab, and the limit applies to the matching lane on the Planning board of the team.

-   The lane header shows the number of stories in the lane and the limit.
-   A lane without a limit shows only the number of stories.
-   When a lane reaches its limit, the lane header turns amber.
-   When a lane has more stories than its limit, the header turns red and shows an exclamation icon.

**Related topics**  


[WIP limits in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/wip-limits-in-eap.md)

[Substates in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/substates-in-eap.md)

[Create substates for a team in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/create-substates-for-a-team-in-eap.md)

