---
title: Zero Copy Connector for ERP release notes
description: The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.The ServiceNow Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-19"
reading_time_minutes: 5
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, erp data, connect, erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, erp data, connect, erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, erp data, connect, erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, erp data, connect, erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, erp data, connect]
---

# Zero Copy Connector for ERP release notes

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.

## About Zero Copy Connector for ERP

-   Connect to Oracle E-Business Suite \(12.2 and later\).
-   Use REST APIs to extend beyond SAP systems.
-   Use the improved AI suggestions and interface to map fields in the Model Manager.
-   As of version 29.2.11, ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Zero Copy Connector.
-   Discover OData services faster using an AI agent for Zero Copy Connector for ERP.

See [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-overview.md) and [ServiceNow Otto for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md) for more information.

## Activation and other requirements

**Important:** Zero Copy Connector for ERP and ServiceNow Otto for Zero Copy Connector are available in the ServiceNow Store. For details, see the Activation information section of these release notes.

-   **Activation information**

    Install Zero Copy Connector for ERP and ServiceNow Otto for Zero Copy Connector by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    SAP ECC, SAP S/4 HANA, and Oracle E-Business Suite \(12.2 and later\) are the available systems that integrate with Zero Copy Connector for ERP.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## September 2026

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.

### What's new

-   **Support for Oracle E-Business Suite**

    Select Oracle E-Business Suite \(12.2 or later\) as the ERP software when you configure an ERP system record. Oracle E-Business Suite connects through REST.

-   **Use Oracle EBS ISG services**

    Add Oracle E-Business Suite Integrated SOA Gateway \(ISG\) services to a model using their Web Application Description Language \(WADL\) definitions. When you create a model entity for a WADL operation, Zero Copy Connector for ERP generates its fields from the operation's WADL and XSD definitions.

-   **AI search for WADL service endpoints**

    Search for endpoints of discovered WADL services from the interface using AI Search.

-   **Row count for the scriptable API**

    Call the `getRowCount()` method on the `API` class to return the total number of rows that a query matches without retrieving the records. Configure the query as you would for `execute()`.


### What's deprecated or removed

Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## August 2026

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.

### What's new

-   **[ServiceNow Otto for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


### What's changed

-   **[Simplified process for adding a REST entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/add-a-rest-entity-to-a-model-operation.md)**

    After you specify the REST service to use, the endpoint and return type are added automatically.


## Australia General Availability

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.

### What's new

-   **[Support for REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-use-rest.md)**

    Connect to ERPs using REST APIs for read and write operations.

-   **[Implement and deploy faster with the ERP Hire to Retire content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-recruit-to-retire-content-pack.md)**

    Use the Hire to Retire content pack containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Improved mapping visualization and review interface in the Model Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erpc-manage-model-inputs.md)**

    View, review, and manage generated field mapping proposals through enhanced visualization tools in the Model Manager. Accept individual mapping suggestions or auto-apply entire mapping sets with a single action.

-   **[Improved AI Agent for SAP OData services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/now-assist-erp-ai-agent-odata-service-recommender.md)**

    Reduce missed integration opportunities and accelerate development by discovering relevant SAP OData v2 services for your models using the OData Services Recommender AI agent. This workflow finds standard SAP capabilities that align with your use cases.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


### What's changed

-   **[Improved ETL data extractions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/set-up-erp-integration-connection.md)**

    The extract, transform, load \(ETL\) process uses script includes instead of Flow Designer.

-   **[Zero Copy Connector for ERP Data Products renamed to Content Packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-available-content-packs.md)**

    All ERP Data Products, such as Enterprise Data Foundation, Quote to Cash, and Source to Settle, are renamed to Content Packs.

-   **[Zero Copy Connector for ERP Enterprise Data Foundation content pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-canvas-enterprise-data-foundation-content-pack.md)**

    Additional models, including Vendor Bank Details, Vendor Location Details, and Vendor Contact Details, are added to the content pack for use when interacting with an SAP system.


## Australia

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to an Enterprise Resource Planning \(ERP\) system of record, query remote tables, and build data models to use ERP data. Zero Copy Connector for ERP was enhanced and updated in the Australia release.

### What's deprecated or removed

The **Ask AI** button was removed from the Model Manager.

