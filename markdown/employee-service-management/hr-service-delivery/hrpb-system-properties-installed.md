---
title: System properties installed
description: Use these system properties to configure security enforcement, the weekly digest, and the weekly case reconciliation job for the HRBP productivity assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/hrpb-system-properties-installed.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Reference, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# System properties installed

Use these system properties to configure security enforcement, the weekly digest, and the weekly case reconciliation job for the HRBP productivity assistant.

The following table consists of system properties to set up the HRBP productivity assistant.

|Property|Type|Default|Description|
|--------|----|-------|-----------|
|`glide.enforce_security_scope.sn_hrbp_hub`|true/false|true|Enforces sn\_hrbp\_hub ACLs on global tables, such as sys\_attachment, based on the scope of the related record. Users can access an attachment only if they can access its parent record. Don't set to false. Users might read or delete attachments on HRBP records they shouldn't access.|
|`sn_hrbp_hub.impersonateCheck`|true/false|false|Backs the sn\_hrbp\_hub\_\_HrbpHubPropertyImpersonateCheck security attribute. When true, ACLs that use the attribute also restrict access while an admin impersonates another user. When false, impersonation isn't checked.|
|`sn_hrbp_hub.weekly_digest.max_items_per_category`|Integer|10|Sets the maximum number of HR cases listed per category in the HRBP weekly digest email. Higher values make longer emails. A value of 0, blank, or non-numeric uses the default.|
|`sn_hrbp_hub.specialized_assistant_id`|String|`aiux/employeeworks/chat?mw_route=/assistant/agents/{YOUR_ASSISTANT_ID}`|Sets the HRBP productivity assistant link in the HRBP weekly digest email and AIUX widget preview. Replace `{YOUR_ASSISTANT_ID}` with your organization's assistant ID.|
|`sn_hrbp_hub.reconciliation.time_limit_minutes`|Integer \(minutes\)|30|Sets how long one monthly reconciliation run processes cases before it queues a continuation event and stops. Don't exceed 60. After 60 minutes, the system can treat the run as crashed and clear its lock, which lets a second cycle start. A value of 0, blank, or non-numeric uses the default.|
|`sn_hrbp_hub.reconciliation.extraction_limit`|Integer|20000|Limits how many sn\_hr\_core\_case records one run loads into memory. It also caps the records processed per run. With `max_invocations_per_cycle`, it sets the monthly maximum \(default: 20,000 × 50 = 1,000,000\). A value that's too low silently limits coverage every cycle. A value of 0, blank, or non-numeric uses the default.|
|`sn_hrbp_hub.reconciliation.max_invocations_per_cycle`|Integer|50|Limits how many chained runs one reconciliation cycle can use before it stops and alerts. Total processing time is about this value × `time_limit_minutes`. This catches runaway chains. A value of 0, blank, or non-numeric uses the default.|
|`sn_hrbp_hub.auto_deflected_state`|Integer \(as string\)|5|Sets which sn\_hr\_core\_case state counts as auto-deflected in the weekly tally of the HRBP HR Cases widget. The app doesn't ship this property record. To override the default, create the record or edit the widget script.|

