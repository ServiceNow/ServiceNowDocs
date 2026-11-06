---
title: WIP limits in EAP
description: Set a work in progress \(WIP\) limit on a state or substate so that a team sees when a Planning board lane holds more work than planned.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/enterprise-agile-planning/wip-limits-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 1
keywords: [WIP limits, Kanban lanes, Planning board]
breadcrumb: [Explore, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# WIP limits in EAP

Set a work in progress \(WIP\) limit on a state or substate so that a team sees when a Planning board lane holds more work than planned.

A team that starts more work than it can finish ends up with many items that are partly done. Those items wait in lanes, and the team can't easily tell where its work is stuck.

A WIP limit sets the maximum number of stories for one lane of a team. A lane is a story state or one of the substates of the team. When a lane reaches or passes its limit, the lane header on the Planning board shows it, so the team can act before more work piles up.

## WIP limits on the Planning board

The header of each lane shows the number of stories in the lane. When the lane has a limit, the header also shows the limit, for example `1/1`.

-   A lane without a limit shows only the number of stories.
-   A lane that reaches its limit has an amber header.
-   A lane that has more stories than its limit has a red header and an exclamation icon. Point to the icon to see a message such as `WIP limit exceeded: 2 items, limit 1`.

\[Omitted image "eap-planning-board-substates-wip-limits.png"\] Alt text: Planning board with the Design Ready lane over its limit, shown red with an exclamation icon, and the Code review lane at its limit, shown amber.

## Configuring WIP limits

A scrum master sets WIP limits for a team on the **Kanban WIP limits** tab of the Team Settings page. Each lane of a team can have one limit. Each team sets its own limits, so a change doesn't affect other teams. For more information, see [Set WIP limits for Kanban lanes in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/set-wip-limits-for-kanban-lanes-in-eap.md).

To set limits on steps within a state, create substates first. For more information, see [Substates in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/substates-in-eap.md).

