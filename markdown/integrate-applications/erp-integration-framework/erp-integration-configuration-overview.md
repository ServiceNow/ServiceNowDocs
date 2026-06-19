---
title: Configuring Zero Copy Connector for ERP
description: Install Zero Copy Connector for ERP \(Enterprise Resource Planning\) to configure connections to ERP systems of record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, configuration, connection]
breadcrumb: [Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Configuring Zero Copy Connector for ERP

Install Zero Copy Connector for ERP \(Enterprise Resource Planning\) to configure connections to ERP systems of record.

Zero Copy Connector for ERP uses basic authentication to connect a ServiceNow instance with an instance on the system of record \(such as SAP\).

After you configure a connection, you can read and update the system of record and create records with Zero Copy Connector for ERP using ERP models. You can also create remote tables and extraction tables.

Additionally, you can use ERP Semantic Mining to identify legacy applications that are good candidates for replatforming, making their data immediately available on the ServiceNow AI Platform. For more information, see [ERP Semantic Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-customization-mining/erp-customization-mining-overview.md).

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## Connecting to multiple instances

The number of ERP connections you can have per ServiceNow instance depends on your license.

-   **[Requirements for installing Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-installation.md)**  
Before you install Zero Copy Connector for ERP \(Enterprise Resource Planning\), you must complete several configurations, on both the ERP system and on the ServiceNow AI Platform.
-   **[Install Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/install-erp-integration.md)**  
Install Zero Copy Connector for ERP from the ServiceNow Store, so that you can connect to SAP and other ERP systems and start building models on the ServiceNow AI Platform.
-   **[Connect to a system of record from Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/set-up-erp-integration-connection.md)**  
Connect Zero Copy Connector for ERP \(Enterprise Resource Planning\) to a system of record, such as SAP, directly or using a load balancer to enable access to the ERP system.
-   **[Connect Zero Copy Connector for ERP to SAP using OData and HTTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-use-odata-and-http-connection.md)**  
Extract data securely from ERP OData v2 APIs for use in remote tables and extraction tables. OData connects to SAP via HTTP.
-   **[Use an SNC \(Secure Network Communication\) connection in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-use-an-snc-connection-in-erp-canvas.md)**  
Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.
-   **[Zero Copy Connector for ERP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-roles.md)**  
Assign Zero Copy Connector for ERP roles to give team members the access they must have to configure ERP systems, build models, or read ERP data.
-   **[Zero Copy Connector for ERP and security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-and-security.md)**  
In addition to role-based security and access control, Zero Copy Connector for ERP \(Enterprise Resource Planning\) protects personally identifiable data in other ways.
-   **[Guided tours in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/guided-tours-in-erp-canvas.md)**  
Learn about Zero Copy Connector for ERP guided tours including how to connect to an external ERP guided tours, including how to access and take them to build your knowledge of Zero Copy Connector for ERP.
-   **[Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md)**  
A Zero Copy Connector for ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
-   **[Obtaining Zero Copy Connector for ERP metrics and statistics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-obtaining-erp-canvas-metrics-and-statistics.md)**  
Use the Zero Copy Connector for ERP \(Enterprise Resource Planning\) home page dashboard to obtain statistics about transactions and information to help you troubleshoot.

**Parent Topic:**[Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-integration-overview.md)

