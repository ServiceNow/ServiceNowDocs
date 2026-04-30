---
title: Nagios connector instance value parameters
description: The following table displays the Nagios connector instance value parameters that you can fill in, as needed, when creating a Nagios connector instance.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-03-27"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Nagios connector instance value parameters

The following table displays the Nagios connector instance value parameters that you can fill in, as needed, when creating a Nagios connector instance.

<table id="table_lbn_djz_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

debug

</td><td>

Set to **true** to enable debug logs.Default: false

</td></tr><tr><td>

max\_fetch\_interval\_min

</td><td>

Limits metric history retrieval to prevent system overload.Default: 180 minutes

</td></tr><tr><td>

offset\_min

</td><td>

Adds a small time buffer to ensure no metrics are missed.Default: 5 minutes

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

