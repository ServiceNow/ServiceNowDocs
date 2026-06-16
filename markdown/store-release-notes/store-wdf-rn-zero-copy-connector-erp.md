---
title: Zero Copy Connector for ERP release notes
description: Version history for the Zero Copy Connector for ERP application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-wdf-rn-zero-copy-connector-erp.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Workflow Data Fabric release notes, ServiceNow Store release notes]
---

# Zero Copy Connector for ERP release notes

Version history for the Zero Copy Connector for ERP application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 10.1.0 - June 2026**

    Defect fixing and quality improvement

-   **Version 10.0.9 - May 2026**
    -   New in the Australia release:
        -   Support for REST APIsConnect to ERPs using REST APIs for read and write operations.
        -   Improved AI Agent for SAP OData services
            -   Discover relevant SAP OData v2 services for your models using the OData Services Recommender agentic AI workflow. This reduces missed integration opportunities and accelerates development by finding standard SAP capabilities that align with your use cases.
        -   Implement and deploy faster with the Recruit to Retire contact packUse the Recruit to Retire content pack containing models to get Zero Copy Connector for ERP running on your instance faster.
        -   Improved mapping visualization and review interface in the Model Manager
            -   View, review, and manage generated field mapping proposals through enhanced visualization tools in the Model Manager. Accept individual mapping suggestions or auto-apply entire mapping sets with a single action.
    -   UI changes in the Australia release:
        -   Entity types filtered by system version
            -   The Model Manager now shows only entity types compatible with your ERP system version to prevent invalid configurations.
    -   Changed in the Australia release:
        -   Improved ETL data extractions
            -   The ETL process was refactored from Flow Designer to script includes for better performance and reliability.
        -   Zero Copy Connector for ERP data products renamed to content packs
            -   All ERP data products, such as Enterprise Data Foundation, Quote to Cash, and Source to Settle have been renamed to content packs.
        -   Zero Copy Connector for ERP Enterprise Data Foundation content pack
            -   Additional models, including Customer, Vendor, Vendor Bank Details, Vendor Location Details, and Vendor Contact Details have been added to the content pack for use when interacting with an SAP system.
        -   Zero Copy Connector for ERP Source to Settle content pack
            -   Additional models, including Customer, Vendor, Vendor Bank Details, Vendor Location Details, and Vendor Contact Details have been added to the content pack for use when interacting with an SAP system.
-   **Version 9.2.7 - April 2026**

    Changes in this release: An additional system property to specify how many records are retrieved. The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.

-   **Version 9.1.4 - March 2026**

    The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.

-   **Version 9.0.16 - December 2025**
    -   The ServiceNow Zero Copy Connector for ERP application enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform®. Zero Copy Connector for ERP was enhanced and updated in the Zurich release.
    -   Zero Copy Connector for ERP highlights for the Zurich Patch 4 release \(December 2025\):
        -   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
        -   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
        -   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
    -   New in this release:
        -   Set security on model operations. Apply roles and user group names to control access to create, read, and update model operations.
        -   More easily create model operation entity inputs and outputs using scriptable API. Query complex request/response structures faster and easier using scriptable Glide APIs for models instead of Flow Designer.
        -   Check that your production instance has the latest version of a model. Determine if production and non-production instances are using the same or different versions of a model to check if the latest model updates are on your production instance.
        -   Create and change SAP business entities with IDoc. Work with SAP business entities that can only be created or changed using IDOC.
        -   Control data access for ERP AI agents. Grant, modify, and revoke AI agent data access with specific read, write, and query privileges.
        -   Use ETag in update operations. Create update operations where ETag is required and OData services are used. The ETag is fetched by default and sent with the update call.
        -   SAP ECC and SAP S/4HANA are now primary connectors. The SAP ECC and SAP S/4HANA connectors are now primary connectors in Workflow Data Fabric Zero Copy Connectors.
        -   Upload data from SAP SuccessFactors. Access data from SAP SuccessFactors using OData V2 APIs and use the information in Zero Copy Connector for ERP models.
        -   Use automatic mapping to map table fields between systems faster. Map table fields between systems faster with automatic mapping.
        -   View session-level debugging logs. View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.
    -   UI changes in this release:
        -   New icon for outbound messages. A new icon is available in the sidebar to help you easily see existing and create new outbound message configurations for IDOC.
        -   View model version. To help you better understand if your production instance is using the latest version of a model, the version number is visible in the models list and on individual model records.
    -   Changes in this release:
        -   Updates to the Zero Copy Connector for ERP Enterprise Data Foundation data product. Additional models, including Business Partner, Chart of Accounts, Cost Center, and Vendor, have been added to the data product for use when interacting with an SAP system.
        -   Update to the Zero Copy Connector for ERP Quote to Cash data product. Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification, have been added to the data product for use when interacting with an SAP system.
        -   Zero Copy Connector for ERP Source to Settle data product. Additional purchase order models have been added to the data product for use when interacting with an SAP system.
-   **Version 8.0.13 - August 2025**

    Zero Copy Connector for ERP \(formerly ERP Canvas/ERP Data Hub\) is the platform for ERP \(Enterprise Resource Planning\) data in ServiceNow. It provides a unified data model for ERP, enabling users to extract relevant data and store it in remote tables or extraction tables. Additionally, you can update the ERP system using a BAPI \(Business Application Programming Interface\) and OData.


**Parent Topic:**[ServiceNow Store - Workflow Data Fabric release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-workflow-data-fabric-highlights.md)

