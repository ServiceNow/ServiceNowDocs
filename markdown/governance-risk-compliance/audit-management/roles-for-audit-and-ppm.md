---
title: Roles required for Advanced planning capability and Project Portfolio Management integration
description: The advanced planning capability enables integration of Advanced Audit with the Project Portfolio Management \(PPM\) product. The capability creates an equivalent project for the engagement, and provides planning features that could be used for resource planning, cost planning, and so on, from the engagement.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Audit Management reference, Audit Management, Governance, Risk, and Compliance]
---

# Roles required for Advanced planning capability and Project Portfolio Management integration

The advanced planning capability enables integration of Advanced Audit with the Project Portfolio Management \(PPM\) product. The capability creates an equivalent project for the engagement, and provides planning features that could be used for resource planning, cost planning, and so on, from the engagement.

## Engagement planning features and roles

To use the new features of advanced planning capability, users must have the following roles:

<table id="table_dyd_fpg_nmb"><thead><tr><th>

Feature name

</th><th>

Description

</th><th>

Roles and their scope

</th></tr></thead><tbody><tr><td>

Resource Planning

</td><td>

As a resource requester, find the availability of the resources, and create and manage the resource plans for the project and project tasks in the project workspace. For more information, refer to [Create and manage resource plans for a project](https://www.servicenow.com/docs/access?context=manage-resources-for-project&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)

</td><td>

-   Users with sn\_audit.manager plus resource\_user or resource\_manager roles would be able to manage and add resource plans. Users with resource\_manager role would also be able to confirm and allocate the resource plans.
-   Users who already have access to the engagement and also have sn\_ppm\_read or timecard\_user or resource\_user roles are able to view the resource plans on the engagement.

</td></tr><tr><td>

Cost Planning

</td><td>

Project cost plans capture the costs of projects. Create a cost plan to specify the unit cost of a cost type for a fiscal period. For more information, refer to [Create a project cost plan](https://www.servicenow.com/docs/access?context=t_CreateAProjectCostPlan&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)

</td><td>

-   Users with sn\_audit.user or sn\_audit.manager plus it\_project\_manager roles would be able to manage the cost plans.
-   Users with sn\_audit.user or sn\_audit.manager plus project\_manager roles would be able to add a new cost plan.

**Note:** Users are suggested to use it\_project\_manager role instead of project\_manager role by PPM product.

-   Users who already have access to the engagement and also have sn\_ppm\_finance\_read or demand\_manager or program\_manager or portfolio\_manager or project\_manager roles are able to view the cost plans for the engagement.

</td></tr><tr><td>

Resource allocations

</td><td>

After resource requesters create a resource plan, resource managers can confirm the resources to move the plan to the Confirmed state. Resource managers can then allocate resources to the plan and move it to the Allocated state.

 Based on calendar and schedule information, resource managers view resource availability and select the resources under their management that can be confirmed and allocated to specific tasks. For more information, refer to [Resource allocation](https://www.servicenow.com/docs/access?context=r_AllocatingResources&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)

</td><td>

-   Users need both pps\_resource and sn\_audit.user or sn\_audit.external\_auditor roles to be added to the auditors field on the engagement from the resource plan.
-   Users need pps\_resource role to be added as resources to the resource plans.

</td></tr><tr><td>

Time card reporting

</td><td>

You can log hours in a time card for an engagement and other tasks on an engagement. If there is a project associated with an engagement, then the actual expenses and actual resources values roll up. To create a time card, see [Create a time card](https://www.servicenow.com/docs/access?context=t_CreateATimeCard&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

</td><td>

-   Users need timecard\_user role to create a time card.
-   Users who already have access to the engagement, audit tasks, milestones, issues and also have sn\_ppm\_read or timecard\_approver or timecard\_admin roles will be able to view all the time cards on the engagement, audit tasks, milestones, and issues.
-   Users who already have access to the engagement, audit tasks, milestones, and issues and also have the timecard\_user role will only be able to view the time cards that they have reported on the engagement, audit tasks, milestones, and issues.
-   Users need timecard\_approver role to approve a submitted time card. The time sheet policy assigned to the user governs the approval process.

</td></tr></tbody>
</table>**Parent Topic:**[Audit Management reference](audit-management-reference.md)

**Related topics**  


[Roles required for Engagement project planning for Project Portfolio Management](Engagement-project-roles-ppm.md)

