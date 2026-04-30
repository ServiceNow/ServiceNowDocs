---
title: Create a work order task template
description: Create a standalone work order task template, which can be used by different work order templates to create the same task for their work orders. It saves you the effort of creating the same task template every time for each work order template.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Standalone task templates, Template Management, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Create a work order task template

Create a standalone work order task template, which can be used by different work order templates to create the same task for their work orders. It saves you the effort of creating the same task template every time for each work order template.

## Before you begin

You must activate the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Template Management** &gt; **Work Order Task Templates**.

2.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Task type|The type of task to create. The default is Work Order Task.|
    |Name|Unique and descriptive name for this task.|
    |Short Description|Summary of this task|
    |Description|A description of this task.|
    |Parts and quantities|Parts requirements and quantities, as needed. If you selected **Part requirements are not needed by agents** on the Field Service Configuration screen, the **Parts and quantities** fields are not displayed.|
    |Checklist template|Select a checklist template from the list to add a checklist to the tasks created from this work order template.|
    |Dispatch group|The dispatch group used to select the individuals who fulfill the task.|

3.  Click **Submit**.


## Result

A standalone task template is created and ready to be mapped it to any work order template.

## What to do next

After creating a standalone task template, map it to a work order template. This enables the work order template to create similar tasks for different work orders, if required. See [Enable a work order template to create relevant tasks for a work order](add-stand-alone-task-template-to-wo-template.md).

