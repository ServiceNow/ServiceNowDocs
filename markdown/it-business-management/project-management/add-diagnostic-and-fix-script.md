---
title: Add diagnostic and fix scripts
description: Add diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add diagnostic and fix scripts

Add diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.

## Before you begin

Role required: adt\_admin

## About this task

The results of the filter conditions that you specify in a [diagnostic feature](add-diagnostic-feature.md) are used as an input for the diagnostic script while executing. You can also use the result of one script in subsequent scripts.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Scripts**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_ymh_4kr_wjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the diagnostic script. Use a name that clearly explains the objective of the script. The script name also enables you to identify the correct script while mapping the script to a feature when creating a diagnostic scan.

</td></tr><tr><td>

Description

</td><td>

Details describing the actions of the diagnostic script.

</td></tr><tr><td>

Diagnostic script

</td><td>

The code for the diagnostic script. The following example shows a diagnostic script to identify tasks with an invalid top portfolio. ```
/* 
- Inputs can be accessed from scanContext.input as per, the key specified in feature input table.
	eg.  scanContext.input.projectSysID
- To pass variables from the one script to another script use varSpace in scanContext.
	eg.  scanContext.varSpace.variable1 = '...';
*/
(function(scanContext) {
    try {
        var errorTasks = [];
        var encodedQuery = scanContext.input.projectFilter;
        var now_GR = new GlideRecord("pm_project");
        gr.addEncodedQuery(encodedQuery);
        gr.query();
        while (gr.next()) {
            var entitySysID = gr.getValue("sys_id");
            var projectData = new ProjectData(entitySysID);
            var projectTopTaskValidator = new ProjectTopTaskValidator(projectData);

            if (projectTopTaskValidator.tasksWithInvalidTopPortfolioPresent()) {
                var failedTasks = projectTopTaskValidator.getTasksWithInvalidTopPortfolio();
                if (failedTasks && failedTasks.length) {
                    for (var i = 0; i < failedTasks.length; i++) {
                        errorTasks.push(failedTasks[i].sys_id);
                    }
                }
            }
```

</td></tr></tbody>
</table>4.  Include a script for fixing the corrupt or invalid data identified by the diagnostic script.

    1.  Select the **Has Fix script** check box.

    2.  Click the Edit User Roles icon \(![Edit User Roles icon](../image/edit_user_roles_icon.png)\) and choose the roles that can access the diagnostic script.

    3.  In the **Fix script** section, add the code for the fix script.

5.  Click **Submit**.


