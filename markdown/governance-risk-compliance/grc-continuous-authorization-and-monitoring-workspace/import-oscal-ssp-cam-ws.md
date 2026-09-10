---
title: Import OSCAL SSP
description: From the New Import playbook experience page, you can import OSCAL files in the System Security Plan \(SSP\) model into CAM workspace. This action enables you to seamlessly upload authorization package data in OSCAL format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-ssp-cam-ws.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Import in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL SSP

From the New Import playbook experience page, you can import OSCAL files in the System Security Plan \(SSP\) model into CAM workspace. This action enables you to seamlessly upload authorization package data in OSCAL format.

## Before you begin

Role required:

-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)
-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)

**Note:**

-   The catalog, catalog overlay, SSP, and profile file to be imported must be in JSON format and validated using the OSCAL-CLI tool [https://github.com/usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) for any validation error.
-   Recipients are notified through email on completion of the import process.
-   User who should be mapped for CAM specific personas.

The OSCAL SSP import is a synchronous process.

## Enter OSCAL import details

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select \[Omitted image "cam-oscal-import-icon.png"\] Alt text: OSCAL import from the sidebar.

3.  Select **New Import** from the **All OSCAL imports** landing page.

4.  Select **SSP** from the **OSCAL Model** drop-down list.

5.  Enter the **Source** name.

6.  Enter the **Import status recipients** name.

    You can list the users you want to be notified once the OSCAL import is complete. The recipient receives an email notification on the import status.

7.  Select **Next** to continue to the next step in the OSCAL import process.

    You’ll be directed to the **Attachments** tab to attach the SSP files.

8.  Attach the individual files in the **Attachments** tab, then select **Next** to upload the Overlay file.

    **Note:** Catalog, Profile, and SSP are mandatory files.

    -   **Catalog**: Contains the details of the control objectives and its related objects.
    -   **Profile**: Contains a baseline of selected controls from one or more control catalogs.
    -   **SSP**: Contains the details of the authorization boundary, authorization package, system elements, information types, controls, common controls, inherit, hybrid controls, and others.
    -   **Data flow diagram**, **Boundary diagram**, **Network diagram** and **Enterprise Architecture**: These diagrams are attached to the authorization boundary.
9.  Select **Next** to continue with the attachments.

    -   Overlay attachments: Attach one or more overlay files.
    -   POA&amp;M attachments: Add one or more POA&amp;M files.
    -   Authorization boundary attachments: Attach diagrams and other supporting documentation relevant to the authorization boundary, such as boundary assessment documents or architectural diagrams.
    -   Authorization package attachments: Add specific authorization package documents. You can add the following files:

        -   SSP Report
        -   SAP Report
        -   SAR Report
        -   ATO Letter
        -   POA&amp;M Report
        -   Executive Summary
        These documents attach to specific authorization package document fields.

        In addition, under the Attachments section, you can add general supporting documents, such as PDFs, Word documents, or images. These aren't linked to a specific field.

10. Select **Next** to continue to **Roles and Responsibilities**, where you can assign users to specific roles for the imported files.

    These users will retain their roles throughout each step in the authorization package.

11. Select **Next** to continue to **User mapping**, where the system maps users from the OSCAL file to ServiceNow users.

    These users will retain their roles throughout each step in the authorization package.

    When usernames match, the system auto-maps them. When usernames do not match or the user does not exist in ServiceNow, you must manually select the corresponding ServiceNow user. The user mapping step verifies that all required roles are assigned \(System Owner, ISSO, ISSM, Engagement Lead, Auditors\). If mandatory roles are missing after auto-mapping, you must manually assign users before proceeding.

12. Select **Next** to continue to **Preview and Override**, where you can verify the files you uploaded.

13. In the **Preview and Override** tab, review the details that are to be created, skipped, or overridden and then perform one of the following:

    -   Select **Import** to import the SSP model.

        **Note:** When all the data is new and must be imported, the import action creates new records for the respective data. In this case, you can’t skip or override the files. However, if you import a file with the same source and matching records, you’ll have the option to skip the data.

    -   To override data, perform the following actions:
        1.  Select **Select list to override** to choose the data to override.

        2.  Select **Skipped** to list the reference that is to be skipped.

            **Note:** Based on the data you select from the drop-down: If the data is in the **Will be skipped** state, you can only override it. When you override a control objective, all associated control objective requirements will also be overridden.

        3.  Select the reference from the list that you want to override.

            \[Omitted image "cam-oscal-import-ssp6.png"\] Alt text: Overriding skipped files.

        4.  Select **Override** to override one or more selected references.

            The selected reference is flagged as overridden and the **Overridden** count is increased in the preview list.

    -   To skip data, perform the following actions:
        1.  Select **Select list to override** to choose the data to skip.

        2.  Select **Overridden** to list the reference that is to be skipped.

            **Note:** If it is in the **Overridden** state, you can only skip it.

        3.  Select the reference from the list that you want to skip.\[Omitted image "cam-oscal-import-ssp7.png"\] Alt text: Skipping overridden files.
        4.  Select **Skip** to override one or more selected references.

            The selected reference is flagged as skip and the **Will be skipped** count is increased in the preview list.

14. Select **Import** to import the SSP files.

    **Note:** If an error occurs during the import process, review the error message displayed in the pop-up and take the necessary corrective action.

    You can view the import status report in the **All OSCAL import** landing page.

15. If an error occurs during the import process, review the error message displayed in the pop-up and take the necessary corrective action.

    You can also select the More Actions icon on the **Attachments** and **Roles and Responsibilities** tabs to select **Restart Stage** to restart the particular stage.

    **Note:** You can also select the playbook action icon to select **Restart Playbook** to restart the playbook.


**Parent Topic:**[Import in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.md)

