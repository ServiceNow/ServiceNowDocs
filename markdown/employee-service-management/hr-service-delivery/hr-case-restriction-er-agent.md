---
title: HR Service Delivery case restrictions for an Employee Relations agent
description: Even Employee Relations agents with special privileges to view and modify a case are limited from viewing, modifying or restricting a case under certain circumstances for security purposes.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Employee Relations, Employee Relations cases, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR Service Delivery case restrictions for an Employee Relations agent

Even Employee Relations agents with special privileges to view and modify a case are limited from viewing, modifying or restricting a case under certain circumstances for security purposes.

An Employee Relations agent is treated as a normal employee and does not have any kind of special privileges if the agent meets one of the following criteria:

-   The person for whom the case was opened.
-   An involved party in a case.
-   A subject person.

Restrictions are enabled for the Employee Relations agent in the following areas of the ServiceNow instance:

## UI actions

Actions such as Update, Ready for Work, and Cancel that are available to regular employees are also available to the agent. Actions such as Associate Interaction, Delete, Close Complete, Close Incomplete, and Suspend are not available.

## View

Can view only the restricted self-service view of the case on the Agent Workspace, the platform view, and the Employee Center. The agent cannot change the view.

## Access to related lists and records

No access to the related lists and related records for a case, for example, allegations, involved parties, interviews, evidence, and so on. The agent cannot access the related records in the platform view.

## Access to tasks

Can view only the tasks assigned to them and not tasks assigned to other employees.

## Case restriction configuration

Case restriction configuration enables the HR confidential group members to restrict a case using the **Restrict** button available on the case.

Restricting a case means that even if an Employee Relations agent is part of the HR confidential group and is involved in a case, the agent will not have access to that case. For more information on case restriction, see [Configure an employee relations case restriction](../task/hr-er-create-case-restriction.md).

## Security Configuration

For Employee Relations COE \(Center of Excellence\), the HR matching rules skip any Employee Relations agent who meets the criteria so that the case is not assigned to them. For more information, see [Create a COE security policy](../task/hr-create-coe-security-policy.md).

COE security policies are a way to easily restrict access to different COEs via configuration. The underlying COE security policy implementations are [ServiceNow ACLs](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

