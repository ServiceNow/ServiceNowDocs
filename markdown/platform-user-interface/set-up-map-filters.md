---
title: Add a map filter
description: Add a map filter to display filtered map markers. This filter enables you to see only the map markers for the data that you want.Choose a Map Page for your map filter, and determine how it functions on the Map Page.Select your map filter to complete the Map Page filter setup. This setup applies the map filter to your Map Page.Check to see that your map filter was successfully created in your Map Page.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Create an advanced Map Page, Map pages, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add a map filter

Add a map filter to display filtered map markers. This filter enables you to see only the map markers for the data that you want.

## Before you begin

A [map data item](configure-map-data-items.md) should be configured before accomplishing this task. The example map data item can work with the example map filter tables below to successfully set up a map filter.

Role required: admin

## About this task

Map filters can be configured using lists and forms, or scripting. Create a container for your map filters first, configure filter items, and then choose a Map Page for your filter.

## Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Filters**.

2.  Click **New**.

3.  In the **Name** field, enter a name for the map filter.

4.  In the **Application** field, define the application scope, if other than Global.

5.  Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.

6.  In the **Map filter item** field, double-click the record and click the search icon \(![Search icon](../image/QueryIcon.png)\).

7.  To create a Map Page filter item, click **New**.

8.  On the form, fill in the fields.

<table id="table_ewl_cpm_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for your Map Page filter item.

</td></tr><tr><td>

Label

</td><td>

Title for your Map Page filter item that's displayed in the map filter in your Map Page.

</td></tr><tr><td>

UI Type

</td><td>

UI type for your Map Page filter item. This determines how your filter displays on the map page. Select **Single selection**, **Multiple selection**, or **Date picker**. When you select **Date picker**, the data item fields hide and the default value script appears.![The UI Types on a map page.](../image/Map_Filter_UI_Selection.png)

</td></tr><tr><td>

Data type

</td><td>

Data type for your Map Page filter item. Select **Data item** or **Scripted** for the data type. A data item enables you to configure or select data items using lists and forms.

</td></tr><tr><td>

Application

</td><td>

Application scope for your Map Page filter item, if other than Global.**Note:** This field is optional.

</td></tr><tr><td>

Data item

</td><td>

Data item for your Map Page filter item. Select the data item that you previously configured.

</td></tr><tr><td>

Data item table

</td><td>

Data item table for your Map Page filter item. **Note:** This field is automatically populated when a data item is selected.

</td></tr><tr><td>

Data item value field

</td><td>

Data item value field for your Map Page filter item. Choose how data is used in a table.

</td></tr><tr><td>

Default value script

</td><td>

Scripting field for your Map Page filter item.

</td></tr></tbody>
</table>9.  Click **Submit**.

10. When you return to the Map Page Filter form, click the check mark icon \(![Check mark icon](../image/CheckMark.png)\).

    The name of the Map Page filter item that you created is displayed in the field.

11. Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.


## Map Page Filter Item form

Select the options in the table to successfully create your Map Page filter item. This setup works with the [map data item example](configure-map-data-items.md).

<table id="table_drl_r1j_nkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter `Incident`.

</td></tr><tr><td>

Label

</td><td>

Enter `Incident`.

</td></tr><tr><td>

UI Type

</td><td>

Select **Single selection**.

</td></tr><tr><td>

Data type

</td><td>

Select the **data item**.

</td></tr><tr><td>

Application

</td><td>

Skip this field.

</td></tr><tr><td>

Data item

</td><td>

Select **Incident state**. **Note:** This data item is the map data item you created in the map data item example.

</td></tr><tr><td>

Data item table

</td><td>

Skip this field.**Note:** This field is automatically populated when a data item is selected.

</td></tr><tr><td>

Data item value field

</td><td>

Select **Value**.

</td></tr><tr><td>

Default value script

</td><td>

Skip this field.

</td></tr></tbody>
</table>## What to do next

Continue to the next task to [configure a map filter data mapping](set-up-map-filters.md#).

**Parent Topic:**[Create an advanced Map Page](create-advanced-map-page.md)

## Configure a map filter data mapping

Choose a Map Page for your map filter, and determine how it functions on the Map Page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Filters**.

2.  Select your map filter.

3.  On the Map Page Filter record, select your map filter item.

4.  On the Map Page Filter Item record, locate the Map Filter Data Mappings related list and select **New**.

5.  On the form, fill in the fields.

<table id="table_xks_j1m_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map page

</td><td>

Map Page where your map filter is applied.

</td></tr><tr><td>

Data item

</td><td>

Data item for your map filter data mapping. Select the data item that you previously configured.

</td></tr><tr><td>

Application

</td><td>

Optional application scope for your map filter data mapping.

</td></tr><tr><td>

Filter item

</td><td>

Filter item for your map filter data mapping. Select the filter item that you previously configured.**Note:** This field is automatically populated with the filter item.

</td></tr><tr><td>

Table

</td><td>

Table for your map filter data mapping. **Note:** This field is automatically populated when a data item is selected.

</td></tr><tr><td>

Field

</td><td>

Data is retrieved from this field in the table that you selected.

</td></tr></tbody>
</table>6.  Select **Submit**.


### Map Filter Data Mapping form

Select the options in the table to create your map filter data mapping. This setup works with the [map data item example](configure-map-data-items.md).

<table id="table_mpw_bmq_nkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Map page

</td><td>

Select the Map Page that you created.

</td></tr><tr><td>

Data item

</td><td>

Select **Incident** state.**Note:** This data item is the map data item that you created in the map data item example.

</td></tr><tr><td>

Application

</td><td>

Skip this field.

</td></tr><tr><td>

Filter item

</td><td>

Skip this field.**Note:** This field is automatically populated when a data item is selected.

</td></tr><tr><td>

Table

</td><td>

Skip this field.**Note:** This field is automatically populated with the Choice \[sys\_choice\] selection.

</td></tr><tr><td>

Field

</td><td>

Select **Value**.

</td></tr></tbody>
</table>### What to do next

Continue to the next task to [select your map filter](set-up-map-filters.md#), and complete the map filter setup.

## Select map filters

Select your map filter to complete the Map Page filter setup. This setup applies the map filter to your Map Page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Pages**.

2.  Select the Map Page that you want to apply your map filter to.

3.  Select the **Use advanced configuration** check box.

4.  In the **Filter** field, click the search icon \(![Search icon](../image/QueryIcon.png)\) and select the map filter that you created.

5.  Click the menu icon \(![Menu icon](../../workspace/image/menu-icon.png)\) and select **Save**.


### What to do next

You've set up your map filter. Continue to the [next task](set-up-map-filters.md#) to see that you have successfully created it.

## Check your map filter

Check to see that your map filter was successfully created in your Map Page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Map Page** &gt; **Map Pages**.

2.  Select your Map Page.

3.  Click **Try It**.

4.  In your Map Page, click **Filter**.

    Your map filter appears.

    ![Map filter](../image/ExampleMapFilter.png)


