---
title: About Job Architecture
description: Company job architecture data enables you to optimize career growth and development of employees by identifying required, recommended, and additional skills for employee roles.
locale: en-US
release: xanadu
product: Talent Development Core
classification: talent-development-core
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Skills Foundation, Skills Foundation, Talent Development, Employee Service Management]
---

# About Job Architecture

Company job architecture data enables you to optimize career growth and development of employees by identifying required, recommended, and additional skills for employee roles.

Assess the skills of the employee and suggest learning to acquire new skills, promoting talent management via Manager Hub or through Skills profile in Employee Portal. For more information, see [Career tab in Employee Center](manage-skills-profile.md).

Prepare company job architecture data from any HCM \(human capital management\) platform in CSV format and import it to your ServiceNow® instance. After transformation, the data is transferred to the relevant tables like Job Family, Role Group, and Job Profiles. For more information on the transformation process, see [Load job architecture data into your ServiceNow instance](../task/load-data-skills-tables.md).

**Note:** You must import your company job architecture data before being able to onboard employee job profiles in your ServiceNow instance.

From the Company Job Architecture Staging \[sn\_skills\_int\_company\_job\_arch\_staging\] table, the data is populated into the following tables:

-   Job Family \[sn\_skills\_int\_job\_family\] table: Groups similar jobs. For example, Software Engineering, Application Development, Finance and Purchasing, Human Resources, and so on.
-   Job Profiles \[sn\_skills\_int\_job\_profile\] table: Provides an information record about a job that includes a summary and description. For example, Sr. Software Engineer, Project Manager, and so on.
-   Job Levels \[sn\_skills\_int\_job\_level\] table: The level of the job profile. For example, IC1, and IC2.
-   Role Groups \[sn\_skills\_int\_role\_group\] table: Includes roles with a similar set of skills. For example, Front-end, Back-end, Full-stack, and so on.
-   Role Levels \[sn\_skills\_int\_role\_level\] table: The designation of the role in a role group, with the name indicating its level \(IC1, IC2\). For example, Associate Software Engineer - Backend – IC1 – JavaScript L1.
-   Role Group Skills \[sn\_skills\_int\_role\_group\_skill\] table: The mapping of role groups and their skills.
-   Role Level Skills \[sn\_skills\_int\_role\_level\_skill\] table: The mapping of role level and skills with the level of proficiencies for the role level.

For more information about the tables in the Skills Foundation application, see [Components installed with Skills Foundation](../reference/skills-intelligence-users-and-roles.md).

**Note:**

You can also add data specific to your organization to these tables manually.

After the data is imported, connect the job architecture data to the employee profile. For more information, see [Map a role level to the employee profile](../task/skills-int-attach-role-level-emp.md).

