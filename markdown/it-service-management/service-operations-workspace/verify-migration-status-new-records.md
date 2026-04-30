---
title: Perform post-migration tasks for new records
description: Verify that the new record menus in Service Operations Workspace \(SOW\) are consistent with the new record menus in ITSM Agent Workspace \(ITSM AW\) and they are ready for use in SOW. You can update the migrated new record menu settings in SOW based on your requirements.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for new records

Verify that the new record menus in Service Operations Workspace \(SOW\) are consistent with the new record menus in ITSM Agent Workspace \(ITSM AW\) and they are ready for use in SOW. You can update the migrated new record menu settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **New Records** option for ITSM Agent Workspace features. For example, the **New Records** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps to verify the migration.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Verify that the menu items are available in the SOW.

        By default, order is same as available in the ITSM Agent Workspace except for some menu items that are available in the SOW out-of-the-box.

    3.  To make any modifications in order in which the menu items appear on UI, navigate to **All** &gt; **sys\_ux\_page\_property.list**.

    4.  Filter the **Name** with **chrome\_tab** property.

    5.  Select **chrome\_tab** property for Service Operations Workspace.

    6.  In the **Value** field, under the **newTabMenu**, order the JSON object for tables as required.

2.  If the migration fails, perform the following steps.

    1.  Navigate to **All** &gt; **sys\_ux\_page\_property.list**

    2.  Filter the **Name** with **chrome\_tab** property.

    3.  Select **chrome\_tab** property for Service Operations Workspace.

    4.  In the **Value** field, under the **newTabMenu**, add JSON object for tables that are required in SOW new record menu item in the specified format.

    5.  Select **Update**.


**Parent Topic:**[New record menu items migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/new-record-menu-items-migration-itsm-aw-sow.md)

