---
title: Components installed with Health and Safety Risk Management
description: Several types of components are installed with installation of the Health and Safety Risk Management application, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren’t already installed.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 8
breadcrumb: [Reference, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Components installed with Health and Safety Risk Management

Several types of components are installed with installation of the Health and Safety Risk Management application, including tables, user roles, and scheduled jobs. The application also installs related store applications if they aren’t already installed.

## Store applications installed

<table id="table_ulz_4tw_llba"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Core

</td><td>

Installs core data model for Health and Safety. This data model includes common components such as Health and Safety user profile and actions that are used in the Health and Safety applications.

 For more information on store applications, roles, and tables installed with Health and Safety Core, see [Components installed with Health and Safety Core](../../hs-core/reference/components-installed-hs-core.md).

</td></tr><tr><td>

Workplace Core \[sn\_wsd\_core\]

</td><td>

Enables workplace locations for Health and Safety applications.**Important:** The application installation doesn’t install the location demo data for the Workplace Core location model. As a workaround, repair the Workplace Core plugin with the **Load demo data** option.

</td></tr><tr><td>

Risk Heatmap\[sn\_risk\_heatmap\]

</td><td>

Provides a heatmap component that enables you to visualize the risk posture of a safety risk assessment.

</td></tr><tr><td>

Smart Assessment Engine

</td><td>

Enables creating smart assessments for safety inspection or audits. For more information, see [Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/smart-asmnt-engine-landing-page.md).

</td></tr></tbody>
</table>## Roles installed

<table id="table_fy3_q3q_11c"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Hierarchy of controls manager

 \[sn\_hs\_rm.hierarchy\_of\_controls\_manager\]

</td><td>

Create, update, and delete control measure categories

</td><td>

sn\_hs\_rm.hierarchy\_of\_controls\_writer

</td></tr><tr><td>

Hierarchy of controls writer

 \[sn\_hs\_rm.hierarchy\_of\_controls\_writer\]

</td><td>

Create and update control measure categories

</td><td>

sn\_hs\_rm.hierarchy\_of\_controls\_reader

</td></tr><tr><td>

Job safety analysis writer

 \[sn\_hs\_rm.job\_safety\_analysis\_writer\]

</td><td>

-   Create and update job safety analyses \(JSAs\)
-   View filed JSA records

</td><td>

-   sn\_hs\_rm.risk\_category\_reader
-   sn\_hs\_rm.job\_safety\_analysis\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.hierarchy\_of\_controls\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_hs\_rm.control\_measure\_reader

</td></tr><tr><td>

Risk manager

 \[sn\_hs\_rm.risk\_manager\]

</td><td>

Manager for risk team who can

-   View job safety analysis \(JSA\) records in Health and Safety Workspace
-   Create and update job safety analyses \(JSAs\) from Health and Safety Workspace
-   Create, update, and delete:
    -   Hazards
    -   Control measures
    -   Jobs in Job register
    -   Risk matrixes including risk severity, likelihood, and tolerance

</td><td>

-   sn\_hs\_rm.job\_safety\_analysis\_reader
-   sn\_ohs\_im.workspace\_user
-   canvas\_user
-   sn\_hs\_rm.risk\_data\_manager

</td></tr><tr><td>

Job safety analysis reporter

 \[sn\_hs\_rm.jsa\_reporter\]

</td><td>

-   View filed JSA records
-   Submit JSAs from Employee Center and Now Mobile app
-   Use pre-defined jobs from job register when submitting JSAs

</td><td>

-   sn\_hs\_rm.job\_reader
-   sn\_hs\_rm.job\_safety\_analysis\_writer
-   sn\_hs\_rm.template\_reader

</td></tr><tr><td>

Risk assessment approver

 \[sn\_hs\_rm.risk\_assessment\_approver\]

</td><td>

-   Work on approval tasks through Employee Center
-   Review and approve risk assessments

</td><td>

sn\_hs\_rm.risk\_assessment\_reader

</td></tr><tr><td>

Risk assessment manager

 \[sn\_hs\_rm.risk\_assessment\_manager\]

</td><td>

Risk assessment manager who can:

-   Create risk matrixes
-   Conduct risk assessments
-   Assign risk assessments to approver

</td><td>

-   sn\_hs\_rm.risk\_assessment\_writer
-   sn\_hs\_rm.risk\_assessment\_approver

</td></tr><tr><td>

Risk assessment writer

 \[sn\_hs\_rm.risk\_assessment\_writer\]

</td><td>

Create and update risk assessments

</td><td>

-   sn\_hs\_rm.job\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_ohs\_im.action\_writer

</td></tr><tr><td>

Risk category manager

 \[sn\_hs\_rm.risk\_category\_manager\]

</td><td>

Create, update, and delete risk categories

</td><td>

sn\_hs\_rm.risk\_category\_writer

</td></tr><tr><td>

Risk category writer

 \[sn\_hs\_rm.risk\_category\_writer\]

</td><td>

Create and update risk categories

</td><td>

sn\_hs\_rm.risk\_category\_reader

</td></tr><tr><td>

Risk data manager

 \[sn\_hs\_rm.risk\_data\_manager\]

</td><td>

Create, update, and delete

-   Hazards
-   Control measures
-   Jobs in Job register
-   Risk matrixes including risk severity, likelihood, and tolerance

</td><td>

sn\_hs\_rm.risk\_data\_writer

</td></tr><tr><td>

Risk data writer

 \[sn\_hs\_rm.risk\_data\_writer\]

</td><td>

Create and update:

-   Hazards
-   Control measures
-   Jobs in Job register
-   Risk matrixes including risk severity, likelihood, and tolerance

</td><td>

-   sn\_hs\_rm.risk\_category\_reader
-   sn\_hs\_rm.job\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.risk\_matrix\_reader
-   sn\_hs\_rm.template\_reader
-   sn\_hs\_rm.hierarchy\_of\_controls\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_hs\_rm.control\_measure\_reader

</td></tr><tr><td>

Inspection schedule writer

 \[sn\_hs\_rm.inspection\_schedule\_writer\]

</td><td>

Create and update inspection schedules

</td><td>

sn\_hs\_rm.inspection\_schedule\_reader

</td></tr><tr><td>

Safety inspection manager

 \[sn\_hs\_rm.safety\_inspection\_manager\]

</td><td>

Inspection manager who can

-   Build inspection surveys with the Survey designer
-   Create and manage safety inspections in Health and Safety Workspace
-   Schedule safety inspections Health and Safety Workspace
-   Complete inspection surveys
-   Create, update, and delete inspection findings, RCA, and actions

</td><td>

-   sn\_hs\_rm.inspection\_schedule\_writer
-   sn\_ohs\_im.action\_manager
-   sn\_hs\_rm.safety\_inspection\_writer
-   survey\_creator

</td></tr><tr><td>

Safety inspection writer

 \[sn\_hs\_rm.safety\_inspection\_writer\]

</td><td>

Create and update safety inspections and related records

</td><td>

-   sn\_ohs\_im.workspace\_user
-   sn\_hs\_rm.safety\_inspection\_reader
-   canvas\_user
-   sn\_ohs\_im.action\_writer
-   survey\_reader

</td></tr><tr><td>

Safety register manager

 \[sn\_hs\_rm.safety\_register\_manager\]

</td><td>

Create, update, and delete safety registers

</td><td>

sn\_hs\_rm.safety\_register\_writer

</td></tr><tr><td>

Safety\_register\_writer

 \[sn\_hs\_rm.safety\_register\_writer\]

</td><td>

Create and update safety registers

</td><td>

-   sn\_wsd\_core.location\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_ohs\_im.action\_writer

</td></tr><tr><td>

Risk matrix reader

 \[sn\_hs\_rm.risk\_matrix\_reader\]

</td><td>

Can view risk matrixes

</td><td>

None

</td></tr><tr><td>

Job reader

 \[sn\_hs\_rm.job\_reader\]

</td><td>

Can view jobs defined in the Job register

</td><td>

None

</td></tr><tr><td>

JSA template reader

 \[sn\_hs\_rm.template\_reader\]

</td><td>

Can view job safety analysis templates

</td><td>

None

</td></tr><tr><td>

Control measure reader

 \[sn\_hs\_rm.control\_measure\_reader\]

</td><td>

Can view control measures

</td><td>

None

</td></tr><tr><td>

Hazard reader

 \[sn\_hs\_rm.hazard\_reader\]

</td><td>

Can view hazards

</td><td>

None

</td></tr><tr><td>

Hierarchy of controls reader

 \[sn\_hs\_rm.hierarchy\_of\_controls\_reader\]

</td><td>

Can view control measure categories

</td><td>

sn\_ohs\_im.hs\_profile\_reader

</td></tr><tr><td>

Inspection schedule reader

 \[sn\_hs\_rm.inspection\_schedule\_reader\]

</td><td>

Can view inspection schedules

</td><td>

None

</td></tr><tr><td>

Safety inspection reader

 \[sn\_hs\_rm.safety\_inspection\_reader\]

</td><td>

Can view safety inspections and its related records and fields

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader

-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.risk\_matrix\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_ohs\_im.incident\_reader
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Job safety analysis reader

 \[sn\_hs\_rm.job\_safety\_analysis\_reader\]

</td><td>

Can view job safety analyses

</td><td>

sn\_ohs\_im.hs\_profile\_reader

</td></tr><tr><td>

Risk assessment reader

 \[sn\_hs\_rm.risk\_assessment\_reader\]

</td><td>

Can view risk assessments and related records such as risk actions

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_rm.job\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.risk\_matrix\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_hs\_rm.control\_measure\_reader
-   sn\_ohs\_im.workspace\_user
-   canvas\_user
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Risk category reader

 \[sn\_hs\_rm.risk\_category\_reader\]

</td><td>

Can view risk categories

</td><td>

sn\_ohs\_im.hs\_profile\_reader

</td></tr><tr><td>

Safety register reader

 \[sn\_hs\_rm.safety\_register\_reader\]

</td><td>

Can view safety registers

</td><td>

None

</td></tr><tr><td>

Safety audit schedule reader

 \[sn\_hs\_rm.audit\_schedule\_reader\]

</td><td>

Can view audit schedule

</td><td>

None

</td></tr><tr><td>

Safety audit schedule writer

 \[sn\_hs\_rm.audit\_schedule\_writer\]

</td><td>

Can write audit schedule

</td><td>

sn\_hs\_rm.audit\_schedule\_reader

</td></tr><tr><td>

Safety audit manager

 \[sn\_hs\_rm.safety\_audit\_manager\]

</td><td>

Audit manager who can

-   Build audit surveys with the Survey designer
-   Create and manage safety audits in Health and Safety Workspace
-   Schedule safety audits Health and Safety Workspace
-   Complete audit surveys
-   Create, update, and delete audit findings, RCA, observations, risk assessments, and actions

</td><td>

-   sn\_ohs\_im.action\_manager
-   sn\_hs\_rm.safety\_audit\_writer
-   sn\_ohs\_im.observation\_writer
-   survey\_creator
-   sn\_ohs\_im.observation\_reader
-   sn\_hs\_rm.audit\_schedule\_writer

</td></tr><tr><td>

Safety audit reader

 \[sn\_hs\_rm.safety\_audit\_reader\]

</td><td>

Can view safety audit

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.risk\_matrix\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_ohs\_im.incident\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Safety audit writer

 \[sn\_hs\_rm.safety\_audit\_writer\]

</td><td>

Can write safety audit

</td><td>

-   sn\_ohs\_im.document\_writer
-   sn\_ohs\_im.workspace\_user
-   canvas\_user
-   sn\_hs\_rm.risk\_assessment\_writer
-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.observation\_writer\_restricted
-   survey\_reader
-   sn\_hs\_rm.safety\_audit\_reader
-   sn\_ohs\_im.document\_reader
-   survey\_creator
-   sn\_ohs\_im.observation\_reader

</td></tr><tr><td>

Industrial hygienist

 \[sn\_hs\_rm.industrial\_hygienist\]

</td><td>

Industrial hygienist who can:

-   Create exposure types
-   Conduct exposure assessments
-   Assign actions to people affected by exposure

</td><td>

-   sn\_ohs\_im.document\_writer
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_crm.company\_writter
-   sn\_ohs\_im.action\_schedule\_writer
-   sn\_ohs\_im.hs\_profile\_writer
-   sn\_hs\_rm.control\_measure\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_hs\_rm.exposure\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_hs\_crm.company\_reader
-   sn\_hs\_rm.exposure\_writer
-   sn\_ohs\_im.document\_reader

</td></tr><tr><td>

Exposure\_writer

 \[sn\_hs\_rm.exposure\_writer\]

</td><td>

Can create and update exposure related records

</td><td>

sn\_hs\_rm.exposure\_reader

</td></tr><tr><td>

Exposure reader

 \[sn\_hs\_rm.exposure\_reader\]

</td><td>

Can view exposure records

</td><td>

None

</td></tr><tr><td>

Permit requestor

 \[sn\_hs\_rm.permit\_requestor\]

</td><td>

Can request a permit and the type of work

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_rm.job\_safety\_analysis\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_hs\_rm.safety\_inspection\_reader

</td></tr><tr><td>

Permit approver

 \[sn\_hs\_rm.permit\_approver\]

</td><td>

Can approve or reject permit to work request.

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_rm.job\_safety\_analysis\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_hs\_rm.safety\_inspection\_reader

</td></tr><tr><td>

Permit coordinator

 \[sn\_hs\_rm.permit\_coordinator\]

</td><td>

-   Oversees the permit to work workflow.
-   Can issue, reject, or suspend a permit.

</td><td>

-   sn\_hs\_rm.permit\_writer
-   sn\_ohs\_im.action\_manager
-   sn\_ohs\_im.workspace\_user

</td></tr><tr><td>

Permit reader

 \[sn\_hs\_rm.permit\_reader\]

</td><td>

Can view a permit record.

</td><td>

None

</td></tr><tr><td>

Permit writer

 \[sn\_hs\_rm.permit\_writer\]

</td><td>

Can create and update permit request.

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_rm.job\_safety\_analysis\_reader
-   sn\_hs\_rm.permit\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_hs\_rm.safety\_inspection\_reader

</td></tr><tr><td>

Intelligent policy author

 \[ptw\_intelligent\_policy\_author\]

</td><td>

Intelligent policy author for Health and Safety permit to work who can-   View permits and their child records, for example, permit checklists
-   Create and update documents in the Health and Safety document library where the approval policy lives
-   Approve permits

</td><td>

-   sn\_ohs\_im.document\_writer
-   sn\_ohs\_im.document\_reader
-   sn\_hs\_rm.permit\_reader

</td></tr></tbody>
</table>## Tables installed

<table id="table_jy3_q3q_11c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Affected people

 \[sn\_hs\_rm\_affected\_people\]

</td><td>

Stores all users affected by exposures across all locations.

</td></tr><tr><td>

Audits

 \[sn\_hs\_rm\_audit\]

</td><td>

Stores all safety audit records created standalone as well as generated from audit schedules. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Audit schedule

 \[sn\_hs\_rm\_audit\_schedule\]

</td><td>

Stores all audit schedules created for safety audits. This table extends the Health and Safety schedule \[sn\_ohs\_im\_schedule\] table.

</td></tr><tr><td>

Audit questionnaire

 \[sn\_hs\_rm\_audit\_survey\]

</td><td>

Stores all audit questionnaires such as smart assessments and surveys for safety audits. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Criteria\[sn\_hs\_rm\_audit\_criteria\]

</td><td>

Stores all criteria for safety audits.

</td></tr><tr><td>

Item for review\[sn\_hs\_rm\_audit\_item\_for\_review\]

</td><td>

Stores all items for review for safety audits. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Objective\[sn\_hs\_rm\_audit\_objective\]

</td><td>

Stores all objectives for safety audits. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Control measure

 \[sn\_hs\_rm\_control\_measure\]

</td><td>

Stores all control measures that are in place to help prevent or mitigate hazards in your organization.

</td></tr><tr><td>

Document link

 \[sn\_hs\_rm\_document\_link\]

</td><td>

Stores all document links for jobs created in the job register.

</td></tr><tr><td>

Exposure

 \[sn\_hs\_rm\_exposure\]

</td><td>

Stores all exposure records generated from exposure assessments across all locations.

</td></tr><tr><td>

Exposure assessment

 \[sn\_hs\_rm\_exposure\_assessment\]

</td><td>

Stores all exposure assessments conducted for exposure types across all locations.

</td></tr><tr><td>

Exposure source

 \[sn\_hs\_rm\_exposure\_source\]

</td><td>

Stores all exposure sources identified for exposure measurements across all locations.

</td></tr><tr><td>

Exposure type

 \[sn\_hs\_rm\_exposure\_type\]

</td><td>

Stores all exposure types identified across all locations.

</td></tr><tr><td>

Finding

 \[sn\_hs\_rm\_finding\]

</td><td>

Stores all records of findings created for safety inspections. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Hazard

 \[sn\_hs\_rm\_hazard\]

</td><td>

Stores all identified and potential workplace hazards related to all jobs and task types in your organization.

</td></tr><tr><td>

Hazard assessment

 \[sn\_hs\_rm\_hazard\_assessment\]

</td><td>

Stores all hazard assessments performed as part of risk assessments.

</td></tr><tr><td>

Hierarchy of controls

 \[sn\_hs\_rm\_hierarchy\_of\_controls\]

</td><td>

Stores all categories for control measures in your organization. All controls that are related to hazards in your organization are arranged under these categories.

</td></tr><tr><td>

Persons informed

 \[sn\_hs\_rm\_informed\_persons\]

</td><td>

Stores names of all employees and workers who are informed of their job hazards when submitting JSAs.

</td></tr><tr><td>

Inspection

 \[sn\_hs\_rm\_inspection\]

</td><td>

Stores all safety inspection records created standalone as well as generated from inspection schedules. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Inspection schedule

 \[sn\_hs\_rm\_inspection\_schedule\]

</td><td>

Stores all inspection schedules created for safety inspections. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Job

 \[sn\_hs\_rm\_job\]

</td><td>

Stores all jobs with predefined hazards and controls created in the job register. These jobs can be used to quickly submit JSAs and conduct risk assessments.

</td></tr><tr><td>

Hazards and controls

 \[sn\_hs\_rm\_job\_hazard\]

</td><td>

Stores hazards and controls associated with all of the jobs defined in the job register.

</td></tr><tr><td>

Job Safety Analysis

 \[sn\_hs\_rm\_job\_safety\_analysis\]

</td><td>

Stores all job safety analyses \(JSAs\) submitted by employees through Employee Center and Now Mobile app.

</td></tr><tr><td>

Job step

 \[sn\_hs\_rm\_job\_step\]

</td><td>

Stores all jobs steps for the multi-step jobs defined in the job register.

</td></tr><tr><td>

JSA step\[sn\_hs\_rm\_jsa\_step\]

</td><td>

Stores all jobs steps that are added for multi-step jobs when submitting JSAs.

</td></tr><tr><td>

Exposure assessment document

 \[sn\_hs\_rm\_m2m\_exposure\_assessment\_document\]

</td><td>

Stores all documents related to exposure assessments across all locations.

</td></tr><tr><td>

Measurement

 \[sn\_hs\_rm\_measurement\]

</td><td>

Stores all measurements recorded for exposure assessments across all locations.

</td></tr><tr><td>

Permit checklist

 \[sn\_hs\_rm\_permit\_checklist\]

</td><td>

Stores information related to items, tasks, or steps in a checklist.

</td></tr><tr><td>

Permit to work

 \[sn\_hs\_rm\_work\_permit\]

</td><td>

Stores data related to the permit to work request.

</td></tr><tr><td>

Risk assessment

 \[sn\_hs\_rm\_risk\_assessment\]

</td><td>

Stores all records of risk assessments conducted. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Risk category

 \[sn\_hs\_rm\_risk\_category\]

</td><td>

Stores all risk categories for hazards in your organization. All workplace hazards related to all job types in your organization are arranged in these risk categories.

</td></tr><tr><td>

Risks and controls

 \[sn\_hs\_rm\_risk\_controls\]

</td><td>

Stores all Risks and controls records associated with all risk assessments.

</td></tr><tr><td>

Risk matrix

 \[sn\_hs\_rm\_risk\_matrix\]

</td><td>

Stores all risk matrixes created for your organization.

</td></tr><tr><td>

Risk tolerance

 \[sn\_hs\_rm\_risk\_tolerance\]

</td><td>

Stores all risk tolerance records associated with all risk matrixes created.

</td></tr><tr><td>

Safety Register

 \[sn\_hs\_rm\_safety\_register\]

</td><td>

Stores all safety registers created for the hazardous material used in your organization. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Asbestos Safety Register

 \[sn\_hs\_rm\_safety\_register\_asbestos\]

</td><td>

Stores all safety registers created for asbestos material used in your organization. This table extends the Safety Register \[sn\_hs\_rm\_safety\_register\] table.

</td></tr><tr><td>

Chemical Safety Register

 \[sn\_hs\_rm\_safety\_register\_chemical\]

</td><td>

Stores all safety registers created for chemicals. This table extends the Safety Register \[sn\_hs\_rm\_safety\_register\] table.

</td></tr><tr><td>

Template

 \[sn\_hs\_rm\_template\]

</td><td>

Stores all JSA templates with predefined hazards and controls for each job type in your organization.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Risk Management reference](../concept/hs-risk-mgmt-reference.md)

