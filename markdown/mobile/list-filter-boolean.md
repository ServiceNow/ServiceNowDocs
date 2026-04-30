---
title: Add Boolean fields within a mobile filter
description: Add Boolean fields, such as 'Active: Yes / No', within mobile filters, so users can more easily search for specific data and streamline their results.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile list screen filters, List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Add Boolean fields within a mobile filter

Add Boolean fields, such as 'Active: Yes / No', within mobile filters, so users can more easily search for specific data and streamline their results.

## Before you begin

Role required: admin

## Procedure

1.  Create a filter condition field.

    1.  In the web-based UI, enter `sys_sg_filter_condition_field.list` in the filter navigator.

    2.  Select **New**.

    3.  On the Filter Condition Field form, fill in the fields.

        1.  **Name**: Enter a title for the filter condition field.
        2.  **Table**: Select a table which contains the data to filter.
        3.  **Field**: Select a Boolean type field from the list.
    4.  Select **Submit**.

2.  Create a filter condition to group the filter condition fields. For example, choose an incident table and a Boolean-type field to filter based on whether incidents are active or inactive.

    **Note:** You need this element even if only one filter condition field exists.

    1.  In the filter navigator, enter `sys_sg_filter_condition.list`.

    2.  Select **New**.

    3.  On the Filter Condition Form, fill in the fields.

        1.  **Name**: Enter a title for the filter condition field.
        2.  **Type**: Select the reference lookup icon \(![Reference lookup icon](../image/reference-lookup-icon.png)\) and select `Boolean` from the list.
        3.  **Label**: Enter a name for the Boolean filter displayed to the user.
    4.  Right-click in the header and select **Save**.

3.  Create a many-to-many relationship to connect the filter condition and the filter condition field.

    1.  Select the **Filter Conditions Fields** tab within the **Filter Condition** form

    2.  Select **New**.

    3.  In the **Filter Condition Field** field within the Filter Condition M2M Filter Condition Field form, select the reference lookup icon and select the filter condition field you created.

    4.  Select **Submit**.

4.  Add a filter category to display at the top of your filter screen.

    1.  In the filter navigator, enter `sys_sg_filter_category.list`.

    2.  Select **New**.

    3.  On the Filter Category Form, fill in the fields.

        1.  **Name**: Enter a title for the filter category field.
        2.  **Label**: Enter a name for the filter category to display to the user.
        3.  **Table**: Select the same table you defined in the Filter Condition Field Form.
    4.  Right-click in the header and select **Save**.

5.  Create a many-to-many relationship to connect the category and the filter condition.

    1.  Select the **Filter Conditions** tab within the Filter Category form.

    2.  Select **New**.

    3.  In the **Filter Condition** field within the Filter Category M2M Filter Condition form, select the reference lookup icon and select the filter category you created.

    4.  Select **Submit**.

6.  Define a filter that contains the filter category.

    1.  In the filter navigator, enter `sys_sg_filter.list`.

    2.  Select **New** in the Filters form.

    3.  In the **Name** field of the Filter form, enter a name for the filter.

    4.  Right-click in the header and select **Save**.

7.  Create a many-to-many relationship to connect the category and the filter.

    1.  Select **New** in the **Filter M2M Filter Categories** area of the Filter form.

    2.  In the **Filter Category** field within the Filter M2M Filter Category form, select the reference lookup icon and select the filter category you created.

    3.  Select **Submit**.

8.  Assign the created filter with a Boolean field, to either a list screen or a map screen.

    1.  In the filter navigator, enter either `sys_sg_list_screen.list` or `sys_sg_map_screen.list`.

    2.  In the **Name** field, search for the screen where you want to add the filter.

    3.  Select the required screen and in the form perform the following:

        1.  In the **Filter** field, select the reference lookup icon and select the filter you created.
        2.  Make sure that the **Hide filter and sorting field are** cleared.
    4.  Select **Update**.


