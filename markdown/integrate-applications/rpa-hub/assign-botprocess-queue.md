---
title: Assign a bot process to a queue from Queues menu
description: Assign a bot process to a queue in RPA Hub so that it can interact with this queue. You can assign more than one bot process to a queue. Any robot that is associated with the assigned bot process can insert the work item, pick the work item, and update the work item.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Assign a bot process to a queue from Queues menu

Assign a bot process to a queue in RPA Hub so that it can interact with this queue. You can assign more than one bot process to a queue. Any robot that is associated with the assigned bot process can insert the work item, pick the work item, and update the work item.

## Before you begin

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Create a queue. For more information, see [Create a queue in RPA Hub](create-queue.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

If the bot process is enabled for robot pool, then only one queue \(that is not associated with any other bot process\) can be mapped to the current bot process.

To associate a queue to a bot process from the bot process related list, see [Associate a queue to the bot process from the related list](associate-queue-botprocess.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Queues**.

4.  Open the queue that you want to assign a bot process to.

5.  On the **Bot Process Configuration** tab, select **Add**.

6.  On the **Available Bot Process** tab, select the required bot process.

7.  Select **Add**.

8.  Select **Save**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Queue form in RPA Hub](../reference/queue-form.md)

[Unassign a bot process from a queue](unassign-botprocess-queue.md)

[Queue implementation in RPA Hub](../concept/queues-implement-rpa.md)

