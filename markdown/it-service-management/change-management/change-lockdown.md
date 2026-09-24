---
title: Change lockdown
description: Change lockdown allows change managers to pause all or a subset of in-flight change requests. Use it during major unplanned IT, critical, or financial events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/change-lockdown.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [change lockdown, lockdown, change freeze, on hold]
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Change lockdown

Change lockdown allows change managers to pause all or a subset of in-flight change requests. Use it during major unplanned IT, critical, or financial events.

Change lockdown is available in the base system. After installation, the **Change Lockdowns** module appears in the Change application menu. To view or create a new change lockdown, see [Create a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-change-lockdown.md).

A lockdown moves through an approval cycle before it takes effect. You can preview the affected change requests and refine the criteria while the lockdown is in draft. You can also cancel the lockdown when the situation that prompted it is resolved. For the full list of states, see [Change lockdown states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown-states.md).

When a lockdown is approved and it reaches the **Enforced** state, the system writes the previewed change requests to the **Schedule Lockdown Changes** related list and sets their **On hold** field to `true`. Cancelling an enforced lockdown releases those change requests.

For steps on previewing, approval, and cancellation, see [Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md).

**Note:** If a change request was already on hold before the lockdown was created, it remains on hold after the lockdown is cancelled.

## Lockdowns and conflict detection

A new conflict type is introduced, **Inside Change Lockdown** conflict type which identifies change requests that overlap with an active lockdown period.

Conflict detection checks change requests against active lockdown records. If you create or reschedule a change request inside a lockdown period, the system places it on hold automatically.

For more information, see [Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/lockdown-conflict-detection.md).

**Note:**

-   Whether conflict detection runs against a lockdown depends on the change model state configuration.
-   The scheduling assistant excludes enforced lockdown periods when suggesting maintenance windows.

-   **[Create a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-change-lockdown.md)**  
Create a change lockdown to pause in-flight change requests during major unplanned IT, critical, or financial events.
-   **[Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md)**  
Manage a change lockdown by previewing affected change requests, submitting for approval, reverting to draft, or canceling it.
-   **[Set the lockdown preview maximum](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/set-lockdown-preview-maximum.md)**  
Change the maximum number of records that a change lockdown preview displays. This keeps the preview readable on instances with a large volume of change requests.
-   **[Change lockdown states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown-states.md)**  
These states describe where a change lockdown sits in its approval cycle, which actions are available, and whether the lockdown holds any change requests.
-   **[Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/lockdown-conflict-detection.md)**  
Conflict detection checks change requests against active lockdown records in the same run that checks maintenance windows and blackout windows. A change request that falls inside a lockdown period is reported as a conflict and automatically placed on hold.

**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-management.md)

**Related topics**  


[Create a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/create-change-lockdown.md)

[Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md)

[Change lockdown states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown-states.md)

[Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/lockdown-conflict-detection.md)

[Limit conflict detection to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/limit-conflict-detection-state.md)

