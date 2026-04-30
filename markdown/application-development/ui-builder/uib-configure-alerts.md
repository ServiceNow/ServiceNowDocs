---
title: Configure alerts to auto-dismiss
description: Set alerts to automatically clear after a specified time period.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-08-19"
reading_time_minutes: 2
keywords: [UI Builder, alert, auto-dismiss, notifications]
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Configure alerts to auto-dismiss

Set alerts to automatically clear after a specified time period.

## Before you begin

Role required: ui\_builder\_admin

## About this task

You can configure alerts to auto-dismiss in two ways:

-   Experience settings: apply auto-dismiss rules to all alerts of a specific type
-   Events: add an event to override experience settings for specific alerts

**Important:** You must first enable auto-dismiss at the experience settings level before you can configure it at the event level.

Configurations made through an event take priority over those made in the experience settings. For example, in the experience settings, you might set all **Positive** alerts to auto-dismiss after 5 seconds. Then, for a specific **Positive** alert, you could override this initial configuration by adding an event that sets it to auto-dismiss after 10 seconds, or to disable auto-dismiss entirely.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Select **View experience settings**.

4.  Under **Configure alerts**, select the **Auto-dismiss** option next to the alert type you wish to configure.

    ![Configure alerts section of the experience settings, showing auto-dismiss selected for the Info alert type, with 5 seconds entered in the Timeout field.](../image/uib-alerts-experience-settings.png)

    For this example, select the **Auto-dismiss** option next to the **Info** alert type and enter `5` in the **Timeout \(seconds\)** field. **Info** alerts disappear after 5 seconds.

5.  Select **Save**.

6.  Return to the experience view.

7.  Create or open a page.

8.  In the content tree, select **+ Add content**.

9.  Select a **Button** component and select **Add**.

10. In the configuration panel, select the **Events** tab.

11. Under **Button clicked**, select **Add handler**.

12. Select **Add alert notifications** and select **Continue**.

    The **Configure** dialog enables you to edit multiple alerts in one place and displays a preview of the alert being edited. You can select the **+** to add more alerts, then select the alert in the dropdown to configure it.

    ![Configure event dialog with arrows pointing to the alert dropdown and add alert buttons.](../image/uib-alerts-event1.png)

    For this example, leave the alert **Type** as **Info**.

13. At the bottom of the **Configure** dialog, under **Auto-dismiss**, enter `10` in the **Timeout** field.

    ![Configure event dialog with arrows pointing to the selected Auto-dismiss property and the Timeout field with an entered value of 10.](../image/uib-alerts-event2.png)

    This specific **Info** alert disappears after 10 seconds.

14. You can also clear the check box to turn off auto-dismissal for this individual alert.

    **Note:** Other alerts of the same type retain the initial configuration in the experience settings until overridden through an event.

15. Select **Add**.


## Result

Alerts of the selected type are now set to auto-dismiss after the specified time period.

**Parent Topic:**[Customize UI Builder pages using components](../concept/work-components.md)

