---
title: Configuring Zero Copy Connector for ERP
description: Install Zero Copy Connector for ERP to configure connections to ERP \(Enterprise Resource Planning\) systems of record, as well as other ServiceNow products, such as ERP Semantic Mining, Procurement for Field Service Management, and Process Mining.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Configuring Zero Copy Connector for ERP

Install Zero Copy Connector for ERP to configure connections to ERP \(Enterprise Resource Planning\) systems of record, as well as other ServiceNow products, such as ERP Semantic Mining, Procurement for Field Service Management, and Process Mining.

Zero Copy Connector for ERP uses basic authentication to connect a ServiceNow instance with an instance on the system of record \(such as SAP\).

After you configure a connection, you can read and update the system of record with Zero Copy Connector for ERP using ERP models, and create remote tables and extraction tables.

Additionally, you can use ERP Semantic Mining \(ERP-CM\) to identify legacy applications that are good candidates for replatforming, making their data immediately available on the ServiceNow AI Platform. For more information, see [ERP Semantic Mining \(ERP-CM\)](../../erp-customization-mining/concept/erp-customization-mining-overview.md).

## Zero Copy Connector for ERP

![Zero Copy Connector for ERP workflow](../image/erpc-infographic-update.png)

## Connecting to multiple instances

The number of ERP connections you can have per ServiceNow instance depends on your license. If you have the ERP-CM license, you get one connection per instance.

-   **[Requirements for installing Zero Copy Connector for ERP](../reference/erpc-prereqs-for-installation.md)**  
Before you install Zero Copy Connector for ERP, you must complete several configurations, on both the ERP \(Enterprise Resource Planning\) system and on the ServiceNow AI Platform.
-   **[Install Zero Copy Connector for ERP](../task/install-erp-integration.md)**  
Install the Zero Copy Connector for ERP \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.
-   **[Run Guided Setup for Zero Copy Connector for ERP](../task/erp-canvas-guided-setup.md)**  
Run the Guided Setup to configure Zero Copy Connector for ERP.
-   **[Configure the Zero Copy Connector for ERP credentials and connection](../task/set-up-erp-integration-connection.md)**  
Connect Zero Copy Connector for ERP to a system of record \(such as SAP\) directly or using a load balancer to enable access to the ERP \(Enterprise Resource Planning\) system. You must select an existing, configured connection when you set up an ERP system.
-   **[Use an SNC connection in Zero Copy Connector for ERP](erpc-use-an-snc-connection-in-erp-canvas.md)**  
Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.
-   **[Zero Copy Connector for ERP roles](../reference/erp-canvas-roles.md)**  
Administrators assign roles to give team members permission to configure or use Zero Copy Connector for ERP.
-   **[Working with ERP systems in Zero Copy Connector for ERP](erp-canvas-work-with-systems.md)**  
An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.
-   **[Obtaining Zero Copy Connector for ERP metrics and statistics](erpc-obtaining-erp-canvas-metrics-and-statistics.md)**  
Use the Zero Copy Connector for ERP home page dashboard to obtain statistics about transactions and view info to help you troubleshoot.

**Parent Topic:**[Zero Copy Connector for ERP](erp-integration-overview.md)

