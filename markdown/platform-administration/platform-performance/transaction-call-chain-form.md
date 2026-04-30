---
title: Transaction call chain form
description: A description of the fields in the Transaction Call Chain form.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Platform performance, Maintain and monitor, Administer]
---

# Transaction call chain form

A description of the fields in the Transaction Call Chain form.

<table id="table_ocr_xjm_3fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Table

</td><td>

Source table for the script resource executed in the call chain.

</td></tr><tr><td>

Source

</td><td>

Script resource executed in the call chain.

</td></tr><tr><td>

Persisted Sequence

</td><td>

Order in which the script executed in the call chain.

</td></tr><tr><td>

Call Depth

</td><td>

Depth of the executed call chain.For example, a script calling a script include, which in turn calls another script include would have at least three rows. One row has a depth of 1, the second row has a depth of 2, and the third row has a depth of 3.

</td></tr><tr><td>

Trigger Table

</td><td>

Name of trigger table, if any, for the executed call chain component.

</td></tr><tr><td>

Duration\(ms\)

</td><td>

Observed duration of the script execution, in milliseconds.

</td></tr><tr><td>

Transaction Log

</td><td>

Transaction log ID created for the recorded call chain.

</td></tr></tbody>
</table>**Parent Topic:**[Platform performance reference](../concept/platform-performance-references.md)

