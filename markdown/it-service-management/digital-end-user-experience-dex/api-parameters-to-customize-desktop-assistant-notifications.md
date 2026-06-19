---
title: API parameters to configure Desktop Assistant notifications
description: sendDANotification\(\) method parameters in the DesktopAppNotificationUtils script include for configuring Desktop Assistant notifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/api-parameters-to-customize-desktop-assistant-notifications.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# API parameters to configure Desktop Assistant notifications

sendDANotification\(\) method parameters in the `DesktopAppNotificationUtils` script include for configuring Desktop Assistant notifications.

<table id="table_z5k_bwb_glb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**notification\_message**

</td><td>

Body text displayed on the notification card. The value must be a non-empty string and not exceed 1000 characters. If this condition is not met, the API returns a 400 error.

</td></tr><tr><td>

**notification\_title**

</td><td>

Title text displayed at the top of the Desktop Assistant notification card. If omitted, the notification card displays an empty title without raising an error.

</td></tr><tr><td>

**recipient\_list**

</td><td>

The `sys_id` values of the intended recipients, sourced from the User \(sys\_user\) table and provided as a comma-separated string.

</td></tr><tr><td>

**referrer\_id**

</td><td>

The sys\_id of the record that the notification links to.

 This parameter works in combination with **referrer\_table**. If only one of these two parameters is provided, the link behavior is unpredictable.

</td></tr><tr><td>

**referrer\_table**

</td><td>

The name of the table containing the record that the notification links to. For example, incident or sc\_request.

 This parameter works in combination with **referrer\_id**. If only one of these two parameters is provided, the link behavior is unpredictable.

</td></tr><tr><td>

**source**

</td><td>

The source application that triggered the notification. Accepted values are **mim** \(Major Incident Management\) and **pe** \(Proactive Engagement\). The value is case-insensitive. Any other value causes the API to return a 400 error.

**Note:** Desktop Assistant sends notifications for a new source only if the source is added as a choice value in the **Notification source** field of the Desktop Assistant notification \(sn\_dex\_desktop\_assistant\_notification\) table. This enables Desktop Assistant to recognize and track the source.

</td></tr></tbody>
</table>## Parameter interactions and precedence

|Scenario|Behavior|
|--------|--------|
|**notification\_message** is empty, missing, or not a string value.|Returns a 400 error.|
|**notification\_title** is missing or not a string value.|The Desktop Assistant client displays an empty title. No error is raised.|
|**source** is not **mim** or **pe**|Returns a 400 error: `Source record missing in Desktop Assistant Notification Source table`|
|**enable\_push\_notification** is **false**|Returns a 400 error immediately. No record is created and no flow runs.|
|**notification\_time\_to\_live** is set to more than 7 days|The value is capped at seven days.|
|**notification\_time\_to\_live** property is not set|Defaults to seven days.|
|Only one of **referrer\_table** or **referrer\_id** is provided|No error is raised and both fields are stored, but the notification on the Desktop Assistant client may not link to the correct record.|

## Desktop Assistant notification card element‑to‑source mapping

<table id="table_v3j_xhg_2jc"><thead><tr><th>

Desktop Assistant client UI element

</th><th>

Source parameter or field

</th></tr></thead><tbody><tr><td>

Notification title \(card header\)

</td><td>

**notification\_title**

</td></tr><tr><td>

Notification body text

</td><td>

**notification\_message**

</td></tr><tr><td>

Timestamp

</td><td>

Derived from the `sys_created_on` field on the Desktop Assistant Notification Queue \(sn\_dex\_desktop\_notify\_queue\) record. Not an API parameter.

</td></tr><tr><td>

System tray notification

</td><td>

Displayed when the notification status is **Pending** at the time the Desktop Assistant client checks for new notifications. Not an API parameter.

</td></tr></tbody>
</table>**Parent Topic:**[DEX Desktop Assistant reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-desktop-experience-reference.md)

