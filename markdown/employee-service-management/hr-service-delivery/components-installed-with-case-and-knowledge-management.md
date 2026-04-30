---
title: Components installed with Case and Knowledge Management
description: Several types of components install with the activation of the Case and Knowledge Management plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Activate Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Components installed with Case and Knowledge Management

Several types of components install with the activation of the Case and Knowledge Management plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** The Human Resources Scoped app: Core \[com.sn\_hr\_core\] plugin activates the sn\_hr\_core.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only HR admin user by requiring a minimum number \(default is two\) of active users with those admin roles.

## Roles installed

<table id="table_stg_prr_4bb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Case and Knowledge Management administrator

 \[sn\_hr\_core.admin\]

</td><td>

Can access and configure Case and Knowledge Management.

</td><td>

-   approval\_admin
-   assignment\_rule\_admin
-   knowledge\_manager
-   link\_generator\_writer
-   schedule\_admin
-   sn\_cd.content\_admin
-   sn\_hr\_core.content\_writer
-   sn\_hr\_core.manager
-   sn\_hr\_integrations.admin
-   sn\_hr\_le.admin
-   sn\_hr\_pa.admin \(When the PA-Content Pack - HR Scoped App plugin activates.\)
-   sn\_hr\_sp.admin
-   sn\_hr\_sp.hrsp\_employee
-   sn\_templated\_snip.template\_snippet\_admin
-   template\_editor\_global

</td></tr><tr><td>

HR agent\[sn\_hr\_core.basic\]

</td><td>

Grants access to basic HR agents daily work need.

</td><td>

-   document\_management\_user
-   skill\_user
-   sn\_hr\_core.case\_writer
-   sn\_hr\_core.kb\_writer
-   sn\_hr\_core.profile\_writer
-   survey\_reader
-   sn\_hr\_core.report\_creator

</td></tr><tr><td>

HR case reader\[sn\_hr\_core.case\_reader\]

</td><td>

Grants access to read all HR cases.

</td><td>

None

</td></tr><tr><td>

HR case writer\[sn\_hr\_core.case\_writer\]

</td><td>

Grants access to write all HR cases.

</td><td>

-   sn\_hr\_core.case\_reader
-   sn\_templated\_snip.template\_snippet\_reader

</td></tr><tr><td>

HR content reader\[sn\_hr\_core.content\_reader\]

</td><td>

Grants read access to all the table records and their content.

</td><td>

None

</td></tr><tr><td>

HR content writer\[sn\_hr\_core.content\_writer\]

</td><td>

Grants access to create, update, read, and delete all the table records.

</td><td>

sn\_hr\_core.content\_reader

</td></tr><tr><td>

Alumni employee\[sn\_hr\_core.hrsm\_alumni\]

</td><td>

Grants role to the employee who has left the company.

</td><td>

None

</td></tr><tr><td>

Contingent employee\[sn\_hr\_core.hrsm\_contingent\]

</td><td>

Grants role to the employee who works temporary.

</td><td>

None

</td></tr><tr><td>

Contractor employee\[sn\_hr\_core.hrsm\_contractor\]

</td><td>

Grants role to the employee who works as a contractor.

</td><td>

None

</td></tr><tr><td>

Full-time employee\[sn\_hr\_core.hrsm\_employee\]

</td><td>

Grants role to the full-time employee.

</td><td>

None

</td></tr><tr><td>

New hire employee\[sn\_hr\_core.hrsm\_new\_hire\]

</td><td>

Grants role to the employee who is newly hired.

</td><td>

None

</td></tr><tr><td>

HR knowledge writer\[sn\_hr\_core.kb\_writer\]

</td><td>

Grants access to write all HR KB articles.

</td><td>

None

</td></tr><tr><td>

HR manager\[sn\_hr\_core.manager\]

</td><td>

Grants access to all HR cases, profiles, secure information.

</td><td>

-   approver\_user
-   catalog
-   catalog\_admin
-   skill\_admin
-   sn\_hr\_core.basic
-   sn\_hr\_core.secure\_info\_writer
-   sn\_templated\_snip.template\_snippet\_writer
-   survey\_admin

</td></tr><tr><td>

HR Performance Analytics Admin\[sn\_hr\_pa.admin\]

