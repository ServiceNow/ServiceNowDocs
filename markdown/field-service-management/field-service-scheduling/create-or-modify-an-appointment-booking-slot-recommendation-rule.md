---
title: Create or modify an appointment booking slot recommendation rule
description: Create modify a appointment booking slot recommendation rules to categorize the appointment booking slots into recommended slots and available slots.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Appointment slot recommendation, Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create or modify an appointment booking slot recommendation rule

Create modify a appointment booking slot recommendation rules to categorize the appointment booking slots into recommended slots and available slots.

## Before you begin

Role required: appointment\_booking\_admin

## About this task

Appointment Booking uses appointment slot recommendation rules to categorize the available slots for a service into recommended slots and available slots. Slot recommendation rules let you control how the appointment booking slots should be categorized.

An appointment slot is designated as a recommended slot if it meets the conditions defined in the rule.

By defining the rules, you can ensure that the appointment slots are well utilized based on your organization’s specific needs. Multiple rules can be created and applied in a sequence, based on execution order, to give you maximum flexibility and precision.

When seismic appointment booking Calender is activated, it uses these recommendation rules to display the recommended slots for a service.

Field Service Management provides default slot recommendation rule, known as the **Appointment slot recommendation rule**. You can modify this default rule or use it as a template to create new rules.

## Procedure

1.  Navigate to **All** &gt; **Appointment Booking** &gt; **Recommendation rules**.

2.  To create a new rule, click **New**.

    To modify a rule, click the rule name.

3.  In the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the slot recommendation rule.|
    |Active|Select to activate the recommendation rule.|
    |Execution Order|Set the priority for the recommendation rule. Rules with lower execution order values are applied first. Higher values further refine the list.|
    |Table|The table to which this recommendation rule applies. The default table is Appointment Booking Service Configuration.|
    |Conditions|Specify the conditions that will identify which slots to include in the filter.|

4.  Select **Submit**.


## Result

The slot recommendation rule is created or modified.

## What to do next

Add one or more selection criteria for the determination rule. For more information, see [Add selection criteria for an appointment slot recommendation rule](add-selection-criteria-for-an-appointment-slot-recommendation-rule.md).

