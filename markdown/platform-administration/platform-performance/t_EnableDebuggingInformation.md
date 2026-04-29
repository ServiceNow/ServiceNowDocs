---
title: Enable transaction quota debugging
description: You can enable the logging of transaction quota debugging information by enabling the system property.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction quotas, Configure, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Enable transaction quota debugging

You can enable the logging of transaction quota debugging information by enabling the system property.

## Before you begin

Role required: admin

## Procedure

1.  Add the glide.quota.manager.debug system property, and set the value to true.

2.  Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Debug Quotas**.

    The Debug Quota script runs to enable debugging.


## What to do next

After setting the above system property to **true**, go to your system log to see messages from the Quota Manager.

**Related topics**  


[Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#)

