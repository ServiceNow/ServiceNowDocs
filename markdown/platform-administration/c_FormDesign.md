---
title: Using the form designer
description: Administrators or users with the personalize\_form role can use the form design feature to quickly create new or change existing form views.You can move fields to and from the form workspace to display the fields on the form.Use annotations to provide instructions or additional information about fields on a form.Move sections to and from the form layout to display or remove the sections on the form.Use formatters to add information from macros or previously scripted UI elements to a form.You can add a field to a form and the associated table.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configuring forms, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Using the form designer

Administrators or users with the personalize\_form role can use the form design feature to quickly create new or change existing form views.

**Important:** Try configuring your forms with Form Builder instead. Form Builder has all of the Form Designer and Form Layout options. It also has other robust features that help you configure each aspect of the form. For more information, see [Accessing Form Builder](https://www.servicenow.com/docs/access?context=access-form-builder&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

With form design, you can accomplish the same tasks that you can with form layout in a graphical tool called the form designer. You can also access field properties and add information from macros or previously scripted UI elements.

Form design is an alternative to configuring forms that combines several configuration options into one tool. It is available by default for new instances and requires Core UI . Administrators who upgrade from a previous version must activate the Form Designer \(com.glide.ui.ng.fd\) plugin to use the feature.

Access Form Designer by opening an existing form, selecting the Additional actions icon \(![Additional actions icon](../../contextual-search/image/additional-actions.png)\), and then navigating to **Configure** &gt; **Form Design**.

![Callout for the location of the Form Designer application using the additional actions menu on a form.](../image/access-form-designer.png "Accessing Form Designer from an existing form")

![Parts of the form design](../image/UiFormDesign02.png "Parts of the UI form design interface")

-   **The page header**

    The page header displays the current table and view being designed. Each form is tied to a unique table and view combination. For example, there can only be one form for the incident table default view. Select a different view to modify different form layouts for a table.

    ![Parts of the header](../image/UiFormDesignHeader02.png)

-   **The field navigator**

    The field navigator allows you to manage fields on the form. It contains the following elements:

    -   **Filter**: Allows text search on the currently selected tab.
    -   **Fields**: Displays a list of existing fields you can add to the current form.
    -   **Field Types**: Displays a list of field types you can add to the current form. Adding a field type to the form layout creates fields in the selected table when the form layout is saved.
    ![Parts of the field navigator](../image/UiFormDesignFieldNav02.png)

    Field properties are accessed by clicking the gear icon that appears when you point to a field in the form layout.

    ![Field properties](../image/UiFormDesignFieldProps02.png)

-   **Form layout**

    The form layout displays a separate cell for each field, section, annotation, UI element, and related list that is on the form. Each cell has an identifying label and a handle icon to aid in selecting and moving it. The location of the cell in the form layout represents its relative position on the form. Only fields visible on the form layout are displayed on a form.

    ![Form layout](../image/UiFormDesignFormWorkspace02.png "Form layout")


## Show or hide fields with the form designer

You can move fields to and from the form workspace to display the fields on the form.

### Before you begin

Role required: personalize\_form

### About this task

Use the filter to quickly find fields in the field navigator.

### Procedure

1.  Navigate to the form designer.

2.  From the list of fields in the **Field Navigator**, select the field you want to display from the list of available fields.

3.  Drag the field to the form layout.

4.  Drag the field to the location you want it to be on the form.

5.  To remove a field from the form layout, select the field and click the **Remove this field** \(X\) button beside the field label.

6.  Click **Save**.


## Add a form annotation with the form designer

Use annotations to provide instructions or additional information about fields on a form.

### Before you begin

Role required: personalize\_form

### Procedure

1.  Navigate to the form designer.

2.  Click the **Field Types** tab.

3.  Select the **Annotations** field type.

4.  Drag the annotation to the appropriate location on the form.

5.  Point to the **Annotations** field and click the gear icon to open Properties dialog box.

6.  In the Properties dialog box, enter a value for **Annotation Text**.

    You can use HTML tags to format the annotation text.

7.  Click **Save**.


## Add a new section with the form designer

Move sections to and from the form layout to display or remove the sections on the form.

### Before you begin

Role required: personalize\_form

### About this task

Sections can have a one- or two-column layout.

By default, the first section on a form is always a read-only section displaying the label of the table. You cannot remove this section.

### Procedure

1.  Navigate to the form designer.

2.  Select an existing section.

3.  Click the \(+\) button beside the section label to add a section.

4.  Enter a label for the section.

5.  Drag sections to reorder them.

    The label for the first section on the form designer is displayed as the form title.

6.  To delete a section, click the \(x\) button beside the section label.

7.  Click **Save**.

    The following GIF shows how you would use form designer to add and then delete a form section.

    ![Form designer example.](../image/form-design-example.gif)


## Add a formatter with the form designer

Use formatters to add information from macros or previously scripted UI elements to a form.

### About this task

Formatters are used to add information from macros or previously scripted UI elements to a form.

### Procedure

1.  Navigate to the form designer.

2.  Click the **Fields** tab.

3.  In the filter, enter the string `Format`.

4.  Select the formatter you want to add to the form.

5.  Drag the formatter to the location you want it to be on the form.

6.  Click **Save**.


## Add a new field with the form designer

You can add a field to a form and the associated table.

### Before you begin

Role required: personalize\_form

### About this task

Adding a field creates a dictionary entry for the new column in the current table. You can create a custom table and then use the form designer to add fields to the form.

Use the filter to quickly find field types in the field navigator.

### Procedure

1.  Navigate to the form designer.

2.  Click the **Field Types** tab.

3.  Select the cell for the field type to create.

4.  Drag the field type to the location you want it to be on the form.

5.  Enter a label for the field.

6.  Point to a field in the form design area and click the gear icon to access properties.

7.  Click **Save**.


