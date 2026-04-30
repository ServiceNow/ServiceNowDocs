---
title: Manage default related items list
description: You can add or remove items from the default list of related items which is used in duplicate CI remediation for all de-duplication tasks.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage default related items list

You can add or remove items from the default list of related items which is used in duplicate CI remediation for all de-duplication tasks.

## Before you begin

Role required: itil\_admin

## About this task

The default related items list is used by the Duplicate CI Remediator, appearing on the **Merge Relationships and Related Items** tab. You can modify the list for only a specific task in the Duplicate CI Remediator without affecting the default global list.

The default related items list is also used by the [De-duplication dashboard](../concept/dedup-ci-exp-cmdb-workspace.md) in CMDB Workspaceand in Service Graph Workspace for remediation.

Globally modifying the list affects the remediation of all de-duplication tasks in the Duplicate CI Remediatorand in the De-duplication dashboard in CMDB Workspaceand in Service Graph Workspace.

**Note:** Only related items in which the reference field points to Configuration Item \[cmdb\_ci\] in **sys\_dictionary** can be selected for the default related items list. Related items with references to any child of the Configuration Item class cannot be selected for the default related items list, but are still available for merging in the Duplicate CI Remediator for a specific task.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Duplicate CI Remediator Default Related Items**.

2.  On the Default Related Items List for Duplicate CI Remediator page, use the list collector to add or remove items from the **Selected** list.

3.  Click **Save**.


**Parent Topic:**[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

