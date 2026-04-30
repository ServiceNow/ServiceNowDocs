---
title: Generate report
description: Generate a report to view all the automations that you want to import.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migrating automations from UiPath and Blue Prism to ServiceNow RPA Hub, Use, Automation Center, Workflow Data Fabric]
---

# Generate report

Generate a report to view all the automations that you want to import.

## Before you begin

Role required: sn\_ac.automation\_business\_user, sn\_ac.automation\_technical\_user, or sn\_ac.automation\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

2.  Select the Migration accelerator icon \(![Migration accelerator icon](../images/mig-acc-icon.png)\) on the side bar.

3.  Select **Generate migration report**.

    The Generate a migration report dialog is displayed.

4.  Provide the details in the dialog box:

    -   Provide a report name.
    -   Select source details:
        -   Select the source: UiPath or Blue Prism.

            **Note:** Repository URL us available only for UiPath. For Blue Prism you must upload a ZIP file.

        -   **Repository URL** \(only if you select UiPath as the source\): This option enables you to get data from UiPath Orchestration. For information on using this option, see [Generate report using repository URL](../task/repo-url.md).
        -   **Upload ZIP \(with XAML files\)**: This option enables you to upload a local zip with .xaml files and automations. For information on using this option, see [Generate a report using a ZIP file](../task/zip-file.md).
    **Note:** If the report generation takes longer than 300 seconds \(5 minutes\), it is marked as failed. This is controlled by a system property, `sn_ac.polling_timeout_migration_report`. A technical user \(with the role sn\_ac.automation\_technical\_user\) can make changes to the value of the system property.


-   **[Generate report using repository URL](../task/repo-url.md)**  
Generate a migration report using the repository URL that has all the automation files saved.
-   **[Generate a report using a ZIP file](../task/zip-file.md)**  
Generate a migration report using all the files that you have on your local system in a zip file.

**Parent Topic:**[Migrating automations from UiPath and Blue Prism to ServiceNow RPA Hub](migrating-automations-from-uipath.md)

