---
title: Configure sorting capabilities within mobile filters
description: Use the sorting option in lists and maps to help users organize their filtered results and enable them to view the most relevant information. Examples of configurable sorting options are: recently added, assigned to \(ascending\), assigned to \(descending\), and highest priority first.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mobile list screen filters, List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure sorting capabilities within mobile filters

Use the sorting option in lists and maps to help users organize their filtered results and enable them to view the most relevant information. Examples of configurable sorting options are: recently added, assigned to \(ascending\), assigned to \(descending\), and highest priority first.

## Before you begin

A sorting option entitled Default always displays at the top of the sorting list. The values of the default sorting are defined using the **Add sort** and **Sorted by** fields within a data item. See, [Configure a standard data item](sg-studio-create-data-item.md). If values are not defined within a data item, the default sorting definitions of the instance are taken from the web-based platform definition.

Role required: admin

## About this task

By default, when creating item sorting, the instance creates an ascending and descending variant of the item sorting. Each of these entries contains the text "\(Ascending\)" and "\(Descending\)" next to the sorting entry. To change the default display option, see [Configure sorting display options for mobile filters](list-filter-sorting-attributes.md).

**Note:** Filters and sorting options use the same defined categories, as defined by item views and cards.

## Procedure

1.  Create an item sorting to add fields to a list.

    1.  In the web-based UI, enter `sys_sg_item_sorting.list` in the filter navigator.

    2.  Select **New**.

    3.  On the Item Sorting form, fill in the fields.

        1.  **Name**: Enter a title for the item sorting.
        2.  **Type**: Select the reference lookup icon \(![Reference lookup icon](../image/reference-lookup-icon.png)\) and select a filter type from the list.
        3.  **Label**: Enter a name for the sorting option displayed to the user in the sorting list.
    4.  Right-click in the header and select **Save**.

2.  Create an item sorting field, to create a relationship between the item sorting field and the item sorting.

    1.  Click the **Item Sorting Fields** tab in the **Item Sorting** form.

    2.  Select **New**.

    3.  On the Item Sorting Field form, fill in the fields.

        1.  **Name**: Enter a title for the item sorting field.
        2.  **Table**: Select a table which contains data to sort.
        3.  **Field**: Select the element from the tree which relates to the selected table.
        4.  **Item Sorting**: This field defaults to the item sorting name you created earlier.
    4.  Click **Submit**.

3.  Repeat step 2 to display additional sorting options.

    **Note:** To change the sorting display attributes, see [Configure sorting display options for mobile filters](list-filter-sorting-attributes.md).

4.  Add a filter category that contains your item sorting.

    1.  In the filter navigator, enter `sys_sg_filter_category.list`.

    2.  Select **New**.

    3.  On the Filter Category form, fill in the fields.

        1.  **Name**: Enter a title for the filter category field.
        2.  **Label**: Enter a name for the filter category displayed to the user.
        3.  **Table**: Select the same table you defined in the Item Sorting Fields form.
    4.  Right-click in the header and select **Save**.

5.  Create a many-to-many relationship to connect the category and the item sorting.

    1.  Select the **Item Sorting** tab within the **Filter Category** form.

    2.  Select **New**.

    3.  In the **Item Sorting** field within the Filter Category M2M Item Sorting form, select the reference lookup icon and select the item sorting you created.

    4.  Select **Submit**.

6.  Define a filter that contains the item sorting.

    1.  In the filter navigator, enter `sys_sg_filter.list`.

    2.  Select **New** in the Filters form.

    3.  In the **Name** field in the Filter form, enter a name for the filter.

    4.  Right-click in the header and select **Save**.

7.  Create a many-to-many relationship to connect the filter and the filter category.

    1.  Select **New** in the **Filter M2M Filter Categories** area of the Filter form.

    2.  In the **Filter Category** field within the Filter M2M Filter Category form, select the reference lookup icon and select the filter category you created.

    3.  Select **Submit**.

8.  Assign the created filter with the item sorting, to either a list screen or a map screen.

    1.  In the filter navigator, enter:

        -   For a list screen - `sys_sg_list_screen.list`
        -   For a map screen - `sys_sg_map_screen.list`
    2.  In the **Name** field, search for the screen where you want to add the filter.

    3.  Select the required screen and in the form, perform the following:

        1.  In the **Filter** field, select the reference lookup icon and select the filter you created.
        2.  Make sure that the **Hide filter and sorting** field is cleared.
    4.  Select **Update**.


## Result

Your filter sorting configuration may look like the one in the image. Each item sorting has an ascending and descending sorting option associated with it. To change the default display options, see [Configure sorting display options for mobile filters](list-filter-sorting-attributes.md).

![Mobile filter item sorting menu with default setup.](../image/mobile-filter-sort-menu.png)

