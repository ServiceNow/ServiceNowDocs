---
title: Configure a detailed content block
description: A detailed content block displays the content of an existing document, such as an incident, knowledge article, or service management request. The document type determines the page that a list of documents points to.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure a detailed content block

A detailed content block displays the content of an existing document, such as an incident, knowledge article, or service management request. The document type determines the page that a list of documents points to.

## Before you begin

Role required: content\_admin or admin

## About this task

The block works with content types in the **Default detail page** field. For more information, see [Configure a content type](t_CreateAContentType.md).

If you plan to use a script to find a document, configure the form to add the **Script** field if it is not displayed.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Configuration** &gt; **Page Detail Settings**.

2.  Click **New**.

3.  Complete the Detailed Content form.

<table id="table_jp3_mdc_gr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Type a unique name for the Detailed Content block.

</td></tr><tr><td>

Category

</td><td>

Select a category to provide organization for the detailed content block. If the block **Type** is **Show the page's current document**, the category displays content from any link of the same type.

</td></tr><tr><td>

Frame

</td><td>

Select a border styling for the detailed content block. For more information, see [Format a frame](t_Frame.md).

</td></tr><tr><td>

Model Document

</td><td>

Select the document to display by default.

</td></tr><tr><td>

Active

</td><td>

Select this check box to make the block available for use.

</td></tr><tr><td>

Type

</td><td>

Select the behavior for the block.-   **Show a Specific Document**: Displays the **Model Document**.
-   **Show the page's current document**: Displays the currently selected document.
-   **Use a script to find a document**: Uses the **Script** field to select a particular document.


</td></tr><tr><td>

Conditional

</td><td>

Select the check box and enter any scripted conditions to be applied. Selecting this check box adds a **Condition** script field and **Logged on** check box to the form.

</td></tr><tr><td>

Script

</td><td>

Enter a script to find an appropriate document if the **Type** is set to **Use a script to find a document**. Set the **Return** to the GlideRecord of the desired document.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block](t_HeaderBlock.md)

[Create a navigation menu block](t_CreateNavigationMenuBlock.md)

[Configure dynamic blocks](t_CreateADynamicBlock.md)

[Customize the list block](t_DefineTheListBlock.md)

[Configure a static HTML block](t_StaticHTMLBlock.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure content links](t_ConfigureContentLinks.md)

[Configure iFrames](t_IFrame.md)

[Content blocks](../concept/c_ContentBlocks.md)

[Configure a content block](t_CreateAContentBlock.md)

