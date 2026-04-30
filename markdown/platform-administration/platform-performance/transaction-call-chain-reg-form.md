---
title: Transaction call chain register form
description: A description of the fields in the Transaction Call Chain Register form.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-05-13"
reading_time_minutes: 1
breadcrumb: [Platform performance reference, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Transaction call chain register form

A description of the fields in the Transaction Call Chain Register form.

<table id="table_yxx_ndv_tr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

URL

</td><td>

URL for the selected transaction.

</td></tr><tr><td>

Transaction Log

</td><td>

Transaction log ID created during the next occurrence of the URL. This field is empty when you first create the call chain register for a transaction.

</td></tr><tr><td>

Recorded

</td><td>

Check box that indicates if call chain recording has already taken place for this transaction. -   This field is clear \(**false**\) when you first create the call chain register for a transaction.
-   **true** appears when the call chain is recorded during the next occurrence of the URL.

</td></tr><tr><td>

User

</td><td>

\(Optional\) If call chain recording should only take place when a specific user executes the next transaction occurrence, select the user ID. Leave it empty if you want call chain recording to occur regardless of user.

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

