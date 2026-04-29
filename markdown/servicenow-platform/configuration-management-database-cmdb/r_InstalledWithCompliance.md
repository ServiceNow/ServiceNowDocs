---
title: Installed with Compliance
description: These components are installed with the Certification Core plugin.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Installed with Compliance

These components are installed with the Certification Core plugin.

Demo data is included with the Desired State and Architecture Compliance plugins.

The Certification Core plugin adds or modifies these tables.

<table id="table_dms_wcr_3q"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audit \[cert\_audit\]

</td><td>

Contains all the data required to run an audit, including the users assigned to follow-on tasks and the run schedule.

</td></tr><tr><td>

Audit Result \[cert\_audit\_result\]

</td><td>

Contains the results of specific, certification audits.

</td></tr><tr><td>

Follow On Task \[cert\_follow\_on\_task\]

</td><td>

Contains the tasks that were generated from an audit discrepancy.

</td></tr><tr><td>

Certification Template \[cert\_template\]

</td><td>

Contains the definition of the desired state of the record. The template includes a filter that identifies the records to evaluate and the expected attributes and relationship values.

 Contains the records to certify, the expected attributes, and the expected relationship values.

</td></tr><tr><td>

Certification Condition \[cert\_cond\]

</td><td>

Base table that defines the desired attribute or relationship conditions used in templates.

</td></tr><tr><td>

Certification Attribute Condition \[cert\_attr\_cond\]

</td><td>

Contains the conditions that define the desired CI attribute values. This table extends the Certification Condition \[cert\_cond\] base table.

</td></tr><tr><td>

Certification CI Relationship Condition \[cert\_ci\_rel\_cond\]

</td><td>

Contains the CI to CI relationship conditions. This table extends the Certification Condition \[cert\_cond\] base table.

</td></tr><tr><td>

Certification User Relationship Condition \[cert\_user\_rel\_cond\]

</td><td>

Contains the CI to user relationship conditions. This table extends the Certification Condition \[cert\_cond\] base table.

</td></tr><tr><td>

Certification Group Relationship Condition \[cert\_group\_rel\_cond\]

</td><td>

Contains the CI to group relationship conditions. This table extends the Certification Condition \[cert\_cond\] base table.

</td></tr><tr><td>

Certification Related List Condition \[cert\_related\_list\_cond\]

</td><td>

Contains the related list conditions. This table extends the Certification Condition \[cert\_cond\] base table.

</td></tr><tr><td>

Certification Filter \[cert\_filter\]

</td><td>

Contains a certification filter, including the table that contains the records to audit and the filter conditions.

</td></tr></tbody>
</table>## User roles

The certification role is automatically assigned to all users with the itil role when the [Certification Core plugin](../concept/c_ActivatingCompliance.md) is activated or when compliance applications are upgraded. Certification core installs two business rules, both called **Add Certification Role To Manager**, that perform similar tasks on different tables. One rule checks for a manager specified on the User \[sys\_user\] table, and the other checks for the certification role on the User Role \[sys\_user\_has\_role\] table. When both a manager and the certification role are specified for a user, the system automatically grants the certification role to the manager. This functionality ensures that a certification task can be escalated successfully to the next level. The system grants this automatic role to the user's immediate manager only and not to others up the management chain.

**Note:** When a manager has only the certification role and no other role, the manager is considered a Requester and is not counted as a subscribed user \(Fulfiller\).

|Name|Contains roles|Description|
|----|--------------|-----------|
|certification|none|Can read and update certification tasks to resolve discrepancies.|
|certification\_filter\_admin|none|Can create, read, and update certification filters.|
|certification\_admin|certification, certification\_filter\_admin|Can manage the entire certification process. These users can create, edit, and delete all certification records.|

## UI policies

<table id="table_x3w_hfr_3q"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Make table read only

</td><td>

Audit \[cert\_audit\]

</td><td>

Sets the table field derived from the selected filter to read-only.

</td></tr><tr><td>

Hide Audit Type

</td><td>

Audit \[cert\_audit\]

</td><td>

Hides the Audit type field.

</td></tr><tr><td>

Hide next scheduled run

</td><td>

Audit \[cert\_audit\]

</td><td>

Hides the Next scheduled run date when an audit is inactive or on-demand.

</td></tr><tr><td>

Show task fields when create tasks is set to true

</td><td>

Audit \[cert\_audit\]

</td><td>

Displays all fields related to creating tasks when the user selects the Create tasks check box.

</td></tr><tr><td>

Make name mandatory

</td><td>

Audit \[cert\_audit\]

</td><td>

Makes Name a mandatory field.

</td></tr><tr><td>

Prevent editing of Last run date

</td><td>

Audit \[cert\_audit\]

</td><td>

Makes Last run date field read-only.

</td></tr><tr><td>

Show User field

</td><td>

Audit \[cert\_audit\]

</td><td>

