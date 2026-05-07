---
title: Configure the HTML toolbar
description: Configure which buttons are available on the HTML toolbar.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a field editor for the HTML field, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the HTML toolbar

Configure which buttons are available on the HTML toolbar.

## Before you begin

Role required: admin

## Procedure

1.  Update the toolbar options for your preferred HTML field editor.

<table id="choicetable_twl_kgd_rxb"><tbody><tr><td id="d144008e57">

**htmlArea toolbar**

</td><td>

1.  Navigate to the System properties \[sys\_properties\] table by entering `sys_properties.list` in the application navigator.
2.  In the **Name** column, search for `glide.ui.html.toolbar`.
3.  Select the **glide.ui.html.toolbar** property.


</td></tr><tr><td id="d144008e90">

**TinyMCE**

</td><td>

1.  Navigate to the System properties \[sys\_properties\] table by entering `sys_properties.list` in the application navigator.
2.  In the **Name** column, search for `glide.ui.html.editor.toolbar`.
3.  Select the **glide.ui.html.editor.toolbar** property.


</td></tr></tbody>
</table>2.  In the **Value** field, enter or remove buttons for each toolbar as a comma-separated list without spaces.

    For the TinyMCE toolbar, all the toolbar buttons mentioned in the TinyMCE button options table are available in the **glide.ui.html.editor.toolbar.valid\_buttons**. You can choose from the list found there and add it to the System properties \[sys\_properties\] **glide.ui.html.editor.toolbar**. Use a vertical bar \("\|"\) to add a section separator.

<table id="simpletable_exc_mlp_3r"><thead><tr><th>

Button purpose

</th><th>

Accepted button names

</th></tr></thead><tbody><tr><td>

Formatting

</td><td>

-   aligncenter
-   alignjustify
-   alignleft
-   alignright
-   backcolor
-   blocks
-   blockquote
-   bold
-   bullist
-   editimage
-   fontfamily
-   fontsize
-   formatpainter
-   forecolor
-   help
-   indent
-   italic
-   ltr
-   newdocument
-   nonbreaking
-   numlist
-   outdent
-   pagebreak
-   removeformat
-   rtl
-   strikthrough
-   subscript
-   superscript
-   underline


</td></tr><tr><td>

Table functions

</td><td>

-   table
-   tableofcontents


</td></tr><tr><td>

Editing

</td><td>

-   copy
-   cut
-   paste
-   pastetext
-   redo
-   searchreplace
-   undo


</td></tr><tr><td>

Extended functions

</td><td>

-   a11ycheck
-   anchor
-   charmap
-   code
-   codesample
-   emoticons
-   fullscreen \(not supported by Internet Explorer\)
-   help
-   hr
-   editimage
-   insertdatetime
-   link
-   media
-   preview
-   print
-   unlink
-   visualblocks
-   visualchars


</td></tr></tbody>
</table>    For the htmlArea toolbar, use the buttons listed in the htmlArea button options table. Use **separator** to add a section separator.

<table id="htmlArea"><thead><tr><th>

Button purpose

</th><th>

Accepted button names

</th></tr></thead><tbody><tr><td>

Formatting

</td><td>

-   bold
-   editimage
-   fontname
-   fontsize
-   forecolor
-   formatblock
-   formatpainter
-   help
-   hilitecolor
-   indent
-   insertorderedlist
-   insertunorderedlist
-   italic
-   justifycenter
-   justifyfull
-   justifyleft
-   justifyright
-   outdent
-   underline


</td></tr><tr><td>

Editing

</td><td>

-   copy
-   paste
-   undo


</td></tr><tr><td>

Extended functions

</td><td>

-   a11ycheck
-   createlink
-   editimage
-   help
-   htmlmode
-   inserthorizontalrule
-   insertimage
-   inserttable
-   insertvideo


</td></tr></tbody>
</table>3.  Select **Update**.


## What to do next

See [Change the TinyMCE default toolbar](../../workspace/concept/tinymce.md#) for more detailed information.

