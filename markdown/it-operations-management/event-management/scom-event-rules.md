---
title: SCOM metric event rules
description: The base system comes with Microsoft System Center Operations Manager \(SCOM\) metric event rules. SCOM metric event rules bind event metrics to configuration items \(CIs\).
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure alert collection from SCOM, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# SCOM metric event rules

The base system comes with Microsoft System Center Operations Manager \(SCOM\) metric event rules. SCOM metric event rules bind event metrics to configuration items \(CIs\).

When an event's metrics match the event filter conditions, the metrics bind to the indicated CI. The event rules that come with the base system are:

|Rule Name|CI type|
|---------|-------|
|SCOM Metrics - Windows Server|cmdb\_ci\_win\_server|
|SCOM Metrics - IIS Web Server|cmdb\_ci\_microsoft\_iis\_web\_server|
|SCOM Metrics - SQL Server Reporting Services|cmdb\_ci\_db\_mssql\_reporting|
|SCOM Metrics - MS SQL Database|cmdb\_ci\_db\_mssql\_database|
|SCOM Metrics - MSFT SQL Instance|cmdb\_ci\_db\_mssql\_instance|

You can create a custom event rule to bind metrics with other CI types. For details, see [Create or edit an event rule](../task/create-or-edit-event-rule.md).

If the event rule filter doesn't match, the default rule, **SCOM Metrics - Default** \(CI type = **cmdb\_ci\_hardware**\) is invoked. The order number of the default event rule must be higher than the order number of any SCOM event rules \(both those that come with the base system and any custom rules\), so that all other rules are checked for matching before invoking the default rule. For details on event rules, see [Event rules](create-event-rules.md).

**Parent Topic:**[Configure alert collection from SCOM](../task/t_EMConfigureSCOMConnectorInstance.md)

