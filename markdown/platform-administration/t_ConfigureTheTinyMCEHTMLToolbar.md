---
title: Configure the HTML toolbar
description: Configure which buttons are available on the HTML toolbar.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure a field editor for the HTML field, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the HTML toolbar

Configure which buttons are available on the HTML toolbar.

## Before you begin

Role required: admin

## Procedure

1.  Update the toolbar options for your preferred HTML field editor.

<table id="choicetable_twl_kgd_rxb"><tbody><tr><td id="d118680e65">

**htmlArea toolbar**

</td><td>

1.  Navigate to the System properties \[sys\_properties\] table by entering `sys_properties.list` in the application navigator.
2.  In the **Name** column, search for `glide.ui.html.toolbar`.
3.  Select the **glide.ui.html.toolbar** property.


</td></tr><tr><td id="d118680e98">

**TinyMCE**

</td><td>

1.  Navigate to the System properties \[sys\_properties\] table by entering `sys_properties.list` in the application navigator.
2.  In the **Name** column, search for `glide.ui.html.editor.toolbar`.
3.  Select the **glide.ui.html.editor.toolbar** property.


</td></tr></tbody>
</table>2.  In the **Value** field, enter or remove buttons for each toolbar as a comma-separated list without spaces.

    For the TinyMCE toolbar, all the toolbar buttons mentioned in the TinyMCE button options table are available in the **glide.ui.html.editor.toolbar.valid\_buttons** sys\_property. You can choose from the list found there and add it to the System properties \[sys\_properties\] **glide.ui.html.editor.toolbar**. Use a vertical bar \("\|"\) to add a section separator.

    |Button purpose|Accepted button names|
    |--------------|---------------------|
    |Formatting|newdocument, bold, italic, underline, aligncenter,alignjustify alignleft, alignright, indent, outdent, numlist, bullist, blocks, fontfamily, fontsize, forecolor, removeformat, backcolor, blockquote, strikethrough, subscript, superscript, pagebreak, nonbreaking, ltr rtl|
    |Table functions|table, tableofcontents|
    |Editing|copy, cut, paste, pastetext, undo, redo, searchreplace|
    |Extended functions|link, unlink, charmap, code, codesample, hr, image, media, preview, print, visualblocks, visualchars, anchor, emoticons, insertdatetime, fullscreen \(not supported by Internet Explorer\)|

    For the htmlArea toolbar, use the buttons listed in the htmlArea button options table. Use **separator** to add a section separator.

    |Button purpose|Accepted button names|
    |--------------|---------------------|
    |Formatting|formatblock, fontname, fontsize, bold, italic, underline, justifyleft, justifycenter, justifyright, justifyfull, insertorderedlist, insertunorderedlist, outdent, indent, forecolor, hilitecolor|
    |Editing|copy, paste, undo|
    |Extended functions|createlink, inserthorizontalrule, insertimage, insertvideo, inserttable, htmlmode|

3.  Select **Update**.


## What to do next

See [Change the TinyMCE default toolbar](../../workspace/concept/tinymce.md#) for more detailed information.

-   **[Formatting functions in HTML field editors](../../../use/using-forms/reference/r_Formatting.md)**  
The formatting table displays how to control the way text appears.
-   **[Table functions in HTML field editor](../../../use/using-forms/reference/r_TinyMCEVersion4Editor.md)**  
TinyMCE version 6.8.2 uses menus and menu selections to create and edit tables.
-   **[Editing functions in HTML field editor](../../../use/using-forms/reference/r_EditingFunctions.md)**  
Several editing functions are built into TinyMCE.
-   **[Extended functions in HTML field editor](../../../use/using-forms/reference/r_ExtendedFunctions.md)**  
The extended functions available for working with HTML content.

**Parent Topic:**[Configure a field editor for the HTML field](t_ConfigTinyMCEHTMLFieldEditor.md)

**Related topics**  


[Configuring system properties for TinyMCE HTML editor](configuring-system-properties-for-tinymce-html-editor.md)

[Configuring plugins for the TinyMCE HTML editor](configuring-plugins-for-TinyMCE-HTML-editor.md#)

[Configuring the TinyMCE toolbar via Dictionary attributes](../../workspace/concept/tinymce.md#)

