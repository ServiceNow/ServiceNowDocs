---
title: Integrate Panopta as a data source
description: Integrate the Panopta cloud-based monitoring solution with Event Management. To add Panopta as a data source, configuration is required in Panopta.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Panopta as a data source

Integrate the Panopta cloud-based monitoring solution with Event Management. To add Panopta as a data source, configuration is required in Panopta.

## Configure Panopta

To prepare Panopta as a datasource, follow the procedure described in this link: [How do I integrate with ServiceNow](https://docs.fortinet.com/product/fortimonitor/24.3).

When the Event Management integration is configured in Panopta, add the integration to any of your Panopta Alert Timelines so that the ServiceNow instance receives incident events accordingly.

## Optional Event Management configuration

Configure an alert action rule for launch in context of Panopta. For more information, see [Launch web application from alert](../task/t_EMLaunchAnApplication.md) and [Create or edit an alert action rule](../task/t_EMCreateAlertRule.md).

**Parent Topic:**[Integrate with push connectors](../task/configure-listener-transform-script.md)

**Related topics**  


[Configure Event Management connectors](connectors-and-listeners.md)

