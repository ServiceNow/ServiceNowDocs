---
title: Combined Zero Copy Connector for ERP release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Zero Copy Connector for ERP from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-zerocopyconnectorforerp-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Zero Copy Connector for ERP release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Zero Copy Connector for ERP from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Zero Copy Connector for ERP release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Zero Copy Connector for ERP to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Yokohama

</td><td>

-   **[Export and import Zero Copy Connector for ERP custom models](https://www.servicenow.com/docs/access?context=erpc-export-and-import-custom-models&family=yokohama&ft:locale=en-US)**

Share custom models between instances using export and import instead of re-creating the custom models.

-   **[Use an SAP Secure Network Communication \(SNS\) connection](https://www.servicenow.com/docs/access?context=set-up-erp-integration-connection&family=yokohama&ft:locale=en-US)**

Configure an SAP Secure Network Communication \(SNC\) connection to have a certificate-based authentication to access SAP production data based on X.509.

-   **[Control model manager field names](https://www.servicenow.com/docs/access?context=erpc-edit-mapped-value-name-in-model-manager&family=yokohama&ft:locale=en-US)**

Manually edit and maintain model manager fields for a more customizable model management experience.

-   **[More easily create a new table transform map from an extraction table](https://www.servicenow.com/docs/access?context=erpc-create-table-transform-map-from-extraction-table&family=yokohama&ft:locale=en-US)**

Select and map source fields with target fields when creating a table transform map from an extraction table.

-   **[Enhanced $orderby OData query capability](https://www.servicenow.com/docs/access?context=erp-data-hub-odata-query-capabilities&family=yokohama&ft:locale=en-US)**

Specify the order, ascending or descending, in which data should be returned from an output variable.

-   **[Use guided tours in Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=guided-tours-in-erp-canvas&family=yokohama&ft:locale=en-US)**

Learn about features and complete tasks through interactive steps by taking guided tours within Zero Copy Connector for ERP.


</td></tr><tr><td>

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


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist for Zero Copy Connectors](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&family=australia&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Zero Copy Connector for ERP features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[ERP Integration application name change](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=yokohama&ft:locale=en-US)**

The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.


</td></tr><tr><td>

Zurich

</td><td>

-   **[New icon for outbound messages](https://www.servicenow.com/docs/access?context=create-an-idoc-outbound-message-configuration&family=zurich&ft:locale=en-US)**

A new icon is available in the sidebar to help you easily see existing and create new outbound message configurations for IDOC.

-   **[View model version](https://www.servicenow.com/docs/access?context=erp-use-model-versioning&family=zurich&ft:locale=en-US)**

To help you better understand if your production instance is using the latest version of a model, the version number is visible in the models list and on individual model records.


</td></tr><tr><td>

Australia

</td><td>

-   **[Simplified process for adding a REST entity to a model](https://www.servicenow.com/docs/access?context=add-a-rest-entity-to-a-model-operation&family=australia&ft:locale=en-US)**

After you specify the REST service to use, the endpoint and return type are added automatically.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Zero Copy Connector for ERP features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>## Deprecations

Between your current release family and Australia, some Zero Copy Connector for ERP features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

The **Ask AI** button was removed from the Model Manager.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Zero Copy Connector for ERP.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Zero Copy Connector for ERP and ServiceNow Otto for Zero Copy Connector by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Zero Copy Connector for ERP we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Additional requirements**

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.


</td></tr><tr><td>

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

