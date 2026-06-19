---
title: Send a Desktop Assistant notification from server-side script
description: Use DesktopAppNotificationUtils to send Desktop Assistant notifications to users from a server-side script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/send-da-notifications-from-script.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Customizing Desktop Assistant notifications using API parameters, Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Send a Desktop Assistant notification from server-side script

Use `DesktopAppNotificationUtils` to send Desktop Assistant notifications to users from a server-side script.

## Before you begin

Role required: sn\_dex\_desktop.admin or admin

## Procedure

1.  Navigate to **System Properties** &gt; **All Properties** and confirm that **sn\_dex\_desktop.enable\_push\_notification** is set to **true**.

    If the property is set to **false**, the API immediately returns a 400 error and no notification is created.

2.  Collect valid sys\_id values from the User \(sys\_user\) table for each intended notification recipient and format them as a comma-separated string.

3.  Navigate to the server-side context where you want to trigger the notification.

    For example, a Background Script for testing, a business rule, scheduled job, or flow script step for production use.

4.  Call sendDANotification\(\) with **notification\_message**, **recipient\_list**, and **source** as the minimum required parameters.

    **Note:** The **source** parameter accepts `mim` \(Major Incident Management\) or `pe` \(Proactive Engagement\) as its value.

    Example of API call script structure:

    ```
    var utils = new sn_dex_desktop.DesktopAppNotificationUtils();
    var result = utils.sendDANotification({
        notification_title:   "Incident Assigned to You",
        notification_message: "INC0001234 has been assigned to your group. Please review.",
        recipient_list:       "abc123def456...,xyz789...",  // sys_id values, comma-separated
        referrer_table:       "incident",
        referrer_id:          "<incident_sys_id>",
        source:               "mim"
    });
    gs.info(JSON.stringify(result));
    
    ```

    For examples of sending Desktop Assistant notifications using `DesktopAppNotificationUtils`, see [Examples of Desktop Assistant notifications using DesktopAppNotificationUtils](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/examples-da-notifications-script-include.md).

5.  Check the return value to confirm the API call was successful.

    A successful call returns a `responseCode` of **200** and a `notification_id` in the `metadata` field of the response object. Any other response code indicates that the notification was not queued, and the `message` field of the response object states the reason.

6.  Verify that the notification was delivered to the Desktop Assistant client.

    For more information, see [View Desktop Assistant notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/view-notifications.md). If the notification does not appear on the Desktop Assistant client, see [Troubleshoot Desktop Assistant notification delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/resolve-da-notification-issues.md).


