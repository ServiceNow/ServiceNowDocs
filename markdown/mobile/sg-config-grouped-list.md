---
title: Configure a group list screen
description: Create a group list to provide a view of a list of records grouped by a field you specify.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Grouped list screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a group list screen

Create a group list to provide a view of a list of records grouped by a field you specify.

## Before you begin

Before you can create a group list screen, you must create a data item with a group configuration. For more information on configuring a data item, see [Configure a standard data item](sg-studio-create-data-item.md), and note the optional steps for setting the **Group by** field.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the **List** option in the Create a screen page, and then select **Continue**.

5.  Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|The name of your list screen. This name appears as a tile in the mobile application.|
    |Description|Additional information about your list screen.|
    |**Screen Settings**|
    |Available offline|Option to determine whether the screen is available in offline mode or not.|
    |Hide screen name|Option to determine whether the screen name is not shown as the screen header. This is useful if the text already appears in the header name or if it does not provide any value to the user.|
    |Hide filters|Option to prevent the list from displaying a list filter.|
    |Icon|Icon used to represent your list screen when added to a launcher screen.|
    |Custom filter|Option to add a custom filter for filtering record types by category.|
    |Empty state|Configure what displays in an empty space when no data is available to show.|
    |Screen segments|Configure additional screen segments for the list screen.|
    |Top menu function instances|Option to determine whether to use top menu functions to display additional options.|
    |Footer function instances|Option to determine whether to use footer functions to display additional options.|
    |UI parameters|Change how a field or UI element behaves.|
    |Dynamic screen title|Allows you to create an element and map it to a UI parameter. Use it to pass a value from one screen to another and include it in the title of the destination screen.|
    |Role access|Determine which user roles can access this screen. If you have selected no roles, users with any role will have access to the screen. |

6.  In the **Icon** section add an icon.

    This icon displays in the launcher screen when you add it to your group list screen.

7.  In the **Screen segments** section, select **New**.

8.  Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|Name for the screen segment screen.|
    |Order|The order in which the segment appears on the screen. Segments display from the lowest to the highest value.|
    |Screen|Displays the list name from the list screen record.|
    |Max number of offline rows|The number of rows displayed for offline viewing.|
    |Streams|Records that connect data items and list item config records to the list screen.|
    |**Interleave sort**|
    |Sort list stream interleave field|Determine whether the list stream interleave field is sorted in ascending or descending order.|

9.  In the **Streams** section, select **New**.

10. Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|Name for the stream.|
    |Table|Choose the relevant table that contains data to display in your list.|
    |Interleaved field|Select the field you want to use to interleave your data item.|
    |Data item|Data items are queries on a selected table that provide the data presented in a screen.|
    |List item config|Determine how each record appears and the actions associated with it.|

11. In the **Data Item** section choose an existing data item for a grouped list, and then select **Apply**.

12. In the **List item config** section, select **New**.

13. Complete the fields as needed.

<table id="table_kzs_gmh_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the list item config.

</td></tr><tr><td>

Settings - List item config order

</td><td>

The order in which this list item config will render when multiple list item configs are connected to a list stream.

</td></tr><tr><td>

Data

</td><td>

The table associated with your data item.

</td></tr><tr><td>

Conditions

</td><td>

The conditions that determine what is shown if there are multiple list item configs in a list stream.

</td></tr><tr><td>

View using

</td><td>

How the list item config can be viewed.

</td></tr><tr><td>

Card / Legacy card

</td><td>

Cards visually display information from different records.

</td></tr><tr><td>

On tap

</td><td>

Determines how the mobile app responds to a tap on the screen. Select **Use a function instance**.

</td></tr><tr><td>

On tap function instance

</td><td>

Determine what actions appear when a user taps on a list item.

 Select a navigation function or select **New** to create one. For more information about creating a navigation function, see [Navigation functions](../concept/mobile-nav-functions.md).

 **Note:** This option only appears when **Use a function instance** is selected for **On tap**.

</td></tr><tr><td>

Embedded screen

</td><td>

Not a valid option for a group list screen.

 **Note:** This option only appears when **Navigate to screen** is selected for **On tap**.

</td></tr><tr><td>

Leading swipe function instances

</td><td>

Determines the actions performed or that appear when a user initiates a swipe gesture from the front of a list item.**Note:** This function type can't be used on a grouped list.

</td></tr><tr><td>

Trailing swipe function instances

</td><td>

Determines the actions performed or that appear when a user initiates a swipe gesture from the back of a list item.**Note:** This function type can't be used on a grouped list.

</td></tr></tbody>
</table>14. In the **Data** section, select the same table used in the **Data item** section within the list stream record.

15. In the **Card** section, select **Choose** to use an existing card or select **New** to create one.

16. Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the new card.|
    |Description|Additional information about the card.|
    |Active|Select whether the card record is active or not.|
    |Data|The table associated with your data item.|
    |Card template|The layout of UI elements used within the card.|
    |UI rules|The UI rule associated with this card.|

17. In the **Card template** field, select **Choose**.

18. Search for the item **Grouped List**and select **Apply**.

    **Note:** The Grouped List card template is a default template from the base system.

19. Return to the list item config record by selecting it from the configuration tree.

20. In the **On tap** section, select **Use a function instance**.

    The On tap function instance displays.

21. In the **On tap function instance** section, select **New** to determine what actions appear when a user taps on a list item.

22. Complete the fields as needed.

<table id="table_wlv_ynr_qwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

Name for the new function instance.

</td></tr><tr><td>

Description

</td><td>

Additional information about the function instance.

</td></tr><tr><td class="sub-head" colspan="2">

**Settings**

</td></tr><tr><td>

Display label

</td><td>

Label that is visible to end users.

</td></tr><tr><td>

Order

</td><td>

The order which the function instance appears on the card. Function instances display from the lowest to the highest value.

</td></tr><tr><td>

Active

</td><td>

Select whether the function instance record is active or not.

</td></tr><tr><td>

Disable offline

</td><td>

Option to determine whether the function instance record is available in offline mode or not.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your function when added to this function instance record.

</td></tr><tr><td colspan="2">

**Function placement**

</td></tr><tr><td>

Parent table

</td><td>

The parent table that the function instance applies to.**Note:** This field is automatically populated.

</td></tr><tr><td>

Parent

</td><td>

The parent of the function instance to which the list item config applies.**Note:** This field is automatically populated.

</td></tr><tr><td>

Location

</td><td>

The location of the function on your mobile screen.**Note:** This field is automatically populated.

</td></tr><tr><td>

Function

</td><td>

The function used within this function instance.

</td></tr></tbody>
</table>23. In the **Function** section, select **Choose** to use a function or select **New** to create one.

    For more information on mobile functions, see [Mobile functions](../concept/sg-studio-mobile-button-types.md).

24. Select **Save**.


## Result

You now have an screen displaying a list of records, grouped by the field you defined in your data item.

![Group list screen with items from the incident table grouped by category.](../image/GroupedListApplet.png "Group List screen")