</td><td>

HR Performance Analytics Admin role for the scoped application. -   Access and modify the HR PA content packs.
-   Edits Performance Analytics properties.
-   Accesses Admin Console.
-   Launch Dependency Assessment.

 **Note:** This role is contained in the HR Admin \[sn\_hr\_core.admin\] role.

</td><td>

None

</td></tr><tr><td>

HR profile reader\[sn\_hr\_core.profile\_reader\]

</td><td>

Grants access to read all HR Profile records.

</td><td>

None

</td></tr><tr><td>

HR profile writer\[sn\_hr\_core.profile\_writer\]

</td><td>

Grants access to write all HR Profile records.**Note:** This role also grants write access to the Users \(sys\_user\) table.

</td><td>

sn\_hr\_core.profile\_reader

</td></tr><tr><td>

HR report creator\[sn\_hr\_core.report\_creator\]

</td><td>

Allows HR agents with the sn\_hr\_core.basic role to access the HR case \[sn\_hr\_core\_case\] and task \[sn\_hr\_core\_task\] tables to create reports.

</td><td>

 

</td></tr><tr><td>

HR secure information reader\[sn\_hr\_core.secure\_info\_reader\]

</td><td>

Grants access to read all HR cases, read basic user profile information, read secure user information.

</td><td>

sn\_hr\_core.profile\_reader

</td></tr><tr><td>

HR secure information writer\[sn\_hr\_core.secure\_info\_writer\]

</td><td>

Grants access to write all HR cases, write basic user profile information, write secure user information.

</td><td>

-   sn\_hr\_core.profile\_writer
-   sn\_hr\_core.secure\_info\_reader

</td></tr></tbody>
</table>You can assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

