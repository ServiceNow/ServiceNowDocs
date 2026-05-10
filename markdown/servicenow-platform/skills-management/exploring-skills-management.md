---
title: Exploring Skills Management
description: Use Skills Management to associate skills with individual users or groups and assign them to tasks or projects. You can also assess the skills needed for your organization, identify gaps, and implement effective plans for hiring or training of your teams.
locale: en-US
release: australia
product: Skills Management
classification: skills-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exploring Skills Management

Use Skills Management to associate skills with individual users or groups and assign them to tasks or projects. You can also assess the skills needed for your organization, identify gaps, and implement effective plans for hiring or training of your teams.

**Important:** Using the Skills Management application, you can create skills and skill categories manually, and also assign them manually to users. Skills Foundation uses Artificial Intelligence \(AI\) to help your organization leverage skills data for talent management and employee development. When you activate the Skills Foundation plugin \(com.sn\_skills\_int\), it also activates the Skills Management plugin \(com.snc.skills\_management\). For information on Skills Foundation, see [Skills Foundation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/talent-development-core/skills-intelligence.md).

Skills can contain other skills. For example, if you define network as a skill, you can add router as the skill it contains. A user assigned to a parent skill grants access to a child skill. Once a skill is assigned to a group, all members of the group inherit that skill and any others contained within it. Skills management works similar to ServiceNow platform [Create a role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_CreateARole.md).

Using this application, you can:

-   Manage skills for agents and your employees from a central location.
-   Use a standard way to identify skills for your organization and keep them up to date.
-   Group skills into categories and define skill levels to track the expertise of your resources at a granular level.
-   Reduce task or project reassignments by assigning tasks to agents and projects to teams that have the right skills to work on those items.
-   Identify skill gaps and resolve them by implementing effective plans for coaching and training of resources.
-   Manage the effectiveness of your team by evaluating the skills your team has and determining the skills you need for on your projects.

## Integration with ServiceNow® applications

A skill is an ability to do something that comes from training, experience, and practice. As a system administrator, you can define skills for your organization and assign it to users and groups from a central location. As an application manager, you can assign users to tasks based on these skills. For example, if you are an IT manager, you can use the Skills Management application to define skills and assign them to users and groups, which facilitates the routing of incidents to agents with relevant skills.

Group skills into categories and define skill levels to standardize skill implementation across your organization.

Use skills from the centralized location in the following applications:

-   [IT service management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/service-management-for-the-enterprise/c_AgAtAssgmtMlt.md) - As an IT manager, reduce your time and costs while resolving incidents by assigning work items to the right agent. Assess the skill gaps that agents have in your team and coach or train agents based on those needs. Identify and define a standard way to keep skill categories and levels consistent within your team.
-   [Customer service management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-assignment-workbench.md) - As a customer service manager, identify agent skills and automatically route tasks to agents who have the required skill to work on those tasks. Manage your team's effectiveness by understanding what type of skills your employees need to get hired or get trained to take on other roles.
-   [Field service management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/field-service-manager-agent-skills.md)- As a field service or customer service manager, use rules to identify skills and skill levels that agents require to resolve work items such as cases, work order tasks, and agent interactions. Automate skill assignment to reduce a manager's work load. Automatically assign tasks to agents using Field Service dynamic scheduling.
-   [Human resources management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/c_HRSkillsManagement.md) - As an HR manager, identify the types of skills your organization needs and make hiring decisions based on those needs. Manage your team's effectiveness by understanding what type of skills your employees need to get hired or get trained to take on other roles.
-   [Project portfolio management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectTasks.md) - As a project and portfolio manager, standardize how you categorize skills, define skill level types, and add skill levels for your team. Set up skills for your team in a central location and make them available within your team. Prevent project reassignments by assigning projects to the team members who have the right skills to work on them.

## Roles used in Skills Management

<table id="table_emq_gkg_nhb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill administrator \[skill\_admin\]

</td><td>

-   Inherits the skill manager \[skill\_manager\] and skill user \[skill\_user\] roles.
-   Can perform create, read, update, and delete \(CRUD\) operations on skills, skill levels, skill level types, skill categories, and sub categories.

</td></tr><tr><td>

Skill manager \[skill\_manager\]

</td><td>

-   Inherits the skill user \[skill\_user\] role.
-   Can perform read operations on skills, skill levels, skill level types, skill categories, and sub categories.
-   Can assign skills to users and groups.

</td></tr><tr><td>

Skill user \[skill\_user\]

</td><td>

Can perform read operations on skills, skill levels, and skill level types.

</td></tr></tbody>
</table>## Activating Skills Management

The Skills Management application is activated when you enable the Skills Management \(com.snc.skills\_management\) plugin.

