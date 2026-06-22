---
title: Schema view in Table Builder
description: Use Schema view in Table Builder to explore data relationships for your application data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/form-builder-glide-family-release/tb-schema-view.html
release: australia
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Data in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Schema view in Table Builder

Use **Schema** view in Table Builder to explore data relationships for your application data.

## Before you begin

-   Launch Table Builder. For more information, see [Accessing Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/accessing-form-builder.md).
-   \(Optional\) Choose a domain to work within \(if not global\). For more information, see [Domain separation and Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/form-builder-domain-separation.md).
-   \(Optional\) Choose an application scope to work within \(if not global\). For more information, see [Using an application scope with Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/fb-application-scope.md).

Role required: personalize\_dictionary or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-engine-studio/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to the **Data** tab.

    **Note:** Spreadsheet view displays by default.

2.  Select **Schema** from the additional actions menu \(\[Omitted image "tb-data-addl-actions-menu.png"\] Alt text: Additional actions menu.\) to access Schema view.

3.  Navigate through the schema diagram by dragging the canvas with your mouse.

4.  You can perform the following additional actions on this read-only screen.

<table id="choicetable_a2c_l1c_wvb"><tbody><tr><td id="d207407e163">

**Navigation overview controls**

</td><td>

Select the **Overview toggle** icon \(\[Omitted image "icn-us2-schemaview-overview.png"\] Alt text: Overview toggle icon.\) in the lower right corner to toggle the navigational overview controls on or off. This navigational control enables you to perform the following actions:-   When the schema diagram is zoomed in, you can drag the rectangle showing your view around by clicking and dragging it to focus it on the part of the diagram you want to review.
-   Select the **Zoom in** icon \(\[Omitted image "icn-us2-schemaview-zin.png"\] Alt text: Zoom in icon.\) to zoom in.
-   Select the **Zoom out** icon \( \[Omitted image "icn-us2-schemaview-zout.png"\] Alt text: Zoom out icon.\) to zoom out.


</td></tr><tr><td id="d207407e210">

**Show / hide table fields**

</td><td>

The **Expand tables** toggle is toggled on by default to show all the fields within the displayed schema tables. To hide the fields within the displayed schema tables, select **Expand tables** to toggle it off.

</td></tr><tr><td id="d207407e225">

**Show / hide tables**

</td><td>

Use the **Items selected** menu to view a list of application and non-application tables that are displayed in the schema diagram. You can select the table name to remove the selection checkmark, which hides the table from displaying in the diagram. To show the table, select the table name again to toggle the checkmark back on.

</td></tr><tr><td id="d207407e237">

**Set field options**

</td><td>

Use the **Field options** menu to control how fields display in the schema diagram.-   Select **Extended fields** to display extended fields within schema tables.
-   Select **Field type** to show the type of field for each field displayed in the schema tables.


</td></tr><tr><td id="d207407e263">

**Group fields**

</td><td>

Use the **Group fields by** menu to group fields within the displayed tables \(e.g., grouping fields by type\). Choose from the following grouping options:-   No group
-   Extended
-   Reference
-   Type


</td></tr><tr><td id="d207407e290">

**Sort fields**

</td><td>

Use the **Sort fields** menu to sort fields within the displayed tables. Choose from the following sorting options:-   Alphabetically \(A to Z\)
-   Alphabetically \(Z to A\)


</td></tr><tr><td id="d207407e310">

**View legends**

</td><td>

Select **View legends** to view information for interpreting the displayed schema diagram.

</td></tr><tr><td id="d207407e322">

**Table-specific options**

</td><td>

Select the **Additional options** icon \(\[Omitted image "icn-us2-schemaview-addloption.png"\] Alt text: Additional options icon.\) for a table to control how fields in the selected table are displayed, grouped, and/or sorted similar to the top-level options described above.

</td></tr><tr><td id="d207407e340">

**View in Table Builder**

</td><td>

Select the **View Table** icon \(\[Omitted image "icn-us2-schemaview-navtotb.png"\] Alt text: Navigate to Table Builder icon.\) to view the selected table in Table Builder.

</td></tr></tbody>
</table>
**Parent Topic:**[Data in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/form-builder-glide-family-release/table-builder.md)