For further information on user administration and how to manage users, see [User administration](https://www.servicenow.com/docs/access?context=c_UserAdministration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto-close case

</td><td>

Automatically closes HR cases based on the configuration of the HR service for service activity and lifecycle event fulfillment types. This scheduled job runs daily.

</td></tr><tr><td>

Bulk case creation

</td><td>

Creates bulk cases. This scheduled job runs every six hours.

</td></tr><tr><td>

HR Daily Job

</td><td>

Sends reminder notifications to users based on certain HR task parameters. This scheduled job runs daily.

</td></tr><tr><td>

Migrate HR e-signature tasks

</td><td>

Migrates HR task templates and open HR tasks to the new HR task type for e-signature. Also disables the old HR task types for credential, e-signature, and sign document. This scheduled job runs on an on-demand basis.

</td></tr><tr><td>

Update Client Roles

</td><td>

Updates role assignments for HR profiles that are beginning or ending their employment based on the HR condition table. This scheduled job runs daily.**Note:** The base system assigns the HR Admin \(hradmin\) user to this scheduled job. If you delete the HR Admin user, ensure that you assign another user with the HR admin \(sn\_hr\_core.admin\) role to this scheduled job.

</td></tr></tbody>
</table>For further information on scheduled jobs and how to use them, see [Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Tables installed

The \* next to a table indicates it was deprecated for customers taking the Rome release to support a new data model. Existing customers using the legacy COEs and tables are not affected. These tables have been replaced by the Employee Relations feature. For more information, see [Employee Relations cases](../concept/hr-case-employee-relations.md).

<table id="table_pfy_pqk_hbb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\*Allegation\[sn\_hr\_er\_allegation\]

</td><td>

Contains information about an allegation type and subtype.**Note:** A non-metadata table.

</td></tr><tr><td>

\*Allegation Subtype\[sn\_hr\_core\_allegation\_sub\_type\]

</td><td>

Metadata table that provides 59 records to the base system. Allegation subtypes further define an allegation. For example:-   Allegation type = Discrimination
-   Allegation subtypes: Age, disability, Race, and so on.

</td></tr><tr><td>

\*Allegation Type\[sn\_hr\_core\_allegation\_type\]

</td><td>

Metadata table that provides base system records. Examples are:-   Customer Mistreatment
-   Discrimination
-   Drugs and Alcohol
-   Fraud and Theft
-   Harassment
-   Interpersonal Conflict
-   Misconduct
-   Retaliation
-   Wage and Scheduling Issue
-   Workplace Violence

</td></tr><tr><td>

\*Associated Allegation\[sn\_hr\_er\_m2m\_allegation\_party\]

</td><td>

Contains information that associates an allegation to subject of allegations.**Note:** A non-metadata table.

</td></tr><tr><td>

Bank Account\[sn\_hr\_core\_profile\_bank\_account\]

</td><td>

Bank account table.

</td></tr><tr><td>

Bulk Case Creation Data\[sn\_hr\_core\_bulk\_case\_creation\_data\]

</td><td>

Bulk case creation data table.

</td></tr><tr><td>

Bulk Case Creation Run\[sn\_hr\_core\_bulk\_case\_creation\_run\]

</td><td>

Bulk case creation run table.

</td></tr><tr><td>

Case Restriction Configuration\[sn\_hr\_er\_case\_restriction\]

</td><td>

Extends the COE Security Policy \[sn\_hr\_core\_coe\_security\_policy\] table.

</td></tr><tr><td>

Certification and License\[sn\_hr\_core\_certification\_and\_license\]

</td><td>

Certification and License table.

</td></tr><tr><td>

Client Role Rule\[sn\_hr\_core\_client\_role\_rule\]

</td><td>

Client role rule table.

</td></tr><tr><td>

COE\[sn\_hr\_core\_coe\]

</td><td>

Center of Excellence \(COE\) table.

</td></tr><tr><td>

COE Configuration Matching\[sn\_hr\_core\_coe\_config\_matching\]

</td><td>

Center of Excellence \(COE\) configuration matching table.

</td></tr><tr><td>

Compensation\[sn\_hr\_core\_compensation\]

</td><td>

Compensation table.

</td></tr><tr><td>

Compensation Bonus\[sn\_hr\_core\_bonus\]

</td><td>

Bonus compensation table.**Note:** This table is an extension of the Compensation table.

</td></tr><tr><td>

Compensation Salary\[sn\_hr\_core\_salary\]

</td><td>

Salary compensation table.**Note:** This table is an extension of the Compensation table.

</td></tr><tr><td>

Compensation Stocks\[sn\_hr\_core\_stocks\]

</td><td>

Stocks compensation table.**Note:** This table is an extension of the Compensation table.

</td></tr><tr><td>

Corrective Action\[sn\_hr\_er\_corrective\_action\]

</td><td>

Contains information on corrective actions associated with an ER case.**Note:** A non-metadata table.

</td></tr><tr><td>

Direct Deposit\[sn\_hr\_core\_direct\_deposit\]

</td><td>

Direct deposit table.

</td></tr><tr><td>

Employee Relations Case\[sn\_hr\_er\_case\]

</td><td>

Extends the HR case \[sn\_hr\_case\] table.**Note:** A non-metadata table.

</td></tr><tr><td>

HR Beneficiary\[sn\_hr\_core\_beneficiary\]

</td><td>

HR beneficiary table.

</td></tr><tr><td>

HR Benefit\[sn\_hr\_core\_benefit\]

</td><td>

HR benefits table.

</td></tr><tr><td>

HR Benefit Plan\[sn\_hr\_core\_benefit\_provider\]

</td><td>

HR benefit plan table.

</td></tr><tr><td>

HR Benefit Type\[sn\_hr\_core\_benefit\_type\]

</td><td>

HR benefit type table.

</td></tr><tr><td>

HR Case\[sn\_hr\_core\_case\]

</td><td>

HR case table.

</td></tr><tr><td>

HR Benefits Case\[sn\_hr\_core\_case\_benefits\]

</td><td>

HR benefits case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Compensation\[sn\_hr\_core\_case\_compensation\]

</td><td>

HR compensation case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Condition\[sn\_hr\_core\_condition\]

</td><td>

HR condition table.

</td></tr><tr><td>

HR Conditions for Criteria\[sn\_hr\_core\_m2m\_condition\_criteria\]

</td><td>

HR conditions for criteria table.

</td></tr><tr><td>

HR Contact\[sn\_hr\_core\_contact\]

</td><td>

HR contacts table.

</td></tr><tr><td>

HR Corporate Communications Case\[sn\_hr\_core\_case\_corporate\_communcations\]

</td><td>

HR corporate communications case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Criteria\[sn\_hr\_core\_criteria\]

</td><td>

HR criteria table.

</td></tr><tr><td>

HR Criteria for Links\[sn\_hr\_core\_m2m\_link\_template\]

</td><td>

HR criteria for links table.

</td></tr><tr><td>

HR Disability Benefit\[sn\_hr\_core\_disability\_benefit\]

</td><td>

HR disability benefits table.**Note:** This table is an extension of the HR Benefits table.

</td></tr><tr><td>

HR Disciplinary Issue Type\[sn\_hr\_core\_disciplinary\_issue\_type\]

</td><td>

HR disciplinary issue type table.

</td></tr><tr><td>

HR Disciplinary Warning Type\[sn\_hr\_core\_disciplinary\_warning\_type\]

</td><td>

HR disciplinary warning type table.

</td></tr><tr><td>

HR Document Acknowledgement\[sn\_hr\_core\_document\_acknowledgement\]

</td><td>

HR document acknowledgement table.

</td></tr><tr><td>

HR Document Template\[sn\_hr\_core\_document\_template\]

</td><td>

HR document template table.

</td></tr><tr><td>

HR Document Type\[sn\_hr\_core\_document\_type\]

</td><td>

HR document type table.

</td></tr><tr><td>

HR Employee Relations Case\[sn\_hr\_core\_case\_relations\]

</td><td>

HR employee relations case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Ethics Case\[sn\_hr\_core\_case\_ethics\]

</td><td>

HR ethics case table. **Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Global Mobility Case\[sn\_hr\_core\_case\_global\_mobility\]

</td><td>

HR global mobility case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Health Benefit\[sn\_hr\_core\_health\_benefit\]

</td><td>

HR health benefits table.**Note:** This table is an extension of the HR Benefits table.

</td></tr><tr><td>

HR Insurance Benefit\[sn\_hr\_core\_insurance\_benefit\]

</td><td>

HR insurance benefits table.**Note:** This table is an extension of the HR Benefits table.

</td></tr><tr><td>

\*HR Investigations Case\[sn\_hr\_core\_case\_investigation\]

</td><td>

HR investigations case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Operations Report\[sn\_hr\_core\_op\_report\]

</td><td>

HR operations report table.

</td></tr><tr><td>

HR Operations Report Frequency\[sn\_hr\_core\_op\_report\_frequency\]

</td><td>

HR operations report frequency table.

</td></tr><tr><td>

HR Operations Report Type\[sn\_hr\_core\_op\_report\_type\]

</td><td>

HR operations report type table.

</td></tr><tr><td>

HR Operations System\[sn\_hr\_core\_op\_system\]

</td><td>

HR operations system table.

</td></tr><tr><td>

HR Operations System to Report Type\[sn\_hr\_core\_op\_system\_to\_report\_type\]

</td><td>

HR operations system to report type table.

</td></tr><tr><td>

HR Payroll Case\[sn\_hr\_core\_case\_payroll\]

</td><td>

HR payroll case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR PDF Template\[sn\_hr\_core\_pdf\_template\]

</td><td>

HR PDF template table.**Note:** This table is an extension of the HR Document Template table.

</td></tr><tr><td>

\*HR Performance Case\[sn\_hr\_core\_case\_performance\]

</td><td>

HR performance case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Profile\[sn\_hr\_core\_profile\]

</td><td>

HR profiles table.

</td></tr><tr><td>

HR Retirement Benefit\[sn\_hr\_core\_retirement\_benefit\]

</td><td>

HR retirement benefits table.**Note:** This table is an extension of the HR Benefits table.

</td></tr><tr><td>

HR Service\[sn\_hr\_core\_service\]

</td><td>

HR services table.

</td></tr><tr><td>

HR Service Options\[sn\_hr\_core\_service\_option\]

</td><td>

HR service options table.

</td></tr><tr><td>

HR Talent Management Case\[sn\_hr\_core\_case\_talent\_management\]

</td><td>

HR talent management case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Task\[sn\_hr\_core\_task\]

</td><td>

HR task table.

</td></tr><tr><td>

HR Template\[sn\_hr\_core\_template\]

</td><td>

HR template table.

</td></tr><tr><td>

HR Tier Escalation\[sn\_hr\_core\_tier\_definition\]

</td><td>

HR tier escalation table.

</td></tr><tr><td>

HR Total Rewards Case\[sn\_hr\_core\_case\_total\_rewards\]

</td><td>

HR total rewards case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Visa Category\[sn\_hr\_core\_visa\_category\]

</td><td>

HR visa category table.

</td></tr><tr><td>

HR Workforce Administrator\[sn\_hr\_core\_case\_workforce\_admin\]

</td><td>

HR workforce administration case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HRIT Operations Case\[sn\_hr\_core\_case\_operations\]

</td><td>

HRIT operations case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

HR Lifecycle Events Case\[sn\_hr\_le\_case\]

</td><td>

HR lifecycle events case table.**Note:** This table is an extension of the HR Case table.

</td></tr><tr><td>

Interview\[sn\_hr\_er\_interview\]

</td><td>

Contains information related to ER interviews.**Note:** A non-metadata table.

</td></tr><tr><td>

Involved Party\[sn\_hr\_er\_involved\_party\]

</td><td>

Contains information on involved parties related to the ER case.**Note:** A non-metadata table.

</td></tr><tr><td>

Job\[sn\_hr\_core\_job\]

</td><td>

Job table.

</td></tr><tr><td>

Job Profile\[sn\_hr\_core\_job\_profile\]

</td><td>

Job profile table.

</td></tr><tr><td>

Language\[sn\_hr\_core\_language\]

</td><td>

Language table.

</td></tr><tr><td>

Matching Roles\[sn\_hr\_core\_matching\_roles\]

</td><td>

Matching roles table.

</td></tr><tr><td>

PDF Template Mapping\[sn\_hr\_core\_pdf\_template\_mapping\]

</td><td>

PDF template mapping table.

</td></tr><tr><td>

Position\[sn\_hr\_core\_position\]

</td><td>

Position table.

</td></tr><tr><td>

Relationship\[sn\_hr\_core\_relationship\]

</td><td>

Relationship table.

</td></tr><tr><td>

Service Activity\[sn\_hr\_core\_service\_activity\]

</td><td>

Service activity table.

</td></tr><tr><td>

Sn HR Core Background Search Details\[sn\_hr\_core\_service\_activity\]

</td><td>

Background check search details table.

</td></tr><tr><td>

Sn HR Core Badge\[sn\_hr\_core\_badge\]

</td><td>

Badge table.

</td></tr><tr><td>

Sn HR Core Bulk Case Request\[sn\_hr\_core\_bulk\_case\_request\]

</td><td>

Bulk case request table.

</td></tr><tr><td>

Sn HR Core Config Case\[sn\_hr\_core\_config\_case\]

</td><td>

HR service-based case configuration table.

</td></tr><tr><td>

Sn HR Core Config Case Creation\[sn\_hr\_core\_config\_case\_creation\]

</td><td>

Case creation configuration table.

</td></tr><tr><td>

Sn HR Core Config Case Creation Service\[sn\_hr\_core\_config\_case\_creation\_service\]

</td><td>

Case creation service configuration table.

</td></tr><tr><td>

Sn HR Core Email Content\[sn\_hr\_core\_email\_content\]

</td><td>

Email content table.

</td></tr><tr><td>

Sn HR Core Substitute Approver\[sn\_hr\_core\_substitute\_approver\]

</td><td>

Substitute approver table.

</td></tr><tr><td>

Topic Category\[sn\_hr\_core\_topic\_category\]

</td><td>

Topic category table.

</td></tr><tr><td>

Topic Detail\[sn\_hr\_core\_topic\_detail\]

</td><td>

Topic detail table.

</td></tr><tr><td>

Tuition Reimbursement\[sn\_hr\_core\_tuition\_reimbursement\]

</td><td>

Tuition reimbursement table.

</td></tr><tr><td>

User Fields On Case\[sn\_hr\_core\_service\_approval\_option\]

</td><td>

User fields on case table.

</td></tr><tr><td>

Who is covered\[sn\_hr\_core\_who\_is\_covered\]

</td><td>

Who is covered table.

</td></tr></tbody>
</table>For further information on table administration and how to manage data, see [Table administration](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Activate Case and Knowledge Management](../task/activate-case-and-knowledge-management-scoped.md)

