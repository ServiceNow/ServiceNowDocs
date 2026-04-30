---
title: Flows that ship with Zero Copy Connector for ERP
description: Zero Copy Connector for ERP includes two ERP \(Enterprise Resource Planning\) flows that run automatically.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Zero Copy Connector for ERP reference, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Flows that ship with Zero Copy Connector for ERP

Zero Copy Connector for ERP includes two ERP \(Enterprise Resource Planning\) flows that run automatically.

You don't need to do anything to activate the flows, but you can customize them in Workflow Studio if you want. For example, to change the time that they run daily. For more information, see [Edit a flow](https://www.servicenow.com/docs/access?context=flow-edit&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Note:** Zero Copy Connector for ERP appears as **ERP Integration** when you work with it in Workflow Studio.

The flows that Zero Copy Connector for ERP automatically runs are:

-   **Get SAP BAPIs and tables when system becomes active**: This flow is triggered automatically as soon as the ERP heartbeat for an ERP system is live. It detects and retrieves the available BAPIs \(Business Application Programming Interface\) and tables for use when managing models. This flow also reads the OData catalog service if the OData heartbeat is successful.
-   **ETL SAP BAPIs and Tables From all systems**: This flow calls the **Get SAP BAPIs and tables when system becomes active** flow every night to retrieve any changes to available BAPIs and tables on the ERP system.

The flows save their changes to the following tables:

-   sn\_erp\_integration\_sap\_tables\_list
-   sn\_erp\_integration\_sap\_bapi\_list\_list

**Parent Topic:**[Zero Copy Connector for ERP reference](erp-integration-reference.md)

