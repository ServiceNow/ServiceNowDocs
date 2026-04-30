---
title: Configure an agent's maximum universal capacity
description: Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. If the agent's maximum universal capacity has been reached, additional work items won’t be assigned to the agent.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Configure an agent's maximum universal capacity

Prevent an agent from being assigned too many work items by configuring the agent's maximum universal capacity. If the agent's maximum universal capacity has been reached, additional work items won’t be assigned to the agent.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to the universal capacity settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Additional settings section, select **Set up universal capacity**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Universal Capacity**.
2.  Choose a situation.

    -   To create a new maximum universal capacity for an agent, select **New**:

        |Field|Definition|
        |-----|----------|
        |Max Universal Capacity|Maximum capacity for an agent across all service channels. If an agent's current capacity equals the maximum universal capacity, additional work items won’t be assigned to the agent.|
        |Users|The max universal capacity is assigned to the users \(agents\) in the Selected list. Select agents in the Available list and then select the right-pointing arrow to add them to the Selected list. To filter the agents in the Available list, create a filter by selecting **Add Filter** or run an existing filter by selecting **Run Filter**.|

    -   To update an existing maximum universal capacity for an agent, select the maximum universal capacity to update:

        |Field|Definition|
        |-----|----------|
        |Max Universal Capacity|Maximum capacity for an agent across all service channels. If an agent's current capacity equals the maximum universal capacity, additional work items won’t be assigned to the agent.|
        |Universal Capacity In Use|Current workload for an agent across all service channels.|
        |Agent|Name of the agent.|

3.  Select **Submit** for a new universal capacity or **Update** for an existing universal capacity.


**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

