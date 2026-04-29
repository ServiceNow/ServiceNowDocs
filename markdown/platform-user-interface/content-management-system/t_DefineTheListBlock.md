---
title: Customize the list block
description: List blocks are content blocks that dynamically generate a list of links to records within the instance. When a user clicks a link in a list block, the associated information is displayed in a detail page determined by its content type.
locale: en-US
release: australia
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Types of content blocks, Content blocks, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Customize the list block

List blocks are content blocks that dynamically generate a list of links to records within the instance. When a user clicks a link in a list block, the associated information is displayed in a detail page determined by its content type.

## Before you begin

Role required: content\_admin or admin

## About this task

Make the list using a simple query on any table or by scripting a more advanced query. Lists are powerful and flexible. Here are some places that allow you to have complete control over the list display.

|Option|Description|
|------|-----------|
|Frames|Frames provide a method to create decorative containers for content blocks and other elements within the site. When frames are used with the **Type** field, the designer has complete control over list placement.|
|List Type|The List Definitions module defines the type of lists available for content pages. On the List Block form, select a list definition in the **Type** field.|
|List Filtering|Provides every field in the referenced table for more granular results.|
|Max Entries|Limits the results from a table to fit the design of the block.|
|Order and Order Direction|Allows sorting by any field in the referenced table, in either ascending or descending order.|

You can also use list blocks to create a list of links to information outside your instance. Create the external links as records on the Content Link \[content\_link\] table, and then follow the steps in this procedure.

## Procedure

1.  Navigate to **All** &gt; **Content Management** &gt; **Lists**.

2.  Click **New**.

3.  Complete form.

<table id="table_xxt_hgh_fq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the list content block. It is used to identify the record in the instance and is not displayed on the content page. Use the **Title** field for that purpose.

</td></tr><tr><td>

Category

</td><td>

Select a category to provide organization for the list content block.

</td></tr><tr><td>

Type

</td><td>

Select a list definition UI macro to format the list of links.For more information, see [Configure list definitions](t_ConfigureListDefinitions.md).

</td></tr><tr><td>

Frame

</td><td>

Select a border style for the list block. For more information, see [Create a frame UI macro](t_CreateANewFrameUIMacro.md).

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to enable generating a list from a script, rather than from a simple filtered query.

</td></tr><tr><td>

Query

</td><td>

Filters the results using a condition builder.

</td></tr><tr><td>

Active

</td><td>

Select this check box to make the block available for use.

</td></tr><tr><td>

Title

</td><td>

Enter the name to display at the top of the list block when it appears in a content page.

</td></tr><tr><td>

Maximum entries

</td><td>

Set the maximum number of entries to display in this list block.

</td></tr><tr><td>

Table

</td><td>

Select a table to query for the list items. The table determines which detail page displays when a user clicks a link in the list block. For more information, see [Configure a content type](t_CreateAContentType.md) **Note:** The list shows only tables and database views that are in the same scope as the list block.

</td></tr><tr><td>

Conditional

</td><td>

Select this check box to enable the use of scripted conditions. If selected, a **Condition** script field appears. Other fields that appear include the **Logged On** and **Omit if empty** check boxes.

</td></tr></tbody>
</table>4.  Click **Submit**.


-   **[Configure list definitions](t_ConfigureListDefinitions.md)**  
List definitions, similar to content management frames, are decorative containers that control the look and feel of lists.

**Parent Topic:**[Types of content blocks](../reference/r_TypesOfContentBlocks.md)

**Related topics**  


[Configure a header block](t_HeaderBlock.md)

[Create a navigation menu block](t_CreateNavigationMenuBlock.md)

[Configure dynamic blocks](t_CreateADynamicBlock.md)

[Configure a static HTML block](t_StaticHTMLBlock.md)

[Configure Flash movie blocks](t_FlashMovieBlock.md)

[Configure content links](t_ConfigureContentLinks.md)

[Configure iFrames](t_IFrame.md)

[Configure a detailed content block](t_DetailedContentBlock.md)

