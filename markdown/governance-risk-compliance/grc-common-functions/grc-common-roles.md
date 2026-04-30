---
title: Common roles in Governance, Risk, and Compliance
description: Certain common roles are used in multiple GRC modules.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [GRC reference, Common GRC features, Governance, Risk, and Compliance]
---

# Common roles in Governance, Risk, and Compliance

Certain common roles are used in multiple GRC modules.

<table id="table_cqv_djm_nnb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

GRC Business User\[sn\_grc.business\_user\]

</td><td>

Role that is a part of the GRC Profiles application. Assign this role to users who require access only to GRC applications for performing their assigned tasks, providing them limited access to data and information relevant to those tasks. For example, assign this role to a business user who must respond to an attestation or risk assessment, or who must remediate an issue.Starting with the 14.x release, the following permissions are available to the users with the sn\_grc.business\_user role:

 Policy and Compliance Management:

-   Create issues or view all issues that are assigned to them or their group.
-   Accept and approve evidence responses.
-   Assign a remediation task.
-   Acknowledge policies.
-   Contribute to policies.
-   Group or ungroup attestations.
-   Request or approve policy exceptions.
-   Report issues.
-   Respond to observations.
-   Submit and request issue triages.
-   Take an attestation.

 Risk Management:

-   Create or view all issues that are assigned to them or their group.
-   Assign indicator tasks.
-   Assign issues.
-   Assign remediation tasks.
-   Assign risk event tasks.
-   Assign risk response tasks.
-   Approve or assess an advanced risk assessment.
-   Respond to indicator tasks.
-   Respond to the risk identification questionnaire.
-   Respond to the metrics data task.
-   Report issues.
-   Submit issue triage requests.
-   Take the risk assessment.
-   View the risk assessment scope.
-   View risk statements.
-   View the risk assessment scope.
-   View and report risk events.
-   View indicator supporting data.

 Integration with Project Portfolio Management:

-   Create a risk from a library.
-   Elevate an enterprise risk.
-   Initiate an object assessment.
-   View the Project Risk Overview dashboard.

 During an upgrade to either version 11.x or 12.x of GRC: Profiles, users who have previously performed a GRC operation in the past 90 days are automatically assigned with the sn\_grc.business\_user role. This is a one-time event. The group and role are assigned once during the 11.x or 12.x upgrade.

 For more information on the sn\_grc.business\_user role, see [KB0864247](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0864247).

**Note:** You must log in to Now Support to view the Knowledge Base articles.

 **Note:** You can manage who can access your GRC records with the GRC user roles. Earlier, your users with the snc\_internal role could also access the GRC records. As part of the security updates, each GRC application has modified access control lists \(ACLs\) where access to the GRC records is restricted only to the users with the GRC roles.

**Note:** When you \(a GRC user\) run a job to create a record, this will create an entry to the user in the Unique user table.

</td><td>

-   sn\_grc.user\_hierarchy\_reader
-   workspace\_user
-   sn\_grc\_workspace.task\_reader
-   canvas\_user

</td></tr><tr><td>

GRC Business User – Lite \[sn\_grc.business\_user\_lite\]

</td><td>

Role that enables a user to perform only a subset of the tasks that can be performed by the sn\_grc.business\_user. This role is applicable only for customers who are entitled to and have installed the GRC: Business User – Lite application from the ServiceNow Store. Risk Lite Operators are users who have the right to perform only one or more of the listed operations. The users with this role can perform the following activities:-   Read or update the policy acknowledgment, control attestation, take attestation, issues that are assigned to them, remediation task, or evidence request.
-   Report or read the submitted issues, risk events, or policy exceptions.

Risk Management

-   Update issues or view all the issues that are assigned to them or their group.
-   Approve advanced risk assessments.

**Note:** To enable lite operators to approve advanced risk assessments, the administrator must manually add the sn\_risk\_advanced.ara\_approver role to GRC: Business User Lite.

-   Respond to risk response tasks.
-   Approve risk response tasks.
-   Review, approve, or reject a risk event.
-   Respond to a risk identification questionnaire.
-   Update any assigned risk event task.
-   Review or respond to the metrics data tasks.
-   Assign indicator tasks.
-   Respond to indicator task requests.
-   Respond to indicator tasks.
-   Approve policy exceptions and evidence requests.

</td><td>

-   sn\_grc\_workspace.task\_reader
-   canvas\_user
-   sn\_grc.user\_hierarchy\_reader

</td></tr><tr><td>

GRC Admin\[sn\_grc.admin\]

</td><td>

Role that provides a user with administrative access to the GRC suite of applications and modules.

