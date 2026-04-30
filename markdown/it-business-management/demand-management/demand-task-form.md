---
title: Demand task form
description: Use the demand task form to create tasks for a demand.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Demand Management forms, Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Demand task form

Use the demand task form to create tasks for a demand.

<table id="demand_task_form_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Name of the demand task.

</td></tr><tr><td>

Assignment group

</td><td>

Group assigned to the demand task.

</td></tr><tr><td>

Assigned to

</td><td>

Primary resource assigned to the demand task. The following conditions apply:-   If an assignment group is defined, only users in the assignment group are listed.
-   If skills are defined, only users with those skills are listed.
-   If no assignment groups or skills are defined, only users with one of the Project Management application user roles are listed.
-   Users with `timecard_user` role are also listed.

</td></tr><tr><td>

Additional assignee list

</td><td>

Users assigned to the demand task in addition to the single primary resource defined in the **Assigned to** field.

</td></tr><tr><td>

Category

</td><td>

Category of the demand task:-   Initial review
-   Effort estimate
-   Cost estimate
-   Benefit estimate
-   Risk assessment

 The **Category** field selection determines the links available in the related links. For example, the **Add Resource Plan to Demand** related link appears when you set the **Category** value to Effort estimate. Users must have the appropriate role to use these related links.

</td></tr><tr><td>

Actual effort

</td><td>

The actual time spent working on the demand task, which is derived from the approved time card for this demand task.Because this field does not appear by default on the Demand Task form, you must add it by personalizing the form.

</td></tr><tr><td>

Description

</td><td>

Brief description of the demand task.

</td></tr><tr><td>

Number

</td><td>

System-generated ID number with a configurable prefix.

</td></tr><tr><td>

Priority

</td><td>

Sequence in which the task needs to be completed based on impact and urgency.

</td></tr><tr><td>

State

</td><td>

Current state of the demand task. The states include Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Closed Skipped.

</td></tr><tr><td>

Due date

</td><td>

The date by which the task is targeted for completion.

</td></tr><tr><td>

Actual cost

</td><td>

The actual cost of the demand task derived from the number of hours worked and hourly rate of the resource as defined in the rate card. In the absence of a rate card, the hourly rate is derived from the default labor rate card or default system property.

</td></tr><tr><td>

Work notes

</td><td>

Information about the demand task. Work notes are added throughout the demand management life cycle to communicate with other users associated with the demand.**Note:** Users with the business stakeholder role for PPM can view this field. For more information, see [Business stakeholder role for PPM](../../project-portfolio-suite-with-financials/reference/business-stakeholder-role-ppm.md).

</td></tr></tbody>
</table>**Parent Topic:**[Demand Management forms](../concept/demand-management-forms.md)

