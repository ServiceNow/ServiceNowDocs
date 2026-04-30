---
title: View and update your SAP Solution Manager certificate
description: View your SAP Solution Manager certificate, and update the certificate if necessary.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAP Solution Manager setup configurations, SAP configurations enabling the SAP Solution Manager connector, Configure SAP Solution Manager connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
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

    ![SSL Client UI](../image/sap-solman-certificate-update.png)

    The ICM module restarts.


**Parent Topic:**[SAP Solution Manager setup configurations](../concept/sap-solman-configurations.md)

