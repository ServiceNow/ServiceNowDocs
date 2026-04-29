---
title: Playbook activity state-mapping rules
description: Map playbook activity states to states from the given experience record.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Playbook activity state mapping, Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Playbook activity state-mapping rules

Map playbook activity states to states from the given experience record.

![Changing how a Pending state is mapped from flow to playbook activity](../image/activity-state-mapping.gif)

Activity state-mapping rules are required for each Experience Status Table. These rules determine how to update the status for an experience record whenever a playbook user updates the state of an activity, such as when they complete an activity.

The out-of-the-box Global Playbook Experience includes default rules for the **sys\_flow\_data** and **task** tables. These sets of rules are enough for most playbook activities, but additional rules can be created for custom tables if needed.

Find the default mapping rules under the **Status Mapping** tab of a playbook experience.

![Playbook Experience status mapping tab](../image/activity-status-mapping.png "Status Mapping tab")

## Experience status mapping records

A Experience Status Mapping record pulls the states \(**Experience Status value**\) for the given **Experience Status Table**. Map from:

-   **Experience Status to Activity State**, or
-   **Activity State to Experience Status**.

The **Experience Status to Activity State** tab controls which activity state is shown in a card for a given experience status record value. The **Activity State to Experience Status** tab controls how the experience status record is updated when a playbook user updates an activity state, such as skipping an activity.

![Mapping from flow states to playbook activity states](../image/activity-state-mapping-flow-exp2act.png "Bidirectional status mapping between flows and playbook activity states")

![Mapping from playbook activity states to flow states](../image/activity-state-mapping-flow-act2exp.png "Bidirectional status mapping between flows and playbook activity states")

**Note:** There is always a default set of activity states, but the set of states for an experience record depends on the table in your activity definition.

![Mapping from task status values to playbook activity states](../image/activity-state-mapping-task-exp2act.png "Task Status to Activity State Map and vice versa")

![Mapping from playbook activity states to task status values](../image/activity-state-mapping-act2exp.png "Task Status to Activity State Map and vice versa")

**Note:** The number values shown indicate these task statuses:

![Task status values](../image/activity-state-mapping-task-values.png)

Default playbook activity states will always be set.

![Default activity states in a drop-down for the Activity Card Value field](../image/activity-state-mapping-card.png)

**Parent Topic:**[Playbook activity state mapping](playbook-activity-state-mapping.md)

