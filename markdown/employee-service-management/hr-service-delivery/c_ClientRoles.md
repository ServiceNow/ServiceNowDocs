---
title: Client roles
description: You can control what HR functionality that an employee can access using Client Roles. You can license all employees or provide HR services to users in a specific location or group.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage HR roles, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Client roles

You can control what HR functionality that an employee can access using Client Roles. You can license all employees or provide HR services to users in a specific location or group.

Client roles define access within the application. For more information, see [Manage HR roles](c_ManageRoles.md).

ServiceNow provides these roles and modifying them is not recommended. These roles can be added to other roles or groups. There are two groups:

-   HR fulfillment support: sn\_hr\_core.hrsm
-   HR Service Portal: sn\_hr\_sp.hrsp

Both roles contains conditions depending on the type of user:

-   Alumni \(only used when you have the Alumni Center installed\). For more information, see [Setting up your Alumni Center](asc-configure.md).
-   Contingent
-   Contractor
-   Employee
-   Employment Type
-   Location
-   New Hire
-   New Hires Only
-   Office Based Employees
-   Remote Employees

![List of client roles.](../image/client-roles.png "Client Roles")

**Note:** When creating an HR case and an employee does not display, ensure that the employee has any of the sn\_hr\_core.hrsm roles assigned. Also, when an employee cannot access the HR Service Portal, ensure any of the sn\_hr\_sp.hrsp roles are assigned.

Client roles are defined and administered like regular roles. ServiceNow tracks them for licensing purposes.

Assignment of client role rules is defined in the **Client Role Assignment Rules** module.

-   **[Client role assignment rules](../task/t_ClientRoleAssignRules.md)**  
Use Client Role Assignment Rules to automatically assign or reassign a role to an employee.

**Parent Topic:**[Manage HR roles](c_ManageRoles.md)

