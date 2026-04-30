---
title: Integrate Oracle Cloud Infrastructure alarms
description: Integrate Oracle Cloud Infrastructure \(OCI\) alarms with Event Management to send events into ServiceNow by adding a https subscription using Basic Authentication.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Oracle Cloud Infrastructure alarms

Integrate Oracle Cloud Infrastructure \(OCI\) alarms with Event Management to send events into ServiceNow by adding a https subscription using Basic Authentication.

## Before you begin

-   Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.
-   Oracle Cloud Discovery must be performed to ensure that the created alerts are bound to the configuration items in the ServiceNow AI Platform. For more information, see [Oracle Cloud Infrastructure Discovery](../../service-mapping/reference/oracle-cloud-infrastructure-discovery.md).
-   Role required: evt\_mgmt\_integration

## About this task

The Oracle Cloud Notifications service enables you to set up communication channels for publishing messages using topics and subscriptions. When a message is published to a topic, the Notifications service sends the message to all of the topic's subscriptions.

When an Oracle Management Cloud alert is raised, worsens in severity, or clears, you may want to be actively notified through an https custom URL to the ServiceNow instance. The Oracle Cloud connector will be used to create events in ServiceNow®.

You can configure the Event Management environment for the collection of alarms from Oracle Cloud by setting your ServiceNow AI Platform instance as the https subscription.

## Procedure

1.  In the Oracle Cloud console, set up a https subscription.

    1.  On the Create Subscription form, under the Configure Subscription section in the Protocol list, select **HTTPS \(Custom URL\)**.

        **Note:** When the subscription is created, the password will not be shown in clear text.

    2.  In the URL field, enter a URL with the format: `https://<username>:<password>@<instancename>.service-now.com/api/sn_em_connector/em/inbound_event/oraclecloud`.

        For example, `https://oracleevents:oracleevents@instance1.service-now.com/api/sn_em_connector/em/inbound_event/oraclecloud`.

        When the subscription is created with the ServiceNow instance URL, the Oracle Cloud Push connector will receive a payload that will confirm the subscription and is moved to an **Active** state in the Oracle Cloud console.

2.  In the Oracle Cloud console, you can create an alarm definition and set the notification destination with the topic containing the https ServiceNow subscription.

    1.  Navigate to **Observability &amp; Management** &gt; **Alarm Definitions**.

    2.  Click **Create Alarm** or select an existing alarm that you want to set the topic containing the https ServiceNow subscription.

    3.  In the Destinations section in the Topic list, select the topic with the https ServiceNow subscription.

        When an alarm is triggered in the Oracle Cloud console, the same alarm will be received in the Oracle Cloud Push connector in the ServiceNow instance and an event will be created.


## Result

Depending on the Oracle Cloud alarm resource, the alert will bind to the CI using the following Event Field Mapping:

![Event Field mapping form](../image/oracle-field-mapping.png)

You can create other event rules or modify the Event Field Mapping to map to other resource types.

Once the https subscription is configured and an Oracle Cloud alarm triggers a message in Event Management the message:

-   Authenticates the Oracle Cloud alarm message with the relevant ServiceNow user given in the https subscription.
-   Extracts information from the original Oracle Cloud alarm message to populate the required event fields and inserts the event into the ServiceNow AI Platform database.
-   Captures specified content in the **Additional Information** field of the event form.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

