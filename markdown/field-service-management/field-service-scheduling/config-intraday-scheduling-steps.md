---
title: Configuring Intraday schedule automation
description: Intraday schedule automation updates agents schedules to maximize productivity during their shift.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configuring Intraday schedule automation

Intraday schedule automation updates agents schedules to maximize productivity during their shift.

1.  [Activate intra-day schedule automation](../task/activate-intraday-scheduling-plugin.md)

    Administrators must activate the intra-day schedule automation plugin before changing any values.

2.  [Copy intraday schedule automation flows](../task/copy-intraday-scheduleing-flows.md)

    Copy the intra-day schedule automation flows and change only the copies. This practice ensures that you can copy the originals again if something happens to the versions you configure.

3.  \(Optional\) [Change the value for agents being considered early or late](../task/intraday-scheduling-time-value.md)

    Update the value that triggers a notification to the dispatcher indicating whether an agent is early or late.

4.  \(Optional\) [Change the time that determines whether an agent has acted](../task/change-intraday-scheduling-timing.md)

    Update the value that determines whether an agent has acted.

5.  \(Optional\) [Delete a flow](https://www.servicenow.com/docs/access?context=flow-delete&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

    If you do not need a flow installed with intra-day schedule automation, you can delete it.

6.  [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

    Activate the flows when you want to add the configurations to your instance.


-   **[Activate intra-day schedule automation](../task/activate-intraday-scheduling-plugin.md)**  
You can activate the Field Service Management Scheduling Automations plugin \(com.snc.sn\_app\_fsm\_scheduling\_flows\) for Field Service Management if you have the admin role. After the plugin is installed, three flow designer flows and nine subflows are added to your instance.
-   **[Copy intraday schedule automation flows](../task/copy-intraday-scheduleing-flows.md)**  
Duplicate the three intraday schedule automation flows installed with the Field Service Management Scheduling Flow Designer Flows plugin so if something breaks in the flows you activated, you can copy the originals again.
-   **[Change the value for agents being considered early or late](../task/intraday-scheduling-time-value.md)**  
Change the value that determines whether an agent is early or late.
-   **[Change the time that determines whether an agent has acted](../task/change-intraday-scheduling-timing.md)**  
Fine-tune the amount of time that determines whether an agent has acted when scheduled.
-   **[Change the recipients of notifications for intraday schedule automation](../task/intraday-notice-recipient.md)**  
You can change who receives notifications related to intraday schedule automation, so only the necessary recipients receive the notifications. For example, if an agent is late for a task, you can configure notifications to only be sent to the dispatcher.

**Parent Topic:**[Additional scheduling configuration options](advanced-scheduling-and-dispatching-capabilities.md)

