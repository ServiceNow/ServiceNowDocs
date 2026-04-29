---
title: Upload CAD files
description: Import floor plans by uploading the CAD files in bulk.
locale: en-US
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Bulk hierarchy upload, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Upload CAD files

Import floor plans by uploading the CAD files in bulk.

## Before you begin

Role required: sn\_map\_core.map\_admin

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

2.  On the **Bulk hierarchy upload** card, select **Upload hierarchy**.

3.  In the Upload CAD Files section, select **Upload Floor Plans**.

4.  On the Floor plan import group form, fill in the fields.

    For a description of the field values, see [Floor map import group form](../reference/import-group-form.md).

5.  Select **Submit**.

6.  Attach CAD or PNG files to the record.

    For more information about attaching files to a record, see [Manage attachments](https://www.servicenow.com/docs/access?context=t_ManagingAttachments&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

7.  Select **Start Import**.

    The system creates import tasks based on the number of files attached to the record.


## What to do next

-   Work on the import tasks that are created for your import group. For more information about working on import tasks, see [Work on an import task](work-import-task.md).

    After the import tasks are created, the Automate map updates AI agentic workflow is triggered for each task. The Map Admin Agent autonomously retrieves sources for the uploaded CAD file and resumes the import task. If the source isn't found, the agent moves the task to the `Waiting user input` state.

    For more information about the Automate map updates AI agentic workflow, see [Automate map updates agentic workflow](../../now-assist-wsd/concept/automate-map-updates-agent-ai.md).

    **Note:** If you selected **Supervised AI execution** in the Floor map import group form, you must manually trigger the AI agent for every import task.

-   You can auto-generate the georeference for an uploaded floor plan by navigating to the Autocad source, then selecting **Auto Generated Georeference** from the Configuration tab.

    ![Configuration tab on the Autocad source form with the Auto Generate Georeference check box selected.](../images/autocad-auto-georef.png)

    **Note:** The sn\_map\_core.hide\_outdoor\_when\_georeference\_is\_auto\_generated system property controls whether the world map is hidden when entering a building for floors with an auto-generated georeference.


