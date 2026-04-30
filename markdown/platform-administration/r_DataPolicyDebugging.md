---
title: Data policy debugging
description: Debug messages can help administrators identify and resolve data policy problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data policy, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Data policy debugging

Debug messages can help administrators identify and resolve data policy problems.

Debug messages can help you identify and resolve data policy problems. To view data policy debugging messages at the bottom of the screen, navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Debug Data Policies**.

In the example, a data policy is in place to prevent the short description on an incident from being changed when the incident state is set to Open. A user edited the short description while the incident was open and tried to save the changes, but the data policy was enforced.

![](../image/DebuggingDataPolicy.png "Data policy debug messages")

**Parent Topic:**[Data policy](../concept/c_DataPolicy.md)

