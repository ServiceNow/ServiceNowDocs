---
title: Add users to a watch list
description: Watch lists enable you and others to subscribe to notifications of a task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/ai-platform-administration/t\_UseAWatchList.html
release: yokohama
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customizing fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add users to a watch list

Watch lists enable you and others to subscribe to notifications of a task.

## Before you begin

Role required: none

## Procedure

1.  Navigate to a record that you want to add watchers to.

    **Note:** Not all records have watch lists. If you’re unable to see a watch list, you may need to [adjust your form view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/configure-user-experiences/view-management-overview.md) or ask your administrator to update the form to add a watch list.

2.  Expand the watch list by selecting the lock icon \( \[Omitted image "LockIconNE.png"\] Alt text: lock icon\).

3.  Select users with the list controls \(see table\).

    |Icon|Function|
    |----|--------|
    |\[Omitted image "NEIconAddMe.png"\] Alt text: Add me icon|Add yourself to the watchlist|
    |\[Omitted image "NEIconRemoveUser.png"\] Alt text: Remove selected item icon|Remove the highlighted user|
    |\[Omitted image "NEIconPreview.png"\] Alt text: Preview selected item icon|Open the highlighted user's record \(active only when a user record exists\)|
    |\[Omitted image "NEIconAddRemoveUsers.png"\] Alt text: Add/remove multiple icon|Open the Edit Members window to add or remove multiple users \(not available until a record has initially been saved\)|
    |\[Omitted image "NEIconLockWatchlist.png"\] Alt text: Lock Watch list icon|Indicates that the watch list is unlocked; select the icon to lock the watch list|
    |\[Omitted image "NEIconLookup.png"\] Alt text: Lookup using list icon|Open the Users list in a new window to select a single user|
    |\[Omitted image "NEIconAddEmail.png"\] Alt text: Add email address icon|Enter an email address for users who aren’t in the User \[sys\_user\] table or don’t have an email address defined in their user record|


-   **[Configure email notifications for watch lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/ai-platform-administration/t_ConfigNotifications4WatchLists.md)**  
Watch lists \(glide\_list field type\) allow multiple users to subscribe to notifications of a task. You can specify conditions in an email notification to send email notifications to the members when the conditions are met.

**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/ai-platform-administration/customize-fields-now-platform-landing.md)

