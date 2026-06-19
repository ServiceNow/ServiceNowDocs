---
title: Assign user personas, roles, groups, and responsibilities in Grants Management
description: By default, Grants Management comes with roles, personas, and responsibilities that can be assigned to existing users on the platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/public-sector-digital-services/psds-config-gmp-assign-user-roles-responsibilities.html
release: zurich
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Foundation, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Assign user personas, roles, groups, and responsibilities in Grants Management

By default, Grants Management comes with roles, personas, and responsibilities that can be assigned to existing users on the platform.

## Assigning user roles

Assign roles to members of your grants organization Grants Management application so that your users can have delegated access to Grants Management features, capabilities, and data.

There are a few guidelines when assigning roles to users:

-   Determine the roles who would be working on the grant cases for the agency, and what user would do what. For more information on the roles available in Grants Management and to determine which makes sense for each user, see [Grants Management roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/roles-installed-with-public-sector-digital-services.md) and [Grants Management Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-personas.md)
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
-   Create as many groups as needed in your organization. Assign the necessary users to those groups, and then assign the necessary role to those groups if you haven't already. You can create groups first, assign a role to the group, and add users, or you can add user roles individually and then add them to the group. All users in a group will inherit the group role.

To delegate access to grants programs and create organizational teams, you can create assignment groups. This is different from creating internal program teams within a grant program in Grants Management. These are responsibilities that are assigned at the grant program level within the playbook, and adding a user to either of these grant program-level groups do not affect roles at the user and agency level. For information on how to create an internal program team and external reviewer group, see [Add members to a Grant Program internal program team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-gmp-using-add-members-internal-program-team.md) and [Add external reviewer groups in Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-reviewer-team.md).

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

For more information on the roles available in Grants Management and to determine which makes sense for each user, see [Grants Management roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/roles-installed-with-public-sector-digital-services.md) and [Grants Management Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-personas.md)

## Internal Program Team Responsibilities

The following is a list of all internal program team responsibilities that are provided with the Grants Management application by default. You can assign these using the dropdown menus in the Internal Program team activity of the playbook. For information on creating internal program teams, see [Add members to a Grant Program internal program team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-gmp-using-add-members-internal-program-team.md)

Program team responsibilities are different than user roles; responsibilities are tied to the grant program only and determined at the grant program case level. These can only be assigned once a program has been created. A user can have multiple responsibilities across grant programs, per program, and a user's responsibility within a program does not affect a user role.

The following is a list of all internal program team responsibilities that are provided with the Grants Management application by default.

-   Approver
-   Collaborator
-   Observer
-   Program Lead
-   Program Co-lead

-   **[Grants Management Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-personas.md)**  
Understand the key personas involved in Grants Management and their responsibilities in supporting grants.
-   **[Configure read/write access roles for the Grants Management internal program team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-internal-team-default-roles.md)**  
In a Grant Program, certain access is granted to each Internal Program Team user on a case-by-case basis. As an admin, you can delegate read/write access to users within internal teams by mapping specific roles to read/write access.

**Parent Topic:**[Configure Grants Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-foundation.md)

**Previous topic:**[Configure Restricted Caller Access \(RCA\) for Document Templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-fdtn-doc-template-rca.md)

**Next topic:**[Grants Management Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/public-sector-digital-services/psds-config-gmp-personas.md)

