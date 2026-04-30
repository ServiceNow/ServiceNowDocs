---
title: Components installed with Health and Safety Core
description: Several types of components are installed with installation of the Health and Safety Core data model, including tables, user roles, and scheduled jobs. This data model is automatically installed with Health and Safety applications.
locale: en-US
release: zurich
product: Health and Safety Core
classification: health-and-safety-core
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Reference, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Components installed with Health and Safety Core

Several types of components are installed with installation of the Health and Safety Core data model, including tables, user roles, and scheduled jobs. This data model is automatically installed with Health and Safety applications.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Plugins installed

<table id="table_m1h_gg4_cyb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Playbook Experience Core \[com.glide.playbook\_experience.config\]

</td><td>

Activates playbook for Health and Safety incidents.

</td></tr><tr><td>

Explicit Roles

</td><td>

Enables the assignment of \[snc\_external\] role for external workers such as contractor workers.

</td></tr><tr><td>

Document Management\[com.snc.platform\_document\_management\]

</td><td>

Enables you to manage documents in Health and Safety applications. Provides storage space and a filing system that allows you to easily upload, retrieve, and delete documents.

</td></tr></tbody>
</table>## Store applications installed

<table id="table_ulz_4tw_llba"><thead><tr><th>

Store application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Core \[sn\_wsd\_core\]

</td><td>

Enables workplace locations for Health and Safety Incident Management.**Important:** The application installation doesn’t install the location demo data for the Workplace Core location model. As a workaround, repair the Workplace Core plugin with the **Load demo data** option.

</td></tr><tr><td>

Health and Safety Components

</td><td>

Seismic component that enables the visual injury and illness picker, for example, in the Health and Safety Incident Management application. The component is used by safety teams to log injuries associated with an injury and illness report and quickly see the types and severity of injuries​.

</td></tr></tbody>
</table>## Roles installed

<table id="table_hnm_jnp_stb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Safety admin

 \[sn\_ohs\_im.admin\]

</td><td>

Administrator for Health and Safety applications who can:-   Configure the Health and Safety Core and other Health and Safety applications
-   Has read, write, and create access to health and safety data
-   Grant Health and Safety roles

</td><td>

-   template\_read\_global
-   agent\_workspace\_user
-   sn\_ohs\_im.manager
-   workspace\_user
-   sn\_hs\_rm.safety\_register\_manager
-   sn\_hs\_rm.hierarchy\_of\_controls\_manager
-   sn\_ohs\_im.hs\_profile\_writer
-   sn\_hs\_rm.risk\_assessment\_manager
-   sn\_ohs\_im.operations\_manager
-   sn\_hs\_rm.safety\_audit\_manager
-   sn\_hs\_crm.contractor\_coordinator
-   sn\_hs\_rm.risk\_manager
-   sn\_hs\_cm.case\_manager
-   sn\_hs\_rm.risk\_category\_manager
-   sn\_hs\_rm.risk\_data\_manager
-   sn\_ohs\_im.report\_mapping\_manager
-   sn\_ohs\_im.compliance\_manager
-   sn\_hs\_rm.safety\_inspection\_manager
-   sn\_hs\_rm.permit\_coordinator
-   sn\_hs\_rm.industrial\_hygienist
-   canvas\_user
-   sn\_ohs\_im.meeting\_manager
-   platform\_document\_management\_admin
-   sn\_ohs\_im.document\_admin
-   sn\_ohs\_im\_reporter

</td></tr><tr><td>

Safety compliance manager

 \[sn\_ohs\_im.compliance\_manager\]

</td><td>

Administrator for Health and Safety reporting-related tasks who can:-   Manage list of establishments
-   Review and determine which injuries and illnesses are recordable
-   Access and manage report generation such as OSHA 300 log, 300A summary, and 301 incident reports. For more information, see [Health and Safety injury and illness reports](../../ohs-incident-management/concept/injury-illness-reports.md).

</td><td>

-   sn\_ohs\_im.establishment\_writer
-   sn\_ohs\_im.establishment\_reader
-   sn\_ohs\_im.report\_mapping\_manager
-   sn\_ohs\_im.hs\_profile\_reader
-   canvas\_user

</td></tr><tr><td>

Safety reporter

 \[sn\_ohs\_im.reporter\]

</td><td>

Can submit Health and Safety incidents, observations, and questions from Employee Center and Now Mobile app

</td><td>

