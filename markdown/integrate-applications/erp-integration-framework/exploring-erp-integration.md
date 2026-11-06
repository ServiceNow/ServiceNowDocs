---
title: Exploring Zero Copy Connector for ERP
description: Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to connect to an ERP system to read, update, create, and extract data for use on the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/erp-integration-framework/exploring-erp-integration.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, benefit, feature]
breadcrumb: [Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP

Zero Copy Connector for ERP \(Enterprise Resource Planning\) enables you to connect to an ERP system to read, update, create, and extract data for use on the ServiceNow AI Platform.

## Zero Copy Connector for ERP overview

Zero Copy Connector for ERP helps you identify custom Enterprise Resource Planning \(ERP\) apps and fields in an ERP system to access their data on the ServiceNow AI Platform.

Legacy ERP systems can have old, complex custom code and data. The old information requires more time and effort to move to newer versions of the ERP system. Use Zero Copy Connector for ERP to find and replace custom code with digitized workflows, resulting in a clean ERP core. This is the process of ERP modernization.

Zero Copy Connector for ERP supports the following ERP systems:

-   SAP ECC
-   SAP S/4HANA
-   SAP S/4HANA Cloud
-   SuccessFactors
-   Workday
-   Oracle E-Business Suite \(EBS\)

The replatforming of legacy code enables innovation on top of the ERP system without knowledge of the legacy system. Administrators and developers are then relieved of time-consuming efforts to create database views or endpoints in the ERP system and can work on other projects, such as migration.

Use models as the foundation for ERP apps. These models include ERP system data in remote tables and extraction tables. The models enable you to perform read, update, and create operations on the ERP system. After you create models, you can use the extracted and transformed data to build apps that access the models. For example, use ServiceNow Studio to build apps or use the ERP data in flows within Workflow Studio.

Zero Copy Connector for ERP content packs are sets of predefined models and process extensions that are useful examples for developers with little or no SAP domain knowledge. Content packs accelerate the work so that building use cases involving SAP data becomes a faster process that more developers can accomplish. For more information, see [Accelerating SAP integrations with Zero Copy Connector for ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-content-packs.md).

**Note:** Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system, and remains protected there.

## Benefits of Zero Copy Connector for ERP

The unified data model of the ServiceNow AI Platform helps integrate ERP data into the ServiceNow AI Platform. Zero Copy Connector for ERP streamlines ERP data management, making it accessible and actionable within the ServiceNow AI Platform and ServiceNow instances. Configure extraction tables to pull custom or delta data from the ERP system regularly.

|Benefit|Feature|
|-------|-------|
|Configure connections to the ERP system|[Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md)|
|Build ERP models to create read, update, and create operations and organize mirrored ERP data|[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)|
|Work with and query remote tables to view ERP data on the ERP system|[Using ERP remote tables in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-work-with-remote-tables.md)|
|Configure extraction tables to pull custom data from the ERP system regularly|[Extracting and transforming ERP data with Zero Copy Connector for ERP extraction tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erp-canvas-extraction-tables.md)|
|Use ERP data in ServiceNow Studio, Workflow Studio flows and playbooks, Table Builder, UI Builder, and Workspace Builder|[Next steps after extracting data from your ERP system using Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/erp-integration-framework/erpi-next-steps-replatforming.md)|

## Helpful resources

The following ServiceNow resources can help:

-   **\[Omitted image "bus-video-play.svg"\] Alt text: Video**

    Watch [Unlock the full potential of your ERP system](https://www.youtube.com/watch?v=R66HqYLfEc8&t=8s).

-   **\[Omitted image "bus-video-play.svg"\] Alt text: Video**

    Watch [Clean core ERP](https://www.youtube.com/watch?v=oz0eIWupiqs&t=1033s).


