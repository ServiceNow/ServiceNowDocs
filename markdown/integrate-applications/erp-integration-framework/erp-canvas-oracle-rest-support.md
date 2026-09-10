---
title: REST API support for Oracle E-Business Suite
description: REST APIs exchange data with Oracle E-Business Suite \(EBS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-oracle-rest-support.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, oracle, ebs, rest, openapi]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# REST API support for Oracle E-Business Suite

REST APIs exchange data with Oracle E-Business Suite \(EBS\).

## Oracle coverage

REST support covers Oracle EBS 12.2 or later. Data flows directly from the Oracle ERP system to the target system.

For general REST connectivity in Zero Copy Connector for ERP, see [Connecting to other ERP systems using REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-use-rest.md).

## Service discovery

You can discover and list the REST APIs and services available on the Oracle ERP system. The list includes both active and inactive services, so you can see which services exist before you enable them.

## Supported operations

Oracle EBS models with read operation are supported. There is no restriction on operations when using scriptable API.

\[Omitted image "erp-add-oracle-rest-entity-to-model1.jpg"\] Alt text: Add entity page with oracle typed into select service field and two options displayed.

## Importing service definitions

Instead of defining each service manually, you can import a service definition to define REST services dynamically. Oracle EBS Integrated SOA Gateway services are described by WADL documents. For more information, see [WADL service support for Oracle E-Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-wadl-support.md). To add a service manually, see [Add a WADL service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-wadl-service-manually.md).

## Configuring REST operations

Each REST operation supports custom input parameters, request headers, and payload templates, so you can shape the request to match what the Oracle service expects.

For the steps, see [Add an Oracle REST entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-an-oracle-rest-entity-to-a-model-operation.md).

## Authentication

REST connections to Oracle E-Business Suite support basic authentication. For details, see [Authentication methods for Oracle REST connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-authentication-methods.md).

## Fault handling

REST faults are reported with detailed error information so you can identify which request failed and why. For more information, see [Monitor Zero Copy Connector for ERP transactions and logged errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/monitor-erp-data-hub-logged-extraction-and-remote-lookup-transactions.md).

