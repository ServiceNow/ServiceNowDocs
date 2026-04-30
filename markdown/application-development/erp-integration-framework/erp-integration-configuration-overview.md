---
title: Configuring ERP Data Hub
description: Install ERP Data Hub to configure connections to ERP \(Enterprise Resource Planning\) systems of record, as well as other ServiceNow products, such as ERP Customization Mining, Procurement for Field Service Management, and Process Mining.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Configuring ERP Data Hub

Install ERP Data Hub to configure connections to ERP \(Enterprise Resource Planning\) systems of record, as well as other ServiceNow products, such as ERP Customization Mining, Procurement for Field Service Management, and Process Mining.

ERP Data Hub uses basic authentication to connect a ServiceNow instance with an instance on the system of record \(such as SAP\).

After you configure a connection, you can read and update the system of record with ERP Data Hub using ERP models, and create remote tables and extraction tables.

Additionally, you can use ERP Customization Mining \(ERP-CM\) to identify legacy applications that are good candidates for replatforming, making their data immediately available on the ServiceNow AI Platform. For more information, see [ERP Customization Mining \(ERP-CM\)](../../erp-customization-mining/concept/erp-customization-mining-overview.md).

## ERP Data Hub

![ERP Data Hub workflow](../image/erpc-infographic-update.png)

## Connecting to multiple instances

The number of ERP connections you can have per ServiceNow instance depends on your license. If you have the ERP-CM license, you get one connection per instance.

-   **[Requirements for installing ERP Data Hub](../reference/erpc-prereqs-for-installation.md)**  
Before you install ERP Data Hub, you must complete several configurations, on both the ERP \(Enterprise Resource Planning\) system and on the ServiceNow AI Platform.
-   **[Install ERP Data Hub](../task/install-erp-integration.md)**  
Install the ERP Data Hub \(Enterprise Resource Planning\) application \(sn\_erp\_integration\) if you have the admin role from the ServiceNow Store.
-   **[Run Guided Setup for ERP Data Hub](../task/erp-canvas-guided-setup.md)**  
Run the Guided Setup to configure ERP Data Hub.
-   **[Configure the ERP Data Hub credentials and connection](../task/set-up-erp-integration-connection.md)**  
Connect ERP Data Hub to a system of record \(such as SAP\) directly or using a load balancer to enable access to the ERP \(Enterprise Resource Planning\) system. You must select an existing, configured connection when you set up an ERP system.
-   **[ERP Data Hub roles](../reference/erp-canvas-roles.md)**  
Administrators assign roles to give team members permission to configure or use ERP Data Hub.
-   **[Working with ERP systems in ERP Data Hub](erp-canvas-work-with-systems.md)**  
An ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system of record. For example, sales orders or vendor invoices.

**Parent Topic:**[ERP Data Hub](erp-integration-overview.md)

