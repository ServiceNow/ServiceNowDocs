---
title: Data Certification
description: Data Certification manages scheduled and on-demand validations of data in CMDB and non-CMDB tables.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
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

You can use the [CMDB Workspace](../../configuration-management/concept/cmdb-workspace.md)or Service Graph Workspace landing page and its views to fully administer and use Data Certification, view various analytics, and handle Data Certification functions such as:

-   [Create a certification policy](../../configuration-management/task/data-manager-create-policy-wrkspc.md).
-   [Convert legacy certification schedules into Data Manager certification policies](../../configuration-management/task/convert-data-cert-definitions.md).
-   [Review certification tasks](../../configuration-management/task/data-certific-review-tasks.md).
-   [Review failed certification tasks](../../configuration-management/task/data-review-failed-tasks.md).

The Data Certification experience in CMDB Workspace doesn’t provide functionality such as reset, merging of multiple certification tasks, and escalation.

For more information about using Data Certification in CMDB Workspace, see [Data Certification experience in CMDB Workspace and in Service Graph Workspace](../../configuration-management/concept/data-cert-exp-cmdb-workspace.md).

## Data Certification on Core UI \(UI 16\)

[Data Certification experience in CMDB Workspace and in Service Graph Workspace](../../configuration-management/concept/data-cert-exp-cmdb-workspace.md) provides the latest Data Certification functionality. However, the legacy build of Data Certification on Core UI \(UI 16\) is available by navigating to **All** &gt; **Data Certification**. For information about using the CMDB Data Manager legacy build on Core UI, see [Data Certification on Core UI](../../configuration-management/concept/data-certification-legacy.md).

**Note:**

Data Certification in CMDB Workspace and the legacy build of Data Certification on Core UI operate separately, and aren't synchronized. Therefore, any Data Certification elements, such as definitions and schedules, that you create in one of those implementations, doesn't appear and isn't included in the other implementation.

To convert data created in the legacy build of Data Certification on Core UI, into draft Certification policies in CMDB Workspace, see [Convert legacy certification schedules into Data Manager certification policies](../../configuration-management/task/convert-data-cert-definitions.md).

