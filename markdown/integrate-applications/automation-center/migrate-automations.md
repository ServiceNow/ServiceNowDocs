---
title: Migrate automations to ServiceNow RPA Hub
description: Migrate automations to ServiceNow RPA Hub with reduced cost and effort of your migration and improving your enterprise's efficiency.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrating automations from UiPath to ServiceNow RPA Hub, Use, Automation Center, Workflow Data Fabric]
---

# Migrate automations to ServiceNow RPA Hub

Migrate automations to ServiceNow RPA Hub with reduced cost and effort of your migration and improving your enterprise's efficiency.

## Before you begin

Role required: sn\_ac.automation\_technical\_user or sn\_ac.automation\_admin

When a technical user tries to either upload a ZIP file or provide a URL when generating the migration report, an error message is displayed in the **All automations** tab. You can ignore this error message and proceed further.

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center Workspace**.

2.  Select the Migration accelerator icon \(![Migration accelerator icon](../images/mig-acc-icon.png)\) on the side bar.

3.  Select the report that has the automations you want to migrate.

4.  From the **All automations** tab, select the automations that you want to migrate.

5.  Select **Migrate**.

    The **Choose destination instance** dialog box is displayed.

6.  Select an instance where you want to migrate the automations.

    You have two options:

    -   Current Instance \(shows by default\): The logged-in user must have the rpa\_developer role, and the current instance must have app-rpa-foundation version 15.0.0 or later.
    -   Remote Instance \(Configured via Connection and Credentials alias\) - The user with whom the credentials are associated must have the rpa\_developer role and the remote instance must have app-rpa-foundation version 15.0.0 or later.
    For information on how to configure an instance, see [Configure an instance for migration](../task/config-instance.md).

7.  Select **Continue**.

8.  Select **Start Migration** on the confirmation dialog box.


## Result

The automations are migrated. If the automations are being migrated multiple times, multiple versions of the automations are created. The previous versions aren’t overwritten.

The output from the migrated automations is attached to the migrated automation as a .zip file. It has two files: An excel file and an ibot file.

For every migrated automation, an automation request is created.

The automation conversion depends on the complexity of the automation. The more complex the automation, the lower the conversion rate. All manual tasks that are required to convert the automation completely must be done on the target instance.

-   **[Configure an instance for migration](../task/config-instance.md)**  
Configure an instance to migrate your automations.

**Parent Topic:**[Migrating automations from UiPath to ServiceNow RPA Hub](migrating-automations-from-uipath.md)

