---
title: Configuring the Customer History component
description: Users with the admin role can configure several properties for the Customer History component.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Customer Central, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configuring the Customer History component

Users with the admin role can configure several properties for the Customer History component.

## Refresh requested

The Customer History component refreshes automatically, eliminating the need for manual page refreshes.

The **Refresh requested** UI Builder property captures the last refresh timestamp and triggers events such as Context Refresh Requested whenever the value changes. Admins can configure custom event handlers to adjust the refresh behavior as needed.

This property can be set for the following record pages:

-   Front-line case page
-   CSM default record page

To configure this property on the Front-line case page:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  Open the Front-line case page.
4.  Select the **Customer History** component.
5.  Navigate to the Properties panel.
6.  Capture the last refresh timestamp by enabling the **Refresh Requested** property.
7.  Customize the refresh behavior by adding or modifying event handlers under the Events tab.

To configure this property on the CSM default record page:

1.  Select **Customer Central**.
2.  Open the Customer history section.
3.  Navigate to the Properties panel.
4.  Capture the last refresh timestamp by enabling the **Refresh Requested** property.
5.  Customize the refresh behavior by adding or modifying event handlers under the Events tab.

## Header title

The Customizable Customer Activity Title feature enables admins to rename the **Customer History** title directly from the interface.

To change the title: 

1.  In the right navigation pane, navigate to the **Component visibility** settings.
2.  Change the title according to user preferences by editing the **Header title** property.

This customization option is available on all pages where the Customer History component is used.

## Show bordered icons

The **Show bordered icons** check box enables admins to customize icon borders in the interface.

-   Set to true: Enables bordered icons
-   Set to false: Disables bordered icons

![Show bordered option](../image/cust-central-show-bordered-icon.png "Show bordered icons check box")

Admins can adjust this setting based on their preferences.

## Page design

The Page Design feature introduces a drag-and-drop interface for easier customization of page layouts. Admins can add, position, and resize components directly on the page without using tabs.

To use this feature:

1.  On the left navigation pane, select **+Add Content**.
2.  In the toolbox window that appears, enter `Customer history component` and then select and drag it.

The Customer History component is now available in the toolbox.

## Presets

Admins can choose from two new presets for the Customer History component on the Front-line case page to better manage how customer data is displayed.

-   Customer history for record page with lazy load
-   Customer history for record page

To apply a preset:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  Open the Front-line case page.
4.  Select the **Customer History** component.
5.  Select the existing preset in the configuration panel.
6.  In the Select a preset window, choose **All** under **Controller** to view available presets.
7.  Select one of the new presets to update how customer activity is displayed.

Default values are set for all fields to help prevent errors by ensuring that fields are never left null or empty.

## New empty state for context fields

![New empty state for context fields](../image/cust-central-empty-state-field-feature.png "New empty state for context fields")

On the agent side, when viewing a case, customer history or activity data loads automatically if available. If there’s no activity, the system shows `No activities found`. If no account, contact, or consumer is selected, it displays `No customer identified yet`. This behavior is part of the empty state feature, guiding users to select or add context \(account, contact, or consumer\) to proceed.

Admins can now configure cases to handle scenarios where customer contact or name fields are empty. Instead of leaving the fields empty, the system prompts users to add the relevant account or contact information.

## Show with activity creation date

The **Show with activity creation date** property, available in UI Builder, enables admins to control how timestamps are displayed in the Customer History tab.

-   When enabled: Both the timeline and side timestamp display the activity creation date. For example, if a record \(such as a case or interaction\) was created 10 days ago but updated today, both will show today’s date.
-   When not enabled \(default behavior\): Both the timeline and side timestamp display the original record creation date. So, in the same example, the record would continue to show as being created 10 days ago, even if it was updated today.

## Activity time period

The **Activity time period** field in the Customer History component enables admins to define how customer activities are grouped for agents in the CSM Workspace. By default, activities appear by day, but you can change this to group them by quarter or by year.

To configure the filter in the Front-line case page:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  Open the Front-line case page.
4.  Select the **Customer History** component.
5.  Navigate to the Properties panel.
6.  From the Activity time period drop-down, select one of the following options:
    -   **Day**: Enables an additional field where you can enter a date in `DD:MM:YYYY` format.
    -   **Monthly**: Groups activities by month.
    -   **Quarter**: Groups activities by calendar quarter.
    -   **Year**: Groups activities by calendar year.

To configure this property on the CSM default record page:

1.  Select **Customer Central**.
2.  Open the Customer History section.
3.  Navigate to the Properties panel.
4.  From the Activity time period drop-down, select one of the following options:
    -   **Day**: Enables an additional field where you can enter a date in `DD:MM:YYYY` format.
    -   **Monthly**: Groups activities by month.
    -   **Quarter**: Groups activities by calendar quarter.
    -   **Year**: Groups activities by calendar year.

