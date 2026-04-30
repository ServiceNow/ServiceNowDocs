---
title: Layout editor
description: Learn how to use the layout editor to modify a layout without leaving ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 3
breadcrumb: [Set up layouts, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Layout editor

Learn how to use the layout editor to modify a layout without leaving ServiceNow CPQ.

The layout editor enables an admin to edit an layout without leaving ServiceNow CPQ.

![Layout editor](../images/cpq-layout-editor.png)

1.  The layout variable name appears in parenthesis in the header. The layout name and description can be edited by clicking the pencil icon.
2.  Three actions are available: **Replace**, **Export**, and **Save**.
    -   **Replace**: Launches the file picker to select a CSV file to replace the current layout.
    -   **Export**: Exports and downloads a CSV file of the current layout
    -   **Save**: Save changes to the layout. This button will be disabled if no changes have been made to the layout.
3.  The layout editor provides three tabs for editing different aspects of the layout: Arrange Layout, Edit Field Info, and tier definition.

## The Arrange Layout tab

The Arrange Layout tab provides a similar experience to the Layout Wizard. It lets you adjust various depths but does not allow for a change in the overall tier format.

![Layout editor](../images/cpq-layout-editor-arrange-layout.png)

1.  Tier labels can be edited inline by clicking the pencil icon that appears on hover.
2.  Extended properties of the element can be edited by clicking the gear icon, which will launch a window to update the values.
3.  The field label can be edited by clicking the pencil icon, and extended properties of the field can be edited by clicking the gear icon. Fields can also be edited in the Edit Field Info tab.
4.  Clicking the plus icon in a column set lets you search for fields to add to the column set.
5.  Additional column sets can be added to the layout by clicking the plus icon in the tier you want to add to.
6.  Tiers can be added to the layout by clicking the plus icon outside of the existing tiers.

**Tip:** Several keyboard shortcuts are available to rearrange these visual elements. For example, tiers and column sets can be moved vertically by pressing Cmd/Ctrl + ↑ or ↓, and fields can be moved horizontally by pressing Cmd/Ctrl + ← or →. While in the Arrange Layout tab, you can view the keyboard shortcuts by pressing Shift + ? or by clicking the keyboard icon at the top of the page.

## Keyboard shortcuts

Mac:

![Layout editor](../images/cpq-layout-editor-mac.png)

PC:

![Layout editor](../images/cpq-layout-editor-pc.png)

## Missing fields

If a layout contains fields that are no longer available appear slightly grayed out, with a dashed border.

![Layout editor](../images/cpq-layout-editor-missing-fields.png)

## Partially supported elements

Layout elements that are only partially supported appear with a darker gray background. Some properties can still be edited by clicking the gear icon.

Field information such as label, display type, and extended properties can be edited in the layout editor.

![Layout editor](../images/cpq-layout-editor-partially-supported-elements.png)

![Layout editor](../images/cpq-layout-editor-expanded.png)

1.  Search and filter fields associated with the layout.
2.  The field label can be edited inline by clicking the label to edit.
3.  The field display type can be updated from a list of available options for the field type by clicking the display type value for the field you are updating.
4.  Extended properties of the field can be edited by clicking the gear icon and making the edits in a dialog box.

## Edit extended field properties

![Layout editor](../images/cpq-layout-editor-field-properties-1.png)

1.  Class Name: Classes can be added to fields and searched for in the search bar. Classes appear as a pill once added. Classes that control the width and height of the field or align the field to a grid layout have built-in support.
2.  Raw Value: The value can also be edited directly, in the format of key:value pairs. This corresponds to the value column in the layout.csv file.
3.  Cancel and Save

    ![Layout editor](../images/cpq-layout-editor-field-properties-2.png)

4.  Number fields also have three values: **Precision**, **Symbol**, and **Unit**.
    -   **Precision**: Controls the decimal precision of the number field
    -   **Symbol**: Displays to the left of the number field
    -   **Unit**: Displays to the right of the number field

## Tier definition

The overall structure of the layout tiers can be updated in the tier definition tab. This is similar to selecting the initial tier definition when using the Layout Wizard.

![Layout editor](../images/cpq-layout-editor-tier-definition.png)

1.  Tier definition preview: Shows a simplified preview of the currently selected tier definition
2.  Tier definition menu: Provides a list of available tier definitions to select from

When you have made all the changes to the layout, don’t forget to save it, using the Save button in the header.

## Additional considerations

Layouts that were uploaded by using API calls cannot be edited in the layout editor. A message will appear that lets you import a CSV file to replace the layout.

![Layout editor](../images/cpq-layout-editor-cannot-edit-layout.png)

Modifications that cannot be made by using the layout editor can be made by exporting, adjusting, and importing layout CSV files.

The order of rows is not maintained as the layout editor parses the values.

