---
title: ERP Canvas release notes
description: The ServiceNow ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.The ServiceNow ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.The ServiceNow ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/release-notes/erp-canvas-rn.html
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# ERP Canvas release notes

The ServiceNow® ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.

## About ERP Canvas

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   View charts and graphs on the ERP Canvas home page dashboard.
-   Accelerate your adoption of ERP Canvas using content packs.
-   Preview entities in the Model Manager.

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   The name of the application has been changed from ERP Data Hub to ERP Canvas.
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

See [ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-overview.md) for more information.

## Activation and other requirements

**Important:** [ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-overview.md) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install ERP Canvas by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    SAP ECC and S/4 HANA are currently the only available systems that integrate with ERP Canvas.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

## May 2025

The ServiceNow® ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.

### What's new

-   **[ERP Canvas dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-obtaining-erp-canvas-metrics-and-statistics.md)**

    View charts and graphs about transactions on the home page dashboard.

-   **[Implement and deploy faster with ERP content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-canvas-content-packs.md)**

    Use prebuilt content packs containing models to get ERP Canvas running on your instance faster.

-   **[Preview entities in the Model Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-add-entity-to-model-op.md)**

    Preview operations, fields, values, inputs, and outputs in the ERP Canvas Model Manager instead of having to open App Engine Studio.

-   **[View detailed software information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/view-erp-system-information.md)**

    View software information including machine type, node name, supported database, and more.


### What's changed

-   **[View ERP Canvas software information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/view-erp-system-information.md)**

    From the ERP Canvas system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **[Preview model entities before adding to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-canvas-preview-entity.md)**

    In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


## Yokohama

The ServiceNow® ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.

### What's new

-   **[Export and import ERP Canvas custom models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-export-and-import-custom-models.md)**

    Share custom models between instances using export and import instead of re-creating the custom models.

-   **[Use an SAP Secure Network Communication \(SNS\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/set-up-erp-integration-connection.md)**

    Configure an SAP Secure Network Communication \(SNC\) connection to have a certificate-based authentication to access SAP production data based on X.509.

-   **[Control model manager field names](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-edit-mapped-value-name-in-model-manager.md)**

    Manually edit and maintain model manager fields for a more customizable model management experience.

-   **[More easily create a new table transform map from an extraction table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erpc-create-table-transform-map-from-extraction-table.md)**

    Select and map source fields with target fields when creating a table transform map from an extraction table.

-   **[Enhanced $orderby OData query capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-data-hub-odata-query-capabilities.md)**

    Specify the order, ascending or descending, in which data should be returned from an output variable.

-   **[Use guided tours in ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/guided-tours-in-erp-canvas.md)**

    Learn about features and complete tasks through interactive steps by taking guided tours within ERP Canvas.


### What's changed

-   **[ERP Integration application name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/erp-integration-overview.md)**

    The name of the application has been changed from ERP Data Hub to ERP Canvas.


### What's deprecated or removed

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

