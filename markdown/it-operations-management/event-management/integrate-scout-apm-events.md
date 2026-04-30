---
title: Integrate Scout APM events
description: Enable the collection of events from Scout APM by authenticating Scout APM as a data source to integrate it with Event Management.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Scout APM events

Enable the collection of events from Scout APM by authenticating Scout APM as a data source to integrate it with Event Management.

## Before you begin

The Event Management plugin \(com.glideapp.itom.snac\) must be installed.

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Discovery for Scout APM applications is not supported. To enable binding, you must manually create a CI in a ServiceNow instance in the Service Instance \[cmdb\_ci\_service\_auto\] table.

Role required: evt\_mgmt\_admin

## Procedure

1.  Enable Scout APM monitoring as an application service on your ServiceNow instance.

    1.  Navigate to **Configuration** &gt; **Application Service**.

    2.  Provide the application name that you are monitoring.

    3.  Set the operational status to Operational.

    4.  Select **Next**

    5.  Select **Done**.

2.  Log in to the Scout APM console.

3.  Create a notification channel.

    1.  Navigate to **Organization** &gt; **Alerts &amp; Notifications**.

    2.  Select **New Webhook**.

    3.  Provide the name of the webhook and the webhook URL.

        Use the following URL format: `https://<USERNAME>:<PASSWORD>@<INSTANCE_NAME>.service-now.com/api/sn_em_connector/em/inbound_event?source=scout`

    4.  Validate whether the webhook is operational by selecting **Send Test Alert**.

        A new event appears on your ServiceNow instance in the Events \[em\_event\] table with the data source as Scout APM.

4.  In the Organization section, create a new notification group.

    1.  On the **Alerts &amp; Notifications** page, navigate to **Organization** &gt; **Notification Groups**.

    2.  Add a name for the group and select the webhook channel you created.

    3.  Select the **Create Notification Group** button.

5.  In the application section, create alert conditions and configure them to receive alerts for notifications from Scout APM to the ServiceNow instance.

    1.  Navigate to **Applications** &gt; **Alert Conditions**.

    2.  Select the type of alert condition.

        For more information, see the Scout APM documentation.

    3.  Select **Create Alert condition**.

    4.  In the Alert Conditions table, select the notification group you created.

        The alert condition is displayed on the Scout console.

6.  Configure error notifications to receive alerts for errors from the Scout APM to the ServiceNow instance.

    1.  Navigate to **Application** &gt; **Error Notifications**.

    2.  Add a name and description for the notification.

    3.  Select the notification group that you created.

        The Scout APM notification channel is configured with the error notifications.

    4.  Select the **Add Notification Group** button.

        For any new error notifications in the Scout APM application, a new event will be generated in the Events \[em\_event\] table.


## Result

You can view all notifications on your ServiceNow instance in the Events \[em\_event\] table with the data source as Scout APM.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

