---
title: Configuring ERP Canvas
description: Install ERP Canvas to configure connections to ERP \(Enterprise Resource Planning\) systems of record, as well as other ServiceNow products, such as ERP Customization Mining, Procurement for Field Service Management, and Process Mining.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erp-integration-configuration-overview.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# Configuring ERP Canvas

Install ERP Canvas to configure connections to ERP \(Enterprise Resource Planning\) systems of record, as well as other ServiceNow products, such as ERP Customization Mining, Procurement for Field Service Management, and Process Mining.

ERP Canvas uses basic authentication to connect a ServiceNow instance with an instance on the system of record \(such as SAP\).

After you configure a connection, you can read and update the system of record with ERP Canvas using ERP models, and create remote tables and extraction tables.

Additionally, you can use ERP Customization Mining \(ERP-CM\) to identify legacy applications that are good candidates for replatforming, making their data immediately available on the ServiceNow AI Platform. For more information, see [ERP Customization Mining \(ERP-CM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-customization-mining/erp-customization-mining-overview.md).

## ERP Canvas

\[Omitted image "erpc-infographic-update.png"\] Alt text: ERP Canvas workflow

## Connecting to multiple instances

The number of ERP connections you can have per ServiceNow instance depends on your license. If you have the ERP-CM license, you get one connection per instance.

-   **[Requirements for installing ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-prereqs-for-installation.md)**  
Before you install ERP Canvas, you must complete several configurations, on both the ERP \(Enterprise Resource Planning\) system and on the ServiceNow AI Platform.
-   **[Install ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/install-erp-integration.md)**  
Install the ERP Canvas \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.
-   **[Run Guided Setup for ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-guided-setup.md)**  
Run the Guided Setup to configure ERP Canvas.
-   **[Configure the ERP Canvas credentials and connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/set-up-erp-integration-connection.md)**  
Connect ERP Canvas to a system of record \(such as SAP\) directly or using a load balancer to enable access to the ERP \(Enterprise Resource Planning\) system. You must select an existing, configured connection when you set up an ERP system.
-   **[Use an SNC connection in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-use-an-snc-connection-in-erp-canvas.md)**  
Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.
-   **[ERP Canvas roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-roles.md)**  
Administrators assign roles to give team members permission to configure or use ERP Canvas.
-   **[Working with ERP systems in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-work-with-systems.md)**  
An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
-   **[Obtaining ERP Canvas metrics and statistics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erpc-obtaining-erp-canvas-metrics-and-statistics.md)**  
Use the ERP Canvas home page dashboard to obtain statistics about transactions and view info to help you troubleshoot.

**Parent Topic:**[ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-integration-overview.md)

