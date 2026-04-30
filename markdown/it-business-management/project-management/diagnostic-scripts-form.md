---
title: Diagnostic Scripts form
description: Learn about the fields of diagnostic scripts form.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Form field information for Project Management, Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Diagnostic Scripts form

Learn about the fields of diagnostic scripts form.

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
</table>**Related topics**  


[Add diagnostic and fix scripts](../task/add-diagnostic-and-fix-script.md)

