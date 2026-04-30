---
title: Configuring plugins for the TinyMCE HTML editor
description: The TinyMCE HTML editor is a powerful, flexible, and customizable rich text editor. You can configure and extend the editor by using plugins.Configure the TinyMCE plugins in our workspaces.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure a field editor for the HTML field, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring plugins for the TinyMCE HTML editor

The TinyMCE HTML editor is a powerful, flexible, and customizable rich text editor. You can configure and extend the editor by using plugins.

<table id="table_jv1_rrv_lbc"><thead><tr><th>

Plugin name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

a11ychecker

</td><td>

Allows you to check the HTML in the editor for various WCAG &amp; Section 508 accessibility problems. It has an auto-repair feature that lets the user fix identified problems.

</td></tr><tr><td>

accordion

</td><td>

Enables the creation of sections in a document that can be expanded or collapsed to show or hide additional content.

</td></tr><tr><td>

advlist

</td><td>

Extends the core bullist and numlist toolbar controls by adding additional CSS list-style-type styled number formats and bullet types to the controls.

</td></tr><tr><td>

align\_listitems

</td><td>

Confirms that bullets and numbers are aligned along with the content.

</td></tr><tr><td>

anchor

</td><td>

Adds an anchor/bookmark button to the toolbar that inserts an anchor at the editor’s cursor insertion point. It also adds the menu item anchor under the Insert menu.

</td></tr><tr><td>

autolink

</td><td>

Creates hyperlinks automatically when you enter a valid, complete URL. For example, `www.example.com` is converted to `http://www.example.com`.

</td></tr><tr><td>

autoresize

</td><td>

Resizes the editor to the content inside it automatically. It's typically used to help prevent the editor from expanding infinitely as you enter text into the editable area.

</td></tr><tr><td>

charmap

</td><td>

Adds a dialog to the editor with a map of special unicode characters, which can't be added directly from the keyboard.

</td></tr><tr><td>

codemirror

</td><td>

Provides a more advanced code editor than the default text area.

</td></tr><tr><td>

codesample

</td><td>

Insert and embed syntax color highlighted code snippets into the editable area. It also adds a button to the toolbar that opens a dialog box to accept raw code input.

</td></tr><tr><td>

directionality

</td><td>

Adds directionality controls to the toolbar, enabling TinyMCE to better handle languages written from right to left. It also adds a toolbar button for each of its values, ltr for left-to-right text and rtl for right-to-left text.

</td></tr><tr><td>

emoticons

</td><td>

Adds a dialog to the editor that lets you insert emoji into the TinyMCE editable area.

</td></tr><tr><td>

fullscreen

</td><td>

Adds full screen editing capabilities to TinyMCE. When you press the toolbar button, the editable area fills the viewport of the browser.

</td></tr><tr><td>

image

</td><td>

Enables you to insert an image into the TinyMCE editable area.

</td></tr><tr><td>

insertdatetime

</td><td>

Provides a toolbar control and menu item that lets you insert the current date and time into the editable area at the cursor insertion point.

</td></tr><tr><td>

link

</td><td>

Enables you to link external resources, such as website URLs, to selected text in their document.

</td></tr><tr><td>

lists

</td><td>

Enables you to add numbered and bulleted lists to TinyMCE. To enable advanced lists, such as alpha numbered lists and square bullets, you should also enable the Advanced List \(advlist\) plugin.

</td></tr><tr><td>

media

</td><td>

Lets you add HTML5 video and audio elements to the editable area.

</td></tr><tr><td>

nonbreaking

</td><td>

Adds a button for inserting nonbreaking space entities such as &amp;nbsp; at the cursor insert point. It also adds a menu item Nonbreaking space under the Insert menu drop-down list and a toolbar button.

</td></tr><tr><td>

pagebreak

</td><td>

Adds page break support and enables you to insert page breaks in the editable area. This ability is useful where a CMS uses a special separator to break content into pages.

</td></tr><tr><td>

preview

</td><td>

Adds a preview button to the toolbar that opens a dialog box showing the current content in a preview mode.

</td></tr><tr><td>

readonlynoborder

</td><td>

Enables a read-only mode for HTML field types.

</td></tr><tr><td>

searchreplace

</td><td>

Adds search and replace dialogs to TinyMCE.

</td></tr><tr><td>

table

</td><td>

Adds table management functionality to TinyMCE, including dialogs, context menus, context toolbars, menu items, and toolbar buttons.

</td></tr><tr><td>

tableofcontents

</td><td>

Generates a basic table of contents \(ToC\) and inserts it into the editor at the cursor insert point. ToC entries are generated from header elements in the content.

</td></tr><tr><td>

visualblocks

</td><td>

Enables you to see block-level elements in the editable area.

</td></tr><tr><td>

visualchars

</td><td>

Adds the ability to see invisible characters like &amp;nbsp; in the editable area.

</td></tr><tr><td>

wordcount

</td><td>

Adds the functionality for counting words to the TinyMCE editor.

 **Note:** This plugin is no longer supported in workspaces.

</td></tr><tr><td>

powerpaste

</td><td>

Cleans up content from Microsoft Word, Microsoft Excel, Google Docs, and HTML sources automatically to create clean content that matches the look and feel of the site.

</td></tr></tbody>
</table>**Note:** Adding a custom plugin to the valid plugins can cause unexpected results.

## Change the TinyMCE HTML editor plugins

Configure the TinyMCE plugins in our workspaces.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Update the plugin configuration for HTML field \(TinyMCE v6.8.3\) \(glide.ui.html.editor.enabled\_plugins\) property to configure plugins.

    Use a vertical bar \("\|"\) to add a section separator.

<table id="table_crx_3rm_dcc"><thead><tr><th>

Type

</th><th>

Plugins

</th></tr></thead><tbody><tr><td>

Default plugins

</td><td>

-   accordion
-   advlist
-   align\_listitems
-   anchor
-   autolink
-   autoresize
-   charmap
-   codemirror
-   codesample
-   directionality
-   emoticons
-   fullscreen
-   image
-   insertdatetime
-   link
-   lists
-   media
-   nonbreaking
-   pagebreak
-   preview
-   readonlynoborder
-   searchreplace
-   table
-   tableofcontents
-   visualblocks
-   visualchars
-   wordcount


</td></tr><tr><td>

Enabled plugins

</td><td>

-   a11ychecker
-   accordion
-   advlist
-   align\_listitems
-   anchor
-   autolink
-   charmap
-   codemirror
-   codesample
-   directionality
-   emoticons
-   fullscreen
-   image
-   insertdatetime
-   link
-   lists
-   media
-   nonbreaking
-   pagebreak
-   preview
-   readonlynoborder
-   searchreplace
-   table
-   tableofcontents
-   visualblocks
-   visualchars
-   wordcount


</td></tr></tbody>
</table>3.  Make changes \(add/remove\) in the enabled plugins property.

4.  Select save.

    If there's a custom plugin added to enabled plugins its not recommended unless critical.


