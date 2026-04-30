---
title: Change default values of copied fields
description: Change the default values of in the new partial project.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Copy an existing task or project, Create a project task from a project, Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Change default values of copied fields

Change the default values of in the new partial project.

## Before you begin

Role required: admin

## About this task

Actual duration and the actual start and end dates are reset to null values. The state is set to **New** and percent complete is set to **0**. Administrators can modify UI pages to determine which fields are reset or to change the default values.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Pages**.

2.  Open the copy\_partial\_project record.

3.  Use the following script if in the **Processing script** field:

    ```
    /* resetFields is the array containing the list of names of fields that need to be erased from the copied project tasks
    	   * defaultFields is the array containing the key, value pairs of field names and values that need to be set on the copied tasks
    	   */var resetFields =new Array();var defaultFields ={};
    	  resetFields.push("work_start","work_end","work_duration");
    	  defaultFields["state"]="-5";
    	  defaultFields["percent_complete"]="0";
    ```


**Parent Topic:**[Copy an existing task or project](t_CopyExistingTaskorProject.md)

**Related topics**  


[Copy an existing task or project](t_CopyExistingTaskorProject.md)

