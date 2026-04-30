---
title: Import OSCAL catalog
description: Import Open Security Controls Assessment Language \(OSCAL\) JSON format in the Catalog files into CAM workspace. This task focuses on uploading and processing the required JSON files to begin the import process.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Import in OSCAL format, CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Import OSCAL catalog

Import Open Security Controls Assessment Language \(OSCAL\) JSON format in the Catalog files into CAM workspace. This task focuses on uploading and processing the required JSON files to begin the import process.

## Before you begin

Role required: sn\_irm\_cont\_auth.info\_system\_sec\_manager, sn\_irm\_cont\_auth.info\_system\_sec\_officer, or sn\_irm\_cont\_auth.admin

**Note:**

-   The catalog file to be imported must be in JSON format and validated using the OSCAL-CLI tool [https://github.com/usnistgov/oscal-cli](https://github.com/usnistgov/oscal-cli) for any validation error.
-   Recipients are notified through email on completion of the import process.

The OSCAL catalog import is a synchronous process.

## Procedure

1.  Navigate to **Workspaces** &gt; **CAM Workspace**.

2.  In the CAM Workspace, select the OSCAL import landing page icon \(![OSCAL import](../image/cam-oscal-import-icon.png)\).

3.  Select **New Import** from the **All OSCAL imports** landing page.

4.  Select **Catalog** from the **OSCAL Model** drop-down list.

    By default the Catalog model is selected.

5.  Enter the **Source** name.

    The source name that you enter is used as the name for the imported control objective. If a control objective with the same source name exists, the file is skipped during import.

    ![OSCAL import Catalog details tab.](../image/cam-oscal-import-catalog1.png)

6.  Enter the **Import status recipients** name.

    You can list the users you want to be notified once the OSCAL import is complete. The recipients receive an email notification on the import status.

7.  Select **Next** to continue to the next step in the OSCAL import process.

    You’ll be directed to the **Attachments** tab to attach the catalog file.

8.  Select the **Attach File** in the **Attachments** tab to attach the catalog file from your local repository.

    ![OSCAL Catalog Import.](../image/cam-oscal-import-catalog.png)

9.  Select **Next** to verify the files you uploaded.

    The **Preview and Override** tab displays.

    ![OSCAL Catalog preview tab.](../image/cam-oscal-import-catalog2.png)

10. In the **Preview and Override** tab, review the details that are to be created, skipped, or overridden and then perform one of the following:

    -   Select **Import** to import the Catalog model.

        **Note:** When all the data is new and must be imported, the import action creates new records for the respective data. In this case, you can’t skip or override the files. However, if you import a file with the existing source and matching records, you’ll have the option to skip or override the data.

    -   To override data, perform the following actions:
        1.  Select **Select list to override** to choose the data to override.

        2.  Select **Skipped** to list the reference that is to be skipped.

            **Note:** Based on the data you select from the drop-down: If the data is in the **Will be skipped** state, you can only override it. When you override a control objective, all associated control objective requirements will also be overridden.

            ![Overriding skipped files.](../image/cam-oscal-import-catalog3.png)

        3.  Select the reference from the list that you want to override.
        4.  Select **Override** to override one or more selected references.

            The selected reference is flagged as overridden and the **Overridden** count is increased in the preview list.

    -   To skip data, perform the following actions:
        1.  Select **Select list to override** to choose the data to skip.

        2.  Select **Overridden** to list the reference that is to be skipped.

            **Note:** If it is in the **Overridden** state, you can only skip it.

        3.  Select the reference from the list that you want to skip.![Skipping overridden files.](../image/cam-oscal-import-catalog4.png)
        4.  Select **Skip** to override one or more selected references.

            The selected reference is flagged as skip and the **Will be skipped** count is increased in the preview list.

11. Select **Import** to import the catalog files.

    **Note:**

    -   The CAM OSCAL catalog import model doesn’t support test templates and assessment procedures if they’re included in the catalog JSON file.
    -   If an error occurs during the import process, review the error message displayed in the pop-up and take the necessary corrective action.
    You can view the import status report in the **All OSCAL import** landing page.

    All the necessary control objectives are created with the source specified.

    For more information on OSCAL import error, see the [OSCAL Import \[KB1794095\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1794095) article in the Now Support knowledge base.

12. If an error occurs during the import process, review the error message displayed in the pop-up and take the necessary corrective action.

    You can also select the attachments action icon \(![Restart attachments.](../image/cam-oscal-import-attachments-icon.png)\) on the **Attachments** tab to select **Restart Stage** to restart the attachments.![Restarting attachment stage.](../image/cam-oscal-import-catalog5.png)

    **Note:** You can also select the playbook action icon \(![Restart playbook icon](../image/cam-oscal-import-action-icon.png)\) to select **Restart Playbook** to restart the playbook.


**Parent Topic:**[Import in OSCAL format](../concept/import-oscal.md)

