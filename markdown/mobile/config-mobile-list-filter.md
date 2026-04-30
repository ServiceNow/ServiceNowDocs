---
title: Configure a custom filter
description: Manually create a filter experience for your users. Custom filters can include fields that are not in the list pattern.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Mobile list screen filters, List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a custom filter

Manually create a filter experience for your users. Custom filters can include fields that are not in the list pattern.

## Before you begin

Role required: admin

## About this task

This procedure can be used to configure a custom filter for list screens and map screens. The following information applies to list screens, but the same settings are available to configure custom filters for map screens in Mobile App Builder as well.

For information about configuring map screens, see [Configure a map screen](sg-configure-map-screen.md).

**Note:** By default, there are filters that are based on the fields which are displayed in mobile views.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category and select the list screen where you want to configure a custom filter.

4.  In the List Screen form, scroll down to the **Screen Settings** section and verify that the **Hide filters** toggle is turned off.

    **Note:**

    -   Turning off the **Hide filters** toggle makes sure that filters are visible in your app.
    -   Enabling filters also enables sorting functionality for list and map screens.
5.  In the List Screen form, scroll down to the **Custom filter** section and select **New**.

6.  In the Filter form, complete the fields as needed.

<table id="table_evb_5bv_lwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Name of the filter. Enter a unique name. This name is not displayed to users when they filter content.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the filter that helps you identify it.

</td></tr><tr><td>

Active

</td><td>

Toggle that determines whether the filter is operating. Turn it on to activate the filter.

</td></tr><tr><td>

Filter categories

</td><td>

Filter categories help users to filter records by specific item streams. At least one filter category must be defined to enable the custom filter.

 Select **New** to configure a filter category.

</td></tr></tbody>
</table>7.  In the Filter Category form, create filter categories to help users filter records by specific list streams by completing the fields as needed.

    **Note:** At least one filter category must be defined for the custom filter to work.

    |Field|Description|
    |-----|-----------|
    |Properties|
    |Name|Name for the filter category. Enter a unique name. This name is not displayed to users when they filter content.|
    |Label|Name of the filter category that displays on the device to users when they filter content.|
    |Description|Enter a description of the filter category that helps you identify it.|
    |Active|Toggle that determines whether the filter category is operating. Turn it on to activate the filter category.|
    |Data|
    |Table|The table that is the target of the filter category. Select a table from the drop-down list.|
    |Filter conditions|Filter conditions determine which fields users can filter on. Select **New** to configure a filter condition.|

8.  In the Filter Condition form, complete the following fields as needed to create filter conditions to help users filter information on a screen after they set their preferred filtering criteria.

    **Note:** At least one filter condition or one item sorting must be defined for the custom filter to work.

<table id="table_akj_lgv_lwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Properties

</td></tr><tr><td>

Name

</td><td>

Name for the filter condition. Enter a unique name. This name is not displayed to users when they filter content.

</td></tr><tr><td>

Label

</td><td>

Name of the filter condition that displays on the device to users when they filter content. From the end user's perspective, this is the filtered field.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the filter condition that helps you identify it.

</td></tr><tr><td>

Active

</td><td>

Toggle that determines whether the filter condition is operating. Turn it on to activate the filter condition.

</td></tr><tr><td>

Condition type

</td><td>

**Condition type** sets the data type of the database field on which you want to filter. **Condition type** requires two attributes:

 -   Operator attributes, which determine how the filter operates on the data.
-   Display Type attributes, which determine how the data that is returned by the Operator attribute gets displayed in your mobile app.
 Select one of the Condition types from the drop-down list. See [Filter condition attributes](../reference/filter-condition-attributes.md) where the default Operator and Display Type attributes are listed for each Condition type. The default values are marked with an asterisk \(\*\).

 **Note:** If your requirements are satisfied with the default attributes and values, then you don't need to configure attributes any further. Selecting the **Condition type** is all you need to do. If you need to customize your filtering options, you can configure them in Step 10 below.

</td></tr><tr><td>

Filter condition fields

</td><td>

The database fields that users can filter on. Select **New** to configure a filter condition field.

</td></tr></tbody>
</table>9.  In the Filter Condition Field form, create filter condition fields to determine which fields users can filter on by completing the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |Properties|
    |Name|Name of the filter condition field. Enter a unique name. This name is not displayed to users when they filter content.|
    |Description|Enter a description of the filter condition that helps you identify it.|
    |Data|
    |Table|The table that contains the field which you want users to be able to filter on. This field should be pre-filled with the table you chose for the filter category in Step 7.|
    |Field|The field that you want users to be able to filter on. Select a field from the drop-down list.|

10. To configure filter condition attributes, navigate back to the Filter Condition form by selecting it in the navigation menu, scroll down to the **Filter condition attributes** section, and then select **New**.

    In the Filter Condition Attribute form, complete the fields as needed based on the **Condition type** that was set in Step 8. See [Filter condition attributes](../reference/filter-condition-attributes.md) for descriptions of all attributes and their values.

11. Add additional filters by repeating Steps 5 through 12 as needed.

12. Select **Save**.


