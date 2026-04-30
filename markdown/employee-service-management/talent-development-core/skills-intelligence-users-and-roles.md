---
title: Components installed with Skills Foundation
description: Several types of components are installed with the activation of the Skills Foundation application, including user roles and tables.
locale: en-US
release: xanadu
product: Talent Development Core
classification: talent-development-core
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Skills Intelligence Reference, Skills Foundation, Talent Development, Employee Service Management]
---

# Components installed with Skills Foundation

Several types of components are installed with the activation of the Skills Foundation application, including user roles and tables.

## Skills Foundation roles

|Role name|Operations|Roles|
|---------|----------|-----|
|Skills Foundation manager|Can view and validate skills of an employee.|sn\_skills\_int.manager|
|Skills Foundation admin|Can configure system settings with complete access to all the features and functionality related to the employee.|sn\_skills\_int.admin|
|Skills Foundation employee|View and update the skills profile.|sn\_skills\_int.emp|
|Skills Foundation reader|Read the Skills Foundation records.|sn\_skills\_int.reader|
|Skills Foundation Job architecture editor|View and update the job architecture and required statuses.|sn\_skills\_int.job\_arch\_editor|
|Skills Foundation Job architecture admin|View, create, update, remove, and configure the job architecture.|sn\_skills\_int.job\_arch\_admin|

You can assign these roles to the appropriate roles, groups, or users in your application.

-   For information about how to assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   For information about how to assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   For information about how to assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Tables installed

|Table|Description|
|-----|-----------|
|cmn\_skills|Stores the data related to skills.|
|sn\_skills\_int\_job\_family\_m2m\_job\_profile|Stores the relationship between job profiles and job families.|
|sn\_skills\_int\_job\_family|Stores the job family that broadly classifies the jobs based on similar requirements.|
|sn\_skills\_int\_company\_job\_arch\_staging|Stores the Job architecture staging data.|
|sn\_skills\_int\_job\_profile|Stores the job profiles related to the jobs in your organization.|
|sn\_skills\_int\_job\_level|Stores the job levels in your organization.|
|sn\_skills\_int\_job\_level\_to\_level\_config|Stores the progression between job levels.|
|sn\_skills\_int\_related\_role\_group|Stores the data of role groups that are related to each other.|
|sn\_skills\_int\_role\_group|Stores the role groups that classify the roles in your organization.|
|sn\_skills\_int\_role\_group\_skill|Stores the skills data in the role groups.|
|sn\_skills\_int\_role\_level|Stores the role level data in your organization.|
|sn\_skills\_int\_role\_level\_m2m\_ind\_title|Stores the data related to the industry titles imported into your ServiceNow instance.|
|sn\_skills\_int\_employee\_role\_level\_m2m|Stores the relationship of how an employee maps to a role level and whether it’s a primary role.|
|sn\_skills\_int\_role\_level\_skill|Stores skills at the role level.|
|sn\_skills\_int\_proficiency\_autofill\_config|Stores the configuration for proficiency autofill. For more information, see [Set the job proficiency level automatically](../task/proficiency-autofill-config.md).|
|sn\_skills\_int\_extracted\_skill|Stores skills extracted from a resume upload.|
|sn\_skills\_int\_skill\_onboarding\_prediction|Stores the match/duplicate skill predictions from the custom skills imported.|
|sn\_skills\_int\_skill\_onboarding|Stores the custom skills imported.|
|sn\_skills\_int\_skill\_validation|Stores the validation information of the user skills.|
|sn\_skills\_int\_user\_managed\_skill|Stores user skills added to the skills profile.|
|sn\_skills\_int\_dynamic\_skill|Stores the new skills requested from the dynamic sources \( currently only from Credly\).|
|sn\_skills\_int\_dynamic\_skill\_requestor|Stores the requester information for the dynamic skills added.|

**Parent Topic:**[Skills Intelligence Reference](../concept/skills-intelligence-reference.md)

