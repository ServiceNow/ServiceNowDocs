---
title: Deactivate Agent Affinity
description: Deactivate Agent Affinity if you do not want Agent Affinity to assign work assignments to agents.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Agent Affinity, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Deactivate Agent Affinity

Deactivate Agent Affinity if you do not want Agent Affinity to assign work assignments to agents.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  In the **Search** field, enter `glide.awa.agent_affinity.enabled`.

3.  Click **glide.awa.agent\_affinity.enabled**.

4.  On the system property screen, change **Value** from **true** to **false** and click **Update**.

    Agent Affinity is now deactivated.


**Parent Topic:**[Using Agent Affinity](../concept/awa-agent-affinity-concept.md)

