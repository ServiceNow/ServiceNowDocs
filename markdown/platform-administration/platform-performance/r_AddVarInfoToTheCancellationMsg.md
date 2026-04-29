---
title: Methods to add variable information to the cancellation message
description: You can use the following methods of the jvar\_transaction variable to add information to the cancellation message.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Methods to add variable information to the cancellation message

You can use the following methods of the *jvar\_transaction* variable to add information to the cancellation message.

|Method|Description|
|------|-----------|
|getURL\(\)|Returns the URL for the transaction.|
|getReason\(\)|Returns the reason for page cancellation, localized to the user's language.|
|getQuotaId\(\)|Returns the sys\_id of the quota rule.|
|getQuotaName\(\)|Returns the name of the quota rule.|
|getRunTime\(\)|Returns the total run time for the page up to this point.|
|getType\(\)|Returns the type of transaction, such as form, list, report, other.|
|getUser\(\)|Returns the sys\_id of the user.|
|getHomepage\(\)|Returns the sys\_id of the homepage.|
|getHomepageWidget\(\)|Returns the name of the homepage widget.|

**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

