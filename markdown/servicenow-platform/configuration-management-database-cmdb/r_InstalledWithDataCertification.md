---
title: Installed With Data Certification
description: Activating the Data Certification plugin installs the following components.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Activate Data Certification, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Installed With Data Certification

Activating the Data Certification plugin installs the following components.

Demo data is available with Data Certification. The demo data provides information including filters, schedules, instances, and tasks.

## Tables

Data Certification adds the following tables:

|Table|Description|
|-----|-----------|
|Certification Audit Definition \[cert\_audit\_definition\]|Stores collections of certification schedules that can be run as a single entity.|
|Certification Audit Definition Elements \[m2m\_cert\_audit\_def\_cert\_sched\]|Lists the certification schedules in each certification audit definition.|
|Certification Audit Instance \[cert\_audit\_instance\]|Stores the certification instances associated with a specific audit definition.|
|Certification Element \[cert\_element\]|Stores the data elements that are grouped into certification tasks.|
|Certification Filter \[cert\_filter\]|Stores the data that requires certification using a filtering condition for the certification.|
|Certification Instance \[cert\_instance\]|Stores a collection of certification tasks representing a single instance of a scheduled certification. This table extends the Audit \[cert\_audit\] table.|
|Certification Schedule \[cert\_schedule\]|Stores certification for a specific set of information on a specific table, what user or group the tasks are assigned to, and how often this certification is done.|
|Certification Task \[cert\_task\]|Stores individual certification tasks. Certification Task extends the Task table.|

## Script Includes

Data Certification adds the following script includes:

|Name|Description|
|----|-----------|
|CertificationAjax|Provides utilities that enable individual certification elements to be certified, rejected, or reverted.|
|CertificationTaskCreate|Custom code that extends the standard code for certification tasks.|
|CertTaskEscalationTimerPercentage|Updates time and percentage complete information for a certification.|
|CertificationUtilities|Provides utility functions for certification.|

## Client Scripts

Data Certification adds the following client scripts:

|Name|Table|Description|
|----|-----|-----------|
|Alert If Boxes Checked|Certification Task \[cert\_task\]|Provides a warning if the certifier attempts to leave a record without certifying the checked elements|
|Check Table Name|Certification Schedule \[cert\_schedule\]|Updates the table name when a different filter is selected.|

## UI Policies

Data Certification adds the following UI policies:

|Name|Table|Description|
|----|-----|-----------|
|Hide next scheduled run|Certification Schedule \[cert\_schedule\]|Hides the Next Scheduled Run field when the schedule is set to run once or on demand only.|
|Hide Run When Not Active|Certification Schedule \[cert\_schedule\]|Hide "run" associated fields when active is set to false.|
|Make table name read only|Certification Schedule \[cert\_schedule\]|Makes the Table field read-only.|
|Hide Table field|Certification Element \[cert\_element\]|Hides the Table field on the certification task form.|
|Make percent complete field read only|Certification Instance \[cert\_instance\]|Makes the Percent complete field read only when the State is Work in Progress, Closed Complete, Closed Incomplete, or Cancelled.|
|Show Assign to fields|Certification Schedule \[cert\_schedule\]|Shows the Assign To field when the assignment type is User and hides the Assign To field for all other assignment types.|
|Show Group field|Certification Schedule \[cert\_schedule\]|Shows the **Change Group** \(formerly Assignment Group\) field when the assignment type is Group and hides the **Change Group** field for all other assignment types.|
|Show User field|Certification Schedule \[cert\_schedule\]|Shows the User field when the assignment type is User.|
|Show Assignment Fields|Certification Schedule \[cert\_schedule\]|Shows the Assign To Empty option when the assignment type is User Field or Group Field.|

## Business Rules

Data Certification adds the following business rules:

