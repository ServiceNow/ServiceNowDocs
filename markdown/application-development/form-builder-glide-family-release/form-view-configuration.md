---
title: Forms in Table Builder
description: On the Forms tab in Table Builder, you can visually create, configure, and customize the different form views for your users using the form editor. The views that you define contain the elements that appear when a user opens that form or list.
locale: en-US
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Forms in Table Builder

On the **Forms** tab in Table Builder, you can visually create, configure, and customize the different form views for your users using the form editor. The views that you define contain the elements that appear when a user opens that form or list.

## Form View

A form view defines the elements that appear to a user when the user opens a form or list. Each form has a default view, but you may want to create several different form views for different groups of users.

In Table Builder, you can customize multiple views for a form for the different users who input data or view the form. You can also customize the default form view for everyone.

Explore the following major areas when you configure a form or list:

-   Form view selection
-   All form views list
-   Form layout
-   Form fields
-   Form annotations
-   Formatters
-   Embedded lists

## Basic form navigation

The **Forms** tab consists of the following four major areas:

-   Top navigation menu
-   Add form elements panel
-   Form editor
-   Configuration panel

The following table contains a list of some of the other basic navigational elements within the **Forms** tab in Table Builder.

<table id="table_bwb_2cf_jsb"><thead><tr><th>

Navigational element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Forms additional actions list \(![Forms additional actions list](../image/form-addl-actions-list.png)\)

</td><td>

