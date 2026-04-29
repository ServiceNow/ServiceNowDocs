---
title: Data Certification experience in CMDB Workspace and in Service Graph Workspace
description: Use Data Certification in CMDB Workspace or in Service Graph Workspace to administer Data Certification, create certification policies, manage certification tasks, and view analytics about on-going processes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Certification experience in CMDB Workspaceand in Service Graph Workspace

Use Data Certification in CMDB Workspace or in Service Graph Workspace to administer Data Certification, create certification policies, manage certification tasks, and view analytics about on-going processes.

## Use Data Certification in CMDB Workspaceand in Service Graph Workspace

Use the [CMDB Workspace](cmdb-workspace.md)or Service Graph Workspace landing page and views to administer Data Certification:

-   Use the [Management view in CMDB Workspace](cmdb-workspace-mangmnt-view.md) to navigate to CMDB Data Manager to [create a new Certification policy](../task/data-manager-create-policy-wrkspc.md).
-   Use the My work tile on the CMDB Workspace landing page to access your open and overdue certification tasks that you need to review and process.
-   Use the [My Work view in CMDB Workspace](cmdb-workspace-govern-view.md) to access any certification tasks assigned to you under the Certification tasks section.
-   Use the [Governance view in Service Graph Workspace](sg-workspace-governance-view.md) to navigate to CMDB Data Manager to [create a new Certification policy](../task/data-manager-create-policy-wrkspc.md).
-   Use the [Tasks view in Service Graph Workspace](sg-workspace-tasks-view.md) to access any certification tasks assigned to you and certification instances that you own.

Manage certification tasks in CMDB Workspaceand in Service Graph Workspace:

-   [Manage Data Certification instances and tasks, and see progress, status, and insights in the Data Certification Dashboard](data-cert-dashboard-workspace.md)
-   [Review certification tasks in CMDB Workspace](../task/data-certific-review-tasks.md)
-   [Review failed certification tasks](../task/data-review-failed-tasks.md)

## Retention of Data Certification records

Archival and destroy processes of certification policy related records, are separate from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records. Retaining certification policy execution records for longer periods of time is useful in situations where those records are needed for audits and is also useful for the Data Certification Dashboard, which is populated by these records.

The following configurations facilitate the separation of retention policies for Data Certification records:

-   The table cleanup rule for the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table, which is stored in the Auto Flushes \[sys\_auto\_flush\] table, excludes certification policy execution records from recurring cleanups.
-   The Archive CMDB Data Management Tasks archive rule, that applies to all CMDB Data Manager policy execution records, excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table \(Archive Related Records\).
-   The archive rule, Archive Certification Instances, archives certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
-   The archive rule, Archive Certification tasks, archives the certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task\] table. This archive rule also contains an Archive Related Records entry that archives the related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table.

