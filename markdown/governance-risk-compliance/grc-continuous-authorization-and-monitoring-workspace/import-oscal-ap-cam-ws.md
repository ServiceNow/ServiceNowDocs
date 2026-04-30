---
title: Import OSCAL AP
description: Import Assessment Plan \(AP\) data in Open Security Controls Assessment Language \(OSCAL\) format to create or update authorization packages with assessment-related information including engagements, control tests, test plans, and assessment procedures.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-01-16"
reading_time_minutes: 7
breadcrumb: [Import in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL AP

Import Assessment Plan \(AP\) data in Open Security Controls Assessment Language \(OSCAL\) format to create or update authorization packages with assessment-related information including engagements, control tests, test plans, and assessment procedures.

## Before you begin

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

**Note:**

-   The catalog, catalog overlay, System Security Plan \(SSP\), profile, and Assessment Plan \(AP\) file to be imported must be in JSON format and validated using the OSCAL-CLI tool [https://github.com/usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) for any validation error.
-   Recipients are notified through email on completion of the import process.

The OSCAL AP import is an asynchronous process.

## About this task

The Assessment Plan import creates or updates the following components based on the OSCAL JSON structure:

-   Authorization boundary \(if not skipped\)
-   System elements \(if boundary not skipped\)
-   Authorization package
-   Information types
-   Baseline controls
-   Inherited Controls
-   Hybrid Controls
-   Not Applicable Controls
-   Engagement
-   Entity
-   Test Plan
-   Assessment Procedures Plan
-   Control Test
-   Assessment Procedure Test
-   Control objectives
-   Control objective requirements
-   Test templates
-   Assessment procedures

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the OSCAL import landing page icon \(![OSCAL import](../image/cam-oscal-import-icon.png)\).

3.  Select **New Import** from the **All OSCAL imports** landing page.

4.  Select **AP** from the **OSCAL Model** drop-down list.

5.  Enter the **Source** name.

6.  Enter the **Import status recipients** name.

    Recipients receive an email notification about the import status.

7.  Select **Next** to continue to the next step in the OSCAL import process.

    You’re directed to the **Attachments** tab to attach the SSP files.

8.  In the **Attachments** tab, attach the Catalog, Profile, and SSP files and then select **Next** to upload the AP files.

    **Note:** Catalog, Profile, and SSP are required files to attach.

    -   **Catalog**: Contains the details of the control objectives and its related objects.
    -   **Profile**: Contains a baseline of selected controls from one or more control or overlay catalogs.
    -   **Catalog Overlay**: Contains information regarding overlay policies and its control objectives and behavior of the overlay. This behavior depends on the addition or subtraction in which the overlay is included in the Authorization Package. For more information, see [Apply overlays to the baseline controls](apply-overlay-to-baseline.md). You can also upload multiple overlay files.
    -   **SSP**: Contains the details of the authorization boundary, authorization package, system elements, information types, controls, common controls, inherit, hybrid controls, and others.
    -   **Data flow diagram**, **Boundary diagram**, **Network diagram**, and **Enterprise architecture**: These diagrams are attached to the authorization boundary.
9.  Select **Add file** to attach the Overlay file, then select **Next**.

    In the **Upload a file** pop-up page, enter the **Title** for the AP `json` file, then select **Upload**. You can also upload multiple overlay files.

10. Select **Add file** to attach the AP file.

    In the **Upload a file** pop-up page, enter the **Title** for the AP `json` file, then select **Upload**.

11. Select **Next** to proceed with the import process.

12. Select **Add file** to attach the POA&amp;Ms file.

    In the **Upload a file** pop-up page, enter the **Title** for the POA&amp;M `json` file, then select **Upload**.

    **Note:**

    -   You can upload multiple POA&amp;M files.
    -   You can’t import a POA&amp;M file, which is already linked to another active authorization package.
    -   If there are any errors in the uploaded files for import, an error message is displayed, select **Restart** to upload a valid file.
    -   If a warning appears, you can choose to skip it and select **Next** to proceed with the import process.
13. Select **Next** to proceed with the import process.

    You’re directed to the **User and Group Mapping** tab to map the users for the import process.

14. Select the users in the **User mapping** section, then select **Next**.

    The **OSCAL Users** listed in the OSCAL file match the **ServiceNow Users** in your instance, and all roles are automatically mapped in the **Listed as** section.

15. Select the users in the **Group mapping** section, then select **Next**.

    The **OSCAL Group** listed in the OSCAL file match the **ServiceNow Group** in your instance, and all roles are automatically mapped in the **Listed as** section.

16. Select the users in the **Roles and responsibility** section, then select **Next**.

    Assign users to specific roles for the imported files. These users retain their roles throughout each step in the authorization package.

17. You can also select the attachments, package mapping, or user and group mapping action icon \(![Restart attachments or roles and responsibilities.](../image/cam-oscal-import-attachments-icon.png)\) on the **Attachments** or **User and Group Mapping** tab to select **Restart Stage** to restart the particular stage.

    ![Restarting stage.](../image/cam-oscal-import-ssp8.png)

18. Select **Next** to verify the files you uploaded.

    **Preview and Override** tab displays.

    ![OSCAL SSP import.](../image/cam-oscal-import-ssp5.png)

19. In the **Preview and Override** tab, review the details that are to be created, skipped, or overridden and then perform one of the following:

    -   Select **Import** to import the AP model.

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
        4.  Select **Skip** to skip one or more selected references.

            The selected object is flagged as skip and the **Will be skipped** count is increased in the preview list.

20. Select **Import** to import the AP files.

    **Note:** You can also select the playbook action icon \(![Restart playbook icon](../image/cam-oscal-import-action-icon.png)\) to select **Restart Playbook** to restart the playbook.

    -   A pop-up message appears on the commencement of the import process. Select **Close** and you 're directed to the OSCAL import landing page.

        ![OSCAL import process begins.](../image/cam-oscal-landing-final_ssp1.png)

    -   You can view the import status report in the **All OSCAL import** list.

        ![OSCAL import status.](../image/cam-oscal-landing-final_ssp2.png)

    After you initiate the import, the system displays the status for each component as pending, in progress, or completed.


## Result

The system creates or updates the authorization package with assessment information. You can view the created components:

-   The authorization package appears in the package list with assessment procedures and control tests
-   Engagements are created and linked to the package
-   Control tests are generated with the appropriate test templates
-   Test plans are created for each entity
-   Assessment procedures are linked to their respective controls with correct control objectives

The source value you specified during import appears in the Source field for control objectives and other imported components, while entities may reference different sources if they originated from separate OSCAL catalogs.

**Parent Topic:**[Import in OSCAL format](../concept/import-oscal.md)

