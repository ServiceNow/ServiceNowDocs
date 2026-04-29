---
title: API parameters to customize Desktop Assistant notifications
description: Use these parameters in the API to customize the Desktop Assistant notifications.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# API parameters to customize Desktop Assistant notifications

Use these parameters in the API to customize the Desktop Assistant notifications.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Parameter list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Notification message

</td><td>

Enter the notification message you would like to send.

</td></tr><tr><td>

Notification title

</td><td>

Enter a title to the notification.

</td></tr><tr><td>

Recipient list

</td><td>

Add the receipt list of users who can receive this notification.

</td></tr><tr><td>

Referrer id

</td><td>

Enter the corresponding sys\_id of the referred table selected.

</td></tr><tr><td>

Referrer table

</td><td>

Select a type for record on which the notification should be triggered.

</td></tr><tr><td>

Source

</td><td>

Indicates the application from which it got triggered.**Note:**

-   Desktop Assistant supports only Major Incident Management and Proactive Engagement sources out of the box.
-   The notifications will be sent successfully for new sources, only if the new source is added as the new choice value for **Notification source** column in **sn\_dex\_desktop\_assistant\_notification** table, which will allow the Desktop Assistant to track the new source.

</td></tr></tbody>
</table>The following example illustrates the API parameters to customize the Desktop Assistant notifications.

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

