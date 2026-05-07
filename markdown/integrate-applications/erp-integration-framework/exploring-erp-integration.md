---
title: Exploring Zero Copy Connector for ERP
description: Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to connect to an ERP system to read, update, create, and extract data for use on the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, benefit, feature]
breadcrumb: [Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP

Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to connect to an ERP system to read, update, create, and extract data for use on the ServiceNow AI Platform.

## Zero Copy Connector for ERP overview

Zero Copy Connector for ERP helps you identify custom Enterprise Resource Planning \(ERP\) apps and fields in a system of record \(such as SAP\) to access their data on the ServiceNow AI Platform.

Zero Copy Connector for ERP offers a unified data model for ERP systems. Zero Copy Connector for ERP enables you to manage tables that contain both standard and custom fields grouped within ERP models. You can send updates to and extract data from ERP tables on the system of record. Store extracted data in a remote table or an extraction table, depending on the size of datasets and refresh needs.

-   Remote tables get their records from running an associated script against an external data source.
-   Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

**Note:** Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Benefits of Zero Copy Connector for ERP

The unified data model of the ServiceNow AI Platform helps with the seamless integration of ERP data into the ServiceNow AI Platform. Zero Copy Connector for ERP streamlines ERP data management, making it accessible and actionable within the ServiceNow AI Platform and ServiceNow instances.

|Benefit|Feature|
|-------|-------|
|Configure connections to the system of record|[Working with ERP systems in Zero Copy Connector for ERP](erp-canvas-work-with-systems.md)|
|Build ERP models to create read, update, and create operations and organize mirrored ERP data|[Building and managing models to work with ERP data](work-with-erp-data-models.md)|
|Work with and query remote tables to view ERP data on the system of record|[Using ERP remote tables in Zero Copy Connector for ERP](erp-canvas-work-with-remote-tables.md)|
|Configure extraction tables to pull custom data from the ERP system regularly|[Extracting and transforming data in Zero Copy Connector for ERP](erp-canvas-extraction-tables.md)|
|Use ERP data in ServiceNow Studio, Workflow Studio flows and playbooks, Table Builder, UI Builder, and Workspace Builder.|[Next steps after extracting data from your ERP system using Zero Copy Connector for ERP](erpi-next-steps-replatforming.md)|

## Helpful resources

Some ServiceNow resources that can provide you with helpful information are:

-   **![](../../../reuse/icons/brand-icons/bus-video-play.svg) Video**

    Watch [Unlock the full potential of your ERP system](https://www.youtube.com/watch?v=R66HqYLfEc8&t=8s).

-   **![](../../../reuse/icons/brand-icons/bus-video-play.svg) Video**

    Watch [Clean core ERP with App Engine](https://www.youtube.com/watch?v=oz0eIWupiqs&t=1033s).


-   **[Exploring Zero Copy Connector for ERP systems](exploring-erp-systems.md)**  
Create an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to connect to an external ERP system.
-   **[Exploring Zero Copy Connector for ERP content packs](exploring-erp-content-packs.md)**  
Use Zero Copy Connector for ERP \(Enterprise Resource Planning\) content packs to view examples and create an ERP model faster.
-   **[Exploring Zero Copy Connector for ERP models](exploring-erp-models.md)**  
Build ERP \(Enterprise Resource Planning\) models in Zero Copy Connector for ERP to create read, update, and create operations and organize mirrored ERP data.
-   **[Exploring Zero Copy Connector for ERP remote tables and extraction tables](exploring-erp-remote-tables-and-extraction-tables.md)**  
Configure remote tables and extraction tables to work with data from the ERP \(Enterprise Resource Planning\) system of record.
-   **[Identifying ERP candidates to replatform with Zero Copy Connector for ERP](erpi-and-ecm-together.md)**  
Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.

**Parent Topic:**[Zero Copy Connector for ERP](erp-integration-overview.md)

