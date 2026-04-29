---
title: Components installed with Audit Management
description: Activating the GRC: Audit Management \(com.sn\_audit\) plugin adds or modifies several tables, user roles, and other components.Properties are added with activation of GRC: Audit Management.Roles are added with activation of GRC: Audit Management.Tables are added with activation of GRC: Audit Management.Tables are added with activation of GRC: Advanced Audit
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Audit Management reference, Audit Management, Governance, Risk, and Compliance]
---

# Components installed with Audit Management

Activating the GRC: Audit Management \(com.sn\_audit\) plugin adds or modifies several tables, user roles, and other components.

**Parent Topic:**[Audit Management reference](audit-management-reference.md)

## Properties installed with Audit Management and Advanced Audit

Properties are added with activation of GRC: Audit Management.

<table id="table_ght_bmm_vs"><thead><tr><th>

Name

</th><th>

Description

</th><th>

Application

</th></tr></thead><tbody><tr><td>

sn\_audit.retain\_report\_attachments

</td><td>

Retains the previous Word report attachments with the engagement record each time the report is generated

 -   Type: string
-   Default value: No

</td><td>

Audit Management

</td></tr><tr><td>

sn\_audit.knowledge\_base

</td><td>

Name of the knowledge base used to publish Audit reports

 -   Type: string
-   Default value: Audit

</td><td>

Audit Management

</td></tr><tr><td>

sn\_audit\_advanced.default\_adv\_notifica tion\_duedate\_duration

</td><td>

Default duration \(in days\) from the due date of a milestone, based on which, a notification is sent.-   Type: integer
-   Default value: 8

</td><td>

GRC: Advanced Audit

</td></tr><tr><td>

sn\_audit\_advanced.role\_documentation \_link

</td><td>

Documentation link for role requirements for enabling and using advanced planning feature \(with PPM integration\). Type: string

</td><td>

GRC: Advanced Audit

</td></tr><tr><td>

sn\_audit\_advanced.ppm\_project\_docu mentation\_link

</td><td>

Documentation link for project capabilities and role requirements. Type: string

</td><td>

GRC: Advanced Audit

</td></tr><tr><td>

sn\_audit\_advanced.rollup\_documentati on\_link

</td><td>

Documentation link for expenses and resources rollup details, from project to related engagement and plan.

 Type: string

</td><td>

GRC: Advanced Audit

</td></tr></tbody>
</table>## Roles installed with Audit Management

Roles are added with activation of GRC: Audit Management.

<table id="table_bc1_n3m_vs"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Audit Admin\[sn\_audit.admin\]

</td><td>

In addition to the inherited permissions, the audit admin can delete engagements, audit tasks, test templates, and test plans.

</td><td>

-   sn\_audit.manager
-   sn\_grc.admin

</td></tr><tr><td>

Audit approver \[sn\_audit.approver\]

</td><td>

The audit approver can approve an engagement and audit plan. The user with this role can be a part of approver list and the role is classified as Lite operator role.

</td><td>

sn\_audit.reader

</td></tr><tr><td>

Audit reader \[sn\_audit.reader\]

</td><td>

The user can view the audit-related entities such as engagements, plans, observations, audit tasks, and has exclusive read access to all the entities in the Audit Management application. This role is classified as a lite operator role.

</td><td>

sn\_grc.reader

</td></tr><tr><td>

Audit Developer\[sn\_audit.developer\]

</td><td>

In addition to the inherited permissions, the audit developer can add and delete audit report templates.

</td><td>

-   sn\_audit.admin
-   sn\_grc.developer

</td></tr><tr><td>

External Auditor\[sn\_audit.external\_auditor\]

</td><td>

External auditors can be assigned as auditors for an engagement and can be assigned to audit tasks. They can view closed engagements, audit tasks that are assigned to them, and closed audit tasks. If the Policy and Compliance Management plugin or Risk Management plugins are installed, they can also view published policies and all controls and risks in the **Monitor** state.

</td><td>

 

</td></tr><tr><td>

Audit Manager\[sn\_audit.manager\]

</td><td>

In addition to the inherited permissions, the audit manager can create audit tasks \(such as control tests, activities, walkthroughs, and interviews\), engagements, test plans, test templates, issues, remediation tasks, and entities. If Advanced Core is installed, then the audit manager can also create evidence requests.

</td><td>

-   sn\_audit.user
-   sn\_grc.manager

</td></tr><tr><td>

Audit User\[sn\_audit.user\]

</td><td>

In addition to the inherited permissions, the audit user can be assigned audit tasks and create test templates and test plans. The audit user has read-only access to the Risk Management application and modules and the Policy and Compliance Management application and modules.

</td><td>

-   sn\_compliance.reader
-   sn\_grc.reader
-   sn\_grc.user

</td></tr><tr><td>

Engagement Project Manager\[sn\_audit\_advanced.engagement\_project\_manager\]

</td><td>

The audit lead who does advanced planning and could handle plans or engagements.This role is available after GRC: Advanced Audit plugin is activated.

</td><td>

-   sn\_audit.manager
-   resource\_manager
-   it\_project\_manager

</td></tr></tbody>
</table>## Tables installed with Audit Management

Tables are added with activation of GRC: Audit Management.

<table id="table_qlq_g3m_vs"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity\[sn\_audit\_activity\]

</td><td>

Extends Audit Task \[sn\_audit\_task\] and stores audit activities

</td></tr><tr><td>

Audit Task\[sn\_audit\_task\]

</td><td>

Extends Planned Task \[planned\_task\] and is a generic table for all tasks associated with an audit

</td></tr><tr><td>

Base Audit Test\[sn\_audit\_base\_test\]

</td><td>

Base table for Test Templates and Test Plans

</td></tr><tr><td>

Control Test\[sn\_audit\_control\_test\]

