---
title: Transfer email interactions
description: Transfer an email interaction routed by AWA or CCaaS to another agent or queue when the interaction needs to be handled by a different team or individual.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/transfer-email-interactions-eaai.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Transfer email interactions

Transfer an email interaction routed by AWA or CCaaS to another agent or queue when the interaction needs to be handled by a different team or individual.

## Before you begin

Role required: sn\_customerservice\_agent

## About this task

-   For AWA -routed interactions routed by AWA, only available agents and AWA queues appear in the transfer options. When transferring to a queue, AWA routing rules apply to assign the interaction to an eligible agent. When transferring to a specific agent, the interaction is directly assigned.
-   For CCaaS-routed interactions, only queues and agents configured in the external queues section appear in the transfer options.
-   The full email thread and interaction history are preserved on transfer.
-   The transferring agent's capacity is released on transfer. The receiving agent's capacity is blocked on assignment.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \(\[Omitted image "List\_icon.jpg"\] Alt text: Open interactions list \).

3.  In the Interactions section, select **My Interactions**.

4.  Open an email interaction routed by AWA or CCaaS.

5.  Select **Transfer email** from the options.

6.  In the **Transfer Email** window, select one of the following:

    -   To transfer to a queue, select the **Queues** tab, search for the target queue, and select the arrow \(\[Omitted image "arrow.png"\] Alt text: Transfer to queue or agent \) icon.
    -   To transfer to an agent, select the **Agents** tab, search for the target agent, and select the arrow \(\[Omitted image "arrow.png"\] Alt text: Transfer to agent \) icon.

## Result

-   A message confirms the transfer \(for example, `This email has been transferred to Queue name`\).
-   For interactions routed by AWA, the interaction is assigned to the target agent or routed to the target queue according to AWA routing rules.
-   For CCaaS-routed interactions, the interaction record is updated in both CCaaS and the instance.
-   The transferring agent's ownership and capacity are released. The receiving agent's capacity is blocked on assignment. Transfer details including source, target, and timestamp are logged in the Work Item table.

