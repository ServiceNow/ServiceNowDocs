---
title: Project template configuration
description: The Project Template Configuration list defines the items that are included in a template.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Applying templates to projects, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project template configuration

The Project Template Configuration list defines the items that are included in a template.

Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Template Config** to display the Project Template Configuration list. Each item in this list has:

-   A defined parent table. The exception is pm\_project, which is the root or top-level object in the template.
-   A link element. A field that links the parent table and the child table.
-   A list of fields to include in the template. The fields defined in this column are the fields that are copied to a project template.

The Project Template Configuration list contains three default template configuration items: project, project task, and project subtask. You can modify these default items or create additional items from this list.

|Item|Definition|Parent|Link Element|
|----|----------|------|------------|
|pm\_project|Project object|None. This object does not have a parent because it is the root level.|None. This object does not have a link element because it is at the root level.|
|pm\_project\_task|Project task object|pm\_project|Parent. Because this task object is one level below the root level, it uses the parent table as a link element.|
|pm\_project\_task|Project subtask object|pm\_project\_task|Parent. Because this subtask object is two levels below the root level, it uses the parent table as a link element.|

Select an item in the Project Template Configuration list to open the project Template Configuration form. For more information, see [Project template configuration form](../reference/project-template-form.md).

![Project Template Configuration form](../image/ProjectTemplateConfigForm.png "Project Template Configuration form")

-   **[Add a project template configuration item](../task/t_AddNewProjTempConfigItem.md)**  
Add a project template configuration item to include in a template.
-   **[Modify a project template configuration item](../task/t_ModifAProjectTempConfigItem.md)**  
Modify a project template configuration item included in a template.

**Parent Topic:**[Applying templates to projects](c_ProjectTemplates.md)

**Related topics**  


[Create a project template](../task/t_ViewAProjectTemplateForm.md)

[Add an attachment to a project template](../task/t_AddAnAttachmentToAProjectTemplate.md)

[Apply a template on the Project form](../task/t_ApplyATemplateFromTheProjectForm.md)

[Apply template to an existing project](../task/apply-multiple-templates-prj.md)

[Apply template to a blank project in project workspace](../task/t_ApplyTempProjWorkbench.md)

