---
title: State flow cleanup
description: The business rules, client scripts, and UI actions that the system creates automatically to perform custom transitions exist only while the state flow records that use them are present.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing State flows, Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# State flow cleanup

The business rules, client scripts, and UI actions that the system creates automatically to perform custom transitions exist only while the state flow records that use them are present.

When a state flow on a table are deleted, the system attempts to delete any unnecessary programming elements that were created on that table, using these criteria:

<table id="table_jv1_zh2_dbc"><thead><tr><th>

Element

</th><th>

Deleted When

</th></tr></thead><tbody><tr><td>

UI action

 Business rule

 Dictionary override

</td><td>

The state flow that created it is deleted.

</td></tr><tr><td>

Business rule that processes events triggered by a state flow

</td><td>

All state flows for the table specified that have events configured are deleted.

</td></tr><tr><td>

Client script \(onLoad\)

</td><td>

All state flows for the table are deleted.

</td></tr><tr><td>

Client script \(onChange\)

</td><td>

All state flows with field controls are deleted.

</td></tr><tr><td>

Work notes business rule

</td><td>

All state flows with field controls or work notes are deleted.

</td></tr></tbody>
</table>