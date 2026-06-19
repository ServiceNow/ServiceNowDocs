---
title: Assign PMO role for visibility across all partitions
description: Grant users or user groups access to partitioned records in Enterprise-Wide Deployment by assigning the appropriate EWD PMO role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-portfolio-management/assign-pmo-roles-for-visibility-across-all-partitions.html
release: australia
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Configure, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Assign PMO role for visibility across all partitions

Grant users or user groups access to partitioned records in Enterprise-Wide Deployment by assigning the appropriate EWD PMO role.

## Before you begin

Role required: admin

## About this task

You can assign the EWD PMO \[sn\_spm\_ewd.ewd\_pmo\] role to individual users or user groups. Applying this role to a group grants access to all members of that group. The role grants edit access to the data across all partitions regardless of the assigned partition role. This is intended for PMO users who require enterprise-wide visibility across all functions.

**Important:** Assign the EWD PMO role only to users who need cross-partition access, as it grants visibility to data across all partitions. This role does not replace base role requirements. Users must still have the appropriate base roles — for example, it\_project\_manager — to access projects and related records.

For more information on roles installed with Enterprise-Wide Deployment, see the Roles table in [Components installed with Enterprise-Wide Deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/components-installed-with-ewd.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Search for the user record or user group to which you want to assign the EWD PMO \(sn\_spm\_ewd.ewd\_pmo\) role.

3.  In the Roles related list, select **Edit**.

4.  In the **Collection** list, select the required EWD PMO role — **sn\_spm\_ewd.ewd\_pmo** and then select **Add**.

5.  Select **Save**.

    The selected EWD PMO role is assigned to the user or user group. The user can access partitioned records according to the permissions of the assigned role.


## What to do next

Verify that the role assignment is working correctly by impersonating the user and confirming that record visibility matches the expected access level for the assigned role. For details, see [Verify partition configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/verify-partition-configuration-ewd.md).

