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

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   View charts and graphs on the Zero Copy Connector for ERP home page dashboard.
-   Accelerate your adoption of Zero Copy Connector for ERP using content packs.
-   Preview entities in the Model Manager.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

See [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

**Important:** [Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Zero Copy Connector for ERP dashboard](https://www.servicenow.com/docs/access?context=erpc-obtaining-erp-canvas-metrics-and-statistics&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    View charts and graphs about transactions on the home page dashboard.

-   **[Implement and deploy faster with ERP content packs](https://www.servicenow.com/docs/access?context=erp-canvas-content-packs&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use prebuilt content packs containing models to get Zero Copy Connector for ERP running on your instance faster.

-   **[Preview entities in the Model Manager](https://www.servicenow.com/docs/access?context=erpc-add-entity-to-model-op&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Preview operations, fields, values, inputs, and outputs in the Zero Copy Connector for ERP Model Manager instead of having to open App Engine Studio.

-   **[View detailed software information](https://www.servicenow.com/docs/access?context=view-erp-system-information&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    View software information including machine type, node name, supported database, and more.


[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   **[Export and import Zero Copy Connector for ERP custom models](https://www.servicenow.com/docs/access?context=erpc-export-and-import-custom-models&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Share custom models between instances using export and import instead of re-creating the custom models.

-   **[Use an SAP Secure Network Communication \(SNS\) connection](https://www.servicenow.com/docs/access?context=set-up-erp-integration-connection&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Configure an SAP Secure Network Communication \(SNC\) connection to have a certificate-based authentication to access SAP production data based on X.509.

-   **[Control model manager field names](https://www.servicenow.com/docs/access?context=erpc-edit-mapped-value-name-in-model-manager&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Manually edit and maintain model manager fields for a more customizable model management experience.

-   **[More easily create a new table transform map from an extraction table](https://www.servicenow.com/docs/access?context=erpc-create-table-transform-map-from-extraction-table&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Select and map source fields with target fields when creating a table transform map from an extraction table.

-   **[Enhanced $orderby OData query capability](https://www.servicenow.com/docs/access?context=erp-data-hub-odata-query-capabilities&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Specify the order, ascending or descending, in which data should be returned from an output variable.

-   **[Use guided tours in Zero Copy Connector for ERP](https://www.servicenow.com/docs/access?context=guided-tours-in-erp-canvas&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Learn about features and complete tasks through interactive steps by taking guided tours within Zero Copy Connector for ERP.


## Changed in this release

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[View Zero Copy Connector for ERP software information](https://www.servicenow.com/docs/access?context=view-erp-system-information&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    From the Zero Copy Connector for ERP system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **[Preview model entities before adding to a model](https://www.servicenow.com/docs/access?context=erp-canvas-preview-entity&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   **[ERP Integration application name change](https://www.servicenow.com/docs/access?context=erp-integration-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    The name of the application has been changed from ERP Data Hub to Zero Copy Connector for ERP.


## Removed in this release

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

## Activation information

Install Zero Copy Connector for ERP by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

SAP ECC and S/4 HANA are currently the only available systems that integrate with Zero Copy Connector for ERP.

## Related ServiceNow applications and features

-   **[ERP Semantic Mining \(ERP-CM\)](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Identify ERP application candidates from your system of record with custom data to re-platform using ServiceNow AI Platform® low-code apps.

-   **[Build apps using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    AES consumes Financial Services Remote Tables as ERP data pills to help you create custom low-code apps and flows based on migration candidates.

-   **[Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

