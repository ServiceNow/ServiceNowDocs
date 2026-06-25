---
title: Customizing Desktop Assistant notifications using API parameters
description: Administrators can send customized Desktop Assistant notifications to specific users by using the DesktopAppNotificationUtils script include with a set of notification parameters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/customizing-da-notifications-api.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 3
breadcrumb: [Set up Desktop Assistant, Configure, Digital End-User Experience, IT Service Management]
---

# Customizing Desktop Assistant notifications using API parameters

Administrators can send customized Desktop Assistant notifications to specific users by using the `DesktopAppNotificationUtils` script include with a set of notification parameters.

Desktop Assistant notifications are sent using the sendDANotification\(\) method of the `DesktopAppNotificationUtils` script include in the sn\_dex\_desktop application scope. This method is a server-side invocation that can be called from business rules, Background Scripts, Scheduled Jobs, Flow Script Steps, or Flow Designer actions. It is not exposed as a REST endpoint or Notify API. The Desktop Assistant client receives these notifications and displays them on the user's device, notifying employees of time-sensitive events such as major incidents affecting their services or software licenses that are about to expire.

By default, Major Incident Management \(MIM\) and Proactive Engagement \(PE\) send notifications through Desktop Assistant without invoking this API. For more information, see [Desktop Assistant notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/da-push-notifications.md). Use the `DesktopAppNotificationUtils` API to send notifications from additional sources.

**Note:** Desktop Assistant notifications require the Desktop Assistant client to be installed and running on the user's endpoint device.

## Desktop Assistant notification delivery process

1.  Server-side trigger: A server-side component such as a business rule, Flow Designer action, or Scheduled Job initiates the notification delivery process by calling the sendDANotification\(\) method on the `DesktopAppNotificationUtils` script include.
2.  Validation and record creation: The script include validates the input parameters and inserts a record into the Desktop Assistant notification \(sn\_dex\_desktop\_assistant\_notification\) table if validation succeeds. This record stores the notification title, message body, recipient list or device list, source, and expiry date.
3.  Asynchronous background processing: Creating the notification record triggers the desktop\_assistant\_notification\_call background flow. This flow runs asynchronously, allowing the original caller to continue without waiting for delivery processing to complete.
4.  Notification preparation and queuing: The background flow calls the internal DesktopNotificationAPI.sendNotification\(\) method, which prepares the notification for delivery and inserts rows into the Desktop Assistant Notification Queue \(sn\_dex\_desktop\_notify\_queue\) table. Each row in this table represents one delivery attempt for one device token.
5.  Notification delivery to the endpoint: The Agent Client Collector \(ACC\) running on the end user's device retrieves pending entries from the queue and delivers the notification to the Desktop Assistant client.

    By default, notification delivery is event-driven. The platform triggers the **sn\_dex\_desktop.triggerCheckdef** event, which signals the ACC agent to check for new notifications.


## How notifications appear in the Desktop Assistant client

Each Desktop Assistant notification appears as a card in the Desktop Assistant notification panel. The notification card displays the title, message body, and a timestamp indicating when the notification was sent.

If a notification is associated with a ServiceNow record, the card includes a deep link that opens the linked record directly. When the user's device is active at notification delivery time, a brief system tray toast notification also appears. The toast disappears automatically, while the notification card remains available in the Desktop Assistant panel for later reference.

## Notification visibility duration

The **sn\_dex\_desktop.sn\_desktop\_assistant.notification\_time\_to\_live** system property controls notification visibility duration in the Desktop Assistant client. You can set this value from **1** to **7** days, with a default of **7** days. If a value greater than **7** days is configured, the visibility period is limited to seven days. After the notification reaches its expiry date, it is automatically removed from the Desktop Assistant notification panel.

**Related topics**  


[Setting up DEX Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/config-dex-desktop-exp.md)

[Desktop Assistant notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/da-push-notifications.md)

[Send a Desktop Assistant notification from server-side script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/send-da-notifications-from-script.md)

[Examples of Desktop Assistant notifications using DesktopAppNotificationUtils](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/examples-da-notifications-script-include.md)

[API parameters to configure Desktop Assistant notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/api-parameters-to-customize-desktop-assistant-notifications.md)

[Digital End-User Experience properties and settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-properties-settings.md)

