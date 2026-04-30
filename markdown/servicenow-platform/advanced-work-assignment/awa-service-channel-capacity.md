---
title: Service channel capacity and utilization
description: In Advanced Work Assignment, capacity is the number of work items automatically assigned to agents supporting a service channel. Utilization is the condition that identifies the work item states supported in the channel.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service channels, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service channel capacity and utilization

In Advanced Work Assignment, capacity is the number of work items automatically assigned to agents supporting a service channel. Utilization is the condition that identifies the work item states supported in the channel.

Agents have an assigned capacity for each service channel. This capacity is based on the default capacity set for the channel. The agent capacity for one service channel \(for example, chat\) does not interfere with the capacity on other service channels \(for example, case or incident\). Admins can set the **Default capacity** for a channel on the Service Channel form. This setting applies to all agents supporting the channel.

Managers can override the default capacity for:

-   Individual agents, by using the **Agent Capacity Override** related list on the Service Channel form.
-   Groups of agents, by using the **Agent Capacity Override** related list on the Group form.

If an agent already has a capacity override, setting the override again updates the existing capacity for that agent. Override capacity is stored in the Agent Capacity \(awa\_agent\_capacity\) table.

-   **[Create or configure a service channel](../task/awa-create-service-channel.md)**  
Create or configure a service channel that is used in Advanced Work Assignment \(AWA\).

**Parent Topic:**[Service channels](awa-service-channels.md)

