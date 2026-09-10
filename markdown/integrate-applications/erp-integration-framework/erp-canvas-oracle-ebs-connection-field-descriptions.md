---
title: Oracle E-Business Suite connection field descriptions
description: The Oracle E-Business Suite connection in Zero Copy Connector for ERP contains endpoint, credential, and Oracle context values that determine which data the connection can read.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-connection-field-descriptions.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, oracle, ebs, connection, field, isg]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Oracle E-Business Suite connection field descriptions

The Oracle E-Business Suite connection in Zero Copy Connector for ERP contains endpoint, credential, and Oracle context values that determine which data the connection can read.

For process details, see [Create an Oracle E-Business Suite connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-create-an-oracle-ebs-connection.md).

## Connection field descriptions

|Field|Description|
|-----|-----------|
|ISG base URL|Base URL of the Oracle Integrated SOA Gateway \(ISG\) REST endpoint. HTTPS is required.|
|MID Server|MID Server that routes requests to the Oracle E-Business Suite instance.|

## Oracle context parameter descriptions

These values are sent with each request so that Oracle E-Business Suite evaluates the request in the correct business context.

|Parameter|Description|
|---------|-----------|
|Org ID|Identifier of the Oracle E-Business Suite operating unit that the request applies to.|
|Ledger ID|Identifier of the Oracle E-Business Suite ledger that the request applies to.|
|Responsibility|Oracle E-Business Suite responsibility that determines which functions and data the request can access.|
|NLS Language|Language that Oracle E-Business Suite uses for the response, set using the Oracle National Language Support value.|

