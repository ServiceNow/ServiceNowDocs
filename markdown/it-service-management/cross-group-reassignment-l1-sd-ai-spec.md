---
title: Cross-group reassignment for the L1 IT Service Desk AI Specialist
description: Cross-group reassignment lets the L1 IT Service Desk AI Specialist act when a different assignment group usually resolves incidents like the one it is working on. Learn how the Off, Recommend only, and On settings work, and what happens to the incident.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/cross-group-reassignment-l1-sd-ai-spec.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 3
keywords: [cross-group reassignment, reassignment, reassign, routing recommendation, assignment group, autonomous]
breadcrumb: [Explore, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Cross-group reassignment for the L1 IT Service Desk AI Specialist

Cross-group reassignment lets the L1 IT Service Desk AI Specialist act when a different assignment group usually resolves incidents like the one it is working on. Learn how the Off, Recommend only, and On settings work, and what happens to the incident.

## How cross-group reassignment works

When the L1 IT Service Desk AI Specialist works on an incident, it compares the incident with similar resolved incidents. If a different assignment group resolved most of those incidents, and the L1 IT Service Desk AI Specialist is confident enough that this group is the consistent resolver, it acts on the pattern.

What it does depends on the **Cross-group reassignment** setting. You can set it to recommend the reassignment to your service desk team, or you can let the L1 IT Service Desk AI Specialist reassign the incident itself.

The setting is off by default, and service desk managers can edit it. The cross-group check runs before the L1 IT Service Desk AI Specialist does any resolution work, so it applies in both autonomous and supervised execution mode. When **Cross-group reassignment** is **On**, the L1 IT Service Desk AI Specialist reassigns the incident even in supervised mode. For more information about the modes, see [Autonomous and supervised execution modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/auto-vs-supervised-l1-itsd-ai-spec.md).

## Settings

Configure these settings in the Reassign section of the task settings. For details, see [Reassign fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md).

|Setting|Description|
|-------|-----------|
|**Cross-group reassignment**: **Off**|The L1 IT Service Desk AI Specialist doesn't act on the pattern. This is the default.|
|**Cross-group reassignment**: **Recommend only**|The L1 IT Service Desk AI Specialist posts a recommendation and unassigns itself. It never changes the assignment group, so your service desk team decides whether to reassign the incident.|
|**Cross-group reassignment**: **On**|The L1 IT Service Desk AI Specialist reassigns the incident on its own. It sets the assignment group to the recommended group and unassigns itself. It doesn't use the **Choose where to reassign records** setting.|

## What happens to the incident

When the L1 IT Service Desk AI Specialist acts on a cross-group pattern, it does the following:

1.  Adds a work note for your service desk team that explains the pattern.
2.  When **Cross-group reassignment** is **On**, sets the assignment group to the recommended group and ignores the **Choose where to reassign records** setting. When it is **Recommend only**, leaves the assignment group unchanged.
3.  Unassigns itself from the incident.
4.  Sets the incident state to the record state that you mapped to the **New** state of the L1 IT Service Desk AI Specialist, or to the standard New state if you haven't mapped one, so the incident appears as an unassigned item for the receiving team. It doesn't change the state of resolved or closed incidents.

## What the work note says

The work note has the same sections in both modes. The wording changes to match what the L1 IT Service Desk AI Specialist did.

-   **Routing Recommendation**: How many similar resolved incidents the L1 IT Service Desk AI Specialist reviewed, how many of them the recommended team resolved, and its confidence as a percentage. In Recommend only mode, it says that it recommends reassigning the incident. In On mode, it says that it reassigned the incident.
-   **What I've Done**: In Recommend only mode, it says that it unassigned itself and that the recommendation is advisory only. In On mode, it says that it reassigned the incident to the recommended team and unassigned itself so the team can take ownership.
-   **Next Steps for the Service Desk**: In Recommend only mode, it asks your team to review the referenced incidents and confirm whether to reassign the incident. In On mode, it asks your team to review the referenced incidents, which show why the incident was reassigned.
-   **Referenced Incidents**: A list of the closest similar incidents, each linked to its record.

An administrator can edit the work note text in the **Cross-group reassignment recommendation** template.

## Reporting

The L1 IT Service Desk AI Specialist records the same reassignment reason for both modes, because the mode describes how the incident is reassigned, not why.

In Recommend only mode, you can track how often your service desk team follows the recommendations on the Performance dashboard. For more information, see [Cross-group reassignment outcomes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/perf-overview-l1-sd-ai-spec.md).

