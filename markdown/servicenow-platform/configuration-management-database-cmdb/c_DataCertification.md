---
title: Data Certification
description: Data Certification manages scheduled and on-demand validations of data in CMDB and non-CMDB tables.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data Certification

Data Certification manages scheduled and on-demand validations of data in CMDB and non-CMDB tables.

Information is added to the CMDB by Discovery, by importing from third-party tools, or manually. For regulatory or procedural reasons, information in the CMDB requires checks for accuracy and certification. The person or team responsible for certification can define what information requires verification and the frequency of verification. Using CMDB Data Manager supports policy-driven validation of specific attributes using the certification policy type. CMDB Data Manager generates certification tasks for verifying the data on a recurring schedule, which then, individuals assigned to those tasks answer a series of questions to verify the data.

Use Data Certification to:

-   Maintain the accuracy, completeness, and reliability of critical data in both, CMDB and non-CMDB tables.
-   Create a framework for ongoing data compliance, regulatory, governance, and operational standards.

Data certification can be performed against specific fields on specific tables. Based on the certification schedule, certification tasks are automatically created and assigned. A certification task represents the work of verifying the data associated with a particular record. For example, you can set up a certification to validate key information fields, such as **Operating System** and **CPU count**, on all Windows servers located in Chicago. You can then assign the tasks to the appropriate team member automatically.

When planning an implementation of Data Certification, answer the following questions:

-   What information requires certification?
-   When is the due date for certification?
-   Who must perform the certification?

Domain separated systems can use the Data Certification application.

## Data Certification experience in CMDB Workspaceand in Service Graph Workspace

You can use [CMDB Workspace](../../configuration-management/concept/cmdb-workspace.md)or Service Graph Workspace landing page and views to fully administer and use Data Certification, view various analytics, and handle Data Certification functions such as:

-   [Create a certification policy](../../configuration-management/task/data-manager-create-policy-wrkspc.md).
-   [Convert legacy certification schedules into Data Manager certification policies](../../configuration-management/task/convert-data-cert-definitions.md).
-   [Review certification tasks](../../configuration-management/task/data-certific-review-tasks.md).
-   [Review failed certification tasks](../../configuration-management/task/data-review-failed-tasks.md).

The Data Certification experience in CMDB Workspace doesn’t provide functionality such as reset, merging of multiple certification tasks, and escalation.

For more information about using Data Certification, see [Data Certification experience in CMDB Workspace and in Service Graph Workspace](../../configuration-management/concept/data-cert-exp-cmdb-workspace.md).

