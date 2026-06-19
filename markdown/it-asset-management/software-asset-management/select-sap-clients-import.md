---
title: Select SAP clients to import data
description: Select the Remote Function Call \(RFC\) connections that the SAP ABAP program uses to import data from your SAP clients into the central system and then into your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/select-sap-clients-import.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
keywords: [SAP clients, RFC connection, ABAP program, SAP data import]
breadcrumb: [Set up SAP integration to establish a connection with SAP, Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Select SAP clients to import data

Select the Remote Function Call \(RFC\) connections that the SAP ABAP program uses to import data from your SAP clients into the central system and then into your ServiceNow instance.

## Before you begin

RFC connections must be configured and active in transaction **SM59** before selecting clients. The creation and configuration of RFC connections is a standard SAP Basis procedure performed by the SAP Basis team.

Role required: SAP Basis administrator

## About this task

The Advanced Business Application Programming \(ABAP\) program is a centralized solution that establishes a connection between your SAP system and your ServiceNow instance. After you import the transport files into an SAP client, then that client becomes the central system. The central system uses RFC connections to connect with all other clients and fetch data into the ServiceNow custom tables.

The central system can be an SAP Solution Manager or any other SAP client with an active RFC connection.

## Procedure

1.  Verify that the RFC connection is correctly configured in transaction **SM59**.

    The required fields are **Target Host**, **Instance No.**, **Language**, **Client**, **User**, and **PW Status**.\[Omitted image "sap-client-fields1.png"\] Alt text: Target Host field in RFC connection\[Omitted image "sap-client-fields2.png"\] Alt text: Required fields including Language, Client, User, and PW Status in RFC connection

2.  Run the `/NOW/SAMP_RFC_DETAILS` RFC program to select the list of RFC connections that can import data into your ServiceNow instance.

    The RFC program uses only the selected RFC connections to import data from your SAP clients into the central system.

    \[Omitted image "sap-client-rfc.png"\] Alt text: Options to select RFC connections that can import data into your ServiceNow instance

3.  If you want indirect access data from that RFC system, then select the **Is Indirect Access?** after selecting an RFC list.

    \[Omitted image "sap-client-indirect-access.png"\] Alt text: Report to get the RFC list for ServiceNow showing all the options

4.  Select **Test RFC connection** to verify that the ping test for the RFC connection has passed with a checkmark.

5.  Select **Save to ServiceNow RFC List** to store the selected RFCs in the custom RFC table.

    After saving, the RFC is visible under the **Display RFC List ServiceNow** option in the `/NOW/SAMP_RFC` transaction code.


## What to do next

Activate the OData services and assign a system alias to support OAuth 2.0 authentication for the integration. For details, see [Activate OData services and assign a system alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/activate-odata-services-sap.md).

