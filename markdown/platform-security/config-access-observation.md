---
title: Configure access observation
description: Create an access observation record to review access to a data column during a specified time window.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access observer]
---

# Configure access observation

Create an access observation record to review access to a data column during a specified time window.

## Before you begin

Role required: security\_admin

## Procedure

1.  Navigate to **All** &gt; **Access Observer** &gt; **Access Observer Configuration**.

2.  Select **New** to create a record.

3.  On the form, fill in the fields.

<table id="table_ggl_1lb_qbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Whether the record is active. Your record is automatically marked active during the observation period and is inactive otherwise.

</td></tr><tr><td>

Application

</td><td>

The scoped application for the record. This field is read only.

</td></tr><tr><td>

Table

</td><td>

Table that contains the column to be observed

</td></tr><tr><td>

Column

</td><td>

The column within the selected table to be observed. The following field types are supported:-   Email
-   Date
-   Date/Time
-   Journal
-   Journal Input
-   Phone number \(E164\)
-   String
-   String \(UTF-8\)
-   Translated
-   Translated Field
-   Translated HTML
-   Translated Text
-   URL


</td></tr><tr><td>

Start job immediately

</td><td>

If selected, observation begins as soon as the record is created.

</td></tr><tr><td>

End date and time

</td><td>

The time at which observation ends.

</td></tr><tr><td>

Start date and time

</td><td>

The time at which observation begins. This field is only visible if **Start job immediately** isn’t selected.

</td></tr></tbody>
</table>4.  Select **Submit** to save the record.


## What to do next

Once the observation window your defined has started, you can see each instance where the column was access detailed in the records on the Access Observer log \[sys\_data\_ob\_log\] table.

**Parent Topic:**[Access observer](../concept/access-observer.md)

