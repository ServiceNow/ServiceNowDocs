---
title: Create an Import Group
description: Create an import group and use it to update floor plans in bulk.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-06-24"
reading_time_minutes: 1
breadcrumb: [Bulk update floor plans, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Create an Import Group

Create an import group and use it to update floor plans in bulk.

## Before you begin

Role required: sn\_map\_core.map\_admin, sn\_map\_core.map\_editor

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Bulk imports** &gt; **Import Groups**.

    You can also navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

2.  On the Floor plan import groups list, select **New**.

    **Note:** If you are in the Map Studio, select **Import files** on the **Bulk update maps** card.

3.  On the Floor plan import group form, fill in the fields.

    For a description of the field values, see [Floor map import group form](../reference/import-group-form.md).

4.  Select **Submit**.

5.  Attach CAD or PNG files to the record.

    For more information about attaching files to a record, see [Manage attachments](https://www.servicenow.com/docs/access?context=t_ManagingAttachments&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

6.  Select **Start Import**.

    The system creates import tasks based on the number of files attached to the record.


## What to do next

Work on the import tasks that are created for your import group. For more information about working on import tasks, see [Work on an import task](work-import-task.md).

After the import tasks are created, the Automate map updates AI agentic workflow is triggered for each task. The Map Admin Agent autonomously retrieves sources for the uploaded CAD file and resumes the import task. If the source isn't found, the agent moves the task to the `Waiting user input` state.

For more information about the Automate map updates AI agentic workflow, see [Automate map updates agentic workflow](../../now-assist-wsd/concept/automate-map-updates-agent-ai.md).

**Note:** If you selected **Supervised AI execution** in the Floor map import group form, you must manually trigger the AI agent for every import task.

**Parent Topic:**[Bulk update floor plans](../concept/bulk-import-cad-files.md)

**Previous topic:**[Bulk update floor plans](../concept/bulk-import-cad-files.md)

**Next topic:**[Work on an import task](work-import-task.md)

