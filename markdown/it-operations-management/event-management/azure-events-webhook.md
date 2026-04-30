---
title: Integrate Azure Monitor with basic authentication
description: Integrate Microsoft Azure with Event Management by adding a standard webhook in Azure Monitor.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrate Azure Monitor as an authenticated data source, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Azure Monitor with basic authentication

Integrate Microsoft Azure with Event Management by adding a standard webhook in Azure Monitor.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Roles required: evt\_mgmt\_admin and web\_service\_admin

## About this task

Configure the Event Management environment for the collection of events from Azure by authenticating Azure Monitor as a data source. In your Azure Monitor portal, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

On the Azure portal, alert correlation rules are defined through the **Correlate alerts** setting within Alert Processing Rules. When **Correlate alerts** is assigned on the Azure portal, the Azure Monitor alerts received on the ServiceNow® instance within 60 minutes are grouped using tag based alert clustering.

## Procedure

1.  In the ServiceNow AI Platform, create a user account or identify an existing ServiceNow user for this integration.

    Also ensure the relevant ServiceNow sys\_user is assigned the evt\_mgmt\_integration role. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

2.  In your Azure Monitor portal, update the Azure Monitor alert rules to use an action group with a standard webhook:

    1.  Create an action group with **action type=webhook**, and provide the URL that includes the user ID and password of the ServiceNow user in the endpoint.

        For example:

        `https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=azuremonitor`

        **Note:** If you have multiple tenants on the Azure portal and you want to use bidirectional functionality to acknowledge, close, or reopen an alert on the Azure Portal, then the URL for the webhook has to be in the following format: `https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=azuremonitor&event_class=<new_connector_instance_name>`. The &lt;new\_connector\_instance\_name&gt; is the new Azure pull connector instance that you need to create for each tenant with other Azure service principal credentials. To know how to create the pull connector, see [Configure Azure Monitor Bi-directional connector](configure-azure-bi-directional-connector.md).

    2.  In the Webhook section, make sure that **Yes** is selected for the **Enable the common alert schema** option.


## Result

Alerts start flowing from the Azure Monitor into the Event Management plugin. The plugin extracts information from the original Azure Monitor alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to **All Events** to see the events.

## What to do next

If you want to send alert state changes on the ServiceNow instance from the ServiceNow alerts to the Azure Portal, you need to enable the Azure Monitor Bi-directional connector. For more information, see [Configure Azure Monitor Bi-directional connector](configure-azure-bi-directional-connector.md).

**Parent Topic:**[Integrate Azure Monitor as an authenticated data source](../concept/azure-integration.md)

