---
title: Configure alert collection from SCOM
description: Alerts from the Microsoft System Center Operations Manager \(SCOM\) are collected using the SCOM connector instance.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure alert collection from SCOM

Alerts from the Microsoft System Center Operations Manager \(SCOM\) are collected using the SCOM connector instance.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The SCOM connector instance requires configuration before receiving alerts and Metric Intelligence raw data from the SCOM server. You can limit the collection of SCOM alerts to only those alerts that belong to the SCOM group that you specify.

## Procedure

1.  Configure the SCOM connector instance.

2.  Configure the Microsoft System Center Operations Manager \(SCOM\) connector instance to receive alerts and Metric Intelligence raw data from the SCOM server.

3.  Limit collected SCOM alerts to specific SCOM groups.


-   **[Configure the SCOM connector instance](t_EMConfigureSCOMConnector.md)**  
Configure the Microsoft System Center Operations Manager \(SCOM\) connector instance to receive alerts and Metric Intelligence raw data from the SCOM server.
-   **[Limit collected SCOM alerts to specific SCOM groups](t_EMAssignRoleSCOMGroup.md)**  
Limit the collection of SCOM alerts to only those alerts that belong to the specified SCOM group.
-   **[SCOM metric event rules](../concept/scom-event-rules.md)**  
The base system comes with Microsoft System Center Operations Manager \(SCOM\) metric event rules. SCOM metric event rules bind event metrics to configuration items \(CIs\).

**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

