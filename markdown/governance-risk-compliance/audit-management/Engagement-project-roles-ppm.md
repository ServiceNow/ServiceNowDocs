---
title: Roles required for Engagement project planning for Project Portfolio Management
description: The advanced planning capability enables integration of Advanced Audit with the Project Portfolio Management \(PPM\) product. The capability creates an equivalent project for the engagement, and provides planning features that could be used for resource planning, cost planning, and so on, from the engagement project.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Audit Management reference, Audit Management, Governance, Risk, and Compliance]
---

# Roles required for Engagement project planning for Project Portfolio Management

The advanced planning capability enables integration of Advanced Audit with the Project Portfolio Management \(PPM\) product. The capability creates an equivalent project for the engagement, and provides planning features that could be used for resource planning, cost planning, and so on, from the engagement project.

## Engagement-project planning features and roles

To understand the roles required for using the engagement-project planning features, see the following table:

<table id="table_byp_frg_nmb"><thead><tr><th>

Feature

</th><th>

Description

</th><th>

Roles and their scope

</th></tr></thead><tbody><tr><td>

Resource planning

</td><td>

As a resource requester, find the availability of the resources, and create and manage the resource plans for the project and project tasks in the project workspace. For more information, refer to [Create and manage resource plans for a project](https://www.servicenow.com/docs/access?context=manage-resources-for-project&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)

</td><td>

-   Users with at least resource\_user role can add resource plans using the **New** button and with it\_project\_manager role can manage and add new resource plans using the **Manage** button. Users with resource\_manager role would be able to confirm and allocate resource plans.
-   Users with sn\_ppm\_read or timecard\_user or resource\_user role would be able to see the resource plans for the engagement project.

</td></tr><tr><td>

Cost planning

</td><td>

Project cost plans capture the costs of projects. Create a cost plan to specify the unit cost of a cost type for a fiscal period. For more information, refer to [Create a project cost plan](https://www.servicenow.com/docs/access?context=t_CreateAProjectCostPlan&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)

</td><td>

-   Users with sn\_audit.user or sn\_audit.manager role and it\_project\_manager would be able to manage the cost plan. Users with the it\_project\_manager role can add new cost plans. Users with sn\_audit.user or sn\_audit.manager and project\_manager role would be able to add a new cost plan.
-   Users with sn\_audit.user or sn\_audit.manager role and project\_manager role would be able to add a new cost plan. Users are suggested to use the it\_project\_manager role instead of project\_manager role by PPM. Users with the it\_project\_manager role can also add new cost plans.

</td></tr><tr><td>

Related links on Engagement project

</td><td>

Users can enter the project budget, move projects, calculate completion estimates for the engagement project using the related links which appear based on the roles and permissions.

</td><td>

-   Users need portfolio\_manager role to create project budget. If a user role is being added manually, use the it\_portfolio\_manager role instead of portfolio\_manager role.
-   Users need project\_manager role to be able to calculate completion estimates, and move project. If a user role is being added manually, use the it\_project\_manager role instead of project\_manager role.

</td></tr></tbody>
</table>**Parent Topic:**[Audit Management reference](audit-management-reference.md)

**Related topics**  


[Roles required for Advanced planning capability and Project Portfolio Management integration](roles-for-audit-and-ppm.md)

