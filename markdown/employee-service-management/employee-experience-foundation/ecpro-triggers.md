---
title: Campaign bundle triggers
description: Define a trigger to make the content in the campaign stage available to employees.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating campaigns, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Campaign bundle triggers

Define a trigger to make the content in the campaign stage available to employees.

A campaign bundle organizes and manages the delivery of campaign content. When configuring a bundle, you set the bundle trigger, which determines when content becomes available and for how long.

**Note:** The interface use the terms "bundle" and "stage" interchangeably.

<table id="table_wkx_tbv_gbc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Immediate

</td><td>

The content is visible to the audience immediately after campaign publication, for the duration of the campaign.[Create a campaign stage with immediate trigger](../task/create-stage-immediate-trigger.md)

</td></tr><tr><td>

Fixed date

</td><td>

The content becomes available according to a specific start and end date and time and within the start and end date and time of the campaign.

</td></tr><tr><td>

Recurring

</td><td>

Use to create a campaign stage \(bundle\) that has date-based repeatable content. For example, use this trigger for content specific to employee birthdays or work anniversaries.[Create a campaign stage with recurring trigger](../task/create-stage-recurring-trigger.md)

</td></tr><tr><td>

To-do completion

</td><td>

The content in this campaign stage becomes available when a user completes a specific to-do item from another stage in the campaign.[Create a campaign stage with to-do trigger](../task/create-stage-to-do-trigger.md)

</td></tr><tr><td>

Dynamic

</td><td>

The campaign stage triggers when a field in a table \(sn\_hr\_core\_profile or sys\_user\) fulfills a specific condition. An example use case for this trigger type is a new hire campaign, where each stage contains onboarding content for each week and delivers the content based on the employment start date.**Note:** The dynamic stage trigger will show content only one time. To configure a stage that is triggered on a repetitive basis, such as on an annual basis, use the recurring trigger.

[Create a campaign stage with dynamic trigger](../task/create-stage-dynamic-trigger.md)

</td></tr><tr><td>

Condition

</td><td>

This trigger type is specifically for Employee Journeys: Parental Leave of Absence. You can use it for your process, but it is an advanced feature that requires building a triggering mechanism, such as a business rule or scripting.[Create a campaign stage with condition trigger](../task/create-stage-condition-trigger.md)

</td></tr></tbody>
</table>