---
title: Create form annotations in Table Builder
description: Add instructional text and other design elements to your forms by using form annotations in Table Builder.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Forms in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Create form annotations in Table Builder

Add instructional text and other design elements to your forms by using form annotations in Table Builder.

## Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](../concept/accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](../concept/form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](../concept/fb-application-scope.md).

**Note:** To understand how to approach customizing your forms, review [Table Builder workflow and navigation](../concept/form-builder-workflow.md).

Role required: personalize\_form or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to the **Forms** tab in Table Builder.

2.  Choose a view to work with.

    For detailed information on how to choose a view for a form, see [Choose a form view in Table Builder](manage-form-views.md).

3.  To display a list of the available components that you can add to your form view, in the Add form elements panel, select **Components**.

    **Note:** You can also launch the Add form elements panel by clicking the Add \(![Add icon.](../image/fb-add-icon.png)\) icon above an existing element in the form editor.

4.  Select the **Annotation** elements, and then drag it to the location in the form editor where you'd like to position the annotation text as shown in the following example.

    ![Add annotation.](../image/fb-annotation-drag.gif "Add annotation")

5.  Select the **Annotation type**.

    |Annotation type|Description|
    |---------------|-----------|
    |**Info Box Blue**|Blue box that surrounds the entered text.|
    |**Info Box Red**|Red box that surrounds the entered text.|
    |**Line Separator**|Line separator inside a section.|
    |**Plain Text**|Text that is entered as plain text.|
    |**Section Details**|Text that is entered as section details.|
    |**Section Plain Text**|Text that is entered as plain text in a section.|
    |**Section Separator**|Line separator between sections.|
    |**Text**|Text that is entered as text.|

6.  Select an option for **Annotation text**.

<table id="choicetable_ttw_vx3_fsb"><thead><tr><th align="left" id="d275882e311">

Annotation text option

</th><th align="left" id="d275882e314">

Description

</th></tr></thead><tbody><tr><td id="d275882e320">

**Plain text**

</td><td>

Text that is entered renders on the form as plain text.

</td></tr><tr><td id="d275882e329">

**Rich text**

</td><td>

Rich text. When you point to the text box below, an Edit rich text icon is displayed. Select this icon to launch a rich text editor window where you can adjust the basic properties for the text that you want to display on the form such as:-   Font size
-   Font color or background color
-   Bold, italic, underline
-   Indentation
-   List type \(bullet or ordered list\)
-   Add hyperlink or remove hyperlink
 To show the HTML code that renders on the form, click **Show HTML**, and then click **Apply**.

</td></tr></tbody>
</table>7.  Enter the desired annotation text in the field that displays in the Annotation panel.

8.  Select **Save**.


**Parent Topic:**[Forms in Table Builder](../concept/form-view-configuration.md)

