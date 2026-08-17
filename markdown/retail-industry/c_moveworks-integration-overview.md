---
title: ServiceNow Otto integration overview
description: The ServiceNow Otto integration sends outbound webhook events to the ServiceNow Otto listener when a Break-Fix case changes to a key state. This enables ServiceNow Otto to proactively notify store associates on their desktop messaging platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/c\_moveworks-integration-overview.html
release: australia
topic_type: concept
last_updated: "2025-07-01"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# ServiceNow Otto integration overview

The ServiceNow Otto integration sends outbound webhook events to the ServiceNow Otto listener when a Break-Fix case changes to a key state. This enables ServiceNow Otto to proactively notify store associates on their desktop messaging platform.

Events are dispatched when a `sn_rtl_stre_servcs_bf_case` transitions to a trigger state and `contact_type = moveworks`. No event is sent if the `opened_by` user has no email address — a warning is logged and the call is skipped.

## Trigger conditions and events

|Transition|Event|Extra payload|
|----------|-----|-------------|
|New \(1\) → Open \(10\)|`case_assigned`|—|
|Any → Resolved \(6\)|`case_resolved`|Resolution code|
|Any → Awaiting Info \(18\)|`case_awaiting_info`|Latest agent comment|

## Failure behavior

HTTP call failures are caught and logged. Case state is never affected by webhook delivery failures.

## Customer prerequisites \(ServiceNow Otto side\)

Install these plugins from the [ServiceNow Otto plugin marketplace](https://marketplace.moveworks.com/). Without them, ServiceNow dispatches events but ServiceNow Otto does not act on them.

|Plugin|Purpose|
|------|-------|
|`Retail_Create_Breakfix_Case`|Case creation via ServiceNow Otto. Built on Moveworks.|
|`Retail_Get_Breakfix_Case_Details`|Case detail retrieval|
|`Retail_Update_Breakfix_Case_Details`|Case field updates|
|`Retail_Notify_Breakfix_Case_Lifecycle`|Handles assigned/resolved/awaiting-info events|