-   sn\_wsd\_core.workplace\_user
-   sn\_ohs\_im.incident\_reporter
-   sn\_hs\_cm.case\_reporter
-   sn\_ohs\_im.observation\_reporter
-   sn\_ohs\_im.meeting\_minute\_reader
-   sn\_ohs\_im.meeting\_reader

</td></tr><tr><td>

Sensitive content user

 \[sn\_ohs\_im.sensitive\_content\_user\]

</td><td>

Can view sensitive content such as incidents and injuries marked as sensitive.**Note:** When a report is generated \(such as OSHA 300 or 300A\), it contains all incidents, including the ones marked as sensitive, according to the template. However, sensitive information is not disclosed in the report as incident details are not included.

</td><td>

None

</td></tr><tr><td>

Observation sensitive content user

 sn\_ohs\_im.sensitive\_observation\_content\_user

</td><td>

Safety agents can view sensitive content on safety observations reported anonymously.**Note:** The agent cannot view the anonymous report without this role assigned to them.

</td><td>

None

</td></tr><tr><td>

Safety workspace user

 \[sn\_ohs\_im.workspace\_user\]

</td><td>

Can access Health and Safety Workspace.

</td><td>

workspace\_user

</td></tr><tr><td>

Safety report manager

 \[sn\_ohs\_im.report\_manager\]

</td><td>

Safety report manager who can:-   Create and manage report field mappings in Health and Safety Workspace
-   Script report field mappings

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   canvas\_user
-   sn\_ohs\_im.report\_mapping\_manager

</td></tr><tr><td>

Report mapping manager

 \[sn\_ohs\_im.report\_mapping\_manager\]

</td><td>

Can create, read, update, and delete report field mappings

</td><td>

-   sn\_ohs\_im.report\_mapping\_reader
-   sn\_ohs\_im.workspace\_user
-   sn\_ohs\_im.report\_mapping\_writer
-   sn\_ohs\_im.report\_mapping\_scripting
-   sn\_hs\_rm.risk\_category\_reader
-   sn\_hs\_rm.job\_reader
-   sn\_hs\_rm.job\_safety\_analysis\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.risk\_matrix\_reader
-   sn\_hs\_rm.hierarchy\_of\_controls\_reader
-   sn\_hs\_rm.audit\_schedule\_reader
-   sn\_hs\_rm.control\_measure\_reader
-   sn\_hs\_rm.safety\_register\_reader
-   sn\_ohs\_im.incident\_reader
-   sn\_hs\_rm.risk\_assessment\_reader
-   sn\_hs\_rm.safety\_inspection\_reader
-   sn\_ohs\_im.establishment\_reader
-   sn\_hs\_crm.company\_reader
-   sn\_hs\_cm.case\_reader
-   sn\_ohs\_im.action\_reader
-   sn\_hs\_rm.safety\_audit\_reader
-   sn\_ohs\_im.document\_reader
-   sn\_ohs\_im.observation\_reader
-   sn\_hs\_rm.inspection\_schedule\_reader
-   sn\_hs\_cm.rtw\_reader
-   sn\_ohs\_im.action\_schedule\_reader

</td></tr><tr><td>

Report mapping reader

 \[sn\_ohs\_im.report\_mapping\_reader\]

</td><td>

Can view report field mappings

</td><td>

None

</td></tr><tr><td>

Report mapping scripting

 \[sn\_ohs\_im.report\_mapping\_scripting\]

</td><td>

Can create, update, and delete script for report field mappings

</td><td>

None

</td></tr><tr><td>

Report mapping writer

 \[sn\_ohs\_im.report\_mapping\_writer\]

</td><td>

Can create, read, and update report field mappings

</td><td>

None

</td></tr><tr><td>

Safety action manager

 \[sn\_ohs\_im.action\_manager\]

</td><td>

Can perform all operations related to Health and Safety Actions

</td><td>

-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.action\_reader
-   sn\_ohs\_im.action\_schedule\_writer
-   sn\_ohs\_im.action\_schedule\_reader

</td></tr><tr><td>

Safety action writer

 \[sn\_ohs\_im.action\_writer\]

</td><td>

Can create and update Health and Safety Actions

</td><td>

sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Safety action reader

 \[sn\_ohs\_im.action\_reader\]

</td><td>

Can view Health and Safety Actions

</td><td>

None

</td></tr><tr><td>

Safety action writer restricted

 \[sn\_ohs\_im.action\_writer\_restricted\]

</td><td>

Can create and update Health and Safety Actions when all restrictions have been met

</td><td>

