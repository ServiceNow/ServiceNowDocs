---
title: Zero Copy Connector for ERP release notes
description: The ServiceNow Zero Copy Connector for ERP application enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. Zero Copy Connector for ERP was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
---

# Zero Copy Connector for ERP release notes

The ServiceNow® Zero Copy Connector for ERP application enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform®. Zero Copy Connector for ERP was enhanced and updated in the Zurich release.

## Zero Copy Connector for ERP highlights for the Zurich release

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
-   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
-   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.
-   The name of the ERP Contact Packs application has been changed to ERP Data Products.
-   Accelerate your adoption of Zero Copy Connector for ERP using new and updated ERP Data Products.

See [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-integration-overview.md) for more information.

**Important:** Zero Copy Connector for ERP is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Zero Copy Connector for ERP to Zurich

If you have existing scheduled extractions and have upgraded to Zurich, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/t_RunFixScripts.md).

## New in the Zurich release

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[Use agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/now-assist-erp-aiagents-data-explorer-workflow.md)**

    Discover ERP database table information and identify relevant ERP Data Product models using the Explore ERP models agentic AI workflow in Now Assist for Zero Copy Connector.

-   **[Now Assist for Zero Copy Connector skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/now-assist-for-zero-copy-connectors-skills.md)**

    More easily identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill. Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use AI to discover model entity options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/use-ai-to-help-add-an-entity-to-a-model.md)**

    Use ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

-   **[Set security on model operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-set-operation-level-security-on-a-model.md)**

    Apply roles and user group names to control access to create, read, and update model operations.

-   **[More easily create model operation entity inputs and outputs using scriptable API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/api-reference/server-api-reference/sn_erp_integrationBothAPI.md)**

    Query complex request/response structures faster and easier using scriptable Glide APIs for models instead of Flow Designer.

-   **[Check that your production instance has the latest version of a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-use-model-versioning.md)**

    Determine if production and non-production instances are using the same or different versions of a model to check if the latest model updates are on your production instance.

-   **[Create and change SAP business entities with IDoc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/create-and-change-sap-business-entities-with-idoc.md)**

    Work with SAP business entities that can only be created or changed using IDOC.

-   **[Control data access for ERP AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/zero-copy-connector-for-erp-ai-agents-use-cases.md)**

    Grant, modify, and revoke AI agent data access with specific read, write, and query privileges.

-   **[Use ETag in update operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erpc-manage-models-read-op.md)**

    Create update operations where ETag is required and OData services are used. The ETag is fetched by default and sent with the update call.

-   **[SAP ECC and SAP S/4HANA are now primary connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/primary-connectors-wdf.md)**

    The SAP ECC and SAP S/4HANA connectors are now primary connectors in Workflow Data Fabric Zero Copy Connectors.

-   **[Upload data from SAP SuccessFactors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/obtain-data-from-successfactors-using-odata-v2-apis.md)**

    Access data from SAP SuccessFactors using OData V2 APIs and use the information in Zero Copy Connector for ERP models.

-   **[Use automatic mapping to map table fields between systems faster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erpc-manage-model-inputs.md)**

    Map table fields between systems faster with automatic mapping.

-   **[View session-level debugging logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/debug-zero-copy-connector-for-erp-models.md)**

    View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.


[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **[Accelerate the development of Source to Settle-based applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-source-to-settle-data-product.md)**

    Create applications with ERP data more easily by exploring the models in the ERP Data Product for the Source to Settle procurement process.

-   **[Use OAuth 2.0 in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/configure-oauth-authorization-code-flow-to-use-in-zero-copy-connector-for-erp.md)**

    Securely validate the user's identity to the external ERP system by executing an OData call to an ERP system, such as SAP, using the OAuth authorization code flow.

-   **[More easily connect to an ERP system without Service Discovery enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-add-a-service-manually.md)**

    Connect to an ERP system, such as SAP, based on metadata from Swagger or Postman.

-   **[Use the new models added to the ERP Data Product for Enterprise Data Foundation Masterdata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-content-pack-enterprise-data-models.md)**

    More easily create applications with ERP data using a new set of standard models in the ERP Data Product for Enterprise Data Foundation.

-   **[Use the new models added to ERP Data Product for Quote to Cash](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-content-pack-sales-order-models.md)**

    More easily create Quote to Cash applications with ERP data using additional credit memo request models in the ERP Data Product for Quote to Cash.

-   **[Export Zero Copy Connector for ERP metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/monitor-export-telemetry-data.md)**

    Export detailed Zero Copy Connector for ERP transaction logs to audit, monitor, and externally analyze and troubleshoot model operations and data flows.


## UI changes

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[New icon for outbound messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/create-an-idoc-outbound-message-configuration.md)**

    A new icon is available in the sidebar to help you easily see existing and create new outbound message configurations for IDOC.

-   **[View model version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-use-model-versioning.md)**

    To help you better understand if your production instance is using the latest version of a model, the version number is visible in the models list and on individual model records.


[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[System info page displays more details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/view-erp-system-information.md)**

    On the system info page, software and other information is shown from the system info table.

-   **Entity cards contain additional information**

    On an entity card, view where data was retrieved from, the scope used during retrieval, and when the data was last retrieved.


## Changed in this release

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   **Additional system property to specify how many records are retrieved**

    The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.


[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[Zero Copy Connector for ERP Enterprise Data Foundation data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-enterprise-data-foundation-content-pack.md)**

    Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Quote to Cash data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-sales-order-content-pack.md)**

    Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Source to Settle data product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-source-to-settle-data-product.md)**

    Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **[ERP Canvas application name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-integration-overview.md)**

    The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.

-   **[ERP Content Packs name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-canvas-content-packs.md)**

    The name of the ERP Contact Packs application has been changed to ERP Data Products.

-   **[Updated guided tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/guided-tours-in-erp-canvas.md)**

    The Add Entity and Add Operation guided tours were updated.


## Activation information

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

## Accessibility

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[ERP Semantic Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/erp-customization-mining-overview.md)**

    Identify ERP application candidates from your system of record with custom data to re-platform using ServiceNow AI Platform® low-code apps.

-   **[Build apps using App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/aes-overview.md)**

    AES consumes Financial Services Remote Tables as ERP data pills to help you create custom low-code apps and flows based on migration candidates.

-   **[Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/remote-tables.md)**

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

