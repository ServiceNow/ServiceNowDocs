---
title: Requested Allocation form
description: Use Requested Allocation form to create a request for resource plans in Planning or Rejected state.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resource Management reference, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Requested Allocation form

Use Requested Allocation form to create a request for resource plans in Planning or Rejected state.

<table id="table_df1_q3r_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start date

</td><td>

Start date for the requested allocation record.

</td></tr><tr><td>

End date

</td><td>

End date for the requested allocation record.

</td></tr><tr><td>

FTE

</td><td>

Number of units for the full-time equivalent selection for the requested allocation record.If a resource is requested as FTE, then the planned hours for each requested allocation record are calculated first. A total of all hours is then rolled up as planned hours on the resource plan. See [Resource plans](../concept/c_ResourcePlans.md) for an explanation of FTEs.

**Note:** Capacity isn’t derived from FTE, but from schedules. Both FTE and schedules must be in synchronization with each other.

</td></tr><tr><td>

Resource plan

</td><td>

Resource plan number to which the requested allocation record is attached. This field automatically populates if the requested allocation record is accessed from a resource plan.

</td></tr><tr><td>

Planned hours

</td><td>

Number of hours to allocate to the requested allocation record.By default, the [Resource Plan form](rsrc-plan-form.md) on the resource plan form are proportionally distributed among all the requested allocations based on the number of working days for each requested allocation record. However, it’s possible to override the planned hours or the FTE.

</td></tr><tr><td>

Planned cost

</td><td>

Estimated cost of resource. `Planned cost = Planned hours * hourly rate`

The hourly rate is derived from one of the following sources:

-   **Resource rate** from the resource plan, if the **Rate override** option is selected.
-   [Rate model](../../project-portfolio-suite-with-financials/concept/rate-model.md), if it’s populated on the project or demand to which the resource plan is associated.
-   Labor rate card for user resource plans.
-   Role rate when resource is requested by [resource role](../task/create-resource-role.md), if the role has a rate.
-   Group hourly rate if role doesn’t have a rate or if the role is null.
-   System property **com.snc.time\_card.default\_rate** if all the other conditions fail.

 Planned costs roll up to the **Planned cost** field on the resource plan.

</td></tr><tr><td>

Planned cost in project currency

</td><td>

Planned cost of a project task in project currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and the Project Currency view is enabled.

</td></tr><tr><td>

Planned cost in demand currency

</td><td>

Planned cost of a demand task in demand currency when the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is activated and Demand Currency view is enabled.

</td></tr></tbody>
</table>**Parent Topic:**[Resource Management reference](../task/rsrc-mgmt-reference.md)

