---
title: API parameters to customize Desktop Assistant notifications
description: Use these parameters in the API to customize Desktop Assistant notifications.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# API parameters to customize Desktop Assistant notifications

Use these parameters in the API to customize Desktop Assistant notifications.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification message

</td><td>

The notification message that you would like to send.

</td></tr><tr><td>

Notification title

</td><td>

Title of the notification.

</td></tr><tr><td>

Recipient list

</td><td>

The list of users who can receive the notification.

</td></tr><tr><td>

Referrer id

</td><td>

The corresponding sys\_id of the referred table selected.

</td></tr><tr><td>

Referrer table

</td><td>

Type of record on which the notification should be triggered.

</td></tr><tr><td>

Source

</td><td>

The application from which the notification is triggered.**Note:**

-   Desktop Assistant supports only Major Incident Management and Proactive Engagement sources in the base system.
-   Notifications for new sources are sent successfully only when the source is added as a choice value in the **Notification source** column of the **sn\_dex\_desktop\_assistant\_notification** table. This enables Desktop Assistant to track the new source.

</td></tr></tbody>
</table>The following example illustrates the API parameters to customize Desktop Assistant notifications.

```
var notificationObj = {
  notification_message: "Notification Message",
   notification_title: "DA MIM Notification",
  recipient_list: "Receiving sys_user sysid",
   referrer_id: "referrer record sys_id",
   referrer_table: "incident",
   source: "MIM"
};
var notifyUtils = new sn_dex_desktop.DesktopAppNotificationUtils();
notifyUtils.sendDANotification(notificationObj);
```

**Parent Topic:**[DEX Desktop Assistant reference](dex-desktop-experience-reference.md)

