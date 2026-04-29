---
title: Create a subject criteria condition
description: Create a condition to compare a user information against existing subject criteria input.
locale: en-US
release: australia
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create subject criteria, Data filtration\(Legacy\), Access Management]
---

# Create a subject criteria condition

Create a condition to compare a user information against existing subject criteria input.

## Before you begin

Role required: security\_admin

Criteria conditions compare user attributes against existing criteria inputs to determine whether to allow access to records. In order to create a criteria condition, you need to have created subject criteria. For details on that process see, [Create a subject criteria input](df-create-subject-crit-inputs.md).

## Procedure

1.  On your subject criteria record, open the **Criteria Conditions** tab.

2.  In the **Criteria Conditions** list, click **New**.

3.  On the **Subject Criteria Condition** form, fill in the fields as needed.

    |Field|Description|
    |-----|-----------|
    |Label|A descriptive label for your condition|
    |Application|Scoped application for the subject criteria. This field is read-only, and automatically populates with the current scoped application.|

4.  Create a condition for your subject criteria condition using the condition builder by selecting from the following condition options.

    These condition options include any subject criteria inputs you have created.

5.  Create more conditions by clicking the **Add filter condition** or **Add "OR" clause** buttons.

    **Note:** Unless your conditions are separated by an **or** clause, all conditions must evaluate to true in order for the subject criteria condition to evaluate to true.

6.  Click **Submit** to save the subject criteria condition.


## What to do next

Use subject criteria in your data filtration rules to limit access to tables and records. For details on how to use subject criteria in data filtration rules, see [Create subject criteria](df-create-criteria.md).

