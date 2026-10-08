---
title: Modify a Planned Task Interceptor
description: Customize the Planned Task Interceptor to control what type of planned task record users can create and what choices they see when creating new planned tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/table-administration-and-data-management/t\_CreateAPlannedTask.html
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Planned tasks, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Modify a Planned Task Interceptor

Customize the Planned Task Interceptor to control what type of planned task record users can create and what choices they see when creating new planned tasks.

## Before you begin

The Project Management plugin must be activated. For more information, see [Extending the Task table with Planned tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/table-administration-and-data-management/c_PlannedTask.md).

Role required: admin.

## About this task

An Interceptor helps decide what type of record should be created when it isn't clear what the correct record type is. The Interceptor prompts users to make additional choices that determine the correct type of record.

By default, the Planned Task Interceptor prompts users to choose whether a new planned task is a planned project task, or a planned project. The answers can be modified or added to as needed.

\[Omitted image "PTaskInterceptor.png"\] Alt text: Planned Task Interceptor, asking "What type of Planned Task would you like to create?" Options include "Project" or "Project Task."

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Interceptors**.

2.  Select the **Planned Task** Interceptor.

3.  Modify the **Answers** related list as desired.

    The **Answers** related list specifies what choices are presented, and where the user is redirected after selecting the choice. You can modify the preexisting answer records, or use **New** to create an answer based on what kind of prompt you want to give the user.

    You can modify answers by adding scripts. For more information about scripting in the ServiceNow AI Platform, see [Scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_Script.md).

    \[Omitted image "PTaskInterceptor2.png"\] Alt text: Planned task form, displaying the Answers related list with Project and Project Task answer options.


**Parent Topic:**[Extending the Task table with Planned tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/table-administration-and-data-management/c_PlannedTask.md)

