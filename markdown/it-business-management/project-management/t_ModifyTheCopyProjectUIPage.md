---
title: Change default values of copied project
description: Reset or change the default values for copied fields in the new copied partial or complete project.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Copy a project, Starting a project, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Change default values of copied project

Reset or change the default values for copied fields in the new copied partial or complete project.

## Before you begin

Role required: admin

## About this task

Child tasks are defined with the same relationships, each lasting for the same duration as the original tasks. All project tasks are set to **Pending**. Actual duration and the actual start and end dates are reset to null values. The state is set to **New** and percent complete is set to 0. Administrators can override the Script Include CopyProjectFieldOverride to determine which fields are reset or to change the default values.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Script Include**.

2.  Open the CopyProjectFieldOverride record.

3.  Add the method to override the method defined in the CopyProjectFieldOverrideSNC script for resetting or defaulting the values.

    For example, to copy partial project:

    ```
         /* getResetFieldsForCopyPartialProject method returns the array containing the list of names of fields that need to be erased from the copied project tasks
                        * getDefaultObjectForCopyPartialProject method returns the object containing the key, value pairs of field names and values that need to be set on the copied tasks
                        */var CopyProjectFieldOverride = Class.create();
                        CopyProjectFieldOverride.prototype = Object.extendsObject(CopyProjectFieldOverrideSNC, {
                        getResetFieldsForCopyPartialProject: function() {
                        return ['work_start', ‘work_end’, ‘work_duration’];
                        },
                        getDefaultObjForCopyPartialProject: function() {
                        return {'state': -5,‘percent_complete: 0’};
                    },
                    type: 'CopyProjectFieldOverride'
                    });
    
    ```

    To copy complete project:

    ```
    /* getResetFieldsForCopyProject method returns the array containing the list of names of fields that need to be erased from the copied project tasks
                * getDefaultObjectForCopyProject method returns the object containing the key, value pairs of field names and values that need to be set on the copied tasks
                */var CopyProjectFieldOverride = Class.create();
                CopyProjectFieldOverride.prototype = Object.extendsObject(CopyProjectFieldOverrideSNC, {
                getResetFieldsForCopyProject: function() {
                        return ['work_start' ,"work_end","work_duration"];},
                        getDefaultObjForCopyProject: function()
                        {
                            return {'state': -5, ‘percent_complete: 0’};
                         },
                        type: 'CopyProjectFieldOverride'
                      });
    
    ```

4.  Select **Update**.


**Parent Topic:**[Copy a project](t_CopyAProject.md)

**Related topics**  


[Copy a project](t_CopyAProject.md)