-   sn\_ohs\_im.action\_schedule\_writer
-   sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Establishment writer

 \[sn\_ohs\_im.establishment\_writer\]

</td><td>

Can create and update establishment records in Health and Safety Workspace

</td><td>

None

</td></tr><tr><td>

Establishment reader

 \[sn\_ohs\_im.establishment\_reader\]

</td><td>

Can view records in Health and Safety Workspace

</td><td>

None

</td></tr><tr><td>

Safety incident manager

 \[sn\_ohs\_im.incident\_manager\]

</td><td>

Can perform all operations related to Health and Safety incidents

</td><td>

-   sn\_ohs\_im.incident\_writer
-   sn\_ohs\_im.incident\_reader

</td></tr><tr><td>

Safety incident writer

 \[sn\_ohs\_im.incident\_writer\]

</td><td>

Can create and update Health and Safety incidents

</td><td>

sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Safety incident reader

 \[sn\_ohs\_im.incident\_reader\]

</td><td>

Can view Health and Safety incidents

</td><td>

-   sn\_hs\_rm.risk\_category\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_hs\_rm.template\_reader

</td></tr><tr><td>

Safety incident reporter

 \[sn\_ohs\_im.incident\_reporter\]

</td><td>

Can submit Health and Safety incidents

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_hs\_rm.risk\_category\_reader
-   sn\_hs\_rm.hazard\_reader
-   sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Safety incident writer restricted

 \[sn\_ohs\_im.incident\_writer\_restricted\]

</td><td>

Can create and update Health and Safety incidents when all restrictions have been met

</td><td>

sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Safety observation manager

 \[sn\_ohs\_im.observation\_manager\]

</td><td>

Can perform all operations related to Health and Safety observations

</td><td>

-   sn\_ohs\_im.observation\_writer
-   sn\_ohs\_im.observation\_reader

</td></tr><tr><td>

Safety observation writer

 \[sn\_ohs\_im.observation\_writer\]

</td><td>

Can create and update Health and Safety observations

</td><td>

sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Safety observation reporter

 \[sn\_ohs\_im.observation\_reporter\]

</td><td>

Can submit Health and Safety observations

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Safety observation reader

 \[sn\_ohs\_im.observation\_reader\]

</td><td>

Can view Health and Safety observations

</td><td>

None

</td></tr><tr><td>

Safety observation writer restricted

 \[sn\_ohs\_im.observation\_writer\_restricted\]

</td><td>

Can create and update Health and Safety observations when all restrictions have been met

</td><td>

sn\_wsd\_core.location\_reader

</td></tr><tr><td>

Document admin

 \[sn\_ohs\_im.document\_admin\]

</td><td>

Administrator for Health and Safety documents who can:-   Add, update, and delete Health and Safety related documents in the **Standards and documentation** list
-   Grant access to **Standards and documentation** list

</td><td>

-   sn\_ohs\_im.document\_reader
-   sn\_ohs\_im.document\_writer

</td></tr><tr><td>

Document reader

 \[sn\_ohs\_im.document\_reader\]

</td><td>

Can view Health and Safety documents

</td><td>

None

</td></tr><tr><td>

Document writer

 \[sn\_ohs\_im.document\_writer\]

</td><td>

Can add and update Health and Safety related documents in the **Standards and documentation** list

</td><td>

None

</td></tr><tr><td>

Safety meeting manager

 \[sn\_ohs\_im.meeting\_manager\]

</td><td>

Safety meeting coordinator who can:-   Schedule safety meetings and create invite lists and agendas
-   Create Health and Safety actions for safety meetings
-   Add related documents to safety meetings
-   Mark safety meetings as sensitive and assign the sensitive meeting content user role

</td><td>

-   sn\_ohs\_im.meeting\_writer
-   sn\_ohs\_im.meeting\_minute\_taker

</td></tr><tr><td>

Sensitive meeting content user

 \[sn\_ohs\_im.sensitive\_meeting\_content\_user\]

</td><td>

Can view safety meetings and meeting minutes marked as sensitive

</td><td>

None

</td></tr><tr><td>

Safety meeting minute taker

 \[sn\_ohs\_im.meeting\_minute\_taker\]

</td><td>

Safety meeting minute taker who can:-   Log meeting minutes for a safety meeting
-   Mark attendance for meeting attendees
-   Create actions for meeting minutes
-   Mark meeting minutes as sensitive

</td><td>

-   sn\_ohs\_im.meeting\_reader
-   sn\_ohs\_im.meeting\_minute\_writer

</td></tr><tr><td>

