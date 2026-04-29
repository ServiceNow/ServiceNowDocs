---
title: Configure the alert inbox in SAP Solution Manager
description: Configure SAP solution manager to retrieve alerts in the system by enabling the alert inbox with the SOA manager.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, Enable SAP connector configurations, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the alert inbox in SAP Solution Manager

Configure SAP solution manager to retrieve alerts in the system by enabling the alert inbox with the SOA manager.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to SOA MANAGER in your solution manager: `/sap/bc/webdynpro/sap/appl_soap_management?sap-client=XXX&sap-language=EN#`

2.  Select **Simplified Web Service Configuration**, then validate the form to activate the service.

    You must use simplified mode else the resulting web services is different with other modes and not compatible with the connector.

    ![SOA Management page](../image/sap-soa-mgmt.png)

3.  Select **Search**.

4.  Check the row with the creation type **Simple consumer related**.

    If anything goes wrong, check [Configuring a Service Provider \(Simplified\)](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/684cffda9cbc4187ad7dad790b03b983/7ef0f7eb600a46c78aae7f3c2346d117.html?version=1709%20001)


## What to do next

View alerts generated in SAP Solution Manager to see any pressing issues, as described in [View alerts in the SAP Solution Manager inbox](sap-view-alerts.md).

**Parent Topic:**[SAP Solution Manager setup configurations](../concept/sap-solman-configurations.md)

