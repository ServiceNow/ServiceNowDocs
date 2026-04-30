---
title: Revert Software Asset Management customizations
description: After installing the Software Asset Management application for the first time, or upgrading from the Software Asset Management Foundation plugin, you need to revert customizations for all features work. The Revert Customizations module in the Software Asset Management application can revert customized files related to Software Asset Management back to the base configurations that were skipped during the installation or upgrade process.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Revert Software Asset Management customizations

After installing the Software Asset Management application for the first time, or upgrading from the Software Asset Management Foundation plugin, you need to revert customizations for all features work. The Revert Customizations module in the Software Asset Management application can revert customized files related to Software Asset Management back to the base configurations that were skipped during the installation or upgrade process.

## Before you begin

Role required: sam\_admin

## About this task

The Revert Customizations module shows the **Software Asset Skipped Files** list. All customizations and configurations related to Software Asset Management can be reverted to the base application version.

To ensure feature functionality, you must revert customizations after:

-   A new installation of the Software Asset Management Professional \(com.snc.samp\) plugin
-   Upgrading from the Software Asset Management Foundation \(com.snc.sams\) plugin

You can also revert customizations using the **System Diagnostics** &gt; **Upgrade History** navigation.

## Procedure

1.  Navigate to **Software Asset** &gt; **Administration** &gt; **Revert Customizations** to view the Software Asset Skipped Files list.

2.  Select **Revert** to revert all files with a disposition of **Skipped** to the base application version.

3.  Verify that the disposition of all skipped files is **Reverted** in the customization summary.

    You can also verify the disposition of all skipped files in the Upgrade Details \[sys\_upgrade\_history\_log\] table and the current OOB version in the Update Versions \[sys\_update\_version\] table.


