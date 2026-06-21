---
title: Combined ERP Canvas release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for ERP Canvas from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-erpcanvas-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined ERP Canvas release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for ERP Canvas from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ERP Canvas release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ERP Canvas to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for ERP Canvas.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[New UI for managing models](https://www.servicenow.com/docs/access?context=work-with-erp-data-models&family=washingtondc&ft:locale=en-US)**

Create and map models using tables and BAPIs, and then use the models to read and update the ERP system.

-   **[Read and update SAP from using BAPI function calls](https://www.servicenow.com/docs/access?context=erpc-managing-models-read&family=washingtondc&ft:locale=en-US)**

Add **Read** and **Update** operations to the ERP model using BAPIs and table reads to communicate with the ERP system through the new ERP Model Management page.

    -   Find tables and BAPIs faster in the connected ERP system using AI Search.
    -   Create read operation entities using BAPIs or by the previous method of reading specified ERP tables on the system of record to retrieve data from the ERP system.
    -   Specify input and output parameters to customize the data you're reading or updating. automatically includes required parameters in the query.
    -   Send data to update the ERP system using BAPIs.
-   **[Support for earlier versions of ECC](https://www.servicenow.com/docs/access?context=erpc-prereqs-for-installation&family=washingtondc&ft:locale=en-US)**

Use with earlier versions of ECC, beginning with version SAP ECC 6.0 EHP 8.

-   **[Use actions to build flows that specify where ERP data goes on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=erp-canvas-build-flow-operation&family=washingtondc&ft:locale=en-US)**

Add to flows and specify where the results from read and update operations are stored through a Use ERP Data action in Workflow Studio.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   **[dashboard](https://www.servicenow.com/docs/access?context=erpc-obtaining-erp-canvas-metrics-and-statistics&family=yokohama&ft:locale=en-US)**

View charts and graphs about transactions on the home page dashboard.

-   **[Implement and deploy faster with ERP content packs](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&family=yokohama&ft:locale=en-US)**

Use prebuilt content packs containing models to get running on your instance faster.

-   **[Preview entities in the Model Manager](https://www.servicenow.com/docs/access?context=erpc-add-entity-to-model-op&family=yokohama&ft:locale=en-US)**

Preview operations, fields, values, inputs, and outputs in the Model Manager instead of having to open App Engine Studio.

-   **[View detailed software information](https://www.servicenow.com/docs/access?context=view-erp-system-information&family=yokohama&ft:locale=en-US)**

View software information including machine type, node name, supported database, and more.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing ERP Canvas features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[no longer required for](https://www.servicenow.com/docs/access?context=erpc-prereqs-for-installation&family=washingtondc&ft:locale=en-US)**

You can now install without also installing ERP-CM.

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

From the system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **[Preview model entities before adding to a model](https://www.servicenow.com/docs/access?context=erp-canvas-preview-entity&family=yokohama&ft:locale=en-US)**

In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some ERP Canvas features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some ERP Canvas features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ERP Canvas.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

Install by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ERP Canvas we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

SAP ECC and S/4 HANA are currently the only available systems that integrate with . You need the following on your ERP system:

-   SAP ECC \(minimum SAP Netweaver 7.3\)
-   SAP S/4HANA \(all versions supported\)
-   SAP Java Connector

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

SAP ECC and S/4 HANA are currently the only available systems that integrate with .

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ERP Canvas we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ERP Canvas, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ERP Canvas we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ERP Canvas we have noted them here.

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
-   Removed the requirement to have \(ERP-CM\) in order to run .

 See [ERP Integration](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

[Yokohama Patch 3](https://www.servicenow.com/docs/access?context=yokohama-patch-3&family=yokohama&ft:locale=en-US)

-   View charts and graphs on the home page dashboard.
-   Accelerate your adoption of using content packs.
-   Preview entities in the Model Manager.

 [Yokohama Patch 1](https://www.servicenow.com/docs/access?context=yokohama-patch-1&family=yokohama&ft:locale=en-US)

-   The name of the application has been changed from ERP Data Hub to .
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

 See [ERP Integration](https://www.servicenow.com/docs/access?context=erp-integration-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

