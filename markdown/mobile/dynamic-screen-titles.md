---
title: Configure a dynamic screen name for a list screen
description: Configure a screen to dynamically inherit a name from a parametrized list screen. This setup enables users to view a passed parameter as the screen name instead of the screen record name.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [List screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure a dynamic screen name for a list screen

Configure a screen to dynamically inherit a name from a parametrized list screen. This setup enables users to view a passed parameter as the screen name instead of the screen record name.

## Before you begin

Role required: admin

## Procedure

1.  In the web-based UI, enter `sys_sg_screen.list` in the filter navigator.

2.  Select a list screen to inherit the dynamic screen name.

3.  Apply an existing UI parameter in the UI parameter related list.

    1.  If the **UI parameters**, **Screen UI element mappings**, and **Source and UI element** related lists are not displayed, add them by clicking the Additional actions icon \(![Additional actions icon.](../image/context-menu-icon.png)\). Then, select **Configure** &gt; **Related Lists**, and then select the required related lists.

    2.  Click the **UI parameters** tab.

    3.  Select an existing UI parameter.

    4.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Parameter type|Screen|
        |Input source|User input|
        |Input type|Text|

    5.  Click **Submit**.

4.  Define a UI element to serve as the location point of the dynamic screen name.

    **Note:** This step is a one-time configuration. Once you create the UI element, a new record for the screen title location is not required.

    1.  In the web-based UI, enter `sys_sg_ui_element.list` in the filter navigator.

    2.  Click **New** to create a new UI element.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Location|Location where the dynamic screen name displays. Select **Title**.|
        |Name|Name of the UI element.|

    4.  Click **Submit**.

5.  Create a screen UI element and map it to the screen type.

    1.  Click the **Screen UI element mappings** tab.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Screen|Auto-populated with the selected screen, which inherits the dynamic screen parameter.|
        |UI Element|The UI element to be configured.|

    4.  Click **Submit**.

6.  Map the screen UI element with the UI parameter.

    1.  Click the **Source and UI element** tab.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |UI Element|The UI element to display the dynamic screen name.|
        |Source Table|The UI Parameter table.|

    4.  Click **Submit**.


## Result

The screen name dynamically inherits a value from the redirection parameter.

![Dynamic screen name displayed from redirection parameter.](../image/dynamic-name-redirection-parameter.png "Dynamic screen name displayed from the redirection parameter")

