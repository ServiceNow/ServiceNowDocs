---
title: Mobile app screens
description: The Screens module show analytics specific to screens in your mobile application. View user action and navigation details for each mobile app screen.See user actions, gestures, and navigation analytics for each screen.Merge two or more actions to track for a screen.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [UI analysis, Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# Mobile app screens

The Screens module show analytics specific to screens in your mobile application. View user action and navigation details for each mobile app screen.

<table><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Screen name

</td><td>

Name of the selected screen. To change the name of a screen, click the edit icon ![](../image/edit-icon.png).

</td></tr><tr><td>

Sessions

</td><td>

Shows the number of sessions that contained the screen, and the number of impressions. If a screen was opened more than once during a session, it's only counted once.

</td></tr><tr><td>

Average Duration

</td><td>

Shows the average time spent on the screen. Also the percentage of time spent on the screen relative to the average time spent throughout the app during sessions.

</td></tr><tr><td>

% of App Interactions

</td><td>

Shows the relative interaction rate for the screen measured by the number of gestures performed.

</td></tr><tr><td colspan="2">

**Actions, Gestures &amp; Toasts**

</td></tr><tr><td>

Top User Actions

</td><td>

-   % Occurrences
-   % Sessions
-   Avg. / Session

</td></tr><tr><td>

Gestures

</td><td>

Ratio of user gestures per screen, and percentage of unresponsive gestures.

</td></tr><tr><td>

Merge actions ![Merge actions button](../image/merge-actions-button.png)

</td><td>

Enables you to merge actions.

</td></tr><tr><td colspan="2">

**Navigation**

</td></tr><tr><td>

Previous screen

</td><td>

Shows the top screens from which users arrived to the selected screen, and the percentage of sessions arriving from each screen relative to the total number of navigations to it. Rare actions may be omitted.

</td></tr><tr><td>

Next screen

</td><td>

Shows the top screens to which users arrived from the selected screen, and the percentage of sessions navigating to each screen relative to the total number of navigations from it.

</td></tr></tbody>
</table>Where available, you can view sessions that contained a specific screen. Click the Sessions list icon ![](../image/session-icon.png) to view these sessions from the Sessions list.

## View mobile app screen analytics

See user actions, gestures, and navigation analytics for each screen.

### Before you begin

Role required: user

### Procedure

1.  Navigate to **All** &gt; **UI Analysis** &gt; **Screens**.

2.  Scroll the screens list, or enter text in the **Search** field to locate and select a screen.


## Merge screen actions

Merge two or more actions to track for a screen.

### Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

### About this task

Merging actions applies to new sessions only, and doesn't change existing data.

**Note:** After a merger is performed the action can't be reversed.

### Procedure

1.  Navigate to **All** &gt; **UI Analysis** &gt; **Screens**.

2.  Search for and select the screen with the actions you want to merge.

3.  Click the merge icon \(![](../image/merge-actions-button.png)\) next to the first action that you want to merge.

4.  Select the check box next to the second action that you want to merge.

5.  Click **Apply**, after you've selected all the actions you want to merge for a screen.

    The merged actions are listed under the name of the first listed action.


