---
title: Configuring Skills Foundation
description: As an admin, add skills and import data into job architecture tables in your ServiceNow instance to start using Skills Foundation in your organization.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Configuring Skills Foundation

As an admin, add skills and import data into job architecture tables in your ServiceNow instance to start using Skills Foundation in your organization.

## Plugin dependencies

-   Skills Management \(com.snc.skills\_management\)
-   Data Services Base Client \(com.glide.data\_services.base\)
-   Skills Library Data for Skills Management \(com.snc.skills\_management.seed\_data\)

## App dependencies

Employee profile \(sn\_employee\) version 8.0.2.

## Other requirements

-   To access multi-channel prompts, you must have Proactive Prompts \(com.sn\_pp\) version 2.0.0 installed.
-   Employee profiles must exist. For more information, see [Employee profile](../../employee-center/concept/employee-profile-portal.md).

## Setup process

The following procedure describes the steps to install Skills Foundation, upload or create the required data, and start using Skills Foundation in your organization.

**Note:** A successful Skills Foundation installation requires the Skills Workspace plugin, use the Guided setup to install and configure the Skills Foundation application instead of a manual process.

1.  Install the Skills Foundation \[com.sn\_skills\_int\] plugin.
2.  Install the Skills Library Data for Skills Management \(com.snc.skills\_management.seed\_data\) plugin.
3.  \(Optional\) Install the Proactive Prompts plugin, which provides access to multi-channel prompts. For more information, see [Install Proactive Prompts](../../human-resources/task/proactive-prompts-install.md).
4.  Load customer industry skills data. For more information, see [Load your custom skills into Skills Foundation](../task/skills-int-load-custom-skills.md).
5.  Upload job architecture data. For more information, see [About Job Architecture](job-architecture.md).
6.  \(Optional\) Create a job level progression from a job level to a higher job level to indicate the growth path for employees in your organization. For more information, see [Creating a job level progression](../task/skills-int-job-level-progress.md).

    **Note:** Although this step is optional, creating job level progressions enables you to obtain skill-based suggestions for employee career progression as part of employee growth and development. For more information, see [Talent Development Core](../../employee-service-management/concept/egd-landing-page.md).

7.  \(Optional\) Create a configuration that sets the proficiency automatically for skills across role levels based on the skill level type and role group. For more information, see [Set the job proficiency level automatically](../task/proficiency-autofill-config.md).
8.  \(Optional\) Create role groups and role levels based on the type of roles in your organization. For more information, see [Adding role groups and role levels for skills administration](../task/skills-int-add-role-group.md).
9.  Create role-level mapping to industry titles. For more information, see [Map industry titles to role levels](../task/skills-int-map-ind-titles-role-level.md).
10. Assign a role level to an employee using Proactive Prompts or manually. For more information, see [Map a role level to the employee profile](../task/skills-int-attach-role-level-emp.md).
11. Assign users to roles to enable them to perform tasks in Skills Foundation. For more information, see [Components installed with Skills Foundation](../reference/skills-intelligence-users-and-roles-1.md).
12. Provide access to the Skills widget where employees can view and edit skills in their profile in Employee Portal by setting the **sn\_skills\_int.enable\_skills** system property to True.

