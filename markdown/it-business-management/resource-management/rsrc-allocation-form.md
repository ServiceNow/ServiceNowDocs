---
title: Resource Allocation form
description: Use the Resource Allocation form to resource allocations.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Resource Management reference, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource Allocation form

Use the Resource Allocation form to resource allocations.

<table id="table_df1_q3r_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start date

</td><td>

Start date for the resource allocation. The start and end dates must fall within the dates of the resource plan.

</td></tr><tr><td>

End date

</td><td>

End date for the resource allocation.

</td></tr><tr><td>

Resource

</td><td>

Resource to be allocated. The lookup results are filtered by the group, role, or user selected on the resource plan.

</td></tr><tr><td>

Confirmed/Allocated hours

</td><td>

Number of hours that the system confirms or allocates to the resource when the resource plan is confirmed or allocated. Confirmed and allocated hours roll up to the **Confirmed/Allocated hours** field on the resource plan.

</td></tr><tr><td>

FTE

</td><td>

Number of units for the full-time equivalent selection.

 This option appears if you selected **FTE** for the **Request type** field on the resource plan.

</td></tr><tr><td>

Person Days

</td><td>

Number of units for the person days selection.

 This option appears if you selected **Person Days** for the **Request type** field on the resource plan.

</td></tr><tr><td>

Planned cost

</td><td>

Planned cost of the resource.

 `Planned Cost = Planned hours * hourly rate`The hourly rate is derived from one of the following sources:

-   **Resource rate** from the resource plan, if the **Rate override** option is selected.
-   [Rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md), if it is populated on the project or demand to which the resource plan is associated.
-   Labor rate card, if rate model is not available.
-   System property **com.snc.time\_card.default\_rate** if all the other conditions fail.

 Planned costs roll up to the **Planned cost** field on the resource plan.

 The field is not visible on the form by default. Configure the form to add this field if it is not visible.

</td></tr><tr><td>

Confirmed/Allocated cost

</td><td>

Cost of the resource.

 `Confirmed/Allocated Cost = Confirmed/Allocated hours * hourly rate`

 The hourly rate is derived from one of the following sources:

-   **Resource rate** from the resource plan, if the **Rate override** option is selected.
-   Rate model, if it is populated on the project or demand to which the resource plan is associated.
-   Labor rate card, if rate model is not available.
-   System property **com.snc.time\_card.default\_rate** if all the other conditions fail.

 Confirmed and allocated costs roll up to the **Confirmed/Allocated cost** field on the resource plan.

 The field is not visible on the form by default. Configure the form to add this field if it is not visible.

</td></tr><tr><td>

Confirmed/Allocated cost in demand currency

</td><td>

Confirmed/Allocated cost of a demand task in demand currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and Demand Currency view is enabled.

</td></tr><tr><td>

Confirmed/Allocated cost in project currency

</td><td>

Confirmed/Allocated cost of a project task in project currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and Project Currency view is enabled.

</td></tr></tbody>
</table>**Parent Topic:**[Resource Management reference](../task/rsrc-mgmt-reference.md)

