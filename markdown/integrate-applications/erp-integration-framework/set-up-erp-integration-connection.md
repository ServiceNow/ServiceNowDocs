---
title: Connect to a system of record from Zero Copy Connector for ERP
description: Connect Zero Copy Connector for ERP \(Enterprise Resource Planning\) to a system of record, such as SAP, directly or using a load balancer to enable access to the ERP system.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, connect, configure, system, load, balancer, connect, credential]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Connect to a system of record from Zero Copy Connector for ERP

Connect Zero Copy Connector for ERP \(Enterprise Resource Planning\) to a system of record, such as SAP, directly or using a load balancer to enable access to the ERP system.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Identify an existing connection to use or create a connection. For more information, see [Get started with connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-information.md) and [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-https-connection.md).

Note the following:

-   You must specify a connection and login credential to be used simultaneously. That is, the connection you configure uses the defined login credentials for the connection.
-   The credentials you specify for the Zero Copy Connector for ERP connection must match the service user credentials in the system of record.

## About this task

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP systems list by selecting the systems icon ![](../image/erp-systems-icon-sidebar.png) in the side panel.

3.  Open a system record.

4.  Add the configured connection.

    To see a list of all available RFC or HTTP connections, select the search for record icon \(magnifying glass\) in the field.

    ![New system record with filled in fields.](../image/erp-set-up-connection1.png)

5.  Select **Save**.

    For more information, see [Zero Copy Connector for ERP new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).


**Parent Topic:**[Configuring Zero Copy Connector for ERP](../concept/erp-integration-configuration-overview.md)

