---
title: Create or modify an appointment booking slot recommendation rule
description: Appointment booking slot recommendation rules help you highlight the best appointment slots for your customers. Using these rules, you can categorize available appointment slots as recommended or available based on conditions you define, such as proximity, resource availability, or customer preferences.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Enable and configure appointment slot recommendation, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Create or modify an appointment booking slot recommendation rule

Appointment booking slot recommendation rules help you highlight the best appointment slots for your customers. Using these rules, you can categorize available appointment slots as recommended or available based on conditions you define, such as proximity, resource availability, or customer preferences.

## Before you begin

Role required: admin

## About this task

Appointment Booking uses appointment slot recommendation rules to categorize the available slots for a service into recommended slots and available slots. Slot recommendation rules let you control how the appointment booking slots should be categorized.

An appointment slot is designated as a recommended slot if it meets the conditions defined in the rule.

By creating slot recommendation rules, you can

-   Guide customers to the most suitable appointment slots.
-   Prioritize slots to optimize service efficiency.
-   Create multiple rules to precisely match your organization's scheduling goals.

When seismic appointment booking Calender is activated, it uses these recommendation rules to display the recommended slots for a service.

Field Service Management provides default slot recommendation rule, known as the **Appointment slot recommendation rule**. You can modify this default rule or use it as a template to create new rules.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Recommendation rules**.

2.  Create or modify a rule.

    -   To create a new rule, select **New**.
    -   To modify a rule, select the rule name.
3.  In the form, fill the fields.

<table id="table_crz_zc2_ldc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the slot recommendation rule.

</td></tr><tr><td>

Active

</td><td>

Select to activate the recommendation rule.

</td></tr><tr><td>

Execution Order

</td><td>

Set the priority for the recommendation rule. -   Rules with lower execution order values run first.
-   Higher values run later to further refine the recommendations.


</td></tr><tr><td>

Table

</td><td>

Select the table to apply this rule to. The default table is **Appointment Booking Service Configuration**.

</td></tr><tr><td>

Conditions

</td><td>

Define the conditions slots must meet to be recommended. For example, proximity or specific resource availability.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

Your appointment booking slot recommendation rule is created or updated. Appointment slots are categorized as recommended based on your specified conditions.

## What to do next

Enhance appointment booking by adding selection criteria to your recommendation rules. Selection criteria help determine the best appointment slots to recommend to your customers, ensuring optimal scheduling based on factors like proximity, skill availability, or travel time. For more information, see [Add selection criteria for an appointment slot recommendation rule](add-selection-criteria-for-an-appointment-slot-recommendation-rule.md).

