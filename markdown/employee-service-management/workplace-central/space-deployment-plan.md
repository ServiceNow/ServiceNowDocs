---
title: Space Deployment Plan
description: A space deployment plan contains information about how the changes made in the scenario impact the building's spaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/space-deployment-plan.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Space Deployment Plan

A space deployment plan contains information about how the changes made in the scenario impact the building's spaces.

<table><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Space

</td><td>

Workplace location that is used for the scenario-related change.

</td></tr><tr><td>

Floor

</td><td>

Floor of the workplace location.

</td></tr><tr><td>

Building

</td><td>

Building of the workplace location.

</td></tr><tr><td>

Type of change

</td><td>

Type of change made to the space in the scenario plan.The value in this column can be `Allocation`, `Assignment type`, or `(empty)` based on the changes made to the workplace location.

For example, if a space was allocated to IT Support, and the scenario allocates the space to HR and Finance, the Type of change is `Allocation`.

</td></tr><tr><td>

Current value

</td><td>

Current allocation or assignment type value of the workplace location.The value in this column depends on the type of change made to the workplace location.

For example, if a space was allocated to IT Support, and the scenario allocates the space to HR and Finance, the current value is `IT Support`.

</td></tr><tr><td>

Scenario value

</td><td>

Allocation or assignment type value of the workplace location in the scenario.The value in this column depends on the type of change made to the workplace location.

For example, if a space was allocated to the Workplace Entity IT Support, and the scenario allocates the space to HR and Finance, the scenario value is `Workplace Entities: HR, Finance`.

</td></tr><tr><td>

Updates

</td><td>

Number of updates that are made to the workplace location in the scenario.

</td></tr><tr><td>

Updated

</td><td>

Timestamp of the last change made to the workplace location.

</td></tr><tr><td>

Workplace case

</td><td>

Workplace case record that is created for allocation changes to the workplace location.Workplace cases are created after a scenario is deployed. The value in this column is empty for assignment type changes.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Central reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/workplace-central-references.md)

**Related topics**  


[Components installed with Workplace Central]()

[Space Optimization - Key features and actions]()

[Workplace Central Event planner]()

[Scenario and Building - Views, states, settings, and key features]()

[Space request approvals, states, actions, and key features]()

[Move management key features and actions]()

[Case Management - Key features, Actions &amp; Case details]()

[Schedule Plan details form]()

[Scenario details form]()

[User Deployment Plan]()

[Excel column lengths for move projects]()

[Move conflicts for projects created via Excel upload]()

[Workplace Central troubleshooting]()

[Workplace Task form - Space Assignment task]()

[Neighborhood User Assignment Rule form]()

[User Workplace Profile form]()

