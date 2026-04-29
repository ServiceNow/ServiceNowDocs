---
title: Healthcare IT case overview
description: Use the Healthcare IT case to create case types for IT-related healthcare operational requests.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Care Team Operations for Healthcare IT, Healthcare Operations, Healthcare and Life Sciences]
---

# Healthcare IT case overview

Use the Healthcare IT case to create case types for IT-related healthcare operational requests.

By associating these cases with specific healthcare organizations, care team members can easily view all cases created for their team, unit, or organization.

Healthcare IT cases automatically generate related incidents for ITIL fulfillers to handle. These incidents are assigned to supporting agents with the fulfiller role.

Any updates, comments, or status changes made to the incident are reflected in the case, and vice versa. When an incident is linked to a case, the fulfiller needs only manage the incident and the case will automatically update to reflect these changes.

## Incident auto-creation

![Incident auto creation.](../image/cto-it-incident-auto-create.png)

Incidents are created automatically in synchronization with Healthcare IT cases. All information from the Healthcare case is carried over into the incident.

## Comment synchronization

![Comment sync example in Care Team Operations for Healthcare IT.](../image/cto-it-comment-sync.png)

Comments left on the Healthcare IT case are viewable on the incident, and comments left in the **Compose** panel of the Incident are viewable on the Healthcare IT case.

## State synchronization

![State sync for Care Team Operations for Healthcare IT.](../image/cto-it-state-sync.png)

The state of both the incident and the healthcare case remains in synchronization throughout the entire fulfillment process. Use the Care Team Portal to track your case state in real time through viewing case details.

## Accepting or rejecting a solution

If a requesting party selects Accept Solution, the case and incident both enter a closed state.

If a requesting party selects Reject Solution, the state returns to Work in progress on both the incident and the case.

## On hold cases

In cases where an incident is set to **On hold** by the support agent with a reason state set to **Awaiting Caller**, additional information is required from the requester for the agent to proceed.

![On hold message occurring when a case needs more information in Care Team Operations for Healthcare IT.](../image/cto-it-on-hold.png)

This triggers an alert on the case in the Care Team Portal, where the state is changed to **Awaiting info**.

