---
title: Integrate Instana events
description: Integrate Instana with Event Management by adding a standard webhook in the Instana console.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate Instana events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Instana events

Integrate Instana with Event Management by adding a standard webhook in the Instana console.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## Procedure

1.  In the Instana console, navigate to **Settings** &gt; **Events &amp; Alerts** &gt; **Alert Channels**.

2.  Open the **Add Alert Channel** dropdown and select the **Generic Webhook** option.

3.  In the **Webhook URLs** field, create an alert channel by entering the following URL:

    `https://<instance>.service-now.com/api/sn_em_connector/em/inbound_event?source=instana`

4.  To authenticate the ServiceNow URL, enter the following in the **Custom HTTP Request Headers**:

    |Field|Value|
    |-----|-----|
    |Key|Authorization|
    |Value|Basic &lt;base64\_encoded username:password&gt;|

5.  Configure Instana to create alerts for event types or events.

    1.  Navigate to **Settings** &gt; **Events &amp; Alerts** &gt; **Alerts**.

    2.  Select **New Alert**.

    3.  In the **Events** section, select one of the following:

        -   Alert on Event Type\(s\)
        -   Alert on Event\(s\)
    4.  When creating alerts for event types:

        1.  Select the type of events for which you want alerts to be created, such as **Critical Issues**, **All Incidents**, **Warning issues**, and so forth.
        2.  In the **Alerting** section, select the **servicenow** alert channel.
    5.  When creating alerts for events:

        1.  Select the events for which you want alerts to be created.
        2.  In the **Alerting** section, select the **servicenow** alert channel.
    When Instana creates an alert, the alert is sent to the ServiceNow instance. Alerts created for the host entity are bound to the Server \(cmdb\_ci\_server\) table, and alerts created for the website entity are bound to the HTTP\(S\) \(cmdb\_ci\_endpoint\_http\) table.

    Add other entity types in the Instana - ci\_type Event Field Mapping table to ensure that the entity binds with the correct CI in the ServiceNow instance.

6.  To view the event in the Instana source system, you can access it from a ServiceNow instance:

    1.  Navigate to **All** &gt; **Event Management** &gt; **Service Operations Workspace**.

    2.  Select **All Alerts**.

    3.  Select the relevant alert.

    4.  On the **Details** tab, locate the **Actions** section on the right side of the page and in the **Show Event on Instana UI** cell, select **Launch app**.


**Parent Topic:**[Integrate Instana events](../concept/instana-integration.md)

