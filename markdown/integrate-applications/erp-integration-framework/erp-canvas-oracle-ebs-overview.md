---
title: Oracle E-Business Suite support in Zero Copy Connector for ERP
description: Zero Copy Connector for ERP reads business data from Oracle E-Business Suite \(EBS\) through REST services, without copying the data into ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-overview.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [oracle, ebs, e-business suite, isg, zero copy connector for erp, oracle e-business suite, oracle ebs, connect to oracle ebs, oracle ebs erp system, oracle ebs rest services, integrated soa gateway, oracle ebs mid server]
breadcrumb: [Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Oracle E-Business Suite support in Zero Copy Connector for ERP

Zero Copy Connector for ERP reads business data from Oracle E-Business Suite \(EBS\) through REST services, without copying the data into ServiceNow.

## Oracle as an ERP software family

Oracle EBS is available as a selectable ERP software option when you create an ERP system. Oracle forms its own ERP software family, separate from SAP.

For the steps to create the system, see [Create an Oracle E-Business Suite connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-create-an-oracle-ebs-connection.md).

## Supported protocols

Oracle EBS connections support REST only. RFC, IDoc, and OData aren't supported.

Because Oracle EBS uses REST, the connection uses the HTTP connection template and reports HTTP heartbeat information rather than RFC heartbeat information.

## Connection process

Requests are routed through a MID Server.

## Building models from Oracle EBS data

Oracle EBS metadata discovery is manual.

Only read operations on Oracle EBS models are supported in the **Use ERP Data** action.

## Security

For information about role requirements and transport security for Oracle EBS connections, see [Security for Oracle E-Business Suite connections in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-security.md).

-   **[REST API support for Oracle E-Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-rest-support.md)**  
Use REST APIs in Zero Copy Connector for ERP to discover Oracle E-Business Suite \(EBS\) services and build models with read operations.
-   **[WADL service support for Oracle E-Business Suite in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-wadl-support.md)**  
Zero Copy Connector for ERP discovers, parses, and models the custom PL/SQL integration services that Oracle E-Business Suite \(EBS\) describes with WADL documents.
-   **[Security for Oracle E-Business Suite connections in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-security.md)**  
Learn how access control lists \(ACLs\) protect Oracle E-Business Suite \(EBS\) data in Zero Copy Connector for ERP, and which authentication methods Oracle EBS connections support.
-   **[Authentication methods for Oracle REST connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-rest-authentication-methods.md)**  
REST connections to Oracle ERP systems in Zero Copy Connector for ERP support basic authentication.
-   **[Create an Oracle E-Business Suite connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-create-an-oracle-ebs-connection.md)**  
Configure a connection to Oracle E-Business Suite \(EBS\) 12.2 or later so that Zero Copy Connector for ERP can read data from your Oracle ERP system.
-   **[Add a WADL service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-add-a-wadl-service-manually.md)**  
Add an Oracle E-Business Suite \(EBS\) service to a model by supplying its Integrated SOA Gateway alias.
-   **[Add an Oracle REST entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/add-an-oracle-rest-entity-to-a-model-operation.md)**  
Set the input parameters, headers, and payload template for an Oracle Fusion or Oracle E-Business Suite \(EBS\) REST entity. The model then sends the request to the Oracle service.
-   **[Manage input parameters for model operation with Oracle REST entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-oracle-rest.md)**  
Specify how fields on the ERP \(Enterprise Resource Planning\) system map to input parameters and their values. This defines the inputs for an operation that reads, creates, or updates the Oracle ERP system using REST.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.md)

