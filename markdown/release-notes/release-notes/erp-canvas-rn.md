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

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
-   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
-   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.
-   The name of the ERP Contact Packs application has been changed to ERP Data Products.
-   Accelerate your adoption of Zero Copy Connector for ERP using new and updated ERP Data Products.

See [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) for more information.

**Important:** Zero Copy Connector for ERP is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Zero Copy Connector for ERP to Zurich

If you have existing scheduled extractions and have upgraded to Zurich, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://www.servicenow.com/docs/access?context=t_RunFixScripts&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## New in the Zurich release

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Use agentic AI](https://www.servicenow.com/docs/access?context=now-assist-erp-aiagents-data-explorer-workflow&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Discover ERP database table information and identify relevant ERP Data Product models using the Explore ERP models agentic AI workflow in Now Assist for Zero Copy Connector.

-   **[Now Assist for Zero Copy Connector skills](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connectors-skills&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    More easily identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill. Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use AI to discover model entity options](https://www.servicenow.com/docs/access?context=use-ai-to-help-add-an-entity-to-a-model&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Use ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

-   **[Set security on model operations](https://www.servicenow.com/docs/access?context=erp-canvas-set-operation-level-security-on-a-model&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Apply roles and user group names to control access to create, read, and update model operations.

-   **[More easily create model operation entity inputs and outputs using scriptable API](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Query complex request/response structures faster and easier using scriptable Glide APIs for models instead of Flow Designer.

-   **[Check that your production instance has the latest version of a model](https://www.servicenow.com/docs/access?context=erp-use-model-versioning&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Determine if production and non-production instances are using the same or different versions of a model to check if the latest model updates are on your production instance.

-   **[Create and change SAP business entities with IDoc](https://www.servicenow.com/docs/access?context=create-and-change-sap-business-entities-with-idoc&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Work with SAP business entities that can only be created or changed using IDOC.

-   **[Control data access for ERP AI agents](https://www.servicenow.com/docs/access?context=zero-copy-connector-for-erp-ai-agents-use-cases&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Grant, modify, and revoke AI agent data access with specific read, write, and query privileges.

-   **[Use ETag in update operations](https://www.servicenow.com/docs/access?context=erpc-manage-models-read-op&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Create update operations where ETag is required and OData services are used. The ETag is fetched by default and sent with the update call.

-   **[SAP ECC and SAP S/4HANA are now primary connectors](https://www.servicenow.com/docs/access?context=primary-connectors-wdf&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    The SAP ECC and SAP S/4HANA connectors are now primary connectors in Workflow Data Fabric Zero Copy Connectors.

-   **[Upload data from SAP SuccessFactors](https://www.servicenow.com/docs/access?context=obtain-data-from-successfactors-using-odata-v2-apis&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Access data from SAP SuccessFactors using OData V2 APIs and use the information in Zero Copy Connector for ERP models.

-   **[Use automatic mapping to map table fields between systems faster](https://www.servicenow.com/docs/access?context=erpc-manage-model-inputs&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Map table fields between systems faster with automatic mapping.

-   **[View session-level debugging logs](https://www.servicenow.com/docs/access?context=debug-zero-copy-connector-for-erp-models&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Accelerate the development of Source to Settle-based applications](https://www.servicenow.com/docs/access?context=erp-source-to-settle-data-product&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Create applications with ERP data more easily by exploring the models in the ERP Data Product for the Source to Settle procurement process.

-   **[Use OAuth 2.0 in Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=configure-oauth-authorization-code-flow-to-use-in-zero-copy-connector-for-erp&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Securely validate the user's identity to the external ERP system by executing an OData call to an ERP system, such as SAP, using the OAuth authorization code flow.

-   **[More easily connect to an ERP system without Service Discovery enabled](https://www.servicenow.com/docs/access?context=erp-add-a-service-manually&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Connect to an ERP system, such as SAP, based on metadata from Swagger or Postman.

-   **[Use the new models added to the ERP Data Product for Enterprise Data Foundation Masterdata](https://www.servicenow.com/docs/access?context=erp-canvas-content-pack-enterprise-data-models&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    More easily create applications with ERP data using a new set of standard models in the ERP Data Product for Enterprise Data Foundation.

-   **[Use the new models added to ERP Data Product for Quote to Cash](https://www.servicenow.com/docs/access?context=erp-canvas-content-pack-sales-order-models&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    More easily create Quote to Cash applications with ERP data using additional credit memo request models in the ERP Data Product for Quote to Cash.

-   **[Export Zero Copy Connector for ERP metrics](https://www.servicenow.com/docs/access?context=monitor-export-telemetry-data&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Export detailed Zero Copy Connector for ERP transaction logs to audit, monitor, and externally analyze and troubleshoot model operations and data flows.


## UI changes

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[New icon for outbound messages](https://www.servicenow.com/docs/access?context=create-an-idoc-outbound-message-configuration&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    A new icon is available in the sidebar to help you easily see existing and create new outbound message configurations for IDOC.

-   **[View model version](https://www.servicenow.com/docs/access?context=erp-use-model-versioning&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    To help you better understand if your production instance is using the latest version of a model, the version number is visible in the models list and on individual model records.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[System info page displays more details](https://www.servicenow.com/docs/access?context=view-erp-system-information&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    On the system info page, software and other information is shown from the system info table.

-   **Entity cards contain additional information**

    On an entity card, view where data was retrieved from, the scope used during retrieval, and when the data was last retrieved.


## Changed in this release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **Additional system property to specify how many records are retrieved**

    The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.


[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Zero Copy Connector for ERP Enterprise Data Foundation data product](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Quote to Cash data product](https://www.servicenow.com/docs/access?context=erp-canvas-sales-order-content-pack&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Zero Copy Connector for ERP Source to Settle data product](https://www.servicenow.com/docs/access?context=erp-source-to-settle-data-product&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[ERP Canvas application name change](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.

-   **[ERP Content Packs name change](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    The name of the ERP Contact Packs application has been changed to ERP Data Products.

-   **[Updated guided tours](https://www.servicenow.com/docs/access?context=guided-tours-in-erp-canvas&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    The Add Entity and Add Operation guided tours were updated.


## Activation information

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

## Accessibility

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[ERP Semantic Mining](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Identify ERP application candidates from your system of record with custom data to re-platform using ServiceNow AI Platform® low-code apps.

-   **[Build apps using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    AES consumes Financial Services Remote Tables as ERP data pills to help you create custom low-code apps and flows based on migration candidates.

-   **[Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

