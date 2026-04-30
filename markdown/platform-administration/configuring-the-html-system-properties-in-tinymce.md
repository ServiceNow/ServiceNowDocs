---
title: Configuring system properties for TinyMCE HTML editor
description: There are multiple system properties that are used to configure the behaviour of the HTML editor field type. Learn about the system properties available in the TinyMCE rich text editor.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a field editor for the HTML field, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring system properties for TinyMCE HTML editor

There are multiple system properties that are used to configure the behaviour of the HTML editor field type. Learn about the system properties available in the TinyMCE rich text editor.

<table id="table_idc_kqs_kbc"><thead><tr><th>

System properties for TinyMCE HTML editor

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.html.editor.valid\_plugins​

</td><td>

String

</td><td>

Client-side HTML editor plugins that CAN BE added/or used \(spaced delimited\).

**Important:** Removing plugins could cause undesirable side-effects.

</td></tr><tr><td>

glide.ui.html.editor.enabled\_plugins​

</td><td>

String

</td><td>

Client-side HTML editor plugins that should be added \(spaced delimited\) in order for them to get enabled on the widget.

 Only plugins added in glide.ui.html.editor.valid\_plugins​ can be added. Removing plugins could cause undesirable side-effects.

</td></tr><tr><td>

glide.ui.html.editor.toolbar.valid\_buttons​

</td><td>

String

</td><td>

A valid \(supported\) button list for html fields. Use this to limit what buttons CAN BE added to the toolbar.

</td></tr><tr><td>

glide.ui.html.editor.toolbar ​

</td><td>

String

</td><td>

Configures the editing toolbar for HTML fields. This is a space-separated list without commas. Only valid buttons added in glide.ui.html.editor.toolbar.valid\_buttons​​ can be added.

</td></tr><tr><td>

glide.ui.html.editor.paste.html\_import​

</td><td>

Choice list

</td><td>

Paste formatting behavior for HTML. This setting controls how content from sources other than Microsoft Word is filtered when being pasted on html-editor. Note that this includes content copied from TinyMCE itself. The supported values are:

-   Clean: Preserves the structure of the content such as headings, tables, and lists but remove inline styles and classes. This results in simple content that uses the site's CSS stylesheet while retaining the semantic structure from the original document.
-   Merge: Preserves the inline formatting and structure of the original document. Invalid and proprietary styles, tags and attributes are still removed ensuring that the HTML is valid while more closely matching the original document formatting.
-   Prompt: Prompts the user to choose between the clean and merge options after attempting to paste HTML content.

</td></tr><tr><td>

glide.ui.html.editor.paste.word\_import​

</td><td>

Choice list

</td><td>

Paste formatting behavior for word. This setting controls how content from Microsoft Word is filtered when being pasted on html-editor. Note that this includes content copied from TinyMCE itself. The supported values are:

-   Clean: Preserves the structure of the content such as headings, tables, and lists. Removes inline styles and classes. This results in simple content that uses the site’s CSS stylesheet while retaining the semantic structure of the original document.
-   Merge: Preserves the inline formatting and structure of the original document.Removes invalid and proprietary styles, tags and attributes.This ensures the HTML is valid while more closely matching the original document formatting.
-   Prompt: Prompts the user to choose between the clean and merge options after attempting to paste HTML content.

</td></tr><tr><td>

glide.ui.html.editor.font.collection​

</td><td>

String

</td><td>

User can select different font collection for Tiny MCE HTML editor:

 Example with one font:

 ```
<pre>
Arial=arial,helvetica,sans-serif;
</pre>

```

 **Note:** More than one font value should be separated by a semi-colon with no space or line-break.

 Example with more than one font:

 ```
<pre>
Andale Mono=andale mono,times;
Arial=arial,helvetica,sans-serif;
Arial Black=arial black,avant garde;
Book Antiqua=book antiqua,palatino;
Comic Sans MS=comic sans ms,sans-serif;
Courier New=courier new,courier;
Georgia=georgia,palatino;Helvetica=helvetica;
Impact=impact,chicago;Symbol=symbol;
Tahoma=tahoma,arial,helvetica,sans-serif;
Terminal=terminal,monaco;
Times New Roman=times new roman,times;
Trebuchet MS=trebuchet ms,geneva;
Verdana=verdana,geneva;
Webdings=webdings;
Wingdings=wingdings,zapf dingbats;
</pre>

```

</td></tr><tr><td>

glide.ui.html.editor.paste.filtered\_inline\_elements​

</td><td>

String

</td><td>

This setting allows the content to be filtered when pasted from MS Word to the TinyMCE V6 editor. This property takes input as a comma separated string of inline elements to be filtered by selecting the **Remove formatting** button on the paste prompt dialog. Default value is 'strong, b'.

</td></tr><tr><td>

glide.ui.html.editor.convert\_urls

</td><td>

True \| False

</td><td>

This system property is used to set the convert\_urls config of TinyMCE. Default: false.**Note:** This is related to the value of relative\_urls which itself is set by glide.ui.html.editor.relative\_urls.

</td></tr><tr><td>

glide.ui.html.editor.extended\_valid\_elements

</td><td>

String

</td><td>

This system property is used to set the extended\_valid\_elements config of TinyMCE. Default: &lt;Empty string&gt;.

</td></tr><tr><td>

glide.ui.html.editor.relative\_urls

</td><td>

True \| False

</td><td>

glide.ui.html.editor.relative\_urls is used to set the relative\_urls config of TinyMCE. Default: true.**Note:** This is related to the document\_base\_url which is not configurable in ServiceNow and is set to the window.location.origin \(the base url of the instance\).

</td></tr><tr><td>

glide.ui.html.editor.contextmenu

</td><td>

String

</td><td>

Client-side HTML editor has its own context menu, overriding the browser's. Holding Ctrl while right-clicking bypasses the editor's context menu to show the native context menu.

 This property specifies which context menu options are available. Default value is "link image table" \(without quotes\). A value of "false" \(without quotes\) disables the editor's context menu.

</td></tr><tr><td>

glide.ui.html.editor.toolbar.on.focus

</td><td>

String

</td><td>

True: User should be able to see hide toolbar behaviour if they move focus out.

 False: User should always see the toolbar regardless of the tab focus.

 **Note:** This property isn't added OOTB \(out of the box\) but can be added by an admin.

</td></tr><tr><td>

glide.ui.html.editor.default\_link\_target

</td><td>

 

</td><td>

This system property is used to set link\_default\_target.

</td></tr></tbody>
</table>