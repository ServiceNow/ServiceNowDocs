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
breadcrumb: [Import in OSCAL format, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
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

2.  In the CAM Workspace, select the OSCAL import landing page icon \(\[Omitted image "cam-oscal-import-icon.png"\] Alt text: OSCAL import\).

3.  Select **New Import** from the **All OSCAL imports** landing page.

4.  Select **SSP** from the **OSCAL Model** drop-down list.

5.  Enter the **Source** name.

6.  Enter the **Import status recipients** name.

    You can list the users you want to be notified once the OSCAL import is complete. The recipient receives an email notification on the import status.

    \[Omitted image "cam-oscal-import-ssp1.png"\] Alt text: OSCAL import SSP details tab.

7.  Select **Next** to continue to the next step in the OSCAL import process.

    You’ll be directed to the **Roles and Responsibilities** tab to map the users for the import process.

8.  Select the users in the **Roles and Responsibilities** tab.

    Assign users to specific roles for the imported files. These users will retain their roles throughout each step in the authorization package.

    \[Omitted image "cam-oscal-import-ssp3.png"\] Alt text: User information for OSCAL import SSP.

9.  Select **Next** to continue to the next step in the OSCAL import process.

    You’ll be directed to the **Attachments** tab to attach the SSP files.

10. Attach the individual files in the **Attachments** tab, then select **Next** to upload the Overlay file.

    **Note:** Catalog, Profile, and SSP are required files to attach.

    -   **Catalog**: Contains the details of the control objectives and its related objects.
    -   **Profile**: Contains a baseline of selected controls from one or more control catalogs.
    -   **Catalog Overlay**: Contains information regarding overlay policies and its control objectives and behavior of the overlay. This behavior depends on the addition or subtraction in which the overlay is included in the Authorization Package. For more information, see [Apply overlays to the baseline controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/apply-overlay-to-baseline.md). You can also upload multiple overlay files.
    -   **SSP**: Contains the details of the authorization boundary, authorization package, system elements, information types, controls, common controls, inherit, hybrid controls, and others.
    -   **Data flow diagram**, **Boundary diagram**, and **Network diagram**: These diagrams are attached to the authorization boundary.
11. Select **Add file** to attach the Overlay file.

    You can also upload multiple overlay files.\[Omitted image "cam-oscal-import-ssp4.png"\] Alt text: Attach OSCAL SSP files.

12. Select **Next** to verify the files you uploaded.

    **Preview and Override** tab displays.\[Omitted image "cam-oscal-import-ssp5.png"\] Alt text: OSCAL SSP import.

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

    You can also select the attachments or roles and responsibilities action icon \(\[Omitted image "cam-oscal-import-attachments-icon.png"\] Alt text: Restart attachments or roles and responsibilities.\) on the **Attachments** and **Roles and Responsibilities** tab to select **Restart Stage** to restart the particular stage.\[Omitted image "cam-oscal-import-ssp8.png"\] Alt text: Restarting attachment stage.

    **Note:** You can also select the playbook action icon \(\[Omitted image "cam-oscal-import-action-icon.png"\] Alt text: Restart playbook icon\) to select **Restart Playbook** to restart the playbook.


**Parent Topic:**[Import in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.md)

