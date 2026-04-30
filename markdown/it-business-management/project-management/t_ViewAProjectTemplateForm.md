---
title: Create a project template
description: You can create a template from an existing template or a project.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project templates, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create a project template

You can create a template from an existing template or a project.

## Before you begin

Role required: it\_project\_manager

## About this task

When you create a template from a project, all the project attachments and checklists are copied to the template. You can add or remove attachments from the template using the Project Template form. A project template created from an off-schedule project honors the off-schedule tasks.

## Procedure

1.  Create a template.

<table id="choicetable_whk_swd_tw"><thead><tr><th align="left" id="d291111e68">

Option

</th><th align="left" id="d291111e71">

Steps

</th></tr></thead><tbody><tr><td id="d291111e77">

**From an existing template**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **Templates**.
2.  Open the desired project template.
3.  Click the **Copy Template** related link at the bottom of the form.
4.  The Copy Template dialog box opens. The **Template** field is auto-filled with the current template name.


</td></tr><tr><td id="d291111e119">

**From a project**

</td><td>

1.  Navigate to **Project** &gt; **Projects** &gt; **All**.
2.  Open the desired project.
3.  Click the **Save as New Template** related link at the bottom of the form.
4.  The Create Template dialog box opens.


</td></tr></tbody>
</table>2.  Fill in the following fields:

    -   **Template name**: enter a unique name for the new template.
    -   **Description**: enter a brief description of the new template.
3.  Click **OK**.

    The project template form opens for the newly created template.

4.  Make any desired changes to the fields on the project template form.

    The top section of the Project Template form includes basic template information, such as the template name and description. The middle section of the project template form defines the specific data included in the template. The information in this section is built from fields on the project \[pm\_project\] table that the user selects and the values for those fields that the user defines.

<table id="table_yfn_stt_vw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the project template.

</td></tr><tr><td>

Table

</td><td>

Display only. Templates are based on the Project table.

</td></tr><tr><td>

Description

</td><td>

A brief description of the project template.

</td></tr><tr><td>

Template

</td><td>

Includes columns of fields and field values to be included in the template. Click a field in the left column and select the desired field name, then click the field in the right column to enter the field value. If additional information for the field is required, a field appears in the third column. For example, to identify the currency in a money field.-   Click the **X** to the right of a field to remove that field from the template.
-   Use the blank field at the bottom of the list to add new fields.


</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Create Project|Creates a project from this project template.|
    |Copy Template|Creates a copy of this project template.|

    |Field|Description|
    |-----|-----------|
    |Project Template Tasks|The project template task list.|
    |Attachments|The files attached to the template.|

5.  Click **Update**.


**Parent Topic:**[Project templates](../concept/c_ProjectTemplates.md)

**Related topics**  


[Add an attachment to a project template](t_AddAnAttachmentToAProjectTemplate.md)

[Apply a template on the Project form](t_ApplyATemplateFromTheProjectForm.md)

[Apply template to an existing project](apply-multiple-templates-prj.md)

[Apply template to a blank project in project workspace](t_ApplyTempProjWorkbench.md)

[Project template configuration](../concept/c_ProjectTemplateConfiguration.md)

