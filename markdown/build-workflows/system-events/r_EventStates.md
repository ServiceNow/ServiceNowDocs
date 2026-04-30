---
title: Event states
description: The event state describes where in the life cycle the event is.
locale: en-US
release: yokohama
product: System Events
classification: system-events
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [System events reference, System Events, Build workflows]
---

# Event states

The event state describes where in the life cycle the event is.

<table id="table_hb4_bk3_wr"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Ready

</td><td>

The system created the event and it is in the queue waiting to be processed.

</td></tr><tr><td>

Processed

</td><td>

The event successfully ran. An event does not necessarily trigger any further action when processed. Additional functionality must make use of the event.

</td></tr><tr><td>

Error

</td><td>

The event encountered an error during processing. This state is often caused by invalid event parameters. Reprocessing the event may resolve the error.

</td></tr><tr><td>

Transferred

</td><td>

The event was rotated to a different shard of the Event \[`sysevent`\] table. When an event is rotated, a duplicate record is created in an active shard to be processed. A scheduled job processes the event when it is next in the queue, but it is not possible to predict when this will happen as because several events may need to be processed before it. Therefore, you can reprocess the event. See [Reprocess an event](../task/t_ReprocessAnEvent.md).

</td></tr></tbody>
</table>**Parent Topic:**[System events reference](system-events-reference.md)

