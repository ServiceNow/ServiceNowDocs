---
title: Zero Copy Connector for ERP release notes
description: The ServiceNow Zero Copy Connector for ERP application lets you connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Zero Copy Connector for ERP release notes

The ServiceNow® Zero Copy Connector for ERP application lets you connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.

## Zero Copy Connector for ERP highlights for the Australia release

-   Use REST APIs to extend beyond SAP systems.
-   Improved AI suggestions and interface for mapping fields in the Model Manager.

See [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-integration-overview.md) for more information.

**Important:** Zero Copy Connector for ERP is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Support for REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-integration-overview.md)**

    Connect to ERPs using REST APIs for read and write operations.

-   **AI agent for SAP OData services**

    Discover relevant SAP OData v2 services for your models using the OData Services Recommender AI agent. This reduces missed integration opportunities and accelerates development by finding standard SAP capabilities that align with your use cases.

-   **[Implement and deploy faster with the ERP Hire to Retire content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-content-packs.md)**

    Use the Hire to Retire content pack containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Improved mapping visualization and review interface in the Model Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-model-inputs.md)**

    View, review, and manage generated field mapping proposals through enhanced visualization tools in the Model Manager. Accept individual mapping suggestions or auto-apply entire mapping sets with a single action.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Changed in this release

-   **[Improved ETL data extractions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/set-up-erp-integration-connection.md)**

    The ETL process was refactored from Flow Designer to script includes for better performance and reliability.

-   **[Zero Copy Connector for ERP Data Products renamed to Content Packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-available-content-packs.md)**

    All ERP Data Products, such as Enterprise Data Foundation, Quote to Cash, and Source to Settle are renamed to Content Packs.

-   **[Zero Copy Connector for ERP Enterprise Data Foundation content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-enterprise-data-foundation-content-pack.md)**

    Additional models, including Vendor Bank Details, Vendor Location Details, and Vendor Contact Details are added to the content pack for use when interacting with an SAP system.


## Activation information

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

## Related ServiceNow applications and features

-   **[Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)**

    The Now Assist for Zero Copy Connector application includes generative AI skills and AI agents that can help you use Zero Copy Connectors efficiently.

-   **[ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-landing.md)**

    Use ServiceNow Studio to build apps and app files based on ERP data.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

