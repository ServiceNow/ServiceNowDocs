---
title: Assign user personas, roles, groups, and responsibilities in Urban Planning &amp; Permitting Administration
description: By default, Urban Planning &amp; Permitting Administration comes with roles and personas that can be assigned to existing users on the platform.Understand the key personas involved in Urban Planning &amp; Permitting Administration and their responsibilities in supporting land management and operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-config-uppa-assign-user-roles-responsibilities.html
release: brazil
topic_type: concept
last_updated: "2026-03-13"
reading_time_minutes: 6
breadcrumb: [Foundation, Urban Planning &amp; Permitting Administration, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Assign user personas, roles, groups, and responsibilities in Urban Planning &amp; Permitting Administration

By default, Urban Planning &amp; Permitting Administration comes with roles and personas that can be assigned to existing users on the platform.

## Assigning user roles

Assign roles to members of your land management organization Urban Planning &amp; Permitting Administration application so that your users can have delegated access to Urban Planning &amp; Permitting Administration features, capabilities, and data.

There are a few guidelines for assigning roles to users:

-   Determine who will be working on the urban planning cases for the organization, and what actions each user would be taking on the case. For more information on the roles available in Urban Planning &amp; Permitting Administration and to determine which makes sense for each user, see [Roles installed with Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/roles-installed-with-public-sector-digital-services.md) and [Urban Planning &amp; Permitting Administration Personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-config-uppa-assign-user-roles-responsibilities.md).
-   Create as many users as needed in your organization.

Role required: admin

To assign roles to a user within an organization:

1.  Make sure a user record has been created within the organization. Navigate to **All** &gt; **User Administration** &gt; **Users** to create a user record, or open an existing user record.
2.  In the **Roles** related list, select **Edit**.
3.  In the **Collection** list, select the desired roles, and then select **Add**
4.  Select **Save**.
5.  Repeat as many times as needed until all desired users are added to and associated with the organization and have the desired role.

You can also create user groups and assign roles to them. Users assigned to the group inherit the roles.

## Urban Planning &amp; Permitting Administration Personas

Understand the key personas involved in Urban Planning &amp; Permitting Administration and their responsibilities in supporting land management and operations.

### Understanding Urban Planning &amp; Permitting Administration personas

Urban Planning &amp; Permitting Administration supports collaboration between multiple personas, each playing a distinct role in managing, delivering, and consuming services. Understanding these roles helps administrators assign the right access, responsibilities, and tools within the framework.

Urban Planning &amp; Permitting Administration supports access based on predefined personas that reflect the type of work users perform within an organization. These personas can be assigned and tailored to match your organization’s needs. A persona role may contain several roles within. The roles within are automatically added to the user when the persona role is added.

ICM models this flexibility through:

-   **Personas and Roles**

    Defined at the user level. Delegates access for the user across the whole organization.

-   **Responsibilities**

    Defined according to each case, at the case level. Delegates access for the user according to the specific case.


The combination of user roles and responsibilities determines what a user can do within each organization.

### Urban Planning &amp; Permitting Administration user personas

A persona role is pre-configured role in the application that is made up of multiple granular roles, and are designed to correspond to common job titles for members of an organization. Each persona role represents a different way a user interacts with an organization or agency. The following table contains the persona roles included with the Urban Planning &amp; Permitting Administration application, and a description of each persona as it may pertain to a land management organization. For more information on the roles installed with Urban Planning &amp; Permitting Administration, including the roles contained in each persona, see [Urban Planning &amp; Permitting Administration roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/roles-installed-with-public-sector-digital-services.md).

|Persona|Description|Organization Example|
|-------|-----------|--------------------|
|Admin|An administrator is a certified ServiceNow system administrator of the organization. An administrator doesn't use the application directly, but supports configuration of the organization, hierarchy management, and assignment of member roles and responsibilities, including related-party configurations, as well as user and data management.|Admin|
|Investigator|An investigator, or case agent, works within an investigative organization to create cases, create reports, set the narrative, and create all the entities and evidence records within the case. A user or group with this role can create and work on investigative cases. An investigator can only view or work on a case within an organization if they have created it, or are added as a team member on that team. If any case tasks are assigned to them, they may work on them.|A detective \(or group of detectives\) at an investigative organization may submit a case regarding a stolen laptop. They are able to work on the case they submitted, as well as view other cases submitted by other detectives within the organization as long as they are added as a team member. They may also link other detective's cases to theirs, if they have access to that case.|
|Supervisory Agent|A supervisory agent functions similar to a manager or supervisor, reviewing and approving cases and managing an assignment group of investigators \(case agents\), for which they have full access to all cases within that group.|An investigator creates a case draft and adds the entities and support information. A supervisory agent, or supervisor, has a checkpoint to make sure all information is correct and logged, and can approve it to proceed. These agents primarily review cases rather submitting them.|
|Special Agent in Charge|The Special Agent in Charge functions as a director, focusing on the high level, overseeing the department and managing all cases created within their organization. This role allows them to create and fulfill all cases submitted in the organization.|A piece of classified evidence is added to a case, and only the special agent in charge, such as the head detective at an investigative organization, can have access to this evidence.|
|Expert Analyst|The Expert Analyst is a specialist that helps out with the case. Similar to an investigative contributor, the expert analyst may be brought in for their expertise on a subject. This role allows them to work on any part of the case if they are assigned a case task, as well as add or edit evidence and entity records.|A detective may be brought in from another department and added to the team as an expert analyst. They may work on case tasks if they are assigned to them.|
|Investigative Fulfiller \(Team member\)|The Investigative Fulfiller role functions similar to an investigator, but has less access to work on the case. They can view and edit cases to which they have a task assigned to them, and can only view and edit they are added as a team member to. They can view but not add or edit entity or evidence records.|An investigator fulfiller may be brought in from another department to contribute information to the case or complete case tasks. These agents primarily view cases and contribute information related to the case, rather than being assigned to create or work on an entire case. These team members are organization contributors.|
|Task Agent|The Task Agent is assigned to a case task of the case. They can complete case tasks, and view the details of cases for which they have tasks assigned to them.|At the investigative organization, a desk agent primarily handles administrative work, such as completing case tasks. These team members are organization contributors, and mainly view case information pertaining only to that case task.|

