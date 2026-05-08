---
title: Add a button to your mobile web screen that launches Virtual Agent
description: Admins can configure a button on a mobile web screen that end users can use to launch Virtual Agent from their mobile device.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile web screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Add a button to your mobile web screen that launches Virtual Agent

Admins can configure a button on a mobile web screen that end users can use to launch Virtual Agent from their mobile device.

## Before you begin

Role required: admin

## About this task

To add a button to your mobile web screen, you must use UI Builder. For more information, see UI Builder.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Search for your mobile web screen and select it to open it.

3.  In your mobile web screen UXF page, under **Data and scripts**, select **Add data resource**.

4.  In the Select a data resource dialog box, search for `Mobile app bridge`, select it, and then select **Add**.

5.  In the region of the mobile web screen where you want to add the button that launches Virtual Agent, select the plus sign to add a component.

    ![UI Builder shown where you can select the plus sign.](../image/mobwebscre-add-va.png)

6.  Select the **Component** you want to use to launch Virtual Agent in the mobile web screen.

    For example, if you want to add a button that users can select to launch Virtual Agent, select **Components** and then select **Button**.

    ![UI Builder dialog box where you can select a button component.](../image/mobwebscre-select-button.png)

7.  Select the button in your mobile web screen UXF page to configure the component in the menu on the side of the screen:

    1.  Select **Configure** to add a **Label** for the button, such as `Virtual Agent`.
    2.  Select **Events** to connect the button to the API method that launches Virtual Agent.
    3.  In the Events menu, select **Add handler**.
    4.  In the Choose a handler dialog box, scroll down to **Mobile app bridge**, and select **LAUNCH CHAT**.
    5.  Select **Continue**, and then select **Add**.
8.  Select **Save** to save your configuration.


## What to do next

In your mobile web screen on your device, refresh the mobile app to display the button you added for Virtual Agent.

**Parent Topic:**[Mobile web screen](../concept/url-screen.md)

