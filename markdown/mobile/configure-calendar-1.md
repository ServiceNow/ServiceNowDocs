---
title: Configure a calendar screen
description: Create a screen that displays a calendar with a list of related records. Users can see which records are related to dates on the calendar.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Calendar screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a calendar screen

Create a screen that displays a calendar with a list of related records. Users can see which records are related to dates on the calendar.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the **Calendar** option in the Create a screen page, and then select **Continue**.

5.  Complete the fields as needed.

<table id="table_stg_jtg_wwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Properties**

</td></tr><tr><td>

Name

</td><td>

The name of your calendar screen. This name appears as a tile in the mobile application.

</td></tr><tr><td>

Description

</td><td>

Additional information about your calendar screen.

</td></tr><tr><td class="sub-head" colspan="2">

**Settings**

</td></tr><tr><td>

Fetch type

</td><td>

Control when the data is loaded onto the screen. Select the On-demand option for optimum load time performance. For more information, see [Mobile fetch types](../reference/applet-fetch-types.md).

</td></tr><tr><td>

Hide screen name

</td><td>

Option to determine whether the screen name isn't shown as the screen header. This option is useful if the text already appears in the header name or if it doesn't provide any value to the user.

</td></tr><tr><td>

Hide filters and sorting

</td><td>

Option to prevent the calendar screen list from displaying a list filter.

</td></tr><tr><td>

Icon

</td><td>

Icon used to represent your calendar screen when added to a launcher screen.

</td></tr><tr><td>

Custom filters

</td><td>

Option to determine the fields that users can filter by. Use this option to help users find the events that they need.Users can bookmark the selected filters for future reference, by selecting the bookmark icon. For more information, see [Mobile list screen filters](../concept/mobile-list-filters.md).

</td></tr><tr><td>

Screen segments

</td><td>

Configure a screen segments for the calendar screen. Use it to add the calendar element within the screen.

</td></tr><tr><td>

Quick action function action instances

</td><td>

Option to create a quick action button to display directly on the user’s calendar screen. This button helps your users to access commonly used functions, such as transferring records or using a template in the mobile app. After the user taps this button, they have the option to create a new event.If a single quick action function is configured, the user is navigated to the event as defined by you.

If more than one quick action function is configured, a menu from the bottom displays and the user selects the relevant event. For example, create a new incident or create a work order task.

For more information, see [Quick actions](sg-config-quick-actions.md).

**Note:** Quick action function instances can’t be reused so you must configure a new one. However, you can use an existing function to configure your quick action function instance.

</td></tr><tr><td>

Top menu function instances

</td><td>

Option to determine whether to use top menu functions to display additional options.Use the top menu function location for less frequently used actions. You can also use the option on forms when you have more actions listed than conveniently fit in the footer. For more information, see [Use your navigation function as a top menu selection](sg-launcher-navigation-example-3.md).

</td></tr><tr><td>

Input form screen

</td><td>

Option for a calendar screen to display content from a record. For example, the user selects a contact from a menu in a preconfigured input form screen. After tapping this option, the calendar screen opens with filtered data for the selected contact.For more information, see [Input form screen](../concept/parameter-input-screen.md).

</td></tr><tr><td>

UI parameters \(legacy\)

</td><td>

Optional configuration that affects how a field or UI element behaves. Use UI parameters to determine how a value can be entered or whether it's automatically populated for the UI element, based on the end user's action.

</td></tr><tr><td>

Role access

</td><td>

Determine which user roles can access this screen. If you've selected no roles, users with any role will have access to the screen. 

</td></tr></tbody>
</table>6.  In the Icon section, either select an existing icon or create an icon.

    This icon represents the calendar screen in a launcher screen. For more information about creating icons, see [Mobile icons](../reference/sg-mobile-icon.md).

7.  In the Quick action functions instance area, either select an existing function instance or create a new one.

    You can create more than one quick action function instance. For more information see, [Quick actions](sg-config-quick-actions.md).

    **Note:** The quick action button is an effective way for users to add events to the calendar.

8.  In the **Screen segments** section, select **New** to create a segment used for the stream displayed within the calendar.

