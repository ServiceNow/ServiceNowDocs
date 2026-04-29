---
title: Using Agent Affinity
description: Agent Affinity is an Advanced Work Assignment feature that lets you assign work items by an agent's work history, related task, or account team affinity.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Using Agent Affinity

Agent Affinity is an Advanced Work Assignment feature that lets you assign work items by an agent's work history, related task, or account team affinity.

Advanced Work Assignment assigns work items to agents by their availability, capacity, and skills. You can use Agent Affinity to customize this AWA assignment process and identify the agent best suited for the work item. Agent Affinity ensures that the same agent is assigned to a similar work item instead of orienting a new agent every time.

**Note:** Agent Affinity rules do not override assignment eligibility or constraints that are specified on AWA assignment rules.

The types of affinities are:

-   **Historical**

    Identifies the best agent based on the agent's history of serving the same customer.

-   **Related task**

    Identifies the best agent based on the agent's past assignments of related tasks.

-   **Account team**

    Identifies the best agent based on the agent's responsibility or role in the account team.


**Note:** Account team affinity is available only to Customer Service Management customers.

Affinity rules are associated with AWA queues. Up to three rules can be associated with each queue. The affinity order determines how the assignment engine ranks the agents. The agent with the higher order affinity rule is considered as the best agent first.

The following example shows how AWA uses Agent Affinity to determine the best agent for a work item. In this example, AWA is configured to use all three affinities in this order: related task affinity, account team affinity, and historical affinity. George Warren, who is a customer at the Boxeo company, has a router problem. George previously contacted support to report an issue. That case was assigned to agent Ned. The primary support agent for Boxeo is agent John. Within the past seven days, another agent, agent Beth, addressed a chat with Boxeo.

The next time George initiates a customer service chat from the case page, the case is automatically added as a related task to the chat interaction. Agent Affinity uses the related task affinity to look for an agent who has fulfilled past assignments for a related task. Because agent Ned was assigned to a related task on the record, AWA assigns the work item to agent Ned if available with capacity.

![Agent Affinity configured to use related task affinity.](../image/awa-affinity-task-based-example.png "Example of related task affinity")

If agent Ned is unavailable or doesn't have the capacity, AWA uses the account team affinity. AWA looks for another agent based on an agent's responsibility or role in the account team. Because agent John is the primary support agent for the Boxeo company, AWA assigns the work item to Agent John if available with capacity.

![Agent Affinity configured to use account team affinity.](../image/awa-affinity-account-team-example.png "Example of account team affinity")

If agent John is not available, AWA uses the historical affinity and looks for an agent that has recently interacted with the company. This information is stored on the Agent Affinity screen. Because agent Beth addressed a chat with Boxeo within the past seven days, AWA assigns the work item to agent Beth if available with capacity.

![image.awa-affinity-historical-example]

