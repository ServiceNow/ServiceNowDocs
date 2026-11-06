---
title: Create substates for a team in EAP
description: Add substates to a story state for an Agile Team to track work in more detail on stories and on the Planning board in Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/enterprise-agile-planning/create-substates-for-a-team-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 1
keywords: [substates, Team Settings, story states]
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create substates for a team in EAP

Add substates to a story state for an Agile Team to track work in more detail on stories and on the Planning board in Enterprise Agile Planning.

## Before you begin

Role required: sn\_apw\_advanced.eap\_scrum\_master

## About this task

Substates apply to one team at a time. For more information about how substates work, see [Substates in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/substates-in-eap.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.

2.  From the Agile structure section of the left navigation panel, choose your Agile Team.

3.  In the page header, select **Team settings**.

4.  Select **Substates**.

    The tab lists the substates of the team, grouped by state and sorted by order.

    \[Omitted image "eap-substates-tab.png"\] Alt text: Substates tab listing a substate under each of the Ready and Work in progress states.

5.  Select **New** to create a substate.

6.  Fill in the substate fields.

    |Field|Description|
    |-----|-----------|
    |**State**|Story state that the substate belongs to. This field is required.|
    |**Name**|Label that users see for the substate. This field is required.|
    |**Order**|Position of the substate within its state. Substates with lower numbers appear first. This field is required.|
    |**Use as default**|Option to make the substate the default for its state. A state can have only one default substate. The first substate that you create for a state is set as the default even if you don't select this option. If another substate is already the default, it's replaced and a message tells you about the change.|

    The **Team** field is read-only and is set to the team that you opened.

    \[Omitted image "eap-substate-form.png"\] Alt text: Substate form with the State, Name, Order, Team and Use as default fields.

7.  Select **Save**.


## Result

The substate appears in the list under its state, in order. If it's the first default substate for the state, stories in that state that have no substate receive it. A message tells you that the update is running in the background.

**Related topics**  


[Substates in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/substates-in-eap.md)

[Set WIP limits for Kanban lanes in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/set-wip-limits-for-kanban-lanes-in-eap.md)