</td><td>

Extends Audit Task \[sn\_audit\_task\] and stores control tests

</td></tr><tr><td>

Control to Engagement\[sn\_audit\_m2m\_control\_engagement\]

</td><td>

Stores many-to-many relationships between controls and engagements

</td></tr><tr><td>

Engagement\[sn\_audit\_engagement\]

</td><td>

Extends Planned Task \[planned\_task\] and stores engagements

</td></tr><tr><td>

Interview\[sn\_audit\_interview\]

</td><td>

Extends Audit Task \[sn\_audit\_task\] and stores interviews

</td></tr><tr><td>

Entity to Engagement\[sn\_audit\_m2m\_profile\_engagement\]

</td><td>

Stores many-to-many relationships between entities and engagements

</td></tr><tr><td>

Risk to Engagement\[sn\_audit\_m2m\_risk\_engagement\]

</td><td>

Stores many-to-many relationships between risks and engagements

</td></tr><tr><td>

Test Plan\[sn\_audit\_test\_plan\]

</td><td>

Extends Base Audit Test \[sn\_audit\_base\_test\] and stores test plans

</td></tr><tr><td>

Test plan to Engagement\[sn\_audit\_m2m\_test\_plan\_engagement\]

</td><td>

Stores many-to-many relationships between test plans and engagements

</td></tr><tr><td>

Test Template\[sn\_audit\_test\_template\]

</td><td>

Extends Base Audit Test \[sn\_audit\_base\_test\] and stores test templates

</td></tr><tr><td>

Walkthrough\[sn\_audit\_walkthrough\]

</td><td>

Extends Audit Task \[sn\_audit\_task\] and stores walkthroughs

</td></tr><tr><td>

Audit Report Template\[sn\_audit\_report\_template\]

</td><td>

Stores the defined xml, html, or script-based audit report templates

</td></tr><tr><td>

Assessment procedures

 \[sn\_audit\_asmnt\_procedure\_control\_test\]

</td><td>

Stores the assessment objectives of control tests. Identifier and assessment objectives field values are copied over from the Assessment procedure plan table.

</td></tr><tr><td>

Assessment procedure plan

 \[sn\_audit\_asmnt\_procedure\_test\_plan\]

</td><td>

Generated for the test plan. Changes made to the test plan are reflected in the control test table \[sn\_audit\_asmnt\_procedure\_control\_test\]

</td></tr><tr><td>

Assessment procedure templates

 \[sn\_audit\_asmnt\_procedure\]

</td><td>

Stores the assessment objectives

</td></tr><tr><td>

Test template to Assessment procedure

 \[sn\_audit\_m2m\_test\_temp\_asmnt\_procedure\]

</td><td>

Stores many-to-many relationships between test template and assessment procedure

</td></tr></tbody>
</table>**Note:** All additional tables installed by the dependent plugins are also needed for GRC: Audit Management.

## Tables installed with Advanced Audit

Tables are added with activation of GRC: Advanced Audit

<table id="table_qlq_g3m_vs"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audit Task to Milestonesn\_audit\_advanced\_m2m\_audit\_task\_milestone

</td><td>

Stores many-to-many relationships between audit tasks and milestones.

</td></tr><tr><td>

Auditable Unitsn\_audit\_advanced\_auditable\_unit

</td><td>

Stores auditable units.

</td></tr><tr><td>

Auditable Unit To Authority Documentsn\_audit\_advanced\_m2m\_unit\_authority\_document

</td><td>

Stores many-to-many relationships between auditable units and authority documents.

</td></tr><tr><td>

Auditable Unit To Business Applicationsn\_audit\_advanced\_m2m\_unit\_business\_application

</td><td>

Stores many-to-many relationships between auditable units and business applications.

</td></tr><tr><td>

Auditable Unit To Business Processsn\_audit\_advanced\_m2m\_unit\_business\_process

</td><td>

Stores many-to-many relationships between auditable units and business processes.

</td></tr><tr><td>

Auditable Unit To Business Unitsn\_audit\_advanced\_m2m\_unit\_business\_unit

</td><td>

Stores many-to-many relationships between auditable units and business units.

</td></tr><tr><td>

Auditable Unit To Departmentsn\_audit\_advanced\_m2m\_unit\_cmn\_department

</td><td>

Stores many-to-many relationships between auditable units and departments.

</td></tr><tr><td>

Auditable Unit To Locationsn\_audit\_advanced\_m2m\_unit\_location

</td><td>

Stores many-to-many relationships between auditable units and locations.

</td></tr><tr><td>

Auditable Unit To Policysn\_audit\_advanced\_m2m\_unit\_policy

</td><td>

Stores many-to-many relationships between auditable units and policies.

</td></tr><tr><td>

Auditable Unit To Productsn\_audit\_advanced\_m2m\_unit\_product\_model

</td><td>

Stores many-to-many relationships between auditable units and products.

</td></tr><tr><td>

Auditable Unit To Vendorsn\_audit\_advanced\_m2m\_unit\_vendor

</td><td>

Stores many-to-many relationships between auditable units and vendors.

</td></tr><tr><td>

Engagement Projectsn\_audit\_advanced\_engagement\_project

</td><td>

Extends Project table and stores engagement projects for engagements.

</td></tr><tr><td>

Milestonesn\_audit\_advanced\_milestone

</td><td>

Extends Planned Task table and stores milestones.

</td></tr><tr><td>

Observationsn\_audit\_advanced\_observation

</td><td>

Extends Triage table and stores observations.

</td></tr><tr><td>

Plansn\_audit\_advanced\_plan

</td><td>

Extends Planned Task table and stores plans.

</td></tr></tbody>
</table>**Note:** All additional tables installed by the dependent plugins are also needed for GRC: Audit Management.