9.  Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|Name for the screen segment screen.|
    |Order|The order in which the segment appears on the screen. Segments display from the lowest to the highest value.|
    |Screen|Displays the calendar name from the calendar screen record.|
    |Max number of offline rows|The number of rows displayed for offline viewing.|
    |Streams|Records that connect data items and list item config records to the list screen.|
    |**Interleave sort**|
    |Interleave sort|Determine whether the list stream interleave field is sorted in ascending or descending order.|

10. In the **Streams** section, select **New**.

11. Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Name|Name for the calendar event stream.|
    |**Data**|
    |Table|Choose the relevant table that contains the data you want your calendar event stream to display.|
    |Start date field|Select which field in the selected table contains the start date information for your calendar items.|
    |End date field|Select which field in the selected table contains the end date information for your calendar items.|
    |Interleaved field|Select the field that sorts the event stream containing your data items. If you don't select a field, the data items are separated by source.|
    |Data item|Data items are queries on a selected table that provide the data presented in a screen.|
    |List item config|Determine how each record appears and the actions associated with it.|

12. In the **Data** section, complete the following fields:

    1.  **Table** - Select a table that contains the data you want your calendar event stream to display.
    2.  **Start date field** - Select a field from your chosen table to contain the start date information for your calendar items.
    3.  **End date field** - Select a field from your chosen table to contain the end date information for your calendar items.
    4.  \(Optional\) **Interleaved field** - Select the field that sorts the event stream containing your data items. If you don't select a field, the data items are separated by source.
13. In the **Data Item** section, select **New** to create a data item for your calendar event stream, or select **Choose** to reference an existing data item.

    The data items displayed corresponds to the data table that you selected from the **Table** field in the Calendar event stream record. For more information on creating data items, see [Configure a standard data item](sg-studio-create-data-item.md).

14. In the **List item config** section, select **New**, to ensure a visual display appears on your mobile device, or select **Choose** to reference an existing list item config.

15. Complete the fields as needed.

<table id="table_vtg_jtg_wwb"><thead><tr><th>

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

The order in which this list item config renders when multiple list item configs are connected to a list stream.

</td></tr><tr><td>

Data

</td><td>

The table associated with your data item.**Note:** The table used in this record should match the entry in the **Table** field from the calendar event stream record.

</td></tr><tr><td>

Conditions

</td><td>

The conditions that determine what is shown if there are multiple list item configs in a list stream.

</td></tr><tr><td>

View using

</td><td>

How the list item config is viewed.

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

Option to add an embedded screen within a list screen.

 **Note:** This option only appears when **Navigate to screen** is selected for **On tap**.

</td></tr><tr><td>

Leading swipe function instances

</td><td>

Determines the actions performed or appears when a user initiates a swipe gesture from the front of a list item.

</td></tr><tr><td>

Trailing swipe function instances

</td><td>

Determines the actions performed or appears when a user initiates a swipe gesture from the back of a list item.

</td></tr></tbody>
</table>16. In the **On tap** field, select the Use a function instance option.

17. In the **Data** section, select the same table used in the **Table** field within the calendar event stream record.

18. In the View using section, select the **Card** option.

    **Note:** The legacy card option is also available, however legacy cards don't have the same capabilities as regular cards.

19. In the **Card** section, select **Choose** to use an existing card or select **New** to create a card.

20. Complete the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the new card.|
    |Description|Additional information about the card.|
    |Active|Select whether the card record is active or not.|
    |Data|The table associated with your data item.|
    |Card template|The layout of UI elements used within the card.|
    |UI rules|The UI rule associated with this card.|

21. In the **Data** section, select the table that contains the data you want to populate on your card.

22. In the **Card template** field, select **Choose** to reference an existing card template.

23. Select **Save**.

24. To customize elements and attributes of your card, do the following:

    1.  Select the Open in Mobile Card Builder button.

        The Mobile Card Builder tool displays in a new tab.

    2.  Make any required changes to your incident list card. For more information about working with Mobile Card Builder, see [Mobile Card Builder](../concept/mobile-card-builder.md).
    3.  Select **Save**.
25. Select **Save**.


