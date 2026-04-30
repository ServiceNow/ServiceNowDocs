---
title: Manage Related Tables and Scripted Elements forms
description: Manage the Related Tables and Scripted Elements components that are required to create a Microsoft PowerPoint template.
locale: en-US
release: zurich
product: Export to PowerPoint for Application Portfolio Management
classification: export-to-powerpoint-for-application-portfolio-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Export to PowerPoint for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Manage Related Tables and Scripted Elements forms

Manage the **Related Tables** and **Scripted Elements** components that are required to create a Microsoft PowerPoint template.

## Before you begin

Role required: sn\_ppt\_export.ppt\_admin

## Procedure

1.  Navigate to **All** &gt; **PowerPoint Management** &gt; **PowerPoint Report Types**.

2.  Select a parent table record, for example, Project report `pm_project`.

<table id="choicetable_wws_lkm_t5b"><tbody><tr><td id="d205655e82">

**To manage Related Tables**

</td><td>

You can add a custom remote table or a child from the parent table.1.  In the **Related Tables** related list, select **New**.

On the Related tables form, fill the fields. For a description of the field values, see [Related Tables form](../reference/related-tables-form.md).

2.  To add a custom remote table:
    1.  [Create a remote table](https://www.servicenow.com/docs/access?context=create-remote-table&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    2.  Select the required remote table from list.
    3.  Select the **Enable custom script** option.
    4.  In the Custom script box, write the code to establish a connection between the remote table and main table.
3.  To select a child table from the main table:
    1.  Select a child table from list.
    2.  Set the **Parent relation column** to the field that links the child table to the parent table.
4.  Select **Submit**.
The selected table and its relation to the parent table is displayed in the Related tables section.

</td></tr><tr><td id="d205655e162">

**To manage Scripted Elements**

</td><td>

1.  In the **Scripted Elements** component, select **New**.
2.  On Scripted Elements form, fill the fields. For a description of the field values, see [Scripted Elements form](../reference/scripted-elements-form.md).
3.  Select **Submit**.


</td></tr></tbody>
</table>3.  To configure a **Script** component, specify the script logic to generate dynamic content in the template.

    Script components allow you to include calculated or dynamically generated content in your PowerPoint template. Use scripts when the built-in Field, Table, or Text component types do not meet your requirements.

    Example: To display a formatted project health status:

    ```
    (function() {
                      var gr = new GlideRecord('pm_project');
                      gr.get(current.getValue('sys_id'));
                      var health = gr.getValue('health');
                      if (health == 'green') return 'On Track';
                      else if (health == 'yellow') return 'At Risk';
                      else return 'Off Track';
                      })()
    ```

    **Note:** Verify the available scripting API and context variables with your ServiceNow administrator. Script components execute server-side and have access to the current record context.

4.  Select **Update**.


**Parent Topic:**[Configuring Export to PowerPoint](../concept/configure-export-to-ppt.md)

