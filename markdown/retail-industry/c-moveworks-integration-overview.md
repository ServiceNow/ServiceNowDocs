---
title: Moveworks integration overview
description: The Moveworks integration sends outbound webhook events from ServiceNow to the Moveworks listener when a Break-Fix case changes to a key state, enabling Moveworks to proactively notify store associates on their desktop messaging platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/c-moveworks-integration-overview.html
release: australia
topic_type: concept
last_updated: "2025-07-01"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Moveworks integration overview

The Moveworks integration sends outbound webhook events from ServiceNow to the Moveworks listener when a Break-Fix case changes to a key state, enabling Moveworks to proactively notify store associates on their desktop messaging platform.

Events are dispatched when a `sn_rtl_stre_servcs_bf_case` transitions to a trigger state **and** `contact_type = moveworks`. No event is sent if the `opened_by` user has no email address — a warning is logged and the call is skipped.

## Trigger conditions and events

|Transition|Event|Extra payload|
|----------|-----|-------------|
|New \(1\) → Open \(10\)|`case_assigned`|—|
|Any → Resolved \(6\)|`case_resolved`|Resolution code|
|Any → Awaiting Info \(18\)|`case_awaiting_info`|Latest agent comment|

## Failure behavior

HTTP call failures are caught and logged. Case state is never affected by webhook delivery failures.

## Customer prerequisites \(Moveworks side\)

Install these plugins from the Moveworks plugin marketplace. Without them, ServiceNow dispatches events but Moveworks does not act on them.

|Plugin|Purpose|
|------|-------|
|`Retail_Create_Breakfix_Case`|Case creation via Moveworks|
|`Retail_Get_Breakfix_Case_Details`|Case detail retrieval|
|`Retail_Update_Breakfix_Case_Details`|Case field updates|
|`Retail_Notify_Breakfix_Case_Lifecycle`|Handles assigned/resolved/awaiting-info events|

