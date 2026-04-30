---
title: Next steps after extracting data from your ERP system using Zero Copy Connector for ERP
description: After you identify and extract ERP data with Zero Copy Connector for ERP, you can use that data on the ServiceNow AI Platform as the data source for products and apps.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extract, replatform, source, app]
breadcrumb: [Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Next steps after extracting data from your ERP system using Zero Copy Connector for ERP

After you identify and extract ERP data with Zero Copy Connector for ERP, you can use that data on the ServiceNow AI Platform as the data source for products and apps.

## Use retrieved ERP data in flows

Build flows in Workflow Studio to specify details for when you query or update the ERP \(Enterprise Resource Planning\) system.

For example, you can generate a record for each response from the ERP system, making that data available for use on the ServiceNow AI Platform. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).

## Build a ServiceNow app that consumes ERP data

ERP data from the system of record is available in the remote tables and ERP extraction tables that you configure in Zero Copy Connector for ERP. You can also use table transform maps to put extracted ERP data into a Glide table.

After ERP data is available on tables in the ServiceNow AI Platform, you can use those tables as the foundation for app builders. For example, you can use ERP tables when you create applications in ServiceNow Studio.

## ServiceNow low- and pro-code builders

Use any of the following ServiceNow builders to create apps using custom data:

-   [ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Flows in Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-flows&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Playbooks in Workflow Studio](https://www.servicenow.com/docs/access?context=exploring-process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Workspace Builder](https://www.servicenow.com/docs/access?context=workspace-builder-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

## Using Glide to query ERP data

You can also access data from the system of record through the Glide API.

For more information, see [Sample Glide query for ERP data in Zero Copy Connector for ERP](../reference/erp-canvas-sample-glide-query-code.md).

**Parent Topic:**[Using Zero Copy Connector for ERP](work-with-erp-systems-connections-and-remote-tables.md)

