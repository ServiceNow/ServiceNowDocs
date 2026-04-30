---
title: Perform post-migration tasks for form headers
description: Verify that the form header in Service Operations Workspace \(SOW\) are consistent with the form header in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated form header settings in SOW based on your requirements.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configurations and customizations that can be migrated from ITSM Agent workspace to SOW for ITSM, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for form headers

Verify that the form header in Service Operations Workspace \(SOW\) are consistent with the form header in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated form header settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **Record form headers** option for ITSM Agent Workspace features. For example, the **Record form headers** option for Change Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).![Record form header selected in SOW Migration utility tool options](../image/mu-sow-form-header-select.png)

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps to verify the migration.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Open a record in SOW that is corresponding to a table for which form header are migrated.

        For example: If you want to verify the form header migration status for an incident form header, navigate to **List** &gt; **Incident** &gt; **All** and then select any incident record.

    3.  Review the form header on the record.

        You can also view the form header record in sys\_aw\_form\_header and mapping data in the sys\_ux\_m2m\_workspace\_header\_ux\_header\_config table to verify the migrated data.

    4.  If the migration is successful and the form header that exist in ITSM Agent Workspace is not displayed in SOW record, verify the order value of the form header in the sys\_aw\_form\_header table to ensure that it has the least order value.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![Error](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/form-headers-migration-itsm-aw-sow.md#section_tmq_q2j_dcc) section.


**Parent Topic:**[Migration of form headers from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/form-headers-migration-itsm-aw-sow.md)

