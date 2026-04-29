---
title: Perform post-migration tasks for highlighted fields in list and forms
description: Verify that the highlighted fields in list and forms in Service Operations Workspace \(SOW\) are consistent with the highlighted fields in list and forms in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated highlighted fields in list and forms settings in SOW based on your requirements.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Highlighted fields in lists and forms, Configure and customize the migration to SOW, Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM, Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Perform post-migration tasks for highlighted fields in list and forms

Verify that the highlighted fields in list and forms in Service Operations Workspace \(SOW\) are consistent with the highlighted fields in list and forms in ITSM Agent Workspace \(ITSM AW\) and are ready for use in SOW. You can update the migrated highlighted fields in list and forms settings in SOW based on your requirements.

## Before you begin

When performing the migration, you must have selected the **Highlighted fields in list and forms** option for ITSM Agent Workspace features. For example, the **Highlighted fields in list and forms** option for Incident Management. For information about the migration process, see [Migrate from ITSM Agent Workspace to Service Operations Workspace for ITSM](migrate-itsm-agent-workspace-to-sow.md).

Role required: admin

## About this task

At the end of the migration process, a confirmation message specifies if the migration is successful or not. You can review the migration information and perform the post-migration steps to ensure successful migration of your configuration or customization.

## Procedure

1.  If the migration is successful, perform the following steps to verify the migration.

    1.  Open SOW for ITSM and ITSM Agent Workspace instances.

        -   To open SOW, navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.
        -   To open ITSM Agent Workspace, enter `<instance-name>.service-now/workspace` in the web browser.
    2.  Open a record in SOW that is corresponding to the table for which highlighted list and form field configurations are migrated.

        For example: If you want to verify the highlighted list and form field migration status for an incident, navigate to **List** &gt; **Incident** &gt; **All** and then select any incident record.

    3.  Review the highlighted list and form fields for an incident list and record to ensure if the highlighted values are displayed as in ITSM Agent Workspace.

    4.  If the highlighted values are not working as expected, navigate to **All** &gt; **sys\_highlighted\_value.list**.

    5.  Search the **Table** and **Field** record for which the issue exists.

        For example, table is Incident and field is Priority.

    6.  If more than one record with the same **Table** and **Field** combination exist, open the records to check which records are mapped to the SOW Highlighted value config using the sys\_ux\_m2m\_highlighted\_value\_config record in the UX Highlighted Values Configurations related list.

    7.  If there is more than one sys\_highlighted\_value linked to SOW Highlighted value config for that Table and Field combination exist, review the order of the conditions in the Highlighted Value Condition\(sys\_highlighted\_value\_condition\) related list record for each sys\_highlighted\_value.

        The sys\_highlighted\_value\_condition record with lower order is given precedence when rendering the highlighted color for a field in UI.

2.  If the migration fails, perform the following steps.

    1.  On the migration completion page in SOW Admin Center, select **View migration details**.

    2.  Select the **Go to system logs** \(![Error](../../service-builder/image/sb-service-triangle.png)\) icon.

    3.  Review the logs to determine which items failed during migration.

    4.  For each failed item, identify which step has failed and perform the steps mentioned in the [How the migration works](../reference/highlighted-fields-lists-forms-migration-itsm-aw-sow.md#section_ysx_zyl_ccc) section.


**Parent Topic:**[Migration of highlighted fields in lists and forms from ITSM Agent Workspace to Service Operations Workspace for ITSM](../reference/highlighted-fields-lists-forms-migration-itsm-aw-sow.md)

