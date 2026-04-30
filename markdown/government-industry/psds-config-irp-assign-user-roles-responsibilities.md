---
title: Assign user personas, roles, and groups in Information Request Playbook
description: By default, the Information Request Playbook application comes with roles, personas, and responsibilities that can be assigned to existing users on the platform.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Information Request Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Assign user personas, roles, and groups in Information Request Playbook

By default, the Information Request Playbook application comes with roles, personas, and responsibilities that can be assigned to existing users on the platform.

## Assigning user roles

Assign roles to members of your records agency Social Benefits Playbook application so that your users can have delegated access to Social Benefits Playbook features, capabilities, and data.

There are a few guidelines when assigning roles to users:

-   Determine the roles who would be working on the benefit cases for the agency, and what user would do what. For more information on the roles available in Social Benefits Playbook and to determine which makes sense for each user, see [Grants Management roles](../reference/roles-installed-with-public-sector-digital-services.md#gm-roles) and [Grants Management Personas](../reference/psds-config-gmp-personas.md)
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

There are a few guidelines for creating groups:

-   Create one group for administrators and assign the admin role to this group only.
-   Create as many groups as needed in your agency. For example, create an case agent group for each supervisory agent team, and a larger case agents group for the case agents for the entire organization, and a group for all the supervisory agents with their manager. Assign the necessary users to those groups, and then assign the necessary role to those groups if you haven't already. You can create groups first, assign a role to the group, and add users, or you can add user roles individually and then add them to the group. All users in a group will inherit the group role.

To delegate access to benefit programs and create organizational teams, you can create assignment groups.

To create a user assignment group:

1.  Navigate to **All** &gt; **User Administration** &gt; **Group** to create group record.
2.  Select a group **Name**.
3.  In the **Group Members** related list, select **Edit**.
4.  Select one or more names in the **Collection** list.
5.  Select **Add** and **Save**.
6.  Repeat as many times as needed until all desired users are added to the group.
7.  In the **Roles** related list, select **Edit**.
8.  Add the desired roles to the group.
9.  Select **Save**.

For more information on the roles available in Social Benefits Playbook and to determine which makes sense for each user, see [Social Benefits Playbook roles](../reference/roles-installed-with-public-sector-digital-services.md#sb-roles) and [../reference/psds-config-sbp-personas.md](../reference/psds-config-sbp-personas.md).

