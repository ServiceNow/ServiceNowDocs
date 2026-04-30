---
title: Manually create a de-duplication task
description: Manually create a de-duplication task when it is not automatically created. You can then use the Duplicate CI Remediator or the De-duplication dashboard in CMDB Workspace and in Service Graph Workspace to remediate the manually created task.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manually create a de-duplication task

Manually create a de-duplication task when it is not automatically created. You can then use the Duplicate CI Remediator or the De-duplication dashboard in CMDB Workspaceand in Service Graph Workspace to remediate the manually created task.

In some situations, duplicate CIs are not automatically detected and de-duplication tasks are not automatically generated. Such situation happens with a class for which identification rules are not defined and the identification engine cannot be applied. However, you still want to reconcile these duplicate CIs by utilizing the [Duplicate CI Remediator](../task/reconcile-dup-task.md)or the [De-duplication dashboard](dedup-ci-exp-cmdb-workspace.md) in CMDB Workspaceor in Service Graph Workspace.

Use the [CMDBDuplicateTaskUtils](https://www.servicenow.com/docs/access?context=CMDBDuplicateTaskUtilsAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) API to manually create a de-duplication task in which all duplicate CIs are specified. The de-duplication tasks that you create manually and the automatically created tasks, are stored in the same table \(\[reconcile\_duplicate\_task\]\) and are processed in the same manner.

**Note:** You can manually create a de-duplication task only for CMDB CIs and a CI can be specified as a duplicate CI only in a single de-duplication task.

**Parent Topic:**[Duplicate CIs remediation](de-duplication-tasks.md)

