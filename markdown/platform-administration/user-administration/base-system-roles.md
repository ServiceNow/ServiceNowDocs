---
title: System roles
description: Administrators can control access to features and capabilities on a ServiceNow instance by assigning roles to users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/user-administration/base-system-roles.html
release: zurich
product: User Administration
classification: user-administration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Managing roles, User admin, Configure core features, Administer]
---

# System roles

Administrators can control access to features and capabilities on a ServiceNow instance by assigning roles to users.

Your ServiceNow includes roles to grant access to the platform features and applications included a base system instance. Applications you install on your instance may include additional roles to control access to those installed features. For more information about roles, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/user-administration/exploring-user-administration.md).

**Important:** Base system and roles installed with applications can be deactivated by administrators, but can’t modify or rename these roles.

## Base system roles

Base system roles are present in all ServiceNow instances and don’t require the installation of additional plugins.

<table id="table_yly_lly_wq"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

admin

</td><td>

The system administrator role. This role has access to all system features, functions, and data because administrators can override access control list \(ACL\) rules and pass all role checks. Avoid assigning this role to your users when more targeted roles are available.

 **Warning:** Grant this privilege carefully. If you have sensitive information, such as HR records, that you need to protect, you must create a custom admin role for that area. You must also train any users authorized to see those records to act as the administrator. Also note the [Special Administrative Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/user-administration/r_SpecialAdministrativeRoles.md).

</td></tr><tr><td>

agent\_admin

</td><td>

Agent administrators can download and administer the system's built-in agent. They can manage MID Server-related scripts.

</td></tr><tr><td>

ais\_admin

</td><td>

AI search administrators can query, create, update, and delete indexing and search settings and log messages through the [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/overview-ais.md) application.

</td></tr><tr><td>

approval\_admin

</td><td>

Approval administrators can view or modify approval requests not directly assigned to them. Use the approver\_user role to enable approvers to only view or modify requests directly assigned to them. Use of this role requires a Fulfiller license. Use of the approver\_user role requires an Approver license.

</td></tr><tr><td>

approver\_user

</td><td>

Approver users can modify requests for approval routed to them. They also have all capabilities of requesters.**Note:** There’s a fee associated with this role. Don’t assign it to users without confirming your organization has the appropriate entitlement.

</td></tr><tr><td>

assignment\_rule\_admin

</td><td>

Assignment rule administrators can manage assignment rules.

</td></tr><tr><td>

asset

</td><td>

Asset users can manage hardware and software assets.

</td></tr><tr><td>

business\_process\_admin

</td><td>

Business process admins can create, read, update, and delete all records and their relationships in the business process.

 In the context of Governance, Risk, and Compliance \(GRC\), users with the sn\_grc.admin role who manage GRC applications and their setup automatically gain access to this role. This access enables the GRC administrators to administer a business process and its records similar to other GRC tables.

 **Important:** This role is assigned to users who are administrators and have thorough information and training on business processes.

</td></tr><tr><td>

business\_process\_manager

</td><td>

Business process managers can create, read, and update any business process and manage the relationship of business processes with other records. This role is assigned to business process managers who are usually specialists and manage multiple business processes in the organization. These users generally work with other employees and are experts around business processes.

 In the context of GRC, users with the sn\_grc.manager role automatically inherit this role that enables them to manage the business processes for the entire organization.

</td></tr><tr><td>

business\_process\_user

</td><td>

Business process users can update the business processes that a user owns and can also read any business process. This role must be assigned to the respective process owners who manage the business process that they own. This role can also be provided to users who are required to view the business processes in the organization and understand them better.

 In the context of GRC, users with the sn\_risk.user role are automatically assigned this role as this role enables them to manage the business processes they own as well as read all business processes.

</td></tr><tr><td>

catalog

</td><td>

Catalog users can access service catalog requests.

</td></tr><tr><td>

catalog\_admin

</td><td>

Catalog administrators can manage the Service Catalog application, including catalog categories and items.

</td></tr><tr><td>

catalog\_editor

</td><td>

Catalog editors can create, modify, and publish items within categories that they’re assigned to.

</td></tr><tr><td>

catalog\_item\_designer

</td><td>

