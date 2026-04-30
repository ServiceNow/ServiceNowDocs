---
title: Control access to history
description: You can give a role access to view audit history by setting a system property.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Auditing]
---

# Control access to history

You can give a role access to view audit history by setting a system property.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System**.

2.  Select the **glide.history.role** property from the table.

3.  In the **List of roles \(comma-separated\) that can access the history of a record**, select the user roles you want to access history.

4.  Select **Save**.


## Result

Any changes to a field are omitted if a user without read-access views the history of a record.

