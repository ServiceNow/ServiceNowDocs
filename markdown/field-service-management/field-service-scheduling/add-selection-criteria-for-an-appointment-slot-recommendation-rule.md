---
title: Add selection criteria for an appointment slot recommendation rule
description: Enhance appointment booking by adding selection criteria to your recommendation rules. Selection criteria help determine the best appointment slots to recommend to your customers—ensuring optimal scheduling based on factors like proximity, skill availability, or travel time.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Appointment slot recommendation, Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Add selection criteria for an appointment slot recommendation rule

Enhance appointment booking by adding selection criteria to your recommendation rules. Selection criteria help determine the best appointment slots to recommend to your customers—ensuring optimal scheduling based on factors like proximity, skill availability, or travel time.

## Before you begin

Role required: appointment\_booking\_admin

Ensure a recommendation rule already exists, or create one first.

## About this task

By adding selection criterion for an appointment slot recommendation rule, you can

-   Offer customized recommendations based on specific factors, improving their scheduling experience.
-   Automatically prioritize slots based on what matters most, such as minimizing travel or matching customer needs.
-   Adjust how appointment slots are prioritized and displayed to users.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Recommendation rules**.

2.  Select a recommendation rule.

3.  In the **Select Criterion** module, select **New**.

4.  On the form, fill the fields.

<table id="table_y1k_44q_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Criterion

</td><td>

Select a criterion to recommend appointment slots.Field Service Management provides a default selection criterion **Proximate appointments** that recommends slots based on the appointment location.

You can use this criterion or create a new one.

**Note:** The criterion should be a scripted criterion.

</td></tr><tr><td>

Matching rule

</td><td>

Name of the recommendation rule to which this selection criterion applies.

</td></tr><tr><td>

Use for

</td><td>

Select how the criterion should be used.

-   **Ranking and Display**: Rank and visibly display the criterion.
-   **Display Only**: Display the criterion without affecting rank.
-   **Ranking and No Display**: Rank without visibly displaying the criterion.


</td></tr><tr><td>

Order

</td><td>

Order of execution of the selection criterion.

</td></tr><tr><td>

Ranking Method

</td><td>

Select how to rank the criteria.

 -   **More is better**: Higher values receive higher rank \(for example, more skill matches\).
-   **Less is better**: Lower values receive higher rank \(for example, shorter travel time\).


</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The selection criterion is added successfully to the recommendation rule.

