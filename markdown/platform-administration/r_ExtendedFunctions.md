---
title: Extended functions in HTML field editor
description: The extended functions available for working with HTML content.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure the HTML toolbar, Configure a field editor for the HTML field, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Extended functions in HTML field editor

The extended functions available for working with HTML content.

<table id="table_pt3_kjg_vq"><thead><tr><th>

Name

</th><th>

HTML Icon

</th><th>

TinyMCE v6.8.3 Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accordion\*

</td><td>

 

</td><td>

![TinyMCE v6.8.3 Accordion](../image/TinyMCEV6-accordion_icon.png)

</td><td>

Executes the `InsertAccordion` command, adding an Accordion element at the current location.

</td></tr><tr><td>

Add character map\*

</td><td>

![Spec Char html](../image/SpecCharHTML.png)

</td><td>

![TinyMCE v6.8.3 Add character map](../image/TinyMCEV6-add-character-map_icon.png)

</td><td>

Inserts a special character at the current cursor location. Select the button to view a list of available characters. Point to a character to view the name and HTML code. Select a character to insert it.

</td></tr><tr><td>

Anchor\*

</td><td>

 

</td><td>

![TinyMCE v6.8.3 Anchor](../image/TinyMCEv6-anchor_icon.png)

</td><td>

Inserts an anchor into the editor.

</td></tr><tr><td>

Cleanup Messy Code

</td><td>

![Cleanup html](../image/CleanupHTML.png)

</td><td>

 

</td><td>

Fixes standard HTML errors for the selected text, such as invalid tags. Selecting this button might change the layout of existing content. If you don’t like the results, you can select **Undo** to revert this action.

</td></tr><tr><td>

Edit HTML Source/Code

</td><td>

![Html editor button](../image/HTMLEditorButton.png)

</td><td>

![TinyMCE v6.8.3 Code](../image/TinyMCEV6-code_icon.png)

</td><td>

Opens HTML source code in a separate window. See [Editing in HTML Source Mode](../concept/c_UseHTMLFields.md).

</td></tr><tr><td>

Emoticons\*

</td><td>

 

</td><td>

![TinyMCE v6.8.3 Emoticons](../image/TinyMCEV6-emoticons_icon.png)

</td><td>

Opens the Emojis dialog.

</td></tr><tr><td>

Insert date/time\*

</td><td>

 

</td><td>

![TinyMCE v6.8.3 Insert date/time](../image/TinyMCEV6-insertdatetime_icon.png)

</td><td>

Inserts the current date and time into the editor.

</td></tr><tr><td>

Insert/Edit Embedded Media

</td><td>

![Media html](../image/MediaHTML.png)

</td><td>

![TinyMCE v6.8.3 Embed media](../image/TinyMCEV6-embed_icon.png)

</td><td>

Embeds a video from the video library or an attachment. You can also add videos to the video library with this feature. To learn more, see [Embedding Video in HTML Fields](../task/t_EmbeddingVideoInHTMLFields.md).

</td></tr><tr><td>

Insert/Edit Image

</td><td>

![Image html](../image/ImageHTML.png)

</td><td>

![TinyMCE v6.8.3 Image](../image/TinyMCEV6-image_icon.png)

</td><td>

Inserts an image from the image library or an attachment. You can also add images to the image library with this feature. To learn more, see [Embedding Images in HTML Fields](../task/t_EmbeddingImagesInHTMLFields.md).

</td></tr><tr><td>

Insert/Edit Link

</td><td>

![Link html](../image/LinkHTML.png)

</td><td>

![TinyMCE v6.8.3 Link](../image/TinyMCEV6-link_icon.png)

</td><td>

Configures a link for the selected text. You can define the link URL, title \(additional information that appears in the tooltip\), and the target \(same window or new window or tab\).

 [Code reference](http://www.w3schools.com/tags/tag_a.asp): `<a>`

</td></tr><tr><td>

Insert Horizontal Line

</td><td>

![Hr html](../image/HrHTML.png)

</td><td>

 

</td><td>

Inserts a horizontal line at the current location.

</td></tr><tr><td>

Preview\*

</td><td>

![Preview html](../image/PreviewHTML.png)

</td><td>

 

</td><td>

Opens a preview of the HTML field in a separate window without saving changes.

</td></tr><tr><td>

Print\*

</td><td>

 

</td><td>

![TinyMCE v6.8.3 Print](../image/TinyMCEV6-print_icon.png)

</td><td>

Prints the current document.

</td></tr><tr><td>

Remove link\*

</td><td>

![Unlink html](../image/UnlinkHTML.png)

</td><td>

![TinyMCE v6.8.3 Unlink](../image/TinyMCEV6-unlink_icon.png)

</td><td>

Removes the current hyperlink.

</td></tr><tr><td>

Spell Checker

</td><td>

![Spell html](../image/SpellHTML.png)

</td><td>

 

</td><td>

Checks the spelling of text in the HTML field.**Note:** Spell Checker is only available in the htmlArea editor.

</td></tr><tr><td>

Toggle Full Screen Mode\*

</td><td>

![Full screen html](../image/FullScreenHTML.png)

</td><td>

![TinyMCE v6.8.3 Full screen](../image/TinyMCEV6-fullscreen_icon.png)

</td><td>

Expands the HTML field to use the full form view. Select the button again to return to standard form view. **Note:** This feature is available only for the htmlArea editor and isn’t available for Internet Explorer.

</td></tr><tr><td>

Visual blocks\*

</td><td>

 

</td><td>

![TinyMCE v6.8.3 Visual blocks](../image/TinyMCEV6-blocks_icon.png)

</td><td>

Toggles block visibility on or off.

</td></tr><tr><td>

Visual chars\*

</td><td>

![Toggle guides html](../image/ToggleGuidesHTML.png)

</td><td>

 

</td><td>

Shows or hides invisible elements in the article, such as collapsed table borders.

</td></tr></tbody>
</table>**Note:** \*These options aren’t available with htmlArea.

-   **[Embed images in the HTML editor](../task/t_EmbeddingImagesInHTMLFields.md)**  
You can use the HTML field image picker to embed images into HTML fields, and to add images to the image library.
-   **[Link a website in HTML editor](../task/t_LinkingToAWebsiteInHTMLFields.md)**  
You can insert a link to a website in an HTML field.
-   **[Embed videos in the HTML editor](../task/t_EmbeddingVideoInHTMLFields.md)**  
You can insert videos into HTML fields. You can also add videos to the video library using the HTML Insert/Modify Video form.
-   **[Define video file types for HTML fields](../task/t_DefineVideoTypesForHTMLFields.md)**  
You can define the types of video files that can be added to HTML fields.
-   **[Disable user access to the image library for HTML area](../../../administer/form-administration/task/t_ModifyImageUploads.md)**  
By default, users can use and upload images to the image library from an HTML field. You can disable access to the image library from HTML fields. This is only applicable to HTML area and not TinyMCE.
-   **[Configure accordion in TinyMCE HTML editor](../../../administer/form-administration/task/add-accordion-in-tinymce-html-editor.md)**  
You can enable the accordion on the TinyMCE HTML editor in both CoreUI and workspaces. When enabled, the accordion button appears on the HTML editor and can be used to expand/collapse content.

**Parent Topic:**[Configure the HTML toolbar](../../../administer/form-administration/task/t_ConfigureTheTinyMCEHTMLToolbar.md)

