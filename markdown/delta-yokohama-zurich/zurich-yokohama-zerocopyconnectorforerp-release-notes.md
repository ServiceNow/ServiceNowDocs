---
title: Combined Zero Copy Connector for ERP release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Zero Copy Connector for ERP from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-zerocopyconnectorforerp-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Zero Copy Connector for ERP release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Zero Copy Connector for ERP from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Zero Copy Connector for ERP release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Zero Copy Connector for ERP to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

If you have existing scheduled extractions and have upgraded to Zurich, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://servicenow-staging.fluidtopics.net/access?context=t_RunFixScripts&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Zero Copy Connector for ERP.

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

[Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Use agentic AI](https://servicenow-staging.fluidtopics.net/access?context=now-assist-erp-aiagents-data-explorer-workflow&family=zurich&ft:locale=en-US)**

Discover ERP database table information and identify relevant ERP Data Product models using the Explore ERP models agentic AI workflow in Now Assist for Zero Copy Connector.

-   **[Now Assist for Zero Copy Connector skills](https://servicenow-staging.fluidtopics.net/access?context=now-assist-for-zero-copy-connectors-skills&family=zurich&ft:locale=en-US)**

More easily identify SAP objects like tables, BAPI endpoints, and OData endpoints that can then be used to query the data you need with the ERP Data Query skill. Query SAP standard database tables for data and transactional records using the ERP Data Discovery skill.

-   **[Some Now Assist skills are turned on by default](https://servicenow-staging.fluidtopics.net/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)**

The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Use AI to discover model entity options](https://servicenow-staging.fluidtopics.net/access?context=use-ai-to-help-add-an-entity-to-a-model&family=zurich&ft:locale=en-US)**

Use ask AI in model manager to obtain detailed entity options by describing the entity you want to add to a model.

-   **[Set security on model operations](https://servicenow-staging.fluidtopics.net/access?context=erp-canvas-set-operation-level-security-on-a-model&family=zurich&ft:locale=en-US)**

Apply roles and user group names to control access to create, read, and update model operations.

-   **[More easily create model operation entity inputs and outputs using scriptable API](https://servicenow-staging.fluidtopics.net/access?context=sn_erp_int-withJSON_O&family=zurich&ft:locale=en-US)**

Query complex request/response structures faster and easier using scriptable Glide APIs for models instead of Flow Designer.

-   **[Check that your production instance has the latest version of a model](https://servicenow-staging.fluidtopics.net/access?context=erp-use-model-versioning&family=zurich&ft:locale=en-US)**

Determine if production and non-production instances are using the same or different versions of a model to check if the latest model updates are on your production instance.

-   **[Create and change SAP business entities with IDoc](https://servicenow-staging.fluidtopics.net/access?context=create-and-change-sap-business-entities-with-idoc&family=zurich&ft:locale=en-US)**

Work with SAP business entities that can only be created or changed using IDOC.

-   **[Control data access for ERP AI agents](https://servicenow-staging.fluidtopics.net/access?context=zero-copy-connector-for-erp-ai-agents-use-cases&family=zurich&ft:locale=en-US)**

Grant, modify, and revoke AI agent data access with specific read, write, and query privileges.

-   **[Use ETag in update operations](https://servicenow-staging.fluidtopics.net/access?context=erpc-manage-models-read-op&family=zurich&ft:locale=en-US)**

Create update operations where ETag is required and OData services are used. The ETag is fetched by default and sent with the update call.

-   **[SAP ECC and SAP S/4HANA are now primary connectors](https://servicenow-staging.fluidtopics.net/access?context=primary-connectors-wdf&family=zurich&ft:locale=en-US)**

The SAP ECC and SAP S/4HANA connectors are now primary connectors in Workflow Data Fabric Zero Copy Connectors.

-   **[Upload data from SAP SuccessFactors](https://servicenow-staging.fluidtopics.net/access?context=obtain-data-from-successfactors-using-odata-v2-apis&family=zurich&ft:locale=en-US)**

Access data from SAP SuccessFactors using OData V2 APIs and use the information in Zero Copy Connector for ERP models.

-   **[Use automatic mapping to map table fields between systems faster](https://servicenow-staging.fluidtopics.net/access?context=erpc-manage-model-inputs&family=zurich&ft:locale=en-US)**

Map table fields between systems faster with automatic mapping.

-   **[View session-level debugging logs](https://servicenow-staging.fluidtopics.net/access?context=debug-zero-copy-connector-for-erp-models&family=zurich&ft:locale=en-US)**

View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Zero Copy Connector for ERP features.

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

[Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   **[Enterprise Data Foundation data product](https://servicenow-staging.fluidtopics.net/access?context=erp-canvas-enterprise-data-foundation-content-pack&family=zurich&ft:locale=en-US)**

Additional models, including Business Partner, Chart of Account, Cost Center, and Vendor have been added to the data product for use when interacting with an SAP system.

-   **[Quote to Cash data product](https://servicenow-staging.fluidtopics.net/access?context=erp-canvas-sales-order-content-pack&family=zurich&ft:locale=en-US)**

Additional models, including Customer Invoice, Outbound Deliveries, and Service Notification have been added to the data product for use when interacting with an SAP system.

-   **[Source to Settle data product](https://servicenow-staging.fluidtopics.net/access?context=erp-source-to-settle-data-product&family=zurich&ft:locale=en-US)**

Additional purchase order models have been added to the data product for use when interacting with an SAP system.

-   ****

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Zero Copy Connector for ERP features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Zero Copy Connector for ERP features or functionality were deprecated.

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

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

[Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   ****

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

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

[Zurich Patch 4](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

-   Obtain ERP information and explore ERP data products using generative AI and agentic AI in ERP models.
-   Control data access and permissions for Zero Copy Connector for ERP AI agents to ensure that users can only interact with data they are authorized to obtain.
-   Retrieve IDOC information from SAP to create and update a greater number of SAP business entities.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Some Now Assist skills are now turned on by default.

 [Zurich Patch 1](https://servicenow-staging.fluidtopics.net/access?context=zurich-patch-1&family=zurich&ft:locale=en-US)

-   The name of the ERP Canvas application has been changed to Zero Copy Connector for ERP.
-   The name of the ERP Contact Packs application has been changed to ERP Data Products.
-   Accelerate your adoption of Zero Copy Connector for ERP using new and updated ERP Data Products.

 See [ERP Integration overview](https://servicenow-staging.fluidtopics.net/access?context=erp-integration-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

