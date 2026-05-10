---
title: Hide the Platform Analytics library banner
description: On instances that will not be migrated to Platform Analytics experience, set a system property to hide the banner that links to the Platform Analytics experience library.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-20"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Hide the Platform Analytics library banner

On instances that will not be migrated to Platform Analytics experience, set a system property to hide the banner that links to the Platform Analytics experience library.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Create the system property **com.glide.par.unified\_analytics.enabled**.

    For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

3.  Set the value of the property to `false`.


## Result

Users will not see the banner that directs them to the Platform Analytics experience library.

