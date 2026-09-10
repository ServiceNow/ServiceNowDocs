---
title: Create an Oracle E-Business Suite connection
description: Configure a connection to Oracle E-Business Suite \(EBS\) 12.2 or later so that Zero Copy Connector for ERP can read data from your Oracle ERP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-create-an-oracle-ebs-connection.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, oracle, ebs, connection, isg, mid server]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Create an Oracle E-Business Suite connection

Configure a connection to Oracle E-Business Suite \(EBS\) 12.2 or later so that Zero Copy Connector for ERP can read data from your Oracle ERP system.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Confirm that you have the following:

-   An Oracle EBS 12.2 or later instance with the Integrated SOA Gateway \(ISG\) enabled.
-   The base URL of the ISG REST endpoint.
-   Credentials that are authorized to call the ISG REST services.
-   A configured MID Server that can reach the ISG endpoint. For more information, see [Configuring MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configure-mid-server.md).
-   The Oracle EBS context values for the data you want to read: operating unit \(Org ID\), ledger, responsibility, and language.

## About this task

Oracle EBS connections use REST and the HTTP connection template. For background, see [Oracle E-Business Suite support in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-overview.md).

## Procedure

1.  Create a connection and credential alias for the Oracle EBS system.

    For the general process, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connection-alias.md).

2.  Enter the ISG base URL and the credentials for the Oracle EBS system.

3.  Select the MID Server that routes requests to the ISG endpoint.

4.  Enter the Oracle EBS context parameters.

    For the field values, see [Oracle E-Business Suite connection field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-connection-field-descriptions.md).

5.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

6.  Create an ERP system and select the connection alias you created.

    For the general process, see [Create an ERP system in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/create-an-erp-system.md).

7.  In the **ERP software** field, select **Oracle EBS**.

    \[Omitted image "erp-canvas-oracle-ebs-connection1.png"\] Alt text: Oracle EBS system record with ERP software field highlighted.

8.  Select **Submit**.

9.  Verify the connection.

    For more information, see [View Zero Copy Connector for ERP system heartbeat information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/view-erp-system-heartbeat-information.md).


## Result

The Oracle EBS system appears in the ERP systems list and is available when you build models.

## What to do next

Add a WADL service to generate model entities and fields automatically from the service definition. For more information, see [WADL service support for Oracle E-Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-wadl-support.md) and [Add a WADL service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-wadl-service-manually.md).

