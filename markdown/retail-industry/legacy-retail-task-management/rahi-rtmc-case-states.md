---
title: Retail multi-store case states
description: The following table lists all possible states for the Retail multi-store parent case.
locale: en-US
release: yokohama
product: \[Legacy\] Retail Task Management
classification: legacy-retail-task-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create multi-store cases in Retail Task Management Core, Retail Task Management, Retail]
---

# Retail multi-store case states

The following table lists all possible states for the Retail multi-store parent case.

## Retail multi-store parent case states

The following table lists all possible states for the Retail multi-store parent case.

<table id="table_o3v_pgh_b2c"><tbody><tr><td>

**State**

</td><td>

**Description**

</td></tr><tr><td>

Draft

</td><td>

Indicates that parent case is still in draft state and hasn’t yet been submitted.

</td></tr><tr><td>

Generating

</td><td>

Indicates that the parent case has been submitted, and child cases are currently being generated.

</td></tr><tr><td>

Open

</td><td>

Indicates that the parent case is open.

</td></tr><tr><td>

Canceled with error\(s\)

</td><td>

Indicates that the parent case has been canceled, typically due to an instance or platform issue. Any child cases that were generated will be canceled automatically, and this parent case must be re-created.

</td></tr><tr><td>

Closed

</td><td>

Indicates that the parent case is closed.

</td></tr></tbody>
</table>## Retail multi-store child case states

<table id="table_fh3_sgh_b2c"><tbody><tr><td>

**State**

</td><td>

**Description**

</td></tr><tr><td>

New

</td><td>

Indicates that the child case is newly created.

</td></tr><tr><td>

Open

</td><td>

Indicates that the child case is open.

</td></tr><tr><td>

Canceled with error\(s\)

</td><td>

Indicates that the parent case has been canceled, typically due to an instance or platform issue. Any child cases that were generated are automatically, and this parent case must be re-created.

</td></tr><tr><td>

Resolved

</td><td>

Indicates that the child case has been marked as resolved.

</td></tr><tr><td>

Closed

</td><td>

Indicates that the child case is closed.

</td></tr></tbody>
</table>