The Additional actions list \(vertical ellipsis\) on the **Forms** tab provides a quick way to perform any of the following actions:-   Add a new form view
-   Duplicate the selected form view
-   Configure a related list
-   Configure a UI action
-   Navigate to a filterable, sortable list of all form views by selecting **All form views**. See [All form views list](form-view-configuration.md#section_y1f_vxh_1vb).

Changes to the form made in the editor are committed to the selected view.**Note:** The more options button ![Ellipses](../../decision-table/image/ellipses.png) is visible only when forms are accessed through ServiceNow Studio or App Engine Studio and not through ServiceNow AI Platform.

</td></tr><tr><td>

Form view list \(![View list.](../image/fb-view-icon.png)\)

</td><td>

Select a form view from this list or use the Additional actions menu \(vertical ellipsis\) to add a view. Changes to the form made in the editor are committed to the selected view.

</td></tr><tr><td>

PDF extractor

 \(![PDF extractor.](../image/icn-pdf-extractor.png)\)

</td><td>

If a PDF is associated with the selected data table, select this element to launch the PDF extractor tool and view the PDF. See [Use a PDF to create data tables](../../../build/app-engine-studio/concept/pdf-extractor.md#).**Note:** This feature is only available if your licensing entitles you to "exclusive low code capability" and you have Table Builder for App Engine installed. Contact your Solutions consultant for more information.

</td></tr><tr><td>

Form element search bar

 \(![Form element search.](../image/fb-elementsearch-icon.png)\)

</td><td>

Enter keywords here to filter the list of form elements.

</td></tr><tr><td>

Multiple selection check box

 \(![Multiple field selection check box.](../image/fb-field-checkbox-icon.png)\)

</td><td>

When you point to a form element in the Add form elements panel, you can select this option if you want to select and drag multiple fields to the form editor at once.

</td></tr><tr><td>

Add form element icon \(![Add icon.](../image/fb-add-icon.png)\)

</td><td>

When you point to a form element or section, select this icon to add a new section or element above or below the existing element.

</td></tr><tr><td>

Move element icon \(![Move element.](../image/fb-move-icon.png)\)

</td><td>

When you point to a form element, this icon displays on the left edge. Select this icon, and then drag the element to move it to the desired location.

</td></tr><tr><td>

Delete form element icon \(![Delete form element.](../image/fb-delete-icon.png)\)

</td><td>

When you point to a form element in the editor, you can select this icon to remove it from the form view.

</td></tr><tr><td>

Move section arrow icon \(![Move section arrow.](../image/fb-move-arrow-icon.png)\)

</td><td>

When you select a form section, you can select the up or down arrow to move it up or down on the form view.

</td></tr><tr><td>

Delete section icon \(![Delete section icon.](../image/fb-remove-section-icon.png)\)

</td><td>

When you select a form section, you can select this icon to remove the section from the form view.

</td></tr><tr><td>

Open panel icon \(![Open panel icon.](../image/fb-expandpane-icon.png)\)

 Close panel icon \(![Close panel icon.](../image/fb-collapsepane-icon.png)\)

</td><td>

Selecting the Open panel icon expands the panel to the right. Selecting the Close panel icon collapse it.

</td></tr></tbody>
</table>## Form view selection

Select a form view to work with from the form view list in the form editor.

**Note:** You can also select a form view from the Additional actions menu on the **Forms** tab.

See [Choose a form view in Table Builder](../task/manage-form-views.md).

## All form views list

Select **All form views** from the Additional actions menu to the right of the **Forms** tab to browse a filterable list of form view cards \(vertical ellipsis\). This page allows you to create complex filtering and sorting if you have a great deal of form views to navigate.

You have the following options for finding a desired form view if you have a large list of them.

<table id="table_zkp_3zn_15b"><thead><tr><th>

Option

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Search

</td><td>

Type a keyword in the **Search** box. The list of cards will be filtered as you type.

</td></tr><tr><td>

Sort form views

</td><td>

Select an option from the sorting list to sort the form view cards.-   Form name \(a to z\)
-   Form name \(z to a\)
-   Updated by \(a to z\)
-   Updated by \(z to a\)
-   Updated \(recent to last\) - Default option
-   Updated \(last to recent\)

</td></tr><tr><td>

Filter forms by setting up filter criteria

</td><td>

1.  Select the filter icon \(![Filter forms.](../image/filter-flows.png)\).
2.  Add your filter condition criteria including any AND/OR logic.
3.  To add additional conditions, select **+ New condition set**.
4.  Select **Apply**.

</td></tr></tbody>
</table>## Form layout \(sections\)

A view is composed of sections that group the data elements that you want displayed.

You can add multiple sections and change the layout of each section into one or two columns. A section is where you can group the data elements that you want to display for a form view. These elements include form fields, annotations, formatters, and embedded lists.

See [Customize your form layout in Table Builder](../task/customize-form-layout.md).

## Form fields

When you select a table in Table Builder, the available fields are displayed in the form elements panel. You can create fields for the table or configure the fields and their properties.

By dragging these fields into the form editor, you can then visually arrange these fields on the form view you have selected.

See [Add fields to a form layout in Table Builder](../task/add-form-fields.md).

See [Modify field properties in Table Builder form editor](../task/modify-field-properties.md).

## Form annotations

A form annotation is an additional piece of information on a form, such as a line or paragraph of text.

For example, you may want to add instructional text for a particular section on the form. By using Table Builder, you can add a form annotation to the view that displays on-screen instructions on how a user should enter information.

See [Create form annotations in Table Builder](../task/create-form-annotations.md).

## Formatters

A **Formatter** is a read-only element in a form that displays additional information about the selected table record. Unlike fields, formatters are not editable.

See [Using formatters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_Formatters.md).

By using Table Builder, you can visually drag any of the displayed formatters onto the form editor and arrange them.

See [Add formatters in Table Builder](../task/add-formatters.md).

## Embedded lists

You can use an embedded list to display the data for a selected related list on a form. A related list shows the records in the tables that have relationships to the current record. For example, for a form view that references a Problem table, you might want to display a list of locations that are impacted by a selected problem.

With Table Builder, you can visually drag a list from the **Embedded Lists** tab of the form elements panel onto the form editor, and then arrange them.

By adding an embedded list to a form, you enable your users to view or edit the related list without needing to navigate away from the form. Changes to the data in the list are saved when the user saves the form.

See [Add embedded lists in Table Builder](../task/add-embedded-lists-form.md).

-   **[Choose a form view in Table Builder](../task/manage-form-views.md)**  
Choose existing views, duplicate views, or create entirely new views for form users in Table Builder.
-   **[Customize your form layout in Table Builder](../task/customize-form-layout.md)**  
Visually design the look of the forms your users see by customizing form views in Table Builder.
-   **[Add fields to a form layout in Table Builder](../task/add-form-fields.md)**  
Visually add and arrange fields within a form layout to create a form that matches your requirements using Table Builder.
-   **[Modify field properties in Table Builder form editor](../task/modify-field-properties.md)**  
Modify basic field properties for the fields that display for users in a form view from within the **Forms** tab in Table Builder.
-   **[Create form annotations in Table Builder](../task/create-form-annotations.md)**  
Add instructional text and other design elements to your forms by using form annotations in Table Builder.
-   **[Add formatters in Table Builder](../task/add-formatters.md)**  
You can add form elements that display non-field information to users by adding a formatter in Table Builder. For example, you may want to display a **Comments** field where users can add comments to a displayed form.
-   **[Add embedded lists in Table Builder](../task/add-embedded-lists-form.md)**  
Add an embedded list using Table Builder to display data for a selected related list on your form. A related list shows the records in the tables that have relationships to the current record. For example, for a form view that references a Problem table, you might want to display a list of locations that are impacted by a selected problem.
-   **[Preview your form](../task/preview-your-form.md)**  
Previewing and saving your form in Table Builder.

**Parent Topic:**[Using Table Builder](using-fb.md)

