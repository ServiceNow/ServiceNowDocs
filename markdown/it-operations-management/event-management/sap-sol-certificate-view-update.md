---
title: View and update your SAP Solution Manager certificate
description: View your SAP Solution Manager certificate, and update the certificate if necessary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/sap-sol-certificate-view-update.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, Enable SAP connector configurations, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View and update your SAP Solution Manager certificate

View your SAP Solution Manager certificate, and update the certificate if necessary.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Connect to SAP on client 00.

2.  Enter the `strust` transaction.

3.  In the Trust Manager UI, open the SSL client.

4.  Import the SSL certificate and save it.

5.  Use the `smicm` transaction to enable the system to work with both HTTP and HTTPS clients.

6.  Navigate to **Administration** &gt; **ICM** &gt; **Exit Hard** &gt; **Global**.

    \[Omitted image "sap-solman-certificate-update.png"\] Alt text: SSL Client UI

    The ICM module restarts.


**Parent Topic:**[SAP Solution Manager setup configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/sap-solman-configurations.md)