</td><td>

-   business\_process\_admin
-   sn\_grc.user\_hierarchy\_admin
-   sn\_grc\_workspace.task\_admin
-   sn\_grc.manager
-   sn\_data\_registry.admin

</td></tr><tr><td>

GRC System Adminsn\_grc.sn\_grc\_system\_admin

</td><td>

Role that is a system role for running scheduled jobs. This role is equivalent to the admin role. For example, if you want to run a scheduled job for policy acknowledgment, you can set up the system to run the job as GRC admin. The GRC system administrator is a default user that contains the sn\_grc.sn\_grc\_system\_admin role.**Note:** This role isn’t assigned to a person. It’s a technical back-end role that is used for running the scheduled jobs.

</td><td>

-   admin
-   import\_admin
-   sn\_grc.admin

</td></tr><tr><td>

GRC Reader \[sn\_grc.reader\]

</td><td>

Role that provides a user with read access to the GRC suite of applications and modules.

</td><td>

-   pa\_viewer
-   cmdb\_read
-   sn\_data\_registry.reader

</td></tr><tr><td>

GRC Manager\[sn\_grc.manager\]

</td><td>

Role that provides a user with management access to the GRC suite of applications and modules.

</td><td>

-   sn\_grc.user
-   sn\_grc.compliance\_manager
-   business\_process\_manager
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

GRC User \[sn\_grc.user\]

</td><td>

Role that provides a user with management access to the GRC suite of applications and modules.

</td><td>

-   sn\_grc.reader
-   business\_process\_user
-   sn\_grc\_pa.sn\_grc\_pa\_viewer

</td></tr><tr><td>

GRC Developer\[sn\_grc.developer\]

</td><td>

Role that enables a user to perform script-based work such as write scripted factors, scripted formulae for advanced risk assessment, scripted indicators, and so on in GRC.

</td><td>

sn\_grc.admin

</td></tr><tr><td>

GRC Confidential User\[sn\_grc.confidential\_user\]

</td><td>

Role that provides a user with access to the GRC confidential records.

</td><td>

None

</td></tr><tr><td>

GRC User Hierarchy Reader \[sn\_grc.user\_hierarchy\_reader\]

</td><td>

Role that provides a user with read access to the records in the sn\_grc\_user\_hierarchy table.

</td><td>

None

</td></tr><tr><td>

GRC User Hierarchy Admin \[sn\_grc.user\_hierarchy\_admin\]

</td><td>

Role that enables a user to create or delete the records in the sn\_grc\_user\_hierarchy\_configuration table.

</td><td>

None

</td></tr><tr><td>

Workspace task reader \[sn\_grc\_workspace.task\_reader\]

</td><td>

Role that enables a user to read the records in the configuration tables such as the tab configuration, applicable tables, and so on.

</td><td>

None

</td></tr><tr><td>

Audit reader \[sn\_audit.reader\]

</td><td>

Role that enables a user to read the audits and audit-related tables. This role is applicable only for customers who are entitled to and have installed the GRC: Business User – Lite application from the ServiceNow Store.

</td><td>

None

</td></tr><tr><td>

Audit approver \[sn\_audit.approver\]

</td><td>

Role that enables a user to approve the audits. This role is applicable only for customers who are entitled to and have installed the GRC: Business User – Lite application from the ServiceNow Store.

</td><td>

None

</td></tr><tr><td colspan="3">

Roles that are installed with the GRC Employee User application

</td></tr><tr><td colspan="3">

**Note:** The following role is applicable only to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow customer service.

</td></tr><tr><td>

GRC Employee \[sn\_grc\_emp\_user.grc\_employee\]

</td><td>

Role that is applicable only to customers who are entitled to and have installed the GRC Employee User application from the ServiceNow Store. The users with this role can perform the following activities from Employee Center:

-   Read and acknowledge organizational policies.
-   Report risk events and issues.
-   Request policy exceptions.
-   Report a compliance case to the Compliance team.
-   Raise inquiries or requests to the Compliance team.

</td><td>

 

</td></tr></tbody>
</table>The following Operator roles are reclassified as Lite Operator roles when the GRC Employee User application and GRC Business User Lite applications are installed:

-   sn\_grc.business\_user
-   sn\_risk\_advanced.ara\_assessor
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.reader
-   sn\_irm\_cont\_auth.executive\_read

**Note:** This reclassification is applicable only to customers who are entitled to and have installed the GRC Employee User application. For more details, review the entitlement on the subscription dashboard or contact ServiceNow customer service.

**Parent Topic:**[Governance, Risk, and Compliance reference](../concept/grc-reference.md)

