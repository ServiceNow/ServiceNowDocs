---
title: Table Builder workflow and navigation
description: You can start using Table Builder to manage your data tables, forms, or flows by reviewing this high-level workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/form-builder-glide-family-release/form-builder-workflow.html
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Table Builder workflow and navigation

You can start using Table Builder to manage your data tables, forms, or flows by reviewing this high-level workflow.

Learn about the high-level actions that you perform when you are using Table Builder.

## Basic workflow

The following table outlines the basic actions that you take when working in Table Builder.

<table><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Choosing a table or form to work with

</td><td>

To choose a data table or form to work with, launch Table Builder as instructed in [Accessing Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/accessing-form-builder.md) and choose the table or form to work with.

 **Note:** While using Table Builder in App Engine Studio, the table selected here is chosen when you click on a table in your app. However, if Table Builder is launched from UI Builder, you can choose a new table to work with from the drop-down list that displays the name of your currently selected table.

</td></tr><tr><td>

Selecting a domain and application scope

</td><td>

Select a domain and application scope to work within from Table Builder navigation.

 **Note:** While using Table Builder in App Engine Studio, the application scope selected is the app you are working in. However, if Table Builder is launched from UI Builder, you can choose an application scope to work with from the drop-down list in the top right side of your screen \(e.g., Global\).

 See [Domain separation and Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/form-builder-domain-separation.md) and [Using an application scope with Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/fb-application-scope.md).

</td></tr><tr><td>

Modifying table properties

</td><td>

Select **Data** tab to edit table properties directly.

 For more information, see [Data in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/table-builder.md).

</td></tr><tr><td>

Customizing form views

</td><td>

Select **Forms** tab to create and customize new views or configure the form elements for a selected view.

 For more information, see [Forms in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/form-view-configuration.md).

</td></tr><tr><td>

Configuring policies and rules

</td><td>

Select **Policies and rules** tab to configure and control how data is displayed for your form views.

 For more information, see [Policies and rules in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/form-builder-policies-rules.md).

</td></tr><tr><td>

Previewing a form and managing your changes

</td><td>

At any point in the process, you can preview the changes you've made by selecting **Preview**. For more information, see [Preview your form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/preview-your-form.md).

 Save your form view changes at any point in the process by clicking **Save**. Your form view is ready and can be accessed by other applications in the ServiceNow AI Platform.

**Note:** To undo \(\[Omitted image "fb-undo-icon.png"\] Alt text: Undo icon.\) or reapply \(\[Omitted image "fb-redo-icon.png"\] Alt text: Redo icon.\) changes you make, select the Undo or Redo icons at the top of your screen.

</td></tr></tbody>
</table>## Navigational elements

The following table shows and describes the basic navigational elements shown in Table Builder.

<table id="table_rd5_jqm_jsb"><thead><tr><th>

Navigational element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table selection list \(\[Omitted image "fb-tableselection-icon.png"\] Alt text: Table selection list.\)

</td><td>

Choose an option to customize the policies and rules, table properties, fields, or form views for the selected table.

</td></tr><tr><td>

Select domain list

 \(\[Omitted image "fb-domain-icon.png"\] Alt text: Domain selection list.\)

</td><td>

Choose an option to customize the policies and rules, table properties, fields, or form views within the selected domain \(for example, the Global domain\).

</td></tr><tr><td>

Select scope list \(\[Omitted image "fb-app-scope-icon.png"\] Alt text: Application scope selection list.\)

</td><td>

Choose an option to customize the policies and rules, table properties, fields, or form views within the selected application scope \(for example, the Global application scope\).

</td></tr><tr><td>

Undo \(\[Omitted image "fb-undo-icon.png"\] Alt text: Undo icon.\)

 Redo \( \[Omitted image "fb-redo-icon.png"\] Alt text: Redo icon.\)

</td><td>

Select the undo \(\[Omitted image "fb-undo-icon.png"\] Alt text: Undo icon.\) or redo \(\[Omitted image "fb-redo-icon.png"\] Alt text: Redo icon.\) icons in the navigation bar to revert to a previous editing state.

</td></tr><tr><td>

Advanced table properties menu \(\[Omitted image "fb-advancedtable-icon.png"\] Alt text: Advanced table properties menu.\)

</td><td>

Choose an option:

-   **Advanced view** to manage the advanced properties in the selected table. For more information, see [Table administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_TableAdministration.md).
-   **Form designer** to launch the selected table in Form Designer. For more information, see [Using the Form Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_FormDesign.md).
-   **Delete table** to delete the selected table.

**Note:** This option only appears on the Data tab.

</td></tr><tr><td>

Preview

 \(\[Omitted image "fb-preview-icon.png"\] Alt text: Preview icon.\)

</td><td>

Select **Preview** to review the selected form as how it is displayed in the ServiceNow AI Platform. For more information on previewing, see [Preview your form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/preview-your-form.md).

</td></tr><tr><td>

Save \(\[Omitted image "form-save-icon.png"\] Alt text: Save icon.\)

</td><td>

Select **Save** to commit your changes to your selection.

</td></tr><tr><td>

Search fields and filter options

 \(\[Omitted image "icn-search-fields.png"\] Alt text: Search fields and filter options.\)

</td><td>

Use the search box to filter the list of field columns by keyword or use the **Filter options** list to show inactive fields or to hide extended fields from the list \(if a table has been extended from an existing table\).

</td></tr><tr><td>

PDF extractor

 \(\[Omitted image "icn-pdf-extractor.png"\] Alt text: PDF extractor.\)

</td><td>

If a PDF is associated with the selected data table, select this element to launch the PDF extractor tool and view the PDF. See [Use a PDF to create data tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/pdf-extractor.md).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/exploring-fb.md)