Safety meeting writer

 \[sn\_ohs\_im.meeting\_writer\]

</td><td>

Can create and update Health and Safety meetings

</td><td>

-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.document\_writer
-   sn\_ohs\_im.meeting\_reader
-   sn\_ohs\_im.action\_schedule\_writer

</td></tr><tr><td>

Safety meeting reader

 \[sn\_ohs\_im.meeting\_reader\]

</td><td>

Can view Health and Safety meetings

</td><td>

-   sn\_ohs\_im.action\_schedule\_reader
-   sn\_ohs\_im.document\_reader
-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Safety meeting minute writer

 \[sn\_ohs\_im.meeting\_minute\_writer\]

</td><td>

Can create and update meeting minutes for Health and Safety meetings

</td><td>

-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.meeting\_minute\_reader

</td></tr><tr><td>

Safety meeting minute reader

 \[sn\_ohs\_im.meeting\_minute\_reader\]

</td><td>

Can view meeting minutes for Health and Safety meetings

</td><td>

-   sn\_ohs\_im.hs\_profile\_reader
-   sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Health and Safety profile writer

 \[sn\_ohs\_im.hs\_profile\_writer\]

</td><td>

Health and Safety profile writer who:-   Has create access to the Health and Safety profile \[sn\_ohs\_im\_health\_and\_safety\_profile\] table
-   Can assign and update Health and Safety profile to users in your organization, including employees, visitors, and contractors

</td><td>

sn\_ohs\_im.hs\_profile\_reader

</td></tr><tr><td>

Health and Safety profile reader

 \[sn\_ohs\_im.hs\_profile\_reader\]

</td><td>

Can view users with Health and Safety profile in your organization

</td><td>

none

</td></tr><tr><td>

Safety action schedule writer

 \[n\_ohs\_im.action\_schedule\_writer\]

</td><td>

Can write, create, or delete access for action schedule table.

</td><td>

-   sn\_ohs\_im.action\_writer
-   sn\_ohs\_im.action\_schedule\_reader

</td></tr><tr><td>

Safety action schedule reader

 \[sn\_ohs\_im.action\_schedule\_reader\]

</td><td>

Can view safety action schedules.

</td><td>

sn\_ohs\_im.action\_reader

</td></tr><tr><td>

Health and Safety workspace user

 \[sn\_ohs\_im.workspace\_user\]

</td><td>

Has access to the Health and Safety Workspace.

</td><td>

workspace\_user

</td></tr></tbody>
</table>## Tables installed

<table id="table_lnm_jnp_stb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety action

 \[sn\_ohs\_im\_action\]

</td><td>

Stores all actionable outputs from all safety incidents, observations, and root cause analyses.​ This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

Health and Safety document \(Deprecated\)

 \[sn\_ohs\_im\_document\]

</td><td>

Stores Health and Safety related documents. This table has been deprecated.**Note:** All Health and Safety related documents are now stored in the Health and Safety document \[sn\_ohs\_im\_document\_v2\] table. For information on migrating your existing safety documents from the deprecated table into the new Health and Safety document \[sn\_ohs\_im\_document\_v2\] table, see [Migrate existing safety documents to the Document library](../task/hs-migrate-sync-existing-safety-document-docs-library.md).

</td></tr><tr><td>

Health and Safety document

 \[sn\_ohs\_im\_document\_v2\]

</td><td>

Stores all Health and Safety related documents. This table extends the Document \[ds\_document\] table of Document Management application.

</td></tr><tr><td>

Health and Safety document version

 \[sn\_ohs\_im\_document\_version\]

</td><td>

Stores all versions of Health and Safety related documents. This table extends the Versions \[ds\_document\_version\] table of Document Management application.

</td></tr><tr><td>

Health and Safety profile

 \[sn\_ohs\_im\_health\_and\_safety\_profile\]

</td><td>

Stores all users with Health and Safety profile in your organization, including employees, visitors, and contractors.

</td></tr><tr><td>

Asset

 \[sn\_ohs\_im\_m2m\_task\_sn\_ent\_asset\]

</td><td>