Catalog item designers can view the status of their category requests. This role is granted automatically to users when they make a request for an item designer category.

</td></tr><tr><td>

catalog\_manager

</td><td>

Catalog managers can view and assign catalog editors to their categories. Can also create, modify, and publish items within their categories.

</td></tr><tr><td>

category\_manager

</td><td>

Category managers can create, edit, and delete model categories.

</td></tr><tr><td>

cmdb\_dedup\_admin

</td><td>

CMDB de-duplication admins can review and remediate CMDB de-duplication tasks.

</td></tr><tr><td>

cmdb\_ms\_user

</td><td>

CMDB multiscource readers can access and run a multi-source CMDB query, but can't create a query. This role contains Contains cmdb\_read role.

</td></tr><tr><td>

cmdb\_ms\_editor

</td><td>

Can create and run a query, has full read and write access, but can't do Recompute. Contains cmdb\_ms\_read role.

</td></tr><tr><td>

cmdb\_ms\_admin

</td><td>

Can create and run a query, and can modify CMDB 360 properties. Contains cmdb\_ms\_write role.

</td></tr><tr><td>

cmdb\_read

</td><td>

Can read any CMDB table. Contained in admin and itil.

</td></tr><tr><td>

communication\_manager

</td><td>

Manages communication for major incidents and is responsible for communicating with all stakeholders.

</td></tr><tr><td>

contract\_manager

</td><td>

Can create, edit, and delete contracts through the Contract Management application.

</td></tr><tr><td>

data\_classification\_admin

</td><td>

Administers all aspects of the Data Classification application, data classification code setup and assignment,

</td></tr><tr><td>

data\_classification\_auditor

</td><td>

Audits Data Classification code assignments.

</td></tr><tr><td>

ecmdb\_admin

</td><td>

Can administer the CMDB.

</td></tr><tr><td>

filter\_admin

</td><td>

Can manage filters.

</td></tr><tr><td>

filter\_global

</td><td>

Can create global filters.

</td></tr><tr><td>

filter\_group

</td><td>

Can create filters that belong to groups of which the user is a member.

</td></tr><tr><td>

gauge\_maker

</td><td>

Can create gauges from reports. Starting with Helsinki, reports are no longer made into gauges.

</td></tr><tr><td>

guided\_tour\_admin

</td><td>

Can manage and administer Guided Tour functionality.

</td></tr><tr><td>

image\_admin

</td><td>

Can manage image files on the Images \[db\_image\] table.

</td></tr><tr><td>

impersonator

</td><td>

Can impersonate users. This role doesn't allow impersonation of admin users.

</td></tr><tr><td>

import\_admin

</td><td>

Can manage all aspects of import sets and imports.

</td></tr><tr><td>

import\_scheduler

</td><td>

Can schedule imports. **Warning:** Grant this role carefully. The import\_scheduler role is equivalent to giving the user the admin role, because the import\_scheduler has the ability to execute scripts with administrator level privileges.

</td></tr><tr><td>

import\_set\_loader

</td><td>

Can load import sets.

</td></tr><tr><td>

import\_transformer

</td><td>

Can manage import set transform maps and run transforms.

</td></tr><tr><td>

incident\_manager

</td><td>

Manages Incident properties and Major Incident trigger rules.

</td></tr><tr><td>

inventory\_admin

</td><td>

Can create and delete stock information. Only users with the inventory\_admin role can edit stock rules, stockrooms, and stockroom types.

</td></tr><tr><td>

inventory\_user

</td><td>

Has access to stock information. Can create and manage transfer orders.

</td></tr><tr><td>

itil

</td><td>

Can perform standard actions for an ITIL helpdesk technician. Can open, update, close incidents, problems, changes, configuration management items. By default, only users with the itil role can have tasks assigned to them.

</td></tr><tr><td>

itil\_admin

</td><td>

Possesses more privileges than the itil role and is intended for team leads. This role has the ability to delete incidents, problems, changes, and other related entities when both the itil and itil\_admin roles are assigned. In addition, the itil\_admin role grants full control of the CMDB. The itil\_admin role includes all of the permissions granted to the sn\_cmdb\_admin role, which provides full access to CMDB data, tools, and UIs.

</td></tr><tr><td>

knowledge

</td><td>

