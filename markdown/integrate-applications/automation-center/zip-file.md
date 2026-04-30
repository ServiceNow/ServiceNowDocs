---
title: Generate a report using a ZIP file
description: Generate a migration report using all the files that you have on your local system in a zip file.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Generate report, Migrating automations from UiPath and Blue Prism to ServiceNow RPA Hub, Use, Automation Center, Workflow Data Fabric]
---

# Generate a report using a ZIP file

Generate a migration report using all the files that you have on your local system in a zip file.

## Before you begin

Role required: sn\_ac.automation\_business\_user, sn\_ac.automation\_technical\_user, or sn\_ac.automation\_admin

## Procedure

1.  Follow steps 1 through 4 in the [Generate report](../concept/generate-report.md) section.

2.  On step 4, select the **Upload ZIP \(with XAML file\)** option.

    You can upload only one zip file at a time, and the maximum file size is 100 MB.

    **Note:** When selecting UiPath as the source, a ZIP file exported from UiPath Orchestrator should be uploaded. Similarly, when selecting Blue Prism, the ZIP file exported from Blue Prism should be uploaded.

3.  Select **Add file**.

4.  Select **Generate report**.

    A dialog box is displayed with details of the migration. You can choose to run it in the background.

    The report is generated.


**Parent Topic:**[Generate report](../concept/generate-report.md)

