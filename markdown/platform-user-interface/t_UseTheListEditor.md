---
title: Use the list editor
description: The list editor enables you to edit field values directly from a list without navigating to a form.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Methods for list edits, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Use the list editor

The list editor enables you to edit field values directly from a list without navigating to a form.

Use the list editor 

## Before you begin

Role required: none

## About this task

The list editor lets you edit field values in a list without opening a form. Administrators can configure the list editor. By default, list editing is disabled for some tables. Fields of [certain types](https://www.servicenow.com/docs/access?context=r_AdministeringTheListEditor&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) cannot be edited from lists.

Before the list editor opens, access rights to edit the field are verified. If this process takes longer than expected, a loading indicator appears. If the field has a dependency relationship \(for example, Category and Subcategory\), then a composite editor opens to enable editing of all dependent fields. You must have permissions to edit all dependent fields to use the list editor.

## Procedure

1.  Double-click in an empty area of the field.

    The appropriate editor for the field type opens.

    **Note:** You can enable single-click editing from the [list personalization interface](../concept/c_PersonalLists.md#). You can also use keyboard navigation to access the list editor.

2.  Enter the appropriate values.

    To clear a list field configuration, refresh your browser session by reloading the page, and the original list field configuration returns.

3.  Save the records by performing the appropriate action for your list version.

    Select the save icon \(![Save icon](../image/Save.png)\). Select the cancel icon \(![Cancel icon](../image/Cancel.png)\) or press the Escape key to retain the original value.

    ![Editing the category field within a list.](../image/ListEditDependent.png "List editor")

4.  To use keyboard navigation, press the Tab key until the first field in the list is selected, and then select the field to edit in one of the following ways.

    -   Move right: Tab or the Right Arrow key.
    -   Move left: Shift + Tab or the Left Arrow key.
    -   Move down: the Down Arrow key.
    -   Move up: the Up Arrow key.
    To select multiple fields in the same column, hold Shift and press the Down Arrow or the Up Arrow key.

5.  Press the Enter key to open the list editor.

6.  Enter a new value.

    To add another line in a multi-line text field, press Shift + Enter.

7.  Save or cancel your changes in one of the following ways:

    -   Press the Enter key. The new value is saved and the field below the edited field becomes selected.
    -   Press the Tab key. If the list is configured to save immediately, the new value is saved. If the list is configured to save data by rows, an indicator appears beside the value and the list editor opens for the next field. The row is saved only when you navigate away from the row or select the check mark icon beside the row.
    -   Press Ctrl + Enter keys. If the list is configured to save immediately, the new value is saved. If the list is configured to save data by rows, an indicator appears beside the value and the current field remains selected.
    -   Press the Esc key. The list editor closes without saving changes and the field remains selected.
    **Note:** Certain browsers use different key combinations to edit certain field values. For example, to edit a list using Chrome, press the Spacebar.


**Parent Topic:**[Methods for list edits](../reference/r_MethodsForListEdits.md)

**Related topics**  


[Edit multiple records in a list using the list editor](t_EditMultRecUsingListEditor.md)

[Edit multiple records in a list using an editing form](t_EditMultiRecUsingEditingForm.md)