|Name|Table|Description|
|----|-----|-----------|
|Adjust dates for cert tasks|Certification Instance \[cert\_instance\]|Adjusts dates for tasks belonging to the certification instance when the dates are changed for an active certification.|
|Cancel Instance|Certification Instance \[cert\_instance\]|Cancels all open certification tasks when an active certification is canceled.|
|certification audit instance events|Certification Audit Instance \[cert\_audit\_instance\]|Sends an inserted event when an active certification audit instance is created. Sends a completed event when an active certification audit instance is marked as complete or incomplete.|
|certification element events|Certification Element \[cert\_element\]|Sends a failed event when an element of a certification is marked as failed.|
|certification instance events|Certification Instance \[cert\_instance\]|Sends an inserted event when an instance of a certification is created. Sends a completed event when an instance of a certification is completed.|
|Certification Instance Rollup|Certification Task \[cert\_task\]|Updates the Percent complete field on the certification instance record.|
|certification task events|Certification Task \[cert\_task\]|Sends an inserted event when a task is inserted. Sends a completed event when a task is deactivated. Sends a canceled event when a task is canceled.|
|Certification Task Values|Certification Element \[cert\_element\]|Updates the percent complete of the parent task when a certification element is updated.|
|Check Certification Audit Progress|Certification Instance \[cert\_instance\]|Updates the completion status of the audit instance as a whole when a certification that is part of an audit is complete.|
|Clean Certification Views|Certification Instance \[cert\_instance\]|Cleans all related records when a certification instance is deleted.|
|Copy certification schedule fields|Certification Instance \[cert\_instance\]|Copies changes to the certification schedule to the certification instance.|
|Merge Certification Tasks|Certification Task \[cert\_task\]|Merges two tasks together when a task is reassigned and there is another task for the same instance with the new user.|
|Prevent delete of Filter with Schedule|Certification Filter \[cert\_filter\]|Prevents the deletion of a filter that is used in a schedule.|
|Reassign Notification|Certification Task \[cert\_task\]|Sends out a notification to the new and previous assignees when a task is reassigned.|
|Rollup State|Certification Task \[cert\_task\]|Updates all necessary parent items when task state is changed.|
|Update audit reference|Certification Task \[cert\_task\]|Makes Data Certification records compatible with Desired State records. This rule makes sure that the Audit field is correctly completed when a record is inserted using Insert and Stay.|
|Update audit result|Certification Element \[cert\_element\]|Makes Data Certification records compatible with Desired State records for reporting purposes. This rule puts certified values in the Desired value column when an audit is Certified. It also puts actual values in the Discrepancy value column when an audit is Failed.|
|Update follow\_on\_task &amp; audit references|Certification Element \[cert\_element\]|Makes Data Certification records compatible with Desired State records for reporting purposes. This rule makes certification tasks compatible with follow-on tasks and displays all tasks, regardless of origin.|
|Update next run time|Certification Schedule \[cert\_schedule\]|Updates the Next scheduled run field when a schedule runs Daily, Weekly, Monthly, or Periodically.|
|Verify Fields|Certification Schedule \[cert\_schedule\]|Verifies that no field is used in both Display and Certification fields when the fields of a certification schedule are changed.|

## Formatter

Data Certification adds the following formatter:

|Name|Description|
|----|-----------|
|Certification Task Elements|Enables custom user interface formatting of elements on a certification task. For example, displays the green check mark and red exclamation point to use when certifying an element.|

## Properties

<table id="table_tpx_kyz_sp"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.cert\_task\_activity.fields

</td><td>

System Properties \[sys\_properties\]

</td><td>

Defines which journal field is the task activity field. Default: work\_notes

</td></tr></tbody>
</table>## User Roles

Data Certification adds the following user roles:

<table id="table_qbm_pyz_sp"><thead><tr><th>

Role

</th><th>

Contains Roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

certification\_admin

</td><td>

certification

</td><td>

Can:-   Create and configure certifications
-   Override provided answers
-   Perform certification tasks for certification task owners
-   Send certification task notifications to users and owners at any time
-   Cancel or delete certifications in any state

</td></tr><tr><td>

certification\_filter\_admin

</td><td>

certification

</td><td>

Can create and manage all data certification filters.

</td></tr><tr><td>

certification

</td><td>

none

</td><td>

Can update active or incomplete tasks assigned to them or to groups of which they are a member. Can also update configuration items owned by them or by groups of which they are a member. Receives email notifications when assigned certification tasks.

</td></tr></tbody>
</table>## Events

Data Certification adds the following events. The ServiceNow system uses these events to send email notifications to task owners and managers about changes in certification records.

|Name|Description|
|----|-----------|
|cert\_audit\_instance.completed|A certification audit instance has been completed.|
|cert\_audit\_instance.inserted|A certification audit instance has been inserted.|
|cert\_element.failed|A certification element has failed certification.|
|cert\_instance.complete|A certification instance has been completed.|
|cert\_instance.inserted|A certification instance has been inserted.|
|cert\_task.cancelled|A certification task has been canceled.|
|cert\_task.completed|A certification task has been completed.|
|cert\_task.escalate|A certification task record has been escalated.|
|cert\_task.inserted|A new certification task has been created.|
|cert\_task.notifications|A certification task notification has been resent to a user.|
|cert\_task.overdue|A certification task is past its specified completion date.|
|cert\_task.reassign|A certification task has been reassigned.|
|cert\_task.warning|A new task escalation point has been reached.|

## Email Templates

Data Certification adds the following email templates:

|Name|Message|
|----|-------|
|certification.task.cancelled|A certification task assigned to you/your group as part of the data certification and management process has been canceled.|
|certification.task.reminder.inserted|A certification task that has been assigned to you/your group as part of the data certification and management process requires attention.|
|certification.task.reminder.outstanding|A certification task that has been assigned to you/your group as part of the data certification and management process requires attention.|
|certification.task.reminder.overdue|A certification task that has been assigned to you/your group as part of the data certification and management process is overdue.|