Can create, edit, and review knowledge base articles.

</td></tr><tr><td>

knowledge\_admin

</td><td>

Can manage the knowledge base.

</td></tr><tr><td>

list\_updater

</td><td>

Can use Update Entire List and Update Selected menu options on lists.

</td></tr><tr><td>

maint

</td><td>

Reserved for ServiceNow use.

</td></tr><tr><td>

mid\_server

</td><td>

Role that any MID server user should be granted. This role gives the MID server access to the tables it ordinarily uses.

</td></tr><tr><td>

model\_manager

</td><td>

Can create CMDB models. Model manager can control the base models and any model extensions that aren’t software or consumables. Consumable models are controlled by the asset manager role \(asset\). Software models are control by the software asset manager role \(SAM\).

</td></tr><tr><td>

major\_incident\_manager

</td><td>

Initiates the major incident process by assessing and approving major incident candidates or creating a major incident. Maintains the ownership and accountability for the life cycle of the incident. Identifies the users and groups to be involved in the resolution activities and sets up communication channels.

</td></tr><tr><td>

nobody

</td><td>

The nobody role means that no user has access - not even admin or maint. Use the nobody role carefully. The nobody role takes precedence over the admin override option on ACLs, so even admins can’t have access. See Create an ACL rule.

 Don’t assign it to specific users. You can use this role in ACLs that control access to resources, such as UI pages, processors, script includes, and records.

 **Warning:** Applying the nobody role may be irreversible if applied to some important system functions.

</td></tr><tr><td>

personalize

</td><td>

Can configure forms, lists, rules, controls, scripts.

</td></tr><tr><td>

personalize\_choices

</td><td>

Can configure [choices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_ViewChoiceListDefinitions.md) and predefined responses for non-journal fields designated as choice or suggestion fields.

</td></tr><tr><td>

personalize\_control

</td><td>

Can [configure controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/list-administration/t_ConfigureListControls.md) on lists, such as filters, links, and buttons.

</td></tr><tr><td>

personalize\_dictionary

</td><td>

Can configure dictionary entries and [labels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_ChangeFieldLabelOrHint.md).

</td></tr><tr><td>

personalize\_form

</td><td>

Can [configure forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configure-form-layout.md).

</td></tr><tr><td>

personalize\_list

</td><td>

Can [configure lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/list-administration/t_ConfigureTheListLayout.md) and list [calculations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/list-administration/t_ConfigureListCalculations.md).

</td></tr><tr><td>

personalize\_responses

</td><td>

Can configure predefined responses for [journal fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/c_JournalFields.md) designated as suggestion fields.

</td></tr><tr><td>

personalize\_rules

</td><td>

Can configure business rules and scripts. This role contains the following specialized roles for granting selective, administrative access to rules and scripts:-   business\_rule\_admin
-   client\_script\_admin
-   ui\_policy\_admin
-   ui\_action\_admin

</td></tr><tr><td>

personalize\_styles

</td><td>

Can configure [field styles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_DefineFieldStyles.md).

</td></tr><tr><td>

personalize\_ui

</td><td>

Can configure forms and lists.

</td></tr><tr><td>

public

</td><td>

No login is required to access features or functions with the public role.

</td></tr><tr><td>

release\_admin

</td><td>

Can edit Release history for a release.

</td></tr><tr><td>

report\_admin

</td><td>

Can manage reports.

</td></tr><tr><td>

report\_global

</td><td>

Can create global reports.

</td></tr><tr><td>

report\_group

</td><td>

Can create reports and share reports with groups that the user is a member of. Users with this role can edit reports shared by other users in the group.

</td></tr><tr><td>

report\_publisher

</td><td>

Can make reports available on a public page.

</td></tr><tr><td>

report\_scheduler

</td><td>

Can schedule a report to be emailed.

</td></tr><tr><td>

script\_fix\_admin

</td><td>

Can create and manage fix scripts but can’t run fix scripts.

</td></tr><tr><td>

search\_application\_admin

</td><td>

Can query, create, update, and delete records on search UX-related tables. Contains the ais\_admin role.

</td></tr><tr><td>

sn\_appclient.app\_client\_company\_installer

</td><td>