Shows or hides fields based on the Assignment type selected. The system shows the User field when you select the following assignment types:-   User Field if the Assign to empty option is Create Assigned Task.
-   Specific User

</td></tr><tr><td>

Show Assign to fields

</td><td>

Audit \[cert\_audit\]

</td><td>

Shows or hides fields based on the Assignment type selected. The system shows the Assign to field when the assignment type is User Field.

</td></tr><tr><td>

Show Assignment Fields

</td><td>

Audit \[cert\_audit\]

</td><td>

Shows or hides fields based on the Assignment type selected. The system shows the Assign to empty field when you select either of the following assignment types:-   User Field
-   Group Field

</td></tr><tr><td>

Show Group field

</td><td>

Audit \[cert\_audit\]

</td><td>

Shows or hides fields based on the Assignment type selected. The system shows the Group field when you select either of the following assignment types:-   Specific Group
-   Group Field if the Assign to empty option is Create Assigned Task.

</td></tr><tr><td>

Hide "run" associated fields when active is set to false

</td><td>

Audit \[cert\_audit\]

</td><td>

Hides these scheduling fields when the audit is inactive:-   Run
-   Day
-   Time
-   Last scheduled run

</td></tr><tr><td>

Show script window on Scripted Audit

</td><td>

Audit \[cert\_audit\]

</td><td>

Displays the Run this script field when the audit type is Scripted.

</td></tr><tr><td>

Make table read only

</td><td>

Certification Condition \[cert\_cond\]

</td><td>

Sets the table field derived from the selected filter to read-only.

</td></tr></tbody>
</table>## Script includes

|Name|Description|
|----|-----------|
|DesiredStateUtil|Utility functions for desired state, used to clone a template for Insert functionality.|
|CMDBRElationshipAjax|Tool to get all relationships for a given table.|
|RelationshipQueryParseAjax|Parses condition filters. This script include is the internal code used in generating the compliance conditions.|
|CertificationUtils|Utility functions for certification that find Next run time value, and so on.|
|CertTaskEscalationTimerPercentage|Utility method for setting escalation timer durations.|
|ConditionUtilsAjax|AJAX utilities for parsing queries into a human-readable format.|
|DeleteInactiveVersionsAjax|AJAX server-side script to delete all inactive versions of a record.|

## Client scripts

|Name|Table|Description|
|----|-----|-----------|
|Make audit type read only if not new|Certification Template \[cert\_template\]|Sets the correct audit type for new records, and if the record is not new, sets the Audit type field to read only.|
|Update table name \(filter\)|Audit \[cert\_audit\]|Updates the table Name field when the filter is updated.|
|Update table name|Audit \[cert\_audit\]|Updates the table Name field when the template is updated.|
|Set table name on new|Audit \[cert\_audit\]|Returns the table name from the template or filter.|
|Update table name|Certification Template \[cert\_template\]|Updates the table Name field when a new filter is chosen and checks all existing conditions to see if they work for the new table.|
|Show conditions when table is set|Certification Template \[cert\_template\]|Shows and hides conditions appropriately when the table is set.|
|Reset filter when audit type changes|Certification Template \[cert\_template\]|Clears the filter and updates the lists shown when the audit type is changed.|

## Business rules

|Name|Table|Description|
|----|-----|-----------|
|Clone condition|Certification Condition \[cert\_cond\]|Part of certification versioning. This business rule retains the original ID when a condition is changed.|
|Copy audit type from audit|Audit Result \[cert\_audit\_result\]|Ensures that all audit results have the same audit type as the audit that generated them.|
|Copy values from template|Audit \[cert\_audit\]|When a user selects a template, and updates the table, filter, and audit type from the template.|
|Delete condition|Certification Condition \[cert\_cond\]|Part of certification versioning that deletes a condition.|
|Prevent deletion of audit with results|Audit \[cert\_audit\]|Prevents deletion of an audit containing results.|
|Prevent delete of Filter with Template|Certification Filter \[cert\_filter\]|Prevents deletion of a filter still linked to a template or audit.|
|Prevent deletion of result with task|Audit Result \[cert\_audit\_result\]|Prevents deletion of an audit result with an attached task.|
|Prevent delete of Template with Audit|Certification Template \[cert\_template\]|Prevents deletion of a template still being used by an audit.|
|Update conditions' tables|Certification Template \[cert\_template\]|When storing template conditions, properly run all workflows and update the condition fields to contain the display version of the conditions.|
|Update filter version|Certification Filter \[cert\_filter\]|Creates a version when the filter changes in any meaningful way.|
|Update next run time|Audit \[cert\_audit\]|Updates the time in the Next scheduled run field when an audit is modified.|
|Update next run time during execution|Audit \[cert\_audit\]|When the audit runs, update the Next scheduled run field to the next time the audit is scheduled to run.|
|Update table|Certification Template \[cert\_template\]|Update the stored table to the table of the filter.|
|Update template version|Certification Template \[cert\_template\]|Creates a version when the template changes in any meaningful way.|

