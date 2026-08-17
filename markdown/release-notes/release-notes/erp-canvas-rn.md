---
title: ERP Canvas release notes
description: The ServiceNow ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# ERP Canvas release notes

The ServiceNow® ERP Canvas application \(formerly known as ERP Data Hub\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Canvas was enhanced and updated in the Yokohama release.

## ERP Canvas highlights for the Yokohama release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   View charts and graphs on the ERP Canvas home page dashboard.
-   Accelerate your adoption of ERP Canvas using content packs.
-   Preview entities in the Model Manager.

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   The name of the application has been changed from ERP Data Hub to ERP Canvas.
-   Export and import custom ERP models between instances.
-   Enhance communication security between SAP systems and your ServiceNow instance by using the SAP Secure Network Communication \(SNC\) connection option.
-   Manually name, edit, and maintain model manager fields.

See  for more information.

**Important:**  is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   **ERP Canvas dashboard**

    View charts and graphs about transactions on the home page dashboard.

-   **Implement and deploy faster with ERP content packs**

    Use prebuilt content packs containing models to get ERP Canvas running on your instance faster.

-   **Preview entities in the Model Manager**

    Preview operations, fields, values, inputs, and outputs in the ERP Canvas Model Manager instead of having to open App Engine Studio.

-   **View detailed software information**

    View software information including machine type, node name, supported database, and more.


[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **Export and import ERP Canvas custom models**

    Share custom models between instances using export and import instead of re-creating the custom models.

-   **Use an SAP Secure Network Communication \(SNS\) connection**

    Configure an SAP Secure Network Communication \(SNC\) connection to have a certificate-based authentication to access SAP production data based on X.509.

-   **Control model manager field names**

    Manually edit and maintain model manager fields for a more customizable model management experience.

-   **More easily create a new table transform map from an extraction table**

    Select and map source fields with target fields when creating a table transform map from an extraction table.

-   **Enhanced $orderby OData query capability**

    Specify the order, ascending or descending, in which data should be returned from an output variable.

-   **Use guided tours in ERP Canvas**

    Learn about features and complete tasks through interactive steps by taking guided tours within ERP Canvas.


## Changed in this release

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   ****

    From the ERP Canvas system form, view detailed system information including machine type, node name, supported database, and Unicode status.

-   **Preview model entities before adding to a model**

    In the Model Manager, confirm you are adding the correct entity by examining and verifying read table entities before adding the entity to a model.


[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   **ERP Integration application name change**

    The name of the application has been changed from ERP Data Hub to ERP Canvas.


## Removed in this release

The sn\_erp\_integration.enableJobModification property has been removed and is no longer required in order to schedule an extraction.

## Activation information

Install ERP Canvas by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Additional requirements

SAP ECC and S/4 HANA are currently the only available systems that integrate with ERP Canvas.

## Related ServiceNow applications and features

-   ****

    Identify ERP application candidates from your system of record with custom data to re-platform using ServiceNow AI Platform® low-code apps.

-   ****

    AES consumes Financial Services Remote Tables as ERP data pills to help you create custom low-code apps and flows based on migration candidates.

-   ****

    Financial Services Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

