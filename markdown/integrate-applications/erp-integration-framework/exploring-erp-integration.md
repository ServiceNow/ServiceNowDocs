---
title: Exploring Zero Copy Connector for ERP
description: Zero Copy Connector for ERP \(enterprise resource planning\) enables you to connect to an ERP system to read, update, create, and extract data for use on the ServiceNow AI Platform.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, benefit, feature]
breadcrumb: [Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP

Zero Copy Connector for ERP \(enterprise resource planning\) enables you to connect to an ERP system to read, update, create, and extract data for use on the ServiceNow AI Platform.

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
|Work with and query remote tables to view ERP data on the system of record||
|Configure extraction tables to pull custom data from the ERP system regularly||
|Use ERP data in ServiceNow Studio, Workflow Studio flows and playbooks, Table Builder, UI Builder, and Workspace Builder.||

## Helpful resources

Some ServiceNow resources that can provide you with helpful information are:

-   **![](../../../reuse/icons/brand-icons/bus-video-play.svg) Video**

    Watch [Unlock the full potential of your ERP system](https://www.youtube.com/watch?v=R66HqYLfEc8&t=8s).

-   **![](../../../reuse/icons/brand-icons/bus-video-play.svg) Video**

    Watch [Clean core ERP with App Engine](https://www.youtube.com/watch?v=oz0eIWupiqs&t=1033s).


-   **[Identifying ERP candidates to replatform with Zero Copy Connector for ERP](erpi-and-ecm-together.md)**  
Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.
-   **[zero-copy-connector-for-erp-tutorial-po-lookup.md](zero-copy-connector-for-erp-tutorial-po-lookup.md)**  


**Parent Topic:**[Zero Copy Connector for ERP](erp-integration-overview.md)

