---
title: Configuring the TinyMCE toolbar via Dictionary attributes
description: You can configure the TinyMCE HTML editor for a specific table by configuring the dictionary attributes.Set the toolbar items in your system properties to enable or disable throughout Workspace.Set the attributes in the TinyMCE dictionary to determine which TinyMCE attributes show in a specific table.Set the attributes in the TinyMCE dictionary to enable or disable plugins in a specific HTML field.Change the default height of a specific HTML field to expand the size of a journal field.Change the default font size of a specific HTML field to use a standard font size across forms.You can set a dictionary attribute on a TinyMCE field to allow the use of deprecated HTML tags, such as &lt;b&gt; and &lt;i&gt;. By default, TinyMCE uses the &lt;strong&gt; and &lt;em&gt; tags for bold and italic formatting.You can set a dictionary attribute on a TinyMCE field to allow the use of JavaScript in a URL.You can enable the menu bar on the TinyMCE HTML editor in both CoreUI and workspaces. When enabled, the menu bar appears on the top of the HTML editor which can be used to create, edit and format content. By default, the menu bar is inactive. You can enable it for a specific table via dictionary attribute configuration.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Configure a field editor for the HTML field, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring the TinyMCE toolbar via Dictionary attributes

You can configure the TinyMCE HTML editor for a specific table by configuring the dictionary attributes.

