---
title: Turn off workflows of related tables during remediation
description: Configure de-duplication remediation processes for related tables, to turn off the execution of business rules, workflows, and any other automatic processes that might be turning off the update of referenced duplicate CIs to the main CI. Disabling all these workflows of related tables, allow de-duplication tasks, that would otherwise fail, to complete.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Turn off workflows of related tables during remediation

Configure de-duplication remediation processes for related tables, to turn off the execution of business rules, workflows, and any other automatic processes that might be turning off the update of referenced duplicate CIs to the main CI. Disabling all these workflows of related tables, allow de-duplication tasks, that would otherwise fail, to complete.

## About this task

Related tables \(tables that reference CIs\), might have for example, business rules that prevent the update of the referenced CI to the main CI during duplicate CI remediation. You can configure remediation processes to turn off all automated processes for specific tables, and by doing so, to allow remediation processes to complete. For example, ignore errors and skip ALL business rules, in such related tables. Those settings are stored in the De-duplication Related Table Configurations \[reconcile\_duplicate\_related\_table\_config\] table.

Each record in the reconcile\_duplicate\_related\_table\_config table represents a table with references to CIs. Settings in the De-duplication Related Table Configurations table are in effect during the processing of de-duplication tasks, but only if the system property **glide.duplicate\_ci\_remediator.merge\_related\_items\_enhanced** is **true** \(default value\). In the base system, the De-duplication Related Table Configurations table contains records for the Change \[change\_request\] and the Task CI \[task\_ci\] related tables, which are configured to skip business rules and ignore database errors.

Add records to the De-duplication Related Table Configurations table to configure additional related tables for which you'd like to skip business rules and/or ignore database errors during de-duplication remediation.

For more information about the **glide.duplicate\_ci\_remediator.merge\_related\_items\_enhanced** property or the De-duplication Related Table Configurations \[reconcile\_duplicate\_related\_table\_config\] table, see [Properties related to remediation of duplicate CIs](../reference/properties-duplicate-ci.md) and [Components installed for duplicate CI remediation](../reference/components-installed-with-dup-ci.md).

## Before you begin

Role required: cmdb\_dedup\_admin

## Procedure

1.  Select **All** and then, in the navigation filter enter `reconcile_duplicate_related_table_config.list` to open the De-duplication Related Table Configurations table.

2.  Select **New** and fill out the following fields on the De-duplication Related Table Configurations table form:

<table id="table_g3k_tnw_5gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table Name

</td><td>

Table with references to CI for which settings apply during de-duplication remediation processes.

</td></tr><tr><td>

Disable workflow

</td><td>

Disable the execution of all business rules, workflows, and any other automatic processes for the specified table during remediation.

</td></tr><tr><td>

Proceed with errors

</td><td>

Skip any database errors for the specified table, during de-duplication remediation processes.

</td></tr><tr><td>

Conditions for disabling workflow

</td><td>

Conditions that restricts the application of settings only to those records in **Table Name** that meet the condition.

 For example, in the base system, the change\_request table is configured with the condition 'state is not New'. Therefore, when updating the change\_request table during the remediation process, business rules are skipped only for those records in which 'state is not New'.

</td></tr></tbody>
</table>3.  Select **Submit**.


## What to do next

When configuring de-duplication remediation, you select which tables to include when merging related items. If any table that you select in that configuration step, has a record in the De-duplication Related Table Configurations table to disable workflow, an alert appears. Review that alert carefully, re-examine business rules and other automated processes to confirm your intention of disabling workflows for the respective table.

**Parent Topic:**[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

