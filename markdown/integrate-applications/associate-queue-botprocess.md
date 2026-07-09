---
title: c to the bot process from the related list
description: Associate a queue to a bot process in RPA Hub so that the bot process can interact with this queue. You can associate a bot process to multiple queues. If the bot process is enabled for robot pool, then only one queue \(that is not associated with any other bot process\) can be mapped to the current bot process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/associate-queue-botprocess.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adding details for your bot process, Configuring a bot process record, Use, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# c to the bot process from the related list

Associate a queue to a bot process in RPA Hub so that the bot process can interact with this queue. You can associate a bot process to multiple queues. If the bot process is enabled for robot pool, then only one queue \(that is not associated with any other bot process\) can be mapped to the current bot process.

## Before you begin

Ensure the bot process is not in published state.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

To assign a bot process to a queue from the Queues menu, see [Assign a bot process to a queue from Queues menu in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/assign-botprocess-queue.md).

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(\[Omitted image "rpahublist-icon.png"\] Alt text: List icon.\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open the bot process that you want to assign a queue to.

5.  On the **Queues** tab, select **New**.

6.  In the **Work Queue** field, select the required queue.

7.  Select **Save**.


**Parent Topic:**[Adding details to your bot process in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/post-req-bot-process-rpa.md)

**Related topics**  


[Queue form in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/queue-form.md)

[Unassign a bot process from a queue in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/unassign-botprocess-queue.md)

[Queue implementation in RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/queues-implement-rpa.md)

