---
title: Configuring the Customer History component
description: Users with admin role can configure several properties for the Customer History component.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Customer Central, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configuring the Customer History component

Users with admin role can configure several properties for the Customer History component.

## Refresh requested

The Customer History component refreshes automatically when the account, contact, or consumer is updated on a record, eliminating the need for manual page refreshes.

The **Refresh requested** property captures the last refresh timestamp and triggers events such as Context Refresh Requested whenever the value changes. Admins can configure custom event handlers to adjust the refresh behavior as needed.![Refresh Requested](../image/cust-central-refresh-requested-prop.png)

This property can be set for the following record pages:

-   Front-line case page
-   CSM default record page

To configure this property on the Front-line case page:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  Open the **Front-line case page**, click the **Customer History** component.
4.  Navigate to the **Properties** panel.
5.  Enable the **Refresh Requested** property to capture the last refresh timestamp.
6.  Add or modify event handlers under the Events tab to customize the refresh behavior.

To configure this property on the CSM Default Record page:

1.  Select **Customer Central**.
2.  Open the **Customer Activity** section.
3.  Navigate to the **Properties** panel.
4.  Enable the **Refresh Requested** property to capture the last refresh timestamp.
5.  Add or modify event handlers under the Events tab to customize the refresh behavior.

## Header title

The Customizable Customer Activity Title feature allows admins to rename the **Customer Activity** title directly from the interface.

To change the title: 

1.  Navigate to the **Component visibility** settings in the right navigation pane.
2.  Edit the **Header title** property to change the title according to user preferences.

This customization option is available on all pages where the Customer History component is used.

## Show bordered icons

The **Show bordered icons** check box allows admins to customize icon borders in the interface.![Show bordered option](../image/cust-central-show-bordered-icon.png)

-   Set to true: Enables bordered icons
-   Set to false: Disables bordered icons

Admins can adjust this setting based on their preferences.

## Page design

The Page Design feature introduces a drag-and-drop interface for easier customization of page layouts. Admins can add, position, and resize components directly on the page without using tabs.

To use this feature:

1.  Click **+Add Content** on the left navigation pane.
2.  In the toolbox window that appears, type Customer activity component and then select and drag it.

The Customer History component is now available in the toolbox.

## Presets

Admins can choose from two new presets for the Customer History component on the Front-line case page to better manage how customer data is displayed.

-   Customer activity for record page with lazy load
-   Customer activity for record page

To apply a preset:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CSM/FSM Configurable Workspace** experience.
3.  Open the **Front-line case page** and select the **Customer History** component.
4.  Select the existing preset in the configuration panel.
5.  In the **Select a preset** window, choose **All** under **Controller** to view available presets.
6.  Select one of the new presets to update how customer activity is displayed.

Default values are set for all fields to prevent errors by ensuring that fields are never left null or empty.

## New empty state for context fields

![New empty state for context fields](../image/cust-central-empty-state-field-feature.png)

On the agent side, when viewing a case, customer history or activity data loads automatically if available. If there’s no activity, the system shows “No activities found”. If no account, contact, or consumer is selected, it displays “No customer identified yet”. This behavior is part of the empty state feature, guiding users to select or add context \(account, contact, or consumer\) to proceed.

Admins can now configure cases to handle scenarios where customer contact or name fields are empty. Instead of leaving the fields blank, the system prompts users to add the relevant account or contact information.

