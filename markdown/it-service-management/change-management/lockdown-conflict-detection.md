---
title: Change lockdown conflict detection
description: Conflict detection checks change requests against active lockdown records in the same run that checks maintenance windows and blackout windows. A change request that falls inside a lockdown period is reported as a conflict and automatically placed on hold.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/lockdown-conflict-detection.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [change lockdown, conflict detection, Inside Change Lockdown, on hold]
breadcrumb: [Change lockdown, Configure, Change Management, IT Service Management]
---

# Change lockdown conflict detection

Conflict detection checks change requests against active lockdown records in the same run that checks maintenance windows and blackout windows. A change request that falls inside a lockdown period is reported as a conflict and automatically placed on hold.

The `change.conflict.lockdown` property controls whether conflict detection checks against lockdown records. The property is shipped with the value `true`, so lockdown checking is active by default. For more information, see [Conflict detection properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-conflict-properties.md).

## Conflict detection triggers

By default, conflict detection runs whenever one of the following values on a change request changes:

-   The state of the change request
-   The configuration item
-   The planned start date or the planned end date

Any of these changes triggers a run. A new change request that falls inside a lockdown is placed on hold as soon as you submit it, regardless of the change request state.

You can narrow this behavior to a single state of a change model by using the **Allow Conflict Detection** model state attribute. When the attribute is present on one state, conflict detection runs only when the change request reaches that state. For more information, see [Limit conflict detection to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/limit-conflict-detection-state.md).

## Lockdown conflict results

A change request that falls inside a lockdown period shows a conflict of type **Inside Change Lockdown** in the **Conflicts** tab, with the lockdown record named in the **Schedule** column. The **Conflict status** field is set to **Conflict**, the **On hold** field is set to **true**, and the **On hold reason** field records which lockdown caused the hold.

Rescheduling the change request outside the lockdown period triggers a new conflict detection run. The lockdown conflict is removed, the on hold reason is cleared, and the change request can continue through its states.

-   **[Limit conflict detection to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/limit-conflict-detection-state.md)**  
Use the Allow Conflict Detection attribute to limit conflict detection to a specific change model state. Conflict detection then runs only when a change request reaches that state.

**Parent Topic:**[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

**Related topics**  


[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

[Limit conflict detection to a change model state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/limit-conflict-detection-state.md)

