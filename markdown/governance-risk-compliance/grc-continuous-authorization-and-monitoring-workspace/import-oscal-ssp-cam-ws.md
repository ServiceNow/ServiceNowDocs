---
title: Import OSCAL SSP
description: Import Open Security Controls Assessment Language \(OSCAL\) files in the System Security Plan \(SSP\) model into Continuous Authorization and Monitoring workspace. Import OSCAL SSP enables you import authorization packages, authorization boundary, controls, and others in OSCAL format.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Import in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL SSP

Import Open Security Controls Assessment Language \(OSCAL\) files in the System Security Plan \(SSP\) model into Continuous Authorization and Monitoring workspace. Import OSCAL SSP enables you import authorization packages, authorization boundary, controls, and others in OSCAL format.

## Before you begin

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

**Note:**

-   The catalog, catalog overlay, System Security Plan \(SSP\), and profile file to be imported must be in JSON format and validated using the OSCAL-CLI tool [https://github.com/usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) for any validation error.
-   Recipients are notified through email on completion of the import process.

The OSCAL SSP import is an asynchronous process.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the OSCAL import landing page icon \(![OSCAL import](../image/cam-oscal-import-icon.png)\).

3.  Select **New Import** from the **All OSCAL imports** landing page.

4.  Select **SSP** from the **OSCAL Model** drop-down list.

5.  Enter the **Source** name.

6.  Enter the **Import status recipients** name.

    Recipients receive an email notification about the import status.

    ![OSCAL import SSP details tab.](../image/cam-oscal-import-ssp1.png)

7.  Select **Next** to continue to the next step in the OSCAL import process.

    You’re directed to the **Attachments** tab to attach the SSP files.

8.  In the **Attachments** tab, attach the Catalog, Profile, SSP, and Plans of Action and Milestones \(POA&amp;M\) files and then select **Next** to upload the SSP files.

    **Note:** Catalog, Profile, and SSP are required files to attach.

    -   **Catalog**: Contains the details of the control objectives and its related objects.
    -   **Profile**: Contains a baseline of selected controls from one or more control or overlay catalogs.
    -   **Catalog Overlay**: Contains information regarding overlay policies and its control objectives and behavior of the overlay. This behavior depends on the addition or subtraction in which the overlay is included in the Authorization Package. For more information, see [Apply overlays to the baseline controls](apply-overlay-to-baseline.md). You can also upload multiple overlay files.
    -   **SSP**: Contains the details of the authorization boundary, authorization package, system elements, information types, controls, common controls, inherit, hybrid controls, and others.
    -   **Data flow diagram**, **Boundary diagram**, **Network diagram**, and **Enterprise architecture**: These diagrams are attached to the authorization boundary.
    -   **POA&amp;Ms**: Contains a structured list of issues, milestones, and acceptance tasks.
9.  Select **Add file** to attach the Overlay file, then select **Next**.

    You can also upload multiple overlay files.

    ![Attach OSCAL SSP files.](../image/cam-oscal-import-ssp4.png)

10. Select **Add file** to attach the POA&amp;Ms file, then select **Next**.

    **Note:**

    -   You can upload multiple POA&amp;M files.
    -   You can’t import a POA&amp;M file, which is already linked to another active authorization package.
    -   If there are any errors in the uploaded files for import, an error message is displayed, select **Restart** to upload a valid file.

        ![Import error message.](../image/cam-oscal-import-ssp9.png)

    -   If a warning appears, you can choose to skip it and select **Next** to proceed with the import process.

        ![Import warning message.](../image/cam-oscal-import-ssp10.png)

    You’re directed to the **User and Group Mapping** tab to map the users for the import process.

11. Select the users in the **User mapping** section, then select **Next**.

    The **OSCAL Users** listed in the OSCAL file match the **ServiceNow Users** in your instance, and all roles are automatically mapped in the **Listed as** section.

12. Select the users in the **Group mapping** section, then select **Next**.

    The **OSCAL Group** listed in the OSCAL file match the **ServiceNow Group** in your instance, and all roles are automatically mapped in the **Listed as** section.

13. Select the users in the **Roles and responsibility** section, then select **Next**.

    Assign users to specific roles for the imported files. These users retain their roles throughout each step in the authorization package.

    ![User and group mapping for OSCAL import SSP.](../image/cam-oscal-import-ssp3.png)

14. You can also select the attachments, package mapping, or user and group mapping action icon \(![Restart attachments or roles and responsibilities.](../image/cam-oscal-import-attachments-icon.png)\) on the **Attachments** or **User and Group Mapping** tab to select **Restart Stage** to restart the particular stage.

    ![Restarting stage.](../image/cam-oscal-import-ssp8.png)

15. Select **Next** to verify the files you uploaded.

    **Preview and Override** tab displays.

    ![OSCAL SSP import.](../image/cam-oscal-import-ssp5.png)

16. In the **Preview and Override** tab, review the details that are to be created, skipped, or overridden and then perform one of the following:

    -   Select **Import** to import the SSP model.

        **Note:** When all the data is new and must be imported, the import action creates records for the respective data. In this case, you can’t skip or override the files. However, if you import a file with the same source and matching records, you have the option to skip the data.

    -   To override the object, perform the following actions:
        1.  Select **Select list to override** drop-down to choose the object to override.

        2.  Select **Skipped** to list the object that is to be overridden.
        3.  Select the object from the list that you want to override.

            ![Overriding skipped files.](../image/cam-oscal-import-ssp6.png)

        4.  Select **Override** to override one or more selected object.

            The selected object is flagged as overridden and the **Overridden** count is increased in the preview list.

            **Note:** Based on the object you select from the drop-down: If the object is in the **Will be skipped** state, you can only override it.

            -   When you override an Authorization Boundary, the following related objects are overridden and can’t be skipped.

                -   System elements
                -   Authorization packages
                -   Baseline controls
                -   Information types
                -   Inherited controls
                -   Hybrid controls
                -   Not applicable controls
                **Note:** A new authorization boundary isn’t created but related records are recreated.

            -   When you choose to override an authorization package, the following related objects are overridden and can’t be skipped.
                -   Baseline controls
                -   Information types
                -   Inherited controls
                -   Hybrid controls
                -   Not applicable controls
            -   When you override an authorization package, a new authorization package is created and marks the existing authorization package as inactive.
            -   When you override a control objective, its related control objective requirements are also overridden.
            -   When you override a test template, its related assessment procedures are also overridden.
            -   For POA&amp;M, skipped Acceptance tasks and milestones appear in the skipped list, but they can’t be overridden individually. To override them, the mapped POA&amp;M must be overridden. If the POA&amp;M status changes from **Override** to **Skip**, the linked Acceptance tasks and milestones follow.
    -   To skip the object, perform the following actions:
        1.  Select **Select list to override** drop-down to choose the object to skip.

        2.  Select **Overridden** to list the object that is to be skipped.

            **Note:**

            -   You can only skip it if it is in the **Overridden** state.
            -   When you skip a control objective, you can still independently override its related control objective requirements.
        3.  Select the object from the list that you want to skip.

            ![Skipping overridden files.](../image/cam-oscal-import-ssp7.png)

        4.  Select **Skip** to skip one or more selected references.

            The selected object is flagged as skip and the **Will be skipped** count is increased in the preview list.

17. Select **Import** to import the SSP files.

    **Note:** You can also select the playbook action icon \(![Restart playbook icon](../image/cam-oscal-import-action-icon.png)\) to select **Restart Playbook** to restart the playbook.

    -   A pop-up message appears on the commencement of the import process. Select **Close** and you 're directed to the OSCAL import landing page.

        ![OSCAL import process begins.](../image/cam-oscal-landing-final_ssp1.png)

    -   You can view the import status report in the **All OSCAL import** list.

        ![OSCAL import status.](../image/cam-oscal-landing-final_ssp2.png)


**Parent Topic:**[Import in OSCAL format](../concept/import-oscal.md)

