---
title: Register an event
description: You can register an event for a specific table and a business rule that fires the event.
locale: en-US
release: xanadu
product: System Events
classification: system-events
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing system events, System Events, Configure core features, Administer the ServiceNow AI Platform]
---

# Register an event

You can register an event for a specific table and a business rule that fires the event.

## Before you begin

Role required: admin

## Procedure

1.  To register an event, browse to **System Policy** &gt; **Events** &gt; **Registry**, and then click **New**.

2.  On the form fill in the fields.

<table id="table_hbv_pg3_j1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Event name

</td><td>

Name of your new event.

</td></tr><tr><td>

Table

</td><td>

Database table for this event. **Note:** Only tables and database views that are in the same scope as the event appear on the listing.

</td></tr><tr><td>

Queue

</td><td>

Name of the queue that the event is placed into when triggered.Use only lowercase letters, no spaces, and no special characters except underscore \(\_\). For example, `my_queue`. See [Using custom queues to process events](https://www.servicenow.com/docs/access?context=useful-server-side-scripts&version=xanadu&pubname=xanadu-application-development&section=queues-create&ft:locale=en-US).

</td></tr><tr><td>

Priority

</td><td>

Order in which messages will be processed. Lower values have higher priority.**Note:** The com.glide.sysevent.priority.enabled system property is enabled by default. If you disable it, events processing is not done by priority.

</td></tr><tr><td>

Caller Access

</td><td>

Restricted caller access settings.-   Caller Restriction: calls to the resource must be manually approved.
-   Caller Tracking: Calls to the resource are automatically approved.


</td></tr><tr><td>

Fired by

</td><td>

Name of the business rule that runs the event. This field is for reference only and is not used by any process. Make sure that there is enough information to locate your event again.

</td></tr><tr><td>

Description

</td><td>

Short description of the purpose of the event.

</td></tr></tbody>
</table>
