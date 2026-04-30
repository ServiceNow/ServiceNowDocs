---
title: Integrate Honeycomb events
description: Integrate Honeycomb with Event Management by creating a webhook and configuring it as a trigger in the Honeycomb platform.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Honeycomb events

Integrate Honeycomb with Event Management by creating a webhook and configuring it as a trigger in the Honeycomb platform.

## Before you begin

Discovery for Honeycomb services and datasets is not supported. For event/CI binding to work, manually create a CI in the ServiceNow instance.

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## About this task

Configure the Event Management environment for the collection of events from Honeycomb by authenticating Honeycomb as a data source. In the Honeycomb platform, set your ServiceNow AI Platform as the rest endpoint using a webhook.

## Procedure

1.  In the Honeycomb platform, create an integration of **type=webhook**.

    1.  Navigate to **Usage** &gt; **Integrations**.

    2.  Select the **Add Integration** button.

    3.  Enter values in the **Name** and **Webhook URL** fields.

        When enting the Webhook URL, use the following format: `https://<USERNAME>:<PASSWORD>@<INSTANCE_NAME>.service-now.com/api/sn_em_connector/em/inbound_event?source=honeycomb`

    4.  In the **Provider** field, select **Webhook**.

    5.  Select **Add** to complete webhook creation.

2.  Add the webhook to a trigger.

    1.  Navigate to **Triggers** &gt; **Create New Trigger**.

    2.  Add a name and description for the trigger in the relevant fields.

    3.  In the **Alerts** section, configure the threshold and frequency in the relevant fields.

    4.  In the **Recipients** section, select **Add Recipient** and select the webhook created in step [1](honeycomb-event-integration.md#webhook-creation).

    5.  Select **Save Trigger**.

    **Note:** To view the trigger in the Honeycomb platform, navigate to **Quick Response \(in Alert\)** and select **Show Trigger in Honeycomb**.


## Result

Alerts flow from the Honeycomb connector into the Event Management plugin. The plugin extracts information from the original Honeycomb trigger message to populate the required event fields, and inserts the event into the database. You can view the events in your ServiceNow AI Platform instance by navigating **All Events**.

Honeycomb does not send severity information in the trigger message. The default severity for the Honeycomb alert is **3 - Minor**, which can be changed in the Push Connector Configuration section of **Push Connectors** &gt; **Honeycomb Push Connector** . The valid severities are: **1- Critical**, **2- Major**, **3- Minor**, **4- Warning**, and **5- Info**.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

