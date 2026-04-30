---
title: ERP Data Hub release notes
description: The ServiceNow ERP Data Hub application \(formerly known as ERP Canvas\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Data Hub was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# ERP Data Hub release notes

The ServiceNow® ERP Data Hub application \(formerly known as ERP Canvas\) enables you to connect to the ERP \(Enterprise Resource Planning\) system of record, query remote tables, and build data models to use ERP data on the ServiceNow AI Platform. ERP Data Hub was enhanced and updated in the Xanadu release.

## ERP Data Hub highlights for the Xanadu release

-   In Xanadu Patch 3, enabled ODATA integration.
-   In Xanadu Patch 3, added a monitor to track transactions and their progress.
-   In Xanadu Patch 1, changed the name of the application from ERP Canvas to ERP Data Hub.
-   In Xanadu Patch 1, updated the UI to clarify instructions and labels.

See ERP Data Hub for more information.

**Important:** ERP Data Hub is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **OData integration**

    Extract data securely from ERP OData APIs using ETL to be used in remote tables and extraction tables.

-   **Schedule extraction**

    Schedule data extractions into extraction tables with encoded query for delta updates.

-   **Monitor transactions**

    Use the new monitoring feature to track each transaction and its progress; filter the ERP Data Hub task information, such as successes, failures, and more, as needed.

-   **Enhanced heartbeat data**

    Use the enhanced heartbeat feature that now shows RFC, HTTP, and other connectivity status for better visibility to the end user.


## UI changes

-   **[Get notified while entities load](https://www.servicenow.com/docs/access?context=erpc-add-entity-to-model-op&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    A new banner alert indicates that the **Manage entities** tab is loading data, so that you don't think the page is unresponsive when it retrieves data from the ERP system.

-   **[Improved icon for configuring nested output parameters](https://www.servicenow.com/docs/access?context=erp-canvas-manage-outputs&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    The icon to configure nested output parameters has changed to a more accurate intent icon \(![Indentation icon](../../build/erp-integration/image/erpc-output-indent-icon.png)\).

-   **[Clarified in-app text and name for model manager page](https://www.servicenow.com/docs/access?context=erpc-managing-models-read&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    To help you better understand how to work with ERP models, several on-screen directions have been updated. Additionally, the name of the page where you manage models has been renamed from ERP Model Management to ERP model manager.


## Activation information

Install ERP Data Hub by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

SAP ECC and S/4 HANA are currently the only available systems that integrate with ERP Data Hub.

## Related ServiceNow applications and features

-   **[Build apps using App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    AES consumes Remote Tables as ERP data pills to help you create custom low-code apps and flows based on the migration candidates.

-   **[ERP Customization Mining \(ERP-CM\)](https://www.servicenow.com/docs/access?context=erp-customization-mining-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Identify ERP application candidates from your system of record with custom data to re-platform using ServiceNow AI Platform® low-code apps.

-   **[Remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Remote Tables connect the ServiceNow AI Platform to third-party sources or to another instance so that you can retrieve external data and optionally cache it in the memory.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience. Consolidate Playbooks, Workflow Studio, Workflow Studio, Integration Hub integrations, and Decision Builder into one design environment.


**Parent Topic:**[Hyperautomation and Low-code release notes](build-automate-rn-landing.md)