For information on configuring the toolbar, see [Change the TinyMCE default toolbar](tinymce.md#). For information on configuring specific plugins, see [Change TinyMCE plugins for a specific table](tinymce.md#). For information on configuring the default height of an HTML field, see [Change the default height of an HTML field](tinymce.md#). For information on configuring the default font size in an HTML field, see [Change the default font size of an HTML field](tinymce.md#). For information on configuring the menu bar on the TinyMCE HTML editor, see [Configure the menu bar on the TinyMCE HTML editor](tinymce.md#).

## Change the TinyMCE default toolbar

Set the toolbar items in your system properties to enable or disable throughout Workspace.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Update the **Configures the editing toolbar for HTML fields\(TinyMCE v6.8.2\)** \(glide.ui.html.editor.toolbar\) property to add or remove buttons for the toolbar.

    **Note:** Use a vertical bar \("\|"\) to add a section separator.

    |Type|Buttons|
    |----|-------|
    |Default buttons|**bold italic underline undo redo \| fontfamily fontsize table \| forecolor backcolor link unlink \| image media code \| alignleft aligncenter alignright \| bullist numlist fullscreen**|
    |Valid buttons|**newdocument, bold, italic, underline, strikethrough, justifyleft, justifycenter, justifyright, justifyfull, blocks, fontfamily, fontsize, tablecontrols, cut, copy, paste, pastetext, pasteword, search, replace, bullist, numlist, outdent, indent, blockquote, undo, redo, link, unlink, image, cleanup, code, forecolor, backcolor, removeformat, hr, visualaid, sub, sup, charmap, media, preview, fullscreen, accordion**|

3.  Select **Save**.


## Change the TinyMCE toolbar for a specific table

Set the attributes in the TinyMCE dictionary to determine which TinyMCE attributes show in a specific table.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to a record with an HTML-type field that you want to change.

    For example, select an incident, problem, or knowledge record.

2.  Right-click the field label \(for example, Article body\) and select **Configure Dictionary**.

3.  In the Related Links section, select **Advanced View**.

4.  In the **Attributes** field, input `editor.toolbar=` followed by the desired toolbar buttons.

    For example, `editor.toolbar=blocks|bold italic underline strikethrough blockquote subscript superscript removeformat| bullist numlist outdent indent|undo redo|table hr|link unlink|image media code|visualblocks preview fullscreen`.

    **Note:**

    -   Include all the toolbar items that you want displayed, not just the toolbar items you want to add.
    -   The configurations made to a field's Attribute field on the associated Dictionary record overrides the value of the System Property glide.ui.html.editor.toolbar.
    -   Multiple attributes, such as height, toolbar buttons, and toolbar plugins, can be combined within the Attributes field. For example, `editor.height=300,editor.plugins=table colorpicker textcolor link image media codemirror lists advlist fullscreen charmap directionality emoticons hr insertdatetime nonbreaking pagebreak print searchreplace wordcount anchor codesample visualblocks visualchars compat3x autolink align_listitems,editor.toolbar= fontfamily fontsize | bold italic underline strikethrough forecolor backcolor pastetext removeformat | blocks searchreplace undo redo | bullist numlist outdent indent alignleft aligncenter alignright | tableofcontents table link unlink image media codesample | code fullscreen`.
5.  Select **Update**.


## Change TinyMCE plugins for a specific table

Set the attributes in the TinyMCE dictionary to enable or disable plugins in a specific HTML field.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to a record with an HTML-type field that you want to change.

    For example, select an incident, problem, or knowledge record.

2.  Right-click the field label \(for example, Article body\) and select **Configure Dictionary**.

3.  In the Related Links section, select **Advanced View**.

4.  In the **Attributes** field, input `editor.plugins=` followed by the desired plugins, separated with a space.

    For example, `editor.plugins=table colorpicker textcolor link image media codemirror lists advlist fullscreen charmap directionality emoticons hr insertdatetime nonbreaking pagebreak print searchreplace wordcount anchor tableofcontents codesample visualblocks visualchars compat3x autolink align_listitems`.

    **Note:**

    -   Include all the toolbar items that you want displayed, not just the toolbar items you want to add.
    -   The configurations made to a field's Attribute field on the associated Dictionary record overrides the value of the System Property glide.ui.html.editor.toolbar.
    -   Allowed plugins include: advlist align\_listitems anchor autolink autoresize bbcode charmap codemirror codesample colorpicker directionality emoticons fullscreen hr image insertdatetime link lists media nonbreaking pagebreak preview print readonlynoborder searchreplace table textcolor tableofcontents visualblocks visualchars wordcount
    -   Multiple attributes, such as height, toolbar buttons, and toolbar plugins, can be combined within the Attributes field. For example, `editor.height=300,editor.plugins=table colorpicker textcolor link image media codemirror lists advlist fullscreen charmap directionality emoticons hr insertdatetime nonbreaking pagebreak print searchreplace wordcount anchor codesample visualblocks visualchars compat3x autolink align_listitems,editor.toolbar= fontfamily fontsize | bold italic underline strikethrough forecolor backcolor pastetext removeformat | blocks searchreplace undo redo | bullist numlist outdent indent alignleft aligncenter alignright | tableofcontents table link unlink image media codesample | code fullscreen`.
5.  Select **Update**.


## Change the default height of an HTML field

Change the default height of a specific HTML field to expand the size of a journal field.

### Before you begin

Role required: admin

### About this task

HTML field height is configured per HTML field.

### Procedure

1.  Navigate to a record with an HTML-type field that you want to change.

    For example, select an incident, problem, or knowledge record.

2.  Right-click the field label \(for example, Article body\) and select **Configure Dictionary**.

3.  In the Related Links section, select **Advanced View**.

4.  In the **Attributes** field, enter `editor.height=X`, where X is the desired height.

    For example, `editor.height=250`

    **Note:**

    HTML fields can range from 72 to 2000. HTML fields are by default 64.

5.  Select **Update**.

6.  To configure the height of form fields dynamically as the text line increases rather than providing a specific height, complete the following steps:

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**

    2.  In the search bar, enter `glide.ui.html.editor.enabled_plugins` and select the property.

    3.  In the value field, add `autoresize`.

    4.  Select **Update**.

        The autoresize plugin is active.


## Change the default font size of an HTML field

Change the default font size of a specific HTML field to use a standard font size across forms.

### Before you begin

Role required: admin

### About this task

HTML font size is configured per HTML field.

### Procedure

1.  Navigate to a record with an HTML-type field that you want to change.

    For example, select an incident, problem, or knowledge record.

2.  Right-click the field label \(for example, Article body\) and select **Configure Dictionary**.

3.  Select the Default Value tab.

4.  In the **Default value** field, enter `<p style="font-size:X;"></p>`, where X is the default value.

    For example:

    -   To set the font to large, enter `<p style="font-size:large;"></p>`
    -   To set the size to 10, enter `<p style="font-size:10pt;"></p>`
5.  Select **Update**.


## Configure TinyMCE to allow deprecated tags

You can set a dictionary attribute on a TinyMCE field to allow the use of deprecated HTML tags, such as &lt;b&gt; and &lt;i&gt;. By default, TinyMCE uses the &lt;strong&gt; and &lt;em&gt; tags for bold and italic formatting.

### Before you begin

Role required: personalize\_dictionary or admin

### About this task

After you set the dictionary attribute, use code view to manually enter deprecated tags. The editor does not validate any tags you enter manually, for example, if you type an incorrect character.

### Procedure

1.  Navigate to the form with an HTML field that uses TinyMCE.

2.  Right-click the HTML field label and select **Configure dictionary**.

    ![Configure dictionary](../../form-administration/image/HTMLConfigureDictionary.png)

3.  In the **Attributes** field, enter `tinymce_allow_all=true`, separated by a comma if needed.

    Dictionary entry attributes can only be added to when the dictionary entry form is in advanced view, as they are not shown in default view.

    ![Updated attribute field](../../form-administration/image/TinyMCEAllowAll.png)

    If other attributes are already listed, use a comma as a separator.

4.  Select **Update**.


## Configure TinyMCE to allow JavaScript in URLs

You can set a dictionary attribute on a TinyMCE field to allow the use of JavaScript in a URL.

### Before you begin

Role required: personalize\_dictionary or admin

### Procedure

1.  Navigate to the form with an HTML field that uses TinyMCE.

2.  Right-click the HTML field label and select **Configure dictionary**.

    ![Configure dictionary](../../form-administration/image/HTMLConfigureDictionary.png)

3.  In the **Attributes** field, enter `tinymce_allow_script_urls=true`, separated by a comma if needed.

    Dictionary entry attributes can only be added to when the dictionary entry form is in advanced view, as they are not shown in default view.

    ![Dictionary entry in Advanced view](../../form-administration/image/TinyMCEAllowAll.png)

    If other attributes are already listed, use a comma as a separator.

4.  Select **Update**.


## Configure the menu bar on the TinyMCE HTML editor

You can enable the menu bar on the TinyMCE HTML editor in both CoreUI and workspaces. When enabled, the menu bar appears on the top of the HTML editor which can be used to create, edit and format content. By default, the menu bar is inactive. You can enable it for a specific table via dictionary attribute configuration.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to a record with an HTML-type field that you want to change.

    For example, select an incident, problem, or knowledge record.

2.  Right-click the field label and select **Configure Dictionary**.

    ![TinyMCE v6.8.3 Configure dictionary drop-down menu](../../../use/using-forms/image/TinyMCEV6-configure-dictionary.png)

3.  In the Related Links section, select Advanced View.

4.  In the Attributes field, input `editor.config=new TinymceConfigScript().getConfiguration()`.

    ![TinyMCE v6.8.3 Dictionary entry form](../../../use/using-forms/image/TinyMCEV6-dictionary-entry-form.png)

    This **editor.config** attribute points to a script: **TinymceConfigScript\(\)**.

5.  Access the **TinymceConfigScript**.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    2.  Enter `TinymceConfigScript` in the search bar near the top of the form, and select **enter** or **return**.

    3.  Select **TinymceConfigScript**.

        You will be able to see the following script by default.

        ![Script Include for TinymceConfigScript in Buildtools1](../../../use/using-forms/image/TinyMCEV6-script-include-tinymceconfigscript.png)

        ```
        var TinymceConfigScript = Class.create();
        TinymceConfigScript.prototype = {
            initialize: function() {
            },
            setTinymceConfig: function() {
            var tinyConfig = {
                menubar: 'edit format',
                menu: {
                    file: { title: 'File', items: 'importword exportpdf exportword | print | deleteallconversations' },
                    edit: { title: 'Edit', items: 'undo redo | cut copy paste pastetext | selectall | searchreplace' },
                    view: { title: 'View', items: 'code revisionhistory | visualaid visualchars visualblocks | spellchecker | preview fullscreen | showcomments' }
                },
                style_formats: [
                    { title: 'Headings', items: [
                        { title: 'Heading 1', format: 'h1' },
                        { title: 'Heading 2', format: 'h2' },
                        { title: 'Heading 3', format: 'h3' },
                        { title: 'Heading 4', format: 'h4' },
                        { title: 'Heading 5', format: 'h5' },
                        { title: 'Heading 6', format: 'h6' }
                    ]},
                    { title: 'Inline', items: [
                        { title: 'Bold', format: 'bold' },
                        { title: 'Italic', format: 'italic' },
                        { title: 'Underline', format: 'underline' },
                        { title: 'Strikethrough', format: 'strikethrough' },
                        { title: 'Superscript', format: 'superscript' },
                        { title: 'Subscript', format: 'subscript' },
                        { title: 'Code', format: 'code' }
                    ]},
                    { title: 'Blocks', items: [
                        { title: 'Paragraph', format: 'p' },
                        { title: 'Blockquote', format: 'blockquote' },
                        { title: 'Div', format: 'div' },
                        { title: 'Pre', format: 'pre' }
                    ]},
                    { title: 'Align', items: [
                        { title: 'Left', format: 'alignleft' },
                        { title: 'Center', format: 'aligncenter' },
                        { title: 'Right', format: 'alignright' },
                        { title: 'Justify', format: 'alignjustify' }
                    ]}
                ]
            };
            return tinyConfig;
        },
        getConfiguration: function() {
            var config = this.setTinymceConfig();
            answer = JSON.parse(JSON.stringify(config));
        },
        
            type: 'TinymceConfigScript'
        };
        ```

    4.  Set the menu bar attribute to **true** in the script to enable the menu bar.

        This will enable all the options “File” “Edit” “View” “Insert” “Format” “Table” in the menu bar.

    5.  If you want to disable the menu bar set the menu bar attribute to **false**.

    6.  If you only want to enable specific options on the menu bar, you can change the script by listing those specific options in the menu bar.

        For example, menu bar: 'file edit format' so that only these 3 options appear on the menu bar.

    7.  You can also configure the buttons that display within a menu by changing the script.

        ```
        tinymce.init({
            selector: 'textarea', // change this value according to your HTML
            menu:{
                file: { title: 'File', items: 'newdocument restordraft | preview | importword exportpdf exportword | print | deleteallconversations' },
                edit: { title: 'Edit', items: 'undo redo | cut copy paste pastetext | selectall | searchreplace' },
                view: { title: 'View', items: 'code revision history | visualaid visualchars visualblocks | spellchecker | preview fullscreen | showcomments' },
                insert: { title: 'Insert', items: 'image link media addcomment pageembed codesample inserttable | math | charmap emoticons hr | pagebreak nonbreaking anchor tableofcontents | insertdatetime' },
                format: { title: 'Format', items: 'bold italic underline strikethrough superscript subscript codeformat | styles blocks fontfamily fontsize align lineheight | forecolor backcolor | language | removeformat' },
                tools: { title: 'Tools', items: 'spellchecker spellcheckerlanguage | a11ycheck code wordcount' },
                table: { title: 'Table', items: 'inserttable | cell row column | advtablesort | tableprops deletetable' },
                help: { title: 'Help', items: 'help' }
            }
        });
        ```

6.  Configure custom style format options in the TinyMCEConfigScript by appending the CSS in the style\_formats section.

    Example of style\_formats section of the TinyMCEConfigScript:

    ```
    style_formats: [
      { title: 'Headings', items: [
        { title: 'Heading 1', format: 'h1' },
        { title: 'Heading 2', format: 'h2' },
        { title: 'Heading 3', format: 'h3' },
        { title: 'Heading 4', format: 'h4' },
        { title: 'Heading 5', format: 'h5' },
        { title: 'Heading 6', format: 'h6' }
      ]},
      { title: 'Inline', items: [
        { title: 'Bold', format: 'bold' },
        { title: 'Italic', format: 'italic' },
        { title: 'Underline', format: 'underline' },
        { title: 'Strikethrough', format: 'strikethrough' },
        { title: 'Superscript', format: 'superscript' },
        { title: 'Subscript', format: 'subscript' },
        { title: 'Code', format: 'code' }
      ]},
      { title: 'Blocks', items: [
        { title: 'Paragraph', format: 'p' },
        { title: 'Blockquote', format: 'blockquote' },
        { title: 'Div', format: 'div' },
        { title: 'Pre', format: 'pre' }
      ]},
      { title: 'Align', items: [
        { title: 'Left', format: 'alignleft' },
        { title: 'Center', format: 'aligncenter' },
        { title: 'Right', format: 'alignright' },
        { title: 'Justify', format: 'alignjustify' }
      ]}
    ]
    ```

    Example with three new style formats added \(Bold text, Red text, My-inline\):

    ```
    tinymce.init({
      selector: 'textarea',  // change this value according to your HTML
      style_formats: [
        { title: 'Bold text', inline: 'b' },
        { title: 'Red text', inline: 'span', styles: { color: '#ff0000' } },
        { name: 'my-inline', title: 'My inline', inline: 'span', classes: [ 'my-inline' ] }
      ],
      // The following option is used to append style formats rather than overwrite the default style formats.
      style_formats_merge: true
    });
    ```

    Access the HTML editor and you will see that the new custom style formats \(Bold text, Red text, My-inline\) appear in the formats section of the menu bar.

    ![TinyMCE v6.8.3 Customized text menu bar](../../../use/using-forms/image/TinyMCEV6-customized-text-menubar.png)


