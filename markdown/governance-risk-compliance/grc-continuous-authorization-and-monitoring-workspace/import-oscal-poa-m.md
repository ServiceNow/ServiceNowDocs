---
title: Import OSCAL POA&amp;M
description: Import Open Security Controls Assessment Language \(OSCAL\) Plans of Action and Milestones \(POA&amp;M\) JSON files by selecting the POA&amp;M model into Continuous Authorization and Monitoring workspace. Import OSCAL POA&amp;M action enables you to upload POA&amp;Ms files and link it to CAM relevant objects like controls, authorization packages, engagements, and others in OSCAL format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal-poa-m.html
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Import in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL POA&amp;M

Import Open Security Controls Assessment Language \(OSCAL\) Plans of Action and Milestones \(POA&amp;M\) JSON files by selecting the **POA&amp;M** model into Continuous Authorization and Monitoring workspace. Import OSCAL POA&amp;M action enables you to upload POA&amp;Ms files and link it to CAM relevant objects like controls, authorization packages, engagements, and others in OSCAL format.

## Before you begin

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

**Note:**

-   The Plan of Actions and Milestones \(POA&amp;Ms\) file to be imported must be in JSON format and validated using the OSCAL-CLI tool [https://github.com/usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) for any validation error.
-   Recipients are notified through email on completion of the import process.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the OSCAL import landing page icon \(\[Omitted image "cam-oscal-import-icon.png"\] Alt text: OSCAL import\).

3.  On the **All OSCAL imports** landing page, select **New Import**.

4.  Select **POA&amp;M** from the **OSCAL Model** drop-down list.

5.  Enter the **Import status recipients** name.

    Recipients receive an email notification about the import status.

    \[Omitted image "cam-oscal-import-poam1.png"\] Alt text: OSCAL import POA&amp;M details tab.

6.  Select **Next** to continue to the next step in the OSCAL import process.

7.  Select **Add file** to attach the POA&amp;Ms file.

8.  Enter the **Title** for the POA&amp;M `json` file, then select **Upload**.

    -   You can upload multiple POA&amp;M files, but all the files should be linked to a same authorization package.
    -   If there are any errors in the uploaded files for import, an error message is displayed, select **Restart** to upload a valid file. If a warning appears, you can choose to skip it and select **Next** to proceed with the import process.
    -   Error: The import fails if a POAM item is mapped to multiple observations or findings. To resolve this issue, correct the JSON file and restart the attachment stage.
    -   Warning: The system skips a POAM item if it’s linked to a non-existent object such as a control, control requirement, or control test. The warning count displays the number of skipped items.
    \[Omitted image "cam-oscal-import-poam2.png"\] Alt text: Uploading POA&amp;M json file.

9.  Select **Next** to continue to the next step in the OSCAL import process.

    You’re directed to the **Package Mapping** tab to associate the POA&amp;M file to a package.

    **Note:** The Package field auto-populates if the related SSP was already imported. You can change the default value and map the POA&amp;M to any other existing package that is in the Implement stage or higher.

10. Select an authorization package from the list, then select **Next**.

    You’re directed to the **User and Group Mapping** tab to map the users for the import process.

11. Select the users in the **User mapping** section, then select **Next**.

    The **OSCAL Users** listed in the OSCAL file match the **ServiceNow Users** in your instance, and all roles are automatically mapped in the **Listed as** section.

12. Select the users in the **Group mapping** section, then select **Next**.

    The **OSCAL Group** listed in the OSCAL file match the **ServiceNow Group** in your instance, and all roles are automatically mapped in the **Listed as** section.

    \[Omitted image "cam-oscal-import-poam3.png"\] Alt text: User and Group mapping.

13. You can also select the attachments, package mapping, or user and group mapping action icon \(\[Omitted image "cam-oscal-import-attachments-icon.png"\] Alt text: Restart attachments or roles and responsibilities.\) on the **Attachments**, **Package Mapping**, or **User and Group Mapping** tab to select **Restart Stage** to restart the particular stage.

    \[Omitted image "cam-oscal-import-poam7.png"\] Alt text: Restarting stage.

14. Select **Next** to verify the files you uploaded.

    \[Omitted image "cam-oscal-import-poam4.png"\] Alt text: OSCAL POA&amp;M import.

    **Preview and Override** tab displays.

15. In the **Preview and Override** tab, review the details that are to be created, skipped, or overridden and then perform one of the following:

    -   Select **Import** to import the POA&amp;M model.

        **Note:** When all the data is new and must be imported, the import action creates records for the respective data. In this case, you can’t skip or override the files. However, if you import a file with the same package and matching records, you have the option to skip the data.

    -   To override data, perform the following actions:
        1.  Select **Select list to override** to choose the object to override.

        2.  Select **Skipped** to list the object that is to be overridden.

            **Note:** Based on the object you select from the drop-down: If the object is in the **Will be skipped** state, you can only override it. If the POA&amp;M status changes from **Override** to **Skip**, the linked Acceptance tasks and milestones follow.

        3.  Select the object from the list that you want to override.

            \[Omitted image "cam-oscal-import-poam5.png"\] Alt text: Overriding skipped files.

        4.  Select **Override** to override one or more selected objects.

            The selected objects are flagged as overridden and the **Overridden** count is increased in the preview list.

    -   To skip data, perform the following actions:
        1.  Select **Select list to override** to choose the objects to skip.

        2.  Select **Overridden** to list the object that is to be skipped.

            **Note:** If it is in the **Overridden** state, you can only skip it.

        3.  Select the object from the list that you want to skip.

            \[Omitted image "cam-oscal-import-poam6.png"\] Alt text: Skipping overridden files.

        4.  Select **Skip** to skip one or more selected objects.

            The selected objects are flagged as skip and the **Will be skipped** count is increased in the preview list.

16. Select **Import** to import the POA&amp;M files.

    **Note:** You can also select the playbook action icon \(\[Omitted image "cam-oscal-import-action-icon.png"\] Alt text: Restart playbook icon\) to select **Restart Playbook** to restart the playbook.

    -   A pop-up message appears on the commencement of the import process. Select **Close** and you 're directed to the OSCAL import landing page.

        \[Omitted image "cam-import-oscal-landing-page2.png"\] Alt text: OSCAL import process begins.

    -   You can view the import status report in the **All OSCAL import** list.

        \[Omitted image "cam-oscal-landing-final1.png"\] Alt text: OSCAL import status.


**Parent Topic:**[Import in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.md)

