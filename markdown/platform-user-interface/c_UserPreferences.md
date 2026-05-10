---
title: User preferences
description: Users can configure many UI features, such as the number of rows per page in a list or whether the response time displays at the bottom of a list or form. Administrators can modify or delete these preferences as needed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# User preferences

Users can configure many UI features, such as the number of rows per page in a list or whether the response time displays at the bottom of a list or form. Administrators can modify or delete these preferences as needed.

User customizations are stored as records in the **User preferences** \[sys\_user\_preference\] table, and are updated each time the user changes the setting. The UI displays according to each user's preferences.

For example, the response time may appear at the bottom of lists and forms by default. If a user hides the response time, a user preference record is created for them showing that the response time indicator as hidden. During the user's future sessions, the response time indicator is hidden. If the user later decides to display the response time, the user preference record is updated appropriately, and future sessions open with the response time indicator visible.

For more information about the preferences available to users, see [User preference settings](../reference/r_UserPreferenceSettings.md) and [Next Experience preferences](../../../get-started/servicenow-overview/concept/set-up-preferences-next-experience.md).

## Viewing and troubleshooting user preferences

Navigate to **User Administration** &gt; **User Preferences** for a list of user preference records. Select a preference name to display that preference in the form view. If troubleshooting for a user, search for their user name to find all of their customizations, and then select a preference name to view.

**Note:** Up to 10,000 user preferences can exist for each user. Exceeding this limit causes system degradation and UI performance issues.

|Field|Description|
|-----|-----------|
|Name|The name of the feature or functionality.|
|Description|An optional short description of the feature or functionality.|
|System|Shows whether this record indicates the system-wide default \(**TRUE**\), or not \(**FALSE**\).|
|Type|Shows the data type of entry accepted for the Value. For example, you can select **string** or **integer**.|
|User|Shows the name of the user for whom the setting is customized. If **User** is empty, the record is for a system-wide default.|
|Value|The current setting for this record. Compare this value to the **User** field and **System** field to determine whether the value shown is a system-wide default or a specific user’s preference.|

You can identify user preference records for system-wide values, also called the default or global values, by the following values:

-   **System=TRUE**
-   **User=blank**

Whenever a user customizes a feature, a separate user preference record is created with the following values:

-   **System=FALSE**
-   **User=&lt;username&gt;**

As a result, the same customizable UI feature may have multiple user preference records.

**Note:** For some features, the system-wide record doesn’t appear in the **User preferences** module until a user customizes it, causing a new record to be added to the **User preferences**.

If a user encounters an unexplained behavior in the user interface, you can check their user preferences by searching the **User preferences** list for their user name. Then, delete or update the user preference record that affects the behavior in question.

**Note:** When an administrator manually changes a user's preference value through this module, the user's next session uses the administrator's setting. However, the user can customize the features again through the UI, which updates their user preference record. If the administrator deletes the user preference record for a particular user, that user's next session uses the system-wide value for that feature. When the user later customizes the feature, the system creates a user preference record for the user.

## Global user preferences

Create system-wide or global user preferences to set a default preference for your users. To make a preference the default, create a preference, check the **System** check box, and leave the **User** field empty.

**Important:** You should never have more than one preference with the same name set as a global user preference.

## User preferences and update sets

User preference records for system-wide values, also called the default or global values, are stored in update sets. Any changes are implemented when you import the update set and affect all users who have not customized the feature. User preference records for specific users aren’t stored in update sets, so user customizations are retained when you import an update set. For more information, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/system-update-sets.md).

-   **[User preference settings](../reference/r_UserPreferenceSettings.md)**  
User preferences primarily track the way individual users interact with various features so that new sessions activate the user's last settings. For example, user preferences track whether the user activates the tabbed or scrolling interface for multi-section forms. Other user preference records enable users with the admin role to adjust certain feature settings.
-   **[Turn off the Next Experience welcome screen after upgrading your instance](../task/remove-welcome-splash-screen.md)**  
You can turn off the Next Experience welcome splash screen that appears in the Core UI after upgrading your instance by creating a user preference.
-   **[Configure available keyboard shortcuts](../task/configure-keyboard-shortcuts.md)**  
Administrators can configure which keyboard shortcuts are available to users.

**Parent Topic:**[User interface configuration](../../core-configuration/concept/p_NavigationAndUIConfiguration.md)