Maps Health and Safety task \[sn\_ohs\_im\_task\] to Enterprise Asset​ to track assets involved in incidents​ and observations.**Note:** Installs only when Expanded Model and Asset Classes \[sn\_ent\] application is installed. For more information, see [Additional features in Health and Safety](../../ohs-incident-management/task/install-hs-incident-mgmt.md#table_ix1_bff_gxb)

</td></tr><tr><td>

Meeting

 \[sn\_ohs\_im\_meeting\]

</td><td>

Stores all safety meeting records. This table extends the Health and Safety task \[sn\_ohs\_im\_task\] table.

</td></tr><tr><td>

M2M action task

 sn\_ohs\_im\_m2m\_ohs\_task\_action

</td><td>

Stores all action tasks created for safety meetings.

</td></tr><tr><td>

Health and Safety m2m meeting document \(Deprecated\)

 \[sn\_ohs\_im\_m2m\_meeting\_document\]

</td><td>

Stores documents related to safety meetings.**Note:** All safety meetings related documents are now stored in the Health and Safety document \[sn\_ohs\_im\_document\_v2\] table.

</td></tr><tr><td>

Health and Safety m2m meeting minute action

 \[sn\_ohs\_im\_m2m\_meeting\_minute\_action\]

</td><td>

Stores all actions created for safety meetings.

</td></tr><tr><td>

Health and Safety meeting attendee

 \[sn\_ohs\_im\_meeting\_attendee\]

</td><td>

Stores all attendees added to safety meetings.

</td></tr><tr><td>

Health and Safety meeting minute

 \[sn\_ohs\_im\_meeting\_minute\]

</td><td>

Stores all meeting minute records created for safety meetings.

</td></tr><tr><td>

5 Whys root cause analysis

 \[sn\_ohs\_im\_rca\_five\_whys\]

</td><td>

Instance of a Root Cause Analysis used by the safety team to identify the root cause of safety tasks, for example, Health and Safety incident \[sn\_ohs\_im\_incident\].​

</td></tr><tr><td>

Root cause analysis

 \[sn\_ohs\_im\_rca\]

</td><td>

Reference base Health and Safety task \[sn\_ohs\_im\_task\] so that it can be associated with any table that extends Health and Safety Task, for example, Health and Safety incident \[sn\_ohs\_im\_incident\].​ This table is the base table extended by all RCA types.

</td></tr><tr><td>

ICAM root cause analysis

 \[sn\_ohs\_im\_rca\_icam\]

</td><td>

Instance of a Root Cause Analysis \[sn\_ohs\_im\_rca\] used by the safety team to identify the root cause of safety inspection findings.​

</td></tr><tr><td>

Report field mapping

 \[sn\_ohs\_im\_report\_field\_mapping\]

</td><td>

Stores all report field mappings created. These mappings enable you to import your reporting PDF templates and map its fields with safety record fields.

</td></tr><tr><td>

Form field mapping

 \[sn\_ohs\_im\_report\_form\_field\_mapping\]

</td><td>

Stores all form field mappings created between your reporting PDF templates' fields and safety records' fields. These mappings help to generate reports from safety records with fields auto-populated in your PDF template.

</td></tr><tr><td>

Schedule

 \[sn\_ohs\_im\_schedule\]

</td><td>

Stores all records of Health and Safety related schedules. Several Health and Safety tables extend this table, for example, Audit schedule \[sn\_hs\_rm\_audit\_schedule\].

</td></tr><tr><td>

Action schedule

 \[sn\_ohs\_im\_action\_schedule\]

</td><td>

Stores records of Health and Safety action schedules.

</td></tr><tr><td>

Health and Safety task

 \[sn\_ohs\_im\_task\]

</td><td>

Extends core Task table. Several Health and Safety tables extend this table for shared fields, for example, WSD Location \[sn\_wsd\_core\_workplace\_location\].

</td></tr><tr><td>

Health and Safety visitor

 sn\_ohs\_im\_health\_and\_safety\_visitor

</td><td>

Stores records of all visitors that have visited your organization or site.

</td></tr></tbody>
</table>**Parent Topic:**[Health and Safety Core reference](../concept/hs-core-reference.md)

**Related topics**  


[Health and Safety action form](../../ohs-incident-management/reference/hs-action-form.md)

[Health and safety action schedule form](../../ohs-incident-management/reference/hs-health-safety-action-schedule-form.md)

[Health and Safety profile form](../../ohs-incident-management/reference/hs-health-safety-profile-form.md)

[Health and Safety document version form](../../ohs-incident-management/reference/hs-document-form.md)

[Health and Safety report field mapping form](../../ohs-incident-management/reference/hs-report-field-mapping-form.md)

[Health and Safety meeting form](../../ohs-incident-management/reference/hs-safety-meeting-form.md)

[Health and Safety meeting attendee form](../../ohs-incident-management/reference/hs-safety-meeting-attendee-form.md)

