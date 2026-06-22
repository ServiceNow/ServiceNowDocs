---
title: Assign partition role for access to the partition
description: Assign a partition role to users or user groups to grant them access to records within a specific partition.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-portfolio-management/assign-partition-role-ewd.html
release: zurich
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Assign partition role for access to the partition

Assign a partition role to users or user groups to grant them access to records within a specific partition.

## Before you begin

-   The partition and its associated role have been created and partition criteria have been configured for all supported tables. For details, see [Create and configure a partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/create-partition-ewd.md).
-   You have identified the users or user groups that should have access to the partition. If you want to create a specific user group for the partition you want to provide access to, create a user group. For details, see [Creating groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/user-administration/ua-creating-groups.md).

Role required: admin

## About this task

Role assignments determine what each user can see at runtime. Users assigned a partition role see only the records from their department's partition. Users assigned roles for multiple partitions see records from all their assigned partitions in a single view, with no duplication or data merging.

For example, assigning the `it_ops` partition role to a user means they see only IT Operations projects, demands, and related records. Assigning both the `it_ops` and `hr_ld` partition roles to a user such as a portfolio lead means they see records from both the partitions.

## Procedure

1.  Navigate to the **All** &gt; **User Administration** &gt; **Users**.

    A list of users appear.

2.  Search for and open the user record to whom you want to assign the partition role.

3.  On the user record, select the Roles related list and select **Edit**.

4.  In the **Collection** list, select the desired partition role\(s\), and then select **Add**.

    For example, search for and add the `it_ops` role to assign Dennis Jackson access to the IT Operations partition. Search for and add the `hr_ld` role to assign John Smith access to the HR Learning and Development partition.

5.  Select **Save** to update the configuration.

    The partition role is assigned to the user. The user can now access only the records that belong to their assigned partition across all workspaces and all tables in scope.

6.  Repeat steps 2 through 5 for each user or user group that requires access to this partition.


## What to do next

-   Grant the EWD PMO \[sn\_spm\_ewd.ewd\_pmo\] role to users who require visibility across all partitions, such as PMO leads and portfolio managers who need enterprise-wide access across all functions. For details, see [Assign PMO role for visibility across all partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/assign-pmo-roles-for-visibility-across-all-partitions.md).
-   Verify that the role assignment is working correctly by impersonating the user and confirming that record visibility matches the expected access level for the assigned role. For details, see [Verify partition configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/verify-partition-configuration-ewd.md).

