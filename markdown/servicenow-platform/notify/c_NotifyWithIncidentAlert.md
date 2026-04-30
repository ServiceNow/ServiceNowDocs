---
title: Using Notify with Incident Communications Management
description: Use Notify with incident communication plan to send SMS messages or start conference calls.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using Notify with Incident Communications Management

Use Notify with incident communication plan to send SMS messages or start conference calls.

Certain configuration steps are required to use Notify with an incident communication plan.

-   Both Notify and Incident Communications Management must be active.
-   Notify must be configured and able to initiate and receive phone calls and SMS messages.
-   The property **com.snc.iam.notify\_number** must be set to an active Notify number with outgoing voice and SMS capability.
-   This Notify number must belong to a number group configured with inbound and outbound conference call workflows.

**Note:** The Conference Call Group number group is configured with conference call workflows by default.

-   **[Initiate a conference call from incident communication plan](../task/t_IALaunchAConferenceCall.md)**  
Use Notify to initiate a conference call from an incident communication plan by inviting one or more users.
-   **[Join and end a conference call from incident communications management](../task/join-end-conference-call-from-icp.md)**  
After a conference call is initiated, join the call to participate in the discussion or end the call when the conference is no longer required.
-   **[Send communication updates for an incident communications plan](../task/t_IASendSMSNotifications.md)**  
Update users on the latest communication on an incident through selected communication channels.

**Parent Topic:**[Using Notify](using-notify.md)

**Related topics**  


[Incident Communications Management](https://www.servicenow.com/docs/access?context=c_IncidentAlertManagement&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

[Numbers and number groups](c_NumberGroups.md)

[Using Notify for making conference calls](c_NotifyConferenceCalls.md)

