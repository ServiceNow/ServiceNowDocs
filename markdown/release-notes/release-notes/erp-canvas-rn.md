---
title: Zero Copy Connector for ERP release notes
description: The ServiceNow Zero Copy Connector for ERP application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. Zero Copy Connector for ERP was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Zero Copy Connector for ERP release notes

The ServiceNow® Zero Copy Connector for ERP application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. Zero Copy Connector for ERP was enhanced and updated in the Yokohama release.

## Zero Copy Connector for ERP highlights for the Yokohama release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   View charts and graphs on the Zero Copy Connector for ERP home page dashboard.
-   Accelerate your adoption of Zero Copy Connector for ERP using content packs.
-   Preview entities in the Model Manager.

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

See [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-overview.md) for more information.

**Important:** [Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-overview.md) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   **[Zero Copy Connector for ERP dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-obtaining-erp-canvas-metrics-and-statistics.md)**

    View charts and graphs about transactions on the home page dashboard.

-   **[Implement and deploy faster with ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-canvas-content-packs.md)**

    Use prebuilt content packs containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Preview entities in the Model Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-add-entity-to-model-op.md)**

    Preview operations, fields, values, inputs, and outputs in the Zero Copy Connector for ERP Model Manager instead of having to open App Engine Studio.

-   **[View detailed software information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/view-erp-system-information.md)**

    View software information including machine type, node name, supported database, and more.


[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **[Export and import Zero Copy Connector for ERP custom models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-export-and-import-custom-models.md)**

    Share custom models between instances using export and import instead of re-creating the custom models.

-   **[Use an SAP Secure Network Communication \(SNS\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/set-up-erp-integration-connection.md)**

    Configure an SAP Secure Network Communication \(SNC\) connection to have a certificate-based authentication to access SAP production data based on X.509.

-   **[Control model manager field names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-edit-mapped-value-name-in-model-manager.md)**

    Manually edit and maintain model manager fields for a more customizable model management experience.

-   **[More easily create a new table transform map from an extraction table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-create-table-transform-map-from-extraction-table.md)**

    Select and map source fields with target fields when creating a table transform map from an extraction table.

-   **[Enhanced $orderby OData query capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-data-hub-odata-query-capabilities.md)**

    Specify the order, ascending or descending, in which data should be returned from an output variable.

-   **[Use guided tours in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/guided-tours-in-erp-canvas.md)**

    Learn about features and complete tasks through interactive steps by taking guided tours within Zero Copy Connector for ERP.


## Changed in this release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   **[View Zero Copy Connector for ERP software information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/view-erp-system-information.md)**

    From the Zero Copy Connector for ERP system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **[Preview model entities before adding to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-canvas-preview-entity.md)**

    In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **[ERP Integration application name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-overview.md)**

    The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.


## Removed in this release

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

## Activation information

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

## Related ServiceNow applications and features

-   **[ERP Semantic Mining \(ERP-CM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-customization-mining-overview.md)**

    Identify ERP application candidates from your system of record with custom data to re-platform using ServiceNow AI Platform® low-code apps.

-   **[Build apps using App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/aes-overview.md)**

    AES consumes Financial Services Remote Tables as ERP data pills to help you create custom low-code apps and flows based on migration candidates.

-   **[Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/remote-tables.md)**

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

