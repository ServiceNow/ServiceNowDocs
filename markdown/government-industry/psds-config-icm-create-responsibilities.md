---
title: Configuring Investigative Case Management responsibility definitions
description: Configure responsibilities within a case, such as Crime Lab Technician, that can be assigned to users at the case level.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Assign personas, roles, responsibilities, and groups, Foundation, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configuring Investigative Case Management responsibility definitions

Configure responsibilities within a case, such as Crime Lab Technician, that can be assigned to users at the case level.

## Before you begin

Role required: admin

## About this task

A responsibility, or responsibility definition, specifies the role or function a user has within an entity or organization, determining access through relationships. When creating a relationship, users are assigned specific responsibilities that grant access to the entity and its related entities. In Investigative Case Management, responsibility definitions are used to delegate case access to team members working on an investigative case in the ICM workspace.

You can use the responsibility definitions provided with the Investigative Case Management application to create teams. By default, Investigative Case Management comes with the following responsibility definitions that can be assigned within the case.

|Responsibility| |
|--------------|---|
|Case Agent| |
|Coroners Office Liason| |
|Crime Lab Technician| |
|District Attorney| |
|Expert Analyst| |
|Internal Affairs Officer| |
|Investigative Assistant| |
|Special Agent in Charge| |
|Supervisory Agent| |

For information on the responsibilities provided with ICM, see [Assign user personas, roles, groups, and responsibilities in Investigative Case Management](psds-config-icm-assign-user-roles-responsibilities.md).

As an admin, you can also modify these role responsibility definitions or create your own to meet your organization requirements and match common team member responsibilities within your investigations.

## About this task

**Note:** If you modify the existing definitions or create definitions, you must update access control lists \(ACLs\) to reflect the changes.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**, or enter `sn_customerservice_responsibility_def.list` in the navigation filter.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Name|Name of the responsibility. For example, Probation Officer.|
    |Type|Type of users to whom the responsibility can be assigned to. Select **User** if this responsibility should be assigned to an employee or user within the organization. When assigning this type, the list of available users comes from the users \[sys\_users\] table.|
    |Unique|Option that you can select to disable the duplicate entries for the responsibility definition. Leave this box unchecked.|

4.  Select **Submit**.

    The new responsibility definition is created, and can be used to create teams at the case level within the investigative case record. To assign a responsibility to a team member within a case, see [Create a case team for an investigative case](../task/psds-config-icm-create-case-team.md).


