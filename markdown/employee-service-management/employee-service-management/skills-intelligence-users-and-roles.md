---
title: Components installed with Skills Foundation
description: Several types of components are installed with the activation of the Skills Foundation application, including user roles and tables.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
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
|Skills Foundation Business partner|Can access skills or career data for managed employees.|sn\_skills\_int.hrbp|
|Skills FoundationWorkspace user|Can access skills workspace|sn\_skills\_int\_ws.workspace\_user|

You can assign these roles to the appropriate roles, groups, or users in your application.

-   For information about how to assign a role to another role, see [Add a role to an existing role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddARoleToAnExistingRole.md).
-   For information about how to assign a role to a group, see [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignRoleToGroup.md).
-   For information about how to assign a role to a user, see [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignARoleToAUser.md).

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
|sn\_skills\_int\_ats\_job\_role\_group\_to\_skill|Stores associated ATS job role groups with skills. Typically used to determine which skills are required, preferred, or relevant for a role imported from a recruiting system.|
|sn\_skills\_int\_ats\_job\_extracted\_skill|Stores skills extracted from ATS job descriptions or requisitions.|
|sn\_skills\_int\_ats\_job\_predicted\_title\_role\_level|Stores AI/ML predictions of job title, role family, and seniority.|
|sn\_skills\_int\_ats\_job\_role\_group\_to\_skill|Stores the role groups that are mapped to the expected or recommended skills.|
|sn\_skills\_int\_job\_posting\_skill\_search|Stores matching job postings and skills.|
|sn\_skills\_int\_last\_job\_req\_skills\_extraction\_run\_at|Stores when the skills extraction last ran for the job requisitions.|
|sn\_skills\_int\_related\_role\_group|Stores the data of role groups that are related to each other.|
|sn\_skills\_int\_role\_group|Stores the role groups that classify the roles in your organization.|
|sn\_skills\_int\_role\_group\_skill|Stores the skills data in the role groups.|
|sn\_skills\_int\_role\_level|Stores the role level data in your organization.|
|sn\_skills\_int\_role\_level\_m2m\_ind\_title|Stores the data related to the industry titles imported into your ServiceNow instance.|
|sn\_skills\_int\_employee\_role\_level\_m2m|Stores the relationship of how an employee maps to a role level and whether it’s a primary role.|
|sn\_skills\_int\_role\_level\_skill|Stores skills at the role level.|
|sn\_skills\_int\_proficiency\_autofill\_config|Stores the configuration for proficiency autofill. For more information, see [Set the job proficiency level automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/talent-development-core/proficiency-autofill-config.md).|
|sn\_skills\_int\_extracted\_skill|Stores skills extracted from a resume upload.|
|sn\_skills\_int\_skill\_onboarding\_prediction|Stores the match/duplicate skill predictions from the custom skills imported.|
|sn\_skills\_int\_skill\_onboarding|Stores the custom skills imported.|
|sn\_skills\_int\_skill\_validation|Stores the validation information of the user skills.|
|sn\_skills\_int\_skill\_import\_row|Stores details of bulk skills import.|
|sn\_skills\_int\_user\_managed\_skill|Stores user skills added to the skills profile.|
|sn\_skills\_int\_dynamic\_skill|Stores the new skills requested from the dynamic sources \( currently only from Credly\).|
|sn\_skills\_int\_dynamic\_skill\_requestor|Stores the requester information for the dynamic skills added.|
|sn\_skills\_int\_skill\_import\_tracker|Stores overall skill import jobs details and status.|
|sn\_skills\_int\_user\_skill\_import\_row|Stores user or empoyee skill imports|
|sn\_skills\_int\_role\_level\_skill|Stores which skills belong to the role and level of the role.|

