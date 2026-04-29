---
title: Installed with domain separation
description: Several platform components are added or modified with domain separation.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Exploring domain separation, Domain separation for service providers, Access Management]
---

# Installed with domain separation

Several platform components are added or modified with domain separation.

## Roles

|Role|Description|
|----|-----------|
|domain\_admin|Can create, edit, and delete domains.|

## Additions to \[sys\_domain\] fields

The sys\_domain field is added to the following tables:

|Tables|
|------|
|sys\_attachment|
|sys\_user\_has\_role|
|sys\_group\_has\_role|
|sys\_email|
|sys\_user\_group|
|core\_company|
|cmn\_location|
|cmn\_department|
|sys\_gauge|
|sys\_report|
|kb\_feedback|
|sysapproval\_approver|
|sys\_user\_grmember|

## Field for the Task Table

MSP Extensions add a task\_for field to the Task table. This reference field refers to the User table.

## Options for the Group Type

MSP Extensions add several new default options to the type field of the Group table. Add to or update these types as needed to support your domains.

|Tables|
|------|
|Security|
|Support|
|Visibility|

## Business rules

|Name|Table|Description|
|----|-----|-----------|
|Domain - Activate/Deactivate|core\_company|Activates the related domain if at least one of its companies is active. Deactivates the related domain if all related companies are inactive.|
|Domain - Cascade Company|core\_company|Keeps a company's domain in sync with its users, groups, departments, and locations.|
|Domain - Cascade Domain - Email|sys\_email|Keeps an email's domain in sync with its attachments.|
|Domain - Cascade Domain - Group|sys\_user\_group|Keeps a group's domain in sync with its inherited roles \(sys\_group\_has\_role records\).|
|Domain - Cascade Domain - Knowledge|kb\_knowledge|keeps a knowledge article's domain in sync with its related feedback.|
|Domain - Cascade Domain - Task|task|Keeps the domain in sync with related tasks for wf\_context, wf\_executing, wf\_history, attachments, emails, task\_sla and its workflow, sysapproval\_approver and its workflow, and sysapproval\_group and its workflow.|
|Domain - Cascade Domain - User|sys\_user|Keeps a user's domain in sync with its group membership \(sys\_user\_grmember\) and role \(sys\_user\_has\_role\) records.|
|Domain - Cascade Domain - Version|wf\_workflow\_version|Keeps domains in sync with related workflow versions for wf\_activity and wf\_transition.|
|Domain - Deactivate Companies|domain|Deactivates related companies if a domain is deactivated.|
|Domain - Default - Task|task|Sets the task domain based on the Task for user's domain. If this domain would be global, sets domain to Default instead.|
|Domain - Default - User|sys\_user|Sets a user's domain to Default if the domain otherwise would have been global.|
|Domain - Disallow Global Domain Record|domain|Prevents creation of a domain with the name global.|
|Domain - Override Copy|sys\_app\_application|When an application is overridden for a domain, creates a copy of its modules for the new application.|
|Domain - Override Copy|sys\_data\_policy2|When a data policy is overridden for a domain, creates a copy of its data policy rules for the new data policy.|
|Domain - Override Copy|sys\_gauge|When a gauge is overridden for a domain, creates a copy of its gauge counts for the new gauge.|
|Domain - Override Copy|sys\_ui\_action|When a UI action is overridden for a domain, creates a copy of its UI action views for the new UI action.|
|Domain - Override Copy|sys\_ui\_list\_control\_embedded|When an embedded list control is overridden for a domain, creates a copy of its client and server scripts for the new embedded list control.|
|Domain - Override Copy|sys\_ui\_policy|When a UI policy is overridden for a domain, creates a copy of its UI policy actions for the new UI policy.|
|Domain - Set Domain - Approvals|sysapproval\_approver|Sets the domain based on that of the record being approved.|
|Domain - Set Domain - Attachment|sys\_attachment|Sets the domain based on the parent record's domain.|
|Domain - Set Domain - CMDB\_CI|cmdb\_ci|Sets a CI's domain to that of its company.|
|Domain - Set Domain - Department|cmn\_department|Sets a department's domain to that of its company.|
|Domain - Set Domain - Domain|domain|Sets a domain's domain to itself.|
|Domain - Set Domain - Email|sys\_email|Sets the domain based on the parent record's domain. An email's parent record is the record specified in the instance field.|
|Domain - Set Domain - Feedback|kb\_feedback|Sets a knowledge feedback's domain to that of its knowledge article.|
|Domain - Set Domain - Group|sys\_user\_group|Sets a group's domain to that of its company.|
|Domain - Set Domain - Group Approvals|sysapproval\_group|Sets the domain based on that of the record being approved.|
|Domain - Set Domain - Group Role|sys\_group\_has\_role|Sets a group role's domain to that of its group.|
|Domain - Set Domain - Location|cmn\_location|Sets a location's domain to that of its company.|
|Domain - Set Domain - Task SLA|task\_sla|Sets a task SLA's domain to that of its task.|
|Domain - Set Domain - User|sys\_user|Sets a user's domain to that of its company.|
|Domain - Set Domain - User Role|sys\_user\_has\_role|Sets a user role's domain to that of its user.|
|Domain - Set Domain - WF Activity Hist|wf\_history|Sets the workflow activity history domain based on the parent workflow context's domain.|
|Domain - Set Domain - WF Context|wf\_context|Sets the workflow context domain based on the referenced record's domain, if it has one.|
|Domain - Set Domain - WF Exec Activity|wf\_executing|Sets the workflow executing activity domain based on the parent workflow context's domain.|
|Domain - Set task for - Change|change-request|When converting a ticket to a change request, sets the Requested by field to the ticket's Task for value.|
|Domain - Set task for - Incident|incident|When converting a ticket to an incident, sets the Caller field to the ticket's Task for value.|
|Domain - Validate Default|domain|Ensures only one domain has the Default check box selected.|
|Domain - Validate Primary|domain|Ensures only one domain has the Primary check box selected.|
|Business Rules Installed with Domain Support Plugin|
|Change Domain Set|sys\_dictionary|Sets the domain set to the current domain.|
|Domain support properties|sys\_properties|Sets the system properties to match the domain query method \(domain paths or domain numbering\).|

## Client scripts

|Client script|Description|
|-------------|-----------|
|Domain - Set Company and Location \(sys\_script\)|Monitors the incident caller field for changes. If the company and location fields do not already have a value, the script adds this information from the caller record. If the company and location fields already have a value, the script retains the existing values.|
|Deactivated script|
|\(BP\) Set Location to User|Monitors the incident location field and sets the location field to the caller's location.|

**Parent Topic:**[Exploring domain separation](../concept/c_DomainSeparation.md)

**Related topics**  


[Configuration that can be delegated to internal or external customers](../concept/ds-before-you-begin.md)

[Domain assignment](../concept/c_DomainAssignment.md)

[Visibility domains and Contains domains](../concept/c_DomainVisibility.md)

[Domain scope](../concept/c_DomainScope.md)

[Concepts for service providers](../concept/sp-concepts.md)

[Domain separation recommended practices for service providers](bp-domain-sep-recommended.md)

