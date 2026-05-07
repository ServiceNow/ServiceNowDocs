---
title: Assign user personas, roles, groups, and responsibilities in Investigative Case Management
description: By default, Investigative Case Management comes with roles, personas, and responsibilities that can be assigned to existing users on the platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Assign user personas, roles, groups, and responsibilities in Investigative Case Management

By default, Investigative Case Management comes with roles, personas, and responsibilities that can be assigned to existing users on the platform.

## Assigning user roles

Assign roles to members of your investigative organization Investigative Case Management application so that your users can have delegated access to Investigative Case Management features, capabilities, and data.

There are a few best practices when assigning roles to users:

-   Determine the roles who would be working on the investigative cases for the organization, and what user would do what. For more information on the roles available in Investigative Case Management and to determine which makes sense for each user, see [Roles installed with Public Sector Digital Services](../reference/roles-installed-with-public-sector-digital-services.md) and [Investigative Case Management Personas](../reference/psds-data-model-icm-personas.md)
-   Create as many users as needed in your organization.

Role required: admin

To assign roles to a user within an organization:

1.  Make sure a user record has been created within the organization. Navigate to **All** &gt; **User Administration** &gt; **Users** to create a user record, or open an existing user record.
2.  In the **Roles** related list, select **Edit**.
3.  In the **Collection** list, select the desired roles, and then select **Add**
4.  Select **Save**.
5.  Repeat as many times as needed until all desired users are added to and associated with the organization and have the desired role.

You can also create user groups and assign roles to them. Users assigned to the group inherit the roles.

## Using assignment groups to create organizational teams

There are a few best practices when creating groups:

-   Create one group for administrators and assign the admin role to this group only.
-   Create as many groups as needed in your organization. For example, create an investigator group for each supervisory agent team, and a larger investigator group for the investigators for the entire organization, and a group for all the supervisory agents with their manager. Assign the necessary users to those groups, and then assign the necessary role to those groups if you haven't already. You can create groups first, assign a role to the group, and add users, or you can add user roles individually and then add them to the group. All users in a group will inherit the group role.

To delegate access to cases and create organizational teams, you can create assignment groups. This is different from creating case teams at a case level within an investigative case in ICM, where you assign team responsibilities instead of roles. These do not affect roles at the user level. To create a user assignment group:

1.  Navigate to **All** &gt; **User Administration** &gt; **Group** to create group record.
2.  Select a group **Name**.
3.  In the **Group Members** related list, select **Edit**.
4.  Select one or more names in the **Collection** list.
5.  Select **Add** and **Save**.
6.  Repeat as many times as needed until all desired users are added to the group.
7.  In the **Roles** related list, select **Edit**.
8.  Add the desired roles to the group.
9.  Select **Save**.

For more information on the roles available in Investigative Case Management and to determine which makes sense for each user, see [Investigative Case Management roles](../reference/roles-installed-with-public-sector-digital-services.md#icm-Roles) and [Investigative Case Management Personas](../reference/psds-data-model-icm-personas.md)

## Responsibilities

The following is a list of all responsibilities that are provided with the Investigative Case Management application by default. Responsibility definitions can be used to build teams of users in the Teams tab within the Investigative Case Management workspace. You can assign these using the dropdown menus on the Teams tab. For information on creating case teams, see [Create a case team for an investigative case](../task/psds-config-icm-create-case-team.md)

Responsibilities are different than user roles; responsibilities are tied to the case only and determined at the case level. These can only be assigned once a case has been created. A user can have multiple responsibilities across cases, per case, and a user's responsibility within a case does not affect a user role.

![teams tab](../image/psds_create_team_tab.png)

The following is a list of all responsibility definitions that are provided with the Investigative Case Management application by default. Responsibility definitions can be added and removed as needed using the responsibility definition table. For information on how to configure responsibility definitions, see [Configuring Investigative Case Management responsibility definitions](psds-config-icm-create-responsibilities.md).

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

