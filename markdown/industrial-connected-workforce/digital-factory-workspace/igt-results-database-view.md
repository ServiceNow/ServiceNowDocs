---
title: Industrial Guided Task Result database view
description: The Industrial Guided Task Result \[sn\_icw\_igt\_results\] database view combines the question responses of each IGT task with the operational context of the task. This enables you to report on individual question results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/igt-results-database-view.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-09-25"
reading_time_minutes: 3
keywords: [Industrial Guided Tasks, database view, question results, reporting]
breadcrumb: [Industrial Guided Tasks, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Industrial Guided Task Result database view

The Industrial Guided Task Result \[sn\_icw\_igt\_results\] database view combines the question responses of each IGT task with the operational context of the task. This enables you to report on individual question results.

## How the view works

The view joins Assessment Question Instance \[sn\_smart\_asmt\_question\_instance\] records with Industrial Guided Task \[sn\_icw\_igt\_task\] records that share the same assessment instance. Each row in the view is one question response in one task. You can report on question results by functional location, equipment, standard, or shift without exporting and combining data from several tables.

The view includes only question responses that belong to an IGT task.

The view is installed with the Industrial Guided Tasks application. Users with the ICW Report User \[sn\_icw.report\_user\] role can use the view as the source for reports. For information about database views, see [Working with database views for reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DatabaseViews.md).

## Industrial Guided Task fields

The following fields come from the Industrial Guided Task \[sn\_icw\_igt\_task\] table. In the view, their column names start with the prefix `igt_`.

|Field \[column name\]|Description|
|---------------------|-----------|
|Number \[igt\_number\]|Number of the task.|
|State \[igt\_state\]|State of the task. For more information, see [Industrial Guided Task standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/industrial-guided-task-life-cycle.md).|
|Functional location \[igt\_business\_service\]|Functional location of the task.|
|Equipment \[igt\_cmdb\_ci\]|Equipment for the task.|
|Location \[igt\_location\]|Location of the task.|
|Standard \[igt\_standard\]|IGT standard that the task was created from.|
|Due date \[igt\_due\_date\]|Date by which the task must be completed.|
|Planned start shift \[igt\_planned\_start\_shift\]|Shift in which the task is planned to start.|
|Planned end shift \[igt\_planned\_end\_shift\]|Shift in which the task is planned to end.|
|Assessment instance \[igt\_assessment\_instance\]|Assessment instance that holds the question responses for the task and joins tasks to their responses.|
|Sys ID \[igt\_sys\_id\]|Unique identifier of the task record.|

## Question response fields

The following fields come from the Assessment Question Instance \[sn\_smart\_asmt\_question\_instance\] table. In the view, their column names start with the prefix `response_`.

Each response type is stored in its own field. For a given question, only the field that matches the question type contains the answer. For example, the answer to a numeric question is in the **Number response** field.

|Field \[column name\]|Description|
|---------------------|-----------|
|Assessment question \[response\_assessment\_question\]|Question from the IGT standard that was answered.|
|Assessment instance \[response\_assessment\_instance\]|Assessment instance that the response belongs to.|
|Number response \[response\_number\_response\]|Answer to a numeric question.|
|Text response \[response\_text\_response\]|Answer to a text question.|
|Date response \[response\_date\_response\]|Answer to a date question.|
|Date time response \[response\_date\_time\_response\]|Answer to a date and time question.|
|Reference response \[response\_reference\_response\_record\]|Record selected as the answer to a reference question.|
|Selected response options \[response\_selected\_response\_options\]|Options selected as the answer to a choice question.|
|Comments \[response\_comments\]|Comments entered with the response.|
|Justification \[response\_justification\]|Justification entered with the response.|
|Last responded on \[response\_last\_responded\_on\]|Date and time when the question was last answered.|
|Is responded \[response\_is\_responded\]|Whether the question has been answered.|
|Sys ID \[response\_sys\_id\]|Unique identifier of the question response record.|

**Parent Topic:**[Industrial Guided Tasks reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/industrial-guided-tasks-reference.md)

**Related topics**  


[Create a report on IGT question results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/create-report-igt-question-results.md)