Can install applications containing the same company as the currently logged in instance. User role that enables first-time installation of applications for the company associated with the current instance. A user with this role can’t install an application for another company.

</td></tr><tr><td>

sn\_appclient.app\_client\_user

</td><td>

Can install applications containing the same company as the currently logged in instance.

</td></tr><tr><td>

sn\_cmdb\_admin

</td><td>

Provides full access to CMDB data, tools, and UIs. A CMDB Admin, for example, sets policies in the CI Class Manager and application service requirements. CMDB Admin provides the highest level of access to the CMDB.

</td></tr><tr><td>

sn\_cmdb\_editor

</td><td>

Provides access to CMDB records. A CMDB Editor can't change policies such as in the CMDB Data Manager or in the CI Class Manager.

</td></tr><tr><td>

sn\_cmdb\_user

</td><td>

Provides read-only access to CMDB data and to basic UIs such as CMDB reports and dashboards.

</td></tr><tr><td>

soap

</td><td>

Can query, create, update, and delete records on all tables, as well as execute scripts.

</td></tr><tr><td>

soap\_create

</td><td>

Can create records on all tables and columns.

</td></tr><tr><td>

soap\_delete

</td><td>

Can delete records on all tables and columns.

</td></tr><tr><td>

soap\_ecc

</td><td>

Can query, create, and update on the ECC Queue table only.

</td></tr><tr><td>

soap\_query

</td><td>

Can query records on all tables and columns.

</td></tr><tr><td>

soap\_query\_update

</td><td>

Can query and update records on all tables and columns.

</td></tr><tr><td>

soap\_script

</td><td>

Can execute business rule endpoint function via script.do.

</td></tr><tr><td>

soap\_update

</td><td>

Can update records on all tables and columns.

</td></tr><tr><td>

survey\_admin

</td><td>

Can see all Surveys, their definitions, questions, instances created by them and others. Survey administrators can use all modules in the Survey application menu.

</td></tr><tr><td>

survey\_reader

</td><td>

Users with survey reader role can view surveys and related information, such as survey responses, survey groups, scorecards, and reports. Survey\_reader can’t change or modify a survey or survey responses.

</td></tr><tr><td>

task\_editor

</td><td>

Can edit protected task fields.

</td></tr><tr><td>

template\_editor

</td><td>

Can create templates for personal use, and modify or delete personal templates. Included in the itil role in the base system.

</td></tr><tr><td>

template\_editor\_global

</td><td>

Can create templates for global use.

</td></tr><tr><td>

template\_editor\_group

</td><td>

Can create templates for groups.

</td></tr><tr><td>

template\_scheduler

</td><td>

Can schedule template-based record creation.

</td></tr><tr><td>

text\_search\_admin

</td><td>

Can customize Global Text Search groups and tables.

</td></tr><tr><td>

timecard\_admin

</td><td>

Can approve, modify, and delete the time cards of other users.

</td></tr><tr><td>

ts\_admin

</td><td>

Can administer [Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/search-administration/c_ZingTextSearch.md).

</td></tr><tr><td>

unlimited\_createnow

</td><td>

Role for CreateNow unlimited licensed users.

</td></tr><tr><td>

upgrade\_app

</td><td>

Can upgrade installed applications containing the same company as the currently logged in instance. Can’t perform first-time installations of applications published to the Application Client page.

</td></tr><tr><td>

user

</td><td>

Available for customer use, has no function in the base system.

</td></tr><tr><td>

user\_admin

</td><td>

Can administer users, groups, locations, and companies.

</td></tr><tr><td>

view\_changer

</td><td>

Can switch active views.

</td></tr><tr><td>

workflow\_admin

</td><td>

Can create, edit, publish, or delete graphical workflows.

</td></tr><tr><td>

workflow\_creator

</td><td>

Can create new graphical workflows.

</td></tr><tr><td>

workflow\_publisher

</td><td>

Can publish graphical workflows.

</td></tr></tbody>
</table>## Application-specific roles

Applications you install on your instance may include additional roles. Follow the links in this section to see roles documentation on roles installed along with applications.

|Product|Application|
|-------|-----------|
|Platform Capabilities|Advanced Work Assignment|

**Parent Topic:**[Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/user-administration/ua-creating-roles.md)

