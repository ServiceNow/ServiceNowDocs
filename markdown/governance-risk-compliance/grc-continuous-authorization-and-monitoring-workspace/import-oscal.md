---
title: Import in OSCAL format
description: The CAM OSCAL import offers a playbook-style experience designed to streamline the integration of security control data.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import in OSCAL format

The CAM OSCAL import offers a playbook-style experience designed to streamline the integration of security control data.

This guided process supports importing JSON files in both Catalog and System Security Plan \(SSP\) models, using the OSCAL \(Open Security Controls Assessment Language\) format. From the OSCAL Import landing page, you can view a list of previously imported OSCAL files along with their current statuses. To start a new import, select **New Import** from the **All OSCAL Imports** landing page. The import process then guides you through the following structured stages:

-   **Details**: Enter the import details, such as the OSCAL model, source, and recipients for import status notifications.
-   **Attachments**: Upload the OSCAL-formatted files corresponding to the model selected in the **Details** tab.
    -   For Catalog OSCAL model, you must upload the catalog file to proceed with the import process.
    -   For SSP OSCAL model, you must upload the following files:
        -   Catalog
        -   Profile
        -   SSP
        -   Overlay: You can upload multiple overlay files.
    -   For Assessment Plan \(AP\) OSCAL model, you must upload the following files:
        -   Catalog
        -   Profile
        -   SSP
        -   Assessment Plan: You can upload multiple AP files \(one per engagement.
        -   Overlay: You can upload multiple overlay files \(optional\)
        -   POA&amp;M: You can upload POA&amp;M files \(optional\)
-   **Roles and Responsibilities**: Assign users to specific roles for the imported files. These users will retain their roles throughout each step in the authorization package.

    **Note:** This tab is applicable only when the SSP or Assessment Plan OSCAL model is selected.

-   **Preview and Override**: Review the list of files to be uploaded, along with the number of files that will be created or skipped. Take appropriate actions such as importing, skipping, or overriding.

    **Note:**

    -   You can only override files that are in the skipped state. Additionally, if you override a package, all data associated with that package will be overridden.
    -   For new packages, all SSP and AP-related objects \(engagements, control tests, test plans, entity to engagement mappings\) display as Create New. On import, all objects are created.
    -   For existing packages, all SSP and AP related objects display as "Override" by default. If you skip the package, all related objects are skipped automatically, including baseline controls, information type definitions, inherited controls, hybrid controls, engagements, test plans, control tests, and entity to engagement mappings.
    -   When importing multiple AP files, each file must have a unique UUID. If two AP files contain the same UUID, the import process fails and displays an error message.

Using the CAM import OSCAL feature, you can perform the following:

-   [Import OSCAL catalog](../task/import-oscal-cam-ws.md)
-   [Import OSCAL SSP](../task/import-oscal-ssp-cam-ws.md)
-   

For more information on the OSCAL import error and control catalog, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.

For more information about OSCAL Assessment Plan import, see [OSCAL Assessment Plan export and import](../../grc-cam/concept/oscal-assessment-plan-import-export.md).

-   **[Import OSCAL catalog](../task/import-oscal-cam-ws.md)**  
From the New Import playbook experience page, you can import OSCAL files in the Catalog model into CAM workspace. This task focuses on uploading and processing the required JSON files to begin the import process.
-   **[Import OSCAL SSP](../task/import-oscal-ssp-cam-ws.md)**  
From the New Import playbook experience page, you can import OSCAL files in the System Security Plan \(SSP\) model into CAM workspace. This action enables you to seamlessly upload authorization package data in OSCAL format.

**Parent Topic:**[CAM OSCAL](oscal-cam-ws.md)

