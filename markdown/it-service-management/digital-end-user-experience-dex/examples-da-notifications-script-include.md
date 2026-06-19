---
title: Examples of Desktop Assistant notifications using DesktopAppNotificationUtils
description: Examples showing the sendDANotification\(\) method of DesktopAppNotificationUtils used to send a Major Incident Management \(MIM\) alert and a Proactive Engagement \(PE\) notification.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/examples-da-notifications-script-include.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# Examples of Desktop Assistant notifications using DesktopAppNotificationUtils

Examples showing the sendDANotification\(\) method of `DesktopAppNotificationUtils` used to send a Major Incident Management \(MIM\) alert and a Proactive Engagement \(PE\) notification.

## Major Incident Management alert

The following code sends a P1 major incident alert to two users. The **referrer\_table** and **referrer\_id** parameters specify the incident record that the notification links to.

```
var utils = new sn_dex_desktop.DesktopAppNotificationUtils();

var response = utils.sendDANotification({
    notification_title:   "Major Incident Declared",
    notification_message: "A P1 major incident affecting the VPN gateway has been declared. " +
                          "Your team lead has been notified. Check INC0009001 for updates.",
    recipient_list:       "3a59b56ec6112000bce4d7d220a8df54," +
                          "62826bf03710200044e0bfc8bcbe5df1",
    referrer_table:       "incident",
    referrer_id:          "1c741bd70b2011200523d2e2d9c2d46a",
    source:               "mim"
});

gs.info("DA Notification response: " + JSON.stringify(response));
```

The system returns the following response.

```
{
  "responseCode": "200",
  "message": "Desktop Assistant Notification Call flow called with flow context ID: <guid>",
  "metadata": { "notificationID": "<sys_id of inserted notification record>" }
}
```

## Proactive Engagement notification

The following code sends a license renewal reminder to a single user and includes a link to the related service catalog request.

```
var utils = new sn_dex_desktop.DesktopAppNotificationUtils();

var response = utils.sendDANotification({
    notification_title:   "Action Required: Software License Renewal",
    notification_message: "Your Adobe Acrobat license expires in 5 days. " +
                          "Submit a renewal request through the Service Portal.",
    recipient_list:       "3a59b56ec6112000bce4d7d220a8df54",
    referrer_table:       "sc_request",
    referrer_id:          "<sc_request_sys_id>",
    source:               "pe"
});
```

**Parent Topic:**[DEX Desktop Assistant reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-desktop-experience-reference.md)

