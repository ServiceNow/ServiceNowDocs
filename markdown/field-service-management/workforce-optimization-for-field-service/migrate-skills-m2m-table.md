---
title: Migrate skills to the Task Skill table
description: Migrate data from the Skills field to the Task Skills table to utilize mandatory skills support for executing tasks in a case or work order.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mandatory skills, Manage skills, Users, Set up workforce, Configure, Field Service Management]
---

# Migrate skills to the Task Skill table

Migrate data from the **Skills** field to the Task Skills table to utilize mandatory skills support for executing tasks in a case or work order.

## Before you begin

Role required: wm\_admin, admin

## About this task

The Task Skills \[task\_m2m\_skill\] table stores skills and mandatory skills.

In the Customer Service Management application, the assignment workbench uses the Task Skills table instead of the **Skills** field in the Case table to display agents based on the evaluation criteria for task assignments.

In the Field Service Management application, the work order task assignments done using auto-assignment, dynamic scheduling, and Dispatcher Workspace use the Task Skills table instead of the **Skills** field in the Work Order and Work Order Task tables to assign agents for task assignments.

## Procedure

1.  [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md) with the following settings.

<table id="choicetable_i5b_yht_wcb"><thead><tr><th align="left" id="d59545e84">

Option

</th><th align="left" id="d59545e87">

Description

</th></tr></thead><tbody><tr><td id="d59545e93">

**Create a system property for a table in the Customer Service Management application.**

</td><td>

Make sure that you are logged in to the Customer Service Management application.

**Note:** Configure the System Properties form to display the **Suffix** field.

In the **Suffix** field, enter the name of the system property as follows:**com.snc.skills\_management.&lt;table\_name&gt;\_migrate\_skills**, where &lt;table\_name&gt; is the name of a case task table from which the skills need to be copied.

</td></tr><tr><td id="d59545e118">

**Create a system property for a table in the Field Service Management application.**

</td><td>

Make sure that you are logged in to the Global application.

In the **Name** field, enter the name of the system property in the following format:**com.snc.skills\_management.&lt;table\_name&gt;\_migrate\_skills**, where &lt;table name&gt; is the name of a work order or work order task table from which the skills need to be copied.

</td></tr></tbody>
</table>2.  In the **Type** field, set the value to **true**.

3.  Click **Update**.

4.  Navigate to **System Definition** &gt; **Fix Scripts** and run the **Migrate Skills to Task Skill M2M** fix script.

    The skills are copied to the task\_m2m\_skill table. The name of the table from which the skills are copied gets appended to the **com.snc.skills\_management.task\_skill\_migrated\_tables** system property. When the script is run again, it ignores all tables from which skills have already been migrated.


