---
title: Generate a report using a ZIP file
description: Generate a migration report using all the files that you have on your local system in a zip file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/automation-center/zip-file.html
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Generate report, Migrating automations from third-party applications, Use, Automation Center, Workflow Data Fabric]
---

# Generate a report using a ZIP file

Generate a migration report using all the files that you have on your local system in a zip file.

## Before you begin

Role required: sn\_ac.automation\_business\_user, sn\_ac.automation\_technical\_user, or sn\_ac.automation\_admin

## Procedure

1.  Follow steps 1 through 4 in the [Generate report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/automation-center/generate-report.md) section.

2.  On step 4, select the **Upload ZIP \(with XAML file\)** option.

3.  Select **Add file**.

    You can upload only one ZIP file at a time, and the maximum file size is 100 MB.

    **Note:** Select the ZIP file exported from the respective applications. If you use an UIPath orchestrator data for Blue Prism, it will show an error.

4.  Select **Generate report**.

    A dialog box is displayed with details of the migration. You can choose to run it in the background.

    The report is generated.


**Parent Topic:**[Generate report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/automation-center/generate-report.md)

