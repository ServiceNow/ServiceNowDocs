---
title: Import in OSCAL format
description: The CAM OSCAL import offers a playbook-style experience designed to streamline the integration of security control data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
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
        -   Assessment Plan: You can upload multiple AP files \(one per engagement\).
        -   Overlay: You can upload multiple overlay files \(optional\)
        -   POA&amp;M: You can upload POA&amp;M files \(optional\)
    -   For Assessment Results \(AR\) OSCAL model, you must upload the following files:
        -   Catalog
        -   Profile
        -   SSP
        -   Assessment Plan: The AP file linked to the AR being imported. You can upload multiple AP files.
        -   Assessment Results: The AR file to import. You can upload multiple AR files.
        -   Overlay: You can upload multiple overlay files \(optional\)
        -   POA&amp;M: You can upload multiple POA&amp;M files \(optional\). POA&amp;M items from this file are aggregated with the POA&amp;M items already present in the AR file.
-   **User and Group Mapping**: Map users and groups from the OSCAL files to the corresponding ServiceNow users and groups in your instance. Each user entry shows the roles the user is listed as in the import — for example, Assigned To \(Engagement\), Owner \(Control Test\), or Assigned To \(POA&amp;M\). This step applies to the SSP, AP, and AR OSCAL models.
-   **Roles and Responsibilities**: Assign users to specific roles for the imported files. These users will retain their roles throughout each step in the authorization package.

    **Note:** This tab is applicable when POAM, AR, SSP or Assessment Plan OSCAL model is selected.

-   **Preview and Override**: Review the list of objects to be uploaded, along with the number of objects that will be created or skipped. Take appropriate actions such as importing, skipping, or overriding.

    **Note:**

    -   "CTR Assigned To" and "CTR Opened By appear" roles appear in the user mapping list for packages with associated control tailoring requests. CTR Opened By identifies the user recorded as the creator of the control tailoring request during import. CTR Assigned To identifies the user assigned to the control tailoring request during import. If no user is mapped to either role, the system defaults to the authorizing official configured for the authorization package.
    -   For new packages, all SSP and AP-related objects \(engagements, control tests, test plans, entity to engagement mappings\) display as Create New. On import, all objects are created.
    -   For existing packages, all SSP, AP, AR, and POA&amp;M related objects display as Override by default when importing an AP or AR model. If you skip the package, all related objects are skipped automatically, including baseline controls, information type definitions, inherited controls, hybrid controls, engagements, test plans, control tests, assessment results, and entity to engagement mappings.
    -   When importing multiple AP files, each file must have a unique UUID. If two AP files contain the same UUID, the import process fails and displays an error message.
    -   For AR imports, if an engagement from the package already exists on the instance, you can choose to skip or override the existing engagement and its associated POA&amp;M items.
    -   When you override an existing authorization package during import, the system applies the imported data to the package as follows:

        -   Overlays are overwritten with the imported values
        -   Control objectives from the imported source are created or overwritten
        -   Control tailoring requests from the imported SSP are created as new records associated with the overriding package
-   The import process includes the following behavior:
    -   The import process succeeds even when overlay files contain duplicate control objective references. Each overlay defines behavior and action rules for matching and distinct control objectives, and the system applies these rules to determine which overlay's configuration takes effect for each control objective.
    -   The import now populates the following fields, if the values are present in the export file:

        -   Status
        -   Frequency
        -   Weighting
        -   Implementation statement
        -   Activities
        This applies to controls created during the import of SSP, Assessment Plan, and Assessment Report models.

-   If the imported file contains control tailoring request data, the system creates a control tailoring request record as part of the import. The imported control tailoring request includes:

    -   Requested changes
    -   Overlay controls
    -   Work notes \(visible in the CTR record, marked as imported from OSCAL\)
    -   The created by field, set to the user mapped to the CTR opened by role during import \(defaults to System Owner if not mapped\)
    The control tailoring request record is visible in the authorization package after import.


Using the CAM import OSCAL feature, you can perform the following:

-   [Import OSCAL catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-cam-ws.md)
-   [Import OSCAL SSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-ssp-cam-ws.md)
-   
-   [Import OSCAL Assessment Results \(AR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-assessment-results.md)

For more information on the OSCAL import error and control catalog, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support Knowledge Base.

-   **[Import OSCAL catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-cam-ws.md)**  
From the New Import playbook experience page, you can import OSCAL files in the Catalog model into CAM workspace. This task focuses on uploading and processing the required JSON files to begin the import process.
-   **[Import OSCAL SSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-ssp-cam-ws.md)**  
From the New Import playbook experience page, you can import OSCAL files in the System Security Plan \(SSP\) model into CAM workspace. This action enables you to seamlessly upload authorization package data in OSCAL format.
-   **[Import OSCAL Assessment Results \(AR\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-assessment-results.md)**  
Import an OSCAL Assessment Results \(AR\) package from another instance or external tool to create an engagement.

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

