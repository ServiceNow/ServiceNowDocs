---
title: List screen configuration
description: Configure a list screen so that your users can see a list of records from their mobile app. To access a record from the list, a user can tap the record name.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# List screen configuration

Configure a list screen so that your users can see a list of records from their mobile app. To access a record from the list, a user can tap the record name.

## Before you begin

Role required: admin or delegated developer

## About this task

Create a simple list screen with a single data source, single segment, default filters, and an optional embedded record screen. When creating a list screen, you can automatically generate all downstream records you need by populating the list name, data item, and card.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then select **New**.

4.  Select the **List** option in the Create a screen page, and then select **Continue**.

    ![blank list screen creation record](../image/mab-list-screen-creation.png "New list screen creation screen")

5.  Complete the fields as needed; the associated records are automatically generated for you based on the inputs you provide.

    |Field|Description|
    |-----|-----------|
    |**General settings**|
    |Name|The name of your list screen. This name appears as a tile in the mobile application.|
    |Description|Additional information about your list screen.|
    |Hide screen name|Option to determine whether the screen name isn’t shown as the screen header. This is useful if the text already appears in the header name or if it doesn’t provide any value to the user.|
    |Hide filters|Option to prevent the list from displaying a list filter.|
    |**Content settings**|
    |Data and filtering|Choose or create a data item to determine what information is displayed on your screen.|
    |Card layout and fields|Choose or create a card to determine how information is displayed on your screen.|
    |Functionality|
    |Destination screen|Option to have an embedded record details screen created. This screen is accessed by tapping on an item in the list.|

6.  Select **Create**.

    All necessary downstream records are automatically generated for you and you’ll be taken to the list screen record configuration form. Optional configuration options are available under the **Advanced settings** section.

    **Note:** Selecting **Cancel** takes you back to the **Screens** selection page.

    Automatically generated records are marked with a blue spark icon in the configuration tree.

    ![three generated records with a blue spark next to them](../image/mab-generated-records-icon.png "Generated record icons")

7.  Edit fields or fill in additional ones for your list screen.

    |Field|Description|
    |-----|-----------|
    |**General settings**|
    |Name|The name of your list screen. This name appears as a tile in the mobile application.|
    |Description|Additional information about your list screen.|
    |Available offline|Option to determine whether the screen is available in offline mode or not.|
    |Hide screen name|Option to determine whether the screen name isn’t shown as the screen header. This is useful if the text already appears in the header name or if it doesn’t provide any value to the user.|
    |Hide filters|Option to prevent the list from displaying a list filter.|
    |**Screen segments**|
    |Screen segments|Configure additional screen segments for the list screen.|
    |Advanced settings|
    |Icon|Icon used to represent your list screen when added to a launcher screen.|
    |Custom filter|Option to add a custom filter for filtering record types by category.|
    |Empty state|Configure what displays in an empty space when no data is available to show.|
    |Top menu function instances|Option to determine whether to use top menu functions to display additional options.|
    |Footer function instances|Option to determine whether to use footer functions to display additional options.|
    |Input form screen|Create an input form screen that determines what records show up on your list screen based on user input.|
    |UI parameters \(legacy\)|Change how a field or UI element behaves.|
    |Dynamic screen title|Allows you to create an element and map it to a UI parameter. Use it to pass a value from one screen to another and include it in the title of the destination screen.|
    |Role access|Determine which user roles can access this screen. If you have selected no roles, users with any role will have access to the screen. |

8.  Select **Save**.


## Result

List screen primary screen

![List screen.](../image/mobile-list.png "Created list screen")

## What to do next

-   **Use embedded screens within your list screen**- List screens can be configured to include record screens. Adding an embedded screen enables users to tap on a record, the contents of which are displayed in a new screen. As an admin, you configure this option in the List item config record. For more information, see [Configure a record screen for use with a list screen](sg-configure-form-applet.md).
-   **Configure mobile functions for your list screen** - The List screen can include top menu functions and footer functions to determine the type of action users can perform on a list screen. As an admin, you configure this option in the List screen record. For more information see, [Mobile functions](../concept/sg-studio-mobile-button-types.md) and [Associate a function with a location in the app](../reference/sg-studio-button-instances.md).
-   **Configure role access for records in your list screen** - Use the role access option to configure the records in your list screen to only display to selected roles. As an admin, you configure this option in the List screen record.

