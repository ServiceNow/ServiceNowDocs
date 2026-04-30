---
title: Create demand task form
description: The demand task form information is used to create a demand task for the demand.
locale: en-US
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Form field information, Reference, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Create demand task form

The demand task form information is used to create a demand task for the demand.

<table id="demand_task_form_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

A brief summary of the task, which helps quickly identify the purpose or nature of the work.

</td></tr><tr><td>

Assignment group

</td><td>

Team or group responsible for handling the task.

</td></tr><tr><td>

Number

</td><td>

System-generated ID number with a configurable prefix.

</td></tr><tr><td>

Assigned to

</td><td>

Primary resource responsible for executing or progressing the task. The following conditions apply:-   If an assignment group is defined, users in the assignment group are listed.
-   If skills are defined, users with those skills are listed.
-   If no assignment groups or skills are defined, users with one of the Project Management application user roles are listed.
-   Users with the timecard\_user role are also listed.

</td></tr><tr><td>

Priority

</td><td>

Indicates the urgency and importance of the task. Determines how quickly it should be addressed.

</td></tr><tr><td>

Additional assignee list

</td><td>

Users assigned to the demand task in addition to the single primary resource defined in the **Assigned to** field.

</td></tr><tr><td>

State

</td><td>

Current state of the demand task. All new demand task records are created in the Open state.The states include:

-   Pending
-   Open
-   Work in Progress
-   Closed Complete
-   Closed Incomplete
-   Closed Skipped

</td></tr><tr><td>

Category

</td><td>

Category of the demand task.The categories include:

-   Initial review
-   Effort estimate
-   Cost estimate
-   Benefit estimate
-   Risk assessment

</td></tr><tr><td>

Due date

</td><td>

The expected completion date and time for the task.

</td></tr><tr><td>

Actual effort

</td><td>

The actual time spent working on the demand task, which is derived from the approved time card for this demand task.You must add this field by personalizing the Create New Demand Task form as this field doesn’t appear by default on the form.

</td></tr><tr><td>

Actual cost

</td><td>

The actual cost of the demand task derived from the number of hours worked and hourly rate of the resource as defined in the rate card. In the absence of a rate card, the hourly rate is derived from the default labor rate card or default system property.

</td></tr><tr><td>

Description

</td><td>

Brief description of the demand task.

</td></tr><tr><td>

Work notes

</td><td>

Information about the demand task. Work notes are added throughout the demand management life cycle to communicate with other users associated with the demand.

</td></tr></tbody>
</table>