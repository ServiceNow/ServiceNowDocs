---
title: Employee Relations case restrictions
description: Use Case Restriction Configuration to determine what groups and agents can access or restrict ER cases.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Employee Relations case restrictions

Use Case Restriction Configuration to determine what groups and agents can access or restrict ER cases.

## Groups

Restrict access by Center of Excellence \(COE\) for specific groups:

-   Define what groups can restrict ER cases.
-   Define what groups can view ER cases.

The base system provides one case restriction configuration that enables the HR Confidential group to access ER cases.

For more information, see [Manage HR Groups](../task/t_ManageHRGroups.md).

**Note:** When creating case restrictions, be sure that you have at least one configuration that enables you to read these cases.

## Roles

Members of groups that can access ER cases must have the sn\_hr\_er.confidential role.

For more information, see [Manage HR roles](c_ManageRoles.md) and [Evidence Management for Employee Relations](hr-er-evidence-mgmt.md#).

## COE Security Configuration

Use COE Security Configuration to define group restrictions for a COE and for all or specific HR services under it.

You can then restrict the COE with read and write capabilities.

**Note:** If you choose to restrict other COEs besides Employee Relations Case \[sn\_hr\_er\_case\], you can cause performance issues. ER cases numbering more than 100 K can impact performance.

For more information, see [Create a COE security policy](../task/hr-create-coe-security-policy.md).

COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are ServiceNow ACLs.

Collaborators and the COE for the HR case can conflict. The basic rules are:

-   For all HR cases, collaborators override any security on a COE.
-   Employee Relations \(ER\) cases can override collaborators when restrictions apply.

## ER assignment rules

Use ER assignment rules to assign a group to an ER case.

For more information, see [Employee Relations assignment rules](hr-er-assign-rules.md).

## ER matching rules

Use ER matching rules to assign an agent that has the least number of cases, the required skills, and matches the location.

For more information, see [Employee Relations matching rules](hr-er-matching-rules.md).

