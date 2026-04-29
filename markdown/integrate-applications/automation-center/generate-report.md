---
title: Generate report
description: Generate a report to view all the automations that you want to import.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrating automations from UiPath to ServiceNow RPA Hub, Use, Automation Center, Workflow Data Fabric]
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
        -   **Repository URL**: This option enables you to get data from UiPath Orchestration. For information on using this option, see [Generate report using repository URL](../task/repo-url.md).
        -   **Uplaod ZIP \(with XAML files\)**: This option enables you to upload a local zip with .xaml files and automations. For information on using this option, see [Generate a report using a ZIP file](../task/zip-file.md).

-   **[Generate report using repository URL](../task/repo-url.md)**  
Generate a migration report using the repository URL that has all the automation files saved.
-   **[Generate a report using a ZIP file](../task/zip-file.md)**  
Generate a migration report using all the files that you have on your local system in a zip file.

**Parent Topic:**[Migrating automations from UiPath to ServiceNow RPA Hub](migrating-automations-from-uipath.md)

