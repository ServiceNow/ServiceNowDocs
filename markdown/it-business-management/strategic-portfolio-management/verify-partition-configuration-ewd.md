---
title: Verify partition configuration
description: Verify that partitions are configured correctly by impersonating users with different partition roles and checking that record visibility is enforced across all workspaces.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-portfolio-management/verify-partition-configuration-ewd.html
release: zurich
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 2
keywords: [partition verification, impersonate user, partition roles, record visibility, enterprise-wide deployment]
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Verify partition configuration

Verify that partitions are configured correctly by impersonating users with different partition roles and checking that record visibility is enforced across all workspaces.

## Before you begin

-   You have completed all partition configuration steps:
    -   Partitions created and partition criteria configured for all supported tables. For details, see [Create and configure a partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/create-partition-ewd.md).
    -   Partition roles are assigned to the relevant users or user groups. For details, see [Assign partition role for access to the partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/assign-partition-role-ewd.md).
-   You have access to impersonate users in the system.
-   Test records exist in the supported tables for each partition — for example, projects and demands created for both IT Operations and HR Learning and Development departments.

Role required: admin

## Procedure

1.  Impersonate a user assigned to the first partition role and confirm workspace visibility.

    For example, impersonate a user assigned the `it_ops` role for the IT Operations partition.

    1.  Open **Project Workspace** and confirm that only records from the user's partition are visible in list views, search results, and dashboards.

        Only IT Operations projects and demands are visible. No records from other partitions, such as HR Learning and Development, appear.

2.  Stop impersonating, then impersonate a user assigned to a different partition role and repeat the workspace checks.

    For example, impersonate a user assigned the `hr_ld` role for the HR Learning and Development partition.

    Only HR Learning and Development records are visible. No IT Operations records appear in any workspace, list view, search result, or dashboard.

3.  Stop impersonating, then impersonate a user assigned to roles for multiple partitions and confirm workspace visibility.

    For example, impersonate a portfolio lead who has both the `it_ops` and `hr_ld` roles assigned.

    1.  Open **Project Workspace** and confirm that records from all the user's assigned partitions are visible in a single view, with no duplication.

4.  Stop impersonating, then impersonate a user with the EWD PMO \[sn\_spm\_ewd.ewd\_pmo\] role.

    1.  Open **Project Workspace** and confirm that records from all partitions are visible, regardless of department.


## Result

Partition configuration is complete when all of the following conditions are met:

-   Users see only the records belonging to their assigned partition across all supported views and tables.
-   Users assigned to multiple partitions see records from all their assigned partitions, with no duplication.
-   Users with the EWD PMO role have visibility across all partitions.

