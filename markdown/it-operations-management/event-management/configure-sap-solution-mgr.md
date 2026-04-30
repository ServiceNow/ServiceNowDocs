---
title: Configure RFC in SAP Solution Manager
description: As part of enabling communication with Event Management, you must create a Remote Function Call \(RFC\) in the SAP Solution Manager and install a transport.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, Enable SAP connector configurations, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure RFC in SAP Solution Manager

As part of enabling communication with Event Management, you must create a Remote Function Call \(RFC\) in the SAP Solution Manager and install a transport.

## Before you begin

Role required: evt\_mgmt\_admin

Download the following .psm files and import them into the SAP Solution Manager system.

-   [https://downloads.docs.servicenow.com/resource/enus/cad/K900249.PSM](https://downloads.docs.servicenow.com/resource/enus/cad/K900249.PSM)
-   [https://downloads.docs.servicenow.com/resource/enus/cad/R900249.PSM](https://downloads.docs.servicenow.com/resource/enus/cad/R900249.PSM)

## Procedure

1.  On the SAP UI, enter the transaction code `SM59` and create a new RFC with the following parameters on the **Technical Settings** tab:

    |SAP Parameter|Value|
    |-------------|-----|
    |Target Host|Name of the MID Server.|
    |Service No|Listener port on the MID Server|
    |Path Prefix|The URL of the MID Server transform script: `/api/mid/em/inbound_event?Transform=TransformEvents_SAPSolman`|

    ![SAP Event Collector form](../image/sap-solman-event-collector.png "Technical Settings tab")

2.  On the **Logon &amp; Security** tab, select **Basic Authentication** and enter your Event Management logon credentials in the **User** and **Password** fields.

    ![SAP Logon and Security tab page](../image/sap-solman-logon-security-tab.png "Logon & Security tab")

    A custom SAP BADI \(Business Add-in\) named Z\_ALRT\_REACTION\_IMPL is created and stored as a workbench transport request. After installation, this BADI calls the RFC to connect to Event Management.

    ![Workbench transport request](../image/sap-solman-workbench-transport-request.png)


**Parent Topic:**[SAP Solution Manager setup configurations](../concept/sap-solman-configurations.md)

