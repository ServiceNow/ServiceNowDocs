---
title: Configure a record UI section
description: Use the record UI section type to display records from a selected list as cards with important information. These cards enable users to access your record screens. Select how you want to represent this option visually.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Launcher screen UI sections, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a record UI section

Use the record UI section type to display records from a selected list as cards with important information. These cards enable users to access your record screens. Select how you want to represent this option visually.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  From the **Record type** field, select **UI Section \[sys\_sg\_section\]**, and then select **New**.

5.  From the Create a section dialog box, select **Record section** and then select **Continue**.

6.  Complete the following fields as needed.

    |Field|Description|
    |-----|-----------|
    |**Properties**|
    |Title|Name for the record UI section.|
    |Active|Toggle that sets whether the record section is available or not.|
    |**Settings**|
    |Hide header|Header of this UI section is hidden when this field is enabled. When enabled, the title and the **See all** button are both hidden.|
    |Display title|Title of the section is visible. This option is available only when the header is visible. The title of the section comes from the title of your record section.|
    |Hide "See all" button|The **See all** button within the header is hidden when this field is enabled. This field is available only when the header is visible.|
    |Orientation|Orientation of the record section. You can select either**Horizontal** or **Vertical** based on the amount of space available on your screen.|
    |Hide section if empty|Option for hiding empty UI sections when there's no content to display.|
    |Max items display count|Maximum number of cards that are displayed on the launcher screen. Enter a number in this field. If the number of available records in the destination screen exceed the number set in this field, users must tap **See all** in the header to see the remaining records.|
    |Destination screen|Destination screen determines which records are displayed as cards in the record section. Selecting the card enables you to navigate to the record screen for a record. Selecting **See all** displays the full list screen that you selected for your destination screen.|
    |Role access|User roles that can access this UI section. This field is an optional setting.|

7.  Select **Save**.


## What to do next

After creating record UI sections, you must add the UI sections to a launcher screen so they're displayed. For more information, see [Add a UI section to the launcher screen](ui-section-to-launcher-screen.md).

