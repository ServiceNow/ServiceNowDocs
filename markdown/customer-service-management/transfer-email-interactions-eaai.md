---
title: Transfer email interactions
description: Transfer a CCaaS-routed email interaction to another queue or agent when the interaction needs to be handled by a different team or individual.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Transfer email interactions

Transfer a CCaaS-routed email interaction to another queue or agent when the interaction needs to be handled by a different team or individual.

## Before you begin

Role required: sn\_customerservice\_agent and awa\_external\_user

## About this task

-   The email interaction must be routed via CCaaS. The Transfer Email action is not available for AWA-routed interactions.
-   Only queues and agents configured in the external queues section appear in the transfer options.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \(![List icon](../image/List_icon.jpg) \).

3.  In the Interactions section, select **My Interactions**.

4.  Open an email interaction.

5.  Select **Transfer email** from the options.

    The **Transfer Email** window displays queues and agents configured as external queues in the instance.

6.  Select any one of the following:

    -   To transfer to a queue, select the Queues tab, search for the target queue, and select the arrow \(![Transfer icon to transfer a queue or another agent](../image/arrow.png) \) icon.
    -   To transfer to an agent, select the Agents tab, search for the target agent, and select the arrow \(![Transfer icon to transfer to another agent](../image/arrow.png) \) icon.

        **Note:** Only available agents in the external queue are displayed in the Agents tab.


## Result

-   A message confirms the transfer \(for example, `This email has been transferred to Queue name`\).
-   The interaction record is updated in both CCaaS and the instance.
-   The current agent’s ownership and capacity are released. Transfer details \(source, target, timestamp\) are logged in the Work item table.

