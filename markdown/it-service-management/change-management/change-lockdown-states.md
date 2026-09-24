---
title: Change lockdown states
description: These states describe where a change lockdown sits in its approval cycle, which actions are available, and whether the lockdown holds any change requests.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/change-lockdown-states.html
release: brazil
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [change lockdown, lockdown states]
breadcrumb: [Change lockdown, Configure, Change Management, IT Service Management]
---

# Change lockdown states

These states describe where a change lockdown sits in its approval cycle, which actions are available, and whether the lockdown holds any change requests.

## States of a change lockdown

|State|Description|Available actions|
|-----|-----------|-----------------|
|Draft|The lockdown is being defined. The conditions and the schedule are editable, and no change request is on hold. The **Preview** action becomes available after a schedule entry is saved.|Preview, Update, Request Approval, Delete|
|Awaiting Approval|Approval has been requested and an approval record is generated for the assignment group or the assigned user. No change request is on hold yet.|Preview, Revert to Draft, Cancel Lockdown, Delete|
|Enforced|The lockdown is approved and active. The matched change requests appear in the **Schedule Lockdown Changes** related list with the **On hold** column set to `true`.|Cancel Lockdown, Delete|
|Cancelled|The lockdown has ended. If it had been enforced, the change requests that it held are released. A cancelled lockdown cannot be reverted or reused.|Delete|

## Related lists on a change lockdown

|Related list|Description|
|------------|-----------|
|Schedule Entries|Periods that the lockdown covers. Each entry sets values such as **All day**, **Repeat on**, **End date time**, **Float day**, and **Float week**. A lockdown needs at least one entry.|
|Schedule Lockdown Changes|Change requests that the lockdown holds, with their **Change request** number, **Short description**, **State**, and **On hold** value. This list is populated when the lockdown is enforced.|
|Approvers|Approval records generated for the lockdown, with their state, approver, comments, and creation date.|

**Parent Topic:**[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

**Related topics**  


[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

