---
title: Oracle E-Business Suite support in Zero Copy Connector for ERP
description: Zero Copy Connector for ERP reads business data from Oracle E-Business Suite \(EBS\) through REST services, without copying the data into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-overview.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [oracle, ebs, e-business suite, isg, zero copy connector for erp, oracle e-business suite, oracle ebs, connect to oracle ebs, oracle ebs erp system, oracle ebs rest services, integrated soa gateway, oracle ebs mid server]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Oracle E-Business Suite support in Zero Copy Connector for ERP

Zero Copy Connector for ERP reads business data from Oracle E-Business Suite \(EBS\) through REST services, without copying the data into ServiceNow.

## Oracle as an ERP software family

Oracle EBS is available as a selectable ERP software option when you create an ERP system. Oracle forms its own ERP software family, separate from SAP.

For the steps to create the system, see [Create an Oracle E-Business Suite connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-create-an-oracle-ebs-connection.md).

## Supported protocols

Oracle EBS connections support REST only. RFC, IDoc, and OData aren't supported.

Because Oracle EBS uses REST, the connection uses the HTTP connection template and reports HTTP heartbeat information rather than RFC heartbeat information.

## Connection process

Requests are routed through a MID Server.

## Building models from Oracle EBS data

Oracle EBS metadata discovery is manual.

Only read operations on Oracle EBS models are supported in the **Use ERP Data** action.

## Security

For information about role requirements and transport security for Oracle EBS connections, see [Security for Oracle E-Business Suite connections in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-security.md).

