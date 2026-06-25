---
title: User Deployment Plan
description: A user deployment plan contains information about how the changes made in the scenario impact the employees and their workplace locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-central/user-deployment-plan.html
release: australia
product: Workplace Central
classification: workplace-central
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# User Deployment Plan

A user deployment plan contains information about how the changes made in the scenario impact the employees and their workplace locations.

<table><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

User who is impacted by the scenario-related change.

</td></tr><tr><td>

Operation

</td><td>

Type of operation that is made in the scenario.-   Insert: The user is assigned a new space in the scenario
-   Update: The user's assigned space is changed in the scenario
-   Delete: The user's assignment is removed in the scenario
-   Orphan: The user's neighborhood is resized to 0 in the scenario, so the user's assignment to the neighborhood on the corresponding floor has become orphaned.

</td></tr><tr><td>

From workplace location

</td><td>

Current workplace location that is assigned to the user.

</td></tr><tr><td>

Workplace location

</td><td>

Workplace location assigned to the user in the scenario plan.

</td></tr><tr><td>

Parent

</td><td>

Parent of the assigned workplace location.The system displays up to 2 parents based on the location hierarchy.

</td></tr><tr><td>

Workplace case

</td><td>

Workplace case record that is created for assignment changes of the user.Workplace cases are created after a scenario is deployed.

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

[Space Deployment Plan]()

[Excel column lengths for move projects]()

[Move conflicts for projects created via Excel upload]()

[Workplace Central troubleshooting]()

[Workplace Task form - Space Assignment task]()

[Neighborhood User Assignment Rule form]()

[User Workplace Profile form]()

