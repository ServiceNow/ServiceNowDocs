---
title: Combined Zero Copy Connector for ERP release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Zero Copy Connector for ERP from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-zerocopyconnectorforerp-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Zero Copy Connector for ERP release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Zero Copy Connector for ERP from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Zero Copy Connector for ERP release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Zero Copy Connector for ERP to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

If you have existing scheduled extractions and have upgraded to Zurich, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://www.servicenow.com/docs/access?context=t_RunFixScripts&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Zero Copy Connector for ERP.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[New UI for managing models](https://www.servicenow.com/docs/access?context=work-with-erp-data-models&family=washingtondc&ft:locale=en-US)**

Create and map models using tables and BAPIs, and then use the models to read and update the ERP system.

-   **[Read and update SAP from Zero Copy Connector for ERP using BAPI function calls](https://www.servicenow.com/docs/access?context=erpc-managing-models-read&family=washingtondc&ft:locale=en-US)**

Add **Read** and **Update** operations to the ERP model using BAPIs and table reads to communicate with the ERP system through the new ERP Model Management page.

    -   Find tables and BAPIs faster in the connected ERP system using AI Search.
    -   Create read operation entities using BAPIs or by the previous method of reading specified ERP tables on the system of record to retrieve data from the ERP system.
    -   Specify input and output parameters to customize the data you're reading or updating. Zero Copy Connector for ERP automatically includes required parameters in the query.
    -   Send data to update the ERP system using BAPIs.
-   **[Support for earlier versions of ECC](https://www.servicenow.com/docs/access?context=erpc-prereqs-for-installation&family=washingtondc&ft:locale=en-US)**

Use Zero Copy Connector for ERP with earlier versions of ECC, beginning with version SAP ECC 6.0 EHP 8.

-   **[Use actions to build flows that specify where ERP data goes on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=erp-canvas-build-flow-operation&family=washingtondc&ft:locale=en-US)**

Add to flows and specify where the results from read and update operations are stored through a Use ERP Data action in Workflow Studio.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[OData integration](https://www.servicenow.com/docs/access?context=erp-canvas-use-odata-and-http-connection&family=xanadu&ft:locale=en-US)**

Extract data securely from ERP OData APIs using ETL to be used in remote tables and extraction tables.

-   **[Schedule extraction](https://www.servicenow.com/docs/access?context=erpc-create-a-scheduled-extraction&family=xanadu&ft:locale=en-US)**

Schedule data extractions into extraction tables with encoded query for delta updates.

-   **[Monitor transactions](https://www.servicenow.com/docs/access?context=erp-canvas-monitor-transactions&family=xanadu&ft:locale=en-US)**

Use the new monitoring feature to track each transaction and its progress; filter the ERP Data Hub task information, such as successes, failures, and more, as needed.

-   **[Enhanced heartbeat data](https://www.servicenow.com/docs/access?context=erp-canvas-use-odata-and-http-connection&family=xanadu&ft:locale=en-US)**

Use the enhanced heartbeat feature that now shows RFC, HTTP, and other connectivity status for better visibility to the end user.


</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   **[Zero Copy Connector for ERP dashboard](https://www.servicenow.com/docs/access?context=erpc-obtaining-erp-canvas-metrics-and-statistics&family=yokohama&ft:locale=en-US)**

View charts and graphs about transactions on the home page dashboard.

-   **[Implement and deploy faster with ERP content packs](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&family=yokohama&ft:locale=en-US)**

Use prebuilt content packs containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Preview entities in the Model Manager](https://www.servicenow.com/docs/access?context=erpc-add-entity-to-model-op&family=yokohama&ft:locale=en-US)**

Preview operations, fields, values, inputs, and outputs in the Zero Copy Connector for ERP Model Manager instead of having to open App Engine Studio.

-   **[View detailed software information](https://www.servicenow.com/docs/access?context=view-erp-system-information&family=yokohama&ft:locale=en-US)**

View software information including machine type, node name, supported database, and more.


</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Use agentic AI](https://www.servicenow.com/docs/access?context=now-assist-erp-aiagents-data-explorer-workflow&family=zurich&ft:locale=en-US)**

Discover ERP database table information and identify relevant ERP Data Product models using the Explore ERP models agentic AI workflow in Now Assist for Zero Copy Connector.

-   **[Now Assist for Zero Copy Connector skills](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connectors-skills&family=zurich&ft:locale=en-US)**

More easily identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill. Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use AI to discover model entity options](https://www.servicenow.com/docs/access?context=use-ai-to-help-add-an-entity-to-a-model&family=zurich&ft:locale=en-US)**

Use ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

-   **[Set security on model operations](https://www.servicenow.com/docs/access?context=erp-canvas-set-operation-level-security-on-a-model&family=zurich&ft:locale=en-US)**

Apply roles and user group names to control access to create, read, and update model operations.

-   **[More easily create model operation entity inputs and outputs using scriptable API](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&family=zurich&ft:locale=en-US)**

Query complex request/response structures faster and easier using scriptable Glide APIs for models instead of Flow Designer.

-   **[Check that your production instance has the latest version of a model](https://www.servicenow.com/docs/access?context=erp-use-model-versioning&family=zurich&ft:locale=en-US)**

Determine if production and non-production instances are using the same or different versions of a model to check if the latest model updates are on your production instance.

-   **[Create and change SAP business entities with IDoc](https://www.servicenow.com/docs/access?context=create-and-change-sap-business-entities-with-idoc&family=zurich&ft:locale=en-US)**

Work with SAP business entities that can only be created or changed using IDOC.

-   **[Control data access for ERP AI agents](https://www.servicenow.com/docs/access?context=zero-copy-connector-for-erp-ai-agents-use-cases&family=zurich&ft:locale=en-US)**

Grant, modify, and revoke AI agent data access with specific read, write, and query privileges.

-   **[Use ETag in update operations](https://www.servicenow.com/docs/access?context=erpc-manage-models-read-op&family=zurich&ft:locale=en-US)**

Create update operations where ETag is required and OData services are used. The ETag is fetched by default and sent with the update call.

-   **[SAP ECC and SAP S/4HANA are now primary connectors](https://www.servicenow.com/docs/access?context=primary-connectors-wdf&family=zurich&ft:locale=en-US)**

The SAP ECC and SAP S/4HANA connectors are now primary connectors in Workflow Data Fabric Zero Copy Connectors.

-   **[Upload data from SAP SuccessFactors](https://www.servicenow.com/docs/access?context=obtain-data-from-successfactors-using-odata-v2-apis&family=zurich&ft:locale=en-US)**

Access data from SAP SuccessFactors using OData V2 APIs and use the information in Zero Copy Connector for ERP models.

-   **[Use automatic mapping to map table fields between systems faster](https://www.servicenow.com/docs/access?context=erpc-manage-model-inputs&family=zurich&ft:locale=en-US)**

Map table fields between systems faster with automatic mapping.

-   **[View session-level debugging logs](https://www.servicenow.com/docs/access?context=debug-zero-copy-connector-for-erp-models&family=zurich&ft:locale=en-US)**

View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.


</td></tr><tr><td>

Australia

</td><td>

-   **[Support for REST APIs](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=australia&ft:locale=en-US)**

Connect to ERPs using REST APIs for read and write operations.

-   **[AI agent for SAP OData services](https://www.servicenow.com/docs/access?context=now-assist-erp-aiagents-data-explorer-workflow&family=australia&ft:locale=en-US)**

Discover relevant SAP OData v2 services for your models using the OData Services Recommender AI agent. This reduces missed integration opportunities and accelerates development by finding standard SAP capabilities that align with your use cases.

-   **[Implement and deploy faster with the ERP Hire to Retire content pack](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&family=australia&ft:locale=en-US)**

Use the Hire to Retire content pack containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Improved mapping visualization and review interface in the Model Manager](https://www.servicenow.com/docs/access?context=erpc-manage-model-inputs&family=australia&ft:locale=en-US)**

View, review, and manage generated field mapping proposals through enhanced visualization tools in the Model Manager. Accept individual mapping suggestions or auto-apply entire mapping sets with a single action.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Zero Copy Connector for ERP features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[ERP Semantic Mining no longer required for Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erpc-prereqs-for-installation&family=washingtondc&ft:locale=en-US)**

You can now install Zero Copy Connector for ERP without also installing ERP-CM.

-   **[Use ERP Model Management to create table joins](https://www.servicenow.com/docs/access?context=erp-canvas-add-join-data-model&family=washingtondc&ft:locale=en-US)**

Create table joins in the **Manage entities** tab of the ERP Model Management page by adding parent and child tables as Table read entities, and then managing their order to create join conditions.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   **[View ERP Integration software information](https://www.servicenow.com/docs/access?context=view-erp-system-information&family=yokohama&ft:locale=en-US)**

From the Zero Copy Connector for ERP system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **[Preview model entities before adding to a model](https://www.servicenow.com/docs/access?context=erp-canvas-preview-entity&family=yokohama&ft:locale=en-US)**

In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 7](https://www.servicenow.com/docs/access?context=zurich-patch-7&family=zurich&ft:locale=en-US)

-   **[Additional system property to specify how many records are retrieved](https://www.servicenow.com/docs/access?context=erp-canvas-system-properties&family=zurich&ft:locale=en-US)**

The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.


[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Enterprise Data Foundation data product](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&family=zurich&ft:locale=en-US)**

Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Quote to Cash data product](https://www.servicenow.com/docs/access?context=erp-canvas-sales-order-content-pack&family=zurich&ft:locale=en-US)**

Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Source to Settle data product](https://www.servicenow.com/docs/access?context=erp-source-to-settle-data-product&family=zurich&ft:locale=en-US)**

Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   ****

</td></tr><tr><td>

Australia

</td><td>

-   **[Improved ETL data extractions](https://www.servicenow.com/docs/access?context=set-up-erp-integration-connection&family=australia&ft:locale=en-US)**

The ETL process was refactored from Flow Designer to script includes for better performance and reliability.

-   **[Zero Copy Connector for ERP Data Products renamed to Content Packs](https://www.servicenow.com/docs/access?context=erp-canvas-available-content-packs&family=australia&ft:locale=en-US)**

All ERP Data Products, such as Enterprise Data Foundation, Quote to Cash, and Source to Settle are renamed to Content Packs.

-   **[Zero Copy Connector for ERP Enterprise Data Foundation content pack](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&family=australia&ft:locale=en-US)**

Additional models, including Vendor Bank Details, Vendor Location Details, and Vendor Contact Details are added to the content pack for use when interacting with an SAP system.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Zero Copy Connector for ERP features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Zero Copy Connector for ERP features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Zero Copy Connector for ERP.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP. You need the following on your ERP system:

-   SAP ECC \(minimum SAP Netweaver 7.3\)
-   SAP S/4HANA \(all versions supported\)
-   SAP Java Connector

</td></tr><tr><td>

Xanadu

</td><td>

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr><tr><td>

Yokohama

</td><td>

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr><tr><td>

Zurich

</td><td>

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr><tr><td>

Australia

</td><td>

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Zero Copy Connector for ERP, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   New model management UI for creating models.
-   Support for using BAPIs \(Business Application Programming Interface\) to read and update SAP data.
-   Ability to send updates to the ERP system from the ServiceNow AI Platform by specifying input and output parameters.
-   Support for earlier versions of ECC \(ERP Central Component\).
-   Removed the requirement to have ERP Semantic Mining \(ERP-CM\) in order to run Zero Copy Connector for ERP.

 See [ERP Integration](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   In Xanadu Patch 3, enabled ODATA integration.
-   In Xanadu Patch 3, added a monitor to track transactions and their progress.
-   In Xanadu Patch 1, changed the name of the application from ERP Canvas to Zero Copy Connector for ERP.
-   In Xanadu Patch 1, updated the UI to clarify instructions and labels.

 See [ERP Data Hub](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   View charts and graphs on the Zero Copy Connector for ERP home page dashboard.
-   Accelerate your adoption of Zero Copy Connector for ERP using content packs.
-   Preview entities in the Model Manager.

 [Yokohama Patch 1](https://www.servicenow.com/docs/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

 See [ERP Integration](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
-   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
-   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.
-   The name of the ERP Contact Packs application has been changed to ERP Data Products.
-   Accelerate your adoption of Zero Copy Connector for ERP using new and updated ERP Data Products.

 See [ERP Integration overview](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Use REST APIs to extend beyond SAP systems.
-   Improved AI suggestions and interface for mapping fields in the Model Manager.

 See [ERP Integration](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

