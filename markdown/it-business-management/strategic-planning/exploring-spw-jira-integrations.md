---
title: Exploring SPWJira integrations
description: Learn more about integrating Strategic Planning Workspace with Jira and review the benefits it can provide for different users in your organization.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [explore]
breadcrumb: [SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Exploring SPWJira integrations

Learn more about integrating Strategic Planning Workspace with Jira and review the benefits it can provide for different users in your organization.

## SPW Jira integration overview

As a portfolio manager, you may rely on Strategic Planning Workspace \(SPW\) for roadmap planning, prioritization, and aligning work with strategic goals. However, your delivery teams could prefer using tools like Jira for the actual execution of work such as creating and managing stories and epics. This disconnect could create a visibility gap for portfolio managers, making it difficult to track progress and ensure alignment between strategy and execution.

The SPW-Jira integration helps solve this problem by providing seamless, bi-directional synchronization of key work items, including Epics, Features, Capabilities, and Stories. This synchronization ensures that updates made in either system are reflected in the other, giving portfolio managers real-time insight into execution without leaving SPW.

Sprints are created in EAP and sync to Jira, while status updates flow back from Jira to maintain visibility. This approach enables comprehensive end-to-end planning in SPW with the ability to plan dependencies and capacities across teams and sprints in EAP.

By bridging the gap between strategic planning and operational execution, this integration provides end-to-end visibility, enabling better decision-making, improved collaboration, and stronger alignment across teams.

## SPW Jira Integrations workflow

The following infographic shows how the integration between SPW and Jira work in both the applications.

![Working of SPW Jira integration between the two applications. For details, see the following description.](../images/jira-int-workflow.png)

-   One-to-One Mapping: Each Jira Project is directly mapped to an EAP Team.
-   Bidirectional Sync of Work Items:
    -   Epics, Features, Capabilities, and Stories are synced both ways between SPW and Jira.
    -   Sync applies to creation and updates.

        Example: A product owner creates an Epic in EAP and it appears in Jira. Team members update the Epic in Jira and the changes sync back to EAP.

        **Note:** If your Jira instance has state transition rules, the export sync from EAP to Jira might fail. For example, if a transition rule in Jira restricts a story or work item from moving directly to a **Complete** state without first passing through an **In Progress** state, and the story is marked **Complete** without that intermediate step, the sync fails.

-   Sprint Management:
    -   Sprints can only be created in EAP, then synced to Jira.
    -   Updates to sprints can be made in either application and are synced bidirectionally.

## What to explore next

To learn more about configuring and using SPW Jira Integrations, see:

-   [Configuring SPW Jira Integrations](configuring-spw-jira-integrations.md)
-   [SPW Jira Integrations reference](../reference/spw-jira-integrations-reference.md)

