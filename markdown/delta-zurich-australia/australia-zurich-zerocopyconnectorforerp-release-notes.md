---
title: Combined Zero Copy Connector for ERP release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Zero Copy Connector for ERP from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/delta-zurich-australia/australia-zurich-zerocopyconnectorforerp-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Zero Copy Connector for ERP release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Zero Copy Connector for ERP from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Zero Copy Connector for ERP release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Zero Copy Connector for ERP to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Upgrade information**

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

Zurich

</td><td>

-   **[Use agentic AI](https://www.servicenow.com/docs/access?context=now-assist-erp-aiagents-data-explorer-workflow&family=zurich&ft:locale=en-US)**

Discover ERP database table information and identify relevant ERP Data Product models using the Explore ERP models agentic AI workflow in ServiceNow Otto for Zero Copy Connector.

-   **[ServiceNow Otto for Zero Copy Connector skills](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connectors-skills&family=zurich&ft:locale=en-US)**

More easily identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill. Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.

-   **[Some generative AI skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
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


 -   **[Accelerate the development of Source to Settle-based applications](https://www.servicenow.com/docs/access?context=erp-source-to-settle-data-product&family=zurich&ft:locale=en-US)**

Create applications with ERP data more easily by exploring the models in the ERP Data Product for the Source to Settle procurement process.

-   **[Use OAuth 2.0 in Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=configure-oauth-authorization-code-flow-to-use-in-zero-copy-connector-for-erp&family=zurich&ft:locale=en-US)**

Securely validate the user's identity to the external ERP system by executing an OData call to an ERP system, such as SAP, using the OAuth authorization code flow.

-   **[More easily connect to an ERP system without Service Discovery enabled](https://www.servicenow.com/docs/access?context=erp-add-a-service-manually&family=zurich&ft:locale=en-US)**

Connect to an ERP system, such as SAP, based on metadata from Swagger or Postman.

-   **[Use the new models added to the ERP Data Product for Enterprise Data Foundation Masterdata](https://www.servicenow.com/docs/access?context=erp-canvas-content-pack-enterprise-data-models&family=zurich&ft:locale=en-US)**

More easily create applications with ERP data using a new set of standard models in the ERP Data Product for Enterprise Data Foundation.

-   **[Use the new models added to ERP Data Product for Quote to Cash](https://www.servicenow.com/docs/access?context=erp-canvas-content-pack-sales-order-models&family=zurich&ft:locale=en-US)**

More easily create Quote to Cash applications with ERP data using additional credit memo request models in the ERP Data Product for Quote to Cash.

-   **[Export Zero Copy Connector for ERP metrics](https://www.servicenow.com/docs/access?context=monitor-export-telemetry-data&family=zurich&ft:locale=en-US)**

Export detailed Zero Copy Connector for ERP transaction logs to audit, monitor, and externally analyze and troubleshoot model operations and data flows.


</td></tr><tr><td>

Australia

</td><td>

-   **[Support for Oracle E-Business Suite](https://www.servicenow.com/docs/access?context=erp-canvas-oracle-rest-support&family=australia&ft:locale=en-US)**

Select Oracle E-Business Suite \(12.2 or later\) as the ERP software when you configure an ERP system record. Oracle E-Business Suite connects through REST.

-   **[Use Oracle EBS ISG services](https://www.servicenow.com/docs/access?context=erp-canvas-create-an-oracle-ebs-connection&family=australia&ft:locale=en-US)**

Add Oracle E-Business Suite Integrated SOA Gateway \(ISG\) services to a model using their Web Application Description Language \(WADL\) definitions. When you create a model entity for a WADL operation, Zero Copy Connector for ERP generates its fields from the operation's WADL and XSD definitions.

-   **[AI search for WADL service endpoints](https://www.servicenow.com/docs/access?context=erp-canvas-oracle-ebs-wadl-support&family=australia&ft:locale=en-US)**

Search for endpoints of discovered WADL services from the interface using AI Search.

-   **[Row count for the scriptable API](https://www.servicenow.com/docs/access?context=erp-api-getrowcount&family=australia&ft:locale=en-US)**

Call the `getRowCount()` method on the `API` class to return the total number of rows that a query matches without retrieving the records. Configure the query as you would for `execute()`.


 -   **[Now Assist for Zero Copy Connectors](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&family=australia&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Support for REST APIs](https://www.servicenow.com/docs/access?context=erp-canvas-use-rest&family=australia&ft:locale=en-US)**

Connect to ERPs using REST APIs for read and write operations.

-   **[Implement and deploy faster with the ERP Hire to Retire content pack](https://www.servicenow.com/docs/access?context=erp-canvas-recruit-to-retire-content-pack&family=australia&ft:locale=en-US)**

Use the Hire to Retire content pack containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Improved mapping visualization and review interface in the Model Manager](https://www.servicenow.com/docs/access?context=erpc-manage-model-inputs&family=australia&ft:locale=en-US)**

View, review, and manage generated field mapping proposals through enhanced visualization tools in the Model Manager. Accept individual mapping suggestions or auto-apply entire mapping sets with a single action.

-   **[Improved AI Agent for SAP OData services](https://www.servicenow.com/docs/access?context=now-assist-erp-ai-agent-odata-service-recommender&family=australia&ft:locale=en-US)**

Reduce missed integration opportunities and accelerate development by discovering relevant SAP OData v2 services for your models using the OData Services Recommender AI agent. This workflow finds standard SAP capabilities that align with your use cases.

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

Zurich

</td><td>

-   **[Additional system property to specify how many records are retrieved](https://www.servicenow.com/docs/access?context=erp-canvas-system-properties&family=zurich&ft:locale=en-US)**

The system property sn\_erp\_integration.result\_page\_size has been added to specify the number of records to retrieve from the external system. The default global property for all extractions is set to 50, but can be overridden with this new property.


 -   **[New icon for outbound messages](https://www.servicenow.com/docs/access?context=create-an-idoc-outbound-message-configuration&family=zurich&ft:locale=en-US)**

A new icon is available in the sidebar to help you easily see existing and create new outbound message configurations for IDOC.

-   **[View model version](https://www.servicenow.com/docs/access?context=erp-use-model-versioning&family=zurich&ft:locale=en-US)**

To help you better understand if your production instance is using the latest version of a model, the version number is visible in the models list and on individual model records.


 -   **[Enterprise Data Foundation data product](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&family=zurich&ft:locale=en-US)**

Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Quote to Cash data product](https://www.servicenow.com/docs/access?context=erp-canvas-sales-order-content-pack&family=zurich&ft:locale=en-US)**

Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Source to Settle data product](https://www.servicenow.com/docs/access?context=erp-source-to-settle-data-product&family=zurich&ft:locale=en-US)**

Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[System info page displays more details](https://www.servicenow.com/docs/access?context=view-erp-system-information&family=zurich&ft:locale=en-US)**

On the system info page, software and other information is shown from the system info table.

-   **[Entity cards contain additional information](https://www.servicenow.com/docs/access?context=erpc-add-entity-to-model-op&family=zurich&ft:locale=en-US)**

On an entity card, view where data was retrieved from, the scope used during retrieval, and when the data was last retrieved.


 -   **[ERP Canvas application name change](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=zurich&ft:locale=en-US)**

The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.

-   **[ERP Content Packs name change](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&family=zurich&ft:locale=en-US)**

The name of the ERP Contact Packs application has been changed to ERP Data Products.

-   **[Updated guided tours](https://www.servicenow.com/docs/access?context=guided-tours-in-erp-canvas&family=zurich&ft:locale=en-US)**

The Add Entity and Add Operation guided tours were updated.


</td></tr><tr><td>

Australia

</td><td>

-   **[Simplified process for adding a REST entity to a model](https://www.servicenow.com/docs/access?context=add-a-rest-entity-to-a-model-operation&family=australia&ft:locale=en-US)**

After you specify the REST service to use, the endpoint and return type are added automatically.


 -   **[Improved ETL data extractions](https://www.servicenow.com/docs/access?context=set-up-erp-integration-connection&family=australia&ft:locale=en-US)**

The extract, transform, load \(ETL\) process uses script includes instead of Flow Designer.

-   **[Zero Copy Connector for ERP Data Products renamed to Content Packs](https://www.servicenow.com/docs/access?context=erp-canvas-available-content-packs&family=australia&ft:locale=en-US)**

All ERP Data Products, such as Enterprise Data Foundation, Quote to Cash, and Source to Settle, are renamed to Content Packs.

-   **[Zero Copy Connector for ERP Enterprise Data Foundation content pack](https://www.servicenow.com/docs/access?context=erp-canvas-enterprise-data-foundation-content-pack&family=australia&ft:locale=en-US)**

Additional models, including Vendor Bank Details, Vendor Location Details, and Vendor Contact Details, are added to the content pack for use when interacting with an SAP system.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Zero Copy Connector for ERP features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

 The **Ask AI** button was removed from the Model Manager.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Zero Copy Connector for ERP.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Zero Copy Connector for ERP is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Zero Copy Connector for ERP and ServiceNow Otto for Zero Copy Connector by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Zero Copy Connector for ERP and ServiceNow Otto for Zero Copy Connector are available in the ServiceNow Store. For details, see the Activation information section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **Additional requirements**

SAP ECC and SAP S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.


</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

SAP ECC, SAP S/4 HANA, and Oracle E-Business Suite \(12.2 and later\) are the available systems that integrate with Zero Copy Connector for ERP.


</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   **Accessibility information**

[Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

Zurich

</td><td>

[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
-   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
-   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.
-   Some Now Assist skills are now turned on by default.

 [Zurich Patch 1](https://www.servicenow.com/docs/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.
-   The name of the ERP Contact Packs application has been changed to ERP Data Products.
-   Accelerate your adoption of Zero Copy Connector for ERP using new and updated ERP Data Products.

 See [ERP Integration overview](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Connect to Oracle E-Business Suite \(12.2 and later\).
-   Use REST APIs to extend beyond SAP systems.
-   Use the improved AI suggestions and interface to map fields in the Model Manager.
-   As of version 29.2.11, ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Zero Copy Connector.
-   Discover OData services faster using an AI agent for Zero Copy Connector for ERP.

 See [ERP Integration](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=australia&ft:locale=en-US) and [Now Assist for Zero Copy Connectors](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/delta-zurich-australia/rn-combined-intro.md)

