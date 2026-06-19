---
title: Configure RFC in SAP Solution Manager
description: As part of enabling communication with Event Management, you must create a Remote Function Call \(RFC\) in the SAP Solution Manager and install a transport.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/configure-sap-solution-mgr.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
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
    |RFC Destination|MID\_EVENT\_COLLECTOR2|
    |Target Host|Name of the MID Server.|
    |Service No|Listener port on the MID Server|
    |Path Prefix|The URL of the MID Server transform script: `/api/mid/em/inbound_event?Transform=TransformEvents_SAPSolman`|

    \[Omitted image "sap-solman-event-collector.png"\] Alt text: SAP Event Collector form

2.  On the **Logon &amp; Security** tab, select **Basic Authentication** and enter your Event Management logon credentials in the **User** and **Password** fields.

    \[Omitted image "sap-solman-logon-security-tab.png"\] Alt text: SAP Logon and Security tab page

    A custom SAP BADI \(Business Add-in\) named Z\_ALRT\_REACTION\_IMPL is created and stored as a workbench transport request. After installation, this BADI calls the RFC to connect to Event Management.

    \[Omitted image "sap-solman-workbench-transport-request.png"\] Alt text: Workbench transport request


**Parent Topic:**[SAP Solution Manager setup configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/sap-solman-configurations.md)

