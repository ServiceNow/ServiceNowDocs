---
title: Configure Hardware Asset Management using the Configuration Console
description: Configure the Hardware Asset Management application to manage hardware asset lifecycle, inventory, integrations, and team management setup from a centralized console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/configure-ham-from-console.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 3
breadcrumb: [Configuration Console for Hardware Asset Management, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Configure Hardware Asset Management using the Configuration Console

Configure the Hardware Asset Management application to manage hardware asset lifecycle, inventory, integrations, and team management setup from a centralized console.

## Before you begin

The Hardware Asset Management \(HAM\) application must be installed on your ServiceNow instance.

Role required: To access the Configuration Console, you must have the ham\_admin and ia\_user roles. The setup items available within the console depend on the additional roles assigned. For more information on roles required for modules, see [Configuration Console for Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/config-console-ham.md).

## About this task

The Configuration Console organizes HAM setup into modules. Each module is independent — you can configure the modules and their setup items in any order. The setup items that appear in each module depend on which dependent applications are installed on your ServiceNow instance. If a dependent application isn't installed, its related setup items are hidden automatically.

The **Setup status** section tracks your overall configuration progress. It displays a progress card for each module showing the total number of setup items and how many you have marked as configured.

When you make changes through the Configuration Console, the system captures them in an update set automatically. The update set uses a naming convention defined by the Implementation Agent framework. Child update sets are created for each module's configuration changes under a parent update set. After completing your configuration, you can bundle the update set and apply it to a production instance to replicate the same configuration without repeating the setup manually.

**Note:** You can also upload an existing update set from another ServiceNow instance on the Product Hub page if you want to replicate a previously completed configuration. Only one XML file can be uploaded at a time.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  In the **Manage your products** section of the Admin Home page, select the **Hardware Asset Management** card to open the Product Hub.

3.  In the Configure your product section, select **Configure**.

    -   The Configure Hardware Asset Management page opens in the Configuration Console.
    -   The Setup section displays a progress card for each module showing the total number of setup items and how many are configured. The Setup status section tracks your overall configuration progress
    -   The Configuration Summary in the navigation menu shows the configuration modules and setup items.
    **Tip:** To find a specific setup item without expanding modules manually, enter a keyword in the **Search configurations** field at the top of the console.

4.  Select a module that you want to configure.

    -   From the Configuration Summary navigation menu, select a module.
    -   From the Setup status section, select **Get started** on the module that you want to configure.
    You can configure the modules and their setup items in any order. For a complete list of modules and setup items, see [Modules in the Configuration Console for HAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/config-console-modules-ham.md).

5.  After completing a setup item, select **Mark as configured**.

    **Note:** Marking an item as configured is reversible. You can return to any setup item and change its configuration status at any time.

6.  Review the **Setup status** section to confirm the overall configuration progress.

7.  To bundle your configuration changes for deployment, select **Package and download**.

    The update set is packaged and downloaded as an XML file. Apply this file to a production instance to replicate the same configuration.


## Result

-   Configured items show a Completed status in the Setup status section. As you complete each setup item and mark it as configured, the progress cards update in real-time. You can use the Setup status section to monitor progress, identify items that aren't yet configured, and return to any item at any time.
-   The system captures changes in an Update Set automatically.

    **Note:** You can apply the Update Set to a production instance to replicate the same configuration.


