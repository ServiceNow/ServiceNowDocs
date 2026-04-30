---
title: Generate report using repository URL
description: Generate a migration report using the repository URL that has all the automation files saved.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Generate report, Migrating automations from UiPath and Blue Prism to ServiceNow RPA Hub, Use, Automation Center, Workflow Data Fabric]
---

# Generate report using repository URL

Generate a migration report using the repository URL that has all the automation files saved.

## Before you begin

Role required: sn\_ac.automation\_business\_user, sn\_ac.automation\_technical\_user, or sn\_ac.automation\_admin, and connection\_admin role

**Note:** This option is available only for connections connecting to cloud.uipath. You need the UiPath spoke to perform this task.

## Procedure

1.  Follow steps 1 through 4 in the [Generate report](../concept/generate-report.md) section.

2.  On step 4, select the **Repository URL** option.

3.  Provide the following details in the Select repository connection section:

    1.  **Connection alias**: Select a saved connection alias form the list.
    2.  \(Optional\) Select **Create connection** to create a connection.

        For more information, see [Configure an instance for migration](config-instance.md).

    3.  **Base URL**: This field auto-populates with the corresponding value when an alias is selected.
4.  Select **Generate report**.

    A dialog box is displayed with details of the migration. You can choose to run it in the background.

    The report is generated.


**Parent Topic:**[Generate report](../concept/generate-report.md)

