---
title: Create an article template and use it to create a knowledge article
description: Create new article templates in addition to the pre-defined templates. Add new fields based on how you want to customize and display your content.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure knowledge article templates, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an article template and use it to create a knowledge article

Create new article templates in addition to the pre-defined templates. Add new fields based on how you want to customize and display your content.

## Before you begin

You must activate following plugins:

-   Knowledge Management Advanced \(com.snc.knowledge\_advanced\)
-   Knowledge Management Advanced Installer \(com.snc.knowledge\_advanced.installer\)

Role required: admin, knowledge\_admin or admin, personalize\_form

## About this task

For each new article template, a child table of the Knowledge \[kb\_knowledge\] table is created. When you add a new field to the template, a new column is added to that table created for the template.

## Procedure

1.  Navigate to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Article Templates**, and click **New**.

2.  On the Article Template form, fill in fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the article template. The name can contain only lowercase, alphanumeric ASCII characters and underscores \(\_\).|
    |Description|Description for the article template.|

    **Note:** The **Active** check box is selected by default making the template available for use.

3.  Right-click the form header and click **Save**.

4.  In the Article Templates Field related list, add fields to the template.

    1.  Click **New**.

    2.  On the Article Template Field form, fill in the fields.

<table id="table_oqx_cpb_zbb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field Name

</td><td>

Title to display on the template form.

</td></tr><tr><td>

Field Type

</td><td>

Available field types:-   HTML
-   String
-   Integer
-   Date
-   Date and time


</td></tr><tr><td>

Order

</td><td>

Position of the field in the article page view and the article edit view.

</td></tr><tr><td>

Article Template

</td><td>

\(Read-only\) Name of the article template associated with this field.

</td></tr><tr><td>

Template Table

</td><td>

\(Read-only\) Name of the table for this template.

</td></tr><tr><td>

Template Field

</td><td>

\(Read-only\) Name of the template column associated with this field.

</td></tr><tr><td>

Mandatory

</td><td>

Option to make this field as mandatory. When selected, this field is required to be filled.

</td></tr><tr><td>

Expand/Collapse

</td><td>

Defines whether the template field displays as collapsed or expanded by default.

</td></tr><tr><td>

Active

</td><td>

Option to display the field on the template.

</td></tr><tr><td>

Heading style

</td><td>

CSS formats applied to the template header. For example, to display the background of the template header in red, with a 24-px font size, Arial font family, and white text color, enter the following code: `background-color:red; font-size:24px; font-family:Arial; color:white;`

</td></tr><tr><td>

Field style

</td><td>

CSS formats applied to the template fields. Any CSS format applied at the field level is automatically applied to the header if not already specified in the **Heading style** field. For example, to display the 300px page width, 25px solid green border, 25px padding, and 25px page margin, enter the following code: `width:300px; border:25px solid green; padding:25px; margin:25px;`

</td></tr><tr><td>

Preview text

</td><td>

Preview text displayed on the article template selector. Empty value will display random text.

</td></tr></tbody>
</table>    3.  Click **Submit**.

    The field is added to the template.

5.  In the **SEO Description Tag** field, search for and add article template field name.

    The content in this field is used as meta description tags to search for articles created using this article template.

6.  Configure the Knowledge form to display the fields that you added to the template.

    1.  Navigate to **Knowledge** &gt; **Articles** &gt; **Create New**.

    2.  Select a knowledge base, and then the newly added article template.

    3.  Right-click the header and select **Configure** &gt; **Form Layout**.

    4.  Select and move the fields you added to the article template from the **Available** column to the **Selected** column.

    5.  Click the up or down icon to arrange the fields in the order in which you want them to appear in the Knowledge form.

    6.  Click **Save**.

    **Note:** Authors who started a session before a template was created or activated will see the newly added template upon their next login.


## What to do next

If you want to search for duplicate articles when creating an article from a new template, you must configure the article template table for contextual search. On the Table Configuration form, the **Search context** field must be set to **Knowledge ML Search**. For more information, see Configure table for a contextual search.

**Parent Topic:**[Configure knowledge article templates](../concept/configure-knowledge-article-templates.md)

