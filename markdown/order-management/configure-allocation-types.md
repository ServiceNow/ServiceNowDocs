---
title: Configure allocation types
description: Create and activate allocation types to control how sales credits are split among multiple sales users when they work on the opportunity together.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Install and configure Opportunity Management, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Configure allocation types

Create and activate allocation types to control how sales credits are split among multiple sales users when they work on the opportunity together.

## Before you begin

Role required: sn\_opty\_mgmt\_core.opportunity\_setup\_writer

## Procedure

1.  Navigate to **All** &gt; **Opportunity Management** &gt; **Opportunity Allocation Types**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_qfj_33q_t3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique business identifier for the allocation type:-   Revenue: Distributes the total opportunity amount across eligible participants for ownership, forecasting, and credit.
-   Overlay: Distributes product or line-level opportunity value for shared credit and forecasting.
**Note:** By default, Revenue and Overlay allocation types are available.

</td></tr><tr><td>

Order

</td><td>

Determines order of display on UI and related lists wherever applicable.

</td></tr><tr><td>

Description

</td><td>

\(Optional\) Details about the opportunity allocation type.**Note:** Provides business context for administrators.

</td></tr><tr><td>

Allocation Table

</td><td>

The table or entity the allocation type applies to \(Opportunity or Opportunity Line\).

</td></tr><tr><td>

Allocation Field

</td><td>

The metric used for allocation \(for example, Amount, Cumulative TCV\).

</td></tr><tr><td>

Active

</td><td>

Determines if this allocations type is active and available for allocation processing.

</td></tr><tr><td>

Requires Full Allocation

</td><td>

Specifies whether all allocations under this type must sum to 100%.

</td></tr><tr><td>

Filter by

</td><td>

Allows to configure conditions on the Allocation object. Only records satisfying these conditions will be used for generating the final numbers.

</td></tr></tbody>
</table>    **Note:**

    You can only modify inactive allocation types.

    You can't delete allocation types if it is in use in Opportunity allocations.

4.  Select **Submit**.

    A new opportunity allocation type is created and added on the **Opportunity Allocation Types** page.